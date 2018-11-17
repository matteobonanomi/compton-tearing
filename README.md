# My Compton Config file to remove tearing from XFCE Desktop

This repo provides a sample compton.conf configuration file, optimized for XFCE desktop and any Linux distro. 
It is particularly useful to remove tearing issues that one can experience with XFCE combined with Intel or nVidia graphic cards.

## Getting Started

### Prerequisites
* **If you run Linux** I tested this script on Linux Mint XFCE, Xubuntu 18.04 and Manjaro XFCE. There are good reasons to believe it can fix XFCE experience in any Arch-based and Debian-based distro.
* **If you run Windows** install Linux

### Clone this repo
```
git clone https://github.com/matteobonanomi/comptonnotearing
```

### Install compton compositing manager

**Arch based systems**

```
sudo pacman -S compton
```

**Ubuntu and Debian based systems**

```
sudo apt-get install compton
```

### Configure Compton

1. Copy the configuration file [compton.conf](compton.conf) of this repo in *~/.config/compton.conf*

2. Disable XFCE compositor:

```
xfconf-query -c xfwm4 -p /general/use_compositing -s false
``` 

3. Copy [compton.desktop](compton.desktop]) file of this repo in the autostart folder *~/.config/autostart/compton.desktop* 

4. Restart your machine and ensure that compton is actually running with:

```
pgrep -l compton
``` 
5. Enjoy a web-browser and multimedia experience without any tearing issue! Try and change you graphic card driver (open vs proprietary) if you still have troubles.

## Documentation

* [Manjaro Documentation](https://wiki.manjaro.org/index.php?title=Using_Compton_for_a_tear-free_experience_in_Xfce) - Tear-free Compton on Manjaro XFCE

## Versioning

We use [Git](https://git-scm.com/) for versioning. Look for new available versions, check the [list of commits](https://github.com/matteobonanomi/comptonnotearing/commits/master). 

## Authors

* **Matteo Bonanomi** - [My GitHub](https://github.com/matteobonanomi)

## License

* This project is licensed under the GPL v3 License - see the [LICENSE.md](license.md) file for details

## Acknowledgments

* Acknowledgement is given to [Compton](https://github.com/chjj/compton) developers for providing such a lightweight and stable software
