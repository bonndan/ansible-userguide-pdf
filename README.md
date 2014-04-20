Ansible User Guide PDF Generator
================================

This project creates the ansible documentation as [PDF](https://github.com/bonndan/ansible-userguide-pdf/raw/master/ansible_userguide.pdf).

Installation
------------

Requirements:

* A LaTeX distribution (tested with TexLive)
* Python and Sphinx for building the docs.
* A clone of the [ansible repository](https://github.com/ansible/ansible).

Usage
-----

In the console, call the following (assuming that ../ansible/docsite/) points to the
docsite directory of the ansible repo:

    python build_site.py ../ansible/docsite/rst/
    cd latex; pdflatex --interaction=nonstopmode ansible.tex; i
    mv ansible.pdf ../ansible_userguide.pdf; cd ..

See also here: https://github.com/ansible/ansible/tree/devel/docsite

Copyright
---------

The contents of the documentation are Copyright 2014 Ansible, Inc. The scripts in this 
project are copies of the scripts in the ansible repo.
