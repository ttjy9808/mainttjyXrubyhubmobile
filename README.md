local Lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/InfinitiveUI",true))()
local Win = Lib:CreateWindow("ah",1,nil,nil)

local Main = Win:CreateTab("Main",function() warn(i) end)

Main:CreateButton("Instance E/Press",function()
for i,v in next, getgc(true) do
                if type(v) == "table" and rawget(v, "ID") and rawget(v, "Seconds") then
                    if typeof(v.Seconds) == "number" then
                        rawset(v, "Seconds", 0.001)
                    end
                end
            end
end)

Main:CreateButton("ServerHop",function()
game:GetService("TeleportService"):Teleport(1224212277, game:GetService("Players").LocalPlayer)
end)

local Heist = Win:CreateTab("heist status/level",function() warn(i) end)

Heist:CreateButton("DONT SUPPORT WITH THIS UI",function()
print("doesnt support mobile")
end)

local ESP = Win:CreateTab("ESP",function() warn(i) end)

ESP:CreateButton("ESP ATM",function()
for _,v in pairs(game.Workspace:GetDescendants()) do
        if v.Name == "ATM_600_5" then
            local a = Instance.new("BillboardGui", v)
            a.Size = UDim2.new(1, 0, 1, 0)
            a.Name = "ESP"
            a.AlwaysOnTop = true
            local b = Instance.new("Frame", a)
            b.Size = UDim2.new(1, 0, 1, 0)
            b.BackgroundTransparency = 1
            b.BorderSizePixel = 0
            local c = Instance.new("TextLabel", b)
            c.Text = v.Name
            c.Size = UDim2.new(1, 0, 1, 0)
            c.BackgroundTransparency = 1
            c.BorderSizePixel = 0
            c.TextColor3 = Color3.new(0, 1, 0)
            c.TextSize = 20
            
        local highlight = Instance.new("SelectionBox")
        highlight.Color3 = Color3.new(0, 1, 0)
        highlight.LineThickness = 0.1
        highlight.Adornee = v
        highlight.Parent = v
        highlight.Visible = true
        end
    end
end)

ESP:CreateButton("Luggage ESP",function()
for _,v in pairs(game.Workspace:GetDescendants()) do
        if v.Name == "Luggage_500_5" then
            local a = Instance.new("BillboardGui", v)
            a.Size = UDim2.new(1, 0, 1, 0)
            a.Name = "ESP"
            a.AlwaysOnTop = true
            local b = Instance.new("Frame", a)
            b.Size = UDim2.new(1, 0, 1, 0)
            b.BackgroundTransparency = 1
            b.BorderSizePixel = 0
            local c = Instance.new("TextLabel", b)
            c.Text = v.Name
            c.Size = UDim2.new(1, 0, 1, 0)
            c.BackgroundTransparency = 1
            c.BorderSizePixel = 0
            c.TextColor3 = Color3.new(0, 1, 0)
            c.TextSize = 20
            
        local highlight = Instance.new("SelectionBox")
        highlight.Color3 = Color3.new(0, 1, 0)
        highlight.LineThickness = 0.1
        highlight.Adornee = v
        highlight.Parent = v
        highlight.Visible = true
        end
    end
end)

ESP:CreateButton("Disable ESP",function()
 for _,v in pairs(game.Workspace:GetDescendants()) do
            if v.Name == "ESP" then
                v:Destroy()
            end
        end
end)

local Removelaser = Win:CreateTab("Remove Laser",function() warn(i) end)

Removelaser:CreateButton("Remove All Laser",function()
for i, v in pairs(game.Workspace:GetDescendants()) do
                if v.Name == "MovingLasers" or v.Name == "Laser" or v.Name == "GreenLaser" or v.Name == "GreenLasers" or v.Name == "Lasers" or v.Name == "VaultLasers" or v.Name == "NightLaser" or v.Name == "LaserDoor" or v.Name == "Lava" or v.Name == "Spotlight" or v.Name == "Flamethrowers" or v.Name == "Saws" or v.Name == "SpikeTraps" or v.Name == "Balls" or v.Name == "PressurePlates" or v.Name == "LaserWalls" or v.Name == "WallBeam" or v.Name == "Detectors" or v.Name == "Turrets" then
                    v:Destroy()
                end
            end
end)

