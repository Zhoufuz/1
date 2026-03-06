local v_u_1 = game:GetService("Players")
local v2 = game:GetService("ReplicatedStorage")
local v_u_3 = game:GetService("StarterGui")
local v_u_4 = game:GetService("ProximityPromptService")
local v_u_5 = v_u_1.LocalPlayer
local v6 = v2:WaitForChild("AntiCheatRemotes")
local v7 = v6:WaitForChild("AC_Challenge")
local v_u_8 = v6:WaitForChild("AC_Heartbeat")
local v_u_9 = v6:WaitForChild("AC_Witness")
local v10 = v6:WaitForChild("AC_Notify")
local v_u_11 = {}
local v_u_12 = {}
local v_u_13 = 0
local v_u_14 = 0
local v_u_15 = 0
local v_u_16 = os.clock()
local v_u_17 = 3.5
local function v_u_22(p18, p19, p20)
    -- upvalues: (copy) v_u_3
    local v_u_21 = {
        ["Title"] = tostring(p18 or "ForeverAC"),
        ["Text"] = tostring(p19 or "Cheating detected"),
        ["Duration"] = tonumber(p20) or 3
    }
    for _ = 1, 10 do
        if pcall(function()
            -- upvalues: (ref) v_u_3, (copy) v_u_21
            v_u_3:SetCore("SendNotification", v_u_21)
        end) then
            return true
        end
        task.wait(0.2)
    end
    return false
end
v10.OnClientEvent:Connect(function(p23)
    -- upvalues: (copy) v_u_22
    if type(p23) == "table" then
        v_u_22(p23.title, p23.text, p23.duration)
    end
end)
local function v_u_31(p24, p25)
    local v26 = {}
    if type(p25) == "table" then
        for v27, v28 in pairs(p25) do
            if type(v27) == "string" and v28 == true then
                v26[v27] = true
            end
        end
    end
    if type(p24) ~= "table" then
        return v26
    end
    for v29, v30 in pairs(p24) do
        if type(v29) == "number" and (type(v30) == "string" and v30 ~= "") then
            v26[v30] = true
        elseif type(v29) == "string" then
            if v30 == true then
                v26[v29] = true
            elseif type(v30) == "string" and v30 ~= "" then
                v26[v30] = true
            end
        end
    end
    return v26
end
local function v_u_33(p32)
    -- upvalues: (copy) v_u_31
    return v_u_31(p32, {
        ["ProximityPrompts"] = true
    })
end
local function v_u_35(p34)
    -- upvalues: (copy) v_u_31
    return v_u_31(p34, {
        ["RobloxGui"] = true,
        ["ProximityPrompts"] = true,
        ["BubbleChat"] = true,
        ["VoiceChatSelfView"] = true
    })
end
local function v_u_42(p36, p37)
    -- upvalues: (copy) v_u_31
    local v38 = v_u_31(p36, p37)
    local v39 = {}
    for v40, v41 in pairs(v38) do
        if v41 == true then
            v39[string.lower((tostring(v40)))] = true
        end
    end
    return v39
end
local v_u_43 = v_u_33(nil)
local v_u_44 = v_u_35(nil)
local v_u_45 = v_u_42(nil, nil)
local v_u_46 = v_u_31(nil, {
    ["Players"] = true,
    ["Workspace"] = true
})
local v_u_47 = v_u_31(nil, nil)
local v_u_48 = v_u_31(nil, {
    ["Players"] = true,
    ["Workspace"] = true
})
local v_u_49 = v_u_31(nil, nil)
local function v_u_50()
    -- upvalues: (copy) v_u_16, (ref) v_u_17
    return os.clock() - v_u_16 < v_u_17
end
local v_u_51 = v_u_17
local v_u_52 = {}
local v_u_53 = 0
local v_u_54 = false
local v_u_55 = nil
local v_u_56 = ""
local v_u_57 = {}
local v_u_58 = true
local v_u_59 = {}
local v_u_60 = nil
local v_u_61 = 48
local v_u_62 = ""
local v_u_63 = 2
local v_u_64 = ""
local v_u_65 = ""
local function v_u_68()
    local v66, v67 = pcall(function()
        return game:GetService("CoreGui")
    end)
    if v66 and typeof(v67) == "Instance" then
        return v67
    else
        return nil
    end
end
local v_u_69 = false
local v_u_70 = {}
local v_u_71 = 0
local v_u_72 = nil
local v_u_73 = nil
local v_u_74 = 4
local v_u_75 = 0
local v_u_76 = false
local v_u_77 = ""
local v_u_78 = false
local v_u_79 = ""
local v_u_80 = ""
local v_u_81 = ""
local v_u_82 = ""
local v_u_83 = false
local v_u_84 = {}
local v_u_85 = false
local v_u_86 = ""
local v_u_87 = true
local v_u_88 = {}
local v_u_89 = ""
local v_u_90 = ""
local v_u_91 = ""
local v_u_92 = ""
local v_u_93 = ""
local v_u_94 = nil
local v_u_95 = nil
local v_u_96 = {}
local v_u_97 = false
local v_u_98 = ""
local v_u_99 = nil
local v_u_100 = 0
local v_u_101 = true
local v_u_102 = ""
local v_u_103 = {}
local v_u_104 = true
local v_u_105 = 3.5
local v_u_106 = 192
local v_u_107 = false
local v_u_108 = ""
local v_u_109 = nil
local v_u_110 = nil
local v_u_111 = 0
local v_u_112 = ""
local v_u_113 = ""
local v_u_114 = false
local v_u_115 = true
local v_u_116 = true
local v_u_117 = ""
local v_u_118 = nil
local v_u_119 = ""
local v_u_120 = nil
local v_u_121 = 0
local v_u_122 = ""
for _, v123 in ipairs(v_u_11) do
    local v124 = v123.path or ""
    local v125 = tostring(v124)
    local v126 = string.match(v125, "^[^/]+")
    if v126 and v126 ~= "" then
        if v_u_52[v126] ~= true then
            v_u_53 = v_u_53 + 1
        end
        v_u_52[v126] = true
    end
end
local function v_u_143(p127, p128, p129)
    local v130 = p127.CFrame:PointToObjectSpace(p128)
    local v131 = p127.Size * 0.5
    local v132 = math.max(0, p129 or 0)
    local v133 = v131.X - v132
    local v134 = math.max(0, v133)
    local v135 = v131.Y - v132
    local v136 = math.max(0, v135)
    local v137 = v131.Z - v132
    local v138 = math.max(0, v137)
    local v139 = v130.X
    local v140
    if math.abs(v139) <= v134 then
        local v141 = v130.Y
        if math.abs(v141) <= v136 then
            local v142 = v130.Z
            v140 = math.abs(v142) <= v138
        else
            v140 = false
        end
    else
        v140 = false
    end
    return v140
