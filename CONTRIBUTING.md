# web-video-canvas Build Setup

[Grunt](http://gruntjs.com/) is used for building, including concatenating, minimizing, documenting, and linting.

### Install Grunt and its Dependencies

#### Ubuntu 14.04

1. Install Node.js and its package manager, NPM

- `sudo apt-get install nodejs npm`
- `sudo ln -s /usr/bin/nodejs /usr/bin/node`

2. Install Grunt

- `sudo npm install -g grunt-cli`
- `sudo rm -rf ~/.npm ~/tmp`

3. Install the Grunt tasks specific to this project

- `cd /path/to/web-video-canvas/`
- `npm install .`

4. (Optional) To generate the documentation, you'll need to setup Java. Documentation generation is not required for patches.

- `echo "export JAVA_HOME=/usr/lib/jvm/default-java/jre" >> ~/.bashrc`
- `source ~/.bashrc`

#### Ubuntu 12.04

1. Install Node.js and its package manager, NPM

- `sudo apt-get install python-software-properties`
- `sudo add-apt-repository ppa:chris-lea/node.js`
- `sudo apt-get update && sudo apt-get install nodejs phantomjs`

2. Install Grunt

- `sudo npm install -g grunt-cli`
- `sudo rm -rf ~/.npm ~/tmp`

3. Install the Grunt tasks specific to this project

- `cd /path/to/mjpegcanvasjs/`
- `npm install .`

4. (Optional) To generate the documentation, you'll need to setup Java. Documentation generation is not required for patches.

- `echo "export JAVA_HOME=/usr/lib/jvm/default-java/jre" >> ~/.bashrc`
- `source ~/.bashrc`

#### OS X

1. Install Node.js and its package manager, NPM

- Go to [Node.js Downloads](http://nodejs.org/download/)
- Download and install the Universal pkg file.

2. Install Grunt

- `sudo npm install -g grunt-cli`

3. Install the Grunt tasks specific to this project

- `cd /path/to/web-video-canvas/`
- `npm install .`

### Build with Grunt

Before proceeding, please confirm you have installed the dependencies above.

To run the build tasks:

1. `cd /path/to/web-video-canvas/`
2. `grunt build`

`grunt build` will concatenate and minimize the files under src and replace ros2d.js and ros2d.min.js in the build directory. It will also run the linter and test cases. This is what [Travis CI](https://app.travis-ci.com/github/Techming/web-video-canvas) runs when a Pull Request is submitted.

`grunt dev` will watch for any changes to any of the src/ files and automatically concatenate and minimize the files. This is ideal for those developing as you should only have to run `grunt dev` once.

`grunt doc` will rebuild all JSDoc for the project.