Removelaser:CreateButton("Jewelry",function()
for i,v in pairs(game:GetService("Workspace").Heists["Jewelry Store"].Items:GetChildren()) do 
   if v.Name == "Spotlight" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

for i,v in pairs(game:GetService("Workspace").Heists["Jewelry Store"].Items:GetChildren()) do 
   if v.Name == "Laser" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

for i,v in pairs(game:GetService("Workspace").Heists["Jewelry Store"].Items:GetChildren()) do 
   if v.Name == "Flamethrowers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Apple Store",function()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do 
   if v.Name == "MovingLasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Pyramid level1",function()
for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level1:GetChildren()) do 
   if v.Name == "Lava" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

			      	for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level1:GetChildren()) do 
   if v.Name == "Saws" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

			      	for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level1:GetChildren()) do 
   if v.Name == "SpikeTraps" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

			      	for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level1:GetChildren()) do 
   if v.Name == "Flamethrowers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end

			      	for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level1:GetChildren()) do 
   if v.Name == "Balls" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Pyramid level2",function()
for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level2:GetChildren()) do 
   if v.Name == "Flamethrowers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level2:GetChildren()) do 
   if v.Name == "Lava" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
for i,v in pairs(game:GetService("Workspace").Heists.Pyramid.Level2:GetChildren()) do 
   if v.Name == "PressurePlates" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Club Level1",function()
for i,v in pairs(game:GetService("Workspace").Heists.Club.Level1.Items:GetChildren()) do 
   if v.Name == "Lasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Club Level2",function()
for i,v in pairs(game:GetService("Workspace").Heists.Club.Level2.Items:GetChildren()) do 
   if v.Name == "LaserWalls" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
end)

Removelaser:CreateButton("Bank",function()
for i,v in pairs(game:GetService("Workspace").Heists.Bank.Items.Chunk.Mint.Builds:GetChildren()) do 
   if v.Name == "GreenLaser" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
		for i,v in pairs(game:GetService("Workspace").Heists.Bank.Items.Chunk.Mint.RoomB:GetChildren()) do 
   if v.Name == "GreenLasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end
		for i,v in pairs(game:GetService("Workspace").Heists.Bank.Items.Chunk.Mint.RoomB:GetChildren()) do 
   if v.Name == "Lasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 

		for i,v in pairs(game:GetService("Workspace").Heists.Bank.Items.Chunk.Mint.RoomB:GetChildren()) do 
   if v.Name == "WallBeam" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
		for i,v in pairs(game:GetService("Workspace").Heists.Bank.Items.Chunk.Mint.RoomB.Model:GetChildren()) do 
   if v.Name == "WallBeam" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
end)

Removelaser:CreateButton("Casino",function()
for i,v in pairs(game:GetService("Workspace").Heists.Casino.Stealthy.Items:GetChildren()) do 
   if v.Name == "Detectors" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
			for i,v in pairs(game:GetService("Workspace").Heists.Casino.Stealthy.Items:GetChildren()) do 
   if v.Name == "MovingLasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
			for i,v in pairs(game:GetService("Workspace").Heists.Casino.Items:GetChildren()) do 
   if v.Name == "Lasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
end)

Removelaser:CreateButton("Plane",function()
for i,v in pairs(game:GetService("Workspace").Heists.Plane.Plane:GetChildren()) do 
   if v.Name == "Lasers" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
end)

Removelaser:CreateButton("Ship",function()
for i,v in pairs(game:GetService("Workspace").Heists.Ship.Ship:GetChildren()) do 
   if v.Name == "Turrets" then
       for a,b in pairs(v:GetChildren()) do
           b:Destroy()
       end
   end
end 
end)
