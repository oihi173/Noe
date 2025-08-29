-- Coloque isso dentro de um LocalScript em StarterGui

-- Criando a GUI
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "PainelPersonalizado"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Frame principal (painel)
local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0, 300, 0, 200)
Frame.Position = UDim2.new(0.3, 0, 0.3, 0)
Frame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
Frame.Active = true
Frame.Draggable = true -- permite mover o painel
Frame.Visible = true
Frame.Parent = ScreenGui

-- Imagem de capa
local Capa = Instance.new("ImageLabel")
Capa.Size = UDim2.new(1, 0, 0, 100)
Capa.Position = UDim2.new(0, 0, 0, 0)
Capa.BackgroundTransparency = 1
Capa.Image = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-vCHUr-Tfb6m8HXq5hX7MqyFvYsfNlMIXHpQZG2lfpal4h9UPEadhNAi2&s=10"
Capa.Parent = Frame

-- Botão de abrir/fechar
local ToggleButton = Instance.new("TextButton")
ToggleButton.Size = UDim2.new(0, 100, 0, 30)
ToggleButton.Position = UDim2.new(0.5, -50, 1, -35)
ToggleButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
ToggleButton.Text = "Abrir/Fechar"
ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ToggleButton.Parent = Frame

-- Script de abrir/fechar
local aberto = true
ToggleButton.MouseButton1Click:Connect(function()
	if aberto then
		Frame:TweenSize(UDim2.new(0, 300, 0, 35), "Out", "Quad", 0.3, true)
		aberto = false
	else
		Frame:TweenSize(UDim2.new(0, 300, 0, 200), "Out", "Quad", 0.3, true)
		aberto = true
	end
end)
