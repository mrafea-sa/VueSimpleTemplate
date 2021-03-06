# Vue Simple Template [![Mit License][mit-img]][mit]

This template was created to use vue.js with asp.net core using the [Spa Services](https://github.com/aspnet/JavaScriptServices) library. It aims to be minimalistic with its approach. It also favors Vue's single file component over Typescript, since one of the efforts is to minimize friction when transitioning from a vue-cli project into this template.

## Builds

| Appveyor  |
| :---:     |
| [![Build status][build-img]][build] |

## Packages

| NuGet (Stable) | MyGet (Prerelease) |
| :---: | :---: |
| [![NuGet][nuget-img]][nuget] | [![MyGet][myget-img]][myget] |

## Installation

To install the template, via commandline simply using nuget:

`dotnet new -i "Vue.Simple.Template::*"`

where * is the equivalent of the latest version of the template.

If you would like to tinker with the code locally, you can clone the repository and execute the following command with the dotnet command, using the path of the repo:

`dotnet new -i "$PATH_OF_NUPKG_FILE"`

Once installed as a template you can properly create your own custom projects using the template using the following command:

`dotnet new simplevue -o MyAppName`

It will generate the following folder structure:

``` tree
$
.
├── .editorconfig
├── appsettings.Development.json
├── appsettings.json
├── Program.cs
├── Startup.cs
├── {ProjectName}.csproj
├── /ClientApp
│   ├── package.json
│   ├── package-lock.json
│   ├── babel.config.js
│   ├── /public
│   │    ├── favicon.ico
│   │    └── index.html
│   ├── /src
│   │    ├── store.js
│   │    ├── router.js
│   │    ├── main.js
│   │    ├── app.vue
│   │    ├── /assets
│   │    │    └── logo.png
│   │    ├── /components
│   │    │    └── helloworld.vue
│   │    └── /views
│   │         ├── home.vue
│   │         └── about.vue
│   │
│   └── /node_modules
├── /Controllers
│   └── MainController.cs
└── /Views
    ├── _ViewStart.cshtml
    ├── _ViewImports.cshtml
    └── /Main
         └── Index.cshtml
```

Then proceed to:

``` bash
cd MyAppName
npm install
```

The ClientApp folder includes the default project created using the vue-cli 3.0. You can (optionally) replace the contents of the clientApp folder with your own custom vue project, since this template interacts directly with the vue commands, for building and debugging purposes.

---

## Uninstalling

The syntax for uninstalling from the command line is the following:

`dotnet new -u "Vue.Simple.Template"`

Or

`dotnet new -u "$PATH_OF_NUPKG_FILE"`

### Further info

For More information on how to manage dotnet custom templates see the [docs.microsoft documentation](https://docs.microsoft.com/en-us/dotnet/core/tools/custom-templates).

## Contributing

Check the [contribution guide](https://github.com/Jaxelr/VueSimpleTemplate/blob/master/.github/CONTRIBUTING.md).

[mit-img]: http://img.shields.io/badge/License-MIT-blue.svg
[mit]: https://github.com/Jaxelr/VueSimpleTemplate/blob/master/LICENSE
[build-img]: https://ci.appveyor.com/api/projects/status/vvnkjjckfv6v1dgk?svg=true
[build]: https://ci.appveyor.com/project/Jaxelr/vuetemplate
[nuget-img]: https://img.shields.io/nuget/v/Vue.Simple.Template.svg
[nuget]: https://www.nuget.org/packages/Vue.Simple.Template/
[myget-img]: https://img.shields.io/myget/vue-simple-template/v/Vue.Simple.Template.svg
[myget]: https://www.myget.org/feed/vue-simple-template/package/nuget/Vue.Simple.Template
