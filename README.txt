
https://medium.com/@joel.barmettler/how-to-upload-your-python-package-to-pypi-65edc5fe9c56

#make you code publis-ready

no print statement, instead you can use logging module

everyting is in the classs. If you want to include the test code. put them in the following if statement
if __name__ =="__main__":

#create a python package

create a package (folder name, __init__.py, module files)

in the __init__.py

from MyLib.file import classA


MyLib

#create necessary files
setup.py
setup.cfg
LICENSE.txt
README.md

your package is called MyLib. MyLib is a folder. Inside the folder

MyLib
    __init__.py
    File1.py
    File1.py

File1.py File2.py are module files.

#create a PyPi account

#upload your package to github.com

release git repo of your pacakge. (operate in github.com)

#create the distribution

python setup.py sdist

#upload the distribution

twine upload dist/*

sometimes, you will find it does not upload successfully. Usually it is because you use the project name which is not allowed in the pypi. For example, I first use pypidemo as package name, it does not allow me upload. After I change it to asfpypidemo, it works.

#check if you upload you package successfully.

pip install asfpypidemo

OK!


