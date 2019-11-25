# Fork and Maintain changes from original repository
[Source](https://digitaldrummerj.me/git-syncing-fork-with-original-repo/)

Fork original repository in Github.

Clone forked repository.

	git clone git clone git@github.com:jnoelvictorino/cocktail-party-problem.git
	cd cocktail-party-problem

Setup original repository as upstream to get changes from original repository.

	git remote -v
	# origin	git@github.com:jnoelvictorino/cocktail-party-problem.git (fetch)
	# origin	git@github.com:jnoelvictorino/cocktail-party-problem.git (push)

	git remote add upstream https://github.com/furkaya06/cocktail-party-problem.git
	git remote -v
	# origin	git@github.com:jnoelvictorino/cocktail-party-problem.git (fetch)
	# origin	git@github.com:jnoelvictorino/cocktail-party-problem.git (push)
	# upstream	https://github.com/furkaya06/cocktail-party-problem.git (fetch)
	# upstream	https://github.com/furkaya06/cocktail-party-problem.git (push)

To get changes from original repository:

	git fetch upstream

Then, make sure you are on 'master' branch:
	
	git checkout master

Merge changes from upstream/master to local master branch

	git merge upstream/master

# Create PyEnv VirtualEnv for Kaldi

	pyenv install 3.7.4
	pyenv virtualenv 3.7.4 cocktail-party-problem
	pyenv local cocktail-party-problem
	pip install --upgrade pip
	pip install pipenv
	pipenv install	
	pipenv install jupyter
	jupyter notebook