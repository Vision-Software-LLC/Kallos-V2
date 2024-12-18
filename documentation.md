# Kallos UI Library Documentation

Kallos is a Lua UI library for creating modular, scalable, and customizable UI elements in Roblox.

## Table of Contents
- [Initialization](#initialization)
- [Tabs](#tabs)
- [UI Elements](#ui-elements)
  - [Label](#label)
  - [Toggle](#toggle)
  - [Slider](#slider)
  - [Keybind](#keybind)
  - [Text Input](#text-input)
  - [Dropdown (Expander)](#dropdown-expander)
- [Element Methods](#element-methods)

---

## Initialization

To create a new menu, use the `New` method:

```lua
local menu = kallos:New(string: title)
```

### Menu Properties
- `menu.toggleBind`: *(string)* Keybind to toggle the UI visibility. Default: `"RightShift"`.

---

## Tabs

Create a new tab within the menu:

```lua
local tab = menu:CreateTab(string: name, string: icon)
```

### Tab Parameters
- **name**: The name of the tab.
- **icon**: *(Optional)* The image ID for the tab's icon.

---

## UI Elements

UI elements are created within a tab. Each element has specific parameters and methods for customization.

### Label

```lua
local label = tab:CreateLabel(string: text)
```

#### Label Methods
- `label:SetLabelText(string: text)`  
  Updates the label's text.

- `label:GetLabelText()`  
  Returns the current text of the label.

---

### Toggle

```lua
local toggle = tab:CreateToggle(string: name, string: description, boolean: default, function: callback)
```

#### Toggle Parameters
- **name**: The toggle's name.
- **description**: Description of the toggle.
- **default**: Initial toggle state (`true` or `false`).
- **callback**: Function to execute when the toggle state changes.

#### Toggle Methods
- `toggle:SetToggle(boolean: state)`  
  Sets the toggle's state.

- `toggle:GetToggle()`  
  Returns the current state of the toggle.

---

### Slider

```lua
local slider = tab:CreateSlider(string: name, string: description, number: default, number: minimum, number: maximum, number: interval, function: callback)
```

#### Slider Parameters
- **name**: The slider's name.
- **description**: Description of the slider.
- **default**: Initial slider value.
- **minimum**: Minimum value for the slider.
- **maximum**: Maximum value for the slider.
- **interval**: Step interval for slider value.
- **callback**: Function to execute when the slider value changes.

#### Slider Methods
- `slider:SetSliderValue(number: value)`  
  Sets the slider's value.

- `slider:GetSliderValue()`  
  Returns the current slider value.

---

### Keybind

```lua
local keyBind = tab:CreateKeybind(string: name, string: description, string: defaultKey, function: callback)
```

#### Keybind Parameters
- **name**: The keybind's name.
- **description**: Description of the keybind.
- **defaultKey**: Default keybind.
- **callback**: Function to execute when the keybind is activated.

#### Keybind Methods
- `keyBind:SetKeyBind(string: key)`  
  Sets the keybind's key.

- `keyBind:GetKeyBind()`  
  Returns the current keybind.

---

### Text Input

```lua
local textInput = tab:CreateTextInput(string: name, string: description, string: defaultText, string: placeholderText, function: callback)
```

#### Text Input Parameters
- **name**: The text input's name.
- **description**: Description of the text input.
- **defaultText**: Initial text in the input box.
- **placeholderText**: Placeholder text for the input box.
- **callback**: Function to execute when the text is updated.

#### Text Input Methods
- `textInput:SetTextInput(string: text)`  
  Sets the text input's value.

- `textInput:GetTextInput()`  
  Returns the current text input value.

---

### Dropdown (Expander)

```lua
local dropDown = tab:CreateDropDown(string: name, string: description, string: defaultText, {
    {string: optionText, string: optionDescription},
}, function: callback)
```

#### Dropdown Parameters
- **name**: The dropdown's name.
- **description**: Description of the dropdown.
- **defaultText**: Default selected option.
- **options**: Table of options, where each option is a table containing:
  - **optionText**: Display text of the option.
  - **optionDescription**: Description of the option.
- **callback**: Function to execute when an option is selected.

#### Dropdown Methods
- `dropDown:SetDropDownValue(string: value)`  
  Sets the dropdown's selected value.

- `dropDown:GetDropDownValue()`  
  Returns the currently selected dropdown value.

---

## Element Methods

### General
All UI elements support these methods:

- **Parenting**: Add or remove elements by changing their `Parent` property.
- **Layout Order**: Adjust the `LayoutOrder` property to control the order in which elements appear.

---

