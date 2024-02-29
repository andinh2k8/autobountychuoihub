repeat wait()
until game:IsLoaded()
wait()
local TableChat = {"Long handsome","Config By #chi biet khoc"}
spawn(function()
    while wait() do 
        pcall(function()
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(TableChat[math.random(1,#TableChat)],"All")
            wait(45)
        end)
    end
end)
getgenv().Setting = {
    ["Team"] = "Marines", --Marines,Pirates
    ["Webhook"] = {
        ["Enabled"] = true,
        ["Url Webhook"] = "https://discord.com/api/webhooks/1151047514624098304/HV-9iI3lKp4OJ9o8usfHTjP8gkWRMR6K39eQMQiGQzsG0y6O6NU7WoDtuVD5vY6pqkvC", --Your Url
    },
    ["Misc"] = {
        ["AutoBuyRandomandStoreFruit"] = true,
        ["AutoBuySurprise"] = true,
    },
    ["Click"] = {
        ["Enable"] = true,
        ["Click Gun"] = true,
        ["OnLowHealthDisable"] = true,
        ["LowHealth"] = 4500,
    },
    ["SafeZone"] = {
        ["Enable"] = true,
        ["LowHealth"] = 4500,
        ["MaxHealth"] = 5000,
        ["Teleport Y"] = 2000
    },
    ["Race V4"] = {
        ["Enable"] = true,
    },
    ["Invisible"] = false,
    ["White Screen"] = false,
    ["GunMethod"] = false, --Support Only Melee And Gun,Not Invisible, Turn On Enabled Gun and Melee Please
    ["SpamSkill"] = false, -- Will use all skills as fast as possbile ignore holding skills
    ["Weapons"] = {
        ["Melee"] = {
            ["Enable"] = true,
            ["Delay"] = 3,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 1.5,
                },
               [ "X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.2,
                },

                ["C"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.2,
                },
            },
        },
        ["Blox Fruit"] = {
            ["Enable"] = false,
            ["Delay"] = 1,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 0,
                },
                ["X"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 1.5,
                },

                ["C"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 1.5,
                },
                ["V"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 0.3,
                },
                ["F"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 0,
                },
            },
        },
        ["Gun"] = {
            ["Enable"] = true,
            ["Delay"] = 2,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 0.12,
                },
                ["X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.18,
                },
            },
        },
        ["Sword"] = {
            ["Enable"] = true,
            ["Delay"] = 1,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.18,
                },
                ["X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.26,
                },
            },
        },
    }
}
repeat wait() until game:IsLoaded() and game.Players.LocalPlayer
spawn(function()
    while wait() do
            game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(child)
                if child.Name == 'ErrorPrompt' and child:FindFirstChild('MessageArea') and child.MessageArea:FindFirstChild("ErrorFrame") then
                    game:GetService("TeleportService"):Teleport(game.PlaceId)
                end
            end)
        end
    end)
loadstring(game:HttpGet("https://raw.githubusercontent.com/obiiyeuem/vthangsitink/main/BountyShit.lua"))() 
