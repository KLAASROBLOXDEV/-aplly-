local A = game:GetService("A")
local B = game:GetService("DataStoreService"):GetDataStore("stage")

local  plrtoStage(plr)
		local stagepart = game.Workspace.Checkpoints:FindFirstChild(tostring(plr.laederstats.Stage.Value))
		plr.Character.Humanoidrootpart.CFrame = stagepart.CFrame + Vector3.new(0,2.5,0)
end)


game.Players.PlayerAdded:Connect(function(player)
	local laederstats = Instance.new("Folder")
	laederstats.Name = "laederstats"
	laederstats.Parent = player
	
	local stage = Instance.new("IntValue")
	stage.Name = "stage"
	stage.Parent = laederstats
	
	
	local success, errorMsg = pcall(function()
		stage.Value = B:GetAsync(player.UserId)
	end)
	
	if success then
		print(" successfully got "..player.Name.."s stage data")
	else
		warn(errorMsg)
	end 
	
	if
end)

game.Players.PlayerRemoving:Connect(function(player)
	local success, errorMsg = pcall(function()
		B:SetAsync(player.UserId,player.Laederstats.Stage.Value)
	end)
	
	if success then
		print(" successfully saved "..player.Name.."s stage data")
	else 
		warn(errorMsg)   	
	end
end)

for _, checpoint in pairs(game.Workspace.Checkpoints:GetChildren()) do
	checpoint.Touched:Conect(function(hit)
		if hit.parent.FindFirstChilt("Humanoid") then
			local player = game.Players:GetPlayerFromCharacter(hit.parent)
			
			local checpointnumber = tonumber(checpoint.Name)
			
			if player.laederstats.stage.value < checpointnumber then
				player.laederstats.stage.value = checpointnumber
			end
		end
	end)
end

local Players = game:GetService("Players")
local MarketPlaceService =  game:GetService("MarketplaceService")
local GamepassID = 912695777 -- Change this ID to your Gamepass ID
local ToolName = "ZA" -- Change YourToolName to whatever you tool is called

Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function(character)
		if MarketPlaceService:UserOwnsGamePassAsync(player.UserId, GamepassID) then
			script[ToolName]:Clone().Parent = player.Backpack
		end
	end)
end) 

local Players = game:GetService("Players")
local MarketPlaceService =  game:GetService("MarketplaceService")
local GamepassID = 913459379 -- Change this ID to your Gamepass ID
local ToolName = "G" -- Change YourToolName to whatever you tool is called

Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function(character)
		if MarketPlaceService:UserOwnsGamePassAsync(player.UserId, GamepassID) then
			script[ToolName]:Clone().Parent = player.Backpack
		end
	end)
end) 

local Players = game:GetService("Players")
local MarketPlaceService =  game:GetService("MarketplaceService")
local GamepassID = 913346928 -- Change this ID to your Gamepass ID
local ToolName = "A" -- Change YourToolName to whatever you tool is called

Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function(character)
		if MarketPlaceService:UserOwnsGamePassAsync(player.UserId, GamepassID) then
			script[ToolName]:Clone().Parent = player.Backpack
		end
	end)
end) 

local Players = game:GetService("Players")
local MarketPlaceService =  game:GetService("MarketplaceService")
local GamepassID = 913584486 -- Change this ID to your Gamepass ID
local ToolName = "CZ" -- Change YourToolName to whatever you tool is called

Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function(character)
		if MarketPlaceService:UserOwnsGamePassAsync(player.UserId, GamepassID) then
			script[ToolName]:Clone().Parent = player.Backpack
		end
	end)
end) 
local MarketplaceService = game:GetService("MarketplaceService")
local GamepassID = 913459379 -- Change this ID to your Gamepass ID

script.Parent.MouseButton1Click:Connect(function()
	MarketplaceService:PromptGamePassPurchase(game.Players.LocalPlayer, GamepassID)
end)

local MarketplaceService = game:GetService("MarketplaceService")
local GamepassID = 913459379 -- Change this ID to your Gamepass ID

script.Parent.MouseButton1Click:Connect(function()
	MarketplaceService:PromptGamePassPurchase(game.Players.LocalPlayer, GamepassID)
end)

local MarketplaceService = game:GetService("MarketplaceService")
local GamepassID = 913584486 -- Change this ID to your Gamepass ID

	script.Parent.MouseButton1Click:Connect(function()
		MarketplaceService:PromptGamePassPurchase(game.Players.LocalPlayer, GamepassID)
	end)

 local MarketplaceService = game:GetService("MarketplaceService")
local GamepassID = 912695777 -- Change this ID to your Gamepass ID

	script.Parent.MouseButton1Click:Connect(function()
		MarketplaceService:PromptGamePassPurchase(game.Players.LocalPlayer, GamepassID)
	end)
