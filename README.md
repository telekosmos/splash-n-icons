# Splash'n'Icons

__splash'n'icons__ combine together to get you rid of the concern of resources/assets generation for a Cordova/Phonegap project.
Strongly based, inspired and forked from [phonegap-res](https://github.com/macdonaldr93/phonegap-res) :+1:

## Features
- Automatic splash screen & icon generator for PhoneGap/Cordova 5+.
- Update `config.xml` file with the markup for the generated resources and platforms.
- Create the `icon` and `splash` folders into the `resources/<platform>` folder for the right platforms if they don't exist.
- Use `resize` or `crop` methods (default is `crop`, `-r`, `--resize` changes this)

## Requirements
- Create a splash screen (`splash.png` 2048x2048) & icon (`icon.png` 1024x1024) in the `resources` folder of your phonegap/cordova project
- Create root resources folder for the platforms your project supports (this is `resouces/ios` and/or `resources/android`; necessary nowadays, see below)
- Cordova's `config.xml` file must exist in the root folder
- use `splash-n-icons generate` command to automatically crop and copy it for all the platforms your project supports (currenty works with iOS and Android).
- No need to have a platform installed in your project


## Installation

    sudo npm install -g splash-n-icons

## Quick usage

Create a ```splash.png``` & ```icon.png``` file in the `resources` folder of your phonegap/cordova project and run:

    splash-n-icons generate

## Usage

    splash-n-icons [options]

    Comands:
    generate  Generate assets for platforms iOS/Android

    Options:
    --resize, -r          Use imagemagick resize method instead crop     [boolean]
    --ignorePlaforms, -i  Do not check platforms and generate assets anyway
    --iconfile            The name of the icon file in the resources directory [string]
    --splashfile          The name of the splash icon file in the resources directory [string]
    -h, --help            Show help                                  [boolean]

    Examples:
    splash-n-icons generate  Generate the assets

### Third party requirements

- ImageMagick

Install on a Mac using `homebrew`:

    brew update
    brew install imagemagick
or using `ports`:
	
	port selfupdate
	port install imagemagick
	
### License

MIT

### Future?
- Generate icons __or__ splash screens
- Generate `android` and/or `ios` resource directories
- Add more tests.
