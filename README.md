latex2edx-minimal
=================

latex2edx-minimal est la coquille d'un cours latex2edx minimal pouvant être utilisé dans l'environnement EDUlib ou tout autre environnement Open edX.

Largement inspiré du contenu original du cours latex2edx démo de MIT
* https://github.com/mitocw/content-mit-latex2edx-demo


Coquille minimale
=================

Il y a deux fichiers importants dans le répertoire src qui vous seront utiles pour démarrer votre cours latex2edx:

* moncours.tex supporte une structure de cours incluant un chapitre minimal via l'inclusion du fichier minimal.tex
* minimal.tex contient un chapitre minimal


Documentation
=============

* http://edx-open-learning-xml.readthedocs.org/en/latest/index.html (format Open Learning XML)
* http://mitocw.github.io/latex2edx/html/index.html (format latex2edx)

La documentation de Open Learning XML vous sera utile afin de modifier à la main et selon vos besoins les fichiers se trouvant dans les répertoires about, info, policies, static ou autres qui contiennent des informations sur votre cours.

La documentation de latex2ex vous sera utile afin de modifier à la main et selon vos besoins les fichiers moncours.tex, minimal.tex et autres fichier .tex que vous voudrez ajouter à votre cours.

Pour fins de références, nous vous référons aussi à la documentation originale du cours démo développé par MIT
* https://github.com/mitocw/content-mit-latex2edx-demo 


Installation
============

Pour modifier votre cours, veuillez modifier le fichier src/moncours.tex et/ou le fichier src/minimal.tex. Vous pouvez aussi ajouter d'autres fichiers .tex si vous les incluer dans le fichier src/moncours.tex au préalable. Vous pouvez aussi modifier les fichiers se trouvant dans les répertoires about, info, policies, static ou autres qui contiennent des informations sur votre cours.

Nous vous recommendons de modifier l'image de votre cours se trouvant dans le fichier static/images/course_image.jpg.

Nous vous recommendons de modifier le vidéo d'introduction de votre cours se trouvant dans le fichier about/video.html.

Nous vous recommendons de vous assurer que le nom de votre cours est bien identifié dans le fichier src/moncours.tex et que celui est aussi correct dans le fichier course.xml.

Après avoir fait les modifications nécessaires à votre cours, il faudra maintenant compiler celui-ci. Pour ce faire, exécutez les commandes suivantes dans le répertoire src:
* ln -s .. course
* touch moncours.tex 
* make
* rm course


Si tout s'est déroulé correctement, il faudra maintenant produire le fichier .tar.gz qui sera utilisé lors de l'import de votre cours dans Studio.

Avant de procéder, veuillez vous assurer que le fichier course.xml contient les bonnes informations pour votre cours.

Veuillez aussi vous assurer que le nom du sous-répertoire sous policies est bien équivalent au url_name dans le fichier course.xml. A noter que vous devrez éditer le fichier policy.json afin d'y inclure les paramètres et valeurs appropriées pour votre cours. Voir http://edx.readthedocs.org/projects/edx-open-learning-xml/en/latest/policies/course.html pour plus de détails.

Si vous devez noter des exercices, la lecture de http://edx.readthedocs.org/projects/edx-open-learning-xml/en/latest/policies/grading.html vous sera utile puisque le fichier grading_policy.json doit aussi se retrouver dans le même répertoire que le fichier policy.json mentionné dans le paragraphe précédent.

Ensuite, exécutez la commande suivante dans le répertoire où vous avez importé ce cours minimal:
* tar -cvzf latex2edx-minimal.tar.gz latex2edx-minimal

Bien évidemment, si vous avez changé le nom du répertoire initial (latex2edx-minimal) veuillez utiliser le nom approprié. Idem pour le fichier .tar.gz.

Finalement, vous devrez ensuite importer le fichier .tar.gz dans Studio.

Pour votre information, les sections suivantes de ce README proviennent de la documentation initial du cours démo latex2edx produit par MIT.

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
