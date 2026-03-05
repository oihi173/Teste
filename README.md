-- Wild Horse Islands - Matte Hub
-- UI Customizada + Farm de Pontos

local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local TweenService = game:GetService("TweenService")
local UIS = game:GetService("UserInputService")

local plr = Players.LocalPlayer
local char = plr.Character or plr.CharacterAdded:Wait()
local hrp = char:WaitForChild("HumanoidRootPart")

-- ========== KEY SYSTEM ==========
local keyDono = "lolmagode"
local keyUsuario = tostring(16 + 16)
local keyValida = false

-- ========== CORES E ESTILO ==========
local COR_FUNDO      = Color3.fromRGB(18, 18, 24)
local COR_PAINEL     = Color3.fromRGB(24, 24, 32)
local COR_HEADER     = Color3.fromRGB(30, 30, 42)
local COR_TAB        = Color3.fromRGB(35, 35, 48)
local COR_TAB_ATIVA  = Color3.fromRGB(88, 66, 255)
local COR_BOTAO      = Color3.fromRGB(40, 40, 58)
local COR_BOTAO_HOV  = Color3.fromRGB(55, 55, 78)
local COR_TOGGLE_ON  = Color3.fromRGB(88, 66, 255)
local COR_TOGGLE_OFF = Color3.fromRGB(55, 55, 78)
local COR_TEXTO      = Color3.fromRGB(220, 220, 235)
local COR_SUBTEXTO   = Color3.fromRGB(140, 140, 165)
local COR_SLIDER     = Color3.fromRGB(88, 66, 255)
local COR_SECTION    = Color3.fromRGB(88, 66, 255)

-- ========== GUI PRINCIPAL ==========
local gui = Instance.new("ScreenGui")
gui.Name = "MatteHub"
gui.ResetOnSpawn = false
gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
gui.Parent = plr.PlayerGui

-- ========== HELPERS ==========
local function makeCorner(parent, radius)
    local c = Instance.new("UICorner")
    c.CornerRadius = UDim.new(0, radius or 8)
    c.Parent = parent
    return c
end

local function makePadding(parent, t, b, l, r)
    local p = Instance.new("UIPadding")
    p.PaddingTop = UDim.new(0, t or 6)
    p.PaddingBottom = UDim.new(0, b or 6)
    p.PaddingLeft = UDim.new(0, l or 8)
    p.PaddingRight = UDim.new(0, r or 8)
    p.Parent = parent
end

local function makeLabel(parent, text, size, color, bold)
    local l = Instance.new("TextLabel")
    l.Text = text
    l.TextSize = size or 13
    l.TextColor3 = color or COR_TEXTO
    l.Font = bold and Enum.Font.GothamBold or Enum.Font.Gotham
    l.BackgroundTransparency = 1
    l.TextXAlignment = Enum.TextXAlignment.Left
    l.Size = UDim2.new(1, 0, 0, size and size + 6 or 20)
    l.Parent = parent
    return l
end

local function tween(obj, props, t)
    TweenService:Create(obj, TweenInfo.new(t or 0.15, Enum.EasingStyle.Quad), props):Play()
end

-- ========== BOTÃO FLUTUANTE (IMAGEM) ==========
local imgBtn = Instance.new("ImageButton")
imgBtn.Size = UDim2.new(0, 55, 0, 55)
imgBtn.Position = UDim2.new(0, 15, 0.5, -27)
imgBtn.BackgroundTransparency = 1
imgBtn.Image = "rbxassetid://86993464589982"
imgBtn.ZIndex = 100
imgBtn.Parent = gui

-- Arrastar imagem
local dragging, dragStart, startPos, moveu = false, nil, nil, false

imgBtn.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
        dragging = true
        moveu = false
        dragStart = input.Position
        startPos = imgBtn.Position
    end
end)

imgBtn.InputEnded:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
        dragging = false
    end
end)

UIS.InputChanged:Connect(function(input)
    if dragging and (input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch) then
        local delta = input.Position - dragStart
        if delta.Magnitude > 5 then moveu = true end
        imgBtn.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
    end
end)

