# QtSystray

I created this project to try out Systray Icons
with QT 10 years ago. I ran into an issue that SVG
encoded icons would not render. To reproduce this 
I created this repo and filed the bug report
https://qt-project.atlassian.net/browse/QTBUG-53550

In the mean time the versions of the operating system,
the KDE Desktop and QT have evolved and after a little
adjusting of the CMakeLists.txt file this project
compiles again on QT 6.12 and all icons, including the
SVG icons, work fine.

## To run the demo

* git clone the repo
* open qtcreator
* open the project
* hit the green run triangle icon in bottom left