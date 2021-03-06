SEMAT Accelerator
=================
SEMAT Accelerator (a.k.a. SematAcc) is a web positioning system for [SEMAT](http://semat.org) Essence Theory of Software Engineering.

SematAcc is a response to the lack of practicability of the Essence Theory of Software Engineering. It provides practical ways to learn the Essence theory, as it enables a web positioning system to represent a software system status using Essence Kernel (currently, only the Concerns, Alphas and the States are supported).

The tool itself serves for multiple use cases.
In short, it is an awareness creator, self-positioning system, discussion generator as well as visualization of your project’s current state.
SematAcc was also developed with research in mind. It enables research on Essence by logging the events on each State change.
It might be employed as a valuable tool for controlled experiments and case studies.

The [S4FS Research team](http://www.inf.unibz.it/s4fs/) at the Free University of Bozen-Bolzano released SematAcc as OSS and certainly invite those interested in continuing developing it further to join the excitement.


ESSENCE THEORY OF SOFTWARE ENGINEERING
======================================
SEMAT Essence Theory of Software Engineering [aims to](http://semat.org/?page_id=2):

    Refound software engineering based on a solid theory, proven principles and best practices that:
    -Include a kernel of widely-agreed elements, extensible for specific uses
    -Addresses both technology and people issues
    -Are supported by industry, academia, researchers and users
    -Support extension in the face of changing requirements and technology

A simple introduction to the Essence theory can be found in the materials
of [a special lecture](http://task3.cc/1328/special-lecture-on-semat-essence-of-software-engineering/) held at the Free University of Bozen-Bolzano.
Useful references to complete materials are available there, as well.

BEFORE YOU START
================
We use Google Analytics to analyze sematacc.herokuapp.com traffic.
If you want to use it, too, please set the `ganalaytics` variable to your tracking code (in the form of 'XX-XXXXXXX-X').
The variable is defined in `client/ganalytics.js`.

DEPENDENCIES
============
SematAcc is a regular [Meteor](http://meteor.com) application and it requires `Meteor v1.3+` as a dependency.
Please refer to [Meteor documentation](http://docs.meteor.com) in order to install it.

Although Microsoft Windows is [unoficially supported](http://win.meteor.com), we advice to try SematAcc either in a GNU/Linux environment or on Mac OS X.

USAGE
=====
SematAcc is a regular [Meteor](http://meteor.com) application and it runs as any other Meteor application.
In order to run SematAcc on a development machine, issue the following command in the root folder of the project:

    meteor

SematAcc should be ready and accessible at http://127.0.0.1:3000.

A live version of SematAcc runs on Meteor servers at http://sematacc.herokuapp.com for demo and testing purposes.
Although we try to keep the data stored on there, please do not heavily rely on it.

In order to [deploy](http://docs.meteor.com/#deploying) SematAcc as a private instance on Meteor's servers, issue the following command:

    meteor deploy your-chosen-name.meteor.com

Please note that Meteor hosting is not free. Free hosting is provided by [Heroku](http://heroku.com), and it is described [here](https://medium.com/@leonardykris/how-to-run-a-meteor-js-application-on-heroku-in-10-steps-7aceb12de234#.tcei2hasi).


CITATION
========

If you use SematAcc in research activities, please cite as follows:

Graziotin, D. and Abrahamsson, P. A Web-based modeling tool for the SEMAT Essence theory of software engineering. Journal of Open Research Software 1, 1 (2013), e4. DOI=http://dx.doi.org/10.5334/jors.ad


EVENT LOGGING
=============
SematAcc logs events. Currently only changes in an alpha's state is recorded.
The events for a project are transparently exportable by the user as a CSV string.
It is straightforward to add other events.
Please see [client/kernel/events.js](https://github.com/s4fs/sematacc/blob/master/client/kernel/events.js) for more.
In particular, the line

    Meteor.call('log', Session.get('selectedProjectId'), alpha.name+'.state', state.name);

Is responsible to log an event.

TESTING
=======
Please look at the file TESTING.md

LICENSE
=======
SematAcc is released under the The BSD 3-Clause License. See the LICENSE file for more details.

CREDITS
================
See CONTRIB.md
