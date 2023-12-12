local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local x = library:CreateWindow("ERA-SCRIPT") local b = w:CreateFolder("OP")

b:DestroyGui()

b:Box("Speed","number", function (val) S = val end) b:Box("Jump","number", function (val) J = val end)

b:Toggle("Speed",function(bool) getgenv().Speed = bool Speed(S) end) b:Toggle("Jump",function(bool) getgenv().Jump = bool Jump(J) end)

function TPCFrame (Player_CFrame) if game.Players.LocalPlayer. Character:FindFirstChild("Hu manoid RootPart") then game. Players.LocalPlayer.Char acter. Humanoid RootPart.CFrame = Player_CFrame end end

function RTPCFrame(M_CF) if game. Players. LocalPI ayer.Character:FindFirstChild("Humanoid RootPart") then M_CF.CFrame = game. Players.LocalPlaye r.Character.Humanoid RootPart.CFrame end

end

function PHP(Player_HP)
game.Players.LocalPlayer.Character.Humanoid.Health = Player_HP end

function Chat(Mes, Freq) spawn(function () while getgenv().Chat do local args = {[1] = Mes,[2] = "All"} game:GetService("ReplicatedStorage"). Defa ultChatSystemChatEvents.SayMessageReques t:FireServer(unpack(args)) wait(Freq) end end) end

function Speed(Nume) spawn(function () while getgenv().Speed do game:GetService("Players"). Local Player.Character. Humanoid. WalkSpeed = Nume if not getgenv().Speed then game: GetService("Players").Loca IPlayer. Character. Humanoid. WalkSpeed = 16 end wait() end end) end

function Jump(Nume) spawn(function () while getgenv().Jump do game: GetService("Players").Local Player.Character.Humanoid.JumpPower = Nume if not getgenv().Jump then game:GetService("Players").Loc alPlayer.Character.Humanoid.JumpPower = 50 end wait() end end) end

local a = x:CreateFolder("Reset Character")
a:Toggle("Kill",function(stateee)

if stateee then

game.Players.LocalPlayer.Character. Humanoid.Health = 0

else

game.Players.LocalPlayer.Character. Humanoid. Health = 100

end end)
