# wavetable-synthesis

In this repo I am collating some info on wavetable synthesis that wasn't particularly easy to find in 2024

Some of it is from here https://github.com/TeensyAudio/Wavetable-Synthesis/tree/master

However there was a new version of SoundfontDecoder made which is here https://github.com/PaulStoffregen/SoundfontDecoder/tree/master which is also cloned here 

## SoundFont Decoder

The SoundFont decoder is a python utility to decode a SoundFont file into native C++ datatypes. The decoder can be run via a GUI or via the command line.
How To Run

### To Run Soundfont Decoder Via Python

To run the GUI via Python, you must use Python3, specifically 3.6. The Sf2Utils Python package must be installed in order to run/build the decoder. Sf2Utils can be installed via pip install sf2utils

After dependancies have been installed, invoke the decoder GUI with $ python3 controller.py
Command Line Python Execution

### How to invoke the script:
The -d flag is for debug mode
The -i flag precedes the input file
$ python decoder.py -i soundfont
$ python decoder.py -d -i soundfont

### How To Build SoundfontDecoder.exe

    Pull the latest version of PyInstaller from https://github.com/pyinstaller/pyinstaller (at the time of this writing, PyInstaller in PIP doesn't support Python 3.6).
    Run the setup.py script from the PyInstaller repo.
    After PyInstaller is installed on the system, the pyinstaller.exe will be within the \Scripts folder of the system's Python directory. Navigate to this directory, and run the following command: pyinstaller --onefile --noconsole --name SoundfontDecoder <path-to-wavetable-code>\controller.py
    This will produce an executable file named controller.exe which contains the Soundfont Decoder.

Additional Instructions for building on Ubuntu:

    for step 2, make sure to use python3 when installing: i.e. python3 setup.py install -- this is because tkinter has been renamed to Tkinter in python3
    the executable file will be in the dist directory
