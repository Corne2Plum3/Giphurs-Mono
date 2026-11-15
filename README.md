# Giphurs-Mono

> [!WARNING]
> This repo currently contains very early prototypes of the font. Huge changes might occurs. You should not use it in production.

[Giphurs](https://github.com/Corne2Plum3/Giphurs) font but monospaced.

Better description TODO.

## 0. Requirements

Before going further, you're going to need these installed on your system to compile the font and create the images.

Mandatory:

* [Python 3.13](https://www.python.org/downloads/) (other version not tested).
* [pip](https://pypi.org/project/pip/) to install the Python packages (see below).

Optional(-ish):

* [fontspector](https://github.com/fonttools/fontspector/blob/main/INSTALLATION.md) for testing the font.
	* Or use the [web-based version](https://fonttools.github.io/fontspector/)
* [inkscape](https://inkscape.org/) that can be accessed through command line to generate images of the font.
	* Otherwise something else that can convert SVG to PNG with font features support

And of course a font editor with support of [Unified Font Object](https://unifiedfontobject.org/) version 3 if you want to change the font. [FontForge](https://fontforge.org/en-US/) is highly recommended as this is the editor used to create the font.

## 1. Setup

Everything that you will need will be installed on a virtual environment (so Debian/Ubuntu won't complain about it because of the Python packages). So in this section you will make a virtual environment and add the dependencies inside.

> [!NOTE]
> The following guide has been tested on Linux only (Debian/Ubuntu).

1. Ensure that the current working directory is the root of the project. If not, run the following command, replacing `path/to/the/folder/project` by the path of the directory of the project, basically where the file you're reading right now is in.
	```sh
	cd path/to/the/folder/project
	```

2. Create a python virtual environment. To do so, execute:
	```sh
	python3 -m venv venv
	```

3. Move to the virtual environment you just have created:
	```sh
	source venv/bin/activate 
	```

4. Now we're installing the  Python packages. All of them are listed in the `requirements.txt`. To install all of them with the correct version, run the following command:
	```sh
	pip install -r requirements.txt
	```

## 2. Build the font

Once all dependencies are ready, you can build the fonts using the following command (add `-B` if you want to build the font and that it says that "fonts" is already up to date):
```sh
make clean && make clean_fonts
make build
```

> [!NOTE]
> Run the first command if this isn't the first time you are compiling the font. Sometimes the font binaries aren't updates (and we don't know why...)

More commands are listed in the Makefile. Just run `make help` to get the list of commands.


# License

This font is under the [SIL Open Font License, Version 1.1](https://scripts.sil.org/OFL).