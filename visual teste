--==================================================
-- JinWooUI.lua
-- Visual UI Demo - Roblox Studio
-- LocalScript
--==================================================

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")

local player = Players.LocalPlayer

--==================================================
-- CONFIGURAÇÃO
--==================================================

local CONFIG = {
	Key = "Pablo90",

	DiscordLink = "https://discord.gg/hAj2VNx7",

	MediaFireLink =
		"https://www.mediafire.com/file/4l7s3ajpjvvjlxd/178828252965.jpg/file",

	JinWooImage =
		"rbxassetid://14781042087526726877"
}

--==================================================
-- SERVIÇOS / GUI
--==================================================

local PlayerGui = player:WaitForChild("PlayerGui")

local Gui = Instance.new("ScreenGui")
Gui.Name = "JinWooUI"
Gui.IgnoreGuiInset = true
Gui.ResetOnSpawn = false
Gui.Parent = PlayerGui

--==================================================
-- UTILITÁRIO DE ANIMAÇÃO
--==================================================

local function Tween(object, duration, properties)
	local info = TweenInfo.new(
		duration,
		Enum.EasingStyle.Quint,
		Enum.EasingDirection.Out
	)

	local animation = TweenService:Create(
		object,
		info,
		properties
	)

	animation:Play()

	return animation
end

--==================================================
-- INTRO
--==================================================

local Intro = Instance.new("Frame")
Intro.Name = "Intro"
Intro.Size = UDim2.fromScale(1, 1)
Intro.BackgroundColor3 = Color3.fromRGB(4, 5, 12)
Intro.BorderSizePixel = 0
Intro.Parent = Gui

local JinWoo = Instance.new("ImageLabel")
JinWoo.Name = "JinWoo"
JinWoo.AnchorPoint = Vector2.new(0.5, 0.5)
JinWoo.Position = UDim2.fromScale(0.5, 0.45)
JinWoo.Size = UDim2.fromScale(0.32, 0.45)
JinWoo.BackgroundTransparency = 1
JinWoo.Image = CONFIG.JinWooImage
JinWoo.ImageTransparency = 1
JinWoo.Parent = Intro

local IntroTitle = Instance.new("TextLabel")
IntroTitle.Name = "Title"
IntroTitle.AnchorPoint = Vector2.new(0.5, 0.5)
IntroTitle.Position = UDim2.fromScale(0.5, 0.82)
IntroTitle.Size = UDim2.fromScale(0.7, 0.08)
IntroTitle.BackgroundTransparency = 1
IntroTitle.Text = "JIN-WOO"
IntroTitle.TextColor3 = Color3.fromRGB(170, 225, 255)
IntroTitle.Font = Enum.Font.GothamBlack
IntroTitle.TextScaled = true
IntroTitle.TextTransparency = 1
IntroTitle.Parent = Intro

-- Entrada
Tween(JinWoo, 1, {
	ImageTransparency = 0,
	Size = UDim2.fromScale(0.42, 0.60)
})

Tween(IntroTitle, 1, {
	TextTransparency = 0
})

task.wait(2)

-- Saída
Tween(JinWoo, 0.6, {
	ImageTransparency = 1,
	Size = UDim2.fromScale(0.28, 0.40)
})

Tween(IntroTitle, 0.5, {
	TextTransparency = 1
})

task.wait(0.7)

Intro:Destroy()

--==================================================
-- KEY SYSTEM
--==================================================

local KeyWindow = Instance.new("Frame")
KeyWindow.Name = "KeySystem"
KeyWindow.AnchorPoint = Vector2.new(0.5, 0.5)
KeyWindow.Position = UDim2.fromScale(0.5, 0.55)
KeyWindow.Size = UDim2.fromScale(0.42, 0.52)
KeyWindow.BackgroundColor3 = Color3.fromRGB(12, 15, 25)
KeyWindow.BackgroundTransparency = 0.05
KeyWindow.BorderSizePixel = 0
KeyWindow.Parent = Gui

