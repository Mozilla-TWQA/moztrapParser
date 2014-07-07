mozTrapParser
=============

The tool is used to grab mozTrap information to Excel format.

INSTALLLATION
-------------

The parser doesn't need installation, but you'll need to install OpenPyXL libaray for using.

https://pythonhosted.org/openpyxl/

<p>
    $ pip install openpyxl
</p>

or

<p>
    $ easy_install openpyxl
</p>


PREPARATION
-----------

You'll need to modify some information in the mozTrapParser.py

Code:

```
url = '/api/v1/caseversion/?limit=100&productversion=177&username=awesomeUser&api_key=abcd-efgh-ijkl-mnop-1234&format=json'
xlsxFilename = 'moztrap_fxos_test_case_2.0.xlsx'
```

url composes the RESTfulAPI to mozTrap. You can grab these information from MozTrap (https://moztrap.mozilla.org)

You'll need to give the following information

#######productversion
product version to filter
#######username
after you regestering moztrap, you'll have a username
#######api_key
api key can be generated by admin. You might need to contact an admin for an api_key
https://github.com/mozilla/moztrap/blob/master/docs/userguide/api/key.rst
#######limit
default to 100. the parameter controls the data been processed every cycle


EXECUTION
---------

<p>
    python mozTrapParser.py
</p>

