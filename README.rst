[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FPsypherPunk%2Fdjango-annotator.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FPsypherPunk%2Fdjango-annotator?ref=badge_shield)

================
django-annotator
================

.. image:: https://travis-ci.com/PsypherPunk/django-annotator.png?branch=master
   :target: https://travis-ci.com/PsypherPunk/django-annotator

2.1.0
=====

Django implementation of `annotatorjs Storage <http://annotatorjs.org/>`_.


Implements most of the methods as per the `Core Storage/Search API <http://docs.annotatorjs.org/en/v1.2.x/storage.html#core-storage-api>`_ documentation (``root``, ``index``, ``create``, ``read``, ``update``, ``delete`` and ``search``).

To see a working demo:

.. code:: bash

    virtualenv annotatorjs
    cd annotatorjs
    source bin/activate
    git clone https://github.com/PsypherPunk/django-annotator.git
    cd django-annotator
    ./demo.py

This will run the tests, after which a demo. page will be available at ``/demo``.


Installation
============

The package can be installed via ``pip``:

.. code::

    pip install django-annotator

Following installation it can be added to any Django project by updating the ``INSTALLED_APPS``:

.. code::

    INSTALLED_APPS = (
        ...
        "annotator",
        ...
    )

Then run ``migrate`` to include the new tables from ``django-annotator``:


.. code::

    ./manage.py migrate

Annotator
---------

The package relies on *Annotator* being installed in your project—see the `documentation <http://docs.annotatorjs.org/en/v1.2.x/getting-started.html>`_ for details of its inclusion.

Settings
--------

As per Annotator's documentation, the `root <http://docs.annotatorjs.org/en/v1.2.x/storage.html#root>`_ endpoint will return information in the format:

.. code::

    {
        "name": "django-annotator-store",
        "version": "2.1.0"
    }

The ``name`` returned can be configured by setting ``ANNOTATOR_NAME`` in your ``settings`` (defaulting to the above).

django-cors-headers
+++++++++++++++++++

If you have any issues with *Cross-origin resource sharing (CORS)*, consider installing the ``django-cors-headers`` `package <https://github.com/ottoyiu/django-cors-headers>`_.


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FPsypherPunk%2Fdjango-annotator.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FPsypherPunk%2Fdjango-annotator?ref=badge_large)