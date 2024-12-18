# Kallos UI Library V2

Kallos is a Lua-based UI library designed for Roblox developers. It provides a modular and customizable framework to create stunning and functional user interfaces for your projects. The library includes built-in components like labels, toggles, sliders, keybinds, text inputs, and dropdown menus.

## Features

- **Ease of Use**: Simple API to create and manage UI elements.
- **Customizable**: All UI components are fully customizable.
- **Responsive**: Automatically scales to different screen sizes.
- **Modular Design**: Add or remove components as needed.

## Getting Started

To get started, add the `kallos.lua` file to your Roblox project. Include the library in your script:

```lua
local kallos = loadstring(game:HttpGet("https://raw.githubusercontent.com/Vision-Software-LLC/Kallos-V2/refs/heads/main/source.min.lua"))()
```

## Example Script

Here's a simple example demonstrating how to create a menu with a tab and a toggle:

```lua
local kallos = loadstring(game:HttpGet("https://raw.githubusercontent.com/Vision-Software-LLC/Kallos-V2/refs/heads/main/source.min.lua"))()

-- Create the main menu
local menu = kallos:New("Example Menu")

-- Add a tab
local exampleTab = menu:CreateTab("Example Tab", "rbxassetid://123456789")

-- Add a toggle to the tab
exampleTab:CreateToggle("Example Toggle", "This is a toggle example", false, function(state)
    print("Toggle State: ", state)
end)
```

For detailed setup instructions and examples, refer to the [Documentation](https\://github.com/Vision-Software-LLC/Kallos-V2/blob/main/documentation.md).
