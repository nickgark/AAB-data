# AAB-data

This is a collection of library data for the Traveller roleplaying game, designed for use with the [AAB plugin for TiddlyWiki](https://github.com/nickgark/AAB). Where appropriate, I've indicated the canon sources from which these entries are drawn (the `sources` field); entries with no listed sources are my own work.

The individual entries (or in TiddlyWiki terms, tiddlers) are in thematic groups, expressed in JSON. The order in which these files are loaded into a TiddlyWiki is important, because some files contain tiddlers which override others; the files are effectively modular chunks of knowledge which can be included to provide more background information to your players.

For example:

* `majorrace.json` defines a tiddler for the Aslan race
    * `aslan.json` expands the Aslan tiddler and adds a number of extra tiddlers that provide more information, including a tiddler about the Aslan language Trokh
        * `trokh.json` contains a list of common words in Trokh

These files should be added to TiddlyWiki in the order given; if they're not, more detailed entries will be overwritten by less detailed. Unfortunately, TiddlyWiki doesn't have a good mechanism for expressing dependencies of this form (unless one wilfully misuses the plugin mechanism), so the following hierarchical list will have to suffice:

* `aab.json`
* `starport.json` - defines starport types used by AAB plugin
* `tradecodes.json` - defines trade codes used by AAB plugin
* `govtype.json` - defines government types used by AAB plugin
* `installations.json` - defines bases/installations used by AAB plugin
* `travel.json` - defines travel codes used by AAB plugin
    * `tas.json`
* `techlevel.json`
    * `technology.json`
* `sophont.json`
    * `majorrace.json` - short entries for each major race
        * `aslan.json`
            * `trokh.json`
        * `droyne.json`
            * `oynprith.json`
        * `hiver.json`
        * `kkree.json`
            * `kee.json`
        * `solomani.json`
        * `vargr.json`
            * `gvegh.json`
        * `vilani.json`
            * `svilani.json`
        * `zhodani.json`
            * `zdetl.json`
    * `minorrace.json` - entries for minor races (many stubs)
* `astrography.json`
    * `mains.json`
    * `clusters.json`
    * `sectors.json`
    * `rifts.json`
