Ansible User Guide PDF Generator
================================

This project creates a PDF file from the ansible documentation.

Installation
------------

Requirements:

* A LaTeX distribution (tested with TexLive)
* Python and Sphinx for building the docs.
* A clone of the ansible repository.

Usage
-----

In the console, call the following (assuming that ../ansible/docsite/) points to the
docsite directory of the ansible repo:

    python build_site.py ../ansible/docsite/
    cd latex; pdflatex --interaction=nonstopmode ansible.tex; mv ansible.pdf ../ansible_userguide.pdf; cd ..



