# Why trac can't run firstly #

It's about the apache2's problem, there is a config file called port.conf under the path "/etc/apache2", I have to add:

```bash
Listen 8080
```

Then Apache2 will open the port for web service.

# Tackling python module name for Trac #

After running python with apache2, there was always python error:

```bash
No module named trac
```

Some said that egg format of python library can't be read by mod_python, so I install trac in a another way:

```bash
easy_install --always-unzip Trac-0.12b1.zip
```
## References ##

[ImportError: No module named trac](https://ruk.ca/content/importerror-no-module-named-trac)

# How to run command within NSIS #

In order to do some dirty works, I have to run a command during installing product. I have tried many methods that are all failed, because I am the new user of NSIS. After some investigations, I think the copy statements and running statements should be in the same section, as below: 

```nsis
Section "serverice"
    ClearErrors
    SetOutPath "$INSTDIR"
    file "mydick.exe"
  
    ExecWait '"$$INSTDIR\mydick.exe" -insert'
SectionEnd
```

Finally, it worked. But I still don't know the reason, I guess that's the policy that NSIS designed.

# How to ssh into a VM guest using NAT #

Maybe there's another way to do this, but in VirtualBox, VM's Network panel, click on advanced, click on Port Forwarding button. In there set up a rule whose protocol is TCP:

```bash
Host IP: 127.0.0.1
Host Port: 2222
Guest IP: 10.0.2.15
Guest Port: 22
```

Then enable ssh in the guest, and I'm able to connect from the host using:

```bash
ssh -p 2222 user@127.0.0.1
```
# How to build llvm&clang on Windows  64 bits #

Besides the tutorial from http://clang.llvm.org/get_started.html, I must use Cygwin64bit as the command interface and run

```bash
 cmake -G "Visual Studio 15 2017 Win64" -t host=x64 ..
```

This command will generate the vs's project file correctly!
