local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player.PlayerGui)
gui.Name = "REDzHUB"

-- Função para criar botões
local function criarBotao(nome, pos, acao)
    local botao = Instance.new("TextButton", gui)
    botao.Size = UDim2.new(0,250,0,35)
    botao.Position = UDim2.new(0,pos.X,0,pos.Y)
    botao.Text = nome
    botao.BackgroundColor3 = Color3.new(0.2,0.2,0.2)
    botao.TextColor3 = Color3.new(1,1,1)
    botao.MouseButton1Click:Connect(acao)
    return botao
end

-- Funções simples de exemplo
local function trollVersion()
    print("Troll Version ativada!")
end

local function resetarStats()
    player.Character.Humanoid.WalkSpeed = 16
    player.Character.Humanoid.JumpPower = 50
    workspace.Gravity = 196.2
end

local function spawnCasa()
    print("Casa spawnada!")
end

local function deletarCasa()
    print("Casa deletada!")
end

local function teleportCasa()
    print("Teleportado para sua casa!")
end

local function spawnCarro()
    print("Carro spawnado!")
end

local function destruirCarro()
    print("Carro destruído!")
end

local function congelarPlayer()
    print("Player congelado!")
end

local function trollarPlayer()
    print("Player trollado!")
end

-- Exemplo de botões principais
criarBotao("Troll Version (BETA)", Vector2.new(20,20), trollVersion)
criarBotao("Resetar Velocidade/Pulo/Gravidade", Vector2.new(20,60), resetarStats)
criarBotao("Spawn Casa", Vector2.new(20,100), spawnCasa)
criarBotao("Deletar Casa", Vector2.new(20,140), deletarCasa)
criarBotao("Teleport para Minha Casa", Vector2.new(20,180), teleportCasa)
criarBotao("Spawn Carro", Vector2.new(20,220), spawnCarro)
criarBotao("Destruir Carro", Vector2.new(20,260), destruirCarro)
criarBotao("Congelar Player", Vector2.new(20,300), congelarPlayer)
criarBotao("Trollar Player", Vector2.new(20,340), trollarPlayer)

-- Adicione mais botões e funções conforme o menu!

-- Créditos
local creditos = Instance.new("TextLabel", gui)
creditos.Size = UDim2.new(0,250,0,30)
creditos.Position = UDim2.new(0,20,0,380)
creditos.Text = "Créditos: redz9999"
creditos.BackgroundTransparency = 1
creditos.TextColor3 = Color3.new(1,1,0)
creditos.Font = Enum.Font.SourceSansBold
creditos.TextScaled = true
