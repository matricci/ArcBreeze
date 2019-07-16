
# ArcBreeze:
 
ArcBreeze is a fork of sierrabreeze that don't try to mimic MacOSX, instead it is Based on the Arc Theme. My goal with this decoration is provide a coherent look to the Arc Theme on Plasma Desktop

## Screenshot:

![Screenshot](Screenshot.png)

## How to install 
By now, the only way to install _ArcBreeze_ is to build the source code, __but don't panic__, is quite easy.
Download the following dependencies:
### Dependencies:

#### Ubuntu


```shell
sudo apt install build-essential libkf5config-dev libkdecorations2-dev libqt5x11extras5-dev qtdeclarative5-dev extra-cmake-modules libkf5guiaddons-dev libkf5configwidgets-dev libkf5windowsystem-dev libkf5coreaddons-dev gettext

```

#### Arch Linux


```shell
sudo pacman -S kdecoration qt5-declarative qt5-x11extras    # 				Decoration
sudo pacman -S cmake extra-cmake-modules
```


#### Fedora


```shell
sudo dnf install cmake extra-cmake-modules  
sudo dnf install "cmake(Qt5Core)" "cmake(Qt5Gui)" "cmake(Qt5DBus)" "cmake(Qt5X11Extras)" "cmake(KF5GuiAddons)" "cmake(KF5WindowSystem)" "cmake(KF5I18n)" "cmake(KDecoration2)" "cmake(KF5CoreAddons)" "cmake(KF5ConfigWidgets)"

```


Then download and build the code :)

```shell
git clone https://github.com/matricci/ArcBreeze.git
cd ArcBreeze
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DKDE_INSTALL_LIBDIR=lib -DBUILD_TESTING=OFF -DKDE_INSTALL_USE_QT_SYS_PATHS=ON
sudo make install

```
  
To avoid logging out, issue
```shell
kwin_x11 --replace &
```
Change the window decoration:
*Settings &rarr; Application Style &rarr; Window Decorations*.

## Acknowledgments:
- The author of SierraBreeze window decoration: Igor Shovkun https://github.com/ishovkun/SierraBreeze
- The authors of Breeze window decorations Martin Gräßlin and Hugo Pereira Da Costa
- Andrey Orst, the author of Breezemite Aurorae window decoration
https://github.com/andreyorst/Breezemite
- Chris Holland for his blog about patching Breeze decorations
https://zren.github.io/projects/2017/07/08/patching-breeze-window-decorations.html
