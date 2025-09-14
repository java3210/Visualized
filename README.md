# Importing the Library
```lua
local Visualized = loadstring(game:HttpGet('https://github.com/java3210/Visualized/blob/main/main/dowload.lua?raw=true', true))()
```
## Create Window
```lua
local Window = Visualized.new({
	Title = "Synapse X",
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