-- ========== PAINEL PRINCIPAL ==========
local painelAberto = false
local painelFrame = Instance.new("Frame")
painelFrame.Size = UDim2.new(0, 420, 0, 480)
painelFrame.Position = UDim2.new(0.5, -210, 0.5, -240)
painelFrame.BackgroundColor3 = COR_PAINEL
painelFrame.BorderSizePixel = 0
painelFrame.Visible = false
painelFrame.ZIndex = 50
painelFrame.Parent = gui
makeCorner(painelFrame, 12)

-- Sombra
local shadow = Instance.new("ImageLabel")
shadow.Size = UDim2.new(1, 30, 1, 30)
shadow.Position = UDim2.new(0, -15, 0, -15)
shadow.BackgroundTransparency = 1
shadow.Image = "rbxassetid://5554236805"
shadow.ImageColor3 = Color3.fromRGB(0,0,0)
shadow.ImageTransparency = 0.5
shadow.ZIndex = 49
shadow.ScaleType = Enum.ScaleType.Slice
shadow.SliceCenter = Rect.new(23,23,277,277)
shadow.Parent = painelFrame

-- Arrastar painel
local dragPanel, dragPanelStart, dragPanelPos = false, nil, nil
local header = Instance.new("Frame")
header.Size = UDim2.new(1, 0, 0, 60)
header.BackgroundColor3 = COR_HEADER
header.BorderSizePixel = 0
header.ZIndex = 51
header.Parent = painelFrame
makeCorner(header, 12)

-- Cobrir cantos inferiores do header
local headerBottom = Instance.new("Frame")
headerBottom.Size = UDim2.new(1, 0, 0, 12)
headerBottom.Position = UDim2.new(0, 0, 1, -12)
headerBottom.BackgroundColor3 = COR_HEADER
headerBottom.BorderSizePixel = 0
headerBottom.ZIndex = 51
headerBottom.Parent = header

-- Imagem no header
local headerImg = Instance.new("ImageLabel")
headerImg.Size = UDim2.new(0, 40, 0, 40)
headerImg.Position = UDim2.new(0, 12, 0.5, -20)
headerImg.BackgroundTransparency = 1
headerImg.Image = "rbxassetid://86993464589982"
headerImg.ZIndex = 52
headerImg.Parent = header

-- Título
local titulo = Instance.new("TextLabel")
titulo.Text = "Matte Hub"
titulo.TextSize = 18
titulo.Font = Enum.Font.GothamBold
titulo.TextColor3 = COR_TEXTO
titulo.BackgroundTransparency = 1
titulo.Position = UDim2.new(0, 62, 0, 8)
titulo.Size = UDim2.new(1, -110, 0, 22)
titulo.TextXAlignment = Enum.TextXAlignment.Left
titulo.ZIndex = 52
titulo.Parent = header

-- Subtítulo
local subtitulo = Instance.new("TextLabel")
subtitulo.Text = "Wild Horse Islands Farm"
subtitulo.TextSize = 11
subtitulo.Font = Enum.Font.Gotham
subtitulo.TextColor3 = COR_SUBTEXTO
subtitulo.BackgroundTransparency = 1
subtitulo.Position = UDim2.new(0, 62, 0, 32)
subtitulo.Size = UDim2.new(1, -110, 0, 16)
subtitulo.TextXAlignment = Enum.TextXAlignment.Left
subtitulo.ZIndex = 52
subtitulo.Parent = header

-- Botão fechar
local btnFechar = Instance.new("TextButton")
btnFechar.Text = "✕"
btnFechar.TextSize = 16
btnFechar.Font = Enum.Font.GothamBold
btnFechar.TextColor3 = COR_SUBTEXTO
btnFechar.BackgroundTransparency = 1
btnFechar.Position = UDim2.new(1, -40, 0, 10)
btnFechar.Size = UDim2.new(0, 30, 0, 30)
btnFechar.ZIndex = 52
btnFechar.Parent = header

-- Arrastar pelo header
header.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        dragPanel = true
        dragPanelStart = input.Position
        dragPanelPos = painelFrame.Position
    end
end)
header.InputEnded:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        dragPanel = false
    end
end)
UIS.InputChanged:Connect(function(input)
    if dragPanel and input.UserInputType == Enum.UserInputType.MouseMovement then
        local delta = input.Position - dragPanelStart
        painelFrame.Position = UDim2.new(dragPanelPos.X.Scale, dragPanelPos.X.Offset + delta.X, dragPanelPos.Y.Scale, dragPanelPos.Y.Offset + delta.Y)
    end
end)

