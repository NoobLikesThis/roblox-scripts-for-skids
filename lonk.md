### fe stand script
```
fe stand script----

--[[
leaked by the people
So this is the list of hats you need to be wearing (they are all free to get) :
https://www.roblox.com/catalog/451220849/Lavender-Updo
https://www.roblox.com/catalog/63690008/Pal-Hair
https://www.roblox.com/catalog/48474294/ROBLOX-Girl-Hair (this one is in a bundle) - https://www.roblox.com/bundles/282/ROBLOX-Girl 	
https://www.roblox.com/catalog/48474313/Red-Roblox-Cap
https://www.roblox.com/catalog/62234425/Brown-Hair
https://www.roblox.com/catalog/62724852/Chestnut-Bun (this one is in a bundle) - https://www.roblox.com/bundles/239/Woman
https://www.roblox.com/catalog/4819740796/Robox
also the last hat is the head of the stand]]--
 
 --[[Controls:
 Q - Summon/Unsummon
 E - Barrage - Throws Punches
 R - Mech Legs Walk - (when you spam the key) press "Q" to reset the stand
 T - Blackhole - Sucks people and things in a blackhole
 F - Arm Teleport - Your arm goes forward and teleports you
 G - Long Neck - Makes your neck very long
 H - Cape - Stand transforms into a cape and makes you quicker
 J - Dance - The stand starts dancing next to you
 Z - Stand Idle 1 - The stand stays at the same pose
 X - Stand Idle 2 - You walk very slow on top of the stand
 C - Dash Forward - The stand gives you a massive push and boost you forward
 V - Throne - The stand transforms into a throne for you
 B - Stand Idle 3 - The stand stands with its arms crossed behind you
 Those are pretty much the moves of the Fe Stand...]]--


for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetChildren()) do
if v:IsA("Accessory") then
print(v)
end
end
    
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
    if v:IsA("Accessory") and v.Handle:FindFirstChild("SpecialMesh") then
    ag = v.Handle:FindFirstChild("SpecialMesh")
    ag:Destroy()
    end
    end
    
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
    if v:IsA("Accessory") and v.Handle:FindFirstChild("Mesh") then
    ag = v.Handle:FindFirstChild("Mesh")
    ag:Destroy()
    end
    end

    wait()
    
    for _,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
		if v:IsA("Accessory") then
		    v.Handle.Transparency = 1
            v.Handle.Parent = workspace
			v.Parent = workspace
		end
    end

    wait(0.1)
    
    game.Players.LocalPlayer.Character:BreakJoints()
    
    wait(7)
    
local unanchoredparts = {}
local movers = {}
 local tog = true
 local move = false
local Player = game:GetService("Players").LocalPlayer
local Character = Player.Character
local mov = {};
local mov2 = {};

local Head = "MeshPartAccessory" --press f9 and find the hat that looks like a heads name and put it here
local x = -2   --Edit Position for head
local y = 2.8   --Edit Position for head x2
local z = 3 --Edit Position for head x3


local Hats = {rightarm = Character:WaitForChild("Hat1"),
             leftarm  = Character:WaitForChild("Pal Hair"),
             rightleg = Character:WaitForChild("LavanderHair"),
             leftleg  = Character:WaitForChild("Pink Hair"),
              torso1   = Character:WaitForChild("Robloxclassicred"),
             torso2   = Character:WaitForChild("Kate Hair"),
             
}

for i,v in next, Hats do
v.Handle.AccessoryWeld:Remove()
for _,mesh in next, v:GetDescendants() do
if mesh:IsA("Mesh") or mesh:IsA("SpecialMesh") then
mesh:Remove()
end
end
end
local Network = coroutine.create(function()
while true do
game:GetService("RunService").Heartbeat:Wait()
settings().Physics.AllowSleep = false
game:GetService("Players").LocalPlayer.MaximumSimulationRadius = math.pow(math.huge,math.huge)*math.huge
game:GetService("Players").LocalPlayer.SimulationRadius = math.pow(math.huge,math.huge)*math.huge
end
end)
coroutine.resume(Network)

function ftp(str)
    local pt = {};
    if str ~= 'me' and str ~= 'random' then
        for i, v in pairs(game.Players:GetPlayers()) do
            if v.Name:lower():find(str:lower()) then
                table.insert(pt, v);
            end
        end
    elseif str == 'me' then
        table.insert(pt, plr);
	elseif str == 'random' then
		table.insert(pt, game.Players:GetPlayers()[math.random(1, #game.Players:GetPlayers())]);
    end
    return pt;
end

Character.Head.Transparency = 0
Character.Head.face:Remove()
Character.Torso.Transparency = 0
Character["Right Arm"].Transparency = 0
Character["Left Arm"].Transparency = 0
Character["Right Leg"].Transparency = 0
Character["Left Leg"].Transparency = 0
local function align(i,v)
local att0 = Instance.new("Attachment", i)
att0.Position = Vector3.new(0,0,0)
local att1 = Instance.new("Attachment", v)
att1.Position = Vector3.new(0,0,0)
local AP = Instance.new("AlignPosition", i)
AP.Attachment0 = att0
AP.Attachment1 = att1
AP.RigidityEnabled = false
AP.ReactionForceEnabled = false
AP.ApplyAtCenterOfMass = true
AP.MaxForce = 9999999
AP.MaxVelocity = math.huge
AP.Responsiveness = 65
local AO = Instance.new("AlignOrientation", i)
AO.Attachment0 = att0
AO.Attachment1 = att1
AO.ReactionTorqueEnabled = true
AO.PrimaryAxisOnly = false
AO.MaxTorque = 9999999
AO.MaxAngularVelocity = math.huge
AO.Responsiveness = 50
end
align(Hats.torso1.Handle, Character["Torso"])
align(Hats.torso2.Handle, Character["Torso"])
align(Hats.rightarm.Handle, Character["Torso"])
align(Hats.leftarm.Handle, Character["Torso"])
align(Hats.rightleg.Handle, Character["Torso"])
align(Hats.leftleg.Handle, Character["Torso"])
Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)

Character:WaitForChild("Torso"):FindFirstChild("Attachment").Name = "Attachment1"
Character:WaitForChild("Torso"):FindFirstChild("Attachment").Name = "Attachment2"
Character:WaitForChild("Torso"):FindFirstChild("Attachment").Name = "Attachment3"
Character:WaitForChild("Torso"):FindFirstChild("Attachment").Name = "Attachment4"
Character:WaitForChild("Torso"):FindFirstChild("Attachment").Name = "Attachment5"

Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

Character:WaitForChild(Head).Handle.AccessoryWeld:Remove()
local alignpos = Instance.new("AlignPosition", Character)
local alignorien = Instance.new("AlignOrientation", Character)
local att1 = Instance.new("Attachment", Character:WaitForChild(Head).Handle)
local att2 = Instance.new("Attachment", Character:WaitForChild("Head"))
alignpos.Attachment0 = att1
alignpos.Attachment1 = att2
alignpos.RigidityEnabled = false
alignpos.ReactionForceEnabled = false
alignpos.ApplyAtCenterOfMass = true
alignpos.MaxForce = 99999999
alignpos.MaxVelocity = math.huge
alignpos.Responsiveness = 65
alignorien.Attachment0 = att1
alignorien.Attachment1 = att2
alignorien.ReactionTorqueEnabled = true
alignorien.PrimaryAxisOnly = false
alignorien.MaxTorque = 99999999
alignorien.MaxAngularVelocity = math.huge
alignorien.Responsiveness = 50
att2.Position = Vector3.new(x,y,z)






game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "z" then
     if toggle == false then
         
         Character.Humanoid.WalkSpeed = 16
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
            Character.Humanoid.HipHeight = 0
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.1,1.9,-0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,1.9,0.7)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-2.9,2.2,-1)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,1.9,0.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.1,0.1,0)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,-0.1,0.7)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(95,50,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(70,0,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(90,50,10)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,50,20)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(95,50,0)
                
           
 
	    

                
            att2.Position = Vector3.new(-1.7,y,0.3)
            toggle = false
        end
    end
end)


game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "x" then
     if toggle == false then
         

          
         Character.Humanoid.WalkSpeed = 16
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
     
       
     Character.Humanoid.WalkSpeed = 5
            Character.Humanoid.HipHeight = 6
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,-5.9,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,-5.9,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,-3.9,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.2,-3.9,-0.3)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-7.9,-0.3)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-7.9,0)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(70,0,20)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(70,0,-20)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                
                
           
 
	    

                
            att2.Position = Vector3.new(0,-5.5,0)
            toggle = false
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "c" then
     if tog == true then
         
         tog = false
         
         Character.Humanoid.HipHeight = 0
         
         att2.Position = Vector3.new(0,0.5,1)
         
          Character.Humanoid.WalkSpeed = 16
          
           Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
         Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.6,0.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.6,0.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-0.5,3.2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-0.5,3.2)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(-35,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(10,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(-35,0,0)
                
    wait(0.5)

                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.6,1)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.6,1)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-0.5,3.2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-0.5,3.2)
                
    wait(0.1)
    
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.6,2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.6,2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-0.5,3.2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-0.5,3.2)
            
            wait(0.1)
            
            Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.6,0.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.6,0.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-0.5,3.2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-0.5,3.2)
            
            wait(0.1)
            
            game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector*300
            
                wait(0.5)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                att2.Position = Vector3.new(x,y,z)
                wait(1)
            tog = true
        end
    end
end)


game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "q" then
     if toggle == false then
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
         Character.Humanoid.WalkSpeed = 16
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
     Character.Humanoid.WalkSpeed = 16
     Character.Humanoid.HipHeight = 0
            Character.Humanoid.HipHeight = 0
          Character:WaitForChild("Torso").Attachment.Position = Vector3.new(500,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(500,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(500,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(500,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(200,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(500,0,3)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(-35,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(10,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(-35,0,0)
                
                
           
 
	    

                
            att2.Position = Vector3.new(500,0.5,1)
            toggle = false
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "v" then
     if toggle == false then
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
           
            
            Character.Humanoid.HipHeight = 1.8
            
            wait(0.2)
            
            
            Character.Humanoid.Sit = true
            
            Character.Torso.Anchored = true
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,1)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,-0.5,-0.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,-0.5,-0.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-1)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-1)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(0,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                
                
           
 
	    

                
            att2.Position = Vector3.new(0,-5,-1)
            toggle = false
        end
    end
end)


game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "e" then
     if tog == true then
         
         Character.Humanoid.HipHeight = 0
         
         Character.Humanoid.WalkSpeed = 5
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
         att2.Position = Vector3.new(0,0.6,-3.3)
         
         tog = false
         

    

           Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.5,-6)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-3)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,20,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-40,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                
            wait(.06)
            
            att2.Position = Vector3.new(0.3,0.6,-3.3)
            
                
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
            
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,15,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-40,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.08)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
            
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,15,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.08)
             
             att2.Position = Vector3.new(0.5,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,40,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-15,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                
            wait(.08)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            

             wait(.08)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
         
            wait(.07)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.07)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.07)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.07)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.07)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-1.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.07)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.07)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.07)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.07)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                            
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
             wait(.06)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.06)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                
             wait(.06)
             
             att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.06)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5) 
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
            
            wait(.06)
            
            att2.Position = Vector3.new(0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1,0.5,-2)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)
            
                                        Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,-20,0)
            
            wait(.06)
            
            att2.Position = Vector3.new(-0.3,0.6,-3.3)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1,0.5,-2)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.8,0.5,-8)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2.5)    
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,30,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-30,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(110,20,0)
                
                wait(0.1)
               
               att2.Position = Vector3.new(0.3,0.6,-2.5)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-2.7)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-2.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0,-2.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0,-2.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-2)    
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,5,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(65,-2,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(130,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(130,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,5,0)
                
                wait(0.3)
                
                               att2.Position = Vector3.new(0,3.6,-3.5)
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,3,-3.6)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,3,-3.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,3,-3.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,3.7,-4.6)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,1,-3.5)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,1,-3.5)    
            
                            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,5,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(70,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(-55,-2,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,5,0)
                
                
               wait(1)
            
            
         wait()
           
             
          Character.Humanoid.Sit = false
         
         Player.Character.Humanoid.WalkSpeed = 16
         
         Character.Torso.Anchored = false
         
         att2.Position = Vector3.new(x,y,z)
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
            wait(1)
            tog = true
                
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "f" then
     if tog == true then
         
         Character.Humanoid.WalkSpeed = 4
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
        toggle = false
                
                att2.Position = Vector3.new(x,y,z)
                
           
             Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
                wait(0.1)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                wait()
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                 Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2.5,2.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)
           
           wait(1)
           
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2.5,-50)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)
            
            wait(0.1)
 
	    
	    
	    Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)


                 Character:SetPrimaryPartCFrame(Character:GetPrimaryPartCFrame()*CFrame.new(0, 0, -50))
                 
                 Character.Humanoid.WalkSpeed = 16
         
                 
            att2.Position = Vector3.new(x,y,z)
            wait(1)
            tog = true
        end
    end
end)




game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "h" then
     if toggle == false then
         
         Character.Humanoid.WalkSpeed = 16
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
     
      Character.Humanoid.WalkSpeed = 30
            Character.Humanoid.HipHeight = 0
          Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,1.5)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.5,-2.2,5.4)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.5,-2.2,5.4)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-1.5,3.2)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-1.5,3.2)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(-50,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(-10,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(-30,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(-30,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(-50,0,0)
                
                
           
 
	    

                
            att2.Position = Vector3.new(0,-20,1)
            toggle = false
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "g" then
     if toggle == false then
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
             Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)


		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
           
            
            Character.Humanoid.HipHeight = 0
            
            wait(0.2)
            
            
            Character.Humanoid.Sit = false
            
            Character.Torso.Anchored = false
            
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(0,2,0)
            Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0,4,0)
            Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(0,6,0)
            Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0,8,0)
            Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(0,10,0)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0,12,0)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                
                
           
 
	    

                
            att2.Position = Vector3.new(0,12.8,0)
            toggle = false
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "b" then
     if toggle == false then
         
         Character.Humanoid.WalkSpeed = 16
         
         Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
            Character.Humanoid.HipHeight = 0
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		      Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
            Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
            Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
            Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
            Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
            Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
           
                
                
                
                att2.Position = Vector3.new(x,y,z)
           toggle = true
 else
            Character.Humanoid.HipHeight = 0
            Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-0.4,2.3,2.6)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(0.5,2.3,2.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,0,3)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,0,2.7)
            
            
           
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,90,20)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,80,-20)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,-10,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
	    

                
            att2.Position = Vector3.new(0,2.8,3)
            toggle = false
        end
    end
end)


game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "r" then
     if toggle == false then
         Character.Humanoid.WalkSpeed = 0
          
          Character.Humanoid.HipHeight = 2.5
          
          att2.Position = Vector3.new(0,0.5,1)
          
Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-1.5,-5,0)
Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(1.5,-5,-1.5)
Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,-2,0)
Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,-2,-1)
Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-1.5,-3.5,0)
Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(1.5,-3.5,-1)
          
Hats.torso1.Handle.Attachment.Rotation = Vector3.new(0,0,0)
Hats.torso2.Handle.Attachment.Rotation = Vector3.new(40,0,0)
Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(65,0,0)
Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(160,0,0)
Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(140,0,0)
Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(0,0,0)

wait(.1)



Hats.torso1.Handle.Attachment.Rotation = Vector3.new(0,0,0)
Hats.torso2.Handle.Attachment.Rotation = Vector3.new(40,0,0)
Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(65,0,0)
Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(160,0,-0.5)
Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(140,0,0)
Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(0,0,0)

wait(.2)
game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector*100
Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-1.5,-5,-1.5)
Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(1.5,-5,0)
Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,-2,-1)
Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,-2,0)
Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-1.5,-3.5,-1)
Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(1.5,-3.5,0)
wait()
         
         
          Character.Humanoid.WalkSpeed = 0
          
          Character.Humanoid.HipHeight = 2.5
    

toggle = true

else

          
          att2.Position = Vector3.new(0,0.5,1)
          
 Character.Humanoid.WalkSpeed = 0
          
          Character.Humanoid.HipHeight = 2.5
    
wait()
att2.Position = Vector3.new(0,0.5,1)
Hats.torso1.Handle.Attachment.Rotation = Vector3.new(0,0,0)
Hats.torso2.Handle.Attachment.Rotation = Vector3.new(65,0,0)
Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(40,0,0)
Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(140,0,0)
Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(160,0,0)
Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(0,0,0)




Hats.torso1.Handle.Attachment.Rotation = Vector3.new(0,0,0)
Hats.torso2.Handle.Attachment.Rotation = Vector3.new(65,0,0)
Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(40,0,0)
Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(140,0,0)
Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(160,0,-0.5)
Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(0,0,0)


wait(.2)
game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector*100
Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-1.5,-5,0)
Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(1.5,-5,-1.5)
Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,-2,0)
Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,-2,-1)
Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-1.5,-3.5,0)
Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(1.5,-3.5,-1)
            toggle = false
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "j" then
     if tog == true then
         
         toggle = false
         
         Character.Humanoid.HipHeight = 0
         
         att2.Position = Vector3.new(-5,0.5,0)
         
          Character.Humanoid.WalkSpeed = 16
          
           Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
         Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.5,0,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,0,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-2,0)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)

            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                
            wait(0.1)
            
            att2.Position = Vector3.new(-5,0.5,0)
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,0,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-2,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,15)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,1.5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,1)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                  att2.Position = Vector3.new(-4.7,0.5,0)
                  
                 wait(0.05)
                 
                 att2.Position = Vector3.new(-5,0.5,0)
                 
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.6,0.2,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                    
                    
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,3)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,30)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,2.5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,2)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                
                wait(0.03)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.7,0.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,1)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,45)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,3)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,2)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                
                wait(0.03)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.7,0.5,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-2)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,60)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,3.5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,3)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                
                wait (0.02)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.7,0.6,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-4)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,75)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,4)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                
                wait(0.02)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.35,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.7,0.7,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-5)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,90)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,4)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                
                wait(0.02)
                
                att2.Position = Vector3.new(-5,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.35,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.7,1,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.55,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.55,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-6)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,110)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,4)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                
                wait(0.02)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.35,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,1.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.6,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.6,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-4)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,130)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                
                wait(0.02)
            
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.35,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.4,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.4,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.4,1.6,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.6,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.6,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-4)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,160)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6.5)
                
                wait(0.02)
                
                att2.Position = Vector3.new(-4.8,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.3,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.3,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.2,1.8,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.55,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.55,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-6)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,200)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                
                wait(0.2)
                
                att2.Position = Vector3.new(-5,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.4,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,1.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.65,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.65,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-3)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,130)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                
                                wait(0.2)
                                
                                att2.Position = Vector3.new(-4.8,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.3,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.3,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.2,1.8,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.55,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.55,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,8)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-6)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,200)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                
                                wait(0.2)
                                
                                att2.Position = Vector3.new(-5,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.4,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,1.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.65,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.65,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-3)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,130)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                                                wait(0.2)
                                                
                                                att2.Position = Vector3.new(-4.8,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.3,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.3,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.2,1.8,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.55,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.55,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-6)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,200)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,7)
                
                                wait(0.2)
                                
                                att2.Position = Vector3.new(-5,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.4,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,1.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.65,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.65,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-3)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,130)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                                                wait(0.2)
                                                
                                                att2.Position = Vector3.new(-4.8,0.5,0)
                
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.3,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.3,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.2,1.8,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.55,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.55,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-6)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,200)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                
                                wait(0.2)
                att2.Position = Vector3.new(-5,0.5,0)
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.15,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.4,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,1.4,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.65,-1.9,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.65,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,-3)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,130)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,6)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,6)
                
                        wait(0.1)
                        
                        Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-5.4,0.1,0)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-4.5,0,0)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,0,0)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-6.5,0,0)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-5.5,-2,0)
                Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-4.5,-2,0)
                
                Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(95,0,1.5)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(90,0,1)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,5)
                  att2.Position = Vector3.new(-4.7,0.5,0)
                  
                  wait(0.5)
                  
                Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                att2.Position = Vector3.new(x,y,z)
                wait(1)
            tog = true
        end
    end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
 if KeyPressed == "t" then
     if tog == true then
         
         tog = false
         
         Character.Humanoid.HipHeight = 0
         
         att2.Position = Vector3.new(0,0.5,-6)
         
          Character.Humanoid.WalkSpeed = 0
          
           Character.Humanoid.Sit = false
         
         Character.Torso.Anchored = false
         
         Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-0.5,0,-6)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(0.5,0,-6)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-1.5,0.5,-6.5)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(1.5,0.5,-6.5)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-0.5,-2,-6)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(0.5,-2,-6)
            
            Hats.torso1.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(0,10,10)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(0,-10,-10)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(100,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(80,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(90,0,0)
                
                                         for index, part in pairs(workspace:GetDescendants()) do
    if part:IsA("Part") and part.Anchored == false and part:IsDescendantOf(Player.Character) == false then
        table.insert(unanchoredparts, part)
        part.Massless = true
        part.CanCollide = false
        part.Transparency = 0
        if part:FindFirstChildOfClass("BodyPosition") ~= nil then
            part:FindFirstChildOfClass("BodyPosition"):Destroy()
        end
    end
end
for index, part in pairs(unanchoredparts) do
    local mover = Instance.new("BodyPosition", part)
    table.insert(movers, mover)
    mover.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
    local temp1 = Instance.new("BodyThrust", part)
    temp1.Location = Vector3.new(10,-3,-8)
    temp1.Force = Vector3.new(0,0,4000)

end
    for index, mover in pairs(movers) do
        mover.Position = Player.Character:FindFirstChild("HumanoidRootPart").CFrame:PointToWorldSpace(Vector3.new(0, 0, -10))
    end
               wait(4)
               
               Character.Humanoid.WalkSpeed = 16
               
               Character:WaitForChild("Torso").Attachment.Position = Vector3.new(-2.5,2,3)
                Character:WaitForChild("Torso").Attachment1.Position = Vector3.new(-1.5,2,3)
                Character:WaitForChild("Torso").Attachment2.Position = Vector3.new(-3.5,2,3)
                Character:WaitForChild("Torso").Attachment3.Position = Vector3.new(-0.7,2,2.7)
                Character:WaitForChild("Torso").Attachment4.Position = Vector3.new(-2.5,0.2,2.7)
            Character:WaitForChild("Torso").Attachment5.Position = Vector3.new(-1.5,0,3)

		       Hats.torso1.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                Hats.torso2.Handle.Attachment.Rotation = Vector3.new(90,10,0)
                Hats.rightarm.Handle.Attachment.Rotation = Vector3.new(80,-20,25)
                Hats.leftarm.Handle.Attachment.Rotation = Vector3.new(110,0,0)
                Hats.rightleg.Handle.Attachment.Rotation = Vector3.new(95,0,0)
                Hats.leftleg.Handle.Attachment.Rotation = Vector3.new(85,0,0)
                att2.Position = Vector3.new(x,y,z)
                
                wait(1)
   
            tog = true
        end
    end
end)

while true do
    Hats.CanCollide = true
    wait(0.5)
    end







netless-------

-- Netless ReAnimation
-- Created by MiAiHsIs1226
function Senti_IiiiIiIiIiiIiIIiIIiIi_(a,_)if a~=nil then if _>-2+(-41)+(2)+(72)+(95)+(-91)+(30)then print("you're usin fps unlock")end if Senti_IiiiIiIiIiiIiIIiIIiIie then print("you usin synapse.congratulations(I have no idea what to say)")end if("hello")=="x68x65x6Cx6Cx6F"then print("are you usin a bad exploit?")end return true elseif a==nil then return true else return end end Senti_IiiiIiIiIiiIiIIiIIiIie=Senti_IiiiIiIiIiiIiIIiIIiIie or nil Senti_IiiiIiIiIiiIiIIiIIiIid=Senti_IiiiIiIiIiiIiIIiIIiIid or Instance.new("Script") Senti_IiiiIiIiIiiIiIIiIIiIic=game:GetService("Workspace"):GetRealPhysicsFPS() Senti_IiiiIiIiIiiIiIIiIIiIib=game:GetService("Players")['LocalPlayer'] Senti_IiiiIiIiIiiIiIIiIIiIia=Senti_IiiiIiIiIiiIiIIiIIiIi_(Senti_IiiiIiIiIiiIiIIiIIiIib,Senti_IiiiIiIiIiiIiIIiIIiIic) if(not Senti_IiiiIiIiIiiIiIIiIIiIia)==true then return pcall(function()game:GetService("TestService"):Fail("Cannot load script")end)end return xpcall(function(a,b)local c=a local _=b a,b=nil,nil table.clear(c()) local _={} local b={} b.number=(65-(20/100)+.2) local d=getmetatable(newproxy(true)) local a=getmetatable(setmetatable({},{})) spawn(function()if c()then wait() d[2](d[3](d[4]))()else return"bitch"end end) local _=function(_)local d="" local a=function(_)return(_:gsub(".",function(_)if tonumber(_)then return _ else return""end end))end for _,c in next,string.split(_,"\a")do local _=tonumber(a(c)) if _~=nil then d=d..string.char(_-b.number)elseif c then d=d..c end end return d:sub(4)end a.index=_([['{\173;\176;\162;\165;\180;\181;\179;\170;\175;\168;}']]) d={} d[1-(20/100)+.2]=c() d[2-(20/100)+.2]=d[1][a.index] d[3-(20/100)+.2]=_ d[4-(20/100)+.2]=[['{\167;\176;\179;\97;\170;\109;\183;\97;\170;\175;\97;\175;\166;\185;\181;\109;\97;\168;\162;\174;\166;\123;\136;\166;\181;\148;\166;\179;\183;\170;\164;\166;\105;\99;\145;\173;\162;\186;\166;\179;\180;\99;\106;\111;\141;\176;\164;\162;\173;\145;\173;\162;\186;\166;\179;\111;\132;\169;\162;\179;\162;\164;\181;\166;\179;\123;\136;\166;\181;\133;\166;\180;\164;\166;\175;\165;\162;\175;\181;\180;\105;\106;\97;\165;\176;\78;\75;\170;\167;\97;\183;\123;\138;\180;\130;\105;\99;\131;\162;\180;\166;\145;\162;\179;\181;\99;\106;\97;\162;\175;\165;\97;\183;\111;\143;\162;\174;\166;\97;\191;\126;\99;\137;\182;\174;\162;\175;\176;\170;\165;\147;\176;\176;\181;\145;\162;\179;\181;\99;\97;\181;\169;\166;\175;\97;\78;\75;\168;\162;\174;\166;\123;\136;\166;\181;\148;\166;\179;\183;\170;\164;\166;\105;\99;\147;\182;\175;\148;\166;\179;\183;\170;\164;\166;\99;\106;\111;\137;\166;\162;\179;\181;\163;\166;\162;\181;\123;\164;\176;\175;\175;\166;\164;\181;\105;\167;\182;\175;\164;\181;\170;\176;\175;\105;\106;\78;\75;\183;\111;\151;\166;\173;\176;\164;\170;\181;\186;\97;\126;\97;\151;\166;\164;\181;\176;\179;\116;\111;\175;\166;\184;\105;\110;\115;\118;\111;\119;\109;\113;\109;\113;\106;\78;\75;\166;\175;\165;\106;\78;\75;\168;\162;\174;\166;\123;\136;\166;\181;\148;\166;\179;\183;\170;\164;\166;\105;\99;\147;\182;\175;\148;\166;\179;\183;\170;\164;\166;\99;\106;\111;\137;\166;\162;\179;\181;\163;\166;\162;\181;\123;\164;\176;\175;\175;\166;\164;\181;\105;\167;\182;\175;\164;\181;\170;\176;\175;\105;\106;\78;\75;\184;\162;\170;\181;\105;\111;\113;\114;\106;\78;\75;\183;\111;\151;\166;\173;\176;\164;\170;\181;\186;\97;\126;\97;\151;\166;\164;\181;\176;\179;\116;\111;\175;\166;\184;\105;\113;\109;\113;\109;\113;\106;\78;\75;\166;\175;\165;\106;\78;\75;\166;\175;\165;\78;\75;\166;\175;\165;\78;\75;\78;\75;\168;\162;\174;\166;\123;\136;\166;\181;\148;\166;\179;\183;\170;\164;\166;\105;\99;\148;\181;\162;\179;\181;\166;\179;\136;\182;\170;\99;\106;\123;\148;\166;\181;\132;\176;\179;\166;\105;\99;\148;\166;\175;\165;\143;\176;\181;\170;\167;\170;\164;\162;\181;\170;\176;\175;\99;\109;\97;\188;\97;\78;\75;\149;\170;\181;\173;\166;\97;\126;\97;\99;\143;\176;\181;\170;\167;\170;\164;\162;\181;\170;\176;\175;\99;\124;\78;\75;\149;\166;\185;\181;\97;\126;\97;\99;\143;\166;\181;\173;\166;\180;\180;\97;\162;\164;\181;\170;\183;\162;\181;\166;\165;\157;\175;\132;\179;\166;\162;\181;\166;\165;\97;\163;\186;\97;\142;\170;\130;\170;\137;\180;\138;\180;\114;\115;\115;\119;\99;\124;\78;\75;\138;\164;\176;\175;\97;\126;\97;\99;\179;\163;\185;\181;\169;\182;\174;\163;\123;\112;\112;\181;\186;\177;\166;\126;\130;\180;\180;\166;\181;\103;\170;\165;\126;\118;\114;\113;\120;\114;\121;\115;\114;\114;\117;\103;\184;\126;\114;\118;\113;\103;\169;\126;\114;\118;\113;\99;\124;\78;\75;\133;\182;\179;\162;\181;\170;\176;\175;\97;\126;\97;\114;\119;\124;\190;\106;\78;\75;}']]end,function(_)game:GetService("TestService"):Fail("\n"..(script or Instance.new('Script')):GetFullName().." has occurred an error:".._)end,getfenv,setfenv)
```
### knife
```
me = game.Players.LocalPlayer
char = me.Character
selected = false
attacking = false
hurt = false
grabbed = nil
mode = "kill"
bloodcolors = {"Bright red", "Really red", "Crimson"}
enabled = true
enabled2 = true
 
local breaksound = Instance.new("Sound")
breaksound.SoundId = "http://www.roblox.com/asset/?id=2801263"
breaksound.Parent = game.Workspace
breaksound.Volume = 0.8
    
local killsound = Instance.new("Sound")
killsound.SoundId = "http://www.roblox.com/asset?id=16950449"
killsound.Pitch = 0.65
killsound.Parent = game.Workspace
 
local drainsound = Instance.new("Sound")
drainsound.SoundId = "http://www.roblox.com/asset/?id=2785493"
drainsound.Pitch = 0.7
 
 
function prop(part, parent, collide, tran, ref, x, y, z, color, anchor, form)
part.Parent = parent
part.formFactor = form
part.CanCollide = collide
part.Transparency = tran
part.Reflectance = ref
part.Size = Vector3.new(x,y,z)
part.BrickColor = BrickColor.new(color)
part.TopSurface = 0
part.BottomSurface = 0
part.Anchored = anchor
part.Locked = true
part:BreakJoints()
end
 
function weld(w, p, p1, a, b, c, x, y, z)
w.Parent = p
w.Part0 = p
w.Part1 = p1
w.C1 = CFrame.fromEulerAnglesXYZ(a,b,c) * CFrame.new(x,y,z)
end
 
function mesh(mesh, parent, x, y, z, type)
mesh.Parent = parent
mesh.Scale = Vector3.new(x, y, z)
mesh.MeshType = type
end
 
function remgui()
    for _,v in pairs(me.PlayerGui:GetChildren()) do
        if v.Name == "Modeshow" then
            v:remove()
        end
    end
end
 
function inform(text,delay)
    remgui()
    local sc = Instance.new("ScreenGui")
    sc.Parent = me.PlayerGui
    sc.Name = "Modeshow"
    local bak = Instance.new("Frame",sc)
    bak.BackgroundColor3 = Color3.new(1,1,1)
    bak.Size = UDim2.new(0.94,0,0.1,0)
    bak.Position = UDim2.new(0.03,0,0.037,0)
    bak.BorderSizePixel = 0
    local gi = Instance.new("TextLabel",sc)
    gi.Size = UDim2.new(0.92,0,0.09,0)
    gi.BackgroundColor3 = Color3.new(0,0,0)
    gi.Position = UDim2.new(0.04,0,0.042,0)
    gi.TextColor3 = Color3.new(1,1,1)
    gi.FontSize = "Size14"
    gi.Text = text
    coroutine.resume(coroutine.create(function()
        wait(delay)
        sc:remove()
    end))
end
 
if char:findFirstChild("Bricks",true) then
    char:findFirstChild("Bricks",true):remove()
end
 
bricks = Instance.new("Model",me.Character)
bricks.Name = "Bricks"
 
--Parts-------------------------Parts-------------------------Parts-------------------------Parts----------------------
 
rarm = char:findFirstChild("Right Arm")
larm = char:findFirstChild("Left Arm")
lleg = char:findFirstChild("Left Leg")
torso = char:findFirstChild("Torso")
hum = char:findFirstChild("Humanoid")
rleg = char:findFirstChild("Right Leg")
 
righthold = Instance.new("Part")
prop(righthold, bricks, false, 1, 0, 0.1, 0.1, 0.1, "Mid gray", false, "Custom")
w11 = Instance.new("Weld")
weld(w11, rarm, righthold, 0, 0, 0, 0, 1, 0)
 
lefthold = Instance.new("Part")
prop(lefthold, bricks, false, 1, 0, 0.1, 0.1, 0.1, "Mid gray", false, "Custom")
w12 = Instance.new("Weld")
weld(w12, larm, lefthold, 0, 0, 0, 0, 1, 0)
 
hold = Instance.new("Part")
prop(hold, bricks, false, 0, 0, 0.2, 0.3, 0.3, "Black", false, "Custom")
oh = Instance.new("Weld")
weld(oh, torso, hold, -math.pi/-0.86, 1.5, math.rad(0), -0.35, -0.4, -0.5)
 
knife = Instance.new("Part")
knife.Material = "Wood"
prop(knife, bricks, false, 0, 0, 0.25, 1.1, 0.3, "Pine Cone", false, "Custom")
orr = Instance.new("Weld")
weld(orr, hold, knife, 0, 0, 0, 0, 0.7, 0)
ar = Instance.new("Weld")
weld(ar, lefthold, nil, math.pi/2, 0, math.pi, 0, 0, 0)
 
blade = Instance.new("Part")
blade.Material = "Neon"
prop(blade, bricks, false, 0, 0, 0.1, 2.5, 0.25, "Mid gray", false, "Custom")
Instance.new("BlockMesh",blade).Scale = Vector3.new(0.3,1,1)
w2 = Instance.new("Weld")
weld(w2, knife, blade, 0, 0, 0, 0, -0.65, 0)
 
blade2 = Instance.new("Part")
blade2.Material = "Neon"
prop(blade2, bricks, false, 0, 0, 0.1, 0.4, 0.25, "Mid gray", false, "Custom")
local mew = Instance.new("SpecialMesh",blade2)
mew.MeshType = "Wedge"
mew.Scale = Vector3.new(0.3,1,1)
w3 = Instance.new("Weld")
weld(w3, blade, blade2, 0, 0, 0, 0, -1.45, 0)
 
 
rb = Instance.new("Part")
prop(rb, bricks, false, 1, 0, 0.1, 0.1, 0.1, "Bright red", false, "Custom")
w13 = Instance.new("Weld")
weld(w13, torso, rb, 0, 0, 0, -1.5, -0.5, 0)
 
lb = Instance.new("Part")
prop(lb, bricks, false, 1, 0, 0.1, 0.1, 0.1, "Bright red", false, "Custom")
w14 = Instance.new("Weld")
weld(w14, torso, lb, 0, 0, 0, 1.5, -0.5, 0)
 
rw = Instance.new("Weld")
weld(rw, rb, nil, 0, 0, 0, 0, 0.5, 0)
 
lw = Instance.new("Weld")
weld(lw, lb, nil, 0, 0, 0, 0, 0.5, 0)
 
grabweld = nil
platlol = nil
lolhum = nil
 
function touch(h)
    if hurt then
        if grabbed == nil then
            local hu = h.Parent:findFirstChild("Humanoid")
            local head = h.Parent:findFirstChild("Head")
            local torz = h.Parent:findFirstChild("Torso")
            if hu ~= nil and head ~= nil and torz ~= nil and h.Parent.Name ~= name then
                if hu.Health > 0 then
                grabbed = torz
                hu.PlatformStand = true
                local w = Instance.new("Weld")
                weld(w,righthold,grabbed,math.pi/2,0.2,0,0.7,-0.9,-0.6)
                grabweld = w
                lolhum = hu
                local lolxd = true
                platlol = lolxd
                hu.Changed:connect(function(prop)
                    if prop == "PlatformStand" and platlol then
                        hu.PlatformStand = true
                    end
                end)
                end
            end
        end
    end
end
 
righthold.Touched:connect(touch)
lefthold.Touched:connect(touch)
 
function bleed(part,po)
    local lol1 = math.random(5,30)/100
    local lol2 = math.random(5,30)/100
    local lol3 = math.random(5,30)/100
    local lol4 = math.random(1,#bloodcolors)
    local p = Instance.new("Part")
    prop(p,part.Parent,false,0,0,lol1,lol2,lol3,bloodcolors[lol4],false,"Custom")
    p.CFrame = part.CFrame * CFrame.new(math.random(-5,5)/10,po,math.random(-5,5)/10)
    p.Velocity = Vector3.new(math.random(-25,25),math.random(-25,25),math.random(-25,25))
    p.RotVelocity = Vector3.new(math.random(-400,400)/10,math.random(-400,400)/10,math.random(-400,400)/10)
    p.CanCollide = true
    coroutine.resume(coroutine.create(function()
        wait(3)
        p:remove()
    end))
end
 
h = Instance.new("HopperBin",me.Backpack)
 
h.Name = "Knife"
 
script.Parent = h
 
 
bin = h
 
 
 
function select(mouse)
    orr.Part1 = nil
    ar.Part1 = knife
    mouse.Button1Down:connect(function()
        if attacking == false then
            attacking = true
            lw.Part1 = larm
            rw.Part1 = rarm
            hurt = true
            for i=1, 8 do
                rw.C0 = rw.C0 * CFrame.new(-0.03,0,-0.08) * CFrame.fromEulerAnglesXYZ(0.18,0.04,0)
                lw.C0 = lw.C0 * CFrame.new(0.06,0,-0.06) * CFrame.fromEulerAnglesXYZ(0.15,-0.11,-0.05)
                wait()
            end
            wait(1)
            hurt = false
            if grabbed == nil then
                for i=1, 4 do
                    rw.C0 = rw.C0 * CFrame.new(0.06,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.36,-0.08,0)
                    lw.C0 = lw.C0 * CFrame.new(-0.12,0,0.12) * CFrame.fromEulerAnglesXYZ(-0.3,0.22,0.05)
                    wait()
                end
                lw.C0 = CFrame.new(0,0,0)
                rw.C0 = CFrame.new(0,0,0)
                lw.Part1 = nil
                rw.Part1 = nil
                attacking = false
            end
        elseif hurt == false and grabbed ~= nil and mode == "drop" then
            enabled2 = true
            grabweld:remove()
            grabweld = nil
            platlol = false
            grabbed = nil
            lolhum.PlatformStand = false
            lolhum = nil
            for i=1, 4 do
                rw.C0 = rw.C0 * CFrame.new(0.06,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.36,-0.08,0)
                lw.C0 = lw.C0 * CFrame.new(-0.12,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.3,0.2,0)
                wait()
            end
            lw.C0 = CFrame.new(0,0,0)
            rw.C0 = CFrame.new(0,0,0)
            lw.Part1 = nil
            rw.Part1 = nil
            attacking = false
            platlol = nil
            
        elseif hurt == false and grabbed ~= nil and grabweld ~= nil and mode == "kill" and enabled2 == true then
            enabled2 = false
            enabled = false
            
            breaksound.Parent = grabbed
            breaksound:Play()
            
            for i=1, 5 do
                lw.C0 = lw.C0 * CFrame.new(0.02,0.15,-0.02) * CFrame.fromEulerAnglesXYZ(-0.05,0,-0.03)
                wait()
            end
            local duh = grabbed
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)                
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)
            bleed(duh,1)
            wait(0.12)
            for i=1, 5 do
                lw.C0 = lw.C0 * CFrame.new(-0.02,-0.15,0.02) * CFrame.fromEulerAnglesXYZ(0.05,-0,0.03)
                wait()
            end
            
            
            if grabbed.Parent:findFirstChild("HumanoidRootPart",true) then
                        for i, plr in pairs(game.Players:GetChildren()) do
                        if plr.Name ~= game.Players.LocalPlayer.Name then
                        for i = 1, 10 do
                        game.ReplicatedStorage.meleeEvent:FireServer(plr)
                        end
                 end
          end
            end
            grabbed.Parent.Humanoid.Health = grabbed.Parent.Humanoid.Health / 1.5
            
        elseif hurt == false and grabbed ~= nil and grabweld ~= nil and mode == "drain" and enabled == true then
                enabled = false
                enabled2 = true
                
                for i=1, 2 do
                    lw.C0 = lw.C0 * CFrame.new(0.06,0,-0.06) * CFrame.fromEulerAnglesXYZ(0.15,-0.11,-0.05)
                    wait()
                end 
 
                while char.Humanoid.Health == char.Humanoid.MaxHealth do
                    bleed(grabbed, 1)
                    char.Humanoid.Health = char.Humanoid.Health + 1
                    grabbed.Parent.Humanoid.Health = grabbed.Parent.Humanoid.Health - 1
                    wait(0.0335)
                end
                
                for i=1, 1 do
                    lw.C0 = lw.C0 * CFrame.new(-0.12,0,0.12) * CFrame.fromEulerAnglesXYZ(-0.3,0.22,0.05)
                    wait()
                end
                enabled = true
                
                
        elseif hurt == false and grabbed ~= nil and grabweld ~= nil and mode == "throw" then
            enabled2 = true
            grabweld:remove()
            grabweld = nil
            local bf = Instance.new("BodyForce",grabbed)
            bf.force = torso.CFrame.lookVector * 4000
            bf.force = bf.force + Vector3.new(0,1500,0)
            coroutine.resume(coroutine.create(function()
                wait(0.12)
                bf:remove()
            end))
            for i=1, 6 do
                rw.C0 = rw.C0 * CFrame.new(0,0,0) * CFrame.fromEulerAnglesXYZ(0.35,0,0)
                lw.C0 = lw.C0 * CFrame.new(0,0,0) * CFrame.fromEulerAnglesXYZ(-0.18,0,0)
                wait()
            end
            for i=1, 4 do
                rw.C0 = rw.C0 * CFrame.new(0,0,0) * CFrame.fromEulerAnglesXYZ(-0.47,0,0)
                lw.C0 = lw.C0 * CFrame.new(0,0,0) * CFrame.fromEulerAnglesXYZ(0.2,0,0)
                wait()
            end
            wait(0.2)
            platlol = false
            grabbed = nil
            lolhum.PlatformStand = false
            lolhum = nil
            for i=1, 4 do
                rw.C0 = rw.C0 * CFrame.new(0.06,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.36,-0.08,0)
                lw.C0 = lw.C0 * CFrame.new(-0.12,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.3,0.2,0)
                wait()
            end
            lw.C0 = CFrame.new(0,0,0)
            rw.C0 = CFrame.new(0,0,0)
            lw.Part1 = nil
            rw.Part1 = nil
            attacking = false
            platlol = nil
        elseif hurt == false and grabbed ~= nil and lolhum ~= nil and grabweld ~= nil and mode == "para" then
            enabled2 = true
            killsound.Parent = grabbed
            killsound:Play()
            for i=1, 5 do
                lw.C0 = lw.C0 * CFrame.new(0.02,0.12,0.1) * CFrame.fromEulerAnglesXYZ(-0.05,0,-0.03)
                wait()
            end
            local ne = grabbed:findFirstChild("Neck")
            coroutine.resume(coroutine.create(function()
                local duh = grabbed
                local duh2 = grabbed.Parent.Head
                local lolas = lolhum
                duh.RotVelocity = Vector3.new(math.random(-20,20),math.random(-20,20),math.random(-20,20))
                for i=1, 75 do
                    wait()
                    local hm = math.random(1,15)
                    pcall(function()
                        if hm == 1 then
                            duh2.Sound.Pitch = math.random(90,110)/100
                            duh2.Sound:play()
                            script.Parent.Splat:Play();
                        end
                    end)
 
                    if hm > 0 and hm < 4 then
 
                        bleed(duh,1)
                        bleed(duh2,-0.1)
                        bleed(duh,1)
                        bleed(duh2,-0.1)
                        bleed(duh,1)
                        bleed(duh,1)
                        bleed(duh,1)                                        
                    end
                end
                wait(1.2)
                
                lolas.Health = 0
                for i=1, 85 do
                    wait()
                    local hm = math.random(1,9)
                    pcall(function()
                        if hm == 1 then
                            duh2.Sound.Pitch = math.random(90,110)/100
                            duh2.Sound:play()
                        end
                    end)
                    if hm > 0 and hm < 3 then
                        bleed(duh,1)
                        bleed(duh2,-0.5)
                    end
                end
            end))
            for i=1, 3 do
                lw.C0 = lw.C0 * CFrame.new(0.02,0.12,0.1) * CFrame.fromEulerAnglesXYZ(-0.05,0,-0.03)
                if ne ~= nil then
                    grabbed.Neck.C0 = grabbed.Neck.C0 * CFrame.fromEulerAnglesXYZ(-0.35,0,0)
                end
                wait()
            end
            grabweld:remove()
            grabweld = nil
            for i=1, 4 do
                lw.C0 = lw.C0 * CFrame.new(-0.04,-0.24,-0.2) * CFrame.fromEulerAnglesXYZ(0.1,0,0.06)
                wait()
            end
            for i=1, 4 do
                rw.C0 = rw.C0 * CFrame.new(0.06,0,0.16) * CFrame.fromEulerAnglesXYZ(-0.36,-0.08,0)
                lw.C0 = lw.C0 * CFrame.new(-0.12,0,0.12) * CFrame.fromEulerAnglesXYZ(-0.3,0.22,0.05)
                wait()
            end
            lw.C0 = CFrame.new(0,0,0)
            rw.C0 = CFrame.new(0,0,0)
            lw.Part1 = nil
            rw.Part1 = nil
            platlol = false
            grabbed = nil
            lolhum = nil
            attacking = false
            platlol = nil
        end
    end)
    mouse.KeyDown:connect(function(kai)
        key = kai:lower()
        if key == "q" then
            mode = "drop"
            inform("Fix Knife",1)
        elseif key == "e" then
            mode = "kill"
            inform("Kill",1)
        end
    end)
end
 
function desel()
    repeat wait() until attacking == false
    orr.Part1 = knife
    ar.Part1 = nil
end
 
bin.Selected:connect(select)
bin.Deselected:connect(desel)
 
char.Humanoid.Died:connect(function()
    pcall(function()
        grabweld:remove()
        grabweld = nil
        grabbed = nil
        platlol = false
        platlol = nil
    end)
end)
 
inform("v2.0.2 Grab Knife Loaded | e = Kill /\ q = Fix Knife",3)
wait(3.2)
inform("Made By ASADCATONVERM :D | Edit by: C4#4172", 2)
```
