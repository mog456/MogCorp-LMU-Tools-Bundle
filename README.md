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
![MogCorp LMU Tools](img/elementsComp03.png "MogCorp LMU Tools")

The MogCorp LMU Tools Bundle is a collection of [SimHub](https://www.simhubdash.com/) dashboards for Le Mans Ultimate. The bundle contains the following modules:
- MogCorp CornerMajig - a customisable realtime corner analysis tool
- MogCorp StrategyThingy - a customisable realtime tyre analysis tool and pit strategy calculator
- MogCorp TyreFrippery - a tyre info display widgety thing
- MogCorp SessionInfoMaBob - minimal session information display
- [Redadeg plugin](https://github.com/tembob64/Redadeg.lmuDataPlugin) for SimHub (used to capture LMU telemetry)

This bundle is meant to be modular; you can pick and choose which elements to use, either separately or by combining elements into one Dash/overlay within SimHub. This was initially conceived as a means to produce a more functional overlay for our creaking leader, Hestor MogWitt III: a VR user in LMU. More info on this process is outlined HERE [LINK]. 

Should these tools prove useful then MogCorp will continue development towards offering these resources via a SimHub plugin. So if you find it useful and want more, you know what to do right?

# Download and Install
Download the latest release [here](https://github.com/mog456/MogCorp-LMU-Tools-Bundle/releases/latest) and unzip it.

***IMPORTANT*** After unzipping make sure to copy the file Redadeg.lmuDataPlugin.dll to your SimHub installation root dir.
Usually found at: ```...\Program Files (x86)\SimHub\```

Once you have the plugin copied to the SimHub dir just double click each of the dashboards in the bundle to install them in SimHub.

Launch Simhub and make sure the 'Redadeg LMU Data plugin' is enabled by going to 'Add/Remove Features' and enabling it there. If you can't see the plugin in SimHub make sure you have copied the Redadeg.lmuDataPlugin.dll to your SimHub installation root dir. 

![Enable PlugIn](img/enable%20redadeg.png "Enable Plugin")

You should now see the dashboards in SimHub's 'Dash Studio' tab and be able to launch them from there.

----
- ***TIP:*** *These tools are packaged as SimHub dashboards but can be enabled as overlays by clicking on the 'MORE' option on the right of the dashboard in SimHub and selecting 'Convert to overlay'. Doing this will create the overlay in the 'Overlays' Tab of SimHub.*
----

# MogCorp StrategyThingy
![Strategy Thingy](img/strategyComp.png "StrategyThingy")

A live strategy display that tracks fuel/energy consumption over the previous 5 valid laps and suggests your next pit strategy. Display type (e.g. nrg/fuel etc) is automatically selected by vehicle class. Main functionality includes:

- Where remaining race time is more than current vehicle fuel/nrg capacity, output will return a 'full stint' strategy - e.g. 100% nrg/max fuel
- Where remaining race time is within the max capacity of the vehicle, output will return an estimated nrg/fuel strat based on last 5 valid laps consumption
- In cases where remaining race time is within the nrg/fuel capacity of the vehicle, output will also display live fuel/nrg, time and laps delta to race finish
- Output displays a LED indicator that indicates the difference between your selected strategy (in game) and the estimated strategy, where GREEN = within 1.0 (units fuel/nrg%), RED = under estimate, ORANGE = over estimate.
- Where race time remaining is within capacity of vehicle, the estimated strategy will also account for extra laps of nrg/fuel as defined in strategyThingy_settings.json (see below for setting details).
- Output will also display a fuel/nrg warning (red background) indicator when current levels are below thresholds in settings.json.

 The strategyThingy settings.json is located at ```../Program Files (x86)/SimHub/DashTemplates/MogCorp StrategyThingy/JavascriptExtensions/Extras/Settings/strategyThingy_settings.json```. Again, just change the values you want (e.g. extraLaps, fuel/nrg warning levels) and save it.

 # MogCorp CornerMajig
A brake/throttle trace overlay that allows users to analyse per corner performance in realtime on a per track basis. This tool keeps track of your performance (braking distance, min speed, max speed and time in corner) on a per corner basis compared with your performance on your best lap in the current session. Using built-in per track data users can get an idea of where time is being gained/lost in each corner.
![CornerMajig Image](img/cornerMajig_ScreenShot.png "CornerMajig")

**SETTINGS:** CornerMajig has an editable settings file that allows users to change the functionality of the tool. The CornerMajig settings can be found at: ```../Program Files (x86)/SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/Extras/Settings/cornerMajig_settings.json```. Just open that JSON up in a text editor and alter the settings to suit.

Remember to save the settings file (just hit 'Save' or CTRL+S) and restart the dash for the setting to take effect.

*(There are a few other options in the settings file but they are mostly about debug display for those so inclined.)*

**NOTE: For more info on the trackData.json and how to edit this file see this more detailed breakdown...[LINK]**

# MogCorp TyreFrippery
![Tyre Frippery](img/TyreFrippery_02.png "TyreFrippery")

Its a tyre widgety thing that displays info about those tyres including:
- Temperature (IMO and overall)
- Wear (visual and numeric indicator)
- Pressures

# MogCorp SessionInfoMaBob
![SessionInfoMaBob](img/SessionInfoMaBob_01.png "SessionInfoMaBob")

Displays stuff about the current session....

# Extra Info
## Create a modular Dash
To create a modular (all in one) dash/overlay in SimHub using a selection of MogCorpLMU tools is quite straightforward but you will need to pay attention to the dir structure in SimHub and how any Javascript extensions and .json files associated with each MogCorp LMU tool are organised. Each tool is easy to copy and move into position within your own custom all in one Dash. If you don't get what I'm talking about when I say things like dir structure you may have some problems....

So here are the steps I've used to create my own all in one VR Dash:
- in SimHub 'create a new Dashboard' and give it a name.
- Set your new Dashboard properties to the size you require in Dashboard/Dahboard Properties (I used 1920 x 1080 for my full VR Dash)
- Set the background of your Dash to transparent (in Dashboard/Manage Screens)
 
Now open each element from the MogCorp LMU tools you want to add by finding the Dash in SimHub and clicking on 'More' then 'Edit dashboard'. This will open the selected dash in a new tab in the dash editor.
- Select the top most level of the MogCorp tool in the editor and copy it.
- Go back to your dash (which should still be open in tis own tab in the dash editor) and just paste it in.
- You can now drag the dash element wherever you want it on your dash.

When copy/pasting CornerMajig OR StrategyThingy into your new dash you will have to move some files about and edit a few lines of code to get everything working. In SimHub links to extensions/.json files are relative so your new dash will not find the appropriate links until you move and edit them. So..

----
- The new dash you just created will be in the dir at `.../SimHub/DashTemplates/YOUR NEW DASH NAME`
- the dir you need to focus on will be in that dir and named `JavascriptExtensions`. In this dir you'll need to dupe the relevant files from the MogCorp originals. You can follow my dir structure but it's not absolutely necessary.

----
  Copy the .js extension files from the original dash to your new dash (`.../SimHub/DashTemplates/YOUR NEW DASH NAME/JavascriptExtensions/`)
- Copy CornerMajig js extension. `.../SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/MogCorpCornerMajig.js`
- Copy StrategyThingy js extension. `.../SimHub/DashTemplates/MogCorp StrategyThingy/JavascriptExtensions/MogCorpStrategyThingy.js`

----
  Next copy the settings/trackData json files to your dash dir. I've created a dir structure for convenience but as long as the files are under `/JavascriptExtensions` you'll be fine.
- Copy CornerMajig settings.json. `.../SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/Extras/Settings/cornerMajig_settings.json`
- Copy StrategyThingy_settings.json. `.../SimHub/DashTemplates/MogCorp StrategyThingy/JavascriptExtensions/Extras/Settings/strategyThingy_settings.json` 
- Copy CornerMajig trackData.json. `.../SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/Extras/Data/trackData.json`

----
Finally in order to get everything hooked up you just need to edit ``JavascriptExtensions/MogCorpCornerMajig.js`` and ``JavascriptExtensions/MogCorpStrategyThingy.js`` so the new .json paths resolve correctly:

In `JavascriptExtensions/MogCorpCornerMajig.js` edit the lines as follows (right at the top of the script so you can't miss it):

```
let settingsPath_CORNERS = './DashTemplates/YOUR NEW DASH NAME/JavascriptExtensions/PATH TO YOUR COPY OF cornerMajig_settings.json';
let trackDataPath_CORNERS = './DashTemplates/Mogs LMU Dash_FULL/JavascriptExtensions/PATH TO YOUR COPY OF trackData.json';
```

Similarly in `JavascriptExtensions/MogCorpStrategyThingy.js` edit the line:
```
let strategySettingsPath = './DashTemplates/Mogs LMU Dash_FULL/JavascriptExtensions/PATH TO YOUR COPY OF strategyThingy_settings.json';
```

*(If you're lost here I am able to offer help)*

## A Note On trackData.json
The MogCorp CornerMajig tool relies on the .json file trackData.json found at ``.../SimHub/DashTemplates/MogCorp CornerMajig/JavascriptExtensions/Extras/Data/trackData.json``. This file may come down to personal preference in terms of when a corner starts/ends. Editing this file (e.g. moving the 'start' of a corner backwards or moving the 'end' of a corner forward) can be done at your own discretion. Similarly some corners have been amalgamated into one - e.g. turn 1 and 2 at Bahrain) this is purely my own preference and if you wish to edit this file please feel free. What I would ask is that I am aware that some of the data contained here may be noticeably off. If you find this to be the case and you have edited the trackData please let me know so I can include any updated data in future releases.

In terms of editing the trackData.json make sure there is no corner overlap (e.g. a corner start distance SHOULD NOT BE GREATER THAN the previous corners' end distance) *AND* make sure that each data element in corners[] has an individual cornerName. There is absolutely no need for the corners to named sequentially (1, 2, 3, etc). The names are strings so you can call them what you want **AS LONG AS** each cornerName is unique.

Also, this cornerMajig tool is potentially extensible (in terms of being adapted for other sims) as it is only reliant on core SimHub telemetry data. If you have track data you wish to be included but is related to a sim other than LMU, again let me know as I'd be happy to incorporate it if you can provide me with the data (I have been using data from MoTeC).

# Acknowledgements
Huge thanks to [Redadeg plugin](https://github.com/tembob64/Redadeg.lmuDataPlugin) for allowing me to use this plugin. Awesome.

Our humble thanks also go out to all that have supported MogCorp over the last few years. Whether you realise it or not you have been a great help to us in the fumbling darkness. Especially everyone at [Bongo Racing](https://www.youtube.com/@BongoRacing). If you want to get in touch about this stuff you can reach me via the Discord you'll find at that link.

# ToDo
- If support for this project is forthcoming we will do away with much of the faffing when copying settings etc. and centralise everything in a SimHub plugin.
- trackData.json only has the base LMU tracks at this point
