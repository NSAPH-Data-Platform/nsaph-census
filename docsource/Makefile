# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = .
BUILDDIR      = build

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)


github:
	@rm -rf ../docs/*
	@cp ../CHANGELOG.md $(SOURCEDIR)
	@cp .nojekyll ../docs/
	@make html
	@cp -a build/html/. ../docs

gitlab:
	@rm -rf ../public/*
	@cp ../CHANGELOG.md $(SOURCEDIR)
	@cp .nojekyll ../public/
	@make html
	@cp -a build/html/. ../public