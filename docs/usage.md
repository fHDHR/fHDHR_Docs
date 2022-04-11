# Usage

## Author Notes

* All Testing is currently done in Proxmox LXC, Ubuntu 20.04, Python 3.8

## Prerequisites

* A Linux or Mac "Server". Windows currently does not work. A "Server" is a computer that is typically always online.
* Python 3.7 or later.
* Plugins may have other requirements as well.

## Optional Prerequisites

* If you intend to use Docker, [this guide](https://docs.docker.com/get-started/) should help you get started. The author of fHDHR is not a docker user, but will still try to help.

## Installation

### Linux

> The below instructions use the user "sysop", but you can run it as any user. The script will allow you to run as root, but warns against doing so.

1. Download the release zip, or git clone to your prefered location.  

```bash
cd /home/sysop && git clone https://github.com/fHDHR/fHDHR.git
```

2. Navigate into your script directory and install the python requirements.  

```bash
cd fHDHR && pip3 install -r requirements.txt
```

3. Copy the included `config.example.ini` file to a known location:

```bash
cp config.example.ini /home/sysop/config.ini
```

> The script will not run without this - there is no default configuration file location. 
 
4. Modify the configuration file to suit your needs.

5. Install desired fHDHR plugins.

> fHDHR will technically run without plugins installed, but is practically useless without an "origin" plugin.  

6. Install plugin python requirements file:

```bash
pip3 install -r requirements.txt
```

7. Run with the path to the config file:

```bash
python3 /home/sysop/fhdhr/main.py -c=/home/sysop/config.ini
```

### Docker

If you wish to use fHDHR in Docker, then check out the [Docker documentation](./installation_docker.md). 

## Setup

Now that you have fHDHR running, you can navigate (in a web browser) to the IP:Port from the configuration step above.  

If you did not setup a `discovery_address` in your config, SSDP will be disabled. This is not a problem as clients like Plex can have the IP:Port entered manually!  

You can copy the xmltv link from the webUI and use that in your client software to provide Channel Guide information.
