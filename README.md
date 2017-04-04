# Meilix
[![Build Status](https://travis-ci.org/fossasia/meilix.svg?branch=master)](https://travis-ci.org/fossasia/meilix)

Beautiful [lubuntu](http://lubuntu.net) based Linux OS for Hotels and Public Spaces with a system lock.
Features:
* Based on lubuntu
* Light weight
* Fast
* Contains neccessary packages
* PPA synced with github

## Customizing Distribution

- After cloning open build.sh to change. Read comment in build.sh to understand how to change.
(Note: Please not change anything at # Install core packages and do not delete any in hotelos folder).

### Creating a metapackage
Creating a metapackage is really easy, we will make use of [equivs](http://apt.ubuntu.com/p/equivs) to make our metapackage.
- First, install equivs.
- Now run equivs: `equivs-control ns-control`
- It will create a file called ns-control, open this file with your text editor.
- Modify the file to your needs modifying the needy information.
- Then run: `equivs-build ns-control` to build your metapackage, thats all simple and easy.
- To add it to meilix follow adding a metapackage to meilix section.

### Adding a Metapackage to meilix
- Create a metapackage and place it in the root directory of the project
- Add it to the build.sh file
- Install `reprepro` if you don't have it run: `sudo apt-get install reprepro`
- Make sure you are on the meilix repository.
- Run the following command for each meta-package you create: `reprepro includedeb trusty ./nameOfYourMeta-package.deb`

**Note: Remember to replace nameOfYourMeta-package with the name of the meta-package**

## Communication
Chat: [Slack Channel](http://fossasia.slack.com/messages/linux/) | [Get an Invite](http://fossasia-slack.herokuapp.com/)
