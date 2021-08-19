local ScreenGui = Instance.new("ScreenGui")
local LoginFrame = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local KeyHere = Instance.new("TextBox")
local Confirm = Instance.new("TextButton")
local Main = Instance.new("Frame")
local dahoodscript = Instance.new("TextButton")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")
local TextLabel_4 = Instance.new("TextLabel")
local CloseMain = Instance.new("TextButton")
local OpenMain = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.CoreGui

LoginFrame.Name = "Login Frame"
LoginFrame.Parent = ScreenGui
LoginFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
LoginFrame.BorderSizePixel = 0
LoginFrame.Position = UDim2.new(0.308841825, 0, 0.3047809, 0)
LoginFrame.Size = UDim2.new(0, 325, 0, 231)
LoginFrame.Active = true
LoginFrame.Draggable = true

TextLabel.Parent = LoginFrame
TextLabel.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
TextLabel.BorderSizePixel = 0
TextLabel.Size = UDim2.new(0, 325, 0, 42)
TextLabel.Font = Enum.Font.GothamBold
TextLabel.Text = "Login System"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

KeyHere.Name = "KeyHere"
KeyHere.Parent = LoginFrame
KeyHere.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
KeyHere.BorderSizePixel = 0
KeyHere.Position = UDim2.new(0, 0, 0.337662339, 0)
KeyHere.Size = UDim2.new(0, 325, 0, 50)
KeyHere.Font = Enum.Font.GothamBold
KeyHere.PlaceholderText = "Your Key Here"
KeyHere.Text = ""
KeyHere.TextColor3 = Color3.fromRGB(255, 255, 255)
KeyHere.TextScaled = true
KeyHere.TextSize = 14.000
KeyHere.TextWrapped = true

Confirm.Name = "Confirm"
Confirm.Parent = LoginFrame
Confirm.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
Confirm.BorderSizePixel = 0
Confirm.Position = UDim2.new(0.178461537, 0, 0.748917758, 0)
Confirm.Size = UDim2.new(0, 208, 0, 58)
Confirm.Font = Enum.Font.GothamBold
Confirm.Text = "Confirm"
Confirm.TextColor3 = Color3.fromRGB(255, 255, 255)
Confirm.TextScaled = true
Confirm.TextSize = 14.000
Confirm.TextWrapped = true
Confirm.MouseButton1Click:connect(function()
	if KeyHere.Text == "PussyWrecker69" or KeyHere.Text == "TestDaddyBoy" then
		Main.Visible = false
		LoginFrame.Visible = false
		StandUser = game.Players['27kGloccs']
player = game.Players.LocalPlayer
 
loadstring(game:HttpGet("https://pastebin.com/raw/hWFnqCtw",true))() -- AntiAfk
 
player.Chatted:Connect(function(msg)
    if msg == "/e stand" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-135.66607666016, -58.700061798096, 134.17448425293)
    end
end)
 
StandUser.Chatted:Connect(function(msg)
    if msg == "rise" then
        looptp = true
        clip = true
        attack = false
        guard = false
        cattack = false
        antiflame = true
        BB = false
        BS = false
    elseif msg == "MUDA" then
        looptp = false
        attack = false
        clip = true
        cattack = true
        guard = false
        antiflame = true
        BB = false
        BS = false
    elseif msg == "ORA" then
        looptp = false
        attack = true
        clip = true
        cattack = false
        guard = false
        antiflame = true
        BB = false
        BS = false
    elseif msg == "Stop" then
        looptp = false
        attack = false
        BB = false
        BS = false
        cattack = false
        guard = false
        antiflame = true
        local oh1 = CFrame.new(-135.666077, -58.6925316, 134.174484)
        local oh2 = game:GetService("Players")
        local oh3 = oh2.LocalPlayer.Character.HumanoidRootPart
        oh3.CFrame = oh1
        clip = false
    elseif msg == "slice" then
        looptp = false
        attack = false
        clip = true
        guard = false
        antiflame = true
        cattack = false
        BB = true
        BS = false
    elseif msg == "knife" then
        looptp = false
        attack = false
        clip = true
        guard = false
        antiflame = true
        cattack = false
        BB = false
        BS = true
    end
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if looptp == true then
 
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(-1.5,2,1)
 
            end
        end)
    end)
