How to Use
1. Clone the Repository
Start by cloning the repository to your local machine. Open Terminal and run the following commands:

bash
Copy code
git clone https://github.com/yourusername/reshade-installer-macos.git
cd reshade-installer-macos
2. Make the Script Executable
Before running the script, you need to ensure it has the correct permissions. This step is crucial to allow the script to execute:

bash
Copy code
chmod +x install_reshade.sh
3. Install Required Dependencies
Make sure you have the necessary dependencies installed on your macOS system. You can install them using Homebrew:

Wine: Required for running Windows executables like the ReShade installer.

bash
Copy code
brew install --cask wine-stable
Other Tools: curl, git, grep, and tar are typically pre-installed on macOS. If not, install them with:

bash
Copy code
brew install curl git grep tar
4. Run the Script
With everything set up, you can now run the script:

bash
Copy code
./install_reshade.sh
This script will:

Prompt you to enter the path to the game directory.
Automatically download the latest version of ReShade.
Install ReShade using Wine, configuring it for your game.
5. (Optional) Wrapping the Script into a macOS Application
For a more user-friendly experience, you can wrap this script into a macOS application:

Wrapping with Automator
Open Automator and create a new application.
Add a "Run Shell Script" action and paste the script content.
Save the Automator workflow as an application (ReShade Installer.app).
Run the .app file by double-clicking it.
Wrapping with Platypus
Download Platypus from here.
Create a new project, choose "Shell" as the script type, and paste in the script.
Customize the settings, then build the .app bundle.
Distribute or use the .app like any other macOS application.
6. Troubleshooting
Permissions Issues: If you encounter errors related to permissions, make sure the script is executable (chmod +x install_reshade.sh).
Wine Not Found: If the script fails due to Wine not being found, verify that Wine is installed and configured correctly (brew install --cask wine-stable).
