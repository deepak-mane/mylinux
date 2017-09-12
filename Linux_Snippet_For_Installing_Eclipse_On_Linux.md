# mylinux
---
# LINUX SNIPPET FOR 

## To Install Eclipse on Oracle Linux
---

### If you've downloaded Eclipse from their official website, follow these steps for the installation.

1. Extract the eclipse.XX.YY.tar.gz using
```linux
tar -zxvf eclipse.XX.YY.tar.gz
tar -zxvf eclipse-cpp-oxygen-R-linux-gtk-x86_64.tar.gz
```
2. Become root and Copy the extracted folder to /opt
```linux
sudo mv eclipse.XX.YY /opt
```
3. Create a desktop file and install it:
```linux
gedit eclipse.desktop
```
4. and copy the following to the eclipse.desktop file
```linux
[Desktop Entry]
Name=Eclipse 
Type=Application
Exec=env UBUNTU_MENUPROXY=0 eclipse44
Terminal=false
Icon=eclipse
Comment=Integrated Development Environment
NoDisplay=false
Categories=Development;IDE;
Name[en]=Eclipse
```
and make sure that it has executable permission, then execute the following command to automatically install it in the unity:
```linux
sudo desktop-file-install eclipse.desktop
```
5. Create a symlink in /usr/local/bin using
```linux
sudo ln -s /opt/eclipse/eclipse /usr/local/bin/eclipse44
```
6. For eclipse icon to be displayed in dash, eclipse icon can be added as
```linux
sudo cp /opt/eclipse/icon.xpm /usr/share/pixmaps/eclipse.xpm
```
7. Don't forget that you need to have either OpenJDK or Sun Java installed to be able to run eclipse. Check this question for more information about Java installation. Here is a simple example of installing Open JDK 1.6:
```linux
sudo apt-get install openjdk-6-jdk
```
8. Launch Eclipse and then give it the required permissions to modify the osgi file:
```linux
sudo chown -R $USER:$USER /opt/eclipse/configuration/org.eclipse.osgi
```
#### PS: You must launch Eclipse first, because the org.eclipse.osgi directory is created only afterthe first launch.


##### END OF SNIPPET 4:53 PM 9/12/2017