tycho-sample
============
Overview
------------
The project consists of several sub-projects (which should be built in the given order; the parent is not buildable):
* sample.p2-bundle-repository: Builds a p2 repository containing third party dependencies (in this case spring dm).
* sample.feature: Builds an eclipse feature containing dependencies to bundles modified with additional data via a p2.inf file.
* sample.p2-feature-repository: Builds a p2 repository containing the feature and needed bundles.
* sample.plugin: Builds a simple GUI plugin.
* sample.product: Builds the product which consists of the feature and plugin.

Problem
------------
See [Thread on Stackoverflow](http://stackoverflow.com/questions/17855554/installable-units-are-missing-in-p2-repository-so-that-tycho-p2-director-fails).

Error
------------

    Installing sample 1.0.0.201308071227.
    Installation failed.
    Cannot complete the install because one or more required items could not be found.
     Software being installed: sample 1.0.0.201308071227 (sample 1.0.0.201308071227)
     Missing requirement: Sample Feature 1.0.0.201308071203 (sample.feature.feature.group 1.0.0.201308071203) requires
     'configure.org.springframework.osgi.core 0.0.0' but it could not be found 
     Cannot satisfy dependency: 
      From: sample 1.0.0.201308071227 (sample 1.0.0.201308071227)
      To: sample.feature.feature.group [1.0.0.201308071203] 