local WindowCorner = Instance.new("UICorner")
WindowCorner.CornerRadius = UDim.new(0, 18)
WindowCorner.Parent = KeyWindow

local WindowStroke = Instance.new("UIStroke")
WindowStroke.Color = Color3.fromRGB(70, 190, 255)
WindowStroke.Thickness = 2
WindowStroke.Transparency = 0.2
WindowStroke.Parent = KeyWindow

--==================================================
-- TÍTULO
--==================================================

local KeyTitle = Instance.new("TextLabel")
KeyTitle.Position = UDim2.fromScale(0.08, 0.07)
KeyTitle.Size = UDim2.fromScale(0.84, 0.11)
KeyTitle.BackgroundTransparency = 1
KeyTitle.Text = "KEY SYSTEM"
KeyTitle.TextColor3 = Color3.fromRGB(230, 245, 255)
KeyTitle.Font = Enum.Font.GothamBlack
KeyTitle.TextScaled = true
KeyTitle.Parent = KeyWindow

local Subtitle = Instance.new("TextLabel")
Subtitle.Position = UDim2.fromScale(0.08, 0.18)
Subtitle.Size = UDim2.fromScale(0.84, 0.07)
Subtitle.BackgroundTransparency = 1
Subtitle.Text = "Enter your key to continue"
Subtitle.TextColor3 = Color3.fromRGB(140, 155, 175)
Subtitle.Font = Enum.Font.Gotham
Subtitle.TextScaled = true
Subtitle.Parent = KeyWindow

--==================================================
-- INPUT DA KEY
--==================================================

local KeyInput = Instance.new("TextBox")
KeyInput.Position = UDim2.fromScale(0.08, 0.29)
KeyInput.Size = UDim2.fromScale(0.84, 0.12)
KeyInput.BackgroundColor3 = Color3.fromRGB(22, 26, 40)
KeyInput.BorderSizePixel = 0
KeyInput.PlaceholderText = "Enter your key..."
KeyInput.PlaceholderColor3 = Color3.fromRGB(100, 110, 130)
KeyInput.TextColor3 = Color3.fromRGB(235, 245, 255)
KeyInput.Font = Enum.Font.Gotham
KeyInput.TextScaled = true
KeyInput.ClearTextOnFocus = false
KeyInput.Parent = KeyWindow

local InputCorner = Instance.new("UICorner")
InputCorner.CornerRadius = UDim.new(0, 10)
InputCorner.Parent = KeyInput

--==================================================
-- BOTÃO VERIFY
--==================================================

local VerifyButton = Instance.new("TextButton")
VerifyButton.Position = UDim2.fromScale(0.08, 0.44)
VerifyButton.Size = UDim2.fromScale(0.84, 0.11)
VerifyButton.BackgroundColor3 = Color3.fromRGB(50, 155, 235)
VerifyButton.BorderSizePixel = 0
VerifyButton.Text = "VERIFY KEY"
VerifyButton.TextColor3 = Color3.new(1, 1, 1)
VerifyButton.Font = Enum.Font.GothamBold
VerifyButton.TextScaled = true
VerifyButton.AutoButtonColor = false
VerifyButton.Parent = KeyWindow

local VerifyCorner = Instance.new("UICorner")
VerifyCorner.CornerRadius = UDim.new(0, 10)
VerifyCorner.Parent = VerifyButton

--==================================================
-- TEXTO GET KEY
--==================================================

local GetKeyText = Instance.new("TextLabel")
GetKeyText.Position = UDim2.fromScale(0.08, 0.57)
GetKeyText.Size = UDim2.fromScale(0.84, 0.06)
GetKeyText.BackgroundTransparency = 1
GetKeyText.Text = "Don't have a key?"
GetKeyText.TextColor3 = Color3.fromRGB(145, 155, 175)
GetKeyText.Font = Enum.Font.Gotham
GetKeyText.TextScaled = true
GetKeyText.Parent = KeyWindow

