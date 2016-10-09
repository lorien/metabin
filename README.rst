Metabin
=======

What is that?
-------------

Proof-of-concept HTML/js pastebin application that stores AES encrypted
data at other paste bin applications. That means you can run this app from
any web hosting or just from you local drive.


What happens when I submit the data
-----------------------------------

* you provide data and password
* data is encrypted with your password
* encrypted dump is submit to external pastebin service
* you get the URL of your dump


What happens when I open dump URL
---------------------------------

* you provide a password
* encrypted data is requested from external pastebin service
* data is decrypted with your password
* you see unencrypted data


What is encryption algo?
------------------------

AES in GCM mode. Encryption runs with SJCL library.


What external pastebin services are used?
-----------------------------------------

The app can use any pastebin that allows to upload content by simple POST request.


How do you submit AJAX POST request to external domains?
--------------------------------------------------------

I use yahoo YQL service. See details in this blog article: http://www.christianheilmann.com/2009/11/16/using-yql-to-read-html-from-a-document-that-requires-post-data/ 
