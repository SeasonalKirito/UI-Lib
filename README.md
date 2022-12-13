# 📜UI-Lib📜
This UI Libary is not an offical release of mine, this is a Guided use of the UI Library, Give credits to who ever got their source stolen.


# 🖥️Booting the Library🖥️
This is just a lil beta ui lib so im not gonna re write so much of the code so just put the code in this website right infront of your code
```
https://raw.githubusercontent.com/SeasonalKirito/UI-Lib/main/Epic%20Thing%20Lib.lua
```


# ⌨️Loading a Window⌨️
```lua
local Window = library:Window("Name", "Author") -- This will make the main window which will support this whole ui lib
```


# 📁Tabs📁
```lua
local Tabs = {
    Changelogs = Window:Tab("Changelogs");
    Home = Window:Tab("Home");
    Main = Window:Tab("Main");
    Misc = Window:Tab("Misc");
}
```


# 📑Sections📑
```lua
local Sections = {
    Changelogs = {
         Updates = Tabs.Changelogs:Section("Updates");
         Updates = Tabs.Changelogs:Section("Credits");
    Home = {
        Credits = Tabs.Home:Section("Discord");
    };
    Main = {
        Autofarm = Tabs.Main:Section("Main");
    };
    Misc = {
        Miscellaneous = Tabs.Misc:Section('Miscellaneous')
    };
}
```


# 🔘Button🔘
```lua
Sections.Home.Discord:Button("Copy Script.gg | REBORN Discord Invite", function()
    setclipboard('https://discord.gg/Uh2s7MvMAf')
end)
```


# ⚠️Notification⚠️
```lua
Sections.Home.Credits:Button(".gg/Script.gg | REBORN", function()
    setclipboard('https://discord.gg/Uh2s7MvMAf')
    Window:Notification("Message", {Text = "Copied!"; ConfirmText = "Okay";})
end)
```


# ⚫Toggle⚫
```lua
getgenv().AutoClick = value

Sections.Main.Autofarm:Toggle("Auto Click", function(value)
    getgenv().AutoClick = value
    while AutoClick do task.wait(0.1)
        fireclickdetector(workspace.button.ClickPart.ClickDetector)
    end
end)
```
