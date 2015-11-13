latex2edx-minimal
=================

latex2edx-minimal est la coquille d'un cours latex2edx pouvant être utilisé dans l'environnement EDUlib.

Inspiré de
* https://github.com/mitocw/content-mit-latex2edx-demo

Ce répertoire contient un exemple d'un cours minimal d'un cours edX généré via latex2edx (https://github.com/mitocw/latex2edx).

Coquille minimale
=================

Il y a deux fichiers importants dans le répertoire src:

moncours.tex supporte une structure de cours incluant un chapître minimal via l'inclusion du fichier minimal.tex


Documentation
=============

* http://mitocw.github.io/latex2edx/html/index.html (format latex2edx)
* http://edx-open-learning-xml.readthedocs.org/en/latest/index.html (format Open Learning XML)

La documentation de Open Learning XML sera utile afin de modifier à la main et selon vos besoins les fichiers se trouvant dans les répertoires about, info, policies, static ou autres qui contiennent des informations sur votre cours.

Pour fins de références, nous conservons ici aussi la documentation originale du cours démo développé par MIT
* https://github.com/mitocw/content-mit-latex2edx-demo 


Installation
============

Pour modifier votre cours, veuillez modifier le fichier src/moncours.tex et/ou le fichier src/minimal.tex. Vous pouvez aussi ajouter d'autres fichiers .tex si vous les incluer dans le fichier src/moncours.tex au préalable.

Après avoir fait vos modifications, il faut maintenant compiler votre cours. Pour ce faire, allez dans le répertoire src et exécutez les commandes suivantesL
* ln -s .. course
* touch moncours.tex 
* make
* rm course

Si tout s'est déroulé correctement, il faut maintenant produire le fichier .tar.gz pour votre cours. Pour ce faire, exécutez la commande suivante dans le répertoire où vous avez importé ce cours minimal:
* tar -cvzf latex2edx-minimal.tar.gz latex2edx-minimal

Bien évidemment, si vous avez changé le nom du répertoire initial (latex2edx-minimal) veuillez utiliser le nom approprié. Idem pour le fichier .tar.gz.

Il vous suffit ensuite d'importer ce cours dans https://studio.edulib.org


Live Example Site
=================

https://edge.edx.org/courses/MITx/MIT.latex2edx/2014_Spring/about

LaTeX Source Files
==================

The main tex files are in the "src" directory.

See these latex files for specific examples of latex code with latex2edx macros:

* https://github.com/mitocw/content-mit-latex2edx-demo/blob/master/src/basic.tex

* https://github.com/mitocw/content-mit-latex2edx-demo/blob/master/src/advanced.tex

To compile this course, check out this repository, go to src, and run "make"

Contents
========

This is a sample course generated from a latex source file, compiled
into edX XML using latex2edx. Content includes examples of basic
problems, text, and video modules, as well as advanced problems using
custom graders written in python, and graphical input via javascript.

Examples included:

* Numerical response with inline labels
* Custom response problem with two inputs
* Formula response problem checking mathematical equations
* Matrix expression equality testing (for math expressions with nonabelian operators)
* Quantum mechanics ket input
* Adaptive hints using "hint_fn" scripts
* Drag and drop problem created via latex2dnd

See the latex2edx distribution and the latexdnd package (https://github.com/mitocw/latex2dnd) for more information.
