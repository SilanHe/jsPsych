![logo](http://www.jspsych.org/img/jspsych-logo.jpg)

jsPsych is a JavaScript library for creating behavioral experiments that run in a web browser. jsPsych provides a framework for defining experiments using a set of flexible plugins that create different kinds of tasks a subject could complete during an experiment. By assembling these different plugins together it is possible to create many different types of experiments.

Examples
----------

Several example experiments and plugin demonstrations are available in the `/examples` folder.

Documentation
-------------

Documentation is available at [docs.jspsych.org](http://docs.jspsych.org).

Need help?
----------

For questions about using the library, please use the [Discussions forum](https://github.com/jspsych/jsPsych/discussions).

Contributing
------------

Contributions to the code are welcome. Please use the [Issue tracker system](https://github.com/jodeleeuw/jsPsych/issues) to report bugs or discuss suggestions for new features and improvements. If you would like to contribute code, [submit a Pull request](https://help.github.com/articles/using-pull-requests).

Citation
--------

If you use this library in academic work, please cite the [paper that describes jsPsych](http://link.springer.com/article/10.3758%2Fs13428-014-0458-y):

de Leeuw, J.R. (2015). jsPsych: A JavaScript library for creating behavioral experiments in a Web browser. *Behavior Research Methods*, _47_(1), 1-12. doi:10.3758/s13428-014-0458-y

Response times
--------------

Wondering if jsPsych can be used for research that depends on accurate response time measurement? For most purposes, the answer is yes. Response time measurements in jsPsych (and JavaScript in general) are comparable to those taken in standard lab software like Psychophysics Toolbox and E-Prime. Response times measured in JavaScript tend to be a little bit longer (10-40ms), but have similar variance. See the following references for extensive work on this topic.

* [de Leeuw, J. R., & Motz, B. A. (2016). Psychophysics in a Web browser? Comparing response times collected with JavaScript and Psychophysics Toolbox in a visual search task. *Behavior Research Methods*, *48*(1), 1-12.](http://link.springer.com/article/10.3758%2Fs13428-015-0567-2)
* [Hilbig, B. E. (2016). Reaction time effects in lab- versus web-based research: Experimental evidence. *Behavior Research Methods*, *48*(4), 1718-1724.](http://dx.doi.org/10.3758/s13428-015-0678-9)
* [Pinet, S., Zielinski, C., Mathôt, S. et al. (2017). Measuring sequences of keystrokes with jsPsych: Reliability of response times and interkeystroke intervals.  *Behavior Research Methods*, *49*(3), 1163-1176.](http://link.springer.com/article/10.3758/s13428-016-0776-3)
* [Reimers, S., & Stewart, N. (2015). Presentation and response time accuracy in Adobe Flash and HTML5/JavaScript Web experiments. *Behavior Research Methods*, *47*(2), 309-327.](http://link.springer.com/article/10.3758%2Fs13428-014-0471-1)


Credits
-------

jsPsych was created by Josh de Leeuw ([@jodeleeuw](https://github.com/jodeleeuw)).

There have been many [contributors](https://github.com/jodeleeuw/jsPsych/blob/master/contributors.md) to the library. Thank you!

jsPsych Bundler
---------------

# jsPsych_bundler
By virtue of its plugin architecture, jsPsych is very extensible. However, since each plugin is 
contained in a separate JavaScript file, downloading a lot of plugins from a web-server can cause
high server load and make your experiment load relatively slowly. The jsPsych_bunder bundles jsPsych 
and a list of plugins into a single file, so that only one JavaScript file needs to be included.

# Installing the bundler
## Clone jsPsych
Clone the jsPsych repository to your hard drive, for example via the [GitHub GUI](https://desktop.github.com/).
## Install Node and NPM
Node and NPM can be downloaded via [this link](https://nodejs.org/en/).
## Download required files from this repo
From this repo, download <a href="https://raw.githubusercontent.com/tpronk/jsPsych_bundler/master/plugins.json" download>plugins.json</a> and <a href="https://raw.githubusercontent.com/tpronk/jsPsych_bundler/master/webpack.config.js" download>webpack.config.js</a>. Put these files in the directory where you cloned jsPsych.
## Go to the jsPsych directory
Open a command prompt and go to the directory on your hard drive where you cloned the jsPsych repository.
## Install webpack and webpack-cli
In the command prompt, run the following two statements:
```
npm install webpack
```
```
npm install webpack-cli
```
Now you're set to go!

# Configuring the bundler
The file **plugins.json** contains a JSON array with plugins you'd like to bundle with jsPsych. Put the plugins your experiment requires in this file.

# Running the bundler
Run the statement below to make a file **jspsych.bundle.js**. This file will contain jsPsych and the plugins you've listed in **plugins.json**.
```
webpack
```