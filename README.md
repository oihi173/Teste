--[[ Protected by Lua Guard ]]

( function (...) local Players=game:GetService(string.char(0x50,0x6C,0x61,0x79,0x65,0x72,0x73)) local RunService=game:GetService(string.char(0x52,0x75,0x6E,0x53,0x65,0x72,0x76,0x69,0x63,0x65)) local TweenService=game:GetService(string.char(0x54,0x77,0x65,0x65,0x6E,0x53,0x65,0x72,0x76,0x69,0x63,0x65)) local _lllIllIIlI=game:GetService(string.char(0x56,0x69,0x72,0x74,0x75,0x61,0x6C,0x49,0x6E,0x70,0x75,0x74,0x4D,0x61,0x6E,0x61,0x67,0x65,0x72)) local GuiService=game:GetService(string.char(0x47,0x75,0x69,0x53,0x65,0x72,0x76,0x69,0x63,0x65)) local _IIllllllII=Players.LocalPlayer local _IlIlllIllI=_IIllllllII.Character or _IIllllllII.CharacterAdded:Wait() local _IllIIIIIII=_IlIlllIllI:WaitForChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74)) local _lIlIlIllll=_IlIlllIllI:WaitForChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) local _IIIllIIlIl=_IIllllllII:WaitForChild(string.char(0x50,0x6C,0x61,0x79,0x65,0x72,0x47,0x75,0x69)) local _IllIllllII=loadstring(game:HttpGet(string.char(0x68,0x74,0x74,0x70,0x73,0x3A,0x2F,0x2F,0x73,0x69,0x72,0x69,0x75,0x73,0x2E,0x6D,0x65,0x6E,0x75,0x2F,0x72,0x61,0x79,0x66,0x69,0x65,0x6C,0x64)))() local _lllIIIlllI=_IllIllllII:CreateWindow({Name=string.char(0x57,0x48,0x49,0x20,0x46,0x61,0x72,0x6D,0x20,0x76,0x39),LoadingTitle=string.char(0x57,0x48,0x49,0x20,0x46,0x61,0x72,0x6D),LoadingSubtitle=string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E,0x20,0x69,0x6E,0x74,0x65,0x67,0x72,0x61,0x64,0x6F),ConfigurationSaving={Enabled=false},Discord={Enabled=false},KeySystem=false,}) local _IIllllIIlI=false local _IIlIIIIIlI=0x32 local _lllllllIlI=0x2BC local _llIIllllII=0x3 local _IlllIIlIII=false local _IllIIIIllI=true local _IIlllIlIlI=true local _IIIIIIllII=0x14 local _IlIIllIIII=0x3 local _IllllllIIl=0xA local _llllIlllIl,cavaloConn=nil,nil local _llIIIlIlll=Vector3.new(3595.69,21.00,-6875.07) local _lIIIIllIll=Vector3.new(3636.73,21.00,-6899.10) local _llIllllIll=true local _IIlIIIIIll=string.char(0x53,0x69,0x6E,0x67,0x6C,0x65,0x20,0x53,0x74,0x61,0x6B,0x65) local _IlIIlIlIlI=0x3 local _IIIIlIlIII=false local _llllIllIIl=string.char(0x61,0x75,0x74,0x6F) local _IlIlIIIlII=string.char(0x61,0x6D,0x62,0x6F,0x73) local _lIlIlIlllI=true local _lIIIIlIIlI=true local _llIIIIllIl,AJUSTE_Y=0x0,0x0 local _IllIlIllIl=false local _IlIIlIlIII={cross={_llIlIIIllI=string.char(0x43,0x72,0x6F,0x73,0x73,0x20,0x43,0x6F,0x75,0x6E,0x74,0x72,0x79),_lIIIIIIlII=Vector3.new(3674.61,21.00,-7141.42)},river={_llIlIIIllI=string.char(0x42,0x65,0x67,0x69,0x6E,0x20,0x52,0x69,0x76,0x65,0x72,0x20,0x52,0x75,0x6E),_lIIIIIIlII=Vector3.new(3708.41,16.32,-6400.22)},} local _IIIlllIIIl=0xA local _llIIllIIlI=0xF0 local _llIIllIlll=0x7D0 local _IIllIlIIlI,corridaConn,alvoCorrida=false,nil,nil local _lIlllllIII=Vector3.new(3678.48,25.50,-7140.38) local _IlIIllllIl=Vector3.new(3706.19,19.86,-6396.10) local _IIlllIIlll=0x3 local _lIlIIIlIIl=0x3 local _IIlIIIIIlI,treinoThread=nil,nil local _IIIIIIIIII,ultimoPulo=0.3,0x0 local function _IllIIlIlIl(title,content) if _llIIllllII<=0x0 then return end
 _IllIllllII:Notify({Title=title,Content=content,Duration=_llIIllllII,Image=nil}) end
 local _llIIIlIlll,cLabel,aLabel,cavLabel local function _IIIlIllllI(lbl,_lllIIIIIlI) if lbl then pcall( function ()lbl:Set(_lllIIIIIlI) end
 ) end
 end
 local _IIIllIlllI= function () end
 local _IIIlIlIlIl= function () end
 local _lIllllIllI= function () end
 local _IIlllllIIl= function () end
 local _IllIIIIIIl= function () end
 local _IIllIllIll= function () end
 local _IIlIlllIll={[string.char(0x4E,0x6F,0x64,0x65)]=true,[string.char(0x53,0x68,0x6F,0x70,0x49,0x6E,0x74,0x65,0x72,0x61,0x63,0x74,0x69,0x6F,0x6E,0x50,0x61,0x72,0x74)]=true,[string.char(0x42,0x6F,0x75,0x6E,0x64,0x73)]=true,[string.char(0x43,0x6F,0x6D,0x70,0x65,0x74,0x69,0x74,0x69,0x76,0x65,0x52,0x61,0x63,0x65,0x53,0x74,0x61,0x6D,0x69,0x6E,0x61,0x42,0x6F,0x6F,0x73,0x74)]=true,[string.char(0x43,0x6F,0x6D,0x70,0x65,0x74,0x69,0x74,0x69,0x76,0x65,0x52,0x61,0x63,0x65,0x53,0x70,0x65,0x65,0x64,0x42,0x6F,0x6F,0x73,0x74)]=true,[string.char(0x42,0x6F,0x75,0x6E,0x64)]=true,[string.char(0x53,0x6C,0x69,0x64,0x65,0x50,0x61,0x72,0x74)]=true,} local _IlIlIlIIII={[string.char(0x43,0x6F,0x6D,0x70,0x65,0x74,0x69,0x74,0x69,0x76,0x65,0x52,0x61,0x63,0x65,0x49,0x74,0x65,0x6D)]=true,[string.char(0x42,0x69,0x6C,0x6C,0x62,0x6F,0x61,0x72,0x64)]=true,[string.char(0x57,0x69,0x6E,0x64,0x20,0x74,0x75,0x72,0x62,0x69,0x6E,0x65)]=true,[string.char(0x52,0x65,0x77,0x61,0x72,0x64,0x50,0x69,0x63,0x6B,0x75,0x70,0x4E,0x6F,0x64,0x65,0x73)]=true,} local _lIlIlllIlI={[Enum.Material.Glass]=true,[Enum.Material.ForceField]=true,} local function _IIIIlIlIII(o) if not o or not o.Parent then return false end
 if not o:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then return false end
 if not o:FindFirstChildOfClass(string.char(0x54,0x6F,0x75,0x63,0x68,0x54,0x72,0x61,0x6E,0x73,0x6D,0x69,0x74,0x74,0x65,0x72)) then return false end
 if _IIlIlllIll[o.Name] then return false end
 if o.Parent and _IlIlIlIIII[o.Parent.Name] then return false end
 if _lIlIlllIlI[o.Material] then return false end
 local _lIlIlIlllI=o.Name:lower() if _lIlIlIlllI:find(string.char(0x62,0x6F,0x75,0x6E,0x64)) or _lIlIlIlllI:find(string.char(0x6E,0x6F,0x64,0x65)) or _lIlIlIlllI:find(string.char(0x73,0x68,0x6F,0x70)) or _lIlIlIlllI:find(string.char(0x62,0x6F,0x6F,0x73,0x74)) or _lIlIlIlllI:find(string.char(0x73,0x6C,0x69,0x64,0x65)) then return false end
 if o.Parent then local _lIIllIIIlI=o.Parent.Name:lower() if _lIIllIIIlI:find(string.char(0x63,0x6F,0x6D,0x70,0x65,0x74,0x69,0x74,0x69,0x76,0x65,0x72,0x61,0x63,0x65)) then return false end
 end
 return true end
 local _IlIllIIlll={}workspace.DescendantAdded:Connect( function (o)task.defer( function () if _IIIIlIlIII(o) then _IlIllIIlll[o]=true end
 end
 ) end
 )workspace.DescendantRemoving:Connect( function (o)_IlIllIIlll[o]=nil end
 )task.spawn( function () for _,o in ipairs(workspace:GetDescendants()) do if _IIIIlIlIII(o) then _IlIllIIlll[o]=true end
 end
 end
 ) local function _IIIlIIIIll() local _lIllIlllIl,bestDist=nil,math.huge local _IIIlllllIl=_IllIIIIIII.Position for o in pairs(_IlIllIIlll) do if o and o.Parent then local _llIlllIlIl=(_IIIlllllIl-o.Position).Magnitude if _llIlllIlIl<=_lllllllIlI and _llIlllIlIl<bestDist then bestDist,_lIllIlllIl=_llIlllIlIl,o end
 end
 end
 return _lIllIlllIl end
 local function _IIlllllIII(raio) local _lIllIlllIl,bestDist=nil,math.huge local _lIIIIIIlII=_IllIIIIIII.Position for o in pairs(_IlIllIIlll) do if o and o.Parent then local _llIlllIlIl=(_lIIIIIIlII-o.Position).Magnitude if _llIlllIlIl<=raio and _llIlllIlIl<bestDist then bestDist,_lIllIlllIl=_llIlllIlIl,o end
 end
 end
 return _lIllIlllIl end
 local function _lIlIIlIIll() local _IIIIlllllI,_IIIlllllIl=0x0,_IllIIIIIII.Position for o in pairs(_IlIllIIlll) do if o and o.Parent and (_IIIlllllIl-o.Position).Magnitude<=_lllllllIlI then _IIIIlllllI+=0x1 end
 end
 return _IIIIlllllI end
 local function _lIlIllIIII() for _,_lIIlIlllII in ipairs(workspace:GetDescendants()) do if _lIIlIlllII:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) and _lIIlIlllII~=_IlIlllIllI and _lIIlIlllII:FindFirstChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) and _lIIlIlllII:FindFirstChild(string.char(0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74)) then if (_lIIlIlllII.RootPart.Position-_IllIIIIIII.Position).Magnitude<0xF then return _lIIlIlllII.RootPart,_lIIlIlllII end
 end
 end
 return nil,nil end
 local _lIIlIllIIl local function _lIIIlIlIII() if _lIIlIllIIl then return end
 _lIIlIllIIl=_IIllllllII.Idled:Connect( function () local _IllIlllllI,vu=pcall( function () return game:GetService(string.char(0x56,0x69,0x72,0x74,0x75,0x61,0x6C,0x55,0x73,0x65,0x72)) end
 ) if _IllIlllllI and vu then vu:CaptureController();vu:ClickButton2(Vector2.new()) end
 end
 ) end
 local function _lIllIIIllI() if _lIIlIllIIl then _lIIlIllIIl:Disconnect();_lIIlIllIIl=nil end
 end
 local _lIIllIlllI,flyConn,flyActive=nil,nil,false local function _lllIllIlII() local _llllIIlIlI=Instance.new(string.char(0x50,0x61,0x72,0x74))_llllIIlIlI.Size,_llllIIlIlI.Transparency,_llllIIlIlI.Anchored,_llllIIlIlI.CanCollide=Vector3.new(0x2,0x1,0x2),0x1,true,false _llllIIlIlI.CFrame,_llllIIlIlI.Parent=_IllIIIIIII.CFrame,workspace return _llllIIlIlI end
 local function _lIlIllIlIl() if flyActive then return end
 flyActive=true _lIIllIlllI=_lllIllIlII() local _lIlIIIIlIl=_IlIlllIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand=true end
 if flyConn then pcall( function ()flyConn:Disconnect() end
 ) end
 flyConn=RunService.Heartbeat:Connect( function () if _lIIllIlllI and _lIIllIlllI.Parent then _IllIIIIIII.CFrame=_lIIllIlllI.CFrame end
 end
 ) end
 local function _IIIIIlllIl()flyActive=false if flyConn then flyConn:Disconnect();flyConn=nil end
 if _lIIllIlllI then _lIIllIlllI:Destroy();_lIIllIlllI=nil end
 for _,o in ipairs(_IllIIIIIII:GetChildren()) do if o:IsA(string.char(0x42,0x6F,0x64,0x79,0x56,0x65,0x6C,0x6F,0x63,0x69,0x74,0x79)) or o:IsA(string.char(0x42,0x6F,0x64,0x79,0x47,0x79,0x72,0x6F)) or o:IsA(string.char(0x42,0x6F,0x64,0x79,0x50,0x6F,0x73,0x69,0x74,0x69,0x6F,0x6E)) then pcall( function ()o:Destroy() end
 ) end
 end
 local _lIlIIIIlIl=_IlIlllIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand=false end
 end
 local function _IlIIIlIIII(destination) if not _lIIllIlllI or not _lIIllIlllI.Parent then return end
 local _IIlIlllIll=(_lIIllIlllI.Position-destination).Magnitude if _IIlIlllIll<0x1 then return end
 local _lllIlIlIIl=TweenService:Create(_lIIllIlllI,TweenInfo.new(_IIlIlllIll/_IIlIIIIIlI,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),{CFrame=CFrame.new(destination)})_lllIlIlIIl:Play();_lllIlIlIIl.Completed:Wait() end
 local _lllIlIIIll=nil local function _lIIlIlIIIl() if _lllIlIIIll then pcall( function ()_lllIlIIIll:Disconnect() end
 ) end
 _lllIlIIIll=RunService.Heartbeat:Connect( function () if not _IllIIIIllI or not flyActive or not _lIIllIlllI or not _lIIllIlllI.Parent then return end
 local _IlIIIIIllI=_IIIlIIIIll() if not _IlIIIIIllI or not _IlIIIIIllI.Parent then return end
 local _llIIlIllll=(_IlIIIIIllI.Position-_lIIllIlllI.Position).Unit _lIIllIlllI.CFrame=CFrame.new(_lIIllIlllI.Position,_lIIllIlllI.Position+_llIIlIllll) if _IIlllIlIlI and _IlllIIlIII then local _IIlIIIlIII=_lIlIllIIII() if _IIlIIIlIII and _IIlIIIlIII.Parent and _llllIlllIl and _llllIlllIl.Parent then _llllIlllIl.CFrame=CFrame.new(_llllIlllIl.Position,_llllIlllIl.Position+_llIIlIllll) end
 end
 end
 ) end
 local function _IIIIIlllIl() if _lllIlIIIll then _lllIlIIIll:Disconnect();_lllIlIIIll=nil end
 end
 local function _llllIIlIIl() local _llllIIlIlI=Instance.new(string.char(0x50,0x61,0x72,0x74))_llllIIlIlI.Size,_llllIIlIlI.Transparency,_llllIIlIlI.Anchored,_llllIIlIlI.CanCollide=Vector3.new(0x3,0x2,0x3),0x1,true,false _llllIIlIlI.CFrame,_llllIIlIlI.Parent=_IllIIIIIII.CFrame+Vector3.new(0x5,0x0,0x0),workspace return _llllIIlIlI end
 local function _IIlIIIIllI()_IlllIIlIII=true _llllIlllIl=_llllIIlIIl() if cavaloConn then pcall( function ()cavaloConn:Disconnect() end
 ) end
 cavaloConn=RunService.Heartbeat:Connect( function () if _llllIlllIl and _llllIlllIl.Parent then local _IIlIIIlIII=_lIlIllIIII() if _IIlIIIlIII and _IIlIIIlIII.Parent then _IIlIIIlIII.CFrame=_llllIlllIl.CFrame end
 end
 end
 ) end
 local function _IIllIlIlIl()_IlllIIlIII=false if cavaloConn then cavaloConn:Disconnect();cavaloConn=nil end
 if _llllIlllIl then _llllIlllIl:Destroy();_llllIlllIl=nil end
 end
 local function _llIIIlllII(destination) if not _llllIlllIl or not _llllIlllIl.Parent then return end
 local _IIlIlllIll=(_llllIlllIl.Position-destination).Magnitude if _IIlIlllIll<0x1 then return end
 local _lllIlIlIIl=TweenService:Create(_llllIlllIl,TweenInfo.new(_IIlIlllIll/_IIlIIIIIlI,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),{CFrame=CFrame.new(destination)})_lllIlIlIIl:Play();_lllIlIlIIl.Completed:Wait() end
 local function _llllIllIII(_lIlllIlllI) if not _lIlIlIlllI then return end
 pcall( function ()_IllIllllII:SetVisibility(_lIlllIlllI) end
 ) end
 local function _llIlIIIIll(_lIIIIIIlII) if not (_lIIllIlllI and _lIIllIlllI.Parent) then _IllIIIIIII.CFrame=CFrame.new(_lIIIIIIlII);task.wait(0.2); return end
 if _IIIIlIlIII then _lIIllIlllI.CFrame=CFrame.new(_lIIIIIIlII) if _IlllIIlIII and _llllIlllIl and _llllIlllIl.Parent then _llllIlllIl.CFrame=CFrame.new(_lIIIIIIlII+Vector3.new(0x5,0x0,0x0)) end
 task.wait(0.2) else _IlIIIlIIII(_lIIIIIIlII) if _IlllIIlIII and _llllIlllIl and _llllIlllIl.Parent then _llIIIlllII(_lIIIIIIlII) end
 end
 end
 local function _IIlIlIllll(_lllIlIIllI) local _lIIllIllll,md=nil,_lllIlIIllI or 0x1E for _,_llllIIlIlI in ipairs(workspace:GetDescendants()) do if _llllIIlIlI:IsA(string.char(0x50,0x72,0x6F,0x78,0x69,0x6D,0x69,0x74,0x79,0x50,0x72,0x6F,0x6D,0x70,0x74)) and _llllIIlIlI.Enabled then local _lIIIlIIIll,_lIIIIIIlII=_llllIIlIlI.Parent,nil if _lIIIlIIIll and _lIIIlIIIll:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then _lIIIIIIlII=_lIIIlIIIll.Position elseif _lIIIlIIIll and _lIIIlIIIll:IsA(string.char(0x41,0x74,0x74,0x61,0x63,0x68,0x6D,0x65,0x6E,0x74)) then _lIIIIIIlII=_lIIIlIIIll.WorldPosition end
 if _lIIIIIIlII then local _llIlllIlIl=(_lIIIIIIlII-_IllIIIIIII.Position).Magnitude if _llIlllIlIl<md then md,_lIIllIllll=_llIlllIlIl,_llllIIlIlI end
 end
 end
 end
 return _lIIllIllll end
 local function _IIIlllIIIl() local _lIlIlIllII=_IIlIlIllll(0x1E) local _IIIllIllll=false if _lIlIlIllII and fireproximityprompt and (_llllIllIIl==string.char(0x61,0x75,0x74,0x6F) or _llllIllIIl==string.char(0x70,0x72,0x6F,0x6D,0x70,0x74) or _llllIllIIl==string.char(0x61,0x6D,0x62,0x6F,0x73)) then pcall(fireproximityprompt,_lIlIlIllII)_IIIllIllll=true end
 local _lllIlIIlll=_llllIllIIl==string.char(0x74,0x65,0x63,0x6C,0x61) or _llllIllIIl==string.char(0x61,0x6D,0x62,0x6F,0x73) or (_llllIllIIl==string.char(0x61,0x75,0x74,0x6F) and not _IIIllIllll) if _lllIlIIlll then local _lIllIIIIll=(_lIlIlIllII and _lIlIlIllII.HoldDuration) or 0x0 _lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.E,false,game)task.wait(math.max(_lIllIIIIll,0x0)+0.15)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.E,false,game) end
 end
 local function _lIlIIIIIll(_llIlIIIllI) local _lIlllllIII=_IIIllIIlIl:FindFirstChild(string.char(0x50,0x72,0x6F,0x6D,0x70,0x74,0x73)) return (_lIlllllIII and _lIlllllIII:FindFirstChild(_llIlIIIllI,true)) or _IIIllIIlIl:FindFirstChild(_llIlIIIllI,true) end
 local function _lIIIlllllI(_IlIIllllll) local _IlIIllIlII=_IlIIllllll while _IlIIllIlII and _IlIIllIlII~=_IIIllIIlIl do if _IlIIllIlII:IsA(string.char(0x47,0x75,0x69,0x4F,0x62,0x6A,0x65,0x63,0x74)) and not _IlIIllIlII.Visible then return false end
 if _IlIIllIlII:IsA(string.char(0x53,0x63,0x72,0x65,0x65,0x6E,0x47,0x75,0x69)) and not _IlIIllIlII.Enabled then return false end
 _IlIIllIlII=_IlIIllIlII.Parent end
 return _IlIIllllll.AbsoluteSize.X>0x0 end
 local function _IlIIllllll(_llIlIIIllI,tempo) local _lllIlIIllI=os.clock()+(tempo or 0xF) while os.clock()<_lllIlIIllI do local _IlIIllllll=_lIlIIIIIll(_llIlIIIllI) if _IlIIllllll and _lIIIlllllI(_IlIIllllll) then return _IlIIllllll end
 task.wait(0.25) end
 end
 local function _IIlllIIIll(_IlIIllllll) local _IlIlIIIlIl=_IlIIllllll.Parent if _IlIlIIIlIl and _IlIlIIIlIl:IsA(string.char(0x53,0x63,0x72,0x6F,0x6C,0x6C,0x69,0x6E,0x67,0x46,0x72,0x61,0x6D,0x65)) then local _lIIIIlIlII=_IlIIllllll.AbsolutePosition.Y-_IlIlIIIlIl.AbsolutePosition.Y+_IlIlIIIlIl.CanvasPosition.Y local _llIIIlIlII=_lIIIIlIlII-(_IlIlIIIlIl.AbsoluteSize.Y-_IlIIllllll.AbsoluteSize.Y)/0x2 _IlIlIIIlIl.CanvasPosition=Vector2.new(_IlIlIIIlIl.CanvasPosition.X,math.max(0x0,_llIIIlIlII))task.wait(0.4) end
 end
 local function _IIIllIllll(_lIlllIllll,_IIllIIlIll) if not _lIIIIlIIlI then return end
 local _llIllIIIlI=Instance.new(string.char(0x53,0x63,0x72,0x65,0x65,0x6E,0x47,0x75,0x69))_llIllIIIlI.IgnoreGuiInset,_llIllIIIlI.DisplayOrder,_llIllIIIlI.ResetOnSpawn=true,0x3E8,false _llIllIIIlI.Parent=_IIIllIIlIl local _llIlllIlIl=Instance.new(string.char(0x46,0x72,0x61,0x6D,0x65))_llIlllIlIl.Size,_llIlllIlIl.Position=UDim2.fromOffset(0x10,0x10),UDim2.fromOffset(_lIlllIllll-0x8,_IIllIIlIll-0x8)_llIlllIlIl.BackgroundColor3=Color3.fromRGB(0x0,0xFF,0x0)_llIlllIlIl.Parent=_llIllIIIlI Instance.new(string.char(0x55,0x49,0x43,0x6F,0x72,0x6E,0x65,0x72),_llIlllIlIl).CornerRadius=UDim.new(0x1,0x0)task.delay(1.5, function ()_llIllIIIlI:Destroy() end
 ) end
 local function _IIIllIllll(_lIlllIllll,_IIllIIlIll)_IIIllIllll(_lIlllIllll,_IIllIIlIll) if _IlIlIIIlII==string.char(0x6D,0x6F,0x75,0x73,0x65) or _IlIlIIIlII==string.char(0x61,0x6D,0x62,0x6F,0x73) then _lllIllIIlI:SendMouseMoveEvent(_lIlllIllll,_IIllIIlIll,game)task.wait(0.1)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x0)task.wait(0.05)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x0) end
 if _IlIlIIIlII==string.char(0x74,0x6F,0x71,0x75,0x65) or _IlIlIIIlII==string.char(0x61,0x6D,0x62,0x6F,0x73) then pcall( function ()_lllIllIIlI:SendTouchEvent(0x1,0x0,_lIlllIllll,_IIllIIlIll)task.wait(0.08)_lllIllIIlI:SendTouchEvent(0x1,0x2,_lIlllIllll,_IIllIIlIll) end
 ) end
 end
 local function _lIlIIlllIl(_llIlIIIllI) local _IlIIllllll=_IlIIllllll(_llIlIIIllI,0xF) if not _IlIIllllll then return false end
 _IIlllIIIll(_IlIIllllll) local _llIlIlIllI=_IlIIllllll.AbsolutePosition+_IlIIllllll.AbsoluteSize/0x2 local _lIlllIllll=_llIlIlIllI.X+_llIIIIllIl local _IIllIIlIll=_llIlIlIllI.Y+GuiService:GetGuiInset().Y+AJUSTE_Y _llllIllIII(false);task.wait(0.15)_IIIllIllll(_lIlllIllll,_IIllIIlIll)task.wait(0.15);_llllIllIII(true) return true end
 local function _lIlIllIIIl(palavras,tempo) local _lllIlIIllI=os.clock()+(tempo or 0xA) while os.clock()<_lllIlIIllI do local _IIllIIIlIl=false pcall( function () for _,guiObj in ipairs(_IIIllIIlIl:GetDescendants()) do if _IIllIIIlIl then break end
 if guiObj:IsA(string.char(0x54,0x65,0x78,0x74,0x42,0x75,0x74,0x74,0x6F,0x6E)) or guiObj:IsA(string.char(0x49,0x6D,0x61,0x67,0x65,0x42,0x75,0x74,0x74,0x6F,0x6E)) then local _IIIlllIIll=(guiObj.Text or guiObj.Name or ""):lower() for _,palavra in ipairs(palavras) do if _IIIlllIIll:find(palavra,0x1,true) and _lIIIlllllI(guiObj) then local _IIIlIIIlll,absSize=guiObj.AbsolutePosition,guiObj.AbsoluteSize local _lIlllIllll=_IIIlIIIlll.X+absSize.X/0x2 local _IIllIIlIll=_IIIlIIIlll.Y+absSize.Y/0x2+GuiService:GetGuiInset().Y _llllIllIII(false);task.wait(0.1)_IIIllIllll(_lIlllIllll,_IIllIIlIll)task.wait(0.1);_llllIllIII(true)_IIllIIIlIl=true;break end
 end
 end
 end
 end
 ) if _IIllIIIlIl then return true end
 task.wait(0.3) end
 return false end
 local function _IlllIIllIl() if _IllIlIllIl then return false end
 _IllIlIllIl=true local _IllIlllllI,resultado=pcall( function ()_IllIIlIlIl(string.char(0x4D,0x69,0x73,0x73,0xC3,0xA3,0x6F),string.char(0xF0,0x9F,0x93,0x9C,0x20,0x49,0x6E,0x64,0x6F,0x20,0x70,0x65,0x67,0x61,0x72,0x20,0x61,0x20,0x6D,0x69,0x73,0x73,0xC3,0xA3,0x6F,0x2E,0x2E,0x2E))_llIlIIIIll(_llIIIlIlll);task.wait(0.5)_IIIlllIIIl();task.wait(0.8) if not _lIlIIlllIl(_IIlIIIIIll) then return false end
 task.wait(0.8)_llIlIIIIll(_lIIIIllIll);task.wait(0.5)_IIIlllIIIl();task.wait(1.5) return true end
 )_llllIllIII(true)_IllIlIllIl=false if not _IllIlllllI then return false end
 return resultado end
 local function _llIlllIlII() local _lIlIIIIlIl=_IlIlllIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) if _lIlIIIIlIl then _lIlIIIIlIl.Jump=true end
 pcall( function ()_lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.Space,false,game)task.wait(0.05)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.Space,false,game) end
 ) end
 local function _IlIIllIIll(_IlIIIIIllI) if not _IlIIIIIllI or not _IlIIIIIllI.Parent then return end
 local _llIlllIlIl=(_IllIIIIIII.Position-_IlIIIIIllI.Position).Magnitude if _llIlllIlIl<=_IllllllIIl and os.clock()-ultimoPulo>=_IIIIIIIIII then ultimoPulo=os.clock()_llIlllIlII() end
 end
 local function _IlllllIllI(_IlIIIIIllI) local _IllIlIIIll=_IlIIIIIllI.Position+Vector3.new(0x0,_IIIIIIllII,0x0)_IlIIIlIIII(_IllIlIIIll) if _IlllIIlIII and _llllIlllIl and _llllIlllIl.Parent then _llIIIlllII(_IllIlIIIll) end
 task.wait(0.2) local _IlIlIIIlll=_IlIIIIIllI.Position+Vector3.new(0x0,_IlIIllIIII,0x0)_IlIIIlIIII(_IlIlIIIlll) if _IlllIIlIII and _llllIlllIl and _llllIlllIl.Parent then _llIIIlllII(_IlIlIIIlll) end
 _IlIIllIIll(_IlIIIIIllI) local _IIllIllllI=tick() while _IlIIIIIllI.Parent and tick()-_IIllIllllI<0x2 do task.wait(0.03) end
 task.wait(0.3) end
 local _lllllIlllI,corridaThread=nil,nil local function _IllIlIlllI() if corridaConn then corridaConn:Disconnect();corridaConn=nil end
 alvoCorrida,_IIllIlIIlI=nil,false end
 local function _IlIlIIIlll(corrida) if not corrida or _IIllIlIIlI or _IllIlIllIl then return false end
 _IIllIlIIlI=true local _IllIlllllI=pcall( function ()_IllIIlIlIl(string.char(0x43,0x6F,0x72,0x72,0x69,0x64,0x61),corrida.nome) if not flyActive then _lIlIllIlIl() end
 _llIlIIIIll(corrida.pos);task.wait(0.5)_IIIlllIIIl();task.wait(0x1) local _llIlIIlIlI=os.clock() local _IlIIIlIIII,_IllIIllIlI=false,nil while _lllllIlllI do local _llIlIlIllI=_IIlllllIII(_llIIllIlll)alvoCorrida=_llIlIlIllI if _llIlIlIllI and _llIlIlIllI.Parent then _IlIIIlIIII,_IllIIllIlI=true,nil _IlllllIllI(_llIlIlIllI) else alvoCorrida=nil _IllIIllIlI=_IllIIllIlI or os.clock() local _lIIIlllIIl=_IlIIIlIIII and _IlIIlIlIlI or _IIIlllIIIl if os.clock()-_IllIIllIlI>=_lIIIlllIIl then break end
 task.wait(0.2) end
 if os.clock()-_llIlIIlIlI>=_llIIllIIlI then break end
 task.wait() end
 end
 )_IllIlIlllI() return _IllIlllllI end
 local function _llIlllIlII()_lllllIlllI=nil if corridaThread then pcall( function ()task.cancel(corridaThread) end
 );corridaThread=nil end
 _IllIlIlllI()_IIIIIlllIl()_IIllIlIlIl() end
 local function _lIIlIIIllI()_IIlIIIIIlI=nil if treinoThread then pcall( function ()task.cancel(treinoThread) end
 );treinoThread=nil end
 end
 local function _lIlllllIII(_lIIIIIIlII,nomePalavras) if not flyActive then _lIlIllIlIl() end
 _llIlIIIIll(_lIIIIIIlII)task.wait(_lIlIIIlIIl)_IIIlllIIIl();task.wait(0x1)_lIlIllIIIl(nomePalavras,0xA)task.wait(0x1) local _llIlIIlIlI=os.clock() local _IlIIIlIIII,_IllIIllIlI=false,nil while _IIlIIIIIlI do local _llIlIlIllI=_IIlllllIII(_llIIllIlll) if _llIlIlIllI and _llIlIlIllI.Parent then _IlIIIlIIII,_IllIIllIlI=true,nil _IlllllIllI(_llIlIlIllI) else _IllIIllIlI=_IllIIllIlI or os.clock() local _lIIIlllIIl=_IlIIIlIIII and _IIlllIIlll or _IIIlllIIIl if os.clock()-_IllIIllIlI>=_lIIIlllIIl then break end
 task.wait(0.2) end
 if os.clock()-_llIlIIlIlI>=_llIIllIIlI then break end
 task.wait() end
 end
 local function _llIIIIIlII(key)_lIllllIllI();_IIlllllIIl();_IllIIIIIIl();_IIllIllIll()task.wait(0.1)_IIlIIIIIlI=key local _IIIlIllIII=(key==string.char(0x74,0x72,0x65,0x69,0x6E,0x6F,0x31)) and {_lIIIIIIlII=_lIlllllIII,palavras={string.char(0x62,0x65,0x67,0x69,0x6E),string.char(0x63,0x72,0x6F,0x73,0x73),string.char(0x63,0x6F,0x75,0x6E,0x74,0x72,0x79)}} or {_lIIIIIIlII=_IlIIllllIl,palavras={string.char(0x62,0x65,0x67,0x69,0x6E),string.char(0x72,0x69,0x76,0x65,0x72),string.char(0x72,0x75,0x6E)}}_IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x54,0x72,0x65,0x69,0x6E,0x61,0x6D,0x65,0x6E,0x74,0x6F))_lIlIllIlIl()treinoThread=task.spawn( function () while _IIlIIIIIlI==key do pcall( function ()_lIlllllIII(_IIIlIllIII.pos,_IIIlIllIII.palavras) end
 ) if _IIlIIIIIlI~=key then break end
 task.wait(0x1) end
 end
 ) end
 local _IIIIllIlIl,mcActive,mcClick,mcEPress=nil,false,false,false local _llIIIlIlll,mcArrived,mcFlying,mcTween=nil,false,false,nil local _IIllIIlIII={string.char(0x53,0x74,0x72,0x61,0x77,0x62,0x65,0x72,0x72,0x69,0x65,0x73),string.char(0x4D,0x65,0x73,0x68,0x65,0x73,0x2F,0x48,0x61,0x79),string.char(0x4D,0x65,0x73,0x68,0x65,0x73,0x2F,0x57,0x68,0x65,0x61,0x74,0x20,0x50,0x6C,0x61,0x6E,0x65),string.char(0x43,0x6F,0x74,0x74,0x6F,0x6E,0x20,0x50,0x6C,0x61,0x6E,0x74),string.char(0x4D,0x65,0x73,0x68,0x65,0x73,0x2F,0x43,0x6F,0x63,0x6F,0x6E,0x75,0x74),string.char(0x42,0x6F,0x75,0x6E,0x64,0x73),string.char(0x52,0x61,0x73,0x70,0x62,0x65,0x72,0x72,0x69,0x65,0x73),string.char(0x4D,0x65,0x73,0x68,0x65,0x73,0x2F,0x42,0x75,0x73,0x68,0x20,0x28,0x31,0x29),} local function _IIIIIllIlI(name) return type(name)==string.char(0x73,0x74,0x72,0x69,0x6E,0x67) and (name:lower():find(string.char(0x72,0x6F,0x63,0x6B))~=nil) end
 local function _lIIIlIIlll(_IlIIllllll,kwList) local _lIlIlIlllI=(_IlIIllllll.Name..string.char(0x7C)..(_IlIIllllll.Parent and _IlIIllllll.Parent.Name or "")):lower() local _IIIlIllIII=false for _,kw in ipairs(kwList) do if _lIlIlIlllI:find(kw,0x1,true) then _IIIlIllIII=true break end
 end
 if not _IIIlIllIII then return false end
 if _IllIIIIIII and _IllIIIIIII.Parent then if (_IlIIllllll.Position-_IllIIIIIII.Position).Magnitude<=0xA then return true end
 end
 return false end
 local function _IlIIIlIIIl(_IlIIllllll) local _lIlIlIlllI=(_IlIIllllll.Name..string.char(0x7C)..(_IlIIllllll.Parent and _IlIIllllll.Parent.Name or "")):lower() if not _lIlIlIlllI:find(string.char(0x77,0x65,0x6C,0x6C),0x1,true) then return false end
 local _IIIlIllIII=_lIlIlIlllI:find(string.char(0x64,0x6F,0x6F,0x72),0x1,true) or _lIlIlIlllI:find(string.char(0x72,0x6F,0x63,0x6B),0x1,true) if not _IIIlIllIII then return false end
 if _IllIIIIIII and _IllIIIIIII.Parent then if (_IlIIllllll.Position-_IllIIIIIII.Position).Magnitude<=0xA then return true end
 end
 return false end
 local _lllllIllII,MC_BLOCKED_RADIUS=Vector3.new(600.65,30.88,-350.68),0xC local function _IlIIIlIlIl(_IlIIllllll) if not _IlIIllllll then return false end
 if not (_IllIIIIIII and _IllIIIIIII.Parent) then return false end
 local _lIlIlIlllI=(_IlIIllllll.Name..string.char(0x7C)..(_IlIIllllll.Parent and _IlIIllllll.Parent.Name or "")):lower() local _llIlllIlIl=(_IlIIllllll.Position-_IllIIIIIII.Position).Magnitude local _IIllllIIIl=false pcall( function () if typeof(_IlIIllllll.Material)==string.char(0x45,0x6E,0x75,0x6D,0x49,0x74,0x65,0x6D) and _IlIIllllll.Material==Enum.Material.Slate then _IIllllIIIl=true end
 end
 ) if (_IIllllIIIl or _lIlIlIlllI:find(string.char(0x64,0x6F,0x6F,0x72),0x1,true)) and _llIlllIlIl<=0x14 then return true end
 if (_lIlIlIlllI:find(string.char(0x72,0x69,0x76,0x65,0x72,0x20,0x72,0x6F,0x63,0x6B,0x20,0x70,0x69,0x6C,0x6C,0x61,0x72),0x1,true) or _lIlIlIlllI:find(string.char(0x62,0x75,0x69,0x6C,0x64,0x61,0x62,0x6C,0x65),0x1,true)) and _llIlllIlIl<=0x14 then return true end
 if _lIlIlIlllI:find(string.char(0x74,0x6F,0x6F,0x6C,0x73),0x1,true) and _llIlllIlIl<=0x19 then return true end
 local _lIlIIlllll=(_IlIIllllll.Name==string.char(0x4D,0x6F,0x64,0x65,0x6C) or _IlIIllllll.Name==string.char(0x4C,0x61,0x6E,0x74,0x65,0x72,0x6E)) or (_IlIIllllll.Parent and (_IlIIllllll.Parent.Name==string.char(0x4D,0x6F,0x64,0x65,0x6C) or _IlIIllllll.Parent.Name==string.char(0x4C,0x61,0x6E,0x74,0x65,0x72,0x6E))) if _lIlIIlllll and _llIlllIlIl<=0xC then return true end
 if (_IlIIllllll.Position-_lllllIllII).Magnitude<=MC_BLOCKED_RADIUS then return true end
 if _IlIIIlIIIl(_IlIIllllll) then return true end
 return false end
 local _IIIIllIlII=string.char(0x5E,0x7B,0x5B,0x25,0x78,0x25,0x2D,0x5D,0x2B,0x7D,0x24) local function _IIIlIlIlll(_IlIIllllll) local _lIIlIlllIl,depth=_IlIIllllll,0x0 while _lIIlIlllIl and depth<0xA do if (_lIIlIlllIl.Name or ""):match(_IIIIllIlII) then return _lIIlIlllIl end
 _lIIlIlllIl,depth=_lIIlIlllIl.Parent,depth+0x1 end
 return nil end
 local function _IIIIIllIII(_IlIIllllll) return _IIIlIlIlll(_IlIIllllll)~=nil end
 local function _IIIlllIlIl(o,_IIIIlllIll) if not o or not o.Parent then return false end
 if not o:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then return false end
 if not _IIIIIllIII(o) then return false end
 if _IlIIIlIlIl(o) then return false end
 if _IIIIlllIll==string.char(0x6D,0x69,0x6E,0x65) then if not _IIIIIllIlI(o.Name) then return false end
 if _IlIIIlIIIl(o) then return false end
 return true end
 if _lIIIlIIlll(o,{string.char(0x77,0x6F,0x6F,0x64),string.char(0x64,0x65,0x63,0x6F,0x72)}) then return false end
 if _IlIIIlIIIl(o) then return false end
 local _lIlIlIlllI=o.Name:lower() local _IIIIIlllII=(o.Parent and o.Parent.Name:lower()) or "" for _,_IIIIlllllI in ipairs(_IIllIIlIII) do local _lIIIlIlllI=_IIIIlllllI:lower() if _lIlIlIlllI:find(_lIIIlIlllI,0x1,true) or _IIIIIlllII:find(_lIIIlIlllI,0x1,true) then return true end
 end
 return false end
 local function _IlllIlIIIl(_IIIIlllIll) local _lIllIlllIl,bestDist=nil,math.huge local _IIIlllllIl=_IllIIIIIII.Position local function _llIIlllIlI(container) for _,o in ipairs(container:GetDescendants()) do if _IIIlllIlIl(o,_IIIIlllIll) then local _llIlllIlIl=(o.Position-_IIIlllllIl).Magnitude if _llIlllIlIl<bestDist then bestDist,_lIllIlllIl=_llIlllIlIl,o end
 end
 end
 end
 pcall( function () local _IllIlIIlII=workspace:FindFirstChild(string.char(0x49,0x73,0x6C,0x61,0x6E,0x64,0x73)) if _IllIlIIlII then for _,island in ipairs(_IllIlIIlII:GetChildren()) do if island.Name:match(_IIIIllIlII) then _llIIlllIlI(island) else for _,folder in ipairs(island:GetChildren()) do if folder.Name:match(_IIIIllIlII) then _llIIlllIlI(folder) end
 end
 end
 end
 end
 end
 ) if _lIllIlllIl==nil then pcall( function () for _,o in ipairs(workspace:GetDescendants()) do if o:IsA(string.char(0x46,0x6F,0x6C,0x64,0x65,0x72)) and o.Name:match(_IIIIllIlII) then _llIIlllIlI(o) end
 end
 end
 ) end
 return _lIllIlllIl end
 local function _IIlIIllIIl(_IlIIllllll) local _IIlIIIIlll=workspace.CurrentCamera if not _IIlIIIIlll then return nil end
 local _IIIIllIIlI=_IlIIllllll.Position+Vector3.new(0x0,_IlIIllllll.Size.Y/0x2,0x0) local _IIIlIlIllI,onScreen=_IIlIIIIlll:WorldToViewportPoint(_IIIIllIIlI) if onScreen then return math.floor(_IIIlIlIllI.X+0.5),math.floor(_IIIlIlIllI.Y+0.5) end
 local _lllllIIlll=_IIlIIIIlll.ViewportSize return math.floor(_lllllIIlll.X/0x2),math.floor(_lllllIIlll.Y/0x2) end
 local function _lIlllIIlII() if not (_llIIIlIlll and _llIIIlIlll.Parent) then return end
 local _lIlllIllll,_IIllIIlIll=_IIlIIllIIl(_llIIIlIlll) if not _lIlllIllll then return end
 pcall( function ()_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x1)task.wait(0.05)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x1) end
 ) end
 local function _IIllIIIllI()pcall( function ()_lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.E,false,game)task.wait(0.04)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.E,false,game) end
 ) end
 local function _llIlIlIllI() if not (_IllIIIIIII and _IllIIIIIII.Parent) then return end
 local _llIlIlIllI=_IllIIIIIII.Parent local _lIlIIIIlIl=_llIlIlIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64))pcall( function ()_IllIIIIIII.Anchored=true _IllIIIIIII.AssemblyLinearVelocity,_IllIIIIIII.AssemblyAngularVelocity=Vector3.new(),Vector3.new() if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand,_lIlIIIIlIl.WalkSpeed,_lIlIIIIlIl.JumpPower,_lIlIIIIlIl.AutoRotate=true,0x0,0x0,false end
 for _,_llllIIlIlI in ipairs(_llIlIlIllI:GetDescendants()) do if _llllIIlIlI:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then _llllIIlIlI.CanCollide=false end
 end
 end
 ) end
 local function _IlllIIllII() if not (_IllIIIIIII and _IllIIIIIII.Parent) then return end
 local _llIlIlIllI=_IllIIIIIII.Parent local _lIlIIIIlIl=_llIlIlIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64))pcall( function ()_IllIIIIIII.Anchored=false _IllIIIIIII.AssemblyLinearVelocity,_IllIIIIIII.AssemblyAngularVelocity=Vector3.new(),Vector3.new() if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand,_lIlIIIIlIl.WalkSpeed,_lIlIIIIlIl.JumpPower,_lIlIIIIlIl.AutoRotate=false,0x10,0x32,true end
 for _,_llllIIlIlI in ipairs(_llIlIlIllI:GetDescendants()) do if _llllIIlIlI:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then _llllIIlIlI.CanCollide=true end
 end
 end
 ) end
 local function _llIlIlllll(tp) if not (_IllIIIIIII and _IllIIIIIII.Parent) then return end
 local _IIlIIIIlll=workspace.CurrentCamera if not _IIlIIIIlll then return end
 local _IlllIlIlll=CFrame.lookAt(_IllIIIIIII.Position,tp) local _IlIIlIllll=_IllIIIIIII.Position+_IlllIlIlll.LookVector*-3.5+Vector3.new(0x0,1.7,0x0)_IIlIIIIlll.CameraType=Enum.CameraType.Fixed _IIlIIIIlll.CFrame=CFrame.lookAt(_IlIIlIllll,tp+Vector3.new(0x0,-0.3,0x0)) end
 local function _llIIIIlIIl(_IlIIIlllII) if mcFlying then return end
 mcFlying,mcArrived=true,false if not (_IllIIIIIII and _IllIIIIIII.Parent) then mcFlying=false return end
 _llIlIlIllI() local _IlIIIIIlII=(_IIIIllIlIl==string.char(0x6D,0x69,0x6E,0x65)) and 1.5 or 0x1 local _lIllIIlIlI=_IlIIIlllII.Position+Vector3.new(0x0,_IlIIIIIlII,0x0) local _llIIIIIIlI=CFrame.lookAt(_lIllIIlIlI,_IlIIIlllII.Position)pcall( function ()_IllIIIIIII.CFrame=_IllIIIIIII.CFrame+Vector3.new(0x0,0x2,0x0) end
 ) local _IIlIlllIll=(_lIllIIlIlI-_IllIIIIIII.Position).Magnitude local _llllIIlIII=math.max(_IIlIlllIll/0x46,0.3) local function _IIIlIlIlII()pcall( function ()_IllIIIIIII.CFrame=_llIIIIIIlI _IllIIIIIII.AssemblyLinearVelocity,_IllIIIIIII.AssemblyAngularVelocity=Vector3.new(),Vector3.new()_llIlIlllll(_IlIIIlllII.Position) end
 )mcFlying,mcArrived=false,true end
 local _IllIlllllI,tw=pcall( function () return TweenService:Create(_IllIIIIIII,TweenInfo.new(_llllIIlIII,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),{CFrame=_llIIIIIIlI}) end
 ) if not _IllIlllllI or not tw then pcall( function ()_IllIIIIIII.CFrame=_llIIIIIIlI end
 )_IIIlIlIlII(); return end
 mcTween=tw tw:Play()tw.Completed:Connect(_IIIlIlIlII) end
 local function _lllIIlllIl() if _IIIIllIlIl==string.char(0x6D,0x69,0x6E,0x65) then mcClick= not mcClick _IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),mcClick and string.char(0x43,0x6C,0x69,0x71,0x75,0x65,0x3A,0x20,0x41,0x74,0x69,0x76,0x61,0x64,0x6F) or string.char(0x43,0x6C,0x69,0x71,0x75,0x65,0x3A,0x20,0x50,0x61,0x75,0x73,0x61,0x64,0x6F)) elseif _IIIIllIlIl==string.char(0x63,0x6F,0x6C,0x6C,0x65,0x63,0x74) then mcEPress= not mcEPress _IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),mcEPress and string.char(0x54,0x65,0x63,0x6C,0x61,0x20,0x45,0x3A,0x20,0x41,0x74,0x69,0x76,0x61,0x64,0x6F) or string.char(0x54,0x65,0x63,0x6C,0x61,0x20,0x45,0x3A,0x20,0x50,0x61,0x75,0x73,0x61,0x64,0x6F)) else _IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),string.char(0x45,0x73,0x63,0x6F,0x6C,0x68,0x61,0x20,0x75,0x6D,0x20,0x6D,0x6F,0x64,0x6F,0x20,0x70,0x72,0x69,0x6D,0x65,0x69,0x72,0x6F)) end
 end
 _IIIllIlllI= function ()mcActive,_llIIIlIlll,mcArrived,_IIIIllIlIl=false,nil,false,nil mcClick,mcEPress=false,false if mcTween then pcall( function ()mcTween:Cancel() end
 ) end
 mcTween=nil _IlllIIllII()pcall( function () local _IIlIIIIlll=workspace.CurrentCamera if _IIlIIIIlll then _IIlIIIIlll.CameraType=Enum.CameraType.Custom end
 end
 ) end
 local function _IIlllIlIll(_IIIIlllIll)_IIIlIlIlIl() if mcActive and _IIIIllIlIl==_IIIIlllIll then _IIIllIlllI()_IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),string.char(0x44,0x65,0x73,0x61,0x74,0x69,0x76,0x61,0x64,0x6F,0x3A,0x20)..(_IIIIlllIll==string.char(0x6D,0x69,0x6E,0x65) and string.char(0x4D,0x49,0x4E,0x45) or string.char(0x43,0x4F,0x4C,0x4C,0x45,0x43,0x54))) return end
 _IIIllIlllI()_IIIIllIlIl=_IIIIlllIll if _IIIIlllIll==string.char(0x6D,0x69,0x6E,0x65) then mcClick,mcEPress=true,false else mcEPress,mcClick=true,false end
 local _IlIIIlllII=_IlllIlIIIl(_IIIIlllIll) if not _IlIIIlllII then _IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),string.char(0x4E,0x61,0x64,0x61,0x20,0x65,0x6E,0x63,0x6F,0x6E,0x74,0x72,0x61,0x64,0x6F,0x20,0x70,0x6F,0x72,0x20,0x70,0x65,0x72,0x74,0x6F)) return end
 if not (_IllIIIIIII and _IllIIIIIII.Parent) then return end
 mcActive,_llIIIlIlll=true,_IlIIIlllII _IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),(_IIIIlllIll==string.char(0x6D,0x69,0x6E,0x65) and string.char(0x4D,0x49,0x4E,0x45) or string.char(0x43,0x4F,0x4C,0x4C,0x45,0x43,0x54))..string.char(0x20,0x69,0x6E,0x69,0x63,0x69,0x61,0x64,0x6F))_llIIIIlIIl(_IlIIIlllII) end
 task.spawn( function () while true do task.wait(0.16)pcall( function () if mcActive and mcArrived and mcClick and _IIIIllIlIl==string.char(0x6D,0x69,0x6E,0x65) and _llIIIlIlll and _llIIIlIlll.Parent then _lIlllIIlII() end
 end
 ) end
 end
 )task.spawn( function () while true do task.wait(0.25)pcall( function () if mcActive and mcArrived and mcEPress and _IIIIllIlIl==string.char(0x63,0x6F,0x6C,0x6C,0x65,0x63,0x74) and _llIIIlIlll and _llIIIlIlll.Parent then _IIllIIIllI() end
 end
 ) end
 end
 )task.spawn( function () while true do task.wait(0.1)pcall( function () if not (mcActive and mcArrived and _llIIIlIlll and _llIIIlIlll.Parent) then return end
 if not (_IllIIIIIII and _IllIIIIIII.Parent) then return end
 local _IlIIIIIlII=(_IIIIllIlIl==string.char(0x6D,0x69,0x6E,0x65)) and 1.5 or 0x1 local _lIllIIlIlI=_llIIIlIlll.Position+Vector3.new(0x0,_IlIIIIIlII,0x0) if (_IllIIIIIII.Position-_lIllIIlIlI).Magnitude>0.75 then _llIlIlIllI()pcall( function ()_IllIIIIIII.CFrame=CFrame.lookAt(_lIllIIlIlI,_llIIIlIlll.Position)_IllIIIIIII.AssemblyLinearVelocity,_IllIIIIIII.AssemblyAngularVelocity=Vector3.new(),Vector3.new() end
 ) end
 _llIlIlllll(_llIIIlIlll.Position) end
 ) end
 end
 )RunService.RenderStepped:Connect( function ()pcall( function () if mcActive and mcArrived and _llIIIlIlll and _llIIIlIlll.Parent then _llIlIlllll(_llIIIlIlll.Position) end
 end
 ) end
 )task.spawn( function () while true do task.wait(0.4)pcall( function () if mcActive and mcArrived and _llIIIlIlll then if not _llIIIlIlll.Parent then _llIIIlIlll=nil local _lIIIIIlIll=_IlllIlIIIl(_IIIIllIlIl) if _lIIIIIlIll then _llIIIlIlll=_lIIIIIlIll _llIIIIlIIl(_lIIIIIlIll) else _IIIllIlllI()_IllIIlIlIl(string.char(0x4D,0x69,0x6E,0x65,0x2F,0x43,0x6F,0x6C,0x6C,0x65,0x63,0x74),string.char(0x54,0x75,0x64,0x6F,0x20,0x63,0x6F,0x6C,0x65,0x74,0x61,0x64,0x6F,0x21)) end
 end
 end
 end
 ) end
 end
 ) local UserInputService=game:GetService(string.char(0x55,0x73,0x65,0x72,0x49,0x6E,0x70,0x75,0x74,0x53,0x65,0x72,0x76,0x69,0x63,0x65))UserInputService.InputBegan:Connect( function (input,gp) if gp then return end
 pcall( function () if input.KeyCode==Enum.KeyCode.C then _lllIIlllIl() end
 end
 ) end
 ) local _IllIllIllI={} local _IlIIllllIl={string.char(0x77,0x69,0x6C,0x64),string.char(0x73,0x65,0x6C,0x76,0x61,0x67,0x65,0x6D),string.char(0x73,0x61,0x6C,0x76,0x61,0x6A,0x65)} local function _lIlllIllIl(o) if o:IsA(string.char(0x42,0x69,0x6C,0x6C,0x62,0x6F,0x61,0x72,0x64,0x47,0x75,0x69)) then _IllIllIllI[o]=true end
 end
 workspace.DescendantAdded:Connect(_lIlllIllIl)workspace.DescendantRemoving:Connect( function (o)_IllIllIllI[o]=nil end
 )task.spawn( function () for _,o in ipairs(workspace:GetDescendants()) do _lIlllIllIl(o) end
 end
 ) local function _llIIIIIIIl(gui) local _lIlIllllll={} for _,o in ipairs(gui:GetDescendants()) do if o:IsA(string.char(0x54,0x65,0x78,0x74,0x4C,0x61,0x62,0x65,0x6C)) or o:IsA(string.char(0x54,0x65,0x78,0x74,0x42,0x75,0x74,0x74,0x6F,0x6E)) or o:IsA(string.char(0x54,0x65,0x78,0x74,0x42,0x6F,0x78)) then local _lIlIIIlIIl=o.ContentText if _lIlIIIlIIl==nil or _lIlIIIlIIl=="" then _lIlIIIlIIl=o.Text end
 if _lIlIIIlIIl~="" then _lIlIllllll[#_lIlIllllll+0x1]=_lIlIIIlIIl end
 end
 end
 return table.concat(_lIlIllllll,string.char(0x20)) end
 local function _IIllIIIIII(gui) if gui.Name==string.char(0x43,0x61,0x70,0x74,0x75,0x72,0x65,0x50,0x72,0x6F,0x67,0x72,0x65,0x73,0x73) then return true end
 local _lIlIlIlllI=_llIIIIIIIl(gui):lower() if _lIlIlIlllI=="" then return false end
 for _,f in ipairs(_IlIIllllIl) do if _lIlIlIlllI:find(f,0x1,true) then return true end
 end
 return false end
 local function _IIlIIIlIll(gui) local _lIIlIlllIl,depth=gui.Adornee or gui.Parent,0x0 while _lIIlIlllIl and _lIIlIlllIl~=workspace and depth<0xC do if _lIIlIlllIl:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) and _lIIlIlllIl:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) then return _lIIlIlllIl end
 _lIIlIlllIl,depth=_lIIlIlllIl.Parent,depth+0x1 end
 return nil end
 local _lIllIllIIl,HORSE_RESEARCH_TIME=0x5,1.5 local _IIIllIIlIl,targetHorse,isFloating=false,nil,false local _IlIIlIllll,horseGyro,horseConn,horseTrackConn=nil,nil,nil,nil local _IIllIIllII=0x46 local _IIllIIllll,ultimaValidacao=0x0,0x0 local function _lIIllIlllI(_lIIlIlllII) if _lIIlIlllII.PrimaryPart then return _lIIlIlllII.PrimaryPart end
 local _llIIlIlIII,bigSize=nil,0x0 for _,_lIlllIlllI in ipairs(_lIIlIlllII:GetDescendants()) do if _lIlllIlllI:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then local _lIIIIlIlII=_lIlllIlllI.Size.Magnitude if _lIIIIlIlII>bigSize then bigSize,_llIIlIlIII=_lIIIIlIlII,_lIlllIlllI end
 end
 end
 return _llIIlIlIII end
 local function _IIIlIIllIl(_lIIlIlllII) local _lllllIIlIl=-math.huge for _,_lIlllIlllI in ipairs(_lIIlIlllII:GetDescendants()) do if _lIlllIlllI:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then local _IIIIllIIlI=_lIlllIlllI.Position.Y+_lIlllIlllI.Size.Y/0x2 if _IIIIllIIlI>_lllllIIlIl then _lllllIIlIl=_IIIIllIIlI end
 end
 end
 return _lllllIIlIl==-math.huge and _IllIIIIIII.Position.Y or _lllllIIlIl end
 local function _IIIIIIlIIl(_lIIlIlllII) if not _lIIlIlllII or not _lIIlIlllII.Parent then return false end
 if _lIIlIlllII==_IlIlllIllI then return false end
 for gui in pairs(_IllIllIllI) do if gui.Parent and _IIllIIIIII(gui) and _IIlIIIlIll(gui)==_lIIlIlllII then return true end
 end
 return false end
 local function _IIllIlIIII() local _lIlIIIlIlI,vistos={},{} local _IIIlllllIl=_IllIIIIIII.Position for gui in pairs(_IllIllIllI) do if gui.Parent and _IIllIIIIII(gui) then local _lIIlIlllII=_IIlIIIlIll(gui) if _lIIlIlllII and not vistos[_lIIlIlllII] and _lIIlIlllII~=_IlIlllIllI and not Players:GetPlayerFromCharacter(_lIIlIlllII) then vistos[_lIIlIlllII]=true local _lIIIlllIlI=_lIIllIlllI(_lIIlIlllII) if _lIIIlllIlI then local _IIlIlllIll=(_lIIIlllIlI.Position-_IIIlllllIl).Magnitude if _IIlIlllIll<=0xA86 then table.insert(_lIlIIIlIlI,{_lIIlIlllII=_lIIlIlllII,_IIlIlllIll=_IIlIlllIll,_IIIlllIIll=_llIIIIIIIl(gui)}) end
 end
 end
 end
 end
 table.sort(_lIlIIIlIlI, function (a,_lIlIIlIIII) return a.dist<_lIlIIlIIII.dist end
 ) return _lIlIIIlIlI end
 local function _IllIIlIIIl() if horseTrackConn then horseTrackConn:Disconnect();horseTrackConn=nil end
 end
 local function _IlIlllIlll(_lIIlIlllII)_IllIIlIIIl()horseTrackConn=RunService.Heartbeat:Connect( function () if not isFloating or not _IlIIlIllll then return end
 if not _lIIlIlllII or not _lIIlIlllII.Parent then _IllIIlIIIl(); return end
 local _lIIIlllIlI=_lIIllIlllI(_lIIlIlllII) if not _lIIIlllIlI then return end
 local _IlIIIlllII=Vector3.new(_lIIIlllIlI.Position.X,_IIIlIIllIl(_lIIlIlllII)+_lIllIllIIl,_lIIIlllIlI.Position.Z)_IlIIlIllll.Position=_IlIIlIllll.Position:Lerp(_IlIIIlllII,0.15) end
 ) end
 local function _llIIIIlIll() if isFloating then return end
 isFloating=true local _lIlIIIIlIl=_IlIlllIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand=true end
 _IlIIlIllll=Instance.new(string.char(0x42,0x6F,0x64,0x79,0x50,0x6F,0x73,0x69,0x74,0x69,0x6F,0x6E))_IlIIlIllll.MaxForce=Vector3.new(math.huge,math.huge,math.huge)_IlIIlIllll.P,_IlIIlIllll.D,_IlIIlIllll.Position=0x1D4C,0x1F4,_IllIIIIIII.Position _IlIIlIllll.Parent=_IllIIIIIII horseGyro=Instance.new(string.char(0x42,0x6F,0x64,0x79,0x47,0x79,0x72,0x6F))horseGyro.MaxTorque=Vector3.new(math.huge,math.huge,math.huge)horseGyro.P,horseGyro.D,horseGyro.CFrame=0x2710,0x1F4,_IllIIIIIII.CFrame horseGyro.Parent=_IllIIIIIII end
 local function _IlIlIllIIl() if not isFloating then return end
 isFloating=false _IllIIlIIIl() local _lIlIIIIlIl=_IlIlllIllI:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) if _lIlIIIIlIl then _lIlIIIIlIl.PlatformStand=false end
 if _IlIIlIllll then _IlIIlIllll:Destroy();_IlIIlIllll=nil end
 if horseGyro then horseGyro:Destroy();horseGyro=nil end
 targetHorse=nil end
 local function _lllIllIIlI(_lIIlIlllII,speed) local _lIIIlllIlI=_lIIllIlllI(_lIIlIlllII) if not _lIIIlllIlI then return false end
 local _llIllIIllI=Vector3.new(_lIIIlllIlI.Position.X,_IIIlIIllIl(_lIIlIlllII)+_lIllIllIIl,_lIIIlllIlI.Position.Z) local _IIlIlllIll=(_IllIIIIIII.Position-_llIllIIllI).Magnitude if _IIlIlllIll<0x2 then return true end
 if _IlIIlIllll then _IlIIlIllll.Parent=nil end
 local _lllIlIlIIl=TweenService:Create(_IllIIIIIII,TweenInfo.new(math.max(_IIlIlllIll/speed,0.1),Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),{CFrame=CFrame.new(_llIllIIllI)})_lllIlIlIIl:Play();_lllIlIlIIl.Completed:Wait() if _IlIIlIllll then _IlIIlIllll.Parent=_IllIIIIIII end
 return true end
 local function _IIIlIIllIl(_lIIlIlllII) local _lIIIlllIlI=_lIIllIlllI(_lIIlIlllII) if not _lIIIlllIlI then return end
 _lllIllIIlI(_lIIlIlllII,_IIllIIllII) if _IlIIlIllll then _IlIIlIllll.Position=Vector3.new(_lIIIlllIlI.Position.X,_IIIlIIllIl(_lIIlIlllII)+_lIllIllIIl,_lIIIlllIlI.Position.Z) end
 _IlIlllIlll(_lIIlIlllII) end
 local function _IlIllllIII()task.wait(0.2)_lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.Two,false,game)task.wait(0.1)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.Two,false,game)task.wait(0.3) end
 local function _IlIlllllII() local _lIlIIIlIlI=_IIllIlIIII() if #_lIlIIIlIlI>0x0 then targetHorse=_lIlIIIlIlI[0x1].model ultimaValidacao=tick()_llIIIIlIll()_IIIlIIllIl(targetHorse) local _llIlIIIllI=_lIlIIIlIlI[0x1].texto~="" and _lIlIIIlIlI[0x1].texto or targetHorse.Name _IIIlIllllI(cavLabel,string.char(0x48,0x6F,0x72,0x73,0x65,0x3A,0x20)..nome) return true end
 return false end
 local function _llIlIlIllI() if horseConn then return end
 _IIIllIIlIl,_IIllIIllll=true,0x0 _IIIlIllllI(cavLabel,string.char(0x48,0x6F,0x72,0x73,0x65,0x3A,0x20,0x50,0x72,0x6F,0x63,0x75,0x72,0x61,0x6E,0x64,0x6F,0x2E,0x2E,0x2E))task.spawn( function ()_IlIlllllII() end
 )horseConn=RunService.Heartbeat:Connect( function () if not _IIIllIIlIl then return end
 local _lIllIlllll=tick() if targetHorse then if _lIllIlllll-ultimaValidacao>=0.5 then ultimaValidacao=_lIllIlllll if not _IIIIIIlIIl(targetHorse) then targetHorse=nil end
 end
 if targetHorse then return end
 end
 _IllIIlIIIl()targetHorse=nil if _lIllIlllll-_IIllIIllll>=HORSE_RESEARCH_TIME then _IIllIIllll=_lIllIlllll if not _IlIlllllII() then _IlIlIllIIl()_IIIlIllllI(cavLabel,string.char(0x48,0x6F,0x72,0x73,0x65,0x3A,0x20,0x50,0x72,0x6F,0x63,0x75,0x72,0x61,0x6E,0x64,0x6F,0x2E,0x2E,0x2E)) end
 end
 end
 ) end
 local function _lIIIIllllI()_IIIllIIlIl=false if horseConn then horseConn:Disconnect();horseConn=nil end
 _IlIlIllIIl()_IIIlIllllI(cavLabel,string.char(0x48,0x6F,0x72,0x73,0x65,0x3A,0x20,0x4F,0x66,0x66)) end
 local _IlIIIlIlIl=false local _lIIlIllIlI=nil task.spawn( function () while true do task.wait(0x1) if _IlIIIlIlIl then pcall( function () local _IIlIIIIlll=workspace.CurrentCamera if not _IIlIIIIlll then return end
 local _lllllIIlll=_IIlIIIIlll.ViewportSize local _lIlllIllll,_IIllIIlIll=math.floor(_lllllIIlll.X/0x2),math.floor(_lllllIIlll.Y/0x2)_lllIllIIlI:SendMouseMoveEvent(_lIlllIllll,_IIllIIlIll,game)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x0)task.wait(0.05)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x0) end
 ) end
 end
 end
 ) local _IllIlIllII=0x96 local _IIIIllIllI=Vector3.new(-1672.22,25.00,730.57) local _IIllIIlIII=0xC local _lllIlIIIll=0x4 local _IlllllIIIl=true local _llIIlllIll=false local _lIllIlIllI=0x0 local _IlIlIlIlIl,cacheMesh={},{} local _IIIlIllIII=0x1AC local _lIlIllIlIl=0x17 local function _lIlIIIlIll()_lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.E,false,game)task.wait(0.15)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.E,false,game) end
 local function _lllIIIllIl(_IIIIlllIll) for _,_llIlllIlIl in ipairs(_IIIIlllIll:GetDescendants()) do if _llIlllIlIl:IsA(string.char(0x50,0x72,0x6F,0x78,0x69,0x6D,0x69,0x74,0x79,0x50,0x72,0x6F,0x6D,0x70,0x74)) and fireproximityprompt then pcall(fireproximityprompt,_llIlllIlIl) elseif _llIlllIlIl:IsA(string.char(0x43,0x6C,0x69,0x63,0x6B,0x44,0x65,0x74,0x65,0x63,0x74,0x6F,0x72)) and fireclickdetector then pcall(fireclickdetector,_llIlllIlIl) end
 end
 end
 local function _IllIlllIll() local _lllIIllIlI,sy=_IIIlIllIII,_lIlIllIlIl+GuiService:GetGuiInset().Y _lllIllIIlI:SendMouseMoveEvent(_lllIIllIlI,sy,game)task.wait(0.02)_lllIllIIlI:SendMouseButtonEvent(_lllIIllIlI,sy,0x0,true,game,0x0)task.wait(0.02)_lllIllIIlI:SendMouseButtonEvent(_lllIIllIlI,sy,0x0,false,game,0x0) end
 local function _IIIIlIIIII(_IIIIlllIll) if cacheMesh[_IIIIlllIll] then return true end
 if not _IIIIlllIll:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) then return false end
 if not _IIIIlllIll.Name:match(string.char(0x5E,0x7B,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B)) then return false end
 local _IlllIIlIll=_IIIIlllIll:FindFirstChild(string.char(0x41,0x74,0x74,0x61,0x63,0x68,0x65,0x64,0x54,0x6F,0x42,0x6F,0x64,0x79)) if not _IlllIIlIll then return false end
 for _,_llIlllIlIl in ipairs(_IlllIIlIll:GetDescendants()) do local _IIIIlllllI=_llIlllIlIl.Name:lower() if _IIIIlllllI:find(string.char(0x70,0x75,0x6D,0x70)) or _IIIIlllllI:find(string.char(0x6A,0x61,0x63,0x6B)) then cacheMesh[_IIIIlllIll]=true return true end
 end
 return false end
 local function _IlIlIIllII(_IIIIlllIll) if not (_IIIIlllIll and _IIIIlllIll.Parent) then return false end
 local _lIlIIIIlIl=_IIIIlllIll:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) return _lIlIIIIlIl and _lIlIIIIlIl.Health>0x0 and _IIIIlllIll:FindFirstChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74))~=nil end
 local function _IIlIlIIllI(_IIIIlllIll) return _IIIIlllIll and _IIIIlllIll.Parent and not _IIIIlllIll:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) and _IIIIlllIll:FindFirstChild(string.char(0x53,0x68,0x6F,0x77,0x57,0x68,0x65,0x6E,0x44,0x72,0x61,0x67,0x67,0x65,0x64)) and _IIIIlllIll:FindFirstChild(string.char(0x42,0x6F,0x64,0x79)) end
 local function _llIlllIIll(_IIIIlllIll) local _lIlIIlIIII=_IIIIlllIll:FindFirstChild(string.char(0x42,0x6F,0x64,0x79)) if _lIlIIlIIII and _lIlIIlIIII:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then return _lIlIIlIIII.Position end
 if _IIIIlllIll.PrimaryPart then return _IIIIlllIll.PrimaryPart.Position end
 for _,_llIlllIlIl in ipairs(_IIIIlllIll:GetDescendants()) do if _llIlllIlIl:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then return _llIlllIlIl.Position end
 end
 end
 local function _lllIllIIIl(tipo) local _lllllIlIIl=_IllIIIIIII if not _lllllIlIIl then return end
 local _lIIllIllll,_IIlIlllIll=nil,math.huge for _,_IIIIlllIll in ipairs(workspace:GetDescendants()) do if _IIIIlllIll:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) and ( not _IlIlIlIlIl[_IIIIlllIll] or _IlIlIlIlIl[_IIIIlllIll]<tick()) and _IIIIlIIIII(_IIIIlllIll) then local _lIIIIIIlII if tipo==string.char(0x76,0x69,0x76,0x61) and _IlIlIIllII(_IIIIlllIll) then _lIIIIIIlII=_IIIIlllIll.HumanoidRootPart.Position elseif tipo==string.char(0x6D,0x6F,0x72,0x74,0x61) and _IIlIlIIllI(_IIIIlllIll) then _lIIIIIIlII=_llIlllIIll(_IIIIlllIll) end
 if _lIIIIIIlII then local _llIlllIlIl=(_lIIIIIIlII-_lllllIlIIl.Position).Magnitude if _llIlllIlIl<_IIlIlllIll then _lIIllIllll,_IIlIlllIll=_IIIIlllIll,_llIlllIlIl end
 end
 end
 end
 return _lIIllIllll end
 local function _llIlIlIlll(posFn,tol,timeout) local _IIllIllllI=tick() while _llIIlllIll and tick()-_IIllIllllI<timeout do local _IlllllIIlI=RunService.Heartbeat:Wait() local _lllllIlIIl=_IllIIIIIII local _llllIIlIlI=posFn() if not (_lllllIlIIl and _llllIIlIlI) then return false end
 local _llIlllIlIl=_llllIIlIlI-_lllllIlIIl.Position _lllllIlIIl.AssemblyLinearVelocity,_lllllIlIIl.AssemblyAngularVelocity=Vector3.zero,Vector3.zero if _llIlllIlIl.Magnitude<=tol then _lllllIlIIl.CFrame=CFrame.new(_llllIIlIlI)*_lllllIlIIl.CFrame.Rotation return true end
 local _lllIIlIlll=math.min(_llIlllIlIl.Magnitude,_IllIlIllII*_IlllllIIlI)_lllllIlIIl.CFrame=CFrame.new(_lllllIlIIl.Position+_llIlllIlIl.Unit*_lllIIlIlll)*_lllllIlIIl.CFrame.Rotation end
 return false end
 local function _llllIIIlll(_IIIIlllIll) local _IllIlllllI=_llIlIlIlll( function () local _llllIIlIlI=_llIlllIIll(_IIIIlllIll) return _llllIIlIlI and (_llllIIlIlI+Vector3.new(0x0,_lllIlIIIll,0x0)) end
 ,0x2,0xA) if not _IllIlllllI then _IlIlIlIlIl[_IIIIlllIll]=tick()+0xA return end
 task.wait(0.2)_lIlIIIlIll()_lllIIIllIl(_IIIIlllIll)task.wait(0.5)_llIlIlIlll( function () return _IIIIllIllI end
 ,0x3,0x28)task.wait(0.5) if _IlllllIIIl then _lIlIIIlIll()task.wait(0.5) end
 _IlIlIlIlIl[_IIIIlllIll]=tick()+0xA end
 local function _IlllIlIIlI(_IIIIlllIll) local _IIllIllllI,_lIlIIIIIII=tick(),0x0 while _llIIlllIll and _IlIlIIllII(_IIIIlllIll) and tick()-_IIllIllllI<0x28 do local _lllllIlIIl=_IllIIIIIII if not _lllllIlIIl then break end
 local _lIIIIIIlII=_IIIIlllIll.HumanoidRootPart.Position _lllllIlIIl.CFrame=CFrame.lookAt(_lIIIIIIlII+Vector3.new(0x0,_IIllIIlIII,0x0),_lIIIIIIlII)_lllllIlIIl.AssemblyLinearVelocity,_lllllIlIIl.AssemblyAngularVelocity=Vector3.zero,Vector3.zero if tick()-_lIlIIIIIII>0.5 then _lIlIIIIIII=tick()_lllIIIllIl(_IIIIlllIll)_IllIlllIll() end
 RunService.Heartbeat:Wait() end
 task.wait(1.5) end
 _IIlllllIIl= function ()_llIIlllIll=false _lIllIlIllI+=0x1 _IlIlIlIlIl,cacheMesh={},{} end
 local function _llIllIlIll()_IIlllllIIl()_llIIlllIll=true local _llllIIlIlI=_lIllIlIllI task.spawn( function () while _llIIlllIll and _lIllIlIllI==_llllIIlIlI do local _IIIIlllIll=_lllIllIIIl(string.char(0x6D,0x6F,0x72,0x74,0x61)) if _IIIIlllIll then _llllIIIlll(_IIIIlllIll) else local _lIlllIlllI=_lllIllIIIl(string.char(0x76,0x69,0x76,0x61)) if _lIlllIlllI then _IlllIlIIlI(_lIlllIlllI) else task.wait(0x1) end
 end
 task.wait() end
 end
 )_IllIIlIlIl(string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E),string.char(0xF0,0x9F,0x8E,0x83,0x20,0x41,0x75,0x74,0x6F,0x20,0x41,0x62,0xC3,0xB3,0x62,0x6F,0x72,0x61,0x20,0x4F,0x4E,0x20,0x28,0x63,0x6C,0x69,0x71,0x75,0x65,0x20,0x34,0x32,0x38,0x2F,0x32,0x33,0x29)) end
 local _IlllIIIlII,BICHO_ESPERA=0x4,0x1 local _lIIlIIIllI,BICHO_TEMPO_MAX,BICHO_IGNORAR=0xF,0x8,0x3C local _lIlIlllIIl=false local _llIlIllIIl=0x0 local _lllIlIIIII={} local function _IIllIllIIl(name) return name:match(string.char(0x5E,0x7B,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x7D,0x24))~=nil end
 local function _lIIlllIIll(_IlIIllllll) return _IlIIllllll:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) and _IIllIllIIl(_IlIIllllll.Name) and _IlIIllllll:FindFirstChild(string.char(0x49,0x6E,0x74,0x65,0x72,0x61,0x63,0x74,0x69,0x6F,0x6E,0x50,0x61,0x72,0x74)) and _IlIIllllll:FindFirstChild(string.char(0x42,0x6F,0x64,0x79)) and _IlIIllllll:FindFirstChild(string.char(0x46,0x6F,0x72,0x63,0x65,0x46,0x69,0x65,0x6C,0x64)) and _IlIIllllll:FindFirstChildOfClass(string.char(0x41,0x6E,0x69,0x6D,0x61,0x74,0x69,0x6F,0x6E,0x43,0x6F,0x6E,0x74,0x72,0x6F,0x6C,0x6C,0x65,0x72)) and not _IlIIllllll:FindFirstChildOfClass(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64)) end
 local function _lIIlllIIlI(_lIIIlllIlI) local _lIIllIllll,menor=nil,math.huge for _,_IlIIllllll in ipairs(workspace:GetDescendants()) do if _lIIlllIIll(_IlIIllllll) then local _IllllIIIIl=_lllIlIIIII[_IlIIllllll] if not _IllllIIIIl or os.clock()>_IllllIIIIl then local _llIlllIlIl=(_IlIIllllll.InteractionPart.Position-_lIIIlllIlI.Position).Magnitude if _llIlllIlIl<menor then _lIIllIllll,menor=_IlIIllllll,_llIlllIlIl end
 end
 end
 end
 return _lIIllIllll end
 _IllIIIIIIl= function ()_lIlIlllIIl=false _llIlIllIIl+=0x1 _lllIlIIIII={} end
 local function _lllllIlIll()_IllIIIIIIl()_lIlIlllIIl=true local _llllIIlIlI=_llIlIllIIl task.spawn( function () while _lIlIlllIIl and _llIlIllIIl==_llllIIlIlI do local _llIlIlIllI=_IIllllllII.Character local _lIIIlllIlI=_llIlIlIllI and _llIlIlIllI:FindFirstChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74)) if not _lIIIlllIlI then task.wait(0.5)continue end
 local _IIlllIIIIl=_lIIlllIIlI(_lIIIlllIlI) if not _IIlllIIIIl then task.wait(0x1)continue end
 local _lIIlIllIll=false local _IllllIllII=_IIlllIIIIl.AncestryChanged:Connect( function (_,_llllIIlIlI) if not _llllIIlIlI then _lIIlIllIll=true end
 end
 ) local _llIlIIlIlI,chegou=os.clock(),false while _lIlIlllIIl and _llIlIllIIl==_llllIIlIlI and not _lIIlIllIll and _lIIIlllIlI.Parent do local _IIlIllIIII=_IIlllIIIIl:FindFirstChild(string.char(0x49,0x6E,0x74,0x65,0x72,0x61,0x63,0x74,0x69,0x6F,0x6E,0x50,0x61,0x72,0x74)) if not _IIlIllIIII or not _IIlIllIIII:IsDescendantOf(workspace) then break end
 if os.clock()-_llIlIIlIlI>BICHO_TEMPO_MAX then break end
 local _IlllllIIlI=RunService.Heartbeat:Wait() local _lIIllllIlI=_IIlIllIIII.Position local _lIIlIlIlll=_lIIllllIlI-_lIIIlllIlI.Position local _IIlIlllIll=_lIIlIlIlll.Magnitude if _IIlIlllIll<=_IlllIIIlII then chegou=true break end
 local _lllIIlIlll=math.min(_IllIlIllII*_IlllllIIlI,_IIlIlllIll-_IlllIIIlII)_lIIIlllIlI.CFrame=CFrame.new(_lIIIlllIlI.Position+_lIIlIlIlll.Unit*_lllIIlIlll,_lIIllllIlI)_lIIIlllIlI.AssemblyLinearVelocity=Vector3.zero end
 _IllllIllII:Disconnect()_lllIlIIIII[_IIlllIIIIl]=os.clock()+(chegou and _lIIlIIIllI or BICHO_IGNORAR) if chegou then task.wait(BICHO_ESPERA) end
 end
 end
 )_IllIIlIlIl(string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E),string.char(0xF0,0x9F,0xA6,0xB4,0x20,0x42,0x69,0x63,0x68,0x6F,0x20,0x4F,0x4E)) end
 local _IlIllllIlI=Vector3.new(-956.14,34.50,1371.59) local _llllllllll=0.003 local _lIIIIIIlII=true local _IllllIlIIl=0x12C local _llIIIIlllI=0x2 local _lllIIlIlIl=0.35 local _IllIIIIlll=true local _lllIIlIIIl=Vector3.new(0x0,0x2,0x3) local _IIIIlIIlIl=string.char(0x5E,0x7B,0x3F,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x25,0x2D,0x25,0x78,0x2B,0x7D,0x3F,0x24) local _IIIlIlllll=false local _lIllIIIIlI=0x0 local function _lIlIllllll() return GuiService:GetGuiInset().Y end
 local function _lIllIllIII(_lIIIIIIlII) local _lllllIlIIl=_IllIIIIIII if _lllllIlIIl then _lllllIlIIl.CFrame=CFrame.new(_lIIIIIIlII)_lllllIlIIl.AssemblyLinearVelocity=Vector3.zero end
 end
 local function _lllIIIIIll(fn,_lllIlIIllI,intervalo,prazo) local _IIllIllllI=os.clock() while _IIIlIlllll and os.clock()-_IIllIllllI<_lllIlIIllI do if prazo and os.clock()>=prazo then return nil end
 local _IIlIlIIIIl=fn() if _IIlIlIIIIl then return _IIlIlIIIIl end
 task.wait(intervalo or 0.1) end
 return nil end
 local function _llIIIIIlll(_IIlllIIIIl,usarFire) local _lIllIIIIll=_lllIIlIlIl local _lIlIlIllII=_IIlllIIIIl and _IIlllIIIIl.prompt if _lIlIlIllII and _lIlIlIllII.Parent then pcall( function ()_lIlIlIllII.RequiresLineOfSight=false _lIlIlIllII.MaxActivationDistance=0x1E end
 )_lIllIIIIll=math.max(_lllIIlIlIl,_lIlIlIllII.HoldDuration+0.2) end
 _lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.E,false,game) if usarFire and _lIlIlIllII and _lIlIlIllII.Parent and fireproximityprompt then pcall(fireproximityprompt,_lIlIlIllII) end
 task.wait(_lIllIIIIll)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.E,false,game) end
 local function _IIllIIlIIl() local _IlIlIIIlIl={} local _IllIlllIll=_IIIllIIlIl:FindFirstChild(string.char(0x4D,0x65,0x6E,0x75,0x73)) local _llllIIlIIl=_IllIlllIll and _IllIlllIll:FindFirstChild(string.char(0x44,0x69,0x61,0x6C,0x6F,0x67,0x75,0x65)) if not _llllIIlIIl or not _llllIIlIIl.Visible then return _IlIlIIIlIl end
 for _,o in ipairs(_llllIIlIIl:GetDescendants()) do if o:IsA(string.char(0x54,0x65,0x78,0x74,0x42,0x75,0x74,0x74,0x6F,0x6E)) and o.Visible and o.AbsoluteSize.X>0x0 and o.AbsoluteSize.Y>0x0 and o.Text~="" then table.insert(_IlIlIIIlIl,o) end
 end
 return _IlIlIIIlIl end
 local function _IllIlllIIl(trecho) for _,o in ipairs(_IIllIIlIIl()) do if o.Text:lower():find(trecho,0x1,true) then return o end
 end
 return nil end
 local function _IllllIllII() return #_IIllIIlIIl()>0x0 end
 local function _lllllllllI(o) local _llIlIlIllI=o.AbsolutePosition+o.AbsoluteSize/0x2 local _lIlllIllll,_IIllIIlIll=_llIlIlIllI.X,_llIlIlIllI.Y+_lIlIllllll()_lllIllIIlI:SendMouseMoveEvent(_lIlllIllll,_IIllIIlIll,game)task.wait(0.05)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x0)task.wait(0.05)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x0) end
 local function _IIIIllIIlI() local _lIIllIllll,melhorNota for _,_llIlllIlIl in ipairs(workspace:GetDescendants()) do if _llIlllIlIl:IsA(string.char(0x50,0x72,0x6F,0x78,0x69,0x6D,0x69,0x74,0x79,0x50,0x72,0x6F,0x6D,0x70,0x74)) and _llIlllIlIl.Enabled then local _llllIIlIlI,_lIIIIIIlII=_llIlllIlIl.Parent,nil if _llllIIlIlI and _llllIIlIlI:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) then _lIIIIIIlII=_llllIIlIlI.Position elseif _llllIIlIlI and _llllIIlIlI:IsA(string.char(0x41,0x74,0x74,0x61,0x63,0x68,0x6D,0x65,0x6E,0x74)) then _lIIIIIIlII=_llllIIlIlI.WorldPosition elseif _llllIIlIlI and _llllIIlIlI:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) then _lIIIIIIlII=_llllIIlIlI:GetPivot().Position end
 if _lIIIIIIlII then local _IIlIlllIll=(_lIIIIIIlII-_IlIllllIlI).Magnitude local _lllIIIIIlI=(_llIlllIlIl.ActionText..string.char(0x20)..d.ObjectText):lower() local _llIllIlIlI=_lllIIIIIlI:find(string.char(0x63,0x61,0x76,0x61,0x6C,0x6F),0x1,true) or _lllIIIIIlI:find(string.char(0x68,0x6F,0x72,0x73,0x65),0x1,true) if _IIlIlllIll<0x19 and not _llIllIlIlI then local _IllIIlllll=_IIlIlllIll if _lllIIIIIlI:find(string.char(0x66,0x61,0x6C,0x61,0x72),0x1,true) or _lllIIIIIlI:find(string.char(0x74,0x61,0x6C,0x6B),0x1,true) then _IllIIlllll=_IllIIlllll-0x64 end
 if not melhorNota or _IllIIlllll<melhorNota then _lIIllIllll,melhorNota=_llIlllIlIl,_IllIIlllll end
 end
 end
 end
 end
 return _lIIllIllll end
 local function _llIIIIllII() for _llIlllIIlI=0x1,0x5 do if not _IIIlIlllll then return false end
 local _lIlIlIllII=_lllIIIIIll(_IIIIllIIlI,0x3,0.3)_llIIIIIlll({_lIlIlIllII=_lIlIlIllII},false) local _lIlIIIIlII=_lllIIIIIll(_IllllIllII,1.2,0.05) if not _lIlIIIIlII and _lIlIlIllII and fireproximityprompt then pcall(fireproximityprompt,_lIlIlIllII)_lIlIIIIlII=_lllIIIIIll(_IllllIllII,1.5,0.05) end
 if _lIlIIIIlII then return true end
 task.wait(0.3) end
 return false end
 local function _lllllIlllI() local _lllIlIIllI=os.clock()+0xC local _IIIlIIIIII=false while _IIIlIlllll and os.clock()<_lllIlIIllI do local _IlIlIIIlIl=_IIllIIlIIl() if #_IlIlIIIlIl==0x0 then if _IIIlIIIIII then return true end
 task.wait(0.1) else local _IIlIlllIll=_IllIlllIIl(string.char(0x67,0x68,0x6F,0x73,0x74,0x20,0x76,0x69,0x73,0x69,0x6F,0x6E)) local _lIIIllIllI=_IllIlllIIl(string.char(0x63,0x6C,0x6F,0x73,0x65)) if _IIlIlllIll then _lllllllllI(_IIlIlllIll);_IIIlIIIIII=true;task.wait(0.4) elseif _lIIIllIllI then _lllllllllI(_lIIIllIllI);_IIIlIIIIII=true;task.wait(0.4) else task.wait(0.5) end
 end
 end
 return false end
 local function _llllllIlll() local _IlIlIIIlIl={} local _lIlllllIII=_IIIllIIlIl:FindFirstChild(string.char(0x50,0x72,0x6F,0x6D,0x70,0x74,0x73)) local _lllllIllII=_lIlllllIII and _lIlllllIII:FindFirstChild(string.char(0x42,0x75,0x74,0x74,0x6F,0x6E,0x52,0x65,0x61,0x63,0x74,0x69,0x6F,0x6E,0x47,0x61,0x6D,0x65)) local _llIllllIlI=_lllllIllII and _lllllIllII:FindFirstChild(string.char(0x42,0x75,0x74,0x74,0x6F,0x6E,0x73)) if not _llIllllIlI or not _lllllIllII.Visible then return _IlIlIIIlIl end
 for _,o in ipairs(_llIllllIlI:GetDescendants()) do if o:IsA(string.char(0x47,0x75,0x69,0x42,0x75,0x74,0x74,0x6F,0x6E)) and o.Visible and o.AbsoluteSize.X>0x0 and o.AbsoluteSize.Y>0x0 then table.insert(_IlIlIIIlIl,o) end
 end
 return _IlIlIIIlIl end
 local _lIlIIIIIII=setmetatable({},{__mode=string.char(0x6B)}) local function _IIIIlIIIll(o,repetido) local _llIlIlIllI=o.AbsolutePosition+o.AbsoluteSize/0x2 local _lIlllIllll,_IIllIIlIll=_llIlIlIllI.X,_llIlIlIllI.Y+_lIlIllllll()_lllIllIIlI:SendMouseMoveEvent(_lIlllIllll,_IIllIIlIll,game)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x0)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x0) if repetido and _lIIIIIIlII and firesignal then pcall(firesignal,o.MouseButton1Click)pcall(firesignal,o.Activated) end
 end
 local _IIIlIlIlIl=nil local _lllIlllIll={} local function _IlIIlIIIIl(o) if o.Name==string.char(0x53,0x68,0x6F,0x70,0x49,0x6E,0x74,0x65,0x72,0x61,0x63,0x74,0x69,0x6F,0x6E,0x50,0x61,0x72,0x74) then _lllIlllIll[o]=true end
 end
 workspace.DescendantAdded:Connect(_IlIIlIIIIl)workspace.DescendantRemoving:Connect( function (o)_lllIlllIll[o]=nil end
 )task.spawn( function () for _,o in ipairs(workspace:GetDescendants()) do _IlIIlIIIIl(o) end
 end
 ) local function _IIlIlIlllI(_lIIIIIIlII) for shop in pairs(_lllIlllIll) do if shop and shop.Parent then if (shop.Position-_lIIIIIIlII).Magnitude<0x14 then return true end
 end
 end
 return false end
 local function _lIlIIlIIII(_IIllllllII) local _lllllIlIIl=_IllIIIIIII if not _lllllIlIIl then return nil end
 local _lIIllIllll,md,vistos=nil,nil,{} for _,_llIlllIlIl in ipairs(workspace:GetDescendants()) do if _llIlllIlIl.Name==string.char(0x47,0x68,0x6F,0x73,0x74,0x53,0x6D,0x6F,0x6B,0x65) then local _IIIIlllIll=_llIlllIlIl.Parent while _IIIIlllIll and _IIIIlllIll~=workspace do if _IIIIlllIll:IsA(string.char(0x4D,0x6F,0x64,0x65,0x6C)) and _IIIIlllIll.Name:match(_IIIIlIIlIl) then break end
 _IIIIlllIll=_IIIIlllIll.Parent end
 if _IIIIlllIll and _IIIIlllIll~=workspace and not vistos[_IIIIlllIll] and not _IIllllllII[_IIIIlllIll] then vistos[_IIIIlllIll]=true local _lIIIlllIlI=_IIIIlllIll:FindFirstChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74)) or _IIIIlllIll.PrimaryPart or _IIIIlllIll:FindFirstChildWhichIsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74),true) local _IIlIllIIII=_llIlllIlIl.Parent:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) and _llIlllIlIl.Parent or _lIIIlllIlI if _IIlIllIIII then if _IIlIlIlllI(_IIlIllIIII.Position) then continue end
 local _IIlIlllIll=(_IIlIllIIII.Position-_lllllIlIIl.Position).Magnitude if not md or _IIlIlllIll<md then _lIIllIllll,md={modelo=_IIIIlllIll,_lIIIlllIlI=_lIIIlllIlI or _IIlIllIIII,_IIlIllIIII=_IIlIllIIII,_lIlIlIllII=_IIIIlllIll:FindFirstChildWhichIsA(string.char(0x50,0x72,0x6F,0x78,0x69,0x6D,0x69,0x74,0x79,0x50,0x72,0x6F,0x6D,0x70,0x74),true),},_IIlIlllIll end
 end
 end
 end
 end
 return _lIIllIllll end
 if _IIIIlllIll and _IIIIlllIll~=workspace and not vistos[_IIIIlllIll] and not _IIllllllII[_IIIIlllIll] then vistos[_IIIIlllIll]=true local _lIIIlllIlI=_IIIIlllIll:FindFirstChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74)) or _IIIIlllIll.PrimaryPart or _IIIIlllIll:FindFirstChildWhichIsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74),true) local _IIlIllIIII=_llIlllIlIl.Parent:IsA(string.char(0x42,0x61,0x73,0x65,0x50,0x61,0x72,0x74)) and _llIlllIlIl.Parent or _lIIIlllIlI if _IIlIllIIII then local _IIlIlllIll=(_IIlIllIIII.Position-_lllllIlIIl.Position).Magnitude if not md or _IIlIlllIll<md then _lIIllIllll,md={modelo=_IIIIlllIll,_lIIIlllIlI=_lIIIlllIlI or _IIlIllIIII,_IIlIllIIII=_IIlIllIIII,_lIlIlIllII=_IIIIlllIll:FindFirstChildWhichIsA(string.char(0x50,0x72,0x6F,0x78,0x69,0x6D,0x69,0x74,0x79,0x50,0x72,0x6F,0x6D,0x70,0x74),true),},_IIlIlllIll end
 end
 end
 end
 end
 return _lIIllIllll end
 local function _IllIllIlII(_IIlllIIIIl) return ( not _IIlllIIIIl.modelo.Parent) or ( not _IIlllIIIIl.parte.Parent) or ( not _IIlllIIIIl.modelo:FindFirstChild(string.char(0x47,0x68,0x6F,0x73,0x74,0x53,0x6D,0x6F,0x6B,0x65),true)) end
 local function _IIlllIIlIl(_IIlllIIIIl) local _lllllIlIIl=_IllIIIIIII if _lllllIlIIl and _IIlllIIIIl.parte and _IIlllIIIIl.parte.Parent then local _IlIlllllll=_IIlllIIIIl.parte.Position _lllllIlIIl.CFrame=CFrame.lookAt(_IlIlllllll+_lllIIlIIIl,_IlIlllllll)_lllllIlIIl.AssemblyLinearVelocity=Vector3.zero end
 end
 local function _IIIlllIIll(_IIlllIIIIl) local _lllllIlIIl=_IllIIIIIII if _lllllIlIIl and _IIlllIIIIl.parte and _IIlllIIIIl.parte.Parent then if (_lllllIlIIl.Position-_IIlllIIIIl.parte.Position).Magnitude>0xC then _IIlllIIlIl(_IIlllIIIIl) end
 end
 end
 local function _IllllllIII(_IIlllIIIIl,prazo) local _lllIlIIllI=os.clock()+_llIIIIlllI local _llIlllIIlI=0x0 while _IIIlIlllll and os.clock()<_lllIlIIllI and not (prazo and os.clock()>=prazo) do _llIlllIIlI+=0x1 _IIlllIIlIl(_IIlllIIIIl)task.wait(0.1)_llIIIIIlll(_IIlllIIIIl,_llIlllIIlI>=0x2) local _IlIIIlllll=math.min(_lllIlIIllI,os.clock()+0.6) if prazo then _IlIIIlllll=math.min(_IlIIIlllll,prazo) end
 while _IIIlIlllll and os.clock()<_IlIIIlllll do if #_llllllIlll()>0x0 then return true end
 task.wait(0.03) end
 end
 return false end
 local function _IIlIlIIIIl(_IIllllllII,prazo) for _=0x1,0x8 do if ( not _IIIlIlllll) or (prazo and os.clock()>=prazo) then return nil end
 local _IIlllIIIIl=_lllIIIIIll( function () return _lIlIIlIIII(_IIllllllII) end
 ,0x8,0.2,prazo) if not _IIlllIIIIl then return nil end
 if _IllllllIII(_IIlllIIIIl,prazo) then return _IIlllIIIIl end
 _IIllllllII[_IIlllIIIIl.modelo]=true end
 return nil end
 local function _IIIlIlIIlI() local _IIllllllII={}_lIllIllIII(_IlIllllIlI)task.wait(0x1) if _llIIIIllII() then _lllllIlllI() else task.wait(0x1) end
 if not _IIIlIlllll then return end
 task.wait(0.3) local _IIlllIIIIl=_IIlIlIIIIl(_IIllllllII,nil) if not _IIlllIIIIl then task.wait(1.5) return end
 local _lllIllIllI=os.clock()+_IllllIlIIl local _lIlllllIll,falhas=nil,0x0 while _IIIlIlllll and os.clock()<_lllIllIllI do local _IllllIlIlI=#_llllllIlll() if _IllllIlIlI>0x0 then _lIlllllIll,falhas=nil,0x0 if _IllIIIIlll and not _IllIllIlII(_IIlllIIIIl) then _IIIlllIIll(_IIlllIIIIl) end
 elseif _IllIllIlII(_IIlllIIIIl) then _lIlllllIll,falhas=nil,0x0 _IIllllllII[_IIlllIIIIl.modelo]=true local _llIIIlIlII=_IIlIlIIIIl(_IIllllllII,_lllIllIllI) if _llIIIlIlII then _IIlllIIIIl=_llIIIlIlII else _IIllllllII={} end
 else _lIlllllIll=_lIlllllIll or os.clock() if os.clock()-_lIlllllIll>0.5 then if _IllllllIII(_IIlllIIIIl,_lllIllIllI) then falhas=0x0 else falhas+=0x1 if falhas>=0x2 then _IIllllllII[_IIlllIIIIl.modelo]=true local _llIIIlIlII=_IIlIlIIIIl(_IIllllllII,_lllIllIllI) if _llIIIlIlII then _IIlllIIIIl=_llIIIlIlII else _IIllllllII={} end
 falhas=0x0 end
 end
 _lIlllllIll=nil end
 end
 task.wait(0.05) end
 if _IIIlIlllll then _lIllIllIII(_IlIllllIlI)task.wait(0x1) end
 end
 _IIllIllIll= function ()_IIIlIlllll=false _lIllIIIIlI+=0x1 if _IIIlIlIlIl then _IIIlIlIlIl:Disconnect();_IIIlIlIlIl=nil end
 _lIlIIIIIII=setmetatable({},{__mode=string.char(0x6B)}) end
 local function _IIllIIIIIl()_IIllIllIll()_IIIlIlllll=true local _llllIIlIlI=_lIllIIIIlI _IIIlIlIlIl=RunService.Heartbeat:Connect( function () if not _IIIlIlllll then return end
 local _lIllIlllll=os.clock() for _,_llIllIIIlI in ipairs(_llllllIlll()) do local _lIlIIIlIIl=_lIlIIIIIII[_llIllIIIlI] if not _lIlIIIlIIl then _lIlIIIIIII[_llIllIIIlI]=_lIllIlllll task.spawn(_IIIIlIIIll,_llIllIIIlI,false) elseif _lIllIlllll-_lIlIIIlIIl>=_llllllllll then _lIlIIIIIII[_llIllIIIlI]=_lIllIlllll task.spawn(_IIIIlIIIll,_llIllIIIlI,true) end
 end
 end
 ) local _IIlIlIIIlI=0x2 local function _llIIIIIlll(_IIlllIIIIl,usarFire) local _lIllIIIIll=_lllIIlIlIl local _lIlIlIllII=_IIlllIIIIl and _IIlllIIIIl.prompt if _lIlIlIllII and _lIlIlIllII.Parent then pcall( function ()_lIlIlIllII.RequiresLineOfSight=false _lIlIlIllII.MaxActivationDistance=0x1E end
 )_lIllIIIIll=math.max(_lllIIlIlIl,_lIlIlIllII.HoldDuration+0.2) end
 task.wait(_IIlIlIIIlI) if not _IIIlIlllll then return end
 _lllIllIIlI:SendKeyEvent(true,Enum.KeyCode.E,false,game) if usarFire and _lIlIlIllII and _lIlIlIllII.Parent and fireproximityprompt then pcall(fireproximityprompt,_lIlIlIllII) end
 task.wait(_lIllIIIIll)_lllIllIIlI:SendKeyEvent(false,Enum.KeyCode.E,false,game) end
 local function _IllllllIII(_IIlllIIIIl,prazo) local _lllIlIIllI=os.clock()+_llIIIIlllI local _llIlllIIlI=0x0 while _IIIlIlllll and os.clock()<_lllIlIIllI and not (prazo and os.clock()>=prazo) do _llIlllIIlI+=0x1 _IIlllIIlIl(_IIlllIIIIl)task.wait(0.1)_llIIIIIlll(_IIlllIIIIl,_llIlllIIlI>=0x2) local _IlIIIlllll=math.min(_lllIlIIllI,os.clock()+0.6) if prazo then _IlIIIlllll=math.min(_IlIIIlllll,prazo) end
 while _IIIlIlllll and os.clock()<_IlIIIlllll do if #_llllllIlll()>0x0 then return true end
 task.wait(0.03) end
 end
 return false end
 local _lIIIlIlIlI=0.1 local function _IIIIlIIIll(o,repetido) local _llIlIlIllI=o.AbsolutePosition+o.AbsoluteSize/0x2 local _lIlllIllll,_IIllIIlIll=_llIlIlIllI.X,_llIlIlIllI.Y+_lIlIllllll()task.wait(_lIIIlIlIlI) if not (o and o.Parent and o.Visible) then return end
 _lllIllIIlI:SendMouseMoveEvent(_lIlllIllll,_IIllIIlIll,game)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,true,game,0x0)_lllIllIIlI:SendMouseButtonEvent(_lIlllIllll,_IIllIIlIll,0x0,false,game,0x0) if repetido and _lIIIIIIlII and firesignal then pcall(firesignal,o.MouseButton1Click)pcall(firesignal,o.Activated) end
 end
 task.spawn( function () while _IIIlIlllll and _lIllIIIIlI==_llllIIlIlI do local _IllIlllllI,err=pcall(_IIIlIlIIlI) if not _IllIlllllI then task.wait(1.5) end
 end
 end
 )_IllIIlIlIl(string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E),string.char(0xF0,0x9F,0x91,0xBB,0x20,0x41,0x75,0x74,0x6F,0x20,0x46,0x61,0x6E,0x74,0x61,0x73,0x6D,0x61,0x20,0x4F,0x4E)) end
 local function _IIIIIllIll()_IIIllIlllI()_lIllllIllI()_lIIIIllllI()_IIlllllIIl()_IllIIIIIIl()_IIllIllIll()_lIllIIIllI()_IIIIIlllIl()_IlIIIlIlIl=false if _lIIlIllIlI then pcall( function ()_lIIlIllIlI:Set(false) end
 ) end
 _IllIIlIlIl(string.char(0x53,0x68,0x75,0x74,0x64,0x6F,0x77,0x6E),string.char(0x54,0x75,0x64,0x6F,0x20,0x70,0x61,0x72,0x61,0x64,0x6F)) end
 _IIIlIlIlIl= function ()_lIllllIllI()_lIIIIllllI()_IIIIIlllIl() end
 local _llIIIIIIIl=nil _lIllllIllI= function ()_IIllllIIlI=false if _llIIIIIIIl then pcall( function ()task.cancel(_llIIIIIIIl) end
 );_llIIIIIIIl=nil end
 _IllIlIllIl=false _llIlllIlII()_lIIlIIIllI()_llllIllIII(true)_IIIIIlllIl()_IIllIlIlIl()_IIIIIlllIl()_IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x4F,0x66,0x66)) end
 local function _IlllIIIlIl() local _IllIIllIlI=os.clock()-_IlIIlIlIlI while _IIllllIIlI do local _llIlIlIllI=_IIIlIIIIll() if not _llIlIlIllI then if _llIllllIll then _IllIIllIlI=_IllIIllIlI or os.clock() if os.clock()-_IllIIllIlI>=_IlIIlIlIlI then if flyActive and _lIIllIlllI and _lIIllIlllI.Parent then _IlllIIllIl() end
 _IllIIllIlI=nil else task.wait(0.5) end
 else task.wait(0x1) end
 else _IllIIllIlI=nil if not flyActive or not _lIIllIlllI or not _lIIllIlllI.Parent then task.wait(0.1)continue end
 _IlllllIllI(_llIlIlIllI) end
 task.wait() end
 end
 local function _lIIllllIII()_IIIllIlllI()_lIllllIllI()task.wait(0.1)_IIllllIIlI=true _lIlIllIlIl()_lIIlIlIIIl()_IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x4F,0x6E))_llIIIIIIIl=task.spawn(_IlllIIIlIl)_IllIIlIlIl(string.char(0x46,0x61,0x72,0x6D),string.char(0x46,0x61,0x72,0x6D,0x20,0x49,0x6E,0x69,0x63,0x69,0x61,0x64,0x6F)) end
 local function _IIllIlIlII(key)_IIIllIlllI()_lIllllIllI()task.wait(0.1)_lllllIlllI=key _IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20)..CORRIDAS[key].nome)_IllIIlIlIl(string.char(0x43,0x6F,0x72,0x72,0x69,0x64,0x61),_IlIIlIlIII[key].nome)_lIlIllIlIl()corridaThread=task.spawn( function () while _lllllIlllI==key do _IlIlIIIlll(_IlIIlIlIII[key]) if _lllllIlllI~=key then break end
 task.wait(0x1) end
 end
 ) end
 local _lIlIlIllIl=_lllIIIlllI:CreateTab(string.char(0x53,0x74,0x61,0x74,0x75,0x73),nil)_lIlIlIllIl:CreateSection(string.char(0x52,0x65,0x61,0x6C,0x2D,0x54,0x69,0x6D,0x65,0x20,0x49,0x6E,0x66,0x6F))_llIIIlIlll=_lIlIlIllIl:CreateLabel(string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x4F,0x66,0x66))cLabel=_lIlIlIllIl:CreateLabel(string.char(0x50,0x6F,0x69,0x6E,0x74,0x73,0x20,0x69,0x6E,0x20,0x72,0x61,0x64,0x69,0x75,0x73,0x3A,0x20,0x30))aLabel=_lIlIlIllIl:CreateLabel(string.char(0x41,0x6E,0x74,0x69,0x2D,0x41,0x46,0x4B,0x3A,0x20,0x4F,0x66,0x66))cavLabel=_lIlIlIllIl:CreateLabel(string.char(0x48,0x6F,0x72,0x73,0x65,0x3A,0x20,0x4F,0x66,0x66))task.spawn( function () while true do task.wait(0x2)_IIIlIllllI(cLabel,string.char(0x50,0x6F,0x69,0x6E,0x74,0x73,0x20,0x69,0x6E,0x20,0x72,0x61,0x64,0x69,0x75,0x73,0x3A,0x20)..countPoints()) end
 end
 ) local _IllIIllIII=_lllIIIlllI:CreateTab(string.char(0x46,0x61,0x72,0x6D),nil)_IllIIllIII:CreateButton({Name=string.char(0x49,0x4E,0x49,0x43,0x49,0x41,0x52,0x20,0x46,0x4C,0x59,0x20,0x46,0x41,0x52,0x4D),Callback= function () if _IIllllIIlI then _lIllllIllI()_IllIIlIlIl(string.char(0x46,0x61,0x72,0x6D),string.char(0x46,0x61,0x72,0x6D,0x20,0x70,0x61,0x72,0x61,0x64,0x6F)) else _lIIllllIII() end
 end
 })_IllIIllIII:CreateSection(string.char(0x4D,0x69,0x73,0x73,0xC3,0xA3,0x6F,0x20,0x41,0x75,0x74,0x6F,0x6D,0xC3,0xA1,0x74,0x69,0x63,0x61))_IllIIllIII:CreateDropdown({Name=string.char(0x4D,0x69,0x73,0x73,0xC3,0xA3,0x6F,0x20,0x70,0x61,0x72,0x61,0x20,0x63,0x6C,0x69,0x63,0x61,0x72),Options={string.char(0x53,0x69,0x6E,0x67,0x6C,0x65,0x20,0x53,0x74,0x61,0x6B,0x65),string.char(0x42,0x69,0x67,0x20,0x54)},CurrentOption={string.char(0x53,0x69,0x6E,0x67,0x6C,0x65,0x20,0x53,0x74,0x61,0x6B,0x65)},MultipleOptions=false,Flag=string.char(0x6D,0x69,0x73,0x73,0x61,0x6F,0x44,0x72,0x6F,0x70,0x64,0x6F,0x77,0x6E),Callback= function (opt) local _lIlllIlllI=type(opt)==string.char(0x74,0x61,0x62,0x6C,0x65) and opt[0x1] or opt if _lIlllIlllI then _IIlIIIIIll=_lIlllIlllI end
 end
 })_IllIIllIII:CreateToggle({Name=string.char(0x54,0x65,0x6C,0x65,0x70,0x6F,0x72,0x74,0x61,0x72,0x20,0x61,0x74,0xC3,0xA9,0x20,0x61,0x73,0x20,0x63,0x6F,0x6F,0x72,0x64,0x65,0x6E,0x61,0x64,0x61,0x73),CurrentValue=false,Flag=string.char(0x74,0x65,0x6C,0x65,0x70,0x6F,0x72,0x74,0x65,0x4D,0x69,0x73,0x73,0x61,0x6F,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI)_IIIIlIlIII=_lIlllIlllI end
 })_IllIIllIII:CreateSection(string.char(0x43,0x6F,0x72,0x72,0x69,0x64,0x61,0x73)) local _lIIlIIIIIl,togRiver _lIIlIIIIIl=_IllIIllIII:CreateToggle({Name=string.char(0x43,0x72,0x6F,0x73,0x73,0x20,0x43,0x6F,0x75,0x6E,0x74,0x72,0x79),CurrentValue=false,Flag=string.char(0x63,0x72,0x6F,0x73,0x73,0x4C,0x6F,0x6F,0x70,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if not _lIlllIlllI then if _lllllIlllI==string.char(0x63,0x72,0x6F,0x73,0x73) then _llIlllIlII()_IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x4F,0x66,0x66))_IllIIlIlIl(string.char(0x43,0x6F,0x72,0x72,0x69,0x64,0x61),string.char(0x43,0x72,0x6F,0x73,0x73,0x20,0x43,0x6F,0x75,0x6E,0x74,0x72,0x79,0x20,0x70,0x61,0x72,0x61,0x64,0x61)) end
 return end
 if togRiver then pcall( function ()togRiver:Set(false) end
 ) end
 _IIllIlIlII(string.char(0x63,0x72,0x6F,0x73,0x73)) end
 })togRiver=_IllIIllIII:CreateToggle({Name=string.char(0x42,0x65,0x67,0x69,0x6E,0x20,0x52,0x69,0x76,0x65,0x72,0x20,0x52,0x75,0x6E),CurrentValue=false,Flag=string.char(0x72,0x69,0x76,0x65,0x72,0x4C,0x6F,0x6F,0x70,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if not _lIlllIlllI then if _lllllIlllI==string.char(0x72,0x69,0x76,0x65,0x72) then _llIlllIlII()_IIIlIllllI(_llIIIlIlll,string.char(0x53,0x74,0x61,0x74,0x75,0x73,0x3A,0x20,0x4F,0x66,0x66))_IllIIlIlIl(string.char(0x43,0x6F,0x72,0x72,0x69,0x64,0x61),string.char(0x42,0x65,0x67,0x69,0x6E,0x20,0x52,0x69,0x76,0x65,0x72,0x20,0x52,0x75,0x6E,0x20,0x70,0x61,0x72,0x61,0x64,0x61)) end
 return end
 if _lIIlIIIIIl then pcall( function ()_lIIlIIIIIl:Set(false) end
 ) end
 _IIllIlIlII(string.char(0x72,0x69,0x76,0x65,0x72)) end
 })_IllIIllIII:CreateSection(string.char(0x43,0x6F,0x6E,0x66,0x69,0x67,0x75,0x72,0x61,0xC3,0xA7,0xC3,0xB5,0x65,0x73))_IllIIllIII:CreateSlider({Name=string.char(0x46,0x6C,0x79,0x20,0x53,0x70,0x65,0x65,0x64),Range={0x5,0x12C},Increment=0x5,CurrentValue=0x32,Flag=string.char(0x73,0x70,0x65,0x65,0x64,0x53,0x6C,0x69,0x64,0x65,0x72),Callback= function (_lIlllIlllI)_IIlIIIIIlI=_lIlllIlllI end
 }) local _IIIlllIlII=_lllIIIlllI:CreateTab(string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E),nil)_IIIlllIlII:CreateSection(string.char(0x48,0x61,0x6C,0x6C,0x6F,0x77,0x65,0x65,0x6E,0x20,0x46,0x61,0x72,0x6D)) local _lIIllllllI,togBicho,togFant _lIIllllllI=_IIIlllIlII:CreateToggle({Name=string.char(0xF0,0x9F,0x8E,0x83,0x20,0x41,0x75,0x74,0x6F,0x20,0x41,0x62,0xC3,0xB3,0x62,0x6F,0x72,0x61),CurrentValue=false,Flag=string.char(0x61,0x62,0x6F,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if _lIlllIlllI then if togBicho then pcall( function ()togBicho:Set(false) end
 ) end
 if togFant then pcall( function ()togFant:Set(false) end
 ) end
 _llIllIlIll() else _IIlllllIIl() end
 end
 })togBicho=_IIIlllIlII:CreateToggle({Name=string.char(0xF0,0x9F,0xA6,0xB4,0x20,0x42,0x69,0x63,0x68,0x6F),CurrentValue=false,Flag=string.char(0x62,0x69,0x63,0x68,0x6F,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if _lIlllIlllI then if _lIIllllllI then pcall( function ()_lIIllllllI:Set(false) end
 ) end
 if togFant then pcall( function ()togFant:Set(false) end
 ) end
 _lllllIlIll() else _IllIIIIIIl() end
 end
 })togFant=_IIIlllIlII:CreateToggle({Name=string.char(0xF0,0x9F,0x91,0xBB,0x20,0x41,0x75,0x74,0x6F,0x20,0x46,0x61,0x6E,0x74,0x61,0x73,0x6D,0x61),CurrentValue=false,Flag=string.char(0x66,0x61,0x6E,0x74,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if _lIlllIlllI then if _lIIllllllI then pcall( function ()_lIIllllllI:Set(false) end
 ) end
 if togBicho then pcall( function ()togBicho:Set(false) end
 ) end
 _IIllIIIIIl() else _IIllIllIll() end
 end
 })_IIIlllIlII:CreateSection(string.char(0x56,0x65,0x6C,0x6F,0x63,0x69,0x64,0x61,0x64,0x65))_IIIlllIlII:CreateSlider({Name=string.char(0x53,0x70,0x65,0x65,0x64,0x20,0x56,0x6F,0x6F,0x20,0x28,0x41,0x62,0xC3,0xB3,0x62,0x6F,0x72,0x61,0x2F,0x42,0x69,0x63,0x68,0x6F,0x29),Range={0xA,0x1F4},Increment=0xA,CurrentValue=0x96,Flag=string.char(0x73,0x70,0x65,0x65,0x64,0x43,0x46,0x72,0x61,0x6D,0x65,0x53,0x6C,0x69,0x64,0x65,0x72),Callback= function (_lIlllIlllI)_IllIlIllII=_lIlllIlllI end
 }) local _lIIlllIlIl=_lllIIIlllI:CreateTab(string.char(0x48,0x6F,0x72,0x73,0x65,0x73),nil)_lIIlllIlIl:CreateToggle({Name=string.char(0x56,0x6F,0x61,0x72,0x20,0x61,0x74,0x65,0x20,0x57,0x69,0x6C,0x64,0x20,0x48,0x6F,0x72,0x73,0x65),CurrentValue=false,Flag=string.char(0x63,0x61,0x76,0x61,0x6C,0x6F,0x77,0x68,0x69),Callback= function (_lIlllIlllI) if _lIlllIlllI then _IlIllllIII()_llIlIlIllI() else _lIIIIllllI() end
 end
 })_lIIlllIlIl:CreateSlider({Name=string.char(0x53,0x70,0x65,0x65,0x64,0x20,0x28,0x76,0x6F,0x61,0x72,0x20,0x61,0x74,0x65,0x20,0x6F,0x20,0x63,0x61,0x76,0x61,0x6C,0x6F,0x29),Range={0x46,0x12C},Increment=0x5,CurrentValue=0x46,Flag=string.char(0x68,0x6F,0x72,0x73,0x65,0x66,0x6C,0x79,0x73,0x70,0x65,0x65,0x64,0x77,0x68,0x69),Callback= function (_lIlllIlllI)_IIllIIllII=_lIlllIlllI end
 })_lIIlIllIlI=_lIIlllIlIl:CreateToggle({Name=string.char(0x41,0x75,0x74,0x6F,0x20,0x43,0x6C,0x69,0x63,0x6B,0x20,0x28,0x31,0x73,0x29),CurrentValue=false,Flag=string.char(0x61,0x75,0x74,0x6F,0x43,0x6C,0x69,0x63,0x6B,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI)_IlIIIlIlIl=_lIlllIlllI end
 }) local _IllIlIllll=_lllIIIlllI:CreateTab(string.char(0x55,0x74,0x69,0x6C,0x73),nil)_IllIlIllll:CreateToggle({Name=string.char(0x41,0x6E,0x74,0x69,0x2D,0x41,0x46,0x4B),CurrentValue=false,Flag=string.char(0x61,0x66,0x6B,0x54,0x6F,0x67,0x67,0x6C,0x65),Callback= function (_lIlllIlllI) if _lIlllIlllI then _lIIIlIlIII();_IIIlIllllI(aLabel,string.char(0x41,0x6E,0x74,0x69,0x2D,0x41,0x46,0x4B,0x3A,0x20,0x4F,0x6E)) else _lIllIIIllI();_IIIlIllllI(aLabel,string.char(0x41,0x6E,0x74,0x69,0x2D,0x41,0x46,0x4B,0x3A,0x20,0x4F,0x66,0x66)) end
 end
 })_IllIlIllll:CreateButton({Name=string.char(0x50,0x41,0x52,0x41,0x52,0x20,0x54,0x55,0x44,0x4F),Callback= function ()_IIIIIllIll() end
 })_IIllllllII.CharacterAdded:Connect( function (nc)_IlIlllIllI=nc _IllIIIIIII=nc:WaitForChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64,0x52,0x6F,0x6F,0x74,0x50,0x61,0x72,0x74))_lIlIlIllll=nc:WaitForChild(string.char(0x48,0x75,0x6D,0x61,0x6E,0x6F,0x69,0x64))_lIllllIllI()_lIIIIllllI() end
 )_IllIIlIlIl(string.char(0x57,0x48,0x49,0x20,0x46,0x61,0x72,0x6D,0x20,0x76,0x31,0x32),string.char(0x41,0x62,0xC3,0xB3,0x62,0x6F,0x72,0x61,0x20,0x28,0x63,0x6C,0x69,0x71,0x75,0x65,0x20,0x34,0x32,0x38,0x2F,0x32,0x33,0x29,0x20,0x2B,0x20,0x42,0x69,0x63,0x68,0x6F,0x20,0x2B,0x20,0x46,0x61,0x6E,0x74,0x61,0x73,0x6D,0x61)) end
 )(...)