-- Abrir/fechar
local function togglePainel()
    painelAberto = not painelAberto
    if painelAberto then
        painelFrame.Visible = true
        painelFrame.Size = UDim2.new(0, 420, 0, 0)
        tween(painelFrame, {Size = UDim2.new(0, 420, 0, 480)}, 0.2)
    else
        tween(painelFrame, {Size = UDim2.new(0, 420, 0, 0)}, 0.15)
        task.delay(0.15, function() painelFrame.Visible = false end)
    end
end

imgBtn.InputEnded:Connect(function(input)
    if (input.UserInputType == Enum.UserInputType.MouseButton1 or
        input.UserInputType == Enum.UserInputType.Touch) and not moveu then
        if not keyValida then
            keyFrame.Visible = true
        else
            togglePainel()
        end
    end
end)
btnFechar.MouseButton1Click:Connect(function()
    togglePainel()
end)

-- ========== TABS ==========
local tabBar = Instance.new("Frame")
tabBar.Size = UDim2.new(1, 0, 0, 38)
tabBar.Position = UDim2.new(0, 0, 0, 60)
tabBar.BackgroundColor3 = COR_FUNDO
tabBar.BorderSizePixel = 0
tabBar.ZIndex = 51
tabBar.Parent = painelFrame

local tabLayout = Instance.new("UIListLayout")
tabLayout.FillDirection = Enum.FillDirection.Horizontal
tabLayout.SortOrder = Enum.SortOrder.LayoutOrder
tabLayout.Padding = UDim.new(0, 2)
tabLayout.Parent = tabBar
makePadding(tabBar, 5, 5, 6, 6)

-- Conteúdo
local conteudo = Instance.new("ScrollingFrame")
conteudo.Size = UDim2.new(1, 0, 1, -100)
conteudo.Position = UDim2.new(0, 0, 0, 100)
conteudo.BackgroundColor3 = COR_PAINEL
conteudo.BorderSizePixel = 0
conteudo.ScrollBarThickness = 3
conteudo.ScrollBarImageColor3 = COR_TAB_ATIVA
conteudo.CanvasSize = UDim2.new(0, 0, 0, 0)
conteudo.AutomaticCanvasSize = Enum.AutomaticSize.Y
conteudo.ZIndex = 51
conteudo.Parent = painelFrame
makePadding(conteudo, 8, 8, 10, 10)

local conteudoLayout = Instance.new("UIListLayout")
conteudoLayout.SortOrder = Enum.SortOrder.LayoutOrder
conteudoLayout.Padding = UDim.new(0, 6)
conteudoLayout.Parent = conteudo

-- Tabs e páginas
local tabs = {}
local paginas = {}
local tabAtiva = nil

local function criarTab(nome, icone)
    local btn = Instance.new("TextButton")
    btn.Text = icone .. " " .. nome
    btn.TextSize = 11
    btn.Font = Enum.Font.GothamBold
    btn.TextColor3 = COR_SUBTEXTO
    btn.BackgroundColor3 = COR_TAB
    btn.BorderSizePixel = 0
    btn.Size = UDim2.new(0.24, -2, 1, 0)
    btn.AutoButtonColor = false
    btn.ZIndex = 52
    btn.Parent = tabBar
    makeCorner(btn, 6)

    local pagina = Instance.new("Frame")
    pagina.Size = UDim2.new(1, 0, 0, 0)
    pagina.BackgroundTransparency = 1
    pagina.AutomaticSize = Enum.AutomaticSize.Y
    pagina.Visible = false
    pagina.ZIndex = 51
    pagina.Parent = conteudo

    local pLayout = Instance.new("UIListLayout")
    pLayout.SortOrder = Enum.SortOrder.LayoutOrder
    pLayout.Padding = UDim.new(0, 6)
    pLayout.Parent = pagina

    table.insert(tabs, btn)
    table.insert(paginas, pagina)
    local idx = #tabs

    btn.MouseButton1Click:Connect(function()
        for i, t in ipairs(tabs) do
            tween(t, {BackgroundColor3 = COR_TAB, TextColor3 = COR_SUBTEXTO}, 0.1)
            paginas[i].Visible = false
        end
        tween(btn, {BackgroundColor3 = COR_TAB_ATIVA, TextColor3 = COR_TEXTO}, 0.1)
        pagina.Visible = true
        tabAtiva = idx
    end)

    return pagina
