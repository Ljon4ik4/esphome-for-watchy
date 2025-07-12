# Root folder
* watchy-v3.yaml: main source file for v3-watchy
* watchy-v2.yaml: main source file for v2-watchy
* README.md: introduction to the project
* pins-v3.yaml: pin layout for v3-watchy
* pins-v2.yaml: pin layout for v2-watchy
* util.h: code to calculate sleep times and get the coordinates of a clock depending on time
* min_spiffs.csv: partition table (minimal allocation for SPIFFS filesystem, which stores static files, assets, logs...)
* default_8MB.csv : partition table, 
* mdi.yaml: material design icons to be used in standard esphome haml
* mdi.h: material design icons for use in lambdas i.e. cpp code
* ls-usb.sh: helper to list /dev/cu.usbmodem*
* LICENSE: MIT-license
* icons.h: maps weathercodes to corresponding mdi icons
* config-example.yaml: file containing the configuration (timezone etc)


# doc folder
contains pictures used in README.md

# fonts folder
* mdi folder: material design font
* futura bold folder: futura bold font
* pillow.rb: script to install pillow, probably unnecessary on most systems having pip

# utils folder
* the .json files manage some typescript dependencies and packaging
* generate.ts just runs the other typescript scripts
* generate-v2.ts generates the watchy-v2.yaml from the v3 one
* generate-config-example.ts takes the config.yaml and creates a config-example.yaml replacing values with placeholders (not done yet)
* generate-mdi.ts: extracts the mdi's used in watchyv3.yaml and outputs them to mdi.yaml and mdi.h (getting them from `fonts/mdi/scss/_variables.scss`, which does not exist in the repo - probably has to be added or installed somehow)

# automations folder
these run on home assistant, not on watchy
* watchy-weather.yaml: sends weather to watchy 
* watchy-calendar-agenda.yaml: sends todays calendar to watchy
* test-agenda.yaml: sending atest item for agenda
