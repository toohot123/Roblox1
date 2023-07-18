Nexus_Version = 104

local FileName, Success, Error, Function = 'ic3w0lf22.Nexus.lua'

if isfile and readfile and isfile(FileName) then -- Execute ASAP, update later.
	Function, Error = loadstring(readfile(FileName), 'Nexus')

	if Function then
		Function()

		if Nexus then Nexus:Connect() end
	end
end

for i=1, 10 do
	Success, Error = pcall(function()
		local Response = (http_request or (syn and syn.request)) { Method = 'GET', Url = 'https://raw.githubusercontent.com/ic3w0lf22/Roblox-Account-Manager/master/RBX%20Alt%20Manager/Nexus/Nexus.lua' }

		if not Response.Success then error(('HTTP Error %s'):format(Response.StatusCode)) end

		Function, Error = loadstring(Response.Body, 'Nexus')

		if not Function then error(Error) end

		if isfile and not isfile(FileName) then
			writefile(FileName, Response.Body)
		end
		
		if not Nexus then -- Nexus was already ran earlier, this will update the existing file to the latest version instead of re-creating Nexus
			Function()
			Nexus:Connect()
		end
	end)
	
	if Success then break else task.wait(1) end
end

if not Success and Error then
	(messagebox or print)(('Nexus encountered an error while launching!\n\n%s'):format(Error), 'Roblox Account Manager', 0)
end
_G.RoyxSpecialMode = "Hell Factory";
_G["External Config"] = {
    ["Kai Gems"] = true, -- true / false
    ["Kai Story"] = false, -- true / false
    ["Kai Battle Pass"] = false, -- true / false
    ["Kai Infinity Castle"] = false, -- true / false
    ["Auto Set Resource"] = true, -- true / false
    ["Select End Game Mode"] = "Auto Sell", -- "Instant Leave" / "Auto Sell"
    ["End Wave"] = 25, -- number
    ["Maximum Added Gems"] = 60000, -- number
    ["Close Roblox When Maximum Added Gems"] = false, -- true / false
    ["Using Limit Farming"] = false, -- true / false
    ["Stop Farming When The Limit Is Reached"] = false, -- true / false
    ["Send Webhook When The Limit Is Reached"] = true, -- true / false
    ["Webhook Url"] = "https://discord.com/api/webhooks/1062029974359523411/WjdR9INcmrXq2zWkWSR4QtAtKOwgepMVP-eCzWEHTyeukglWIjPOH3yE5AsDpmwoByBP", -- string
    ["RAM Port"] = "7963", -- string
    ["RAM Password"] = "", -- string
    ["RAM Private Server Url"] = "", -- string
    ["RAM Auto Description"] = true, -- true / false
    ["RAM Auto Private Server"] = false, -- true / false
    ["RAM Auto Exit"] = false, -- true / false
    ["Fps Limit"] = 15, -- number
    ["Lock Fps"] = true, -- true / false
    ["Release Fps When Rejoin"] = false, -- true / false
    ["Select Unit"] = {"Slot 1", "Slot 2", "Slot 3", "Slot 4", "Slot 5", "Slot 6"}, -- table  {"Slot 1", "Slot 2", "Slot 3", "Slot 4", "Slot 5", "Slot 6"}
};
local Key = _G.Key
local DiscordId = _G.DiscordId

queue_on_teleport(string.format([[
    _G.Key = "%s"
    _G.DiscordId = "%s"
    
    loadstring(game:HttpGet(" https://raw.githubusercontent.com/toohot123/acc/main/README.md"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/toohot123/robloxconfig/main/README.md"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Natsuhanaki/Royx_PC/main/loader.lua"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/toohot123/Roblox1/main/README.md"))()
]], Key, DiscordId))

-- loadstring(game:HttpGet("https://raw.githubusercontent.com/Natsuhanaki/Royx_PC/main/loader.lua"))()

print("Executed!");