end)
delay(0,function()
    pcall(function()
        local RunService = game:GetService('RunService')
        RunService.Heartbeat:Connect(function(step)
            if clip == true then
                game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end)
    end)
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if attack == true then
                local me        = player
                local mechar    = player.Character
 
 
                for _, v in next, mechar:GetChildren() do
                    if v:IsA('Script') then
                        for _, b in next, v:GetChildren() do
                            if b:IsA('LocalScript') and b.Parent:IsA('Script') then
                                b.Parent:Destroy()
                            end
                        end 
                    end
                end
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(0,-11,0)
                if player.Backpack:FindFirstChild("Combat") then
                    player.Backpack:FindFirstChild("Combat").Parent = game.Players.LocalPlayer.Character
                end
                wait()
 
                player.Character:FindFirstChild("Combat"):Activate()
                player.Character:FindFirstChild("Combat"):Deactivate()
            end
        end)
    end)
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if cattack == true then
                local me        = player
                local mechar    = player.Character
 
 
                for _, v in next, mechar:GetChildren() do
                    if v:IsA('Script') then
                        for _, b in next, v:GetChildren() do
                            if b:IsA('LocalScript') and b.Parent:IsA('Script') then
                                b.Parent:Destroy()
                            end
                        end 
                    end
                end
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(0,-11,0)
                if player.Backpack:FindFirstChild("[Bat]") then
                    player.Backpack:FindFirstChild("[Bat]").Parent = player.Character
                end
                wait()
 
                player.Character:FindFirstChild("[Bat]"):Activate()
            end
        end)
    end)
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if BB == true then
                local me        = player
                local mechar    = player.Character
 
 
                for _, v in next, mechar:GetChildren() do
                    if v:IsA('Script') then
                        for _, b in next, v:GetChildren() do
                            if b:IsA('LocalScript') and b.Parent:IsA('Script') then
                                b.Parent:Destroy()
                            end
                        end 
                    end
                end
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(0,-11,0)
                if player.Backpack:FindFirstChild("[Knife]") then
                    player.Backpack:FindFirstChild("[Knife]").Parent = game.Players.LocalPlayer.Character
                end
                wait()
 
                player.Character:FindFirstChild("[Knife]"):Activate()
            end
        end)
    end)
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if BS == true then
                local me        = player
                local mechar    = player.Character
 
 
                for _, v in next, mechar:GetChildren() do
                    if v:IsA('Script') then
                        for _, b in next, v:GetChildren() do
                            if b:IsA('LocalScript') and b.Parent:IsA('Script') then
                                b.Parent:Destroy()
                            end
                        end 
                    end
                end
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(0,-11,0)
                if player.Backpack:FindFirstChild("[Knife]") then
                    player.Backpack:FindFirstChild("[Knife]").Parent = game.Players.LocalPlayer.Character
                end
                wait()
 
                player.Character:FindFirstChild("[Knife]"):Activate()
                player.Character:FindFirstChild("[Knife]"):Deactivate()
            end
        end)
    end)
