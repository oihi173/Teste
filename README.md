--[[ Protected by Lua Guard ]]

( function (...) local Players = game:GetService("\080\108\097\121\101\114\115") local RunService = game:GetService("\082\117\110\083\101\114\118\105\099\101") local TweenService = game:GetService("\084\119\101\101\110\083\101\114\118\105\099\101") local _lIllIllllI = game:GetService("\086\105\114\116\117\097\108\073\110\112\117\116\077\097\110\097\103\101\114") local GuiService = game:GetService("\071\117\105\083\101\114\118\105\099\101") local _lllIIIlIll = Players.LocalPlayer local _IIIIlIIllI = _lllIIIlIll.Character or _lllIIIlIll.CharacterAdded:Wait() local _lIllIIIIIl = _IIIIlIIllI:WaitForChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") local _IIIlllllII = _IIIIlIIllI:WaitForChild("\072\117\109\097\110\111\105\100") local _llIllIlllI = _lllIIIlIll:WaitForChild("\080\108\097\121\101\114\071\117\105") local _IlllIIIlII = loadstring(game:HttpGet("\104\116\116\112\115\058\047\047\115\105\114\105\117\115\046\109\101\110\117\047\114\097\121\102\105\101\108\100"))() local _lIlllIIlIl = _IlllIIIlII:CreateWindow({ Name = "\087\072\073\032\070\097\114\109\032\118\057", LoadingTitle = "\087\072\073\032\070\097\114\109", LoadingSubtitle = "\072\097\108\108\111\119\101\101\110\032\105\110\116\101\103\114\097\100\111", ConfigurationSaving = { Enabled = false }, Discord = { Enabled = false }, KeySystem = false, }) local _IlllllIlIl = false local _IIlIIlIlll = 0x32 local _lIIllIlIIl = 0x2BC local _IIIIlIIlll = 0x3 local _lIIIlIlIIl = false local _llIlllllll = true local _IlIIIllIlI = true local _llIlllIlll = 0x14 local _IllllIIlIl = 0x3 local _IlIlIIlIIl = 0xA local _IllIIlIlII, cavaloConn = nil, nil local _IIlIIlllIl = Vector3.new(3595.69, 0x15, -6875.07) local _IllIIlllII = Vector3.new(3636.73, 0x15, -6899.1) local _lIlIIlIlIl = true local _lIlllIlIII = "\083\105\110\103\108\101\032\083\116\097\107\101" local _IIIIIIIllI = 0x3 local _lIllIlIIIl = false local _lllllIIllI = "\097\117\116\111" local _lIllllIllI = "\097\109\098\111\115" local _llIlIIlIlI = true local _IIIllIIllI = true local _IIIlIIlIIl, AJUSTE_Y = 0x0, 0x0 local _IIlIllIIlI = false local _lllIIIIlII = { cross = { _lIlIlllIll = "\067\114\111\115\115\032\067\111\117\110\116\114\121", _IlIlIIIIlI = Vector3.new(3674.61, 0x15, -7141.42) }, river = { _lIlIlllIll = "\066\101\103\105\110\032\082\105\118\101\114\032\082\117\110", _IlIlIIIIlI = Vector3.new(3708.41, 16.32, -6400.22) }, } local _IIllIIIIlI = 0xA local _lllIIllIIl = 0xF0 local _IlIlIIlIll = 0x7D0 local _IllIIIlIlI, corridaConn, alvoCorrida = false, nil, nil local _IlIllIIlII = Vector3.new(3678.48, 25.5, -7140.38) local _lllIIllllI = Vector3.new(3706.19, 19.86, -6396.1) local _IlIIllIlII = 0x3 local _llIlIlllIl = 0x3 local _llIlllIIII, treinoThread = nil, nil local _IIllIlIlIl, ultimoPulo = 0.3, 0x0 local function _IllIIIIIIl(title, content) if _IIIIlIIlll <= 0x0 then return end
 _IlllIIIlII:Notify({ Title = title, Content = content, Duration = _IIIIlIIlll, Image = nil }) end
 local _llIlIIllll, cLabel, aLabel, cavLabel local function _llIIIIIIlI(lbl, _IllIIIIIII) if lbl then pcall( function () lbl:Set(_IllIIIIIII) end
 ) end
 end
 local _IllIllllll = function () end
 local _lIIIllIlII = function () end
 local _IllllIIlll = function () end
 local _lIIIIlllll = function () end
 local _IlIIlIlllI = function () end
 local _lllllIlIlI = function () end
 local _lIIIlIIlll = { ["\078\111\100\101"]=true,["\083\104\111\112\073\110\116\101\114\097\099\116\105\111\110\080\097\114\116"]=true,["\066\111\117\110\100\115"]=true, ["\067\111\109\112\101\116\105\116\105\118\101\082\097\099\101\083\116\097\109\105\110\097\066\111\111\115\116"]=true,["\067\111\109\112\101\116\105\116\105\118\101\082\097\099\101\083\112\101\101\100\066\111\111\115\116"]=true, ["\066\111\117\110\100"]=true,["\083\108\105\100\101\080\097\114\116"]=true, } local _IlIlIllIII = { ["\067\111\109\112\101\116\105\116\105\118\101\082\097\099\101\073\116\101\109"]=true,["\066\105\108\108\098\111\097\114\100"]=true, ["\087\105\110\100\032\116\117\114\098\105\110\101"]=true,["\082\101\119\097\114\100\080\105\099\107\117\112\078\111\100\101\115"]=true, } local _IlllIIlIIl = { [Enum.Material.Glass]=true,[Enum.Material.ForceField]=true, } local function _lllllIIlll(o) if not o or not o.Parent then return false end
 if not o:IsA("\066\097\115\101\080\097\114\116") then return false end
 if not o:FindFirstChildOfClass("\084\111\117\099\104\084\114\097\110\115\109\105\116\116\101\114") then return false end
 if _lIIIlIIlll[o.Name] then return false end
 if o.Parent and _IlIlIllIII[o.Parent.Name] then return false end
 if _IlllIIlIIl[o.Material] then return false end
 local _IIlIllIIll = o.Name:lower() if _IIlIllIIll:find("\098\111\117\110\100") or _IIlIllIIll:find("\110\111\100\101") or _IIlIllIIll:find("\115\104\111\112") or _IIlIllIIll:find("\098\111\111\115\116") or _IIlIllIIll:find("\115\108\105\100\101") then return false end
 if o.Parent then local _IIlIIIIIIl = o.Parent.Name:lower() if _IIlIIIIIIl:find("\099\111\109\112\101\116\105\116\105\118\101\114\097\099\101") then return false end
 end
 return true end
 local _IIIIIIlIII = {} workspace.DescendantAdded:Connect( function (o) task.defer( function () if _lllllIIlll(o) then _IIIIIIlIII[o] = true end
 end
 ) end
 ) workspace.DescendantRemoving:Connect( function (o) _IIIIIIlIII[o] = nil end
 ) task.spawn( function () for _, o in ipairs(workspace:GetDescendants()) do if _lllllIIlll(o) then _IIIIIIlIII[o] = true end
 end
 end
 ) local function _IIlIIIIIIl() local _IllllllIll, bestDist = nil, math.huge local _lllIIIlllI = _lIllIIIIIl.Position for o in pairs(_IIIIIIlIII) do if o and o.Parent then local _IIllIIIIIl = (_lllIIIlllI - o.Position).Magnitude if _IIllIIIIIl <= _lIIllIlIIl and _IIllIIIIIl < bestDist then bestDist, _IllllllIll = _IIllIIIIIl, o end
 end
 end
 return _IllllllIll end
 local function _lIlIlIIIlI(raio) local _IllllllIll, bestDist = nil, math.huge local _IlIlIIIIlI = _lIllIIIIIl.Position for o in pairs(_IIIIIIlIII) do if o and o.Parent then local _IIllIIIIIl = (_IlIlIIIIlI - o.Position).Magnitude if _IIllIIIIIl <= raio and _IIllIIIIIl < bestDist then bestDist, _IllllllIll = _IIllIIIIIl, o end
 end
 end
 return _IllllllIll end
 local function _lIlIlIIllI() local _IlIIIlIlII, _lllIIIlllI = 0x0, _lIllIIIIIl.Position for o in pairs(_IIIIIIlIII) do if o and o.Parent and (_lllIIIlllI - o.Position).Magnitude <= _lIIllIlIIl then _IlIIIlIlII += 0x1 end
 end
 return _IlIIIlIlII end
 local function _IlllIIlIlI() for _, _IIlIIIIIIl in ipairs(workspace:GetDescendants()) do if _IIlIIIIIIl:IsA("\077\111\100\101\108") and _IIlIIIIIIl ~= _IIIIlIIllI and _IIlIIIIIIl:FindFirstChild("\072\117\109\097\110\111\105\100") and _IIlIIIIIIl:FindFirstChild("\082\111\111\116\080\097\114\116") then if (_IIlIIIIIIl.RootPart.Position - _lIllIIIIIl.Position).Magnitude < 0xF then return _IIlIIIIIIl.RootPart, _IIlIIIIIIl end
 end
 end
 return nil, nil end
 local _lIlIIlIIIl local function _IlIIIlIlIl() if _lIlIIlIIIl then return end
 _lIlIIlIIIl = _lllIIIlIll.Idled:Connect( function () local _IlIIlIIIIl, vu = pcall( function () return game:GetService("\086\105\114\116\117\097\108\085\115\101\114") end
 ) if _IlIIlIIIIl and vu then vu:CaptureController(); vu:ClickButton2(Vector2.new()) end
 end
 ) end
 local function _IIlllIlIll() if _lIlIIlIIIl then _lIlIIlIIIl:Disconnect(); _lIlIIlIIIl = nil end
 end
 local _lIIIllIlIl, flyConn, flyActive = nil, nil, false local function _IlIIIIlIII() local _lIllIIlIII = Instance.new("\080\097\114\116") _lIllIIlIII.Size, _lIllIIlIII.Transparency, _lIllIIlIII.Anchored, _lIllIIlIII.CanCollide = Vector3.new(0x2,0x1,0x2), 0x1, true, false _lIllIIlIII.CFrame, _lIllIIlIII.Parent = _lIllIIIIIl.CFrame, workspace return _lIllIIlIII end
 local function _lIIlIIllII() if flyActive then return end
 flyActive = true _lIIIllIlIl = _IlIIIIlIII() local _IlIlIIIIll = _IIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") if _IlIlIIIIll then _IlIlIIIIll.PlatformStand = true end
 if flyConn then pcall( function () flyConn:Disconnect() end
 ) end
 flyConn = RunService.Heartbeat:Connect( function () if _lIIIllIlIl and _lIIIllIlIl.Parent then _lIllIIIIIl.CFrame = _lIIIllIlIl.CFrame end
 end
 ) end
 local function _IIIlIIIlIl() flyActive = false if flyConn then flyConn:Disconnect(); flyConn = nil end
 if _lIIIllIlIl then _lIIIllIlIl:Destroy(); _lIIIllIlIl = nil end
 for _, o in ipairs(_lIllIIIIIl:GetChildren()) do if o:IsA("\066\111\100\121\086\101\108\111\099\105\116\121") or o:IsA("\066\111\100\121\071\121\114\111") or o:IsA("\066\111\100\121\080\111\115\105\116\105\111\110") then pcall( function () o:Destroy() end
 ) end
 end
 local _IlIlIIIIll = _IIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") if _IlIlIIIIll then _IlIlIIIIll.PlatformStand = false end
 end
 local function _lllIIIIlII(destination) if not _lIIIllIlIl or not _lIIIllIlIl.Parent then return end
 local _llIllllllI = (_lIIIllIlIl.Position - destination).Magnitude if _llIllllllI < 0x1 then return end
 local _lllIlIIIll = TweenService:Create(_lIIIllIlIl, TweenInfo.new(_llIllllllI / _IIlIIlIlll, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), { CFrame = CFrame.new(destination) }) _lllIlIIIll:Play(); _lllIlIIIll.Completed:Wait() end
 local _llIlIIIlIl = nil local function _llllllllll() if _llIlIIIlIl then pcall( function () _llIlIIIlIl:Disconnect() end
 ) end
 _llIlIIIlIl = RunService.Heartbeat:Connect( function () if not _llIlllllll or not flyActive or not _lIIIllIlIl or not _lIIIllIlIl.Parent then return end
 local _lIlIIllIlI = _IIlIIIIIIl() if not _lIlIIllIlI or not _lIlIIllIlI.Parent then return end
 local _IIIIllIIlI = (_lIlIIllIlI.Position - _lIIIllIlIl.Position).Unit _lIIIllIlIl.CFrame = CFrame.new(_lIIIllIlIl.Position, _lIIIllIlIl.Position + _IIIIllIIlI) if _IlIIIllIlI and _lIIIlIlIIl then local _IIIllllIll = _IlllIIlIlI() if _IIIllllIll and _IIIllllIll.Parent and _IllIIlIlII and _IllIIlIlII.Parent then _IllIIlIlII.CFrame = CFrame.new(_IllIIlIlII.Position, _IllIIlIlII.Position + _IIIIllIIlI) end
 end
 end
 ) end
 local function _llIllllIlI() if _llIlIIIlIl then _llIlIIIlIl:Disconnect(); _llIlIIIlIl = nil end
 end
 local function _llIllIIlll() local _lIllIIlIII = Instance.new("\080\097\114\116") _lIllIIlIII.Size, _lIllIIlIII.Transparency, _lIllIIlIII.Anchored, _lIllIIlIII.CanCollide = Vector3.new(0x3,0x2,0x3), 0x1, true, false _lIllIIlIII.CFrame, _lIllIIlIII.Parent = _lIllIIIIIl.CFrame + Vector3.new(0x5,0x0,0x0), workspace return _lIllIIlIII end
 local function _IIlllIlllI() _lIIIlIlIIl = true _IllIIlIlII = _llIllIIlll() if cavaloConn then pcall( function () cavaloConn:Disconnect() end
 ) end
 cavaloConn = RunService.Heartbeat:Connect( function () if _IllIIlIlII and _IllIIlIlII.Parent then local _IIIllllIll = _IlllIIlIlI() if _IIIllllIll and _IIIllllIll.Parent then _IIIllllIll.CFrame = _IllIIlIlII.CFrame end
 end
 end
 ) end
 local function _IlIIlIllII() _lIIIlIlIIl = false if cavaloConn then cavaloConn:Disconnect(); cavaloConn = nil end
 if _IllIIlIlII then _IllIIlIlII:Destroy(); _IllIIlIlII = nil end
 end
 local function _lIllIllIIl(destination) if not _IllIIlIlII or not _IllIIlIlII.Parent then return end
 local _llIllllllI = (_IllIIlIlII.Position - destination).Magnitude if _llIllllllI < 0x1 then return end
 local _lllIlIIIll = TweenService:Create(_IllIIlIlII, TweenInfo.new(_llIllllllI / _IIlIIlIlll, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), { CFrame = CFrame.new(destination) }) _lllIlIIIll:Play(); _lllIlIIIll.Completed:Wait() end
 local function _IllIIlIlll(_lIllIIlIlI) if not _llIlIIlIlI then return end
 pcall( function () _IlllIIIlII:SetVisibility(_lIllIIlIlI) end
 ) end
 local function _IllIIIIlIl(_IlIlIIIIlI) if not (_lIIIllIlIl and _lIIIllIlIl.Parent) then _lIllIIIIIl.CFrame = CFrame.new(_IlIlIIIIlI); task.wait(0.2); return end
 if _lIllIlIIIl then _lIIIllIlIl.CFrame = CFrame.new(_IlIlIIIIlI) if _lIIIlIlIIl and _IllIIlIlII and _IllIIlIlII.Parent then _IllIIlIlII.CFrame = CFrame.new(_IlIlIIIIlI + Vector3.new(0x5,0x0,0x0)) end
 task.wait(0.2) else _lllIIIIlII(_IlIlIIIIlI) if _lIIIlIlIIl and _IllIIlIlII and _IllIIlIlII.Parent then _lIllIllIIl(_IlIlIIIIlI) end
 end
 end
 local function _llIllIlIll(_llllllIlll) local _llIIIIIlll, md = nil, _llllllIlll or 0x1E for _, _lIllIIlIII in ipairs(workspace:GetDescendants()) do if _lIllIIlIII:IsA("\080\114\111\120\105\109\105\116\121\080\114\111\109\112\116") and _lIllIIlIII.Enabled then local _IlllIlIlll, _IlIlIIIIlI = _lIllIIlIII.Parent, nil if _IlllIlIlll and _IlllIlIlll:IsA("\066\097\115\101\080\097\114\116") then _IlIlIIIIlI = _IlllIlIlll.Position elseif _IlllIlIlll and _IlllIlIlll:IsA("\065\116\116\097\099\104\109\101\110\116") then _IlIlIIIIlI = _IlllIlIlll.WorldPosition end
 if _IlIlIIIIlI then local _IIllIIIIIl = (_IlIlIIIIlI - _lIllIIIIIl.Position).Magnitude if _IIllIIIIIl < md then md, _llIIIIIlll = _IIllIIIIIl, _lIllIIlIII end
 end
 end
 end
 return _llIIIIIlll end
 local function _lIIIIlIlII() local _llIlllIlII = _llIllIlIll(0x1E) local _IlIllIllII = false if _llIlllIlII and fireproximityprompt and (_lllllIIllI == "\097\117\116\111" or _lllllIIllI == "\112\114\111\109\112\116" or _lllllIIllI == "\097\109\098\111\115") then pcall(fireproximityprompt, _llIlllIlII) _IlIllIllII = true end
 local _lIIIIlIIIl = _lllllIIllI == "\116\101\099\108\097" or _lllllIIllI == "\097\109\098\111\115" or (_lllllIIllI == "\097\117\116\111" and not _IlIllIllII) if _lIIIIlIIIl then local _lIIlllllll = (_llIlllIlII and _llIlllIlII.HoldDuration) or 0x0 _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.E, false, game) task.wait(math.max(_lIIlllllll, 0x0) + 0.15) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.E, false, game) end
 end
 local function _llIllIllll(_lIlIlllIll) local _IIIlIlIIll = _llIllIlllI:FindFirstChild("\080\114\111\109\112\116\115") return (_IIIlIlIIll and _IIIlIlIIll:FindFirstChild(_lIlIlllIll, true)) or _llIllIlllI:FindFirstChild(_lIlIlllIll, true) end
 local function _IllIlllIIl(_lIIIlIIllI) local _lIllIIIIlI = _lIIIlIIllI while _lIllIIIIlI and _lIllIIIIlI ~= _llIllIlllI do if _lIllIIIIlI:IsA("\071\117\105\079\098\106\101\099\116") and not _lIllIIIIlI.Visible then return false end
 if _lIllIIIIlI:IsA("\083\099\114\101\101\110\071\117\105") and not _lIllIIIIlI.Enabled then return false end
 _lIllIIIIlI = _lIllIIIIlI.Parent end
 return _lIIIlIIllI.AbsoluteSize.X > 0x0 end
 local function _lIIllIlIII(_lIlIlllIll, tempo) local _llllllIlll = os.clock() + (tempo or 0xF) while os.clock() < _llllllIlll do local _lIIIlIIllI = _llIllIllll(_lIlIlllIll) if _lIIIlIIllI and _IllIlllIIl(_lIIIlIIllI) then return _lIIIlIIllI end
 task.wait(0.25) end
 end
 local function _IIllIllIll(_lIIIlIIllI) local _IIlIlIllIl = _lIIIlIIllI.Parent if _IIlIlIllIl and _IIlIlIllIl:IsA("\083\099\114\111\108\108\105\110\103\070\114\097\109\101") then local _lllIIlIlIl = _lIIIlIIllI.AbsolutePosition.Y - _IIlIlIllIl.AbsolutePosition.Y + _IIlIlIllIl.CanvasPosition.Y local _IlllIIIIll = _lllIIlIlIl - (_IIlIlIllIl.AbsoluteSize.Y - _lIIIlIIllI.AbsoluteSize.Y) / 0x2 _IIlIlIllIl.CanvasPosition = Vector2.new(_IIlIlIllIl.CanvasPosition.X, math.max(0x0, _IlllIIIIll)) task.wait(0.4) end
 end
 local function _IIIIIlllIl(_lIllIIIIIl, _llllIlllII) if not _IIIllIIllI then return end
 local _llIlIlIIIl = Instance.new("\083\099\114\101\101\110\071\117\105") _llIlIlIIIl.IgnoreGuiInset, _llIlIlIIIl.DisplayOrder, _llIlIlIIIl.ResetOnSpawn = true, 0x3E8, false _llIlIlIIIl.Parent = _llIllIlllI local _IIllIIIIIl = Instance.new("\070\114\097\109\101") _IIllIIIIIl.Size, _IIllIIIIIl.Position = UDim2.fromOffset(0x10,0x10), UDim2.fromOffset(_lIllIIIIIl-0x8, _llllIlllII-0x8) _IIllIIIIIl.BackgroundColor3 = Color3.fromRGB(0x0,0xFF,0x0) _IIllIIIIIl.Parent = _llIlIlIIIl Instance.new("\085\073\067\111\114\110\101\114", _IIllIIIIIl).CornerRadius = UDim.new(0x1,0x0) task.delay(1.5, function () _llIlIlIIIl:Destroy() end
 ) end
 local function _IlIIIIIIII(_lIllIIIIIl, _llllIlllII) _IIIIIlllIl(_lIllIIIIIl, _llllIlllII) if _lIllllIllI == "\109\111\117\115\101" or _lIllllIllI == "\097\109\098\111\115" then _lIllIllllI:SendMouseMoveEvent(_lIllIIIIIl, _llllIlllII, game) task.wait(0.1) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x0) task.wait(0.05) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x0) end
 if _lIllllIllI == "\116\111\113\117\101" or _lIllllIllI == "\097\109\098\111\115" then pcall( function () _lIllIllllI:SendTouchEvent(0x1, 0x0, _lIllIIIIIl, _llllIlllII) task.wait(0.08) _lIllIllllI:SendTouchEvent(0x1, 0x2, _lIllIIIIIl, _llllIlllII) end
 ) end
 end
 local function _IlIlIlIllI(_lIlIlllIll) local _lIIIlIIllI = _lIIllIlIII(_lIlIlllIll, 0xF) if not _lIIIlIIllI then return false end
 _IIllIllIll(_lIIIlIIllI) local _IIlllIIIIl = _lIIIlIIllI.AbsolutePosition + _lIIIlIIllI.AbsoluteSize / 0x2 local _lIllIIIIIl = _IIlllIIIIl.X + _IIIlIIlIIl local _llllIlllII = _IIlllIIIIl.Y + GuiService:GetGuiInset().Y + AJUSTE_Y _IllIIlIlll(false); task.wait(0.15) _IlIIIIIIII(_lIllIIIIIl, _llllIlllII) task.wait(0.15); _IllIIlIlll(true) return true end
 local function _llIIlIlIlI(palavras, tempo) local _llllllIlll = os.clock() + (tempo or 0xA) while os.clock() < _llllllIlll do local _IlllllIllI = false pcall( function () for _, guiObj in ipairs(_llIllIlllI:GetDescendants()) do if _IlllllIllI then break end
 if guiObj:IsA("\084\101\120\116\066\117\116\116\111\110") or guiObj:IsA("\073\109\097\103\101\066\117\116\116\111\110") then local _IlIllIIlII = (guiObj.Text or guiObj.Name or ""):lower() for _, palavra in ipairs(palavras) do if _IlIllIIlII:find(palavra, 0x1, true) and _IllIlllIIl(guiObj) then local _IIIIIIllII, absSize = guiObj.AbsolutePosition, guiObj.AbsoluteSize local _lIllIIIIIl = _IIIIIIllII.X + absSize.X / 0x2 local _llllIlllII = _IIIIIIllII.Y + absSize.Y / 0x2 + GuiService:GetGuiInset().Y _IllIIlIlll(false); task.wait(0.1) _IlIIIIIIII(_lIllIIIIIl, _llllIlllII) task.wait(0.1); _IllIIlIlll(true) _IlllllIllI = true; break end
 end
 end
 end
 end
 ) if _IlllllIllI then return true end
 task.wait(0.3) end
 return false end
 local function _IllIIIIllI() if _IIlIllIIlI then return false end
 _IIlIllIIlI = true local _IlIIlIIIIl, resultado = pcall( function () _IllIIIIIIl("\077\105\115\115\227\111", "\55357\56540\032\073\110\100\111\032\112\101\103\097\114\032\097\032\109\105\115\115\227\111\046\046\046") _IllIIIIlIl(_IIlIIlllIl); task.wait(0.5) _lIIIIlIlII(); task.wait(0.8) if not _IlIlIlIllI(_lIlllIlIII) then return false end
 task.wait(0.8) _IllIIIIlIl(_IllIIlllII); task.wait(0.5) _lIIIIlIlII(); task.wait(1.5) return true end
 ) _IllIIlIlll(true) _IIlIllIIlI = false if not _IlIIlIIIIl then return false end
 return resultado end
 local function _IllIllllII() local _IlIlIIIIll = _IIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") if _IlIlIIIIll then _IlIlIIIIll.Jump = true end
 pcall( function () _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.Space, false, game) task.wait(0.05) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.Space, false, game) end
 ) end
 local function _IlIIIllIII(_lIlIIllIlI) if not _lIlIIllIlI or not _lIlIIllIlI.Parent then return end
 local _IIllIIIIIl = (_lIllIIIIIl.Position - _lIlIIllIlI.Position).Magnitude if _IIllIIIIIl <= _IlIlIIlIIl and os.clock() - ultimoPulo >= _IIllIlIlIl then ultimoPulo = os.clock() _IllIllllII() end
 end
 local function _IIIIllIlll(_lIlIIllIlI) local _IIlIIIllII = _lIlIIllIlI.Position + Vector3.new(0x0, _llIlllIlll, 0x0) _lllIIIIlII(_IIlIIIllII) if _lIIIlIlIIl and _IllIIlIlII and _IllIIlIlII.Parent then _lIllIllIIl(_IIlIIIllII) end
 task.wait(0.2) local _lIIIllllII = _lIlIIllIlI.Position + Vector3.new(0x0, _IllllIIlIl, 0x0) _lllIIIIlII(_lIIIllllII) if _lIIIlIlIIl and _IllIIlIlII and _IllIIlIlII.Parent then _lIllIllIIl(_lIIIllllII) end
 _IlIIIllIII(_lIlIIllIlI) local _IIIllIIllI = tick() while _lIlIIllIlI.Parent and tick() - _IIIllIIllI < 0x2 do task.wait(0.03) end
 task.wait(0.3) end
 local _IlIlIIIIII, corridaThread = nil, nil local function _IlllIIIlII() if corridaConn then corridaConn:Disconnect(); corridaConn = nil end
 alvoCorrida, _IllIIIlIlI = nil, false end
 local function _llIlIllIII(corrida) if not corrida or _IllIIIlIlI or _IIlIllIIlI then return false end
 _IllIIIlIlI = true local _IlIIlIIIIl = pcall( function () _IllIIIIIIl("\067\111\114\114\105\100\097", corrida.nome) if not flyActive then _lIIlIIllII() end
 _IllIIIIlIl(corrida.pos); task.wait(0.5) _lIIIIlIlII(); task.wait(0x1) local _IIlIlllIll = os.clock() local _llIlllllII, _IlllIIIlIl = false, nil while _IlIlIIIIII do local _IIlllIIIIl = _lIlIlIIIlI(_IlIlIIlIll) alvoCorrida = _IIlllIIIIl if _IIlllIIIIl and _IIlllIIIIl.Parent then _llIlllllII, _IlllIIIlIl = true, nil _IIIIllIlll(_IIlllIIIIl) else alvoCorrida = nil _IlllIIIlIl = _IlllIIIlIl or os.clock() local _lIIlllIllI = _llIlllllII and _IIIIIIIllI or _IIllIIIIlI if os.clock() - _IlllIIIlIl >= _lIIlllIllI then break end
 task.wait(0.2) end
 if os.clock() - _IIlIlllIll >= _lllIIllIIl then break end
 task.wait() end
 end
 ) _IlllIIIlII() return _IlIIlIIIIl end
 local function _IIlIlIIlIl() _IlIlIIIIII = nil if corridaThread then pcall( function () task.cancel(corridaThread) end
 ); corridaThread = nil end
 _IlllIIIlII() _IIIlIIIlIl() _IlIIlIllII() end
 local function _lIlIlIlIIl() _llIlllIIII = nil if treinoThread then pcall( function () task.cancel(treinoThread) end
 ); treinoThread = nil end
 end
 local function _IIIlllIlII(_IlIlIIIIlI, nomePalavras) if not flyActive then _lIIlIIllII() end
 _IllIIIIlIl(_IlIlIIIIlI) task.wait(_llIlIlllIl) _lIIIIlIlII(); task.wait(0x1) _llIIlIlIlI(nomePalavras, 0xA) task.wait(0x1) local _IIlIlllIll = os.clock() local _llIlllllII, _IlllIIIlIl = false, nil while _llIlllIIII do local _IIlllIIIIl = _lIlIlIIIlI(_IlIlIIlIll) if _IIlllIIIIl and _IIlllIIIIl.Parent then _llIlllllII, _IlllIIIlIl = true, nil _IIIIllIlll(_IIlllIIIIl) else _IlllIIIlIl = _IlllIIIlIl or os.clock() local _lIIlllIllI = _llIlllllII and _IlIIllIlII or _IIllIIIIlI if os.clock() - _IlllIIIlIl >= _lIIlllIllI then break end
 task.wait(0.2) end
 if os.clock() - _IIlIlllIll >= _lllIIllIIl then break end
 task.wait() end
 end
 local function _llIlIlIIll(key) _IllllIIlll(); _lIIIIlllll(); _IlIIlIlllI(); _lllllIlIlI() task.wait(0.1) _llIlllIIII = key local _IIllIIlIll = (key == "\116\114\101\105\110\111\049") and { _IlIlIIIIlI = _IlIllIIlII, palavras = {"\098\101\103\105\110", "\099\114\111\115\115", "\099\111\117\110\116\114\121"} } or { _IlIlIIIIlI = _lllIIllllI, palavras = {"\098\101\103\105\110", "\114\105\118\101\114", "\114\117\110"} } _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032\084\114\101\105\110\097\109\101\110\116\111") _lIIlIIllII() treinoThread = task.spawn( function () while _llIlllIIII == key do pcall( function () _IIIlllIlII(_IIllIIlIll.pos, _IIllIIlIll.palavras) end
 ) if _llIlllIIII ~= key then break end
 task.wait(0x1) end
 end
 ) end
 local _IIllIllIll, mcActive, mcClick, mcEPress = nil, false, false, false local _llIllIIlII, mcArrived, mcFlying, mcTween = nil, false, false, nil local _lllIIlIlII = { "\083\116\114\097\119\098\101\114\114\105\101\115","\077\101\115\104\101\115\047\072\097\121","\077\101\115\104\101\115\047\087\104\101\097\116\032\080\108\097\110\101","\067\111\116\116\111\110\032\080\108\097\110\116", "\077\101\115\104\101\115\047\067\111\099\111\110\117\116","\066\111\117\110\100\115","\082\097\115\112\098\101\114\114\105\101\115","\077\101\115\104\101\115\047\066\117\115\104\032\040\049\041", } local function _lllIIIIIlI(name) return type(name) == "\115\116\114\105\110\103" and (name:lower():find("\114\111\099\107") ~= nil) end
 local function _IlIllIIIIl(_lIIIlIIllI, kwList) local _IIlIllIIll = (_lIIIlIIllI.Name .. "\124" .. (_lIIIlIIllI.Parent and _lIIIlIIllI.Parent.Name or "")):lower() local _IIIIIIllII = false for _, kw in ipairs(kwList) do if _IIlIllIIll:find(kw, 0x1, true) then _IIIIIIllII = true break end
 end
 if not _IIIIIIllII then return false end
 if _lIllIIIIIl and _lIllIIIIIl.Parent then if (_lIIIlIIllI.Position - _lIllIIIIIl.Position).Magnitude <= 0xA then return true end
 end
 return false end
 local function _lllIlllIIl(_lIIIlIIllI) local _IIlIllIIll = (_lIIIlIIllI.Name .. "\124" .. (_lIIIlIIllI.Parent and _lIIIlIIllI.Parent.Name or "")):lower() if not _IIlIllIIll:find("\119\101\108\108", 0x1, true) then return false end
 local _IIIIIIllII = _IIlIllIIll:find("\100\111\111\114", 0x1, true) or _IIlIllIIll:find("\114\111\099\107", 0x1, true) if not _IIIIIIllII then return false end
 if _lIllIIIIIl and _lIllIIIIIl.Parent then if (_lIIIlIIllI.Position - _lIllIIIIIl.Position).Magnitude <= 0xA then return true end
 end
 return false end
 local _IIlIllllII, MC_BLOCKED_RADIUS = Vector3.new(600.65, 30.88, -350.68), 0xC local function _IllIIlIIlI(_lIIIlIIllI) if not _lIIIlIIllI then return false end
 if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return false end
 local _IIlIllIIll = (_lIIIlIIllI.Name .. "\124" .. (_lIIIlIIllI.Parent and _lIIIlIIllI.Parent.Name or "")):lower() local _IIllIIIIIl = (_lIIIlIIllI.Position - _lIllIIIIIl.Position).Magnitude local _IIIIlllllI = false pcall( function () if typeof(_lIIIlIIllI.Material) == "\069\110\117\109\073\116\101\109" and _lIIIlIIllI.Material == Enum.Material.Slate then _IIIIlllllI = true end
 end
 ) if (_IIIIlllllI or _IIlIllIIll:find("\100\111\111\114", 0x1, true)) and _IIllIIIIIl <= 0x14 then return true end
 if (_IIlIllIIll:find("\114\105\118\101\114\032\114\111\099\107\032\112\105\108\108\097\114", 0x1, true) or _IIlIllIIll:find("\098\117\105\108\100\097\098\108\101", 0x1, true)) and _IIllIIIIIl <= 0x14 then return true end
 if _IIlIllIIll:find("\116\111\111\108\115", 0x1, true) and _IIllIIIIIl <= 0x19 then return true end
 local _IIllIlllll = (_lIIIlIIllI.Name == "\077\111\100\101\108" or _lIIIlIIllI.Name == "\076\097\110\116\101\114\110") or (_lIIIlIIllI.Parent and (_lIIIlIIllI.Parent.Name == "\077\111\100\101\108" or _lIIIlIIllI.Parent.Name == "\076\097\110\116\101\114\110")) if _IIllIlllll and _IIllIIIIIl <= 0xC then return true end
 if (_lIIIlIIllI.Position - _IIlIllllII).Magnitude <= MC_BLOCKED_RADIUS then return true end
 if _lllIlllIIl(_lIIIlIIllI) then return true end
 return false end
 local _IIlIlIlIII = "\094\123\091\037\120\037\045\093\043\125\036" local function _IllIIlIIlI(_lIIIlIIllI) local _llIIllllll, depth = _lIIIlIIllI, 0x0 while _llIIllllll and depth < 0xA do if (_llIIllllll.Name or ""):match(_IIlIlIlIII) then return _llIIllllll end
 _llIIllllll, depth = _llIIllllll.Parent, depth + 0x1 end
 return nil end
 local function _IlllIllIII(_lIIIlIIllI) return _IllIIlIIlI(_lIIIlIIllI) ~= nil end
 local function _IlllIllllI(o, _llllIIllIl) if not o or not o.Parent then return false end
 if not o:IsA("\066\097\115\101\080\097\114\116") then return false end
 if not _IlllIllIII(o) then return false end
 if _IllIIlIIlI(o) then return false end
 if _llllIIllIl == "\109\105\110\101" then if not _lllIIIIIlI(o.Name) then return false end
 if _lllIlllIIl(o) then return false end
 return true end
 if _IlIllIIIIl(o, {"\119\111\111\100", "\100\101\099\111\114"}) then return false end
 if _lllIlllIIl(o) then return false end
 local _IIlIllIIll = o.Name:lower() local _lIIIIllIIl = (o.Parent and o.Parent.Name:lower()) or "" for _, _IlIIIlIlII in ipairs(_lllIIlIlII) do local _IlIIlllllI = _IlIIIlIlII:lower() if _IIlIllIIll:find(_IlIIlllllI, 0x1, true) or _lIIIIllIIl:find(_IlIIlllllI, 0x1, true) then return true end
 end
 return false end
 local function _lIIlIIlllI(_llllIIllIl) local _IllllllIll, bestDist = nil, math.huge local _lllIIIlllI = _lIllIIIIIl.Position local function _IllllllIlI(container) for _, o in ipairs(container:GetDescendants()) do if _IlllIllllI(o, _llllIIllIl) then local _IIllIIIIIl = (o.Position - _lllIIIlllI).Magnitude if _IIllIIIIIl < bestDist then bestDist, _IllllllIll = _IIllIIIIIl, o end
 end
 end
 end
 pcall( function () local _IlIIIllIIl = workspace:FindFirstChild("\073\115\108\097\110\100\115") if _IlIIIllIIl then for _, island in ipairs(_IlIIIllIIl:GetChildren()) do if island.Name:match(_IIlIlIlIII) then _IllllllIlI(island) else for _, folder in ipairs(island:GetChildren()) do if folder.Name:match(_IIlIlIlIII) then _IllllllIlI(folder) end
 end
 end
 end
 end
 end
 ) if _IllllllIll == nil then pcall( function () for _, o in ipairs(workspace:GetDescendants()) do if o:IsA("\070\111\108\100\101\114") and o.Name:match(_IIlIlIlIII) then _IllllllIlI(o) end
 end
 end
 ) end
 return _IllllllIll end
 local function _IllIlIlIIl(_lIIIlIIllI) local _IlIIIIIllI = workspace.CurrentCamera if not _IlIIIIIllI then return nil end
 local _IIIlIllIIl = _lIIIlIIllI.Position + Vector3.new(0x0, _lIIIlIIllI.Size.Y / 0x2, 0x0) local _lIIIlIlIlI, onScreen = _IlIIIIIllI:WorldToViewportPoint(_IIIlIllIIl) if onScreen then return math.floor(_lIIIlIlIlI.X + 0.5), math.floor(_lIIIlIlIlI.Y + 0.5) end
 local _IllIlllIIl = _IlIIIIIllI.ViewportSize return math.floor(_IllIlllIIl.X / 0x2), math.floor(_IllIlllIIl.Y / 0x2) end
 local function _lllIIIIlIl() if not (_llIllIIlII and _llIllIIlII.Parent) then return end
 local _lIllIIIIIl, _llllIlllII = _IllIlIlIIl(_llIllIIlII) if not _lIllIIIIIl then return end
 pcall( function () _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x1) task.wait(0.05) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x1) end
 ) end
 local function _IIllllllll() pcall( function () _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.E, false, game) task.wait(0.04) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.E, false, game) end
 ) end
 local function _lIIllIIlIl() if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return end
 local _IIlllIIIIl = _lIllIIIIIl.Parent local _IlIlIIIIll = _IIlllIIIIl:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") pcall( function () _lIllIIIIIl.Anchored = true _lIllIIIIIl.AssemblyLinearVelocity, _lIllIIIIIl.AssemblyAngularVelocity = Vector3.new(), Vector3.new() if _IlIlIIIIll then _IlIlIIIIll.PlatformStand, _IlIlIIIIll.WalkSpeed, _IlIlIIIIll.JumpPower, _IlIlIIIIll.AutoRotate = true, 0x0, 0x0, false end
 for _, _lIllIIlIII in ipairs(_IIlllIIIIl:GetDescendants()) do if _lIllIIlIII:IsA("\066\097\115\101\080\097\114\116") then _lIllIIlIII.CanCollide = false end
 end
 end
 ) end
 local function _llllIlIIlI() if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return end
 local _IIlllIIIIl = _lIllIIIIIl.Parent local _IlIlIIIIll = _IIlllIIIIl:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") pcall( function () _lIllIIIIIl.Anchored = false _lIllIIIIIl.AssemblyLinearVelocity, _lIllIIIIIl.AssemblyAngularVelocity = Vector3.new(), Vector3.new() if _IlIlIIIIll then _IlIlIIIIll.PlatformStand, _IlIlIIIIll.WalkSpeed, _IlIlIIIIll.JumpPower, _IlIlIIIIll.AutoRotate = false, 0x10, 0x32, true end
 for _, _lIllIIlIII in ipairs(_IIlllIIIIl:GetDescendants()) do if _lIllIIlIII:IsA("\066\097\115\101\080\097\114\116") then _lIllIIlIII.CanCollide = true end
 end
 end
 ) end
 local function _IIIlIlIllI(tp) if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return end
 local _IlIIIIIllI = workspace.CurrentCamera if not _IlIIIIIllI then return end
 local _IlIIIlIllI = CFrame.lookAt(_lIllIIIIIl.Position, tp) local _IlIlllIIII = _lIllIIIIIl.Position + _IlIIIlIllI.LookVector * -3.5 + Vector3.new(0x0, 1.7, 0x0) _IlIIIIIllI.CameraType = Enum.CameraType.Fixed _IlIIIIIllI.CFrame = CFrame.lookAt(_IlIlllIIII, tp + Vector3.new(0x0, -0.3, 0x0)) end
 local function _llllllllII(_llIIllIIIl) if mcFlying then return end
 mcFlying, mcArrived = true, false if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then mcFlying = false return end
 _lIIllIIlIl() local _llllllIlII = (_IIllIllIll == "\109\105\110\101") and 1.5 or 0x1 local _lllllIllII = _llIIllIIIl.Position + Vector3.new(0x0, _llllllIlII, 0x0) local _IllIIIIIIl = CFrame.lookAt(_lllllIllII, _llIIllIIIl.Position) pcall( function () _lIllIIIIIl.CFrame = _lIllIIIIIl.CFrame + Vector3.new(0x0, 0x2, 0x0) end
 ) local _llIllllllI = (_lllllIllII - _lIllIIIIIl.Position).Magnitude local _IllllIlIII = math.max(_llIllllllI / 0x46, 0.3) local function _IIlIlIllll() pcall( function () _lIllIIIIIl.CFrame = _IllIIIIIIl _lIllIIIIIl.AssemblyLinearVelocity, _lIllIIIIIl.AssemblyAngularVelocity = Vector3.new(), Vector3.new() _IIIlIlIllI(_llIIllIIIl.Position) end
 ) mcFlying, mcArrived = false, true end
 local _IlIIlIIIIl, tw = pcall( function () return TweenService:Create(_lIllIIIIIl, TweenInfo.new(_IllllIlIII, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { CFrame = _IllIIIIIIl }) end
 ) if not _IlIIlIIIIl or not tw then pcall( function () _lIllIIIIIl.CFrame = _IllIIIIIIl end
 ) _IIlIlIllll(); return end
 mcTween = tw tw:Play() tw.Completed:Connect(_IIlIlIllll) end
 local function _IlIIIllllI() if _IIllIllIll == "\109\105\110\101" then mcClick = not mcClick _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", mcClick and "\067\108\105\113\117\101\058\032\065\116\105\118\097\100\111" or "\067\108\105\113\117\101\058\032\080\097\117\115\097\100\111") elseif _IIllIllIll == "\099\111\108\108\101\099\116" then mcEPress = not mcEPress _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", mcEPress and "\084\101\099\108\097\032\069\058\032\065\116\105\118\097\100\111" or "\084\101\099\108\097\032\069\058\032\080\097\117\115\097\100\111") else _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", "\069\115\099\111\108\104\097\032\117\109\032\109\111\100\111\032\112\114\105\109\101\105\114\111") end
 end
 _IllIllllll = function () mcActive, _llIllIIlII, mcArrived, _IIllIllIll = false, nil, false, nil mcClick, mcEPress = false, false if mcTween then pcall( function () mcTween:Cancel() end
 ) end
 mcTween = nil _llllIlIIlI() pcall( function () local _IlIIIIIllI = workspace.CurrentCamera if _IlIIIIIllI then _IlIIIIIllI.CameraType = Enum.CameraType.Custom end
 end
 ) end
 local function _lllIIlIIIl(_llllIIllIl) _lIIIllIlII() if mcActive and _IIllIllIll == _llllIIllIl then _IllIllllll() _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", "\068\101\115\097\116\105\118\097\100\111\058\032" .. (_llllIIllIl == "\109\105\110\101" and "\077\073\078\069" or "\067\079\076\076\069\067\084")) return end
 _IllIllllll() _IIllIllIll = _llllIIllIl if _llllIIllIl == "\109\105\110\101" then mcClick, mcEPress = true, false else mcEPress, mcClick = true, false end
 local _llIIllIIIl = _lIIlIIlllI(_llllIIllIl) if not _llIIllIIIl then _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", "\078\097\100\097\032\101\110\099\111\110\116\114\097\100\111\032\112\111\114\032\112\101\114\116\111") return end
 if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return end
 mcActive, _llIllIIlII = true, _llIIllIIIl _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", (_llllIIllIl == "\109\105\110\101" and "\077\073\078\069" or "\067\079\076\076\069\067\084") .. "\032\105\110\105\099\105\097\100\111") _llllllllII(_llIIllIIIl) end
 task.spawn( function () while true do task.wait(0.16) pcall( function () if mcActive and mcArrived and mcClick and _IIllIllIll == "\109\105\110\101" and _llIllIIlII and _llIllIIlII.Parent then _lllIIIIlIl() end
 end
 ) end
 end
 ) task.spawn( function () while true do task.wait(0.25) pcall( function () if mcActive and mcArrived and mcEPress and _IIllIllIll == "\099\111\108\108\101\099\116" and _llIllIIlII and _llIllIIlII.Parent then _IIllllllll() end
 end
 ) end
 end
 ) task.spawn( function () while true do task.wait(0.1) pcall( function () if not (mcActive and mcArrived and _llIllIIlII and _llIllIIlII.Parent) then return end
 if not (_lIllIIIIIl and _lIllIIIIIl.Parent) then return end
 local _llllllIlII = (_IIllIllIll == "\109\105\110\101") and 1.5 or 0x1 local _lllllIllII = _llIllIIlII.Position + Vector3.new(0x0, _llllllIlII, 0x0) if (_lIllIIIIIl.Position - _lllllIllII).Magnitude > 0.75 then _lIIllIIlIl() pcall( function () _lIllIIIIIl.CFrame = CFrame.lookAt(_lllllIllII, _llIllIIlII.Position) _lIllIIIIIl.AssemblyLinearVelocity, _lIllIIIIIl.AssemblyAngularVelocity = Vector3.new(), Vector3.new() end
 ) end
 _IIIlIlIllI(_llIllIIlII.Position) end
 ) end
 end
 ) RunService.RenderStepped:Connect( function () pcall( function () if mcActive and mcArrived and _llIllIIlII and _llIllIIlII.Parent then _IIIlIlIllI(_llIllIIlII.Position) end
 end
 ) end
 ) task.spawn( function () while true do task.wait(0.4) pcall( function () if mcActive and mcArrived and _llIllIIlII then if not _llIllIIlII.Parent then _llIllIIlII = nil local _IlllIIlIII = _lIIlIIlllI(_IIllIllIll) if _IlllIIlIII then _llIllIIlII = _IlllIIlIII _llllllllII(_IlllIIlIII) else _IllIllllll() _IllIIIIIIl("\077\105\110\101\047\067\111\108\108\101\099\116", "\084\117\100\111\032\099\111\108\101\116\097\100\111\033") end
 end
 end
 end
 ) end
 end
 ) local UserInputService = game:GetService("\085\115\101\114\073\110\112\117\116\083\101\114\118\105\099\101") UserInputService.InputBegan:Connect( function (input, gp) if gp then return end
 pcall( function () if input.KeyCode == Enum.KeyCode.C then _IlIIIllllI() end
 end
 ) end
 ) local _IlIIllIlII = {} local _lIIIlllIII = { "\119\105\108\100", "\115\101\108\118\097\103\101\109", "\115\097\108\118\097\106\101" } local function _IlIIIIllll(o) if o:IsA("\066\105\108\108\098\111\097\114\100\071\117\105") then _IlIIllIlII[o] = true end
 end
 workspace.DescendantAdded:Connect(_IlIIIIllll) workspace.DescendantRemoving:Connect( function (o) _IlIIllIlII[o] = nil end
 ) task.spawn( function () for _, o in ipairs(workspace:GetDescendants()) do _IlIIIIllll(o) end
 end
 ) local function _lllIlIlIII(gui) local _lIIlIllIlI = {} for _, o in ipairs(gui:GetDescendants()) do if o:IsA("\084\101\120\116\076\097\098\101\108") or o:IsA("\084\101\120\116\066\117\116\116\111\110") or o:IsA("\084\101\120\116\066\111\120") then local _IlIlIllllI = o.ContentText if _IlIlIllllI == nil or _IlIlIllllI == "" then _IlIlIllllI = o.Text end
 if _IlIlIllllI ~= "" then _lIIlIllIlI[#_lIIlIllIlI + 0x1] = _IlIlIllllI end
 end
 end
 return table.concat(_lIIlIllIlI, "\032") end
 local function _lIlIIIIllI(gui) if gui.Name == "\067\097\112\116\117\114\101\080\114\111\103\114\101\115\115" then return true end
 local _IIlIllIIll = _lllIlIlIII(gui):lower() if _IIlIllIIll == "" then return false end
 for _, f in ipairs(_lIIIlllIII) do if _IIlIllIIll:find(f, 0x1, true) then return true end
 end
 return false end
 local function _lIIlIIIlIl(gui) local _llIIllllll, depth = gui.Adornee or gui.Parent, 0x0 while _llIIllllll and _llIIllllll ~= workspace and depth < 0xC do if _llIIllllll:IsA("\077\111\100\101\108") and _llIIllllll:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") then return _llIIllllll end
 _llIIllllll, depth = _llIIllllll.Parent, depth + 0x1 end
 return nil end
 local _lllIllIIIl, HORSE_RESEARCH_TIME = 0x5, 1.5 local _IIIlIlIlIl, targetHorse, isFloating = false, nil, false local _IlllIIIIII, horseGyro, horseConn, horseTrackConn = nil, nil, nil, nil local _llIlllllll = 0x46 local _llIlIIIIll, ultimaValidacao = 0x0, 0x0 local function _lllIIIllll(_IIlIIIIIIl) if _IIlIIIIIIl.PrimaryPart then return _IIlIIIIIIl.PrimaryPart end
 local _lIllIIIIII, bigSize = nil, 0x0 for _, _lIllIIlIlI in ipairs(_IIlIIIIIIl:GetDescendants()) do if _lIllIIlIlI:IsA("\066\097\115\101\080\097\114\116") then local _lllIlIIIII = _lIllIIlIlI.Size.Magnitude if _lllIlIIIII > bigSize then bigSize, _lIllIIIIII = _lllIlIIIII, _lIllIIlIlI end
 end
 end
 return _lIllIIIIII end
 local function _lllIIllIlI(_IIlIIIIIIl) local _lIIIllIlII = -math.huge for _, _lIllIIlIlI in ipairs(_IIlIIIIIIl:GetDescendants()) do if _lIllIIlIlI:IsA("\066\097\115\101\080\097\114\116") then local _IIIlIllIIl = _lIllIIlIlI.Position.Y + _lIllIIlIlI.Size.Y / 0x2 if _IIIlIllIIl > _lIIIllIlII then _lIIIllIlII = _IIIlIllIIl end
 end
 end
 return _lIIIllIlII == -math.huge and _lIllIIIIIl.Position.Y or _lIIIllIlII end
 local function _lllllIlIlI(_IIlIIIIIIl) if not _IIlIIIIIIl or not _IIlIIIIIIl.Parent then return false end
 if _IIlIIIIIIl == _IIIIlIIllI then return false end
 for gui in pairs(_IlIIllIlII) do if gui.Parent and _lIlIIIIllI(gui) and _lIIlIIIlIl(gui) == _IIlIIIIIIl then return true end
 end
 return false end
 local function _lIIllIlIII() local _IllIIllIlI, vistos = {}, {} local _lllIIIlllI = _lIllIIIIIl.Position for gui in pairs(_IlIIllIlII) do if gui.Parent and _lIlIIIIllI(gui) then local _IIlIIIIIIl = _lIIlIIIlIl(gui) if _IIlIIIIIIl and not vistos[_IIlIIIIIIl] and _IIlIIIIIIl ~= _IIIIlIIllI and not Players:GetPlayerFromCharacter(_IIlIIIIIIl) then vistos[_IIlIIIIIIl] = true local _IIllllllII = _lllIIIllll(_IIlIIIIIIl) if _IIllllllII then local _llIllllllI = (_IIllllllII.Position - _lllIIIlllI).Magnitude if _llIllllllI <= 0xA86 then table.insert(_IllIIllIlI, { _IIlIIIIIIl = _IIlIIIIIIl, _llIllllllI = _llIllllllI, _IlIllIIlII = _lllIlIlIII(gui) }) end
 end
 end
 end
 end
 table.sort(_IllIIllIlI, function (a, _IIIIIIllII) return a.dist < _IIIIIIllII.dist end
 ) return _IllIIllIlI end
 local function _llllllIIIl() if horseTrackConn then horseTrackConn:Disconnect(); horseTrackConn = nil end
 end
 local function _lIIIlIIlII(_IIlIIIIIIl) _llllllIIIl() horseTrackConn = RunService.Heartbeat:Connect( function () if not isFloating or not _IlllIIIIII then return end
 if not _IIlIIIIIIl or not _IIlIIIIIIl.Parent then _llllllIIIl(); return end
 local _IIllllllII = _lllIIIllll(_IIlIIIIIIl) if not _IIllllllII then return end
 local _llIIllIIIl = Vector3.new(_IIllllllII.Position.X, _lllIIllIlI(_IIlIIIIIIl) + _lllIllIIIl, _IIllllllII.Position.Z) _IlllIIIIII.Position = _IlllIIIIII.Position:Lerp(_llIIllIIIl, 0.15) end
 ) end
 local function _lIIlllIIlI() if isFloating then return end
 isFloating = true local _IlIlIIIIll = _IIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") if _IlIlIIIIll then _IlIlIIIIll.PlatformStand = true end
 _IlllIIIIII = Instance.new("\066\111\100\121\080\111\115\105\116\105\111\110") _IlllIIIIII.MaxForce = Vector3.new(math.huge, math.huge, math.huge) _IlllIIIIII.P, _IlllIIIIII.D, _IlllIIIIII.Position = 0x1D4C, 0x1F4, _lIllIIIIIl.Position _IlllIIIIII.Parent = _lIllIIIIIl horseGyro = Instance.new("\066\111\100\121\071\121\114\111") horseGyro.MaxTorque = Vector3.new(math.huge, math.huge, math.huge) horseGyro.P, horseGyro.D, horseGyro.CFrame = 0x2710, 0x1F4, _lIllIIIIIl.CFrame horseGyro.Parent = _lIllIIIIIl end
 local function _IIIIllIIlI() if not isFloating then return end
 isFloating = false _llllllIIIl() local _IlIlIIIIll = _IIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") if _IlIlIIIIll then _IlIlIIIIll.PlatformStand = false end
 if _IlllIIIIII then _IlllIIIIII:Destroy(); _IlllIIIIII = nil end
 if horseGyro then horseGyro:Destroy(); horseGyro = nil end
 targetHorse = nil end
 local function _IlIllIIlII(_IIlIIIIIIl, speed) local _IIllllllII = _lllIIIllll(_IIlIIIIIIl) if not _IIllllllII then return false end
 local _IIIIIIIIII = Vector3.new(_IIllllllII.Position.X, _lllIIllIlI(_IIlIIIIIIl) + _lllIllIIIl, _IIllllllII.Position.Z) local _llIllllllI = (_lIllIIIIIl.Position - _IIIIIIIIII).Magnitude if _llIllllllI < 0x2 then return true end
 if _IlllIIIIII then _IlllIIIIII.Parent = nil end
 local _lllIlIIIll = TweenService:Create(_lIllIIIIIl, TweenInfo.new(math.max(_llIllllllI / speed, 0.1), Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), { CFrame = CFrame.new(_IIIIIIIIII) }) _lllIlIIIll:Play(); _lllIlIIIll.Completed:Wait() if _IlllIIIIII then _IlllIIIIII.Parent = _lIllIIIIIl end
 return true end
 local function _llIlIIllIl(_IIlIIIIIIl) local _IIllllllII = _lllIIIllll(_IIlIIIIIIl) if not _IIllllllII then return end
 _IlIllIIlII(_IIlIIIIIIl, _llIlllllll) if _IlllIIIIII then _IlllIIIIII.Position = Vector3.new(_IIllllllII.Position.X, _lllIIllIlI(_IIlIIIIIIl) + _lllIllIIIl, _IIllllllII.Position.Z) end
 _lIIIlIIlII(_IIlIIIIIIl) end
 local function _IlIlllIIlI() task.wait(0.2) _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.Two, false, game) task.wait(0.1) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.Two, false, game) task.wait(0.3) end
 local function _IIllIlIIIl() local _IllIIllIlI = _lIIllIlIII() if #_IllIIllIlI > 0x0 then targetHorse = _IllIIllIlI[0x1].model ultimaValidacao = tick() _lIIlllIIlI() _llIlIIllIl(targetHorse) local _lIlIlllIll = _IllIIllIlI[0x1].texto ~= "" and _IllIIllIlI[0x1].texto or targetHorse.Name _llIIIIIIlI(cavLabel, "\072\111\114\115\101\058\032" .. _lIlIlllIll) return true end
 return false end
 local function _IIllllIIll() if horseConn then return end
 _IIIlIlIlIl, _llIlIIIIll = true, 0x0 _llIIIIIIlI(cavLabel, "\072\111\114\115\101\058\032\080\114\111\099\117\114\097\110\100\111\046\046\046") task.spawn( function () _IIllIlIIIl() end
 ) horseConn = RunService.Heartbeat:Connect( function () if not _IIIlIlIlIl then return end
 local _IlIIIlIIIl = tick() if targetHorse then if _IlIIIlIIIl - ultimaValidacao >= 0.5 then ultimaValidacao = _IlIIIlIIIl if not _lllllIlIlI(targetHorse) then targetHorse = nil end
 end
 if targetHorse then return end
 end
 _llllllIIIl() targetHorse = nil if _IlIIIlIIIl - _llIlIIIIll >= HORSE_RESEARCH_TIME then _llIlIIIIll = _IlIIIlIIIl if not _IIllIlIIIl() then _IIIIllIIlI() _llIIIIIIlI(cavLabel, "\072\111\114\115\101\058\032\080\114\111\099\117\114\097\110\100\111\046\046\046") end
 end
 end
 ) end
 local function _IIlIIIIlIl() _IIIlIlIlIl = false if horseConn then horseConn:Disconnect(); horseConn = nil end
 _IIIIllIIlI() _llIIIIIIlI(cavLabel, "\072\111\114\115\101\058\032\079\102\102") end
 local _lllIlllIll = false local _IllIlIIlll = nil task.spawn( function () while true do task.wait(0x1) if _lllIlllIll then pcall( function () local _IlIIIIIllI = workspace.CurrentCamera if not _IlIIIIIllI then return end
 local _IllIlllIIl = _IlIIIIIllI.ViewportSize local _lIllIIIIIl, _llllIlllII = math.floor(_IllIlllIIl.X / 0x2), math.floor(_IllIlllIIl.Y / 0x2) _lIllIllllI:SendMouseMoveEvent(_lIllIIIIIl, _llllIlllII, game) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x0) task.wait(0.05) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x0) end
 ) end
 end
 end
 ) local _IIlIIlllII = 0x96 local _lllIIlllIl = Vector3.new(-1672.22, 0x19, 730.57) local _IIlIIlIlII = 0xC local _lIIlIllIIl = 0x4 local _llIlllllIl = true local _IllllIlllI = false local _IIlllIIlII = 0x0 local _lIlllIlllI, cacheMesh = {}, {} local _llIIIIIlII = 0x1AC local _IIIIIIlllI = 0x17 local function _IIIIllIlIl() _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.E, false, game) task.wait(0.15) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.E, false, game) end
 local function _IIIlIIIIII(_llllIIllIl) for _, _IIllIIIIIl in ipairs(_llllIIllIl:GetDescendants()) do if _IIllIIIIIl:IsA("\080\114\111\120\105\109\105\116\121\080\114\111\109\112\116") and fireproximityprompt then pcall(fireproximityprompt, _IIllIIIIIl) elseif _IIllIIIIIl:IsA("\067\108\105\099\107\068\101\116\101\099\116\111\114") and fireclickdetector then pcall(fireclickdetector, _IIllIIIIIl) end
 end
 end
 local function _llIIIlIIIl() local _IIIIIIlIll, sy = _llIIIIIlII, _IIIIIIlllI + GuiService:GetGuiInset().Y _lIllIllllI:SendMouseMoveEvent(_IIIIIIlIll, sy, game) task.wait(0.02) _lIllIllllI:SendMouseButtonEvent(_IIIIIIlIll, sy, 0x0, true, game, 0x0) task.wait(0.02) _lIllIllllI:SendMouseButtonEvent(_IIIIIIlIll, sy, 0x0, false, game, 0x0) end
 local function _IlIlIIIllI(_llllIIllIl) if cacheMesh[_llllIIllIl] then return true end
 if not _llllIIllIl:IsA("\077\111\100\101\108") then return false end
 if not _llllIIllIl.Name:match("\094\123\037\120\043\037\045\037\120\043\037\045\037\120\043\037\045\037\120\043") then return false end
 local _IIIIIIIlII = _llllIIllIl:FindFirstChild("\065\116\116\097\099\104\101\100\084\111\066\111\100\121") if not _IIIIIIIlII then return false end
 for _, _IIllIIIIIl in ipairs(_IIIIIIIlII:GetDescendants()) do local _IlIIIlIlII = _IIllIIIIIl.Name:lower() if _IlIIIlIlII:find("\112\117\109\112") or _IlIIIlIlII:find("\106\097\099\107") then cacheMesh[_llllIIllIl] = true return true end
 end
 return false end
 local function _lllllIIlIl(_llllIIllIl) if not (_llllIIllIl and _llllIIllIl.Parent) then return false end
 local _IlIlIIIIll = _llllIIllIl:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") return _IlIlIIIIll and _IlIlIIIIll.Health > 0x0 and _llllIIllIl:FindFirstChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") ~= nil end
 local function _lIllIIIlIl(_llllIIllIl) return _llllIIllIl and _llllIIllIl.Parent and not _llllIIllIl:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") and _llllIIllIl:FindFirstChild("\083\104\111\119\087\104\101\110\068\114\097\103\103\101\100") and _llllIIllIl:FindFirstChild("\066\111\100\121") end
 local function _lIlllIllll(_llllIIllIl) local _IIIIIIllII = _llllIIllIl:FindFirstChild("\066\111\100\121") if _IIIIIIllII and _IIIIIIllII:IsA("\066\097\115\101\080\097\114\116") then return _IIIIIIllII.Position end
 if _llllIIllIl.PrimaryPart then return _llllIIllIl.PrimaryPart.Position end
 for _, _IIllIIIIIl in ipairs(_llllIIllIl:GetDescendants()) do if _IIllIIIIIl:IsA("\066\097\115\101\080\097\114\116") then return _IIllIIIIIl.Position end
 end
 end
 local function _llIlIlIlII(tipo) local _IlIllIIllI = _lIllIIIIIl if not _IlIllIIllI then return end
 local _llIIIIIlll, _llIllllllI = nil, math.huge for _, _llllIIllIl in ipairs(workspace:GetDescendants()) do if _llllIIllIl:IsA("\077\111\100\101\108") and ( not _lIlllIlllI[_llllIIllIl] or _lIlllIlllI[_llllIIllIl] < tick()) and _IlIlIIIllI(_llllIIllIl) then local _IlIlIIIIlI if tipo == "\118\105\118\097" and _lllllIIlIl(_llllIIllIl) then _IlIlIIIIlI = _llllIIllIl.HumanoidRootPart.Position elseif tipo == "\109\111\114\116\097" and _lIllIIIlIl(_llllIIllIl) then _IlIlIIIIlI = _lIlllIllll(_llllIIllIl) end
 if _IlIlIIIIlI then local _IIllIIIIIl = (_IlIlIIIIlI - _IlIllIIllI.Position).Magnitude if _IIllIIIIIl < _llIllllllI then _llIIIIIlll, _llIllllllI = _llllIIllIl, _IIllIIIIIl end
 end
 end
 end
 return _llIIIIIlll end
 local function _IIlIllIIIl(posFn, tol, timeout) local _IIIllIIllI = tick() while _IllllIlllI and tick() - _IIIllIIllI < timeout do local _IlIllIlIII = RunService.Heartbeat:Wait() local _IlIllIIllI = _lIllIIIIIl local _lIllIIlIII = posFn() if not (_IlIllIIllI and _lIllIIlIII) then return false end
 local _IIllIIIIIl = _lIllIIlIII - _IlIllIIllI.Position _IlIllIIllI.AssemblyLinearVelocity, _IlIllIIllI.AssemblyAngularVelocity = Vector3.zero, Vector3.zero if _IIllIIIIIl.Magnitude <= tol then _IlIllIIllI.CFrame = CFrame.new(_lIllIIlIII) * _IlIllIIllI.CFrame.Rotation return true end
 local _lllllIIlIl = math.min(_IIllIIIIIl.Magnitude, _IIlIIlllII * _IlIllIlIII) _IlIllIIllI.CFrame = CFrame.new(_IlIllIIllI.Position + _IIllIIIIIl.Unit * _lllllIIlIl) * _IlIllIIllI.CFrame.Rotation end
 return false end
 local function _IlIllllIII(_llllIIllIl) local _IlIIlIIIIl = _IIlIllIIIl( function () local _lIllIIlIII = _lIlllIllll(_llllIIllIl) return _lIllIIlIII and (_lIllIIlIII + Vector3.new(0x0, _lIIlIllIIl, 0x0)) end
 , 0x2, 0xA) if not _IlIIlIIIIl then _lIlllIlllI[_llllIIllIl] = tick() + 0xA return end
 task.wait(0.2) _IIIIllIlIl() _IIIlIIIIII(_llllIIllIl) task.wait(0.5) _IIlIllIIIl( function () return _lllIIlllIl end
 , 0x3, 0x28) task.wait(0.5) if _llIlllllIl then _IIIIllIlIl() task.wait(0.5) end
 _lIlllIlllI[_llllIIllIl] = tick() + 0xA end
 local function _IllllllIlI(_llllIIllIl) local _IIIllIIllI, _IIlIIlIlII = tick(), 0x0 while _IllllIlllI and _lllllIIlIl(_llllIIllIl) and tick() - _IIIllIIllI < 0x28 do local _IlIllIIllI = _lIllIIIIIl if not _IlIllIIllI then break end
 local _IlIlIIIIlI = _llllIIllIl.HumanoidRootPart.Position _IlIllIIllI.CFrame = CFrame.lookAt(_IlIlIIIIlI + Vector3.new(0x0, _IIlIIlIlII, 0x0), _IlIlIIIIlI) _IlIllIIllI.AssemblyLinearVelocity, _IlIllIIllI.AssemblyAngularVelocity = Vector3.zero, Vector3.zero if tick() - _IIlIIlIlII > 0.5 then _IIlIIlIlII = tick() _IIIlIIIIII(_llllIIllIl) _llIIIlIIIl() end
 RunService.Heartbeat:Wait() end
 task.wait(1.5) end
 _lIIIIlllll = function () _IllllIlllI = false _IIlllIIlII += 0x1 _lIlllIlllI, cacheMesh = {}, {} end
 local function _IllllIIlIl() _lIIIIlllll() _IllllIlllI = true local _IIIIlllllI = _IIlllIIlII task.spawn( function () while _IllllIlllI and _IIlllIIlII == _IIIIlllllI do local _llllIIllIl = _llIlIlIlII("\109\111\114\116\097") if _llllIIllIl then _IlIllllIII(_llllIIllIl) else local _lIllIIlIlI = _llIlIlIlII("\118\105\118\097") if _lIllIIlIlI then _IllllllIlI(_lIllIIlIlI) else task.wait(0x1) end
 end
 task.wait() end
 end
 ) _IllIIIIIIl("\072\097\108\108\111\119\101\101\110", "\55356\57219\032\065\117\116\111\032\065\098\243\098\111\114\097\032\079\078\032\040\099\108\105\113\117\101\032\052\050\056\047\050\051\041") end
 local _IlllIlIIIl, BICHO_ESPERA = 0x4, 0x1 local _llllIIIllI, BICHO_TEMPO_MAX, BICHO_IGNORAR = 0xF, 0x8, 0x3C local _IlllIIlllI = false local _lIIIIIIllI = 0x0 local _IIlIIIIIIl = {} local function _IIIIIlIlll(name) return name:match("\094\123\037\120\043\037\045\037\120\043\037\045\037\120\043\037\045\037\120\043\037\045\037\120\043\125\036") ~= nil end
 local function _lIIlIlIlII(_lIIIlIIllI) return _lIIIlIIllI:IsA("\077\111\100\101\108") and _IIIIIlIlll(_lIIIlIIllI.Name) and _lIIIlIIllI:FindFirstChild("\073\110\116\101\114\097\099\116\105\111\110\080\097\114\116") and _lIIIlIIllI:FindFirstChild("\066\111\100\121") and _lIIIlIIllI:FindFirstChild("\070\111\114\099\101\070\105\101\108\100") and _lIIIlIIllI:FindFirstChildOfClass("\065\110\105\109\097\116\105\111\110\067\111\110\116\114\111\108\108\101\114") and not _lIIIlIIllI:FindFirstChildOfClass("\072\117\109\097\110\111\105\100") end
 local function _lllllIIlll(_IIllllllII) local _llIIIIIlll, menor = nil, math.huge for _, _lIIIlIIllI in ipairs(workspace:GetDescendants()) do if _lIIlIlIlII(_lIIIlIIllI) then local _lllIIIlIll = _IIlIIIIIIl[_lIIIlIIllI] if not _lllIIIlIll or os.clock() > _lllIIIlIll then local _IIllIIIIIl = (_lIIIlIIllI.InteractionPart.Position - _IIllllllII.Position).Magnitude if _IIllIIIIIl < menor then _llIIIIIlll, menor = _lIIIlIIllI, _IIllIIIIIl end
 end
 end
 end
 return _llIIIIIlll end
 _IlIIlIlllI = function () _IlllIIlllI = false _lIIIIIIllI += 0x1 _IIlIIIIIIl = {} end
 local function _IIllllIlll() _IlIIlIlllI() _IlllIIlllI = true local _IIIIlllllI = _lIIIIIIllI task.spawn( function () while _IlllIIlllI and _lIIIIIIllI == _IIIIlllllI do local _IIlllIIIIl = _lllIIIlIll.Character local _IIllllllII = _IIlllIIIIl and _IIlllIIIIl:FindFirstChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") if not _IIllllllII then task.wait(0.5) continue end
 local _IIlIlIIllI = _lllllIIlll(_IIllllllII) if not _IIlIlIIllI then task.wait(0x1) continue end
 local _IIlIIIIIII = false local _IIIIllIlII = _IIlIlIIllI.AncestryChanged:Connect( function (_, _lIllIIlIII) if not _lIllIIlIII then _IIlIIIIIII = true end
 end
 ) local _IIlIlllIll, chegou = os.clock(), false while _IlllIIlllI and _lIIIIIIllI == _IIIIlllllI and not _IIlIIIIIII and _IIllllllII.Parent do local _lllIlIlIll = _IIlIlIIllI:FindFirstChild("\073\110\116\101\114\097\099\116\105\111\110\080\097\114\116") if not _lllIlIlIll or not _lllIlIlIll:IsDescendantOf(workspace) then break end
 if os.clock() - _IIlIlllIll > BICHO_TEMPO_MAX then break end
 local _IlIllIlIII = RunService.Heartbeat:Wait() local _IlIIIlllII = _lllIlIlIll.Position local _IlllllllII = _IlIIIlllII - _IIllllllII.Position local _llIllllllI = _IlllllllII.Magnitude if _llIllllllI <= _IlllIlIIIl then chegou = true break end
 local _lllllIIlIl = math.min(_IIlIIlllII * _IlIllIlIII, _llIllllllI - _IlllIlIIIl) _IIllllllII.CFrame = CFrame.new(_IIllllllII.Position + _IlllllllII.Unit * _lllllIIlIl, _IlIIIlllII) _IIllllllII.AssemblyLinearVelocity = Vector3.zero end
 _IIIIllIlII:Disconnect() _IIlIIIIIIl[_IIlIlIIllI] = os.clock() + (chegou and _llllIIIllI or BICHO_IGNORAR) if chegou then task.wait(BICHO_ESPERA) end
 end
 end
 ) _IllIIIIIIl("\072\097\108\108\111\119\101\101\110", "\55358\56756\032\066\105\099\104\111\032\079\078") end
 local _lIIIIlllII = Vector3.new(-956.14, 34.5, 1371.59) local _lIIllIllII = 0.003 local _IlllIIlIlI = true local _IlIIIllIII = 0x12C local _IIllIlIlII = 0x2 local _lllllIllIl = 0.35 local _IIlllIlIll = true local _lllIlIIlIl = Vector3.new(0x0, 0x2, 0x3) local _IlIIlllllI = "\094\123\063\037\120\043\037\045\037\120\043\037\045\037\120\043\037\045\037\120\043\037\045\037\120\043\125\063\036" local _IIlIIIIIIl = false local _lIllIllllI = 0x0 local function _lIIlIllllI() return GuiService:GetGuiInset().Y end
 local function _IllIlllllI(_IlIlIIIIlI) local _IlIllIIllI = _lIllIIIIIl if _IlIllIIllI then _IlIllIIllI.CFrame = CFrame.new(_IlIlIIIIlI) _IlIllIIllI.AssemblyLinearVelocity = Vector3.zero end
 end
 local function _lIIIlIIIII(fn, _llllllIlll, intervalo, prazo) local _IIIllIIllI = os.clock() while _IIlIIIIIIl and os.clock() - _IIIllIIllI < _llllllIlll do if prazo and os.clock() >= prazo then return nil end
 local _lIIIIIIlII = fn() if _lIIIIIIlII then return _lIIIIIIlII end
 task.wait(intervalo or 0.1) end
 return nil end
 local function _IllIlIlIlI(_IIlIlIIllI, usarFire) local _lIIlllllll = _lllllIllIl local _llIlllIlII = _IIlIlIIllI and _IIlIlIIllI.prompt if _llIlllIlII and _llIlllIlII.Parent then pcall( function () _llIlllIlII.RequiresLineOfSight = false _llIlllIlII.MaxActivationDistance = 0x1E end
 ) _lIIlllllll = math.max(_lllllIllIl, _llIlllIlII.HoldDuration + 0.2) end
 _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.E, false, game) if usarFire and _llIlllIlII and _llIlllIlII.Parent and fireproximityprompt then pcall(fireproximityprompt, _llIlllIlII) end
 task.wait(_lIIlllllll) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.E, false, game) end
 local function _IlllIlllIl() local _IIlIlIllIl = {} local _IIllIIllll = _llIllIlllI:FindFirstChild("\077\101\110\117\115") local _llIlllIIIl = _IIllIIllll and _IIllIIllll:FindFirstChild("\068\105\097\108\111\103\117\101") if not _llIlllIIIl or not _llIlllIIIl.Visible then return _IIlIlIllIl end
 for _, o in ipairs(_llIlllIIIl:GetDescendants()) do if o:IsA("\084\101\120\116\066\117\116\116\111\110") and o.Visible and o.AbsoluteSize.X > 0x0 and o.AbsoluteSize.Y > 0x0 and o.Text ~= "" then table.insert(_IIlIlIllIl, o) end
 end
 return _IIlIlIllIl end
 local function _IIllIlllII(trecho) for _, o in ipairs(_IlllIlllIl()) do if o.Text:lower():find(trecho, 0x1, true) then return o end
 end
 return nil end
 local function _lllIlllIIl() return #_IlllIlllIl() > 0x0 end
 local function _lIllIIIIIl(o) local _IIlllIIIIl = o.AbsolutePosition + o.AbsoluteSize / 0x2 local _lIllIIIIIl, _llllIlllII = _IIlllIIIIl.X, _IIlllIIIIl.Y + _lIIlIllllI() _lIllIllllI:SendMouseMoveEvent(_lIllIIIIIl, _llllIlllII, game) task.wait(0.05) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x0) task.wait(0.05) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x0) end
 local function _lIIllIlllI() local _llIIIIIlll, melhorNota for _, _IIllIIIIIl in ipairs(workspace:GetDescendants()) do if _IIllIIIIIl:IsA("\080\114\111\120\105\109\105\116\121\080\114\111\109\112\116") and _IIllIIIIIl.Enabled then local _lIllIIlIII, _IlIlIIIIlI = _IIllIIIIIl.Parent, nil if _lIllIIlIII and _lIllIIlIII:IsA("\066\097\115\101\080\097\114\116") then _IlIlIIIIlI = _lIllIIlIII.Position elseif _lIllIIlIII and _lIllIIlIII:IsA("\065\116\116\097\099\104\109\101\110\116") then _IlIlIIIIlI = _lIllIIlIII.WorldPosition elseif _lIllIIlIII and _lIllIIlIII:IsA("\077\111\100\101\108") then _IlIlIIIIlI = _lIllIIlIII:GetPivot().Position end
 if _IlIlIIIIlI then local _llIllllllI = (_IlIlIIIIlI - _lIIIIlllII).Magnitude local _IllIIIIIII = (_IIllIIIIIl.ActionText .. "\032" .. _IIllIIIIIl.ObjectText):lower() local _IlIlIlllIl = _IllIIIIIII:find("\099\097\118\097\108\111", 0x1, true) or _IllIIIIIII:find("\104\111\114\115\101", 0x1, true) if _llIllllllI < 0x19 and not _IlIlIlllIl then local _llIlIlIIII = _llIllllllI if _IllIIIIIII:find("\102\097\108\097\114", 0x1, true) or _IllIIIIIII:find("\116\097\108\107", 0x1, true) then _llIlIlIIII = _llIlIlIIII - 0x64 end
 if not melhorNota or _llIlIlIIII < melhorNota then _llIIIIIlll, melhorNota = _IIllIIIIIl, _llIlIlIIII end
 end
 end
 end
 end
 return _llIIIIIlll end
 local function _lIlIllIIIl() for _lIIIllIlll = 0x1, 0x5 do if not _IIlIIIIIIl then return false end
 local _llIlllIlII = _lIIIlIIIII(_lIIllIlllI, 0x3, 0.3) _IllIlIlIlI({ _llIlllIlII = _llIlllIlII }, false) local _llIllIIIlI = _lIIIlIIIII(_lllIlllIIl, 1.2, 0.05) if not _llIllIIIlI and _llIlllIlII and fireproximityprompt then pcall(fireproximityprompt, _llIlllIlII) _llIllIIIlI = _lIIIlIIIII(_lllIlllIIl, 1.5, 0.05) end
 if _llIllIIIlI then return true end
 task.wait(0.3) end
 return false end
 local function _lIlIIIIIll() local _llllllIlll = os.clock() + 0xC local _lIllIIlIII = false while _IIlIIIIIIl and os.clock() < _llllllIlll do local _IIlIlIllIl = _IlllIlllIl() if #_IIlIlIllIl == 0x0 then if _lIllIIlIII then return true end
 task.wait(0.1) else local _lllllIlIlI = _IIllIlllII("\103\104\111\115\116\032\118\105\115\105\111\110") local _IIllIllIlI = _IIllIlllII("\099\108\111\115\101") if _lllllIlIlI then _lIllIIIIIl(_lllllIlIlI); _lIllIIlIII = true; task.wait(0.4) elseif _IIllIllIlI then _lIllIIIIIl(_IIllIllIlI); _lIllIIlIII = true; task.wait(0.4) else task.wait(0.5) end
 end
 end
 return false end
 local function _IIIIIllIII() local _IIlIlIllIl = {} local _IIIlIlIIll = _llIllIlllI:FindFirstChild("\080\114\111\109\112\116\115") local _lIIIlllIIl = _IIIlIlIIll and _IIIlIlIIll:FindFirstChild("\066\117\116\116\111\110\082\101\097\099\116\105\111\110\071\097\109\101") local _IlIIllllII = _lIIIlllIIl and _lIIIlllIIl:FindFirstChild("\066\117\116\116\111\110\115") if not _IlIIllllII or not _lIIIlllIIl.Visible then return _IIlIlIllIl end
 for _, o in ipairs(_IlIIllllII:GetDescendants()) do if o:IsA("\071\117\105\066\117\116\116\111\110") and o.Visible and o.AbsoluteSize.X > 0x0 and o.AbsoluteSize.Y > 0x0 then table.insert(_IIlIlIllIl, o) end
 end
 return _IIlIlIllIl end
 local _IIlIIlIlII = setmetatable({}, { __mode = "\107" }) local function _IllIlIllll(o, repetido) local _IIlllIIIIl = o.AbsolutePosition + o.AbsoluteSize / 0x2 local _lIllIIIIIl, _llllIlllII = _IIlllIIIIl.X, _IIlllIIIIl.Y + _lIIlIllllI() _lIllIllllI:SendMouseMoveEvent(_lIllIIIIIl, _llllIlllII, game) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x0) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x0) if repetido and _IlllIIlIlI and firesignal then pcall(firesignal, o.MouseButton1Click) pcall(firesignal, o.Activated) end
 end
 local _lIllllIlll = nil local _IllIlIIIlI = {} local function _IllllllIll(o) if o.Name == "\083\104\111\112\073\110\116\101\114\097\099\116\105\111\110\080\097\114\116" then _IllIlIIIlI[o] = true end
 end
 workspace.DescendantAdded:Connect(_IllllllIll) workspace.DescendantRemoving:Connect( function (o) _IllIlIIIlI[o] = nil end
 ) task.spawn( function () for _, o in ipairs(workspace:GetDescendants()) do _IllllllIll(o) end
 end
 ) local function _lIIllllIlI(_IlIlIIIIlI) for shop in pairs(_IllIlIIIlI) do if shop and shop.Parent then if (shop.Position - _IlIlIIIIlI).Magnitude < 0x14 then return true end
 end
 end
 return false end
 local function _IIlIIlIlIl(_lllIIIlIIl) local _IlIllIIllI = _lIllIIIIIl if not _IlIllIIllI then return nil end
 local _llIIIIIlll, md, vistos = nil, nil, {} for _, _IIllIIIIIl in ipairs(workspace:GetDescendants()) do if _IIllIIIIIl.Name == "\071\104\111\115\116\083\109\111\107\101" then local _llllIIllIl = _IIllIIIIIl.Parent while _llllIIllIl and _llllIIllIl ~= workspace do if _llllIIllIl:IsA("\077\111\100\101\108") and _llllIIllIl.Name:match(_IlIIlllllI) then break end
 _llllIIllIl = _llllIIllIl.Parent end
 if _llllIIllIl and _llllIIllIl ~= workspace and not vistos[_llllIIllIl] and not _lllIIIlIIl[_llllIIllIl] then vistos[_llllIIllIl] = true local _IIllllllII = _llllIIllIl:FindFirstChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") or _llllIIllIl.PrimaryPart or _llllIIllIl:FindFirstChildWhichIsA("\066\097\115\101\080\097\114\116", true) local _lllIlIlIll = _IIllIIIIIl.Parent:IsA("\066\097\115\101\080\097\114\116") and _IIllIIIIIl.Parent or _IIllllllII if _lllIlIlIll then if _lIIllllIlI(_lllIlIlIll.Position) then continue end
 local _llIllllllI = (_lllIlIlIll.Position - _IlIllIIllI.Position).Magnitude if not md or _llIllllllI < md then _llIIIIIlll, md = { modelo = _llllIIllIl, _IIllllllII = _IIllllllII or _lllIlIlIll, _lllIlIlIll = _lllIlIlIll, _llIlllIlII = _llllIIllIl:FindFirstChildWhichIsA("\080\114\111\120\105\109\105\116\121\080\114\111\109\112\116", true), }, _llIllllllI end
 end
 end
 end
 end
 return _llIIIIIlll end
 if _llllIIllIl and _llllIIllIl ~= workspace and not vistos[_llllIIllIl] and not _lllIIIlIIl[_llllIIllIl] then vistos[_llllIIllIl] = true local _IIllllllII = _llllIIllIl:FindFirstChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") or _llllIIllIl.PrimaryPart or _llllIIllIl:FindFirstChildWhichIsA("\066\097\115\101\080\097\114\116", true) local _lllIlIlIll = _IIllIIIIIl.Parent:IsA("\066\097\115\101\080\097\114\116") and _IIllIIIIIl.Parent or _IIllllllII if _lllIlIlIll then local _llIllllllI = (_lllIlIlIll.Position - _IlIllIIllI.Position).Magnitude if not md or _llIllllllI < md then _llIIIIIlll, md = { modelo = _llllIIllIl, _IIllllllII = _IIllllllII or _lllIlIlIll, _lllIlIlIll = _lllIlIlIll, _llIlllIlII = _llllIIllIl:FindFirstChildWhichIsA("\080\114\111\120\105\109\105\116\121\080\114\111\109\112\116", true), }, _llIllllllI end
 end
 end
 end
 end
 return _llIIIIIlll end
 local function _llIlIIlIII(_IIlIlIIllI) return ( not _IIlIlIIllI.modelo.Parent) or ( not _IIlIlIIllI.parte.Parent) or ( not _IIlIlIIllI.modelo:FindFirstChild("\071\104\111\115\116\083\109\111\107\101", true)) end
 local function _lIlIIIllll(_IIlIlIIllI) local _IlIllIIllI = _lIllIIIIIl if _IlIllIIllI and _IIlIlIIllI.parte and _IIlIlIIllI.parte.Parent then local _IIIlIlIlII = _IIlIlIIllI.parte.Position _IlIllIIllI.CFrame = CFrame.lookAt(_IIIlIlIlII + _lllIlIIlIl, _IIIlIlIlII) _IlIllIIllI.AssemblyLinearVelocity = Vector3.zero end
 end
 local function _IIIIllllll(_IIlIlIIllI) local _IlIllIIllI = _lIllIIIIIl if _IlIllIIllI and _IIlIlIIllI.parte and _IIlIlIIllI.parte.Parent then if (_IlIllIIllI.Position - _IIlIlIIllI.parte.Position).Magnitude > 0xC then _lIlIIIllll(_IIlIlIIllI) end
 end
 end
 local function _lllIlIlllI(_IIlIlIIllI, prazo) local _llllllIlll = os.clock() + _IIllIlIlII local _lIIIllIlll = 0x0 while _IIlIIIIIIl and os.clock() < _llllllIlll and not (prazo and os.clock() >= prazo) do _lIIIllIlll += 0x1 _lIlIIIllll(_IIlIlIIllI) task.wait(0.1) _IllIlIlIlI(_IIlIlIIllI, _lIIIllIlll >= 0x2) local _IIIIIIllIl = math.min(_llllllIlll, os.clock() + 0.6) if prazo then _IIIIIIllIl = math.min(_IIIIIIllIl, prazo) end
 while _IIlIIIIIIl and os.clock() < _IIIIIIllIl do if #_IIIIIllIII() > 0x0 then return true end
 task.wait(0.03) end
 end
 return false end
 local function _IllIlIIlll(_lllIIIlIIl, prazo) for _ = 0x1, 0x8 do if ( not _IIlIIIIIIl) or (prazo and os.clock() >= prazo) then return nil end
 local _IIlIlIIllI = _lIIIlIIIII( function () return _IIlIIlIlIl(_lllIIIlIIl) end
 , 0x8, 0.2, prazo) if not _IIlIlIIllI then return nil end
 if _lllIlIlllI(_IIlIlIIllI, prazo) then return _IIlIlIIllI end
 _lllIIIlIIl[_IIlIlIIllI.modelo] = true end
 return nil end
 local function _IllIlIIIIl() local _lllIIIlIIl = {} _IllIlllllI(_lIIIIlllII) task.wait(0x1) if _lIlIllIIIl() then _lIlIIIIIll() else task.wait(0x1) end
 if not _IIlIIIIIIl then return end
 task.wait(0.3) local _IIlIlIIllI = _IllIlIIlll(_lllIIIlIIl, nil) if not _IIlIlIIllI then task.wait(1.5) return end
 local _lllllIIIII = os.clock() + _IlIIIllIII local _IIIIIllIII, falhas = nil, 0x0 while _IIlIIIIIIl and os.clock() < _lllllIIIII do local _lIllllIlIl = #_IIIIIllIII() if _lIllllIlIl > 0x0 then _IIIIIllIII, falhas = nil, 0x0 if _IIlllIlIll and not _llIlIIlIII(_IIlIlIIllI) then _IIIIllllll(_IIlIlIIllI) end
 elseif _llIlIIlIII(_IIlIlIIllI) then _IIIIIllIII, falhas = nil, 0x0 _lllIIIlIIl[_IIlIlIIllI.modelo] = true local _IlllIIIIll = _IllIlIIlll(_lllIIIlIIl, _lllllIIIII) if _IlllIIIIll then _IIlIlIIllI = _IlllIIIIll else _lllIIIlIIl = {} end
 else _IIIIIllIII = _IIIIIllIII or os.clock() if os.clock() - _IIIIIllIII > 0.5 then if _lllIlIlllI(_IIlIlIIllI, _lllllIIIII) then falhas = 0x0 else falhas += 0x1 if falhas >= 0x2 then _lllIIIlIIl[_IIlIlIIllI.modelo] = true local _IlllIIIIll = _IllIlIIlll(_lllIIIlIIl, _lllllIIIII) if _IlllIIIIll then _IIlIlIIllI = _IlllIIIIll else _lllIIIlIIl = {} end
 falhas = 0x0 end
 end
 _IIIIIllIII = nil end
 end
 task.wait(0.05) end
 if _IIlIIIIIIl then _IllIlllllI(_lIIIIlllII) task.wait(0x1) end
 end
 _lllllIlIlI = function () _IIlIIIIIIl = false _lIllIllllI += 0x1 if _lIllllIlll then _lIllllIlll:Disconnect(); _lIllllIlll = nil end
 _IIlIIlIlII = setmetatable({}, { __mode = "\107" }) end
 local function _IllIIllIII() _lllllIlIlI() _IIlIIIIIIl = true local _IIIIlllllI = _lIllIllllI _lIllllIlll = RunService.Heartbeat:Connect( function () if not _IIlIIIIIIl then return end
 local _IlIIIlIIIl = os.clock() for _, _llIlIlIIIl in ipairs(_IIIIIllIII()) do local _IlIlIllllI = _IIlIIlIlII[_llIlIlIIIl] if not _IlIlIllllI then _IIlIIlIlII[_llIlIlIIIl] = _IlIIIlIIIl task.spawn(_IllIlIllll, _llIlIlIIIl, false) elseif _IlIIIlIIIl - _IlIlIllllI >= _lIIllIllII then _IIlIIlIlII[_llIlIlIIIl] = _IlIIIlIIIl task.spawn(_IllIlIllll, _llIlIlIIIl, true) end
 end
 end
 ) local _IllllllIII = 0x2 local function _IllIlIlIlI(_IIlIlIIllI, usarFire) local _lIIlllllll = _lllllIllIl local _llIlllIlII = _IIlIlIIllI and _IIlIlIIllI.prompt if _llIlllIlII and _llIlllIlII.Parent then pcall( function () _llIlllIlII.RequiresLineOfSight = false _llIlllIlII.MaxActivationDistance = 0x1E end
 ) _lIIlllllll = math.max(_lllllIllIl, _llIlllIlII.HoldDuration + 0.2) end
 task.wait(_IllllllIII) if not _IIlIIIIIIl then return end
 _lIllIllllI:SendKeyEvent(true, Enum.KeyCode.E, false, game) if usarFire and _llIlllIlII and _llIlllIlII.Parent and fireproximityprompt then pcall(fireproximityprompt, _llIlllIlII) end
 task.wait(_lIIlllllll) _lIllIllllI:SendKeyEvent(false, Enum.KeyCode.E, false, game) end
 local function _lllIlIlllI(_IIlIlIIllI, prazo) local _llllllIlll = os.clock() + _IIllIlIlII local _lIIIllIlll = 0x0 while _IIlIIIIIIl and os.clock() < _llllllIlll and not (prazo and os.clock() >= prazo) do _lIIIllIlll += 0x1 _lIlIIIllll(_IIlIlIIllI) task.wait(0.1) _IllIlIlIlI(_IIlIlIIllI, _lIIIllIlll >= 0x2) local _IIIIIIllIl = math.min(_llllllIlll, os.clock() + 0.6) if prazo then _IIIIIIllIl = math.min(_IIIIIIllIl, prazo) end
 while _IIlIIIIIIl and os.clock() < _IIIIIIllIl do if #_IIIIIllIII() > 0x0 then return true end
 task.wait(0.03) end
 end
 return false end
 local _IIlIllIllI = 0.1 local function _IllIlIllll(o, repetido) local _IIlllIIIIl = o.AbsolutePosition + o.AbsoluteSize / 0x2 local _lIllIIIIIl, _llllIlllII = _IIlllIIIIl.X, _IIlllIIIIl.Y + _lIIlIllllI() task.wait(_IIlIllIllI) if not (o and o.Parent and o.Visible) then return end
 _lIllIllllI:SendMouseMoveEvent(_lIllIIIIIl, _llllIlllII, game) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, true, game, 0x0) _lIllIllllI:SendMouseButtonEvent(_lIllIIIIIl, _llllIlllII, 0x0, false, game, 0x0) if repetido and _IlllIIlIlI and firesignal then pcall(firesignal, o.MouseButton1Click) pcall(firesignal, o.Activated) end
 end
 task.spawn( function () while _IIlIIIIIIl and _lIllIllllI == _IIIIlllllI do local _IlIIlIIIIl, err = pcall(_IllIlIIIIl) if not _IlIIlIIIIl then task.wait(1.5) end
 end
 end
 ) _IllIIIIIIl("\072\097\108\108\111\119\101\101\110", "\55357\56443\032\065\117\116\111\032\070\097\110\116\097\115\109\097\032\079\078") end
 local function _llIIIlllIl() _IllIllllll() _IllllIIlll() _IIlIIIIlIl() _lIIIIlllll() _IlIIlIlllI() _lllllIlIlI() _IIlllIlIll() _IIIlIIIlIl() _lllIlllIll = false if _IllIlIIlll then pcall( function () _IllIlIIlll:Set(false) end
 ) end
 _IllIIIIIIl("\083\104\117\116\100\111\119\110", "\084\117\100\111\032\112\097\114\097\100\111") end
 _lIIIllIlII = function () _IllllIIlll() _IIlIIIIlIl() _IIIlIIIlIl() end
 local _IIIIllIllI = nil _IllllIIlll = function () _IlllllIlIl = false if _IIIIllIllI then pcall( function () task.cancel(_IIIIllIllI) end
 ); _IIIIllIllI = nil end
 _IIlIllIIlI = false _IIlIlIIlIl() _lIlIlIlIIl() _IllIIlIlll(true) _IIIlIIIlIl() _IlIIlIllII() _llIllllIlI() _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032\079\102\102") end
 local function _lIlllIlIIl() local _IlllIIIlIl = os.clock() - _IIIIIIIllI while _IlllllIlIl do local _IIlllIIIIl = _IIlIIIIIIl() if not _IIlllIIIIl then if _lIlIIlIlIl then _IlllIIIlIl = _IlllIIIlIl or os.clock() if os.clock() - _IlllIIIlIl >= _IIIIIIIllI then if flyActive and _lIIIllIlIl and _lIIIllIlIl.Parent then _IllIIIIllI() end
 _IlllIIIlIl = nil else task.wait(0.5) end
 else task.wait(0x1) end
 else _IlllIIIlIl = nil if not flyActive or not _lIIIllIlIl or not _lIIIllIlIl.Parent then task.wait(0.1) continue end
 _IIIIllIlll(_IIlllIIIIl) end
 task.wait() end
 end
 local function _IIlIlIlIIl() _IllIllllll() _IllllIIlll() task.wait(0.1) _IlllllIlIl = true _lIIlIIllII() _llllllllll() _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032\079\110") _IIIIllIllI = task.spawn(_lIlllIlIIl) _IllIIIIIIl("\070\097\114\109", "\070\097\114\109\032\073\110\105\099\105\097\100\111") end
 local function _IIlIlIIIll(key) _IllIllllll() _IllllIIlll() task.wait(0.1) _IlIlIIIIII = key _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032" .. _lllIIIIlII[key].nome) _IllIIIIIIl("\067\111\114\114\105\100\097", _lllIIIIlII[key].nome) _lIIlIIllII() corridaThread = task.spawn( function () while _IlIlIIIIII == key do _llIlIllIII(_lllIIIIlII[key]) if _IlIlIIIIII ~= key then break end
 task.wait(0x1) end
 end
 ) end
 local _IIlIllIlll = _lIlllIIlIl:CreateTab("\083\116\097\116\117\115", nil) _IIlIllIlll:CreateSection("\082\101\097\108\045\084\105\109\101\032\073\110\102\111") _llIlIIllll = _IIlIllIlll:CreateLabel("\083\116\097\116\117\115\058\032\079\102\102") cLabel = _IIlIllIlll:CreateLabel("\080\111\105\110\116\115\032\105\110\032\114\097\100\105\117\115\058\032\048") aLabel = _IIlIllIlll:CreateLabel("\065\110\116\105\045\065\070\075\058\032\079\102\102") cavLabel = _IIlIllIlll:CreateLabel("\072\111\114\115\101\058\032\079\102\102") task.spawn( function () while true do task.wait(0x2) _llIIIIIIlI(cLabel, "\080\111\105\110\116\115\032\105\110\032\114\097\100\105\117\115\058\032" .. _lIlIlIIllI()) end
 end
 ) local _IIlllIIlIl = _lIlllIIlIl:CreateTab("\070\097\114\109", nil) _IIlllIIlIl:CreateButton({ Name = "\073\078\073\067\073\065\082\032\070\076\089\032\070\065\082\077", Callback = function () if _IlllllIlIl then _IllllIIlll() _IllIIIIIIl("\070\097\114\109", "\070\097\114\109\032\112\097\114\097\100\111") else _IIlIlIlIIl() end
 end
 }) _IIlllIIlIl:CreateSection("\077\105\115\115\227\111\032\065\117\116\111\109\225\116\105\099\097") _IIlllIIlIl:CreateDropdown({ Name = "\077\105\115\115\227\111\032\112\097\114\097\032\099\108\105\099\097\114", Options = {"\083\105\110\103\108\101\032\083\116\097\107\101", "\066\105\103\032\084"}, CurrentOption = {"\083\105\110\103\108\101\032\083\116\097\107\101"}, MultipleOptions = false, Flag = "\109\105\115\115\097\111\068\114\111\112\100\111\119\110", Callback = function (opt) local _lIllIIlIlI = type(opt) == "\116\097\098\108\101" and opt[0x1] or opt if _lIllIIlIlI then _lIlllIlIII = _lIllIIlIlI end
 end
 }) _IIlllIIlIl:CreateToggle({ Name = "\084\101\108\101\112\111\114\116\097\114\032\097\116\233\032\097\115\032\099\111\111\114\100\101\110\097\100\097\115", CurrentValue = false, Flag = "\116\101\108\101\112\111\114\116\101\077\105\115\115\097\111\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) _lIllIlIIIl = _lIllIIlIlI end
 }) _IIlllIIlIl:CreateSection("\067\111\114\114\105\100\097\115") local _llIllllllI, togRiver _llIllllllI = _IIlllIIlIl:CreateToggle({ Name = "\067\114\111\115\115\032\067\111\117\110\116\114\121", CurrentValue = false, Flag = "\099\114\111\115\115\076\111\111\112\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if not _lIllIIlIlI then if _IlIlIIIIII == "\099\114\111\115\115" then _IIlIlIIlIl() _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032\079\102\102") _IllIIIIIIl("\067\111\114\114\105\100\097", "\067\114\111\115\115\032\067\111\117\110\116\114\121\032\112\097\114\097\100\097") end
 return end
 if togRiver then pcall( function () togRiver:Set(false) end
 ) end
 _IIlIlIIIll("\099\114\111\115\115") end
 }) togRiver = _IIlllIIlIl:CreateToggle({ Name = "\066\101\103\105\110\032\082\105\118\101\114\032\082\117\110", CurrentValue = false, Flag = "\114\105\118\101\114\076\111\111\112\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if not _lIllIIlIlI then if _IlIlIIIIII == "\114\105\118\101\114" then _IIlIlIIlIl() _llIIIIIIlI(_llIlIIllll, "\083\116\097\116\117\115\058\032\079\102\102") _IllIIIIIIl("\067\111\114\114\105\100\097", "\066\101\103\105\110\032\082\105\118\101\114\032\082\117\110\032\112\097\114\097\100\097") end
 return end
 if _llIllllllI then pcall( function () _llIllllllI:Set(false) end
 ) end
 _IIlIlIIIll("\114\105\118\101\114") end
 }) _IIlllIIlIl:CreateSection("\067\111\110\102\105\103\117\114\097\231\245\101\115") _IIlllIIlIl:CreateSlider({ Name = "\070\108\121\032\083\112\101\101\100", Range = {0x5, 0x12C}, Increment = 0x5, CurrentValue = 0x32, Flag = "\115\112\101\101\100\083\108\105\100\101\114", Callback = function (_lIllIIlIlI) _IIlIIlIlll = _lIllIIlIlI end
 }) local _lllIIllIlI = _lIlllIIlIl:CreateTab("\072\097\108\108\111\119\101\101\110", nil) _lllIIllIlI:CreateSection("\072\097\108\108\111\119\101\101\110\032\070\097\114\109") local _IIIIIIlIII, togBicho, togFant _IIIIIIlIII = _lllIIllIlI:CreateToggle({ Name = "\55356\57219\032\065\117\116\111\032\065\098\243\098\111\114\097", CurrentValue = false, Flag = "\097\098\111\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if _lIllIIlIlI then if togBicho then pcall( function () togBicho:Set(false) end
 ) end
 if togFant then pcall( function () togFant:Set(false) end
 ) end
 _IllllIIlIl() else _lIIIIlllll() end
 end
 }) togBicho = _lllIIllIlI:CreateToggle({ Name = "\55358\56756\032\066\105\099\104\111", CurrentValue = false, Flag = "\098\105\099\104\111\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if _lIllIIlIlI then if _IIIIIIlIII then pcall( function () _IIIIIIlIII:Set(false) end
 ) end
 if togFant then pcall( function () togFant:Set(false) end
 ) end
 _IIllllIlll() else _IlIIlIlllI() end
 end
 }) togFant = _lllIIllIlI:CreateToggle({ Name = "\55357\56443\032\065\117\116\111\032\070\097\110\116\097\115\109\097", CurrentValue = false, Flag = "\102\097\110\116\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if _lIllIIlIlI then if _IIIIIIlIII then pcall( function () _IIIIIIlIII:Set(false) end
 ) end
 if togBicho then pcall( function () togBicho:Set(false) end
 ) end
 _IllIIllIII() else _lllllIlIlI() end
 end
 }) _lllIIllIlI:CreateSection("\086\101\108\111\099\105\100\097\100\101") _lllIIllIlI:CreateSlider({ Name = "\083\112\101\101\100\032\086\111\111\032\040\065\098\243\098\111\114\097\047\066\105\099\104\111\041", Range = {0xA, 0x1F4}, Increment = 0xA, CurrentValue = 0x96, Flag = "\115\112\101\101\100\067\070\114\097\109\101\083\108\105\100\101\114", Callback = function (_lIllIIlIlI) _IIlIIlllII = _lIllIIlIlI end
 }) local _lIllIIIlIl = _lIlllIIlIl:CreateTab("\072\111\114\115\101\115", nil) _lIllIIIlIl:CreateToggle({ Name = "\086\111\097\114\032\097\116\101\032\087\105\108\100\032\072\111\114\115\101", CurrentValue = false, Flag = "\099\097\118\097\108\111\119\104\105", Callback = function (_lIllIIlIlI) if _lIllIIlIlI then _IlIlllIIlI() _IIllllIIll() else _IIlIIIIlIl() end
 end
 }) _lIllIIIlIl:CreateSlider({ Name = "\083\112\101\101\100\032\040\118\111\097\114\032\097\116\101\032\111\032\099\097\118\097\108\111\041", Range = {0x46, 0x12C}, Increment = 0x5, CurrentValue = 0x46, Flag = "\104\111\114\115\101\102\108\121\115\112\101\101\100\119\104\105", Callback = function (_lIllIIlIlI) _llIlllllll = _lIllIIlIlI end
 }) _IllIlIIlll = _lIllIIIlIl:CreateToggle({ Name = "\065\117\116\111\032\067\108\105\099\107\032\040\049\115\041", CurrentValue = false, Flag = "\097\117\116\111\067\108\105\099\107\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) _lllIlllIll = _lIllIIlIlI end
 }) local _IlllIIIlII = _lIlllIIlIl:CreateTab("\085\116\105\108\115", nil) _IlllIIIlII:CreateToggle({ Name = "\065\110\116\105\045\065\070\075", CurrentValue = false, Flag = "\097\102\107\084\111\103\103\108\101", Callback = function (_lIllIIlIlI) if _lIllIIlIlI then _IlIIIlIlIl(); _llIIIIIIlI(aLabel, "\065\110\116\105\045\065\070\075\058\032\079\110") else _IIlllIlIll(); _llIIIIIIlI(aLabel, "\065\110\116\105\045\065\070\075\058\032\079\102\102") end
 end
 }) _IlllIIIlII:CreateButton({ Name = "\080\065\082\065\082\032\084\085\068\079", Callback = function () _llIIIlllIl() end
 }) _lllIIIlIll.CharacterAdded:Connect( function (nc) _IIIIlIIllI = nc _lIllIIIIIl = nc:WaitForChild("\072\117\109\097\110\111\105\100\082\111\111\116\080\097\114\116") _IIIlllllII = nc:WaitForChild("\072\117\109\097\110\111\105\100") _IllllIIlll() _IIlIIIIlIl() end
 ) _IllIIIIIIl("\087\072\073\032\070\097\114\109\032\118\049\050", "\065\098\243\098\111\114\097\032\040\099\108\105\113\117\101\032\052\050\056\047\050\051\041\032\043\032\066\105\099\104\111\032\043\032\070\097\110\116\097\115\109\097") end
 )(...)
