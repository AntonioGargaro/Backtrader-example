# Backtrader-example
How to install and run Backtrader on your local machine.

---

# Setup Pip and Virtual Enviroment for Python3.4

To begin setting up the environment 'cd' in your terminal to the project directory.

```bash
cd to/directory/of/project
```

### Install Pip

For Linux install Pip by,

```bash
python3.4 -m pip install --user --upgrade pip
```

### Install virtualenv

Once Pip is installed you can now install virtualenv.

virtualenv is used to manage Python packages for different projects. Using virtualenv allows you to avoid installing Python packages globally which could break system tools or other projects. You can install virtualenv using pip.

For Linux install virtualenv by,

```bash
python3.4 -m pip install --user virtualenv
```

### Creating your Virtual environment

virtualenv allows you to manage separate package installations for different projects. It essentially allows you to create a “virtual” isolated Python installation and install packages into that virtual installation. When you switch projects, you can simply create a new virtual environment and not have to worry about breaking the packages installed in the other environments. It is always recommended to use a virtualenv while developing Python applications.

To create a virtual environment, go to your project’s directory and run virtualenv.

For Linux create virtualenv by,

```bash
python3.4 -m virtualenv env
```

You should now have a folder 'env' in your local directory.

### Activating your virtualenv

After creating your virtualenv you will then need to 'activate' it. Failing to activate your virtualenv will cause you to use global libraries.
This can cause problems with overwriting dependency versions if you install them globally.

To activate on Linux have a terminal open in the project folder where you created 'env'.

Then run this command for Linux,

```bash
source env/bin/activate
```

You can tell if it activate successfully if your terminal has prefix '(env)'

```bash
(env) jove:~/to/directory/of/project$
```

You can deactivate from the virtualenv by simply running,

```bash
deactivate
```

### Installing Packages to virtualenv

To install libraries to your local library **MAKE SURE** you have **ACTIVATED** your virtualenv. 

Normally Python virtualenvs come with a 'requirements.txt' file which contains all the dependencies for the source code to work.
Hence you can install all the libraries using 'requirements.txt' with the following command,

```bash
pip install -r requirements.txt
```

If this file doesn't exist then for the purpose of this tutorial you can install the dependency 'backtrader' by,

```bash
pip install backtrader
```

Congratulations, your Python virtualenv is setup!