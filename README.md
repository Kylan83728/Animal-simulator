local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()


local Window = Rayfield:CreateWindow({
   Name = "Rayfield Example Window",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Rayfield Interface Suite",
   LoadingSubtitle = "by Sirius",
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


local MainTab = Window:CreateTab("home", 4483362458) -- Title, Image
local Section = MainTab:CreateSection("home")



local isHitting = false
local players = game:GetService("Players")
local replicatedStorage = game:GetService("ReplicatedStorage")
local player = players.LocalPlayer

-- Fonction pour obtenir le joueur le plus proche
local function getClosestPlayer()
    local closestPlayer = nil
    local shortestDistance = math.huge  -- Une valeur initiale infinie

    -- Parcours de tous les joueurs
    for _, targetPlayer in pairs(players:GetPlayers()) do
        if targetPlayer ~= player and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
            local targetPosition = targetPlayer.Character.HumanoidRootPart.Position
            local playerPosition = player.Character.HumanoidRootPart.Position
            local distance = (targetPosition - playerPosition).Magnitude  -- Calcul de la distance

            -- Si cette distance est plus courte que la prÃ©cÃ©dente, on met Ã  jour
            if distance < shortestDistance then
                closestPlayer = targetPlayer
                shortestDistance = distance
            end
        end
    end

    return closestPlayer
end

local function startKillAura()
    isHitting = true
    while isHitting do
        local closestPlayer = getClosestPlayer()  -- RÃ©cupÃ¨re le joueur le plus proche
        if closestPlayer and closestPlayer.Character and closestPlayer.Character:FindFirstChild("Humanoid") then
            local args = {
                [1] = closestPlayer.Character.Humanoid,
                [2] = 1  -- Valeur Ã  envoyer au serveur, peut Ãªtre ajustÃ©e si nÃ©cessaire
            }
            -- Appelez la fonction sur le serveur
            replicatedStorage.jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))  -- VÃ©rifiez ce nom
        end
        task.wait()  -- Ajoutez une petite attente pour Ã©viter de trop solliciter le serveur
    end
end

local function stopKillAura()
    isHitting = false
end

-- CrÃ©ation du Toggle pour activer/dÃ©sactiver le kill aura
local Toggle = MainTab:CreateToggle({
    Name = "kill aura",
    CurrentValue = false,
    Flag = "Toggle1", 
    Callback = function(Value)
        if Value then
            task.spawn(startKillAura)
        else
            stopKillAura()
        end
    end,
})



Rayfield:LoadConfiguration()
