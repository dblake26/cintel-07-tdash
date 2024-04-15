# Project 7: Issues and Improvements
Desiree Blake

# PyShiny Express: Palmer Penguins Dashboard

- Repository: [pyshiny-penguins-dashboard-express](https://github.com/denisecase/pyshiny-penguins-dashboard-express)
- Live App: [Penguins Dashboard (Express)](https://denisecase.github.io/pyshiny-penguins-dashboard-express/)

Run and publish interactive apps using PyShiny Express and GitHub Pages.

This is a teaching version of the app written for clarity and understanding.
To contribute, please fork the repository and submit a pull request.

## Data Description

This app uses the Palmer Penguins dataset which includes three penguin species observed on three islands in the Palmer Archipelago, Antarctica.
The data has been made available by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER, a member of the Long Term Ecological Research Network.

Column names for the penguins dataset include:

- species: penguin species (Chinstrap, Adelie, or Gentoo)
- island: island name (Dream, Torgersen, or Biscoe) in the Palmer Archipelago
- bill_length_mm: length of the bill in millimeters
- bill_depth_mm: depth of the bill in millimeters
- flipper_length_mm: length of the flipper in millimeters
- body_mass_g: body mass in grams
- sex: MALE or FEMALE

See: <https://allisonhorst.github.io/palmerpenguins/>
## Tools

- Python
- Shiny for Python
- VS Code + Python Extension
- Git
- GitHub

## Try in the Browser

Go to PyShiny Templates at <https://shiny.posit.co/py/templates/>.
Go to Dashboards / Basic Dashboard.

- <https://shiny.posit.co/py/templates/dashboard/>

## Reference App with Detailed Instructions

For more detailed instructions, see <https://github.com/denisecase/pyshiny-penguins-dashboard-express>.
That project README.md has more detailed instructions, including reminders for Mac and Linux. 

## Prerequisites

Before you start, have the following installed:

- **Python**: Install the most recent version from [python.org](https://www.python.org/downloads/).
- **Git**: Download and install Git from [git-scm.com](https://git-scm.com/downloads).
- **Visual Studio Code (VS Code)**: Download from [code.visualstudio.com](https://code.visualstudio.com/).
- **VS Code Extensions**: Install the Python extension and the Shiny extension in VS Code.

## Get the Code

Fork this project into your own GitHub account.
Clone **your** GitHub repo down to your local machine.
IMPORTANT: Use your GitHub **username** in place of denisecase.
[GitHub CLI](https://cli.github.com/) may work better on some machines.

```shell
git clone https://github.com/denisecase/cintel-07-tdash
```

### Configurations

- **Configure Git**: Set up your user name and email with Git using the following commands in your terminal.
Change the values to your name and email address. This is a one-time setup.

  ```shell
  git config --global user.name "Your Name"
  git config --global user.email "youremail@example.com"
  ```

## Run Locally - Initial Start

After cloning your project down to your Documents folder, open the project folder for editing in VS Code.

Create a local project virtual environment named .venv, activate it, and install the requirements.

When VS Code asks to use it for the workspace, select Yes.
If you miss the window, after installing, select from the VS Code menu, View / Command Palette, and type "Python: Select Interpreter" and select the .venv folder.

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands (for Windows - the activate command is slightly different Linux/Mac).

```shell
py -m venv .venv
.venv\Scripts\Activate
py -m pip install --upgrade pip setuptools
py -m pip install --upgrade -r requirements.txt
```

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands.

```shell
shiny run --reload --launch-browser app/app.py
```

Open a browser to <http://127.0.0.1:8000/> and test the app.

## Run Locally - Subsequent Starts

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands.

```shell
.venv\Scripts\Activate
shiny run --reload --launch-browser app/app.py
```

While the app is running, the terminal is fully engaged and cannot be used for other commands. 
To kill the terminal, click the trashcan icon in the VS Code terminal window. 

## After Changes, Export to Docs Folder

Export to docs folder and test GitHub Pages locally.

Open a new terminal (VS Code menu "Terminal" / "New Terminal") in the root project folder and run these commands. 
Remember to activate the environment first. 

```shell
.venv\Scripts\Activate
shiny static-assets remove
shinylive export app docs
py -m http.server --directory docs --bind localhost 8008
```

Open a browser to <http://[::1]:8008/> and test the Pages app.

## Push Changes back to GitHub

Open a terminal (VS Code menu "Terminal" / "New Terminal") in the root project folder and run these commands.

```shell
git add .
git commit -m "Useful commit message"
git push -u origin main
```

## Enable GitHub Pages

Go to your GitHub repo settings and enable GitHub Pages for the docs folder.

