getgenv().SecureMode = true

local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "FRITE HUB",
   LoadingTitle = "Best Gui",
   LoadingSubtitle = "FRITE on top",
   ConfigurationSaving = {
      Enabled = false,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided",
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

Rayfield:Notify(
    {
        Title = "You executed the script",
        Content = "FRITE/C.N on top",
        Duration = 5,
        Image = nil,
        Actions = {
            Ignore = {
                Name = "Okay!",
                Callback = function()
                    print("The user tapped Okay!")
                end
            }
        }
    }
)

local MainTab = Window:CreateTab("Home", 4483362458)

local Section = MainTab:CreateSection("Home")


local Button =
   MainTab:CreateButton(
        {
            Name = "Anti afk ðŸ˜´",
            Callback = function()
                loadstring(game:HttpGet("https://raw.githubusercontent.com/xpzrmodzz/anti-afk2/refs/heads/main/anti%20afk13"))()
            end
        }
    )


local Button =
   MainTab:CreateButton(
        {
            Name = "infinite yeild",
            Callback = function()
                loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
            end
        }
    )

local Button =
    MainTab:CreateButton(
        {
            Name = "keybord universal",
            Callback = function()
                loadstring(game:HttpGet("https://gist.githubusercontent.com/RedZenXYZ/4d80bfd70ee27000660e4bfa7509c667/raw/da903c570249ab3c0c1a74f3467260972c3d87e6/KeyBoard%20From%20Ohio%20Fr%20Fr"))()
            end
                
        }
    )


        
Rayfield:LoadConfiguration()
