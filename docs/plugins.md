# Plugins

There are several plugin types for fHDHR. See below for details regarding what each type is.  
_**Note**: if you wish to use fHDHR with Plex you will need `fHDHR_plugin_interface_hdhr`, as it allows fHDHR to masquerade as an HDHomeRun device (so Plex can understand it)._

## Origins

Look [here](https://github.com/fHDHR) for plugins that start with "fHDHR_plugin_origin_".

An Origin plugin is where we are streaming video from. It provides fHDHR with a channel listing, and how to connect to a service to stream from.  
Some Origin plugins will provide EPG data. Those that don't will have blocks of empty timeslot data created.  
Some Origin Plugins will also provide an added webpage to the webUI.  
Without an Origin plugin installed, fHDHR really cannot do much of anything.

## Interface Plugins

Look [here](https://github.com/fHDHR) for plugins that start with "fHDHR_plugin_interface_".  
Interface plugins provide additionally access to fHDHR. By default, fHDHR provides basic channel with an accessible API for channel tuning, EPG, and m3u.  
A plugin of most interest to the average user will be the `fHDHR_plugin_interface_hdhr` plugin. This plugin provides Plex access to fHDHR as if it was a HDHomeRun device, and as a result **is mandatory if you want to connect Plex to fHDHR**.

## Stream Plugins

Look [Here](https://github.com/fHDHR) for plugins that start with "fHDHR_plugin_stream_".  
These plugins provide alternative methods for streaming. At it's core fHDHR was designed to NOT rely on ffmpeg/vlc to run.  
These plugins can allow transcoding at the fHDHR level, whereas fHDHR core cannot.

## EPG Plugins

Look [here](https://github.com/fHDHR) for plugins that start with "fHDHR_plugin_epg_".  
These plugins provide alternative sources of EPG information. This can be handy for origin plugins that don't provide good/any EPG.
