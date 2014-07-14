[![Dependency Status](https://gemnasium.com/gaiajs/gaiajs-database.svg)](https://gemnasium.com/gaiajs/gaiajs-database)
[![NPM version](https://badge.fury.io/js/gaiajs-database.svg)](http://badge.fury.io/js/gaiajs-database)
 > Database handler for [GAIAJS](https://github.com/gaiajs/gaiajs) Apps

This module configure all persistences and repositories of gaiajs's apps.

## CONFIGURATION OF PERSISTENCE
All driver have:
 * `name`: name of persistence - Optional when there is one persistence
 * `driver`: name or absolute path of driver
 * `debug`: set driver in debug mode - Optional (default: false)
 * `default`: set this persistence by default - Optional (default: false)
 * `dir`: path of directory of models for this persistence (relative to application model directory)
 * `onRun`: generator function to call when all repositories are loaded and configurated.
 Can be wrapped by injector. - Optional

## GAIAJS Injector
# Persistence
Add all persistence in injector. Use name of persistence.
Default persistence is inject with $persitence.
If there is no persistence by default, the first persistence is the default.

inject name :  camel case name + persistence (ex: name is mysql, inject $mysqlPersistence)

# Repository
Create all repositories for models find.

inject name : camel case relative path + Repository
ex:
 - if path is user.js => inject $userRepository
 - if path is rest/user.js => inject $restUserRepository


## LIST OF DRIVERS
<table>
  <thead>
    <tr>
      <th>Database type</th>
      <th>Package name</th>
      <th>Based on package</th>
      <th>Maintainer</th>
      <th>Build status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Mongodb</td>
      <td><a href="https://github.com/gaiajs/gaiajs-driver-mongoose">gaiajs-driver-mongoose</a></td>
      <td><a href="https://github.com/learnboost/mongoose">Mongoose</a></td>
      <td><a href="https://github.com/eyolas">David Touzet</a></td>
      <td><img src="https://travis-ci.org/gaiajs/gaiajs-driver-mongoose.svg?branch=master" alt="Build Status" /></td>
    </tr>
  </tbody>
</table>

## Authors

  - [David Touzet](https://github.com/eyolas)

# License

The MIT License

Copyright (c) 2014, Touzet David <dtouzet@gmail.com>

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
