### peloton-to-garmin
Convert workout data from Peloton into a TCX file that can be uploaded to Garmin


## Setup
1. Download the repo [here](https://github.com/jrit/peloton-to-tcx/archive/master.zip)
1. Extract the zip file
1. Install the latest version of [Python 3](https://www.python.org/downloads/), currently 3.6.4
1. Open `File Explorer` and navigate to the wherever you unzipped the downloaded project
1. Navigate so that you are inside the `peloton-to-garmin` folder
1. Open a command prompt by clicking in the `Location Bar` at the top and typing `cmd` then hit enter
1. From the command prompt run the following command:
    1. `pip install requests ConfigParser`
1. Close the command prompt and return to the `peloton-to-garmin` folder
1. Edit the `config.ini` file and set your Peloton Email and Password, Save and Close

## Usage
* Open a command prompt inside of the `peloton-to-garmin` folder
* Run the following command:
    * `python peloton-to-garmin`
* You will be prompted to enter how many workouts you would like to fetch
* A TCX file for each workout will be created in the `output` directory
* The resulting TCX file can then be uploaded to Garmin

## Autoupload to Garmin
* Put your Garmin connnect credentials in .guploadrc
* Put a fully qualified path to your output folder in runme.sh.  Be careful, all tcx files will be removed before downloading new ones!

## TODO
* Use docker environment variable to set the number of activities to download from peloton
* Use docker environment variable to set all configurable propeties (usernames, passwords, output folder location, etc.)
* Feed names into garmin upload tool along with file names
* Run container as a service that will periodically check for new activities