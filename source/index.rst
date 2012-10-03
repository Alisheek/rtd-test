.. rtd test documentation master file, created by
   sphinx-quickstart on Wed Oct  3 16:58:41 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to rtd test's documentation!
====================================

Contents:

.. http:get:: /users/(int:user_id)/posts/(tag)

   The posts tagged with `tag` that the user (`user_id`) wrote.

   **Example request**:

   .. sourcecode:: http

      GET /users/123/posts/web HTTP/1.1
      Host: example.com
      Accept: application/json, text/javascript

   **Example response**:

   .. sourcecode:: http

      HTTP/1.1 200 OK
      Vary: Accept
      Content-Type: text/javascript

      [
        {
          "post_id": 12345,
          "author_id": 123,
          "tags": ["server", "web"],
          "subject": "I tried Nginx"
        },
        {
          "post_id": 12346,
          "author_id": 123,
          "tags": ["html5", "standards", "web"],
          "subject": "We go to HTML 5"
        }
      ]

   :query sort: one of ``hit``, ``created-at``
   :query offset: offset number. default is 0
   :query limit: limit number. default is 30
   :statuscode 200: no error
   :statuscode 404: there's no user


.. http:method:: GET /api/foo/bar/{id}/?slug

   :arg integer id: An id
   :optparam string slug: A slug

   Search for a list of foobars matching given id.


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

