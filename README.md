[![Crowdin](https://d322cqt584bo4o.cloudfront.net/torrent-file-editor/localized.svg)](https://crowdin.com/project/torrent-file-editor)
[![Version](https://badge.fury.io/gh/torrent-file-editor%2Ftorrent-file-editor.svg)](https://badge.fury.io/gh/torrent-file-editor%2Ftorrent-file-editor)

# **Torrent File Editor**

Qt based GUI tool designed to create and edit .torrent files

Author: Ivan Romanov <[drizt72@zoho.eu](mailto:drizt72@zoho.eu)>  
License: GNU General Public License v3.0 or later  
Homepage: https://torrent-file-editor.github.io  
Sources: https://github.com/torrent-file-editor/torrent-file-editor  
Crowdin translations: https://crowdin.com/project/torrent-file-editor

# Build Instructions

Need to have
 - CMake >= 3.5
 - Qt4 or Qt5 or Qt6
 - [Sparkle](http://sparkle-project.org/) only for Mac OS X

To choose Qt version use `QT*_BUILD=ON` cmake cache entry. Or `QT_QMAKE_EXECUTABLE=/path/to/qmake`. Actually
QT_QMAKE_EXECUTABLE added for autodecting in Qt Creator. Qt Creator adds this enty for each project. If no any from
above will be used Qt5.

## Linux

Should works for any Linux distribution which has CMake and Qt.

### Qt4

```sh
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DQT4_BUILD=ON ..
make
```

### Qt5

```sh
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DQT5_BUILD=ON ..
make
```

If building Qt5 version on Ubuntu 18.04+, install required Qt5LinguistTools from `qttools5-dev` package.

### Qt6

```sh
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release -DQT6_BUILD=ON ..
make
```

If cmake report some Qt6 requirements missing on Ubuntu, install them.

```sh
sudo apt install qt6-tools-dev libqt6core5compat6-dev
```

## Mac OS X

Only Qt5 version

```sh
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
make dmg # to build dmg package
```

I use macOS Mojave 10.14.4 with Qt 5.5.1 and Sparkle 1.20.0.

## Windows

Windows version can be build with official MinGW Qt and Qt Creator. For build Qt6 version need to install Qt5Compat
module. Building with MSVC studio not tested and may not work.

I use Fedora 31 MinGW to build Windows versions. Furthermore I build portable static versions. Package mingw-qt4
modified with some patch to fix building. See [build.sh](build.sh) for details.

### HACK FOR ``Qt5``:

1. Install ``MSYS2``
2. Run  
    ```sh
    pacman -S --disable-download-timeout \
        mingw-w64-x86_64-cmake \
        mingw-w64-x86_64-ninja \
        mingw-w64-x86_64-qt5-base \
        mingw-w64-x86_64-qt5-tools \
        mingw-w64-x86_64-ninja \
        mingw-w64-x86_64-pcre \
        mingw-w64-x86_64-pcre2 \
        mingw-w64-i686-gcc-libs
   ```
3. Run
    ```sh
    mkdir build && cd build
    cmake -DCMAKE_BUILD_TYPE=Release -DQT5_BUILD=ON ..
    ninja
   ```
4. Сopy from the ``build`` folder to your favorite place
    1. File ``torrent-file-editor.exe``
    2. Folders
        1. ``imageformats``
        2. ``platforms``
        3. ``styles``
5. Copy from msys2 installation (such as ``C:\msys64\mingw64\bin``)
    1. ``libpcre2-16-0.dll``
    2. ``libdouble-conversion.dll``
    3. ``libicuuc75.dll``
    4. ``libicuin75.dll``
    5. ``libpcre2-16-0.dll``
    6. ``libmd4c.dll``
    7. ``libzstd.dll``
    8. ``libicudt75.dll``
    9. ``libpcre2-8-0.dll``
    10. ``libgcc_s_seh-1.dll``
    11. ``libwinpthread-1.dll``
    12. ``libstdc++-6.dll``
    13. ``zlib1.dll``
    14. ``Qt5Widgets.dll``
    15. ``Qt5Gui.dll``
    16. ``Qt5Core.dll``
    17. ``libzstd.dll``
    18. ``libwinpthread-1.dll``
    19. ``libstdc++-6.dll``
    20. ``libpng16-16.dll``
    21. ``libpcre2-16-0.dll``
    22. ``libpcre-1.dll``
    23. ``libmd4c.dll``
    24. ``libintl-8.dll``
    25. ``libicuuc75.dll``
    26. ``libicuin75.dll``
    27. ``libicudt75.dll``
    28. ``libiconv-2.dll``
    29. ``libharfbuzz-0.dll``
    30. ``libgraphite2.dll``
    31. ``libglib-2.0-0.dll``
    32. ``libgcc_s_seh-1.dll``
    33. ``libfreetype-6.dll``
    34. ``libdouble-conversion.dll``
    35. ``libbz2-1.dll``
    36. ``libbrotlidec.dll``
    37. ``libbrotlicommon.dll``

# How Can I Help?

The Project is translated from English to several languages.
I would be glad if you add new translations. You can translate the
project to your native language with [Crowdin](https://crowdin.com/project/torrent-file-editor).
It is not difficult and no special knowledges are required.
Or you can correct my English. I know it is not good. Anyway you can
always email <[drizt72@zoho.eu](mailto:drizt72@zoho.eu)> me.

Also feel free to open an issue on GitHub or send me pull requests.

# Translations

<img src="https://flagicons.lipis.dev/flags/4x3/za.svg" width="24" height="24">  Afrikaans - Afrikaans  
<img src="https://flagicons.lipis.dev/flags/4x3/sa.svg" width="24" height="24">  العربية - Arabic  
<img src="https://flagicons.lipis.dev/flags/4x3/bd.svg" width="24" height="24">  বাংলা - Bengali  
<img src="https://flagicons.lipis.dev/flags/4x3/cn.svg" width="24" height="24">  简体中文 - Chinese Simplified  
<img src="https://flagicons.lipis.dev/flags/4x3/tw.svg" width="24" height="24">  繁體中文 - Chinese Traditional  
<img src="https://flagicons.lipis.dev/flags/4x3/cz.svg" width="24" height="24">  Čeština - Czech  
<img src="https://flagicons.lipis.dev/flags/4x3/nl.svg" width="24" height="24">  Nederlands - Dutch  
<img src="https://flagicons.lipis.dev/flags/4x3/us.svg" width="24" height="24">  English - English  
<img src="https://flagicons.lipis.dev/flags/4x3/fi.svg" width="24" height="24">  Suomi - Finnish  
<img src="https://flagicons.lipis.dev/flags/4x3/fr.svg" width="24" height="24">  Français - French  
<img src="https://flagicons.lipis.dev/flags/4x3/de.svg" width="24" height="24">  Deutsch - German  
<img src="https://flagicons.lipis.dev/flags/4x3/il.svg" width="24" height="24">  עברית‎ - Hebrew  
<img src="https://flagicons.lipis.dev/flags/4x3/hu.svg" width="24" height="24">  Magyar - Hungarian  
<img src="https://flagicons.lipis.dev/flags/4x3/id.svg" width="24" height="24">  Indonesia - Indonesian  
<img src="https://flagicons.lipis.dev/flags/4x3/it.svg" width="24" height="24">  Italiano - Italian  
<img src="https://flagicons.lipis.dev/flags/4x3/jp.svg" width="24" height="24">  日本語 - Japanese  
<img src="https://flagicons.lipis.dev/flags/4x3/kr.svg" width="24" height="24">  한국어 - Korean  
<img src="https://flagicons.lipis.dev/flags/4x3/pl.svg" width="24" height="24">  Polski - Polish  
<img src="https://flagicons.lipis.dev/flags/4x3/br.svg" width="24" height="24">  Português  (Brasil) - Portuguese (Brazil)  
<img src="https://flagicons.lipis.dev/flags/4x3/ro.svg" width="24" height="24">  Română - Romanian  
<img src="https://flagicons.lipis.dev/flags/4x3/ru.svg" width="24" height="24">  Русский - Russian  
<img src="https://flagicons.lipis.dev/flags/4x3/es.svg" width="24" height="24">  Español - Spanish  
<img src="https://flagicons.lipis.dev/flags/4x3/tr.svg" width="24" height="24">  Türkçe - Turkish  
<img src="https://flagicons.lipis.dev/flags/4x3/vn.svg" width="24" height="24">  Tiếng Việt - Vietnamese  
<img src="https://flagicons.lipis.dev/flags/4x3/ua.svg" width="24" height="24">  Украї́нська - Ukrainian  
