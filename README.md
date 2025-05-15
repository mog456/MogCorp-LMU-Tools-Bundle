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
- MogCorp StrategyThingy - a customisable realtime tyre analysis tool and pit strategy calculator
- MogCorp TyreFrippery - a tyre info display widgety thing
- MogCorp SessionInfoMaBob - minimal session information display
- [Redadeg plugin](https://github.com/tembob64/Redadeg.lmuDataPlugin) for SimHub (used to capture LMU telemetry)

This bundle is menat to be modular; you can pick and choose which elements to use, either seperately or by combining elements into one Dash/overlay within SimHub. This was initially conceived as a means to produce a more functional overlay for our creaking leader, Hestor MogWitt III: a VR user in LMU. More info on this process is outlined HERE [LINK]. 

Should these tools prove useful then MogCorp will continue development towards offering these resources via a SimHub plugin. So if you find it useful and want mores, you know what to do right?

# Download and Install
Download the latest release [here](https://github.com/mog456/MogCorp-LMU-Tools-Bundle/releases/latest) and unzip it.

***IMPORTANT*** After unzipping make sure to copy the file Redadeg.lmuDataPlugin.dll to your SimHub installation root dir.
Usually found at: ```...\Program Files (x86)\SimHub\```

Once you have the plugin copied to the SimHub dir just double click each of the dasboards in the bundle to install them in SimHub.

Launch Simhub and make sure the Redadeg LMU Data plugin' is enabled by going to 'Add/Remove Features' and enabling it there. If you can't see the plugin in SimHub make sure you have copied the Redadeg.lmuDataPlugin.dll to your SimHub installation root dir. [IMG]

You should now see the dashboards in SimHub's 'Dash Studio' tab and be able to launch them from there. [IMG]

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

*(There are a few other options in the settings file but they are mostly about debug display for those so inclined.)*

**NOTE: For more info on the trackData.json and how to edit this file see this more detailed breakdown...[LINK]**

# MogCorp StrategyThingy

[IMG]
----

A live strategy display that tracks fuel/energy consumption over the previous 5 valid laps and suggests your next pit strategy. Display type (e.g. nrg/fuel etc) is automatically sel;ected by vehicle class. Main functionality includes:

- Where remaining race time is more than current vehicle fuel/nrg capacity, output will return a 'full stint' strategy - e.g. 100% nrg/max fuel
- Where remaining race time is within the max capacity of the vehicle, output will return an estimated nrg/fuel strat based on last 5 valid laps consumption
- In cases where remaining race time is within the nrg/fuel capacity of the vehicle, output will also display live fuel/nrg, time and laps delta to race finish
- Output displays a LED indicator that indicates the difference between your selected startegy (in game) and the estimated startegy, where GREEN = within 1.0 (units fuel/nrg%), RED = under estimate, ORANGE = over estimate.
- Where race time remaining is within capcity of vehicle, the estimated strategy will also account for extra laps of nrg/fuel as defined in strategyThiny_settings.json (see below for setting details).
- Output will also display a fuel/nrg warning (red background) indicator when current levels are below thresholds in settings.json.

 The startegyThingy settings.json is located at ```../Program Files (x86)/SimHub/DashTemplates/MogCorp StrategyThingy/JavascriptExtensions/Extras/Settings/startegyThingy_settings.json```. Again, just change the values you want (e.g. extraLaps, fuel/nrg warning levels) and save it.

# MogCorp TyreFrippery

[IMG]
----

Its a tyre widgety thing that displays info about those tyres including:
- Temperature (IMO and overall)
- Wear (visual and numeric indicator)
- Pressures

# MogCorp SesionInfoMaBob

[IMG]
----

Displays stuff aboout the current session....

# Extra Info

To create a modular all in one type dash using these tools (e.g. for a pinnable VR Dash) see [LINK].

# Acknowledgements

# ToDo

# Contact






