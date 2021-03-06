# kicad-libraries
KiCad libraries containing components and footprints used in electronics projects at YO6SSW.

Here's a quick guide of how to use the library in a project:

1. create project repository on github and clone it locally
2. go to the project directory and add the libraries submodule by running `git submodule add http://github.com/benishor/kicad-libraries libraries`
3. create schema and make sure to add the `libraries/yo6ssw` library to the list of existing libraries by opening EESchema and going to Preferences -> Component Libraries -> Add and selecting the path to your project's libraries/yo6ssw.lib file
4. in order to also use the library's footprints, you need to configure PcbNew to know about them. Open PcbNew, go to Preferences -> Footprint Library Wizard -> Files on my computer -> Next -> go to libraries/yo6ssw.pretty and add it to the project

Whenever you need to fetch existing library updates, perform the following in sequence:
- go to the `libraries` subfolder
- run `git pull`. This will update the library to its latest version.
- get back to the project root and inform git that we would really like to use this current version of the library from now on by issueing a `git add libraries` and `git commit` followed by a `git push`
