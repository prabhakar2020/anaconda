# Anaconda (conda)
Anaconda (conda) useful commands
-----

> **Check conda version**
>> conda --version

> **Create virtual environment using conda**
>> conda create -n test1 python=3.6 <br/>
>> conda create -n test2 python=2.7  <br/>
>> conda create -n test3 python=2.4  <br/>

Above example we can create 3 virtual environments (test1, test2 & test3) with 3 different python versions
> **update conda package manager**
>> conda update -n base -c defaults conda<br/>
        OR<br/>
>> conda update conda<br/>

> **To activate this environment, use**
>> conda activate test1

Above command will activate **test1** environment
> **To deactivate an active environment, use**
>> conda deactivate

> **To list down all virtual environments of conda**
>> conda env list

> **To remove virtual environments**
>> conda env remove -n ENVIRONMENT_NAME<br/>
>> **eg:** conda env remove -n test1

> **Install packages**
>> conda install flask

Above example, If you do not specify the environment name, which in this example is done by --name myenv, the package installs into the current environment:

> **To install a specific package in existing environment**
>> conda install --name test1 flask

> **To install multiple packages at once**
>> conda install --name test1 flask

> **Remove packages from selected environment**
>> conda remove -n ENV_NAME PACKAGE_NAME<br/>
>> **eg:** conda remove -n test1 flask

> **Remove multiple packages from selected environment**
>> conda remove -n ENV_NAME PKG1 PKG2<br/>
>> **eg:** conda remove -n test1 flask curl

> **Searching for the packages**
>> conda search PKG_NAME<br/>
>> conda search tensorflow

> **To update a specific package**
>> conda update flask

> **To know details about current environment**
>> conda info

> **To know full details about current environment**
>> conda info -a

`Note: Above commands prepared and tested on conda v4.7.11 and anaconda Command line client (version 1.7.2)`
