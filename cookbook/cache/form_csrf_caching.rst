.. index::
    single: Cache; CSRF; Forms

缓存包含了使用CSRF保护的表单的页面
==================================

CSRF tokens are meant to be different for every user. This is why you
need to be cautious if you try to cache pages with forms including them.

For more information about how CSRF protection works in Symfony, please
check :ref:`CSRF Protection <forms-csrf>`.

为什么缓存带有CSRF校验码的页面是个难题
--------------------------------------

Typically, each user is assigned a unique CSRF token, which is stored in
the session for validation. This means that if you *do* cache a page with
a form containing a CSRF token, you'll cache the CSRF token of the *first*
user only. When a user submits the form, the token won't match the token
stored in the session and all users (except for the first) will fail CSRF
validation when submitting the form.

In fact, many reverse proxies (like Varnish) will refuse to cache a page
with a CSRF token. This is because a cookie is sent in order to preserve
the PHP session open and Varnish's default behaviour is to not cache HTTP
requests with cookies.

如何缓存带有CSRF保护的页面
--------------------------

To cache a page that contains a CSRF token, you can use more advanced caching
techniques like :ref:`ESI fragments <edge-side-includes>`, where you cache
the full page and embedding the form inside an ESI tag with no cache at all.

Another option would be to load the form via an uncached AJAX request, but
cache the rest of the HTML response.

Or you can even load just the CSRF token with an AJAX request and replace the
form field value with it.

.. _`Cross-site request forgery`: http://en.wikipedia.org/wiki/Cross-site_request_forgery
.. _`Security CSRF Component`: https://github.com/symfony/security-csrf
