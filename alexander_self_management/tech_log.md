# Why trac can't run firstly #

It's about the apache2's problem, there is a config file called port.conf under the path "/etc/apache2", I have to add:

```bash
Listen 8080
```

Then Apache2 will open the port for web service.

# Tackling python module name for Trac #

After running python with apache2, there was always python error:

'''bash
No module named trac
```

Some said that egg format of python library can't be read by mod_python, 
