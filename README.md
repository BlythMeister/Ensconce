Ensconce
========

en·sconce/en'skäns/
Verb:
Establish or settle (someone) in a comfortable, safe, or secret place

![GitHub release (latest by date)](https://img.shields.io/github/v/release/15below/Ensconce)
![GitHub all releases](https://img.shields.io/github/downloads/15below/Ensconce/total)
![Nuget](https://img.shields.io/nuget/v/Ensconce.DotNetTool)
![Nuget](https://img.shields.io/nuget/dt/Ensconce.DotNetTool)


What is this?
-------------

A .net command line tool for aiding deployment of server components.

* Update configuration files and other XML
* Initialise/update related databases
* Render arbitrary text files with environment specific variables
* Move the updated files to their final locations on disk
* Cope with multiple instances of the same component
* Deploy SSRS reports

Deploying A Release
-------------------

Each release contains a nuget package which is an [Octopus](https://octopus.com/) deployment package.

There are 3 required variables, these are:

* DeployPath - set to the folder you want to deploy Ensconce too
* IncludeK8s - set to `True` or `False` depending on if you want Kubernetes deployments
* VersionNumber - set as `#{Octopus.Release.Number}` in order to get the right version number

How do I use it?
----------------

* Get a copy of your component with default configuration to the target server (at 15below we use [Octopus](https://octopus.com/))
* Set up your environment; Ensconce expects one of the following environment variables sets to exist:
	* ClientCode
	* Environment
	* DeployService
* OR
	* FixedStructure = true
* Run Ensconce:
	d:\DeployTools\Ensconce.Console.exe -replace -deployFrom . -deployTo c:\targetDir -updateConfig
* Stuff happens: check the [wiki](https://github.com/15below/Ensconce/wiki) for details

NDjango Usage Notes
----------------

NDjango has been taken from https://github.com/Hill30/NDjango

This repo is no longer maintained and the nuget packages are out of date.

When taken the last commit was: https://github.com/Hill30/NDjango/commit/7dc7a0260489c76f7197dcfb69c1105f8a4c6ab8

Once inside Ensconce, the namespace were updated and code refactored and made to work with the latest frameworks
