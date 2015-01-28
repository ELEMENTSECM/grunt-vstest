# grunt-vstest

> Run tests using the Visual Studio test runner via Grunt

## Getting Started
This plugin requires Grunt `~0.4.5`. In other words it should work on 0.4.5 or higher.

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-vstest --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-vstest');
```

## The "vstest" task

### Overview
In your project's Gruntfile, add a section named `vstest` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
    vstest: {
        dev: {
            src: ["Example.Tests/bin/Release/*Tests.dll"], // Relative path to test dll(s)
			options: {
				// Listing all currently supported options
				settings: "Local.RunSettings",
				inIsolation: true,
				platform: "x64",
				framework: "framework45", // Valid values are Framework35, Framework40 and Framework45
				testCaseFilter: "TestCategory!=KnownError",
				logger: "trx"
			}
        }
    }
});
```

## Contributing
We appreciate the community submitting issues and pull requests. 

## Issues and installing previous versions

If you have any problems with the latest release please log an issue at https://github.com/GeckoInformasjonssystemerAS/grunt-vstest/issues.

If you need to roll back to an earlier version you can use the following syntax to install a specific version

```
npm install grunt-vstest@0.1.2
```

Also see https://www.npmjs.org/doc/json.html#dependencies for details of how to specify a particular package version in your package.json file

## Release Notes

|Version| Notes|
|-------|------|
|0.0.3|Added support for option logger
|0.0.2|Fixed typo on node version required
|0.0.1|Initial commit allowing you to run tests via grunt using the Visual Studio test runner
