use the flatpak

don't try to run it without X-Wayland


https://wiki.archlinux.org/title/Steam
https://www.reddit.com/r/linux_gaming/comments/sok9zw/how_to_use_fsr_on_any_steam_game_with_gamescope/

flatpak --user install com.valvesoftware.Steam
flatpak --user install org.freedesktop.Platform.VulkanLayer.gamescope

Then in Steam, edit the game properties and make it run
`gamescope -- %command%`

This will let you exit the game without crashing weston