# WebUI

[Basic Configuration](../config)  | [Advanced Configuration](../adv_config) |  [WebUI](../webui)

---

This Page will introduce basic handling of the script from the Web Interface provided at IP:Port

The Pages are available in the buttons at the top, links to xmltv and m3u are provided at the top for ease of access.

## Main Landing Page

Below is the main landing page with basic information.

![Main WebUI](./screenshots/webui_main.PNG)

## Channels

This Page will display the channels you have per your origin plugin. It will also provide access to a Channel Editor.

* Note: The Play link in the left hand column can be copied to play a channel in VLC media player!

![Channels Page](./screenshots/webui_channels.PNG)

## Channel Editor

This Page will allow you to edit the channels you have per your origin plugin. From here, you can adjust the channel logo, the channel number, and the channel name.

[Channel Editor Page](screenshots/webui_channels_editor.PNG)

## Guide

This Page give you information about what is currently playing on all stations. It will also show the time remaining for each item.

* Note: The Play link in the left hand column can be copied to play a channel in VLC media player! (If selected EPG is from Origin)

![Guide Page](./screenshots/webui_guide.PNG)

## Tuners

This Page will show all active tuner information. You can also terminate a stream from here.

* Note: Clients will often have an amount buffered, and the connection termination is not immediate from a viewing perspective. However, the connection to the source is indeed cut off.

![Tuners Page](./screenshots/webui_tuners.PNG)

## xmltv

This page will give you access to all the xmltv formats provided by this variant.  
From here, you can manually update or even clear the cached epg, and then update.

![xmltv Page](./screenshots/webui_xmltv.PNG)

## Version

This page will give valuable information about the environment the script is being run in.

![Version Page](./screenshots/webui_version.PNG)

## Diagnostics

This page has various links to json/xml files that make the magic work.

![Diagnostics Page](./screenshots/webui_diagnostics.PNG)

## Settings

This page allows viewing/changing all possible configuration options.  
_Note: This will require a restart of the script to have any effect._

![Settings Page](./screenshots/webui_settings.PNG)
