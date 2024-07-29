# touchstone-feeder
NFT Touchstone metadata sorter 

A script to read all the metadata (.JSON) files in a given directory and create a new Excel file that meets the Touchstone requirements for minting NFTs on the Flow blockchain.

Environment Setup (Windows)
To run the provided Python script on a Windows laptop, you'll need to install the following software and packages:
  1. Python: First, you need to have Python installed on your system. You can download the latest version of Python from the official website (https://www.python.org/downloads/). Make sure to check the box that says "Add Python to PATH" during the installation process.
  2. Pip: Pip (the package installer for Python) is usually included with Python installations. If for some reason it is not included in your Python installation, you can follow the instructions on this page to install pip: https://pip.pypa.io/en/stable/installation/
  3. Pandas: Pandas is a popular data manipulation library for Python. You'll need to install it to run the script. You can do this by running the following command in your Command Prompt:
   ```
   pip install pandas
   ```
   If you encounter any issues, you might need to run the command prompt as administrator.
  4. Openpyxl: This package is needed to allow Pandas to work with Excel files. Install it by running the following command in your Command Prompt:
   ```
   pip install openpyxl
   ```
  5. An IDE or text editor: You'll need a text editor or an Integrated Development Environment (IDE) to write and edit your Python scripts. Some popular options include Visual Studio Code (https://code.visualstudio.com/), Sublime Text (https://www.sublimetext.com/), and PyCharm (https://www.jetbrains.com/pycharm/). Choose the one that suits your preferences and comfort level.

After installing the required software and packages, follow the instructions provided in the previous answer to run the script.

Running the Script
To invoke this Python script, follow these steps:

1. Save the script as a file, for example, `touchstone_feeder.py`.
2. Place your JSON files in the same directory as the script.
3. Open a terminal or command prompt.
4. Navigate to the directory containing the script and JSON files. For example, if your files are in a folder called `my_json_files` on your desktop, you can use the `cd` command to change the directory:
   ```
   cd Desktop/my_json_files
   ```
5. Run the script using the `python` command:
   ```
   python touchstone_feeder.py
   ```
6. The script will run, processing the JSON files and creating an Excel file called `descriptions.xlsx` in the same directory.

Please note that these instructions assume that you have Python installed and added to your system's PATH, as well as the required packages installed (pandas and openpyxl). If you haven't done this, you may need to specify the full path to the Python executable or adjust your PATH settings accordingly, and install the required packages using `pip install pandas openpyxl`.

For this to work, you have to customize the "legendary_traits", "rare_traits", "uncommon_traits and common_traits" (lines 87-129) manually to your NFTs. FORMAT: "Layer": ["Trait", "Trait", "Trait"] EXAMPLE: "Hair": ["Pink_hair", "Blue_hair", "Yellow_hair"]
"""
python -c "import touchstone_feeder; print(touchstone_feeder.__doc__) to see pydoc
