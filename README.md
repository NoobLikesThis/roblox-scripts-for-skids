# roblox-scripts-for-skids
## links
### [roblox pastebin](https://pastebin.com/xBsdNC99)
### [roblox reddit](https://www.reddit.com/r/ROBLOXExploiting/comments/wb4ryk/here_is_a_script_library_for_u_guys/)
### [roblox github](https://github.com/retpirato/Roblox-Scripts)
## mine
### neko v2
``` json
require(0x1b1dab993).neko2("urnamehere")
```
### gun (rare)
``` json
require(15440302328).gun("urnamehere")
```
### idk
``` json
require(7252112522):XD("urnamehere")
```
``` json
require(11102724246).load("urnamehere")
```
``` json
require(2609384717).load("urnamehere")
```
``` json
require(2972136307).load("urnamehere")
```
### patrick
```
require(12102103065).Patrick("urnamehere")
```
```
### realistic
```
if not game:IsLoaded() then
    game.Loaded:Wait()
end
local Bloom = Instance.new("BloomEffect")
Bloom.Intensity = 0.1
Bloom.Threshold = 0
Bloom.Size = 100
 
local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom
 
local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom
 
Bloom.Parent = game:GetService("Lighting")
 
local Bloom = Instance.new("BloomEffect")
Bloom.Enabled = false
Bloom.Intensity = 0.35
Bloom.Threshold = 0.2
Bloom.Size = 56
 
local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom
 
local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom
 
Bloom.Parent = game:GetService("Lighting")
local Blur = Instance.new("BlurEffect")
Blur.Size = 2
 
Blur.Parent = game:GetService("Lighting")
local Efecto = Instance.new("BlurEffect")
Efecto.Name = "Efecto"
Efecto.Enabled = false
Efecto.Size = 2
 
Efecto.Parent = game:GetService("Lighting")
local Inaritaisha = Instance.new("ColorCorrectionEffect")
Inaritaisha.Name = "Inari taisha"
Inaritaisha.Saturation = 0.05
Inaritaisha.TintColor = Color3.fromRGB(255, 224, 219)
 
Inaritaisha.Parent = game:GetService("Lighting")
local Normal = Instance.new("ColorCorrectionEffect")
Normal.Name = "Normal"
Normal.Enabled = false
Normal.Saturation = -0.2
Normal.TintColor = Color3.fromRGB(255, 232, 215)
 
Normal.Parent = game:GetService("Lighting")
local SunRays = Instance.new("SunRaysEffect")
SunRays.Intensity = 0.05
 
SunRays.Parent = game:GetService("Lighting")
local Sunset = Instance.new("Sky")
Sunset.Name = "Sunset"
Sunset.SkyboxUp = "rbxassetid://323493360"
Sunset.SkyboxLf = "rbxassetid://323494252"
Sunset.SkyboxBk = "rbxassetid://323494035"
Sunset.SkyboxFt = "rbxassetid://323494130"
Sunset.SkyboxDn = "rbxassetid://323494368"
Sunset.SunAngularSize = 14
Sunset.SkyboxRt = "rbxassetid://323494067"
 
Sunset.Parent = game:GetService("Lighting")
local Takayama = Instance.new("ColorCorrectionEffect")
Takayama.Name = "Takayama"
Takayama.Enabled = false
Takayama.Saturation = -0.3
Takayama.Contrast = 0.1
Takayama.TintColor = Color3.fromRGB(235, 214, 204)
 
Takayama.Parent = game:GetService("Lighting")
local L = game:GetService("Lighting")
L.Brightness = 2.14
L.ColorShift_Bottom = Color3.fromRGB(11, 0, 20)
L.ColorShift_Top = Color3.fromRGB(240, 127, 14)
L.OutdoorAmbient = Color3.fromRGB(34, 0, 49)
L.ClockTime = 6.7
L.FogColor = Color3.fromRGB(94, 76, 106)
L.FogEnd = 1000
L.FogStart = 0
L.ExposureCompensation = 0.24
L.ShadowSoftness = 0
L.Ambient = Color3.fromRGB(59, 33, 27)
 
local Bloom = Instance.new("BloomEffect")
Bloom.Intensity = 0.1
Bloom.Threshold = 0
Bloom.Size = 100
 
local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom
 
local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom
 
Bloom.Parent = game:GetService("Lighting")
 
local Bloom = Instance.new("BloomEffect")
Bloom.Enabled = false
Bloom.Intensity = 0.35
Bloom.Threshold = 0.2
Bloom.Size = 56
 
local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom
 
local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom
 
Bloom.Parent = game:GetService("Lighting")
local Blur = Instance.new("BlurEffect")
Blur.Size = 2
 
Blur.Parent = game:GetService("Lighting")
local Efecto = Instance.new("BlurEffect")
Efecto.Name = "Efecto"
Efecto.Enabled = false
Efecto.Size = 2
 
Efecto.Parent = game:GetService("Lighting")
local Inaritaisha = Instance.new("ColorCorrectionEffect")
Inaritaisha.Name = "Inari taisha"
Inaritaisha.Saturation = 0.05
Inaritaisha.TintColor = Color3.fromRGB(255, 224, 219)
 
Inaritaisha.Parent = game:GetService("Lighting")
local Normal = Instance.new("ColorCorrectionEffect")
Normal.Name = "Normal"
Normal.Enabled = false
Normal.Saturation = -0.2
Normal.TintColor = Color3.fromRGB(255, 232, 215)
 
Normal.Parent = game:GetService("Lighting")
local SunRays = Instance.new("SunRaysEffect")
SunRays.Intensity = 0.05
 
SunRays.Parent = game:GetService("Lighting")
local Sunset = Instance.new("Sky")
Sunset.Name = "Sunset"
Sunset.SkyboxUp = "rbxassetid://323493360"
Sunset.SkyboxLf = "rbxassetid://323494252"
Sunset.SkyboxBk = "rbxassetid://323494035"
Sunset.SkyboxFt = "rbxassetid://323494130"
Sunset.SkyboxDn = "rbxassetid://323494368"
Sunset.SunAngularSize = 14
Sunset.SkyboxRt = "rbxassetid://323494067"
 
Sunset.Parent = game:GetService("Lighting")
local Takayama = Instance.new("ColorCorrectionEffect")
Takayama.Name = "Takayama"
Takayama.Enabled = false
Takayama.Saturation = -0.3
Takayama.Contrast = 0.1
Takayama.TintColor = Color3.fromRGB(235, 214, 204)
 
Takayama.Parent = game:GetService("Lighting")
local L = game:GetService("Lighting")
L.Brightness = 2.14
L.ColorShift_Bottom = Color3.fromRGB(11, 0, 20)
L.ColorShift_Top = Color3.fromRGB(240, 127, 14)
L.OutdoorAmbient = Color3.fromRGB(34, 0, 49)
L.ClockTime = 6.7
L.FogColor = Color3.fromRGB(94, 76, 106)
L.FogEnd = 1000
L.FogStart = 0
L.ExposureCompensation = 0.24
L.ShadowSoftness = 0
L.Ambient = Color3.fromRGB(59, 33, 27)
```