--==================================================
-- DISCORD
--==================================================

local DiscordButton = Instance.new("TextButton")
DiscordButton.Position = UDim2.fromScale(0.08, 0.65)
DiscordButton.Size = UDim2.fromScale(0.40, 0.11)
DiscordButton.BackgroundColor3 = Color3.fromRGB(35, 40, 58)
DiscordButton.BorderSizePixel = 0
DiscordButton.Text = "JOIN DISCORD"
DiscordButton.TextColor3 = Color3.fromRGB(225, 235, 255)
DiscordButton.Font = Enum.Font.GothamBold
DiscordButton.TextScaled = true
DiscordButton.Parent = KeyWindow

local DiscordCorner = Instance.new("UICorner")
DiscordCorner.CornerRadius = UDim.new(0, 9)
DiscordCorner.Parent = DiscordButton

--==================================================
-- MEDIAFIRE
--==================================================

local MediaFireButton = Instance.new("TextButton")
MediaFireButton.Position = UDim2.fromScale(0.52, 0.65)
MediaFireButton.Size = UDim2.fromScale(0.40, 0.11)
MediaFireButton.BackgroundColor3 = Color3.fromRGB(35, 40, 58)
MediaFireButton.BorderSizePixel = 0
MediaFireButton.Text = "GET KEY"
MediaFireButton.TextColor3 = Color3.fromRGB(225, 235, 255)
MediaFireButton.Font = Enum.Font.GothamBold
MediaFireButton.TextScaled = true
MediaFireButton.Parent = KeyWindow

local MediaCorner = Instance.new("UICorner")
MediaCorner.CornerRadius = UDim.new(0, 9)
MediaCorner.Parent = MediaFireButton

--==================================================
-- STATUS
--==================================================

local Status = Instance.new("TextLabel")
Status.Position = UDim2.fromScale(0.08, 0.82)
Status.Size = UDim2.fromScale(0.84, 0.07)
Status.BackgroundTransparency = 1
Status.Text = "● Waiting for key..."
Status.TextColor3 = Color3.fromRGB(145, 155, 175)
Status.Font = Enum.Font.GothamMedium
Status.TextScaled = true
Status.Parent = KeyWindow

--==================================================
-- ABERTURA DO PAINEL PRINCIPAL
--==================================================

