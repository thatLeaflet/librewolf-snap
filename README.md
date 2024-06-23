Note: This is an unofficial repackaging and is not endorsed by the upstream project. The upstream Librewolf project can be found [here](https://librewolf.net/). Additionally,
- this package probably has broken sandboxing / security issues
- missing functionality due to minimal snap permissions
- will not get automatically updated
- may not get timely updates
- can't be set as default browser
- missing options in right click menu in application launcher (e.g. open private tab)
- should only be used for testing purposes. 

## Want to build the snap yourself?

Before you begin
- Ensure you have snapd installed
- Ensure you have git installed

How to set up snapcraft
- Install snapcraft: run `sudo snap install snapcraft --classic`
- Install lxd: run `sudo snap install lxd`
- Add your user to the lxd group: run `sudo usermod -aG lxd $USER`
- Reboot your computer
- Configure lxd: run `lxd init --minimal`

How to build the snap
- Enter a nice working directory (e.g. ~/projects)
- Download repo: run `git clone https://github.com/thatLeaflet/librewolf-snap.git && cd ./librewolf-snap`
- Build the snap: run `snapcraft`
- Install the snap: run `sudo snap install --dangerous ./librewolf_*_amd64.snap`
- Add permissions: run `sudo snap connect librewolf:browser-sandbox`
