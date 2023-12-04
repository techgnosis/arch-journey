Arch `base` does not include Flatpak. You can install it with the `flatpak` package. You can run `pacman -S flatpak`. Like pacman, Flatpak installs software from remote repositories. When you install the flatpak package, it also sets up the `flathub` repo. You can type `flatpak remotes` to see the repositories that are available. 

Flatpak allows you to install packages at the system level, or the user level. You can only install system level packages from system level repos, and you can only install user level packages from user level repos. That means that you can't install a user level package from the system level Flathub repo. You have to add the Flathub repo at the user level by running the following:

`flatpak repo add etc etc etc`

flatpak install

flatpak run

flatpak uninstall

flatpak uninstall --unused