end

-- ========== COMPONENTES UI ==========
local function addSection(pagina, texto)
    local f = Instance.new("Frame")
    f.Size = UDim2.new(1, 0, 0, 22)
    f.BackgroundTransparency = 1
    f.ZIndex = 52
    f.Parent = pagina

    local linha = Instance.new("Frame")
    linha.Size = UDim2.new(0, 3, 1, 0)
    linha.BackgroundColor3 = COR_SECTION
    linha.BorderSizePixel = 0
    linha.ZIndex = 52
    linha.Parent = f
    makeCorner(linha, 2)

    local lbl = Instance.new("TextLabel")
    lbl.Text = texto
    lbl.TextSize = 12
    lbl.Font = Enum.Font.GothamBold
    lbl.TextColor3 = COR_SECTION
    lbl.BackgroundTransparency = 1
    lbl.Position = UDim2.new(0, 10, 0, 0)
    lbl.Size = UDim2.new(1, -10, 1, 0)
    lbl.TextXAlignment = Enum.TextXAlignment.Left
    lbl.ZIndex = 52
    lbl.Parent = f
end

local function addLabel(pagina, texto)
    local lbl = Instance.new("TextLabel")
    lbl.Text = texto
    lbl.TextSize = 12
    lbl.Font = Enum.Font.Gotham
    lbl.TextColor3 = COR_SUBTEXTO
    lbl.BackgroundTransparency = 1
    lbl.Size = UDim2.new(1, 0, 0, 18)
    lbl.TextXAlignment = Enum.TextXAlignment.Left
    lbl.ZIndex = 52
    lbl.Parent = pagina

    local obj = {}
    function obj:Set(t) lbl.Text = t end
    return obj
end

local function addButton(pagina, texto, cb)
    local btn = Instance.new("TextButton")
    btn.Text = texto
    btn.TextSize = 12
    btn.Font = Enum.Font.GothamBold
    btn.TextColor3 = COR_TEXTO
    btn.BackgroundColor3 = COR_BOTAO
    btn.BorderSizePixel = 0
    btn.Size = UDim2.new(1, 0, 0, 34)
    btn.AutoButtonColor = false
    btn.ZIndex = 52
    btn.Parent = pagina
    makeCorner(btn, 7)

    btn.MouseEnter:Connect(function() tween(btn, {BackgroundColor3 = COR_BOTAO_HOV}, 0.1) end)
    btn.MouseLeave:Connect(function() tween(btn, {BackgroundColor3 = COR_BOTAO}, 0.1) end)
    btn.MouseButton1Click:Connect(function()
        tween(btn, {BackgroundColor3 = COR_TAB_ATIVA}, 0.05)
        task.delay(0.15, function() tween(btn, {BackgroundColor3 = COR_BOTAO}, 0.1) end)
        cb()
    end)
end

