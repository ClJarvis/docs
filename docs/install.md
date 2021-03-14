# Installation

Here's some various ways to can run the project yourself!

## Docker container

If you want, you can run and develop the application within docker container. To do this, firstly you have to make sure that you have Docker installed and running on you local machine. If you don't, here you can see how to get it. To build the app inside a Docker container, follow the following steps:

1. Firstly, build the Docker image based on the supplied Dockerfile docker build -t cthesaurus-img .
1. Then, run the Docker container by using the image that you've just created docker run --name codethesaurus-container -dti -p 8000:8000 -v `pwd`:/code cthesaurus-img
1. You can check if the container is up and running by invoking docker container ls - your container should be present on the list, its name should be set to "codethesaurus-container".
1. Django development server is run automatically when you run the container - page should be available at http://localhost:8000.
1. You can attach to the container by running docker attach codethesaurus-container - after you attach, you have to stop the development server by CTRL+C key combination. After that, you have access to the command line interface inside the container, where you can invoke django managment commands.
1. To edit the respository, do it in your local directory on your machine - the changes that you make will be reflected in the container, thanks to the mounting of the filesystem, which was specified by -v `pwd`:/code option during docker run ... command execution.

## Manual Install - Windows

1. Clone the project (git clone https://github.com/codethesaurus/codethesaur.us.git)
1. Switch into to directory cd codethesaur.us
1. Check to see if Python 3.x is installed with python --version or python3 --version. If Python 3.x isn't installed, visit https://www.python.org/downloads/windows/ or install it with choco install python
1. Install Python's virtual environment venv with the command pip3 install virtualenv
1. To set up new virtual environment, run virtualenv venv
1. To activate virtual environment, run venv\Scripts\activate.bat
1. Run pip install -r requirements.txt
1. Then Run python manage.py runserver
1. In your browser, visit http://127.0.0.1:8000/ or http://localhost:8000/
1. Press CTRL+C in the terminal to stop the server
1. To deactivate the virtual environment, run venv\Scripts\deactivate.bat

## Manual Install - Mac

1. Check to see if Python 3.x is installed with python --version or python3 --version. If Python 3.x isn't installed, install it with brew install python
1. Clone the project (git clone https://github.com/codethesaurus/codethesaur.us.git)
1. Switch into to directory cd codethesaur.us
1. Run pip3 install virtualenv
1. To set up new virtual environment, run virtualenv --no-site-packages venv
1. To activate virtual environment, run source venv/bin/activate
1. Run pip3 install -r requirements.txt
1. Then Run python3 manage.py runserver
1. In your browser, visit http://127.0.0.1:8000/ or http://localhost:8000/
1. Press CTRL+C in the terminal to stop the server
1. To deactivate the virtual environment, run deactivate

## Manual Install - Linux

1. If python3 and pip3 are not installed there is a guide for Linux systems
1. Check system default python --version If the returned text is not python 3.x then using python3 will be required for following steps Or if you would like to set python3 as a default simply open your .bashrc file. sudo nano ~/.bashrc and add alias python='python3'
1. Django 3.11 can be installed using the pip3 package manager. pip3 install django==3.11
1. Install PostgreSQL sudo apt install -y postgresql - Debian
1. Install venv for virtual environment sudo apt install -y python3-venv - Debian Full python3 and venv setup centOS
1. Clone the project (git clone https://github.com/codethesaurus/codethesaur.us.git)
1. Switch into to directory cd codethesaur.us
1. Use directory as virtual environment python3 -m venv codethesaur.us
1. Activate the directory source codethesaur.us/bin/activate
1. Run pip install -r requirements.txt
1. Then run python manage.py runserver
1. In your browser, visit http://127.0.0.1:8000/ or http://localhost:8000/
1. Press CTRL+C in the terminal to stop the server.
