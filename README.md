# DbUp Package Manager Console Scripts
Package Manager Console scripts for [DbUp](http://dbup.github.io/).

## Install
This package is hosted on [NuGet](https://www.nuget.org/packages/dbup-consolescripts/).

    Install-Package dbup-consolescripts

Although dbup-consolescripts does not have a dependency on the [dbup](https://www.nuget.org/packages/dbup/) package, it is assumed you are using the following commands against a [DbUp](http://dbup.github.io/) project.  

## Commands
- **New-Migration [Name]** - Creates a new migration .sql file in the \Scripts folder of the current project and marks it as an *Embedded Resource*.  Uses the timestamped name format %y%m%d%H%M%S.sql (i.e. 150411194108.sql for 04/11/2015 7:41:08 PM).  Optionally, specify a [Name] which will be appended to the file name.
- **Start-Migrations** - Runs any pending migrations by building and running the current project.

When this package is installed, the above commands can be run from the Package Manager Console.  **Note: make sure the "Default project" selected in the Package Manager Console is your DbUp project** before running these commands.

## Development

### Release Process
1. Download latest version of [nuget.exe](https://docs.nuget.org/consume/installing-nuget) to \tools folder.
2. From root project folder, run `rake release[1.2.0,"Release notes here..."]`.