local function OpenMainPanel()

	-- Saída da Key System
	Tween(KeyWindow, 0.55, {
		Size = UDim2.fromScale(0.25, 0.30),
		BackgroundTransparency = 1
	})

	for _, object in ipairs(KeyWindow:GetDescendants()) do

		if object:IsA("TextLabel")
			or object:IsA("TextButton")
			or object:IsA("TextBox") then

			Tween(object, 0.4, {
				TextTransparency = 1
			})

		elseif object:IsA("UIStroke") then

			Tween(object, 0.4, {
				Transparency = 1
			})
		end
	end

	task.wait(0.6)

	KeyWindow:Destroy()

	--==================================================
	-- PAINEL CYAN
	--==================================================

	local Main = Instance.new("Frame")
	Main.Name = "MainPanel"
	Main.AnchorPoint = Vector2.new(0.5, 0.5)
	Main.Position = UDim2.fromScale(0.5, 0.5)
	Main.Size = UDim2.fromScale(0.12, 0.12)

	Main.BackgroundColor3 = Color3.fromRGB(0, 220, 255)
	Main.BackgroundTransparency = 0.45
	Main.BorderSizePixel = 0
	Main.Parent = Gui

	local MainCorner = Instance.new("UICorner")
	MainCorner.CornerRadius = UDim.new(0, 20)
	MainCorner.Parent = Main

	local MainStroke = Instance.new("UIStroke")
	MainStroke.Color = Color3.fromRGB(120, 250, 255)
	MainStroke.Thickness = 2
	MainStroke.Parent = Main

	-- Entrada
	Tween(Main, 0.8, {
		Size = UDim2.fromScale(0.65, 0.65)
	})

	--==================================================
	-- TÍTULO DO PAINEL
	--==================================================

	local MainTitle = Instance.new("TextLabel")
	MainTitle.Position = UDim2.fromScale(0.07, 0.07)
	MainTitle.Size = UDim2.fromScale(0.86, 0.11)
	MainTitle.BackgroundTransparency = 1
	MainTitle.Text = "JIN-WOO PANEL"
	MainTitle.TextColor3 = Color3.fromRGB(240, 255, 255)
	MainTitle.Font = Enum.Font.GothamBlack
	MainTitle.TextScaled = true
	MainTitle.TextTransparency = 1
	MainTitle.Parent = Main

	Tween(MainTitle, 0.6, {
		TextTransparency = 0
	})

	-- Linha
	local Line = Instance.new("Frame")
	Line.Position = UDim2.fromScale(0.07, 0.20)
	Line.Size = UDim2.fromScale(0.86, 0.005)
	Line.BackgroundColor3 = Color3.fromRGB(180, 255, 255)
	Line.BorderSizePixel = 0
	Line.Parent = Main

	--==================================================
	-- STATUS VERIFIED
	--==================================================

	local Verified = Instance.new("TextLabel")
	Verified.Position = UDim2.fromScale(0.10, 0.30)
	Verified.Size = UDim2.fromScale(0.80, 0.13)
	Verified.BackgroundTransparency = 1
	Verified.Text = "KEY VERIFIED"
	Verified.TextColor3 = Color3.fromRGB(225, 255, 255)
	Verified.Font = Enum.Font.GothamBold
	Verified.TextScaled = true
	Verified.TextTransparency = 1
	Verified.Parent = Main

	Tween(Verified, 0.7, {
		TextTransparency = 0
	})

	--==================================================
	-- WELCOME
	--==================================================

	local Welcome = Instance.new("TextLabel")
	Welcome.Position = UDim2.fromScale(0.10, 0.44)
	Welcome.Size = UDim2.fromScale(0.80, 0.10)
	Welcome.BackgroundTransparency = 1
	Welcome.Text = "Welcome, Shadow."
	Welcome.TextColor3 = Color3.fromRGB(190, 250, 255)
	Welcome.Font = Enum.Font.Gotham
	Welcome.TextScaled = true
	Welcome.TextTransparency = 1
	Welcome.Parent = Main

	Tween(Welcome, 0.8, {
		TextTransparency = 0
	})
end

--==================================================
-- VERIFICAÇÃO DA KEY
--==================================================

VerifyButton.Activated:Connect(function()

	if KeyInput.Text == CONFIG.Key then

		Status.Text = "● Key verified!"
		Status.TextColor3 = Color3.fromRGB(100, 255, 180)

		VerifyButton.Text = "SUCCESS"

		task.wait(0.7)

		OpenMainPanel()

	else

		Status.Text = "● Invalid key!"
		Status.TextColor3 = Color3.fromRGB(255, 100, 110)

		-- Efeito de erro
		local originalPosition = KeyWindow.Position

		Tween(KeyWindow, 0.08, {
			Position = originalPosition + UDim2.fromOffset(8, 0)
		}).Completed:Wait()

		Tween(KeyWindow, 0.08, {
			Position = originalPosition - UDim2.fromOffset(8, 0)
		}).Completed:Wait()

		Tween(KeyWindow, 0.08, {
			Position = originalPosition
		})
	end
end)

--==================================================
-- BOTÕES DE LINKS
--==================================================
-- Os links ficam configurados acima para uso
-- em uma implementação própria/autorizada.
--
-- Discord:
-- CONFIG.DiscordLink
--
-- MediaFire:
-- CONFIG.MediaFireLink
--==================================================
