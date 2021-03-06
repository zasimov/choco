﻿<!-- This file is automatically generated based on output from https://github.com/chocolatey/choco/tree/stable/src/chocolatey/infrastructure.app/commands/ChocolateyDownloadCommand.cs using https://github.com/chocolatey/choco/tree/stable/GenerateDocs.ps1. Contributions are welcome at the original location(s). If the file is not found, it is not part of the open source edition of Chocolatey or the name of the file is different. --> 

# Download Command (choco download)

Package Internalizer

[Chocolatey for Business](https://chocolatey.org/compare) starting at licensed version 1.5.0.

Downloads a package from a source, optionally downloading remote 
 resources and recompiling the package to use internal resources. This 
 takes an existing package and makes it available without any internet 
 requirement.

See https://chocolatey.org/docs/features-automatically-recompile-packages

Package Copy / Package Downloader
[Chocolatey Professional](https://chocolatey.org/compare) and up starting in version 1.7.1.

Downloads a package from a source and unpacks it. 

## Usage

    choco download <pkg> [<options/switches>]

## Examples

    choco download sysinternals

    #### [Chocolatey for Business](https://chocolatey.org/compare) only
    choco download notepadplusplus.install --internalize
    choco download notepadplusplus.install --internalize --resources-location \\server\share
    choco download notepadplusplus.install --internalize --resources-location http://somewhere/internal --append-useoriginallocation

## See It In Action

Coming soon

## Options and Switches

**NOTE:** Options and switches apply to all items passed, so if you are
 running a command like install that allows installing multiple
 packages, and you use `--version=1.0.0`, it is going to look for and
 try to install version 1.0.0 of every package passed. So please split
 out multiple package calls when wanting to pass specific options.

Includes [[default options/switches|CommandsReference#default-options-and-switches]] (included below for completeness).

~~~

 downloading multiple packages, and you use `--version=1.0.0`, it is
 going to look for and try to download version 1.0.0 of every package


 -?, --help, -h
     Prints out the help menu.

 -d, --debug
     Debug - Show debug messaging.

 -v, --verbose
     Verbose - Show verbose messaging.

     --acceptlicense, --accept-license
     AcceptLicense - Accept license dialogs automatically. Reserved for 
       future use.

 -y, --yes, --confirm
     Confirm all prompts - Chooses affirmative answer instead of prompting. 
       Implies --accept-license

 -f, --force
     Force - force the behavior. Do not use force during normal operation - 
       it subverts some of the smart behavior for commands.

     --noop, --whatif, --what-if
     NoOp / WhatIf - Don't actually do anything.

 -r, --limitoutput, --limit-output
     LimitOutput - Limit the output to essential information

     --timeout, --execution-timeout=VALUE
     CommandExecutionTimeout (in seconds) - The time to allow a command to 
       finish before timing out. Overrides the default execution timeout in the 
       configuration of 2700 seconds.

 -c, --cache, --cachelocation, --cache-location=VALUE
     CacheLocation - Location for download cache, defaults to %TEMP% or value 
       in chocolatey.config file.

     --allowunofficial, --allow-unofficial, --allowunofficialbuild, --allow-unofficial-build
     AllowUnofficialBuild - When not using the official build you must set 
       this flag for choco to continue.

     --failstderr, --failonstderr, --fail-on-stderr, --fail-on-standard-error, --fail-on-error-output
     FailOnStandardError - Fail on standard error output (stderr), typically 
       received when running external commands during install providers. This 
       overrides the feature failOnStandardError.

     --use-system-powershell
     UseSystemPowerShell - Execute PowerShell using an external process 
       instead of the built-in PowerShell host. Should only be used when 
       internal host is failing. Available in 0.9.10+.

 -s, --source=VALUE
     Source - The source to find the package(s) to download. Defaults to 
       default feeds.

     --version=VALUE
     Version - A specific version to download. Defaults to unspecified.

     --pre, --prerelease
     Prerelease - Include Prereleases? Defaults to false.

 -u, --user=VALUE
     User - used with authenticated feeds. Defaults to empty.

 -p, --password=VALUE
     Password - the user's password to the source. Defaults to empty.

     --cert=VALUE
     Client certificate - PFX pathname for an x509 authenticated feeds. 
       Defaults to empty.

     --cp, --certpassword=VALUE
     Certificate Password - the client certificate's password to the source. 
       Defaults to empty.

     --outputdirectory=VALUE
     OutputDirectory - Specifies the directory for the downloaded Chocolatey 
       package file. If not specified, uses the current directory.

     --recompile, --internalize
     Recompile / Internalize - Download all external resources and recompile 
       the package to use the local resources instead.

     --resources-location=VALUE
     Resources Location - When recompiling, use this location for resources 
       instead of embedding the downloaded resources into the package.

     --append-useoriginallocation, --append-use-original-location
     Append -UseOriginalLocation - When `Install-ChocolateyPackage` is 
       internalized, append the `-UseOriginalLocation` parameter to the 
       function. Business editions only (licensed version 1.7.0+). Requires at 
       least Chocolatey v0.10.1 for `Install-ChocolateyPacakge` to recognize 
       the switch appropriately. Overrides the feature 
       'internalizeAppendUseOriginalLocation' set to by default to 'False'.

~~~

[[Command Reference|CommandsReference]]


***NOTE:*** This documentation has been automatically generated from `choco download -h`. 