end
local function v_u_145(p144)
    if p144:IsA("Part") then
        return p144.Shape == Enum.PartType.Block
    elseif p144:IsA("MeshPart") then
        return p144.CollisionFidelity == Enum.CollisionFidelity.Box
    else
        return false
    end
end
local function v_u_149(p146)
    local v147 = 0
    for v148 = 1, #p146 do
        v147 = (v147 * 131 + string.byte(p146, v148)) % 2147483647
    end
    return tostring(v147)
end
local function v_u_151(p150)
    return p150 == true and "1" or "0"
end
local function v_u_155(p152)
    if type(p152) ~= "number" or (p152 ~= p152 or (p152 == math.huge or p152 == -math.huge)) then
        return "0"
    end
    local v153 = p152 * 1000 + 0.5
    local v154 = math.floor(v153)
    return tostring(v154)
end
local function v_u_158(p156)
    -- upvalues: (copy) v_u_155, (copy) v_u_151
    local v157 = type(p156)
    if v157 == "string" then
        return "s:" .. p156
    elseif v157 == "number" then
        return "n:" .. v_u_155(p156)
    elseif v157 == "boolean" then
        return "b:" .. v_u_151(p156)
    else
        return "u:" .. tostring(p156)
    end
end
local function v_u_169(p159, p160)
    -- upvalues: (copy) v_u_151, (copy) v_u_155, (copy) v_u_158, (copy) v_u_169
    local v161 = p160 or 0
    local v162 = type(p159)
    if v162 == "boolean" then
        return "b" .. v_u_151(p159)
    end
    if v162 == "number" then
        return "n" .. v_u_155(p159)
    end
    if v162 == "string" then
        return "s" .. p159
    end
    if p159 == nil then
        return "z"
    end
    if v162 ~= "table" then
        return "u" .. tostring(p159)
    end
    if v161 >= 3 then
        return "t{}"
    end
    local v163 = {}
    for v164 in pairs(p159) do
        v163[#v163 + 1] = {
            ["rawKey"] = v164,
            ["keyToken"] = v_u_158(v164)
        }
    end
    table.sort(v163, function(p165, p166)
        return p165.keyToken < p166.keyToken
    end)
    local v167 = {}
    for _, v168 in ipairs(v163) do
        v167[#v167 + 1] = v168.keyToken .. "=" .. v_u_169(p159[v168.rawKey], v161 + 1)
    end
    return "t{" .. table.concat(v167, ";") .. "}"
end
local function v_u_179(p170, p171)
    -- upvalues: (copy) v_u_169, (copy) v_u_149
    if type(p171) ~= "table" then
        return ""
    end
    local v172 = {}
    for v173 in pairs(p171) do
        local v174 = tostring(v173)
        if v174 ~= "integrity" then
            v172[#v172 + 1] = {
                ["rawKey"] = v173,
                ["keyText"] = v174
            }
        end
    end
    table.sort(v172, function(p175, p176)
        return p175.keyText < p176.keyText
    end)
    local v177 = { (tostring(p170 or "")) }
    for _, v178 in ipairs(v172) do
        v177[#v177 + 1] = v178.keyText .. ":" .. v_u_169(p171[v178.rawKey], 0)
    end
    return v_u_149(table.concat(v177, "|"))
end
local function v_u_182(p180, p181)
    -- upvalues: (copy) v_u_179
    return v_u_179("w|" .. tostring(p180 or ""), p181)
end
local function v_u_186(p183)
    local v184 = {}
    for v185 in string.gmatch(p183, "[^/]+") do
        v184[#v184 + 1] = v185
    end
    return v184
end
local function v_u_190(p187, p188)
    -- upvalues: (copy) v_u_186
    if type(p188) ~= "string" or p188 == "" then
        return nil
    end
    for _, v189 in ipairs(v_u_186(p188)) do
        if not p187 then
            return nil
        end
        p187 = p187:FindFirstChild(v189)
    end
    return p187
end
local function v_u_195(p191, p192)
    local v193 = {}
    while p192 and p192 ~= p191 do
        local v194 = p192.Name
        table.insert(v193, 1, v194)
        p192 = p192.Parent
    end
    return p192 ~= p191 and "" or table.concat(v193, "/")
end
local function v_u_200(p_u_196)
    if not p_u_196 then
        return ""
    end
    local v197, v198 = pcall(function()
        -- upvalues: (copy) p_u_196
        return p_u_196:GetFullName()
    end)
    if v197 then
        return tostring(v198)
    end
    local v199 = p_u_196.Name
    return tostring(v199)
end
local function v_u_202(p201)
    return string.lower((tostring(p201 or "")))
end
local function v_u_204(p203)
    -- upvalues: (ref) v_u_45, (copy) v_u_202, (copy) v_u_200
    if p203 and p203:IsA("ProximityPrompt") then
        return v_u_45[v_u_202(v_u_200(p203))] == true
    else
        return false
    end
end
local function v_u_207()
    -- upvalues: (copy) v_u_59, (ref) v_u_71
    for v205 in pairs(v_u_59) do
        if v205.Parent == nil then
            v_u_59[v205] = nil
        end
    end
    local v206 = 0
    for _ in pairs(v_u_59) do
        v206 = v206 + 1
    end
    v_u_71 = v206
end
local function v_u_211()
    -- upvalues: (ref) v_u_72, (ref) v_u_73, (copy) v_u_4, (copy) v_u_204, (copy) v_u_59, (ref) v_u_71
    if not (v_u_72 and v_u_73) then
        v_u_72 = v_u_4.PromptShown:Connect(function(p208)
            -- upvalues: (ref) v_u_204, (ref) v_u_59, (ref) v_u_71
            if v_u_204(p208) then
                if v_u_59[p208] ~= true then
                    v_u_59[p208] = true
                    v_u_71 = v_u_71 + 1
                end
            end
        end)
        v_u_73 = v_u_4.PromptHidden:Connect(function(p209)
            -- upvalues: (ref) v_u_59, (ref) v_u_71
            if v_u_59[p209] == true then
                v_u_59[p209] = nil
                local v210 = v_u_71 - 1
                v_u_71 = math.max(0, v210)
            end
        end)
    end
end
local function v_u_214(p212)
    if not p212 then
        return false
    end
    for _, v213 in ipairs(p212:GetDescendants()) do
        if v213:IsA("GuiObject") then
            return true
        end
    end
    return false
end
local function v_u_216(p215)
    while p215 and (p215.Parent and p215.Parent ~= game) do
        p215 = p215.Parent
    end
    if p215 and p215.Parent == game then
        return p215
    else
        return nil
    end
end
local function v_u_220(p217)
    -- upvalues: (copy) v_u_1
    if not p217 then
        return false
    end
    for _, v218 in ipairs(v_u_1:GetPlayers()) do
        local v219 = v218.Character
        if v219 and (p217 == v219 or p217:IsDescendantOf(v219)) then
            return true
        end
    end
    return false
end
local function v_u_228(p221)
    -- upvalues: (copy) v_u_1
    if type(p221) ~= "string" or p221 == "" then
        return false
    end
    local v222 = string.lower(p221)
    for _, v223 in ipairs(v_u_1:GetPlayers()) do
        local v224 = string.lower
        local v225 = v223.Name or ""
        if v224((tostring(v225))) == v222 then
            return true
        end
        local v226 = v223.DisplayName or ""
        local v227 = tostring(v226)
        if v227 ~= "" and string.lower(v227) == v222 then
            return true
        end
    end
    return false
end
local function v_u_232(p229)
    -- upvalues: (copy) v_u_228
    if not p229 then
        return false
    end
    while p229 do
        if p229:IsA("Model") then
            local v230 = v_u_228
            local v231 = p229.Name or ""
            if v230((tostring(v231))) then
                return true
            end
        end
        p229 = p229.Parent
    end
    return false
end
local function v_u_235(p233)
    if not p233 then
        return false
    end
    local v234 = p233:FindFirstAncestorOfClass("Model")
    return v234 and v234:FindFirstChildOfClass("Humanoid") and true or false
end
local function v_u_238(p236)
    -- upvalues: (copy) v_u_220, (copy) v_u_235, (copy) v_u_232, (ref) v_u_47, (copy) v_u_216, (ref) v_u_46
    if not (p236 and p236:IsA("BasePart")) then
        return true
    end
    if v_u_220(p236) or (v_u_235(p236) or v_u_232(p236)) then
        return true
    end
    if p236:GetAttribute("AC_AllowClientSpawn") == true then
        return true
    end
    if v_u_47[p236.ClassName] == true then
        return true
    end
    local v237 = v_u_216(p236)
    return v237 and v_u_46[v237.Name] == true and true or false
end
local function v_u_243(p239, p240, p241)
    -- upvalues: (copy) v_u_228, (copy) v_u_220, (copy) v_u_235, (copy) v_u_232, (ref) v_u_49, (copy) v_u_216, (ref) v_u_48
    if not p239 then
        return true
    end
    if p239:IsA("Player") then
        return true
    end
    if v_u_228(p240) or v_u_228(p241) then
        return true
    end
    if v_u_220(p239) or (v_u_235(p239) or v_u_232(p239)) then
        return true
    end
    if p239:GetAttribute("AC_AllowClientRename") == true then
        return true
    end
    if v_u_49[p239.ClassName] == true then
        return true
    end
    local v242 = v_u_216(p239)
    return v242 and v_u_48[v242.Name] == true and true or false
end
local function v_u_246(p244)
    -- upvalues: (copy) v_u_88, (copy) v_u_57
    local v245 = v_u_88[p244]
    if v245 then
        v245:Disconnect()
        v_u_88[p244] = nil
    end
    v_u_57[p244] = nil
end
local function v_u_252(p_u_247)
    -- upvalues: (copy) v_u_57, (copy) v_u_88, (ref) v_u_58, (copy) v_u_16, (ref) v_u_74, (copy) v_u_243, (ref) v_u_107, (ref) v_u_81, (copy) v_u_200, (ref) v_u_82, (ref) v_u_108, (ref) v_u_112
    if p_u_247 and v_u_57[p_u_247] == nil then
        v_u_57[p_u_247] = p_u_247.Name
        v_u_88[p_u_247] = p_u_247:GetPropertyChangedSignal("Name"):Connect(function()
            -- upvalues: (ref) v_u_57, (copy) p_u_247, (ref) v_u_58, (ref) v_u_16, (ref) v_u_74, (ref) v_u_243, (ref) v_u_107, (ref) v_u_81, (ref) v_u_200, (ref) v_u_82, (ref) v_u_108, (ref) v_u_112
            local v248 = v_u_57[p_u_247] or ""
            local v249 = tostring(v248)
            local v250 = p_u_247.Name or ""
            local v251 = tostring(v250)
            v_u_57[p_u_247] = v251
            if v_u_58 then
                if os.clock() - v_u_16 < v_u_74 then
                    return
                elseif v249 == v251 then
                    return
                elseif not v_u_243(p_u_247, v249, v251) then
                    v_u_107 = true
                    v_u_81 = v_u_200(p_u_247)
                    v_u_82 = p_u_247.ClassName
                    v_u_108 = v249
                    v_u_112 = v251
                end
            else
                return
            end
        end)
    end
end
local function v_u_257()
    -- upvalues: (ref) v_u_54, (copy) v_u_252, (ref) v_u_55, (ref) v_u_87, (copy) v_u_16, (ref) v_u_74, (copy) v_u_5, (copy) v_u_238, (ref) v_u_78, (ref) v_u_79, (copy) v_u_200, (ref) v_u_80, (ref) v_u_98, (ref) v_u_60, (copy) v_u_246
    if not v_u_54 then
        v_u_54 = true
        for _, v253 in ipairs(game:GetDescendants()) do
            v_u_252(v253)
        end
        v_u_55 = game.DescendantAdded:Connect(function(p254)
            -- upvalues: (ref) v_u_252, (ref) v_u_87, (ref) v_u_16, (ref) v_u_74, (ref) v_u_5, (ref) v_u_238, (ref) v_u_78, (ref) v_u_79, (ref) v_u_200, (ref) v_u_80, (ref) v_u_98
            v_u_252(p254)
            if v_u_87 then
                if os.clock() - v_u_16 < v_u_74 then
                    return
                elseif p254:IsA("BasePart") then
                    local v255 = v_u_5.Character
                    if v255 and p254:IsDescendantOf(v255) then
                        return
                    elseif not v_u_238(p254) then
                        v_u_78 = true
                        v_u_79 = v_u_200(p254)
                        v_u_80 = p254.ClassName
                        v_u_98 = v_u_200(p254.Parent)
                    end
                else
                    return
                end
            else
                return
            end
        end)
        v_u_60 = game.DescendantRemoving:Connect(function(p256)
            -- upvalues: (ref) v_u_246
            v_u_246(p256)
        end)
    end
end
local function v_u_258()
    -- upvalues: (copy) v_u_257, (ref) v_u_78
    v_u_257()
    return v_u_78
end
local function v_u_259()
    -- upvalues: (copy) v_u_257, (ref) v_u_107
    v_u_257()
    return v_u_107
end
local function v_u_262(p260, p261)
    while p261 and p261 ~= p260 do
        if p261:IsA("LayerCollector") then
            return p261
        end
        p261 = p261.Parent
    end
    return nil
end
local function v_u_264(p263)
    -- upvalues: (ref) v_u_45, (copy) v_u_211, (copy) v_u_207, (ref) v_u_71, (copy) v_u_214, (ref) v_u_43, (copy) v_u_52
    if not p263 then
        return true
    end
    if p263:GetAttribute("AC_AllowedGui") == true then
        return true
    end
    if p263.Name ~= "ProximityPrompts" then
        return v_u_43[p263.Name] == true and true or v_u_52[p263.Name] == true
    end
    if next(v_u_45) == nil then
        return true
    end
    v_u_211()
    v_u_207()
    return v_u_71 > 0 and true or not v_u_214(p263)
end
local function v_u_267(p265)
    -- upvalues: (ref) v_u_45, (copy) v_u_211, (copy) v_u_207, (ref) v_u_71, (copy) v_u_214, (ref) v_u_44
    if not p265 then
        return true
    end
    if p265:GetAttribute("AC_AllowedGui") == true then
        return true
    end
    if p265.Name ~= "ProximityPrompts" then
        if v_u_44[p265.Name] == true then
            return true
        end
        local v266 = p265.Name
        return string.sub(v266, 1, 6) == "Roblox"
    end
    if next(v_u_45) == nil then
        return true
    end
    v_u_211()
    v_u_207()
    return v_u_71 > 0 and true or not v_u_214(p265)
end
local function v_u_272(p_u_268)
    -- upvalues: (ref) v_u_109, (ref) v_u_110, (ref) v_u_111, (ref) v_u_83, (copy) v_u_84, (copy) v_u_262, (copy) v_u_264, (ref) v_u_85, (ref) v_u_86, (copy) v_u_195, (ref) v_u_64, (ref) v_u_65
    if v_u_109 then
        v_u_109:Disconnect()
        v_u_109 = nil
    end
    v_u_110 = p_u_268
    v_u_111 = os.clock()
    v_u_83 = false
    table.clear(v_u_84)
    for _, v269 in ipairs(p_u_268:GetDescendants()) do
        if v269:IsA("LayerCollector") then
            v_u_84[v269] = true
        end
    end
    v_u_109 = p_u_268.DescendantAdded:Connect(function(p270)
        -- upvalues: (ref) v_u_262, (copy) p_u_268, (ref) v_u_84, (ref) v_u_83, (ref) v_u_264, (ref) v_u_85, (ref) v_u_86, (ref) v_u_195, (ref) v_u_64, (ref) v_u_65
        local v271 = v_u_262(p_u_268, p270)
        if v271 then
            if v_u_84[v271] then
                return
            elseif v_u_83 then
                if v_u_264(v271) then
                    v_u_84[v271] = true
                else
                    v_u_85 = true
                    v_u_86 = v_u_195(p_u_268, v271)
                    v_u_64 = v271.ClassName
                    v_u_65 = "PlayerGui"
                end
            else
                v_u_84[v271] = true
                return
            end
        else
            return
        end
    end)
end
local function v_u_276()
    -- upvalues: (ref) v_u_99, (copy) v_u_68, (ref) v_u_100, (ref) v_u_69, (copy) v_u_70, (copy) v_u_267, (ref) v_u_85, (ref) v_u_86, (copy) v_u_200, (ref) v_u_64, (ref) v_u_65
    if v_u_99 then
        v_u_99:Disconnect()
        v_u_99 = nil
    end
    local v273 = v_u_68()
    if v273 then
        v_u_100 = os.clock()
        v_u_69 = false
        table.clear(v_u_70)
        for _, v274 in ipairs(v273:GetChildren()) do
            if v274:IsA("LayerCollector") then
                v_u_70[v274] = true
            end
        end
        v_u_99 = v273.ChildAdded:Connect(function(p275)
            -- upvalues: (ref) v_u_70, (ref) v_u_69, (ref) v_u_267, (ref) v_u_85, (ref) v_u_86, (ref) v_u_200, (ref) v_u_64, (ref) v_u_65
            if p275:IsA("LayerCollector") then
                if v_u_70[p275] then
                    return
                elseif v_u_69 then
                    if v_u_267(p275) then
                        v_u_70[p275] = true
                    else
                        v_u_85 = true
                        v_u_86 = v_u_200(p275)
                        v_u_64 = p275.ClassName
                        v_u_65 = "CoreGui"
                    end
                else
                    v_u_70[p275] = true
                    return
                end
            else
                return
            end
        end)
    end
end
local function v_u_286()
    -- upvalues: (ref) v_u_101, (copy) v_u_5, (copy) v_u_50, (ref) v_u_110, (copy) v_u_272, (ref) v_u_99, (copy) v_u_276, (ref) v_u_83, (copy) v_u_84, (ref) v_u_111, (ref) v_u_51, (copy) v_u_264, (ref) v_u_53, (ref) v_u_85, (ref) v_u_86, (copy) v_u_195, (ref) v_u_64, (ref) v_u_65, (copy) v_u_68, (ref) v_u_69, (copy) v_u_70, (ref) v_u_100, (copy) v_u_267, (copy) v_u_200
    if not v_u_101 then
        return false
    end
    local v277 = v_u_5:FindFirstChildOfClass("PlayerGui")
    if v_u_50() then
        if v277 and v277 ~= v_u_110 then
            v_u_272(v277)
        end
        if not v_u_99 then
            v_u_276()
        end
        return false
    end
    if v277 and v277 ~= v_u_110 then
        v_u_272(v277)
    end
    if v277 then
        if v_u_83 then
            for v278 in pairs(v_u_84) do
                if v278.Parent == nil or not v278:IsDescendantOf(v277) then
                    v_u_84[v278] = nil
                end
            end
            for _, v279 in ipairs(v277:GetDescendants()) do
                if v279:IsA("LayerCollector") then
                    local v280 = v_u_264(v279)
                    if v_u_53 > 0 and not v280 then
                        v_u_85 = true
                        v_u_86 = v_u_195(v277, v279)
                        v_u_64 = v279.ClassName
                        v_u_65 = "PlayerGui"
                        break
                    end
                    if not v_u_84[v279] then
                        if not v280 then
                            v_u_85 = true
                            v_u_86 = v_u_195(v277, v279)
                            v_u_64 = v279.ClassName
                            v_u_65 = "PlayerGui"
                            break
                        end
                        v_u_84[v279] = true
                    end
                end
            end
        else
            for _, v281 in ipairs(v277:GetDescendants()) do
                if v281:IsA("LayerCollector") then
                    v_u_84[v281] = true
                end
            end
            if v_u_51 <= os.clock() - v_u_111 then
                v_u_83 = true
            end
        end
    end
    local v282 = v_u_68()
    if not v282 then
        return v_u_85
    end
    if not v_u_99 then
        v_u_276()
    end
    if v_u_69 then
        for v283 in pairs(v_u_70) do
            if v283.Parent ~= v282 then
                v_u_70[v283] = nil
            end
        end
        for _, v284 in ipairs(v282:GetChildren()) do
            if v284:IsA("LayerCollector") and not v_u_70[v284] then
                if not v_u_267(v284) then
                    v_u_85 = true
                    v_u_86 = v_u_200(v284)
                    v_u_64 = v284.ClassName
                    v_u_65 = "CoreGui"
                    break
                end
                v_u_70[v284] = true
            end
        end
    else
        for _, v285 in ipairs(v282:GetChildren()) do
            if v285:IsA("LayerCollector") then
                v_u_70[v285] = true
            end
        end
        if v_u_51 <= os.clock() - v_u_100 then
            v_u_69 = true
        end
    end
    return v_u_85
end
local function v_u_290(p287)
    -- upvalues: (copy) v_u_5
    if not p287 then
        return true
    end
    if p287:GetAttribute("AC_AllowedHighlight") == true then
        return true
    end
    local v288 = v_u_5.Character
    local v289 = p287.Adornee
    return v288 and (v289 and v289:IsDescendantOf(v288)) and true or false
end
local function v_u_294()
    -- upvalues: (ref) v_u_94, (ref) v_u_95, (copy) v_u_96
    if not (v_u_94 and v_u_95) then
        for _, v291 in ipairs(game:GetDescendants()) do
            if v291:IsA("Highlight") then
                v_u_96[v291] = true
            end
        end
        v_u_94 = game.DescendantAdded:Connect(function(p292)
            -- upvalues: (ref) v_u_96
            if p292:IsA("Highlight") then
                v_u_96[p292] = true
            end
        end)
        v_u_95 = game.DescendantRemoving:Connect(function(p293)
            -- upvalues: (ref) v_u_96
            if p293:IsA("Highlight") then
                v_u_96[p293] = nil
            end
        end)
    end
end
local function v_u_296()
    -- upvalues: (copy) v_u_294, (copy) v_u_96, (copy) v_u_290, (ref) v_u_97, (ref) v_u_56, (copy) v_u_200, (ref) v_u_102
    v_u_294()
    for v295 in pairs(v_u_96) do
        if v295.Parent == nil then
            v_u_96[v295] = nil
        elseif not v_u_290(v295) then
            v_u_97 = true
            v_u_56 = v_u_200(v295)
            v_u_102 = v_u_200(v295.Parent)
            break
        end
    end
    return v_u_97
end
local function v_u_300(p297, p298)
    -- upvalues: (copy) v_u_103
    for _, v299 in ipairs(p297) do
        if v299 and (v299:IsA("BasePart") and (not v299:IsDescendantOf(p298) and (v299:GetAttribute("AC_IgnoreMaterialTamper") ~= true and v_u_103[v299] == nil))) then
            v_u_103[v299] = {
                ["material"] = v299.Material,
                ["variant"] = v299.MaterialVariant
            }
        end
    end
end
local function v_u_319()
    -- upvalues: (ref) v_u_104, (copy) v_u_16, (ref) v_u_105, (copy) v_u_5, (ref) v_u_75, (ref) v_u_76, (ref) v_u_106, (ref) v_u_61, (copy) v_u_300, (copy) v_u_103, (ref) v_u_77, (copy) v_u_200, (ref) v_u_89, (ref) v_u_90, (ref) v_u_91, (ref) v_u_62, (ref) v_u_63
    if not v_u_104 then
        return false
    end
    if os.clock() - v_u_16 < v_u_105 then
        return false
    end
    local v301 = v_u_5.Character
    if not v301 then
        local v302 = v_u_75 - 1
        v_u_75 = math.max(0, v302)
        return v_u_76
    end
    local v_u_303 = v301:FindFirstChild("HumanoidRootPart")
    if not (v_u_303 and v_u_303:IsA("BasePart")) then
        local v304 = v_u_75 - 1
        v_u_75 = math.max(0, v304)
        return v_u_76
    end
    local v_u_305 = OverlapParams.new()
    v_u_305.FilterType = Enum.RaycastFilterType.Exclude
    v_u_305.FilterDescendantsInstances = { v301 }
    v_u_305.RespectCanCollide = false
    local v306 = v_u_106
    v_u_305.MaxParts = math.max(16, v306)
    local v_u_307 = {}
    if not pcall(function()
        -- upvalues: (ref) v_u_307, (copy) v_u_303, (ref) v_u_61, (copy) v_u_305
        v_u_307 = workspace:GetPartBoundsInRadius(v_u_303.Position, v_u_61, v_u_305)
    end) then
        local v308 = v_u_61 * 2
        v_u_307 = workspace:GetPartBoundsInBox(v_u_303.CFrame, Vector3.new(v308, v308, v308), v_u_305)
    end
    v_u_300(v_u_307, v301)
    local v309 = false
    for _, v310 in ipairs(v_u_307) do
        if v310 and (v310:IsA("BasePart") and (not v310:IsDescendantOf(v301) and v310:GetAttribute("AC_IgnoreMaterialTamper") ~= true)) then
            local v311 = v_u_103[v310]
            if v311 and (v310.Material ~= v311.material or v310.MaterialVariant ~= v311.variant) then
                v309 = true
                v_u_77 = v_u_200(v310)
                local v312 = v311.material
                v_u_89 = tostring(v312)
                local v313 = v310.Material
                v_u_90 = tostring(v313)
                local v314 = v311.variant or ""
                v_u_91 = tostring(v314)
                local v315 = v310.MaterialVariant or ""
                v_u_62 = tostring(v315)
                break
            end
        end
    end
    for v316 in pairs(v_u_103) do
        if v316.Parent == nil then
            v_u_103[v316] = nil
        end
    end
    if v309 then
        v_u_75 = v_u_75 + 1
        local v317 = v_u_63
        if v_u_75 >= math.max(1, v317) then
            v_u_76 = true
        end
    else
        local v318 = v_u_75 - 1
        v_u_75 = math.max(0, v318)
    end
    return v_u_76
end
local function v_u_334()
    -- upvalues: (copy) v_u_5, (copy) v_u_149, (copy) v_u_11, (copy) v_u_190
    local v320 = v_u_5:FindFirstChildOfClass("PlayerGui")
    if not v320 then
        return v_u_149("")
    end
    local v321 = {}
    for _, v322 in ipairs(v_u_11) do
        local v323 = v322.path or ""
        local v324 = tostring(v323)
        local v325 = v322.className or ""
        local v326 = tostring(v325)
        local v327 = v322.requiredEnabled
        local v328
        if v327 == nil then
            v328 = "ANY"
        else
            local v329 = v327 == true
            v328 = tostring(v329)
        end
        local v330 = true
        local v331 = v_u_190(v320, v324)
        if v331 then
            if v326 ~= "" and v331.ClassName ~= v326 then
                v330 = false
            end
        else
            v330 = false
        end
        if v330 and v327 ~= nil then
            local v332 = v327 == true
            local v333 = true
            if v331:IsA("LayerCollector") then
                v333 = v331.Enabled
            elseif v331:IsA("GuiObject") then
                v333 = v331.Visible
            end
            v330 = v333 == v332
        end
        v321[#v321 + 1] = string.format("%s|%s|%s|%s", v324, v326, v328, v330 and "OK" or "BAD")
    end
    table.sort(v321)
    return v_u_149(table.concat(v321, "\n"))
end
local function v_u_346()
    local v_u_335 = {}
    local v_u_336 = {}
    local function v338(p337)
        -- upvalues: (copy) v_u_336, (copy) v_u_335
        if type(p337) == "table" and not v_u_336[p337] then
            v_u_336[p337] = true
            v_u_335[#v_u_335 + 1] = p337
        end
    end
    v338(_G)
    local v339, v340 = pcall(function()
        return getfenv()
    end)
    if v339 and type(v340) == "table" then
        v338(v340)
    end
    local v341 = _G
    v338((rawget(v341, "shared")))
    local v342 = _G
    local v343 = rawget(v342, "getgenv")
    if type(v343) == "function" then
        local v344, v345 = pcall(v343)
        if v344 and type(v345) == "table" then
            v338(v345)
        end
    end
    return v_u_335
end
local function v_u_351(p347, p348)
    for _, v349 in ipairs(p347) do
        for _, v350 in ipairs(p348) do
            if rawget(v349, v350) ~= nil then
                return v350
            end
        end
    end
    return nil
end
local function v_u_355(p_u_352)
    if type(p_u_352) ~= "function" then
        return ""
    end
    local v353, v354 = pcall(function()
        -- upvalues: (copy) p_u_352
        return debug.info(p_u_352, "s")
    end)
    return (not v353 or type(v354) ~= "string") and "" or v354
end
local function v_u_365(p356)
    -- upvalues: (copy) v_u_355
    local v357 = nil
    for _, v358 in ipairs(p356) do
        local v359 = rawget(v358, "getrawmetatable")
        if type(v359) == "function" then
            v357 = v359
            break
        end
    end
    if not v357 then
        return false, ""
    end
    local v360, v361 = pcall(v357, game)
    if not v360 or type(v361) ~= "table" then
        return true, "getrawmetatable_failed"
    end
    for _, v362 in ipairs({ "__namecall", "__index", "__newindex" }) do
        local v363 = rawget(v361, v362)
        if type(v363) == "function" then
            local v364 = v_u_355(v363)
            if v364 ~= "" and v364 ~= "[C]" then
                return true, v362 .. ":" .. v364
            end
        end
    end
    return false, ""
end
local function v_u_370()
    -- upvalues: (copy) v_u_346, (copy) v_u_351, (ref) v_u_92, (copy) v_u_365
    local v366 = v_u_346()
    local v367 = v_u_351(v366, {
        "getgenv",
        "hookfunction",
        "hookmetamethod",
        "newcclosure",
        "getrawmetatable",
        "setreadonly",
        "checkcaller",
        "cloneref",
        "identifyexecutor",
        "getexecutorname",
        "is_synapse_function",
        "syn"
    })
    if v367 then
        v_u_92 = "global:" .. v367
        return true
    else
        local v368, v369 = v_u_365(v366)
        if v368 then
            v_u_92 = "metamethod:" .. tostring(v369)
            return true
        else
            v_u_92 = ""
            return false
        end
    end
end
local function v_u_375(p371)
    local v372 = table.create(#p371)
    for v373, v374 in ipairs(p371) do
        v372[v373] = string.char(v374)
    end
    return table.concat(v372)
end
local v_u_376 = {
    {
        103,
        101,
        116,
        103,
        99
    },
    {
        104,
        111,
        111,
        107,
        102,
        117,
        110,
        99,
        116,
        105,
        111,
        110
    },
    {
        104,
        111,
        111,
        107,
        109,
        101,
        116,
        97,
        109,
        101,
        116,
        104,
        111,
        100
    },
    {
        110,
        101,
        119,
        99,
        99,
        108,
        111,
        115,
        117,
        114,
        101
    },
    {
        103,
        101,
        116,
        114,
        97,
        119,
        109,
        101,
        116,
        97,
        116,
        97,
        98,
        108,
        101
    },
    {
        115,
        101,
        116,
        114,
        101,
        97,
        100,
        111,
        110,
        108,
        121
    },
    {
        99,
        104,
        101,
        99,
        107,
        99,
        97,
        108,
        108,
        101,
        114
    },
    {
        99,
        108,
        111,
        110,
        101,
        114,
        101,
        102
    },
    {
        105,
        100,
        101,
        110,
        116,
        105,
        102,
        121,
        101,
        120,
        101,
        99,
        117,
        116,
        111,
        114
    },
    {
        103,
        101,
        116,
        101,
        120,
        101,
        99,
        117,
        116,
        111,
        114,
        110,
        97,
        109,
        101
    },
    {
        103,
        101,
        116,
        99,
        111,
        110,
        110,
        101,
        99,
        116,
        105,
        111,
        110,
        115
    },
    {
        103,
        101,
        116,
        103,
        101,
        110,
        118
    }
}
local function v_u_385()
    -- upvalues: (copy) v_u_346, (copy) v_u_376, (copy) v_u_375, (ref) v_u_93
    local v377 = v_u_346()
    for _, v378 in ipairs(v_u_376) do
        local v379 = v_u_375(v378)
        for _, v380 in ipairs(v377) do
            if rawget(v380, v379) ~= nil then
                v_u_93 = v379
                return true
            end
        end
    end
    for _, v381 in ipairs(v377) do
        local v382 = rawget(v381, "debug")
        if type(v382) == "table" then
            for _, v383 in ipairs({
                {
                    103,
                    101,
                    116,
                    99,
                    111,
                    110,
                    115,
                    116,
                    97,
                    110,
                    116,
                    115
                },
                {
                    103,
                    101,
                    116,
                    117,
                    112,
                    118,
                    97,
                    108,
                    117,
                    101,
                    115
                },
                {
                    115,
                    101,
                    116,
                    117,
                    112,
                    118,
                    97,
                    108,
                    117,
                    101
                }
            }) do
                local v384 = v_u_375(v383)
                if rawget(v382, v384) ~= nil then
                    v_u_93 = "debug." .. v384
                    return true
                end
            end
        end
    end
    v_u_93 = ""
    return false
end
local function v_u_388()
    -- upvalues: (copy) v_u_5
    local v386 = v_u_5.Character
    if v386 then
        local v387 = v386:FindFirstChildOfClass("Humanoid")
        if v387 then
            if v387.WalkSpeed > 32 then
                return true
            elseif v387.UseJumpPower then
                return v387.JumpPower > 100
            else
                return v387.JumpHeight > 12
            end
        else
            return false
        end
    else
        return false
    end
end
local function v_u_391(p389)
    -- upvalues: (copy) v_u_12, (ref) v_u_13, (ref) v_u_14, (ref) v_u_15
    table.clear(v_u_12)
    v_u_13 = 0
    v_u_14 = 0
    v_u_15 = os.clock()
    if p389 then
        for _, v390 in ipairs(p389:GetDescendants()) do
            if v390:IsA("BasePart") then
                v_u_12[v390] = v390.CanCollide
            end
        end
    end
end
local function v_u_401()
    -- upvalues: (copy) v_u_5, (ref) v_u_15, (copy) v_u_12, (copy) v_u_391, (ref) v_u_13
    local v392 = v_u_5.Character
    if not v392 then
        return false
    end
    if os.clock() - v_u_15 < 3 then
        return false
    end
    if next(v_u_12) == nil then
        v_u_391(v392)
    end
    local v393 = 0
    local v394 = 0
    for v395, v396 in pairs(v_u_12) do
        if v395.Parent == nil then
            v_u_12[v395] = nil
        elseif v396 == true then
            v393 = v393 + 1
            if v395.CanCollide == false then
                v394 = v394 + 1
            end
        end
    end
    for _, v397 in ipairs(v392:GetDescendants()) do
        if v397:IsA("BasePart") and v_u_12[v397] == nil then
            v_u_12[v397] = v397.CanCollide
        end
    end
    if v393 <= 0 then
        return false
    end
    local v398 = v393 * 0.55 + 0.5
    local v399 = math.floor(v398)
    if math.max(4, v399) <= v394 then
        v_u_13 = v_u_13 + 1
    else
        local v400 = v_u_13 - 1
        v_u_13 = math.max(0, v400)
    end
    return v_u_13 >= 2
end
local function v_u_422()
    -- upvalues: (copy) v_u_5, (ref) v_u_15, (ref) v_u_14, (copy) v_u_145, (copy) v_u_143
    local v402 = v_u_5.Character
    if not v402 then
        return false
    end
    if os.clock() - v_u_15 < 3 then
        return false
    end
    local v403 = v402:FindFirstChild("HumanoidRootPart")
    if not (v403 and v403:IsA("BasePart")) then
        return false
    end
    local v404 = v402:FindFirstChildOfClass("Humanoid")
    if not v404 or v404.Health <= 0 then
        return false
    end
    local v405 = v404:GetState()
    if v405 == Enum.HumanoidStateType.Climbing or (v405 == Enum.HumanoidStateType.Swimming or v405 == Enum.HumanoidStateType.Seated) then
        local v406 = v_u_14 - 1
        v_u_14 = math.max(0, v406)
        return false
    end
    local v407 = v403.AssemblyLinearVelocity.X
    local v408 = v403.AssemblyLinearVelocity.Z
    if Vector3.new(v407, 0, v408).Magnitude < 10 or v404.MoveDirection.Magnitude < 0.35 then
        local v409 = v_u_14 - 1
        v_u_14 = math.max(0, v409)
        return false
    end
    local v410 = OverlapParams.new()
    v410.FilterType = Enum.RaycastFilterType.Exclude
    v410.FilterDescendantsInstances = { v402 }
    v410.RespectCanCollide = true
    local v411 = v403.Size.X * 0.7
    local v412 = v403.Size.Y * 0.8
    local v413 = v403.Size.Z * 0.7
    local v414 = Vector3.new(v411, v412, v413)
    local v415 = workspace:GetPartBoundsInBox(v403.CFrame, v414, v410)
    local v416 = false
    for _, v417 in ipairs(v415) do
        if v417 and (v417:IsA("BasePart") and (v417.CanCollide and (not v417:IsDescendantOf(v402) and v_u_145(v417)))) then
            local v418 = v417:GetClosestPointOnSurface(v403.Position)
            local v419 = v403.Position - v418
            if v419.Magnitude > 0 then
                local v420 = v419.Unit.Y
                if math.abs(v420) <= 0.45 then
                    goto l26
                end
            else
                ::l26::
                if v_u_143(v417, v403.Position, 0.2) then
                    v416 = true
                    break
                end
            end
        end
    end
    if v416 then
        v_u_14 = v_u_14 + 1
    else
        local v421 = v_u_14 - 1
        v_u_14 = math.max(0, v421)
    end
    return v_u_14 >= 2
end
local function v_u_424()
    -- upvalues: (copy) v_u_5
    if script.Parent == nil then
        return true
    end
    local v423 = v_u_5:FindFirstChild("PlayerScripts")
    return not v423 and true or not script:IsDescendantOf(v423)
end
local v_u_425 = nil
v_u_5.CharacterAdded:Connect(function(p426)
    -- upvalues: (copy) v_u_391
    v_u_391(p426)
end)
if v_u_5.Character then
    v_u_391(v_u_5.Character)
end
v_u_257()
v7.OnClientEvent:Connect(function(p427)
    -- upvalues: (ref) v_u_51, (ref) v_u_43, (copy) v_u_33, (ref) v_u_44, (copy) v_u_35, (ref) v_u_45, (copy) v_u_42, (copy) v_u_59, (ref) v_u_71, (ref) v_u_101, (ref) v_u_104, (ref) v_u_105, (ref) v_u_61, (ref) v_u_106, (ref) v_u_63, (ref) v_u_115, (ref) v_u_116, (ref) v_u_122, (ref) v_u_87, (ref) v_u_58, (ref) v_u_74, (ref) v_u_46, (copy) v_u_31, (ref) v_u_47, (ref) v_u_48, (ref) v_u_49, (ref) v_u_113, (ref) v_u_114, (ref) v_u_119, (ref) v_u_120, (ref) v_u_117, (ref) v_u_118, (ref) v_u_425
    if type(p427) == "table" then
        local v428 = p427.nonce
        if type(v428) == "string" then
            local v429 = p427.joinGuiGraceSec
            local v430 = tonumber(v429)
            if v430 and v430 >= 0 then
                v_u_51 = v430
            else
                v_u_51 = 3.5
            end
            v_u_43 = v_u_33(p427.ignoredGuiRootNames)
            v_u_44 = v_u_35(p427.ignoredCoreGuiRootNames)
            v_u_45 = v_u_42(p427.allowedProximityPromptPaths, nil)
            table.clear(v_u_59)
            v_u_71 = 0
            v_u_101 = p427.enableUnauthorizedGuiDetection ~= false
            v_u_104 = p427.enableMaterialTamperDetection ~= false
            local v431 = p427.materialTamperGraceSec
            local v432 = tonumber(v431)
            if v432 and v432 >= 0 then
                v_u_105 = v432
            else
                v_u_105 = 3.5
            end
            local v433 = p427.materialTamperSampleRadiusStuds
            local v434 = tonumber(v433)
            if v434 and v434 > 0 then
                v_u_61 = v434
            else
                v_u_61 = 48
            end
            local v435 = p427.materialTamperMaxParts
            local v436 = tonumber(v435)
            if v436 and v436 >= 16 then
                v_u_106 = v436
            else
                v_u_106 = 192
            end
            local v437 = p427.materialTamperStrikeLimit
            local v438 = tonumber(v437)
            if v438 and v438 >= 1 then
                v_u_63 = v438
            else
                v_u_63 = 2
            end
            v_u_115 = p427.requireClientBeatSeq ~= false
            v_u_116 = p427.payloadIntegrityEnabled ~= false
            local v439 = p427.integritySeed or ""
            v_u_122 = tostring(v439)
            v_u_87 = p427.enableClientPartCreateDetection ~= false
            v_u_58 = p427.enableClientRenameDetection ~= false
            local v440 = p427.clientObjectTamperGraceSec
            local v441 = tonumber(v440)
            if v441 and v441 >= 0 then
                v_u_74 = v441
            else
                v_u_74 = 4
            end
            v_u_46 = v_u_31(p427.clientPartCreateIgnoredRootNames, nil)
            v_u_47 = v_u_31(p427.clientPartCreateIgnoredClassNames, nil)
            v_u_48 = v_u_31(p427.clientRenameIgnoredRootNames, nil)
            v_u_49 = v_u_31(p427.clientRenameIgnoredClassNames, nil)
            v_u_113 = p427.canaryFlagKey
            if v_u_113 == nil then
                v_u_113 = ""
            end
            v_u_114 = p427.canaryFlagValue == true
            v_u_119 = p427.canaryMetaKey
            if v_u_119 == nil then
                v_u_119 = ""
            end
            v_u_120 = p427.canaryMetaValue
            v_u_117 = p427.canaryTopKey
            if v_u_117 == nil then
                v_u_117 = ""
            end
            v_u_118 = p427.canaryTopValue
            v_u_425 = p427
        end
    else
        return
    end
end)
task.spawn(function()
    -- upvalues: (ref) v_u_425, (copy) v_u_424, (copy) v_u_286, (copy) v_u_296, (copy) v_u_319, (copy) v_u_385, (ref) v_u_121, (ref) v_u_115, (copy) v_u_334, (copy) v_u_370, (copy) v_u_388, (copy) v_u_401, (copy) v_u_422, (copy) v_u_258, (copy) v_u_259, (ref) v_u_86, (ref) v_u_64, (ref) v_u_65, (ref) v_u_56, (ref) v_u_102, (ref) v_u_77, (ref) v_u_89, (ref) v_u_90, (ref) v_u_91, (ref) v_u_62, (ref) v_u_75, (ref) v_u_93, (ref) v_u_92, (ref) v_u_79, (ref) v_u_80, (ref) v_u_98, (ref) v_u_81, (ref) v_u_82, (ref) v_u_108, (ref) v_u_112, (ref) v_u_113, (ref) v_u_114, (ref) v_u_119, (ref) v_u_120, (ref) v_u_117, (ref) v_u_118, (ref) v_u_116, (copy) v_u_179, (ref) v_u_122, (copy) v_u_9, (copy) v_u_182, (copy) v_u_8
    while true do
        repeat
            task.wait(2)
        until v_u_425
        local v442 = v_u_424()
        local v443 = v_u_425.expectedGuiManifestVersion ~= "v1" and true or v442
        local v444 = v_u_286()
        local v445 = v_u_296()
        local v446 = v_u_319()
        local v447 = v_u_385()
        v_u_121 = v_u_121 + 1
        local v448 = {
            ["nonce"] = v_u_425.nonce,
            ["clientTime"] = os.clock(),
            ["clientBeatSeq"] = v_u_115 and v_u_121 or 0,
            ["guiHash"] = v_u_334(),
            ["watchdogAlive"] = true,
            ["localFlags"] = {
                ["scriptTamper"] = v443,
                ["hookSuspicion"] = v_u_370(),
                ["executorApiSuspicion"] = v447,
                ["propertyDrift"] = v_u_388(),
                ["collisionTamper"] = v_u_401() or v_u_422(),
                ["unauthorizedGui"] = v444,
                ["highlightEsp"] = v445,
                ["materialTamper"] = v446,
                ["clientPartCreateTamper"] = v_u_258(),
                ["clientRenameTamper"] = v_u_259()
            },
            ["localMeta"] = {
                ["unauthorizedGuiPath"] = v_u_86,
                ["unauthorizedGuiClass"] = v_u_64,
                ["unauthorizedGuiSource"] = v_u_65,
                ["highlightPath"] = v_u_56,
                ["highlightParentPath"] = v_u_102,
                ["materialPartPath"] = v_u_77,
                ["materialExpected"] = v_u_89,
                ["materialGot"] = v_u_90,
                ["materialVariantExpected"] = v_u_91,
                ["materialVariantGot"] = v_u_62,
                ["materialStrikeCount"] = v_u_75,
                ["executorApiKey"] = v_u_93,
                ["hookMetaSignal"] = v_u_92,
                ["clientPartCreatePath"] = v_u_79,
                ["clientPartCreateClass"] = v_u_80,
                ["clientPartCreateParentPath"] = v_u_98,
                ["clientRenamePath"] = v_u_81,
                ["clientRenameClass"] = v_u_82,
                ["clientRenameOldName"] = v_u_108,
                ["clientRenameNewName"] = v_u_112
            }
        }
        if v_u_113 ~= "" then
            v448.localFlags[v_u_113] = v_u_114
        end
        if v_u_119 ~= "" then
            v448.localMeta[v_u_119] = v_u_120
        end
        if v_u_117 ~= "" then
            v448[v_u_117] = v_u_118
        end
        if v_u_116 then
            v448.integrity = v_u_179(v_u_122, v448)
        else
            v448.integrity = ""
        end
        v_u_9:FireServer({
            ["nonce"] = v_u_425.nonce,
            ["clientBeatSeq"] = v448.clientBeatSeq,
            ["witnessSig"] = v_u_182(v_u_122, v448)
        })
        v_u_8:FireServer(v448)
    end
end)
