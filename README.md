UserDefaults Utility
====================

Show/edit/search a file for your UserDefaults.



Usage
-----

```console
$ userdefaults-ctl path com.example.app
/Absolute/path/to/.../Preferences/com.example.app.plist
```

```console
$ userdefaults-ctl show com.example.app
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD ...
<plist version="1.0">
...
```

```console
$ userdefaults-ctl edit com.example.app
# Changes

--- com.example.app.plist         2017-02-14 ...
+++ com.example.app.plist.XXXXXX  2017-02-14 ...
@@ -10,7 +10,5 @@
        <true/>
        <key>WebKitShrinksStandaloneImagesTo ...
        <true/>
-       <key>hogehoge</key>
-       <true/>
 </dict>
 </plist>

# Validation
Syntax: VALID
```

```console
$ userdefaults-ctl help
usage: userdefaults-ctl <command>

These are available commands:

   path <bundle_id>   Print a path for the UserDefaults of the booted device
   show <bundle_id>   Print a content of the UserDefaults of the booted device
   edit <bundle_id>   Edit the UserDefaults of the booted device by $EDITOR
   help               Print this help
```



Install
-------

You can install this by the following command (you should customize `path/to/userdefaults-ctl` to the location you like):

```console
$ git clone https://github.com/Kuniwak/userdefaults-ctl path/to/userdefaults-ctl

$ export PATH="path/to/userdefaults-ctl/bin:$PATH"

$ which userdefaults-ctl
path/to/userdefaults-ctl/bin/userdefaults-ctl
``` 



License
-------

[The MIT License (MIT)](https://kuniwak.mit-license.org/)
