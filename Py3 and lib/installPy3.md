The verson of python I used here is 3.x.x
I recommend to use it than 2.x.x because It is a most verson which many data science use.


Step 1 — Update and Upgrade

Logged into your Ubuntu 18.04 server as a sudo non-root user, first update and upgrade your system to ensure that your shipped version of Python 3 is up-to-date.

    $   sudo apt update
    $   sudo apt -y upgrade

Confirm installation if prompted to do so.
Step 2 — Check Version of Python

Check which version of Python 3 is installed by typing:

    $   python3 -V

You’ll receive output similar to the following, depending on when you have updated your system.

Output
Python 3.6.5

Step 3 — Install pip

To manage software packages for Python, install pip, a tool that will install and manage libraries or modules to use in your projects.

    $   sudo apt install -y python3-pip
    or
    $ sudo apt-get -y install python3-pip
    or
    $ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py python3 get-pip.py --force-reinstall

Python packages can be installed by typing:

    pip3 install package_name

Here, package_name can refer to any Python package or library, such as Django for web development or NumPy for scientific computing. So if you would like to install NumPy, you can do so with the command pip3 install numpy.

Step 4 — Install Additional Tools

There are a few more packages and development tools to install to ensure that we have a robust set-up for our programming environment:

    sudo apt install build-essential libssl-dev libffi-dev python3-dev

Step 5 — Install venv

Virtual environments enable you to have an isolated space on your server for Python projects. We’ll use venv, part of the standard Python 3 library, which we can install by typing:

    sudo apt install -y python3-venv

Step 6 — CSetting Up a Virtual Environment

Virtual environments enable you to have an isolated space on your server for Python projects, ensuring that each of your projects can have its own set of dependencies that won’t disrupt any of your other projects.

Setting up a programming environment provides us with greater control over our Python projects and over how different versions of packages are handled. This is especially important when working with third-party packages.
You can set up as many Python programming environments as you want. Each environment is basically a directory or folder on your server that has a few scripts in it to make it act as an environment.

With this installed, we are ready to create environments. Let’s either choose which directory we would like to put our Python programming environments in, or create a new directory with mkdir, as in:

    $   mkdir environments
    $   cd environments

Once you are in the directory where you would like the environments to live, you can create an environment by running the following command:

    $   python3.6 -m venv my_env

Essentially, pyvenv sets up a new directory that contains a few items which we can view with the ls command:

    $   ls my_env

    Output
    bin include lib lib64 pyvenv.cfg share

Together, these files work to make sure that your projects are isolated from the broader context of your local machine, so that system files and project files don’t mix. This is good practice for version control and to ensure that each of your projects has access to the particular packages that it needs. Python Wheels, a built-package format for Python that can speed up your software production by reducing the number of times you need to compile, will be in the Ubuntu 18.04 share directory.

To use this environment, you need to activate it, which you can achieve by typing the following command that calls the activate script:

    $   source my_env/bin/activate

Your command prompt will now be prefixed with the name of your environment, in this case it is called my_env. Depending on what version of Debian Linux you are running, your prefix may appear somewhat differently, but the name of your environment in parentheses should be the first thing you see on your line:

    (my_env) xxx@ubuntu:~/environments$

This prefix lets us know that the environment my_env is currently active, meaning that when we create programs here they will use only this particular environment’s settings and packages.

Note: Within the virtual environment, you can use the command python instead of python3, and pip instead of pip3 if you would prefer. If you use Python 3 on your machine outside of an environment, you will need to use the python3 and pip3 commands exclusively.

After following these steps, your virtual environment is ready to use.

Step 8 — Test Virtual Environment

Open the Python interpreter:

    (my_env) xxx@ubuntu:~/environments$ python

Note that within the Python 3 virtual environment, you can use the command python instead of python3, and pip instead of pip3.

You’ll know you’re in the interpreter when you receive the following output:

    Python 3.6.5 (default, Apr  1 2018, 05:46:30) 
    [GCC 7.3.0] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 

Now, use the print() function to create the traditional Hello, World program:

    >>> print("Hello, World!")

    Output
    Hello, World!

Step 9 — Deactivate Virtual Environment

Quit the Python interpreter:

    >>> quit()

Then exit the virtual environment:

    (my_env) xxx@ubuntu:~/environments$ deactivate
