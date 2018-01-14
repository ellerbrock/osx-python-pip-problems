![python pip pipenv mac](./img/osx-python-pip.jpg)

# Fix for problems with Python and pip 
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg)](https://github.com/ellerbrock/open-source-badges/) [![Gitter Chat](https://badges.gitter.im/frapsoft/frapsoft.svg)](https://gitter.im/frapsoft/frapsoft/) [![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)

## Problem

Today i run in some weird issues installing some tools that after the dependencies where installed the i got error messages that they would not be there. Running direct the Python Shell showed me that its working fine.

After a bit research i found out that Mac have an own Python version and stuff get then mixed up with the version from homebrew. Thought beeing smart and drop an alias got it did not solve the problem since mostly run in the scripts via Shebang.

The fix is to install a tool called `pipenv` for isolationg them from each other (similar like `nvm` for Node.js).

To see how many Python versions are installed run `type -a python`.


## Let's fix it

### Install pipenv

`pip install --user pipenv` 

### Update PATH Variable

Add this folder before $PATH
`echo "$(python -m site --user-base)/bin"`



## How to use it

### Go to your Folder

`cd myproject`

### Install request

`pipenv install requests`

*remember to use always pipenv instead of pip from now!*

### Execute the App

Starting it like before e.g. `./app.py` won't work, you have to run it as well with
`pipenv run python app.py`

Thats it.

Hope i can save others in the future with this tipps some time.


## Contact

[![Github](https://github.frapsoft.com/social/github.png)](https://github.com/ellerbrock/)[![Docker](https://github.frapsoft.com/social/docker.png)](https://hub.docker.com/u/ellerbrock/)[![npm](https://github.frapsoft.com/social/npm.png)](https://www.npmjs.com/~ellerbrock)[![Twitter](https://github.frapsoft.com/social/twitter.png)](https://twitter.com/frapsoft/)[![Facebook](https://github.frapsoft.com/social/facebook.png)](https://www.facebook.com/frapsoft/)[![Google+](https://github.frapsoft.com/social/google-plus.png)](https://plus.google.com/116540931335841862774)[![Gitter](https://github.frapsoft.com/social/gitter.png)](https://gitter.im/frapsoft/frapsoft/)

## License 

[![MIT license](https://badges.frapsoft.com/os/mit/mit-125x28.png?v=103)](https://opensource.org/licenses/mit-license.php)

This work by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/ellerbrock" property="cc:attributionName" rel="cc:attributionURL">Maik Ellerbrock</a> is licensed under a <a rel="license" href="https://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a> and the underlying source code is licensed under the <a rel="license" href="https://opensource.org/licenses/mit-license.php">MIT license</a>.
