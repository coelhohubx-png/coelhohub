repeat task.wait() until game:IsLoaded()

local PlaceIds = {
    -- BloxFruits (Mundos/Mares e servidores privados)
    [2753915549] = "Bloxfruits", 
    [4442272183] = "Bloxfruits", 
    [7449423635] = "Bloxfruits", 
    [79091703265657] = "Bloxfruits", 
    [996949360] = "Bloxfruits", 
    [100117331123089] = "Bloxfruits", 
    [994732206] = "Bloxfruits", 
    
    -- 99 Noites na Floresta
    [126509999114328] = "99 noites na floresta", 
}

local CurrentGame = PlaceIds[game.PlaceId] or "Desconhecido"

-- Sistema de detecção e execução
if CurrentGame == "Bloxfruits" then
    print("[Loader] Blox Fruits detectado! Iniciando script...")
    loadstring(game:HttpGet("https://api.luacrack.site/files/v4/loaders/8a34ade524aac301331777f2a70892fc.lua"))()

elseif CurrentGame == "99 noites na floresta" then
    print("[Loader] 99 Noites na Floresta detectado! Iniciando script...")
    loadstring(game:HttpGet("https://api.luacrack.site/files/v4/loaders/822fddb6c13b81f37135a78a002e1c3e.lua"))()

else
    warn("[Loader] Jogo com PlaceId " .. tostring(game.PlaceId) .. " não está mapeado.")
end
