local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/jensonhirst/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "SpamCar"
})
Tab:AddButton({
	Name = "Button!",
	Callback = function()
      		while true do
    local remote = game:GetService("ReplicatedStorage"):FindFirstChild("RE"):FindFirstChild("1Ca1r")
    if remote then
        local carList = {
            "Easter2025SolidMonsterTruck",
            "Easter2025EasterEggMotorcycle",
            "Easter2025SolidEggMotorcycle"
        }
        for _, car in ipairs(carList) do
            remote:FireServer("PickingCar", car)
            task.wait(0.1)
        end
    end
    task.wait(0.3)
end
  	end    
})

