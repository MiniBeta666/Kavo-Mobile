# Loadstring
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/MiniBeta666/Kavo-Mobile/main/KavoMobile.lua", true))()
```
## Dev Hub Window Style
```lua
local colors = {
    SchemeColor = Color3.fromRGB(252, 240, 3),
    Background = Color3.fromRGB(252, 3, 227),
    Header = Color3.fromRGB(3, 23, 252),
    TextColor = Color3.fromRGB(252, 3, 244),
    ElementColor = Color3.fromRGB(0, 0, 0)
}
local Window = Library.CreateLib("TITLE", colors)
```
## Create Window
```lua
local Window = Library.CreateLib("TITLE", "DarkTheme")
```
## Create Tabs
```lua
local Tab = Window:NewTab("TabName")
```
## Create Section
```lua
local Section = Tab:NewSection("Section Name")
```
## Create Label
```lua
Section:NewLabel("LabelText")
```
## Create Button
```lua
Section:NewButton("ButtonText", "ButtonInfo", function()
    print("Clicked")
end)
```
## Create Toggle
```lua
Section:NewToggle("ToggleText", "ToggleInfo", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
```
## Create Slider
```lua
Section:NewSlider("SliderText", "SliderInfo", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
```
## Create TextBox
```lua
Section:NewTextBox("TextboxText", "TextboxInfo", function(txt)
	print(txt)
end)

```
## Create Keybinds
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	print("You just clicked the bind")
end)

```
## Toggle Ui Keybinds
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
```
## Create DropDown
```lua
Section:NewDropdown("DropdownText", "DropdownInf", {"Option 1", "Option 2", "Option 3"}, function(currentOption)
    print(currentOption)
end)

```


