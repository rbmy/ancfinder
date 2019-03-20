Ancfinder
==========

A website about DC's Advisory Neighborhood Commission system.

Contributing
------------

If you plan to contribute to the repo, you should set up your own fork and open pull requests with any commits you make. Please note that all contributions are made under a [CC0 license](LICENSE.md).

If you're not familiar with forking, Github has a [useful guide](https://help.github.com/articles/fork-a-repo).

Getting Started
---------------

In order to get the site running locally you'll want to start by creating an account for Docker, download, and install the program. The community edition can be downloaded [here](https://www.docker.com/community-edition). Additionally, create a [mapbox account](https://www.mapbox.com) to get a access token.

Next, if you have not done so yet, for this repository from the [Code For DC github page](https://github.com/codefordc). Once forked, clone the repository to your computer to create a working copy.

	git clone git@github.com:yourUserName/ancfinder.git

Starting Ancfinder
------------------
Before you can use docker to start everything up you'll need to app.env and set the `MAPBOX_API_KEY` to the access token for your mapbox account.

At this point you will not have any of the dependencies need to run the website. This is where docker comes in hand. To get all the required dependencies and start the app, run the following at the command line from your cloned repository:

	docker-compose up -d

If you wish to see additional logging you may leave of `-d`.

If you are unfamiliar with docker, there is a very quick and easy tutorial [here](https://medium.com/@deepakshakya/beginners-guide-to-use-docker-build-run-push-and-pull-4a132c094d75) that will get you up to speed.

After all the dependencies have downloaded and installed and ancfinder has started, direct your browser to `localhost` to view the website.

To bring down the app you run the following:

	docker-compose down

If you started things without `-d`, press ctrl + c to kill the process.
