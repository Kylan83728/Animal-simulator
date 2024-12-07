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


local mainTab = Window:CreateTab("home", 4483362458) -- Title, Image


local Section = mainTab:CreateSection("home")


local Toggle = mainTab:CreateToggle({
   Name = "kill aura",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local isHitting = false
local players = game:GetService("Players")
local replicatedStorage = game:GetService("ReplicatedStorage")
local player = players.LocalPlayer


local function startKillAura()
    isHitting = true
    while isHitting do
        for _, targetPlayer in pairs(players:GetPlayers()) do
            if targetPlayer ~= player and targetPlayer.Character and targetPlayer.Character:FindFirstChild("Humanoid") then
                local args = {
                    [1] = targetPlayer.Character.Humanoid,
                    [2] = 1 
                }
                replicatedStorage.jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))
            end
        end
        task.wait() 
end


local function stopKillAura()
    isHitting = false
end


local Toggle = pvpTab:CreateToggle({
    Name = "kill auraðŸ‘»",
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
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})
