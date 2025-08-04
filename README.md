local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local button = script.Parent -- o botão no GUI

-- Velocidade inicial padrão
local currentSpeed = humanoid.WalkSpeed

-- Função ao clicar no botão
button.MouseButton1Click:Connect(function()
	currentSpeed = currentSpeed + 2
	humanoid.WalkSpeed = currentSpeed
	print("Nova velocidade: " .. currentSpeed)
end)
