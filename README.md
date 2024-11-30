local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "ASTRAL HUB - animal simulator🐻",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "animal simulator🐻",
   LoadingSubtitle = "hub",
   Theme = "Default", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})



local farmTab = Window:CreateTab("Farm", 4483362458) -- Title, Image



local Toggle = farmTab:CreateToggle({
   Name = "farm Spawn👊🔥",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Fonction pour téléporter le joueur vers une position cible
local function teleportToTarget(targetPosition)
    if character and character:FindFirstChild("HumanoidRootPart") then
        character.HumanoidRootPart.CFrame = CFrame.new(targetPosition)
    end
end

-- Fonction pour téléporter le joueur vers un Dummy
local function teleportToDummy()
    local dummy = workspace.MAP.dummies.Dummy
    if dummy and dummy:FindFirstChild("HumanoidRootPart") then
        local dummyPosition = dummy.HumanoidRootPart.Position
        teleportToTarget(dummyPosition + Vector3.new(0, 1, 0)) -- Lève légèrement le joueur au-dessus du Dummy
    end
end

-- Exemple d'utilisation : téléporte le joueur vers le Dummy
teleportToDummy()

-- Arguments pour l'envoi d'événements au Dummy
local args = {
    [1] = workspace.MAP.dummies.Dummy.Humanoid,
    [2] = 1
}

isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

-- Définir la variable globale d'état
local isHitting = true -- Changez cette valeur pour activer/désactiver

            game:GetService("ReplicatedStorage").jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))
            task.wait(0.1) -- Pause minimale pour éviter de surcharger le thread
        end
    end)
end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "farm 5k🔥👊",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = workspace.MAP:FindFirstChild("5k_dummies").Dummy2.Humanoid,
    [2] = 4
}

isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))
task.wait(0.1) -- Pause

end
            end)
        end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local Toggle = farmTab:CreateToggle({
   Name = "fire ball spawn🔥",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = Vector3.new(-126.10099792480469, 646.1202392578125, 594.0977783203125),
    [2] = "NewFireball"
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").SkillsInRS.RemoteEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "fire ball 5k🔥",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = Vector3.new(-83.04418182373047, 595.0643920898438, 813.4301147460938),
    [2] = "NewFireball"
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").SkillsInRS.RemoteEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "auto coin",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do
game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("CoinEvent"):FireServer()
task.wait(0.1) -- Pause
wait()
end
end)
        end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "kill all boss🐎🦒🐈🔥🦀🐸🐻",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
while true do
local args = {
    [1] = workspace:WaitForChild("NPC"):WaitForChild("Griffin"):WaitForChild("Humanoid"),
    [2] = 3
}
 
game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
local args = {
    [1] = workspace:WaitForChild("NPC"):WaitForChild("CRABBOSS"):WaitForChild("Humanoid"),
    [2] = 1
}
 
game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
local args = {
    [1] = workspace:WaitForChild("NPC"):WaitForChild("LavaGorilla"):WaitForChild("Humanoid"),
    [2] = 5
}
 
game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
local args = {
    [1] = workspace:WaitForChild("NPC"):WaitForChild("CENTAUR"):WaitForChild("Humanoid"),
    [2] = 4
}
 
game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
local args = {
    [1] = workspace:WaitForChild("NPC"):WaitForChild("DragonGiraffe"):WaitForChild("Humanoid"),
    [2] = 1
}
 
game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
wait()
end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local Button = farmTab:CreateButton({
   Name = "anti afk😴",
   Callback = function()
loadstring(game:HttpGet("https://pastebin.com/raw/2n6FV7Sc"))()
   -- The function that takes place when the button is pressed
   end,
})



local pvpTab = Window:CreateTab("PvP", 4483362458) -- Title, Image



local isHitting = false
local Toggle = pvpTab:CreateToggle({
   Name = "kill aura👻",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local ReplicatedStorage = game:GetService("ReplicatedStorage")

while true do
    local args = {
        [1] = {
            ["action"] = "damage player",
            ["damage"] = 1000000000000  -- Remplace 1000000000000 par le montant de dégâts que tu souhaites infliger
        }
    }

    ReplicatedStorage.Events.NPCDamageEvent:FireServer(unpack(args))
    
    wait(0.1)  -- Attendre 1 seconde entre chaque envoi. Ajuste ce délai selon tes besoins.
end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})




local hommeTab = Window:CreateTab("Homme", 4483362458) -- Title, Image


local isHitting = false
local Toggle = hommeTab:CreateToggle({
   Name = "infini healt♾️",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   local args = {
    [1] = {
        ["action"] = "damage",
        ["damage"] = -math.huge  -- Utilisez 'math.huge' pour représenter l'infini
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

while true do
    game:GetService("ReplicatedStorage").Events.NPCDamageEvent:FireServer(unpack(args))
task.wait(0.01) -- Pause
    wait(0.01)  -- Attendre 1 seconde entre chaque envoi pour éviter une surcharge
end
end
            end)
        end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})