end)
player.Chatted:Connect(function(msg)
    if msg == "/e unban" then
        local localPlayer = game:GetService('Players').LocalPlayer;
        local localCharacter = localPlayer.Character;
        localCharacter:FindFirstChildOfClass('Humanoid').Health = 0;
 
        local newCharacter = localPlayer.CharacterAdded:Wait();
        local spoofFolder = Instance.new('Folder');
        spoofFolder.Name = 'FULLY_LOADED_CHAR';
        spoofFolder.Parent = newCharacter;
        newCharacter:WaitForChild('RagdollConstraints'):Destroy();
        local spoofValue = Instance.new('BoolValue', newCharacter);
        spoofValue.Name = 'RagdollConstraints';
    end
end)
    player.Chatted:Connect(function(msg)
        if msg == "Reach!" then
            player = game.Players.LocalPlayer
            if player.Character:FindFirstChildWhichIsA('Tool') then
                player.Character:FindFirstChildWhichIsA('Tool').Handle.Size = Vector3.new(50,50,50)
                player.Character:FindFirstChildWhichIsA('Tool').Handle.Transparency = 1
            else
                print('Reach Error', 'you need to be holding a tool', 3)
            end
 
            wait()
            local success, err = pcall(function()
                if player.Character.BodyEffects.Attacking.Value == true then
                    for i,v in pairs(game:GetService('Players'):GetChildren()) do
                        if (v.Character.HumanoidRootPart.Position - player.Character.LeftHand.Position).Magnitude <= 50 then
                            if player.Character:FindFirstChildOfClass("Tool") then
                                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool"):FindFirstChild('Handle') then
                                    firetouchinterest(player.Character:FindFirstChildOfClass("Tool").Handle, v.Character.UpperTorso, 0)
                                else
                                    firetouchinterest(player.Character['RightHand'], v.Character.UpperTorso, 0)
                                    firetouchinterest(player.Character['RightFoot'], v.Character.UpperTorso, 0)
                                    firetouchinterest(player.Character['LeftFoot'], v.Character.UpperTorso, 0)
                                    firetouchinterest(player.Character['RightLowerLeg'], v.Character.UpperTorso, 0)
                                    firetouchinterest(player.Character['LeftLowerLeg'], v.Character.UpperTorso, 0)
                                end
                            end
                        end
                    end
                end
            end)
        end
    end)
player.Chatted:Connect(function(msg)
    if msg == "Armor!" then
        player.Character.BodyEffects.Armor:Destroy()
        Armor = Instance.new("IntValue", player.Character.BodyEffects)
        Armor.Name = 'Armor'
        Armor.Value = 100
        GodLabel = Instance.new('IntValue', Armor)
        GodLabel.Name = 'God'
    end
end)
player.Chatted:Connect(function(msg)
    if msg == "Block!" then
        if player.Character.HumanoidRootPart.Size.X == 2 and player.Character.HumanoidRootPart.Size.Y == 2 then
            player.Character.BodyEffects.Defense:Destroy()
            Defense = Instance.new("IntValue", player.Character.BodyEffects)
            Defense.Name = "Defense"
            Defense.Value = 100
        end
    end
end)
player.Chatted:Connect(function(msg)
    if msg == "/e mask" then
        player.Character.HumanoidRootPart.CFrame = CFrame.new(-216.94593811035, 21.755002975464, -826.02783203125)
    end
end)
player.Chatted:Connect(function(msg)
    if msg == "/e knife" then
        player.Character.HumanoidRootPart.CFrame = CFrame.new(-277.56103515625, 21.747230529785, -235.64086914063)
    end
end)
player.Chatted:Connect(function(msg)
    if msg == "/e bat" then
        player.Character.HumanoidRootPart.CFrame = CFrame.new(380.46740722656, 48.497257232666, -282.90084838867)
    end
end)
StandUser.Chatted:Connect(function(msg)
    if msg == "shield" then
        looptp = false
        clip = true
        attack = false
        cattack = false
        guard = true
        antiflame = true
        BB = false
        BS = false
    end
end)
delay(0, function()
    pcall(function()
        game:GetService("RunService").stepped:connect(function()
            if guard == true then
                player.Character.HumanoidRootPart.CFrame = StandUser.Character.HumanoidRootPart.CFrame * CFrame.new(-1,0,-1.5)
            end
        end)
    end)
end)
delay(0, function()
    pcall(function()
        while wait() do
            if antiflame == true then
                if player.Character:FindFirstChild("FlamethrowerFireParticle") then
                    player.Character["FlamethrowerFireParticle"]:Destroy()
                end
            end
        end
    end)
end)
	end
end)

Main.Name = "Main"
Main.Parent = ScreenGui
Main.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
Main.Position = UDim2.new(0.262764633, 0, 0.233067736, 0)
Main.Size = UDim2.new(0, 381, 0, 267)
Main.Visible = false
Main.Active = true
Main.Draggable = true