local function addToggle(pagina, texto, default, cb)
    local f = Instance.new("Frame")
    f.Size = UDim2.new(1, 0, 0, 34)
    f.BackgroundColor3 = COR_BOTAO
    f.BorderSizePixel = 0
    f.ZIndex = 52
    f.Parent = pagina
    makeCorner(f, 7)

    local lbl = Instance.new("TextLabel")
    lbl.Text = texto
    lbl.TextSize = 12
    lbl.Font = Enum.Font.Gotham
    lbl.TextColor3 = COR_TEXTO
    lbl.BackgroundTransparency = 1
    lbl.Position = UDim2.new(0, 10, 0, 0)
    lbl.Size = UDim2.new(1, -60, 1, 0)
    lbl.TextXAlignment = Enum.TextXAlignment.Left
    lbl.ZIndex = 53
    lbl.Parent = f

    local track = Instance.new("Frame")
    track.Size = UDim2.new(0, 40, 0, 20)
    track.Position = UDim2.new(1, -50, 0.5, -10)
    track.BackgroundColor3 = default and COR_TOGGLE_ON or COR_TOGGLE_OFF
    track.BorderSizePixel = 0
    track.ZIndex = 53
    track.Parent = f
    makeCorner(track, 10)

    local knob = Instance.new("Frame")
    knob.Size = UDim2.new(0, 16, 0, 16)
    knob.Position = default and UDim2.new(1, -18, 0.5, -8) or UDim2.new(0, 2, 0.5, -8)
    knob.BackgroundColor3 = Color3.fromRGB(255,255,255)
    knob.BorderSizePixel = 0
    knob.ZIndex = 54
    knob.Parent = track
    makeCorner(knob, 8)

    local valor = default or false
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(1, 0, 1, 0)
    btn.BackgroundTransparency = 1
    btn.Text = ""
    btn.ZIndex = 55
    btn.Parent = f

    btn.MouseButton1Click:Connect(function()
        valor = not valor
        tween(track, {BackgroundColor3 = valor and COR_TOGGLE_ON or COR_TOGGLE_OFF}, 0.15)
        tween(knob, {Position = valor and UDim2.new(1,-18,0.5,-8) or UDim2.new(0,2,0.5,-8)}, 0.15)
        cb(valor)
    end)

    local obj = {}
    function obj:Set(v)
        valor = v
        tween(track, {BackgroundColor3 = v and COR_TOGGLE_ON or COR_TOGGLE_OFF}, 0.15)
        tween(knob, {Position = v and UDim2.new(1,-18,0.5,-8) or UDim2.new(0,2,0.5,-8)}, 0.15)
    end
    return obj
end

local function addSlider(pagina, texto, min, max, default, cb)
    local f = Instance.new("Frame")
    f.Size = UDim2.new(1, 0, 0, 52)
    f.BackgroundColor3 = COR_BOTAO
    f.BorderSizePixel = 0
    f.ZIndex = 52
    f.Parent = pagina
    makeCorner(f, 7)
    makePadding(f, 6, 6, 10, 10)

    local row = Instance.new("Frame")
    row.Size = UDim2.new(1, 0, 0, 18)
    row.BackgroundTransparency = 1
    row.ZIndex = 53
    row.Parent = f

    local lbl = Instance.new("TextLabel")
    lbl.Text = texto
    lbl.TextSize = 12
    lbl.Font = Enum.Font.Gotham
    lbl.TextColor3 = COR_TEXTO
    lbl.BackgroundTransparency = 1
    lbl.Size = UDim2.new(0.7, 0, 1, 0)
    lbl.TextXAlignment = Enum.TextXAlignment.Left
    lbl.ZIndex = 53
    lbl.Parent = row

    local valLbl = Instance.new("TextLabel")
    valLbl.Text = tostring(default)
    valLbl.TextSize = 12
    valLbl.Font = Enum.Font.GothamBold
    valLbl.TextColor3 = COR_SLIDER
    valLbl.BackgroundTransparency = 1
    valLbl.Size = UDim2.new(0.3, 0, 1, 0)
    valLbl.Position = UDim2.new(0.7, 0, 0, 0)
    valLbl.TextXAlignment = Enum.TextXAlignment.Right
    valLbl.ZIndex = 53
    valLbl.Parent = row

    local track = Instance.new("Frame")
    track.Size = UDim2.new(1, 0, 0, 6)
    track.Position = UDim2.new(0, 0, 0, 26)
    track.BackgroundColor3 = COR_FUNDO
    track.BorderSizePixel = 0
    track.ZIndex = 53
    track.Parent = f
    makeCorner(track, 3)

    local fill = Instance.new("Frame")
    fill.Size = UDim2.new((default - min)/(max - min), 0, 1, 0)
    fill.BackgroundColor3 = COR_SLIDER
    fill.BorderSizePixel = 0
    fill.ZIndex = 54
    fill.Parent = track
    makeCorner(fill, 3)

    local valor = default
    local sliding = false

    local hitbox = Instance.new("TextButton")
    hitbox.Size = UDim2.new(1, 0, 0, 20)
    hitbox.Position = UDim2.new(0, 0, 0, 18)
    hitbox.BackgroundTransparency = 1
    hitbox.Text = ""
    hitbox.ZIndex = 56
    hitbox.Parent = f

    local function updateSlider(inputPos)
        local abs = track.AbsolutePosition
        local sz = track.AbsoluteSize
        local pct = math.clamp((inputPos.X - abs.X) / sz.X, 0, 1)
        valor = math.floor(min + pct * (max - min))
        valLbl.Text = tostring(valor)
        fill.Size = UDim2.new(pct, 0, 1, 0)
        cb(valor)
    end

    hitbox.InputBegan:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 then
            sliding = true
            updateSlider(input.Position)
        end
    end)
    hitbox.InputEnded:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 then sliding = false end
    end)
    UIS.InputChanged:Connect(function(input)
        if sliding and input.UserInputType == Enum.UserInputType.MouseMovement then
            updateSlider(input.Position)
        end
    end)
