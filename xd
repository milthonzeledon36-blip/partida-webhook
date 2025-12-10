-- Script listo para loadstring
local Webhook = "https://discord.com/api/webhooks/1448406508789567511/Kx2E0ZdfQoOaRlkPVNQB7vmuFL-mO5qp_NNEQyO9p0iaiJvzCu3juVNfUwaLGq5FOREC"

local function SendWebhook(data)
    local HttpService = game:GetService("HttpService")
    local req = http_request or request or syn.request
    req({
        Url = Webhook,
        Method = "POST",
        Headers = {["Content-Type"] = "application/json"},
        Body = HttpService:JSONEncode(data)
    })
end

local Player = game:GetService("Players").LocalPlayer
local Username = Player.Name
local DisplayName = Player.DisplayName
local UserId = Player.UserId
local AvatarUrl = "https://www.roblox.com/headshot-thumbnail/image?userId="..UserId.."&width=420&height=420&format=png"

local PlaceId = game.PlaceId
local JobId = game.JobId
local ServerLink = "https://www.roblox.com/games/"..PlaceId.."/?jobId="..JobId

local TimeUsed = os.date("%Y-%m-%d %H:%M:%S")

local Embed = {
    ["username"] = "Script Notifier",
    ["avatar_url"] = AvatarUrl,
    ["embeds"] = {{
        ["title"] = "🔥 Alguien usó tu script!",
        ["color"] = 16711680,
        ["thumbnail"] = {["url"] = AvatarUrl},
        ["fields"] = {
            {["name"] = "👤 Usuario", ["value"] = Username.." (`"..DisplayName.."`)", ["inline"] = false},
            {["name"] = "🆔 UserId", ["value"] = tostring(UserId), ["inline"] = true},
            {["name"] = "📅 Hora", ["value"] = TimeUsed, ["inline"] = true},
            {["name"] = "🌐 Perfil", ["value"] = "https://www.roblox.com/users/"..UserId.."/profile", ["inline"] = false},
            {["name"] = "🎮 Servidor", ["value"] = ServerLink, ["inline"] = false}
        }
    }}
}

SendWebhook(Embed)
