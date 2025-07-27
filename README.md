local eggsFolder = game:GetService("Workspace"):FindFirstChild("Eggs") or game.Workspace

for _, egg in pairs(eggsFolder:GetDescendants()) do
    if egg:IsA("Model") and egg:FindFirstChild("Contents") then
        local content = egg.Contents
        print("Egg: " .. egg.Name)
        for _, item in pairs(content:GetChildren()) do
            print("  -> Berisi: " .. item.Name)
        end
    end
end
