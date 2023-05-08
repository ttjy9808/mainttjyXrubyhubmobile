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
local cmdlp = game.Players.LocalPlayer
rejoining = true
            local Decision = "any"
            local GUIDs = {}
            local maxPlayers = 0
            local pagesToSearch = 100
            if Decision == "fast" then pagesToSearch = 5 end
            local Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="))
            for i = 1,pagesToSearch do
                for i,v in pairs(Http.data) do
                    if v.playing ~= v.maxPlayers and v.id ~= game.JobId then
                        maxPlayers = v.maxPlayers
                        table.insert(GUIDs, {id = v.id, users = v.playing})
                    end
                end
                if Http.nextPageCursor ~= null then Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="..Http.nextPageCursor)) else break end
            end
            if Decision == "any" or Decision == "fast" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[math.random(1,#GUIDs)].id, cmdlp)
            elseif Decision == "smallest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[#GUIDs].id, cmdlp)
            elseif Decision == "largest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[1].id, cmdlp)
            else
                print("")
            end
            wait(3)
            rejoining = false
end)

local Heist = Win:CreateTab("heist status/level",function() warn(i) end)

heist:CreateButton("DONT SUPPORT WITH THIS UI",function()
print("doesnt support mobile")
end)
