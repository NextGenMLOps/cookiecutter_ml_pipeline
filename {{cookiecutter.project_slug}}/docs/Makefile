SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = MLOpsExample
SOURCEDIR     = .
BUILDDIR      = _build

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

auto-rst:
	sphinx-apidoc -o $(SOURCEDIR) ../src

html: auto-rst
	@$(SPHINXBUILD) -b html $(SOURCEDIR) $(BUILDDIR)/html
	@echo
	@echo "Build finished. The HTML pages are in $(BUILDDIR)/html."

# Open the documentation in a web browser
view:
	open $(BUILDDIR)/html/index.html

clean:
	-rm -rf $(BUILDDIR)/*
