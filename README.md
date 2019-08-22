# Anaconda (conda)

What is Anaconda
------
* > Anaconda is a free and open-source distribution of the Python and R programming languages for scientific computing and to simplify package management and deployment.
* > Package versions are managed by the package management system conda

What is Conda
------
* > Conda is a cross platform package and environment manager that install and manages conda packages from the Anaconda repository as well as from the Anaconda Cloud. 
* > Conda packages are binaries. There is never a need to have compilers available to install them. Additionally conda packages are not limited to Python software. They may also contain C or C++ libraries, R packages or any other software.<br/>
* > conda has the ability to create isolated environments that can contain different versions of Python and/or the packages installed in them. This can be extremely useful when working with data science tools as different tools may contain conflicting requirements which could prevent them all being installed into a single environment<br/>
* > conda uses a satisfiability (SAT) solver to verify that all requirements of all packages installed in an environment are met. This check can take extra time but helps prevent the creation of broken environments. As long as package metadata about dependencies is correct, conda will predictably produce working environments
* > Over 1,500 packages are available in the Anaconda repository, including the most popular data science, machine learning, and AI frameworks.
* > Conda also combined with PIP since 150,000 packages available on PyPI. Sometimes a package is needed which is not available as a conda package but is available on PyPI and can be installed with pip

Difference between PIP and Conda
------
* > pip is a package manager that facilitates installation, upgrade, and uninstallation of python packages. It also works with virtual python environments.
* > conda is a package manager for any software (installation, upgrade and uninstallation). It also works with virtual system environments.
* > Pip is specific for Python packages and conda is language-agnostic, which means we can use conda to manage packages from any language Pip compiles from source and conda installs binaries, removing the burden of compilation
* > Conda creates language-agnostic environments natively whereas pip relies on virtualenv to manage only Python environments Though it is recommended to always use conda packages, conda also includes pip, so you don’t have to choose between the two. For example, to install a python package that does not have a conda package, but is available through pip, just run conda command and it will fetch package from PyPI

Anaconda (conda CLI) useful commands
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
