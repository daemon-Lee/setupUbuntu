1. Open terminal here

Some time you login on a Folder and need to work with or file on It based on terminal. Only click right-mouse -> seletec Open terminal here.

    sudo apt-get install nautilus-open-terminal -y

2. One-click to minimize

Enable click to minimize on Ubuntu using command line (recommended)
This method is for Ubuntu 18.04 and 17.10 users with GNOME desktop environment.

The first option is using the terminal. I recommend this way to ‘minimize on click’ even if you are not comfortable with the command line.
Open a terminal using Ctrl+Alt+T shortcut or searching for it in the menu. All you need is to copy paste the command below in the terminal.

    gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'

No need of restarting your system or any thing of that sort. You can test the minimize on click behavior immediately after it.
If you do not like ‘click to minimize’ behavior, you can set it back to default using the command below:

    gsettings reset org.gnome.shell.extensions.dash-to-dock click-action
