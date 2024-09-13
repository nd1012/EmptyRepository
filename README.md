# EmptyRepository

This is an empty GIT repository for starting a .NET project. It contains:

- A `LICENSE` file with the MIT license
- An extended `.gitignore` file for Visual Studio
- A `.github` folder with some GitHub configuration and workflow
- A `docs` folder for a docfx generated developer reference
- A `src` folder for the solution source code

## How to start

1. Create an empty GIT repository
2. Download the latest release source code ZIP file
3. Extract the ZIP file contents to your new GIT repository
4. Customize

## Customization

### License

Edit the `LICENSE` file and change the copyright.

### README

Edit the `README.md` file according to your project.

### Create solution

Open Visual Studio and create a new solution with projects in the `src` folder.

The `*.sln` file should be located in the `src` folder directly, while each 
project should be hostet in a sub-folder. The folder name of test projects 
should end with `* Tests`. They'll be ignored in the docfx generated developer 
reference.

### Configure docfx

Open the `src/doxfc Docs/docfx.json` file, customize the copyright and replace 
`PROJECTNAME` with your projects name.

### Alter the `.github` folder files

#### Depandabot

There are no customizations required to the `.github/depandabot.yml` file 
actually. However, if you need changes, you're free to change the file 
contents as required.

#### Workflows

##### CodeQL

Open the `.github/workflows/codeql.yml` file and replace `PROJECTNAME` with 
your projects name. You may add more commands that need to run before the 
CodeQL scan.

##### docfx

Open the `.github/workflows/docfx.yml` file and replace `PROJECTNAME` with 
your projects name.

##### .NET

Open the `.github/workflows/dotnet.yml` file and replace `PROJECTNAME` with 
your projects name. You may add more commands that need to run for the test.

## Initial commit

Now make the initial commit to GitHub. The `Actions` tab will show some failed 
actions, because you'll have to do something more:

### Configure GitHub

There are some things to configure in your GitHub repository:

- Actions need read/write permissions
- Dependabot custom configuration
- CodeQL scanning
- GitHub Pages should use the `docs` folder and refresh on a commit to the 
main branch

## Done!

Now you're done! With your next commit all GitHub actions should run fine, and 
after the docfx workflow ran, you'll have your GitHub Pages content available. 
The docfx workflow will also make an automatic commit to your main branch, if 
the developer reference changed.