end

-- ========== KEY SYSTEM UI ==========
local keyFrame = Instance.new("Frame")
keyFrame.Size = UDim2.new(0, 340, 0, 200)
keyFrame.Position = UDim2.new(0.5, -170, 0.5, -100)
keyFrame.BackgroundColor3 = COR_PAINEL
keyFrame.BorderSizePixel = 0
keyFrame.ZIndex = 200
keyFrame.Visible = true
keyFrame.Parent = gui
makeCorner(keyFrame, 12)

local keyTitulo = Instance.new("TextLabel")
keyTitulo.Text = "🔑 Matte Hub - Key System"
keyTitulo.TextSize = 15
keyTitulo.Font = Enum.Font.GothamBold
keyTitulo.TextColor3 = COR_TEXTO
keyTitulo.BackgroundTransparency = 1
keyTitulo.Position = UDim2.new(0, 0, 0, 16)
keyTitulo.Size = UDim2.new(1, 0, 0, 22)
keyTitulo.ZIndex = 201
keyTitulo.Parent = keyFrame

local keySub = Instance.new("TextLabel")
keySub.Text = "Dono: key secreta | Usuários: resolva 16+16"
keySub.TextSize = 11
keySub.Font = Enum.Font.Gotham
keySub.TextColor3 = COR_SUBTEXTO
keySub.BackgroundTransparency = 1
keySub.Position = UDim2.new(0, 0, 0, 44)
keySub.Size = UDim2.new(1, 0, 0, 16)
keySub.ZIndex = 201
keySub.Parent = keyFrame

local keyBox = Instance.new("TextBox")
keyBox.PlaceholderText = "Digite sua key aqui..."
keyBox.Text = ""
keyBox.TextSize = 13
keyBox.Font = Enum.Font.Gotham
keyBox.TextColor3 = COR_TEXTO
keyBox.PlaceholderColor3 = COR_SUBTEXTO
keyBox.BackgroundColor3 = COR_BOTAO
keyBox.BorderSizePixel = 0
keyBox.Position = UDim2.new(0, 16, 0, 76)
keyBox.Size = UDim2.new(1, -32, 0, 36)
keyBox.ZIndex = 201
keyBox.Parent = keyFrame
makeCorner(keyBox, 7)

local keyErro = Instance.new("TextLabel")
keyErro.Text = ""
keyErro.TextSize = 11
keyErro.Font = Enum.Font.Gotham
keyErro.TextColor3 = Color3.fromRGB(255, 80, 80)
keyErro.BackgroundTransparency = 1
keyErro.Position = UDim2.new(0, 16, 0, 118)
keyErro.Size = UDim2.new(1, -32, 0, 16)
keyErro.ZIndex = 201
keyErro.Parent = keyFrame

local keyBtnConfirm = Instance.new("TextButton")
keyBtnConfirm.Text = "Confirmar"
keyBtnConfirm.TextSize = 13
keyBtnConfirm.Font = Enum.Font.GothamBold
keyBtnConfirm.TextColor3 = COR_TEXTO
keyBtnConfirm.BackgroundColor3 = COR_TAB_ATIVA
keyBtnConfirm.BorderSizePixel = 0
keyBtnConfirm.Position = UDim2.new(0, 16, 0, 148)
keyBtnConfirm.Size = UDim2.new(1, -32, 0, 36)
keyBtnConfirm.AutoButtonColor = false
keyBtnConfirm.ZIndex = 201
keyBtnConfirm.Parent = keyFrame
makeCorner(keyBtnConfirm, 7)

keyBtnConfirm.MouseButton1Click:Connect(function()
    local input = keyBox.Text
    if input == keyDono or input == keyUsuario th
