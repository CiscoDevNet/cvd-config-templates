# Mac OS X Setup

1. Install git. This can be done via typing `git` at a terminal and installing Xcode Developer Tools, or from [git-scm.com](http://git-scm.com)

2. Install the [Homebrew](brew.sh) Package Manager.  

    ```bash
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

3. Install `wget` with Homebrew. 

    ```bash
    brew install wget
    ```

4. Install Python 3 via Homebrew. (Note: Python 3 is currently the default version provided by homebrew.)

    ```bash
    brew install python
    ```

5. Install Python utilities. 

    ```bash
    # Retrieve pip installation script from web
    wget https://bootstrap.pypa.io/get-pip.py
    
    # Install pip into default Python installation 
    sudo -H python get-pip.py 
    
    # Install Virtual Environment with pip 
    sudo -H python -m pip install virtualenv 
    ```

6. Move to your working directory. (This is an example directory; use your local directory structure.)
    ```bash
    cd ~/Code/cvd-config-templates
    ```

7. Setup a Python Virtual Environment.

    ```bash
    virtualenv venv
    source venv/bin/activate 
    ```

8. Create a requirements list. 

    ```bash
    echo 'ansible==2.4.2.0
    ncclient==0.5.3
    requests==2.18.4' > requirements.txt
    ```

9. Install Ansible requirements.

    ```bash
    pip install -r requirements.txt 
    ```

