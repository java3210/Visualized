# Importing the Library
```lua
local Visualized = loadstring(game:HttpGet('https://github.com/java3210/Visualized/blob/main/main/dowload.lua?raw=true', true))()
```
## Create Window
```lua
local Window = Visualized.new({
	Title = "Synapse X",
	Constant = "YOUR CONSTANT HERE"
})
```

## Create Tabs
```lua
local Tabs = Window:Add({
	Title = "General",
	Desc = "Event, Thread, Constant",
	Icon = 103207517628191
})
```

## Create Page Title
```lua
Tabs:PageTitle({
	Title = "Search engine",
	Desc = "The search engine you choose will be used for features like searching from the address bar and from images on web pages. Learn more"
})
```

## Create Section
```lua
local Section = Tabs.new()
```

## Create Line
```lua
Section:Line()
```

# Example [ How to Disable Line at End ]
```lua
Section:Toggle({
	Title = "Toggle",
	Desc = "This is Toggle",
	Value = false,
	DisbleLine = true, -- Disbled Line
	Call = print
})
```

### Create Toggle
```lua
Section:Toggle({
	Title = "Toggle",
	Desc = "This is Toggle",
	Value = false,
	Call = print
})

Toggle:SetValue(<boolean>)
```

### Create Button
```lua
Section:Button({
	Title = "Button",
	Desc = "This is Button",
	Call = function()
		print('Click')
	end,
})
```

### Create Slider
```lua
Section:Slider({
	Title = "Slider",
	Desc = "This is Slider",
	Value = 10,
	Min = 1,
	Max = 100,
	Rounding = 2,
	Call = function(value)
		print(value)
	end,
})
```

### Create Textfield
```lua
Section:Textfield({
	Title = "Textfield",
	Desc = "This is Textfield",
	Value = "Hello",
	Holder = "Waiting ...",
	Call = print,
})
```

### Create List
```lua
Section:List({
	Title = "Dropdown",
	List = {"Apple", "Banana", "Melon"},
	Value = {"Apple", "Banana"},
	Call = function(v)
		print(v)
	end,
})

List:Clear()
List:Clear(<string>)
List:AddList(<string>)
```

### Create Paragarp
```lua
Section2:Paragarp({
	Title = "Paragarp",
	Desc = "This is Paragarp",
})

Paragarp:SetTitle(<string>)
Paragarp:SetDesc(<string>)
```

# Full Example
```lua
local Visualized = loadstring(game:HttpGet('https://github.com/java3210/Visualized/blob/main/main/dowload.lua?raw=true', true))()

local Window = Visualized.new({
	Title = "Synapse X",
	Constant = "",
})

local Tabs = Window:Add({Title = "General",Desc = "Event, Thread, Constant",Icon = 103207517628191 }) do
	Tabs:PageTitle({
		Title = "Search engine",
		Desc = "The search engine you choose will be used for features like searching from the address bar and from images on web pages. Learn more"
	})

	local Section = Tabs.new() do
		Section:Toggle({
			Title = "Toggle",
			Desc = "This is Toggle",
			Value = false,
			Call = print
		})

		Section:Button({
			Title = "Button",
			Desc = "This is Button",
			Call = function()
				print('Click')
			end,
		})

		Section:Slider({
			Title = "Slider",
			Desc = "This is Slider",
			Value = 10,
			Min = 1,
			Max = 100,
			Rounding = 2,
			DisbleLine = true,
			Call = function(value)
				print(value)
			end,
		})
	end
	
end

local Tabs2 = Window:Add({ Title = "General", Desc = "Sub, Hello, Dog, Lobby", Icon = 103207517628191 }) do
	Tabs2:PageTitle({
		Title = "Memory Saver",
		Desc = "Chrome frees up memory from inactive tabs. This gives active tabs and other apps more computer resources and keeps Chrome fast. Your inactive tabs automatically become active again when you go back to them. Learn more about Memory Saver"
	})

	local Section2 = Tabs2.new() do
		Section2:Textfield({
			Title = "Textfield",
			Desc = "This is Textfield",
			Value = "Hello",
			Holder = "Waiting ...",
			Call = print,
		})
		
		local Paragarp = Section2:Paragarp({
			Title = "Paragarp",
			Desc = "This ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis ParagarpThis Paragarp",
		})
		
		Section2:List({
			Title = "Dropdown Multi",
			List = {"Apple", "Banana", "Melon"},
			Value = {"Apple", "Banana"},
			Call = function(v)
				print(v)
			end,
		})
		
		Section2:List({
			Title = "Dropdown",
			List = {"Apple", "Banana", "Melon"},
			Value = "Apple",
			DisbleLine = true,
			Call = function(v)
				print(v)
			end,
		})
	end
end
```
