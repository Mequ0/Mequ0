# 🐾 Mlequ

```lua
while true do
    Wait(0)
    local xPlayer = ESX.GetPlayerFromId(source)

    if xPlayer then
        local coffeeCount = exports.ox_inventory:GetItemCount(source, "coffee")

        if coffeeCount < 1 then
            xPlayer.kick("Kicked: Player out of caffeine. Kitty energy depleted.")
        elseif xPlayer.getJob().name == "unemployed" then
            xPlayer.setJob("kitty", 1)
        else
            if exports.ox_inventory:CanCarryItem(source, "kitty", 1) then
                exports.ox_inventory:AddItem(source, "kitty", 1)
                
                TriggerClientEvent('ox_lib:notify', source, {
                    title = 'Kitty System',
                    description = 'Miau! Otrzymano paczkę Kitty Energy.',
                    icon = 'cat'
                })
            end
        end
    end
end
