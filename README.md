# MMM-DailyBibleVerse
This an extension for the [MagicMirror](https://github.com/MichMich/MagicMirror). It will display the verse of the day from www.biblegateway.com. You can change the version of the verse of the day in the config file. Here is a list of the supported Bible versions: https://www.biblegateway.com/versions/
***Forked from arthurgarzajr/MMM-DailyBibleVerse to make text options**

## Installation
1. Navigate into your MagicMirror's `modules` folder 
2. Execute `git clone https://github.com/arthurgarzajr/MMM-DailyBibleVerse.git`
3. Navigate to newly created folder `MMM-DailyBibleVerse`
4. Execute `npm install`

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
	{
		module: 'MMM-DailyBibleVerse',
		position: 'bottom_bar',	// This can be any of the regions. Best result is in the bottom_bar as verses can take multiple lines in a day.
		config: {
			version: 'NIV', // This can be changed to any version you want that is offered by Bible Gateway. For a list, go here: https://www.biblegateway.com/versions/,
	    	size: 'small' // default value is medium, but can be changed. 
			 /* ADDED Settings for Text Color and Text alignmnet to allow for more flexibility and visibility.
			 textColor: "green",
			 textAlignment: "center"
		}
	}
]
````

## Configuration options

The following properties can be configured:


<table width="100%">
	<!-- why, markdown... -->
	<thead>
		<tr>
			<th>Option</th>
			<th width="100%">Description</th>
		</tr>
	<thead>
	<tbody>
		<tr>
			<td><code>version</code></td>
			<td>Here is a list of the supported Bible versions: https://www.biblegateway.com/versions/
      		<br/>
			Note that <code>version</code> also determines the language of the Bible verse. The language of the Bible reference, i.e. name of the book, is determined by the global <code>language</code> parameter in your config 
			<br/>
      		Examples: <code>ESV</code>, <code>NIV</code>, <code>RV1960</code>, etc.
			</td>
		</tr>
		<tr>
			<td><code>size</code></td>
			<td>Default size is medium but it can be overriden with <code>xsmall</code>, <code>small</code> or <code>large</code>.</td>
		</tr>
		<tr>
			<td><code>textColor</code></td>
			<td>Set the text color you desire.</td>
		</tr>
		<tr>
			<td><code>textAligment</code></td>
			<td>Set how you want the text aligned on the screen. Left, Center, Right</td>
		</tr>
	</tbody>
</table>

## Dependencies
- Access to the internet to download verse of the day from www.biblegateway.com.
- npm package `request`

The MIT License (MIT)
=====================

Copyright © 2016-2017 Arthur Garza

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the “Software”), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

**The software is provided “as is”, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.**
