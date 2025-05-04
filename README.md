[![](https://github.com/mog456/MogCorp-LMU-Tools-Bundle/blob/main/img/mogCorpLogo_300.png?raw=true)](https://www.paypal.com/donate/?business=V4AQ5FUGX8PUW&no_recurring=1&item_name=%27Persistent+Mediocrity+Since+Breakfast%27&currency_code=GBP)


MogCorp has been proudly and consistently underperforming since around breakfast time.\
\
While great efforts are consistently made to maintain this low standard of productivity and development, 
many of our staff have succumbed to a recent outbreak of optimism resulting in an upsurge of instances of adequacy.\
\
In an attempt to reinstate our long and proud history of mediocrity fuelled by existential dread, chronic ennui, and creeping entropy, we are seeking donations from those in the 'real world'
who may find some of our products of use.\
\
Please consider donating so this project can continue to fail sideways.\
\
Hestor MogWitt III (MogCorp CEO)


# MogCorp LMU Tools Bundle
The MogCorp LMU Tools Bundle is a collection of [SimHub](https://www.simhubdash.com/) dashboards for Le Mans Ultimate. The bundle contains the following modules:
- MogCorp CornerMajig - a customisable realtime corner analysis tool
- MogCorp StrategyAndTyresThingy - a customisable realtime tyre analysis tool and pit strategy calculator
- MogCorp SessionInfoMaBob - minimal session information display
- [Redadeg plugin](https://github.com/tembob64/Redadeg.lmuDataPlugin) for SimHub (used to capture LMU telemetry)

# Download and Install
Download the latest release [here](https://github.com/mog456/MogCorp-LMU-Tools-Bundle/releases/latest) and unzip it.

***IMPORTANT*** After unzipping make sure to copy the file Redadeg.lmuDataPlugin.dll to your SimHub installation root dir.
Usually found at: ```...\Program Files (x86)\SimHub\```

Once you have the plugin copied to the SimHub dir just double click each of the dasboards in the bundle to install them in SimHub.

Launch Simhub and make sure the Redadeg LMU Data plugin' is enabled by going to 'Add/Remove Features' and enabling it there. If you can't see the plugin in SimHub make sure you have copied the Redadeg.lmuDataPlugin.dll to your SimHub installation root dir. [IMG]

You should now see the dashboards in SimHub's 'Dash Studio' tab and be able to launch them from there. [IMG]

To create a modular all in one type dash using these tools (e.g. for a pinnable VR Dash) see [LINK].

----
- ***TIP:*** *these tools are packaged as Simhub dashborads but can be enabled as overlays by clicking on the 'MORE' option on the right of the dashboard in SimHub and selecting 'Convert to overlay'. Doing this will create the overlay in the 'Overlays' Tab of SimHub.*
----

# MogCorp CornerMajig
A brake/throttle trace overlay that allows users to analyse per corner performanace in realtime on a per track basis. This tool keeps track of your performance (braking ditance, min speed, max speed and time in corner) on a per corner basis compared with your performance on your best lap in the current session. Using built in per track data users can get an idea of where time is being gained/lost in each corner.

----
- [IMG]
----

**SETTINGS:** CornerMajig has an editable settings file that allows users to chnage the functionality of the tool. The CornerMajig seetings can be found at: ```../Program Files (x86)/SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/Extras/Settings/cornerMajig_settings.json```. Just open that JSON up in a text editor and alter the settings to suit. The default is shown here:
```yaml {
{
  "background": {
      "description": "Set the transparency of the dash background (0.00 - 1.00), where 1.00 is fully opaque",
      "parameters": {
        "transparency": 0.5
      }
    },

    "liveDisplayLayout": {
      "description": "Use 'minSpeed', 'exitSpeed' OR 'brakeDistance' to outline how the live data display objects",
      "description#": "There are 2 rows and any combination of the 3 available properties can be used.",
      "parameters": {
        "row_00": "minSpeed",
        "row_01": "brakeDistance"
      }
    }
}
```

Remember to save the settings file (just hit 'Save' or CTRL+S) and restart the dash for the setting to take effect.





