Command line pastebin for google app-engine, in use at [sprunge.us](http://sprunge.us).

Requirements:

* [pygments](http://pygments.org/). currently using version 1.6.
* [cloudstorage](https://developers.google.com/appengine/docs/python/googlecloudstorageclient/download).

These ^^^ source files needs to be dumped in the app's directory.

Installation method: (Using the GoogleCloudShell)
- create the needed default object/datastore
- create the Google App engine
- start the Google CloudShell, and in there:
-- `git clone` this repo
-- download the [pygments](http://pygments.org/) and [cloudstorage](https://developers.google.com/appengine/docs/python/googlecloudstorageclient/download) source code.
-- move/copy the `pygment` and the `cloudstorage` directories into this repo's cloned directory.
-- in this repo's cloned directory, run `gcloud app deploy .`

don't forget to set some URLs/domains to map to this applicaion.

Version 2:

* Pretty much a complete rewrite, should be transparent to users.
* Sprunge contents are stored in the Blobstore (actually the Cloud Storage
  "default bucket") rather than the Datastore. This gives us more room.
* Existing sprunges are migrated on demand.

Version 1:

* [For reference](https://github.com/rupa/sprunge/releases/tag/v1).

Licensed under the WTFPL.

