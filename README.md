
 # How to start coding
 ![unisonlogo](https://i.imgur.com/k01Cmyr.png)



## _An unnoficial guide_
#### _made my beginners for beginners._


First let's install Atom, which is the IDE we are going to use.
Then let's add the color sintax for the language, and finally let's download the base library and run the tests.
Run this script to do all these things at once!

```bash

CURRENTDIR=$PWD

WORKDIR=/tmp/unison
mkdir $WORKDIR
cd WORKDIR

echo "Installing ATOM IDE..."
sudo add-apt-repository ppa:webupd8team/atom
sudo apt-get update
sudo apt-get install atom
echo "Successfully installed ATOM IDE on your computer. Try atom to test it."

echo "Installing UNISON..."
RELEASE=https://github.com/unisonweb/unison/releases/download/release%2FM1d/unison-linux64.tar.gz  &&
curl -L $RELEASE | tar -x -z  &&
sudo mv ucm /usr/bin/ &&
echo "Successfully installed UNISON on your computer. Try ucm to test it."

git clone https://github.com/unisonweb/unison &&
cd unison/editor-support/atom/language-unison/ &&
apm link &&
cd -


ucm
pull https://github.com/unisonweb/base .base
test
execute !helloWorld

```
# Examples
- Let's make a **wordcounter**!
	- /examples/helloWorld0 Say hello
	- /examples/helloWorld1 Make your first function
	- /examples/helloWorld2 Read a file
	- /examples/helloWorld3 Split words by separator
	- /examples/helloWorld4 Read a file and count its words
