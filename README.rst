.. NOTES FOR CREATING A RELEASE:
..
..   * bumpversion {major|minor|patch}
..   * git push && git push --tags
..   * python setup.py sdist upload
..   * convert into release https://github.com/deanmalmgren/textract/releases


textract
========

Extract text from any document. No muss. No fuss.

`Full documentation <http://textract.readthedocs.org>`__.

textract-page
=============

This is a fork of `textract <https://github.com/deanmalmgren/textract>`__ which provides an additional feature of extracting text from PPTX and PDF documents on a per page basis.

To use this feature with PPTX, pass ``page`` which is a boolean value as an option to ``textract.process`` method. For example::

	text = textract.process('path/to/a.pptx', page=True)

To use this feature with PDF also, pass ``page`` which is a boolean value as an option to ``textract.process`` method. This works only with ``tesseract`` as the ``method``. For example::

	text = textract.process('path/to/b.pdf', method='tesseract', page=True)
