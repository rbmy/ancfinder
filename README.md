ancbrigade
==========

A website about DC's Advisory Neighborhood Commission system.

Dependencies
------------

Set up your environment for installing dependencies:

	git clone --recursive https://github.com/codefordc/ancbrigade
	virtualenv .env # maybe one day we'll use '-p python3' but dotcloud makes that harder
	. .env/bin/activate
	pip install -r requirements.txt
	
Note --recursive on 'git clone' to get the submodule dependencies.

Running the Site
----------------

Just run:

	. .env/bin/activate
	./manage.py runserver
	
Then view the site in your browser at the address shown to you.

Updating Static Data
--------------------

The ANC/SMD metadata is stored statically in ancbrigadesite/static/ancs.json. To update this file
from our Google Doc, our ScraperWiki scraper, and other external data sources, run:

	python3 update_anc_database.py

And to fetch the latest ANC meetings calendar:
	
	python3 update_meeting_database.py
	
Deployment
----------

We're currently deploying to dotCloud.

	sudo pip install dotcloud
	dotcloud setup
	dotcloud connect ancbrigade
	dotcloud push # push changes to the live site
	
