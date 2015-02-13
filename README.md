Ansible User Guide PDF Generator
================================

This project creates the ansible documentation as [PDF](https://github.com/bonndan/ansible-userguide-pdf/raw/master/ansible_userguide.pdf).

Installation
------------

Requirements:

* A LaTeX distribution (tested with TexLive)
* Python and Sphinx for building the docs.
* A clone of the [ansible repository](https://github.com/ansible/ansible).

Steps to install (in Debian/Ubuntu):
   
    # Install python & pip
    apt-get -y install python python-pip
   
    # Install Sphinx via pip
    pip install sphinx
  
    # Install TexLive packages (almost 1GB!)
    apt-get install -y texlive-latex-base texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended
   
    # Clone this repo
    git@github.com:bonndan/ansible-userguide-pdf.git
   
    # Clone Ansible's repo
    git clone git://github.com/ansible/ansible.git --recursive


Usage
-----

In the console, call the following (assuming that ../ansible/docsite/) points to the
docsite directory of the ansible repo:

    cd ansible-userguide-pdf
    python build-site.py ../ansible/docsite/rst/
    cd latex; pdflatex --interaction=nonstopmode ansible.tex;
    mv ansible.pdf ../ansible_userguide.pdf; cd ..

See also here: https://github.com/ansible/ansible/tree/devel/docsite

Copyright
---------

The contents of the documentation are Copyright 2014 Ansible, Inc. The scripts in this 
project are copies of the scripts in the ansible repo.
