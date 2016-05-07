---
permalink: /Biers/dependency/
level: 2
prev: install/
---

# Biers Dependency

<hr/>

## RNAstructure

We are using the **Command Line** (Text Interface) of RNAstructure. Based on our experience, we provide instructuions that is based on and in addtion to RNAstructure's [help page](http://rna.urmc.rochester.edu/Text/index.html). This guide is tested for _Mac OS X_ systems.

* #### Install a C complier, preferably `gcc`. 

We install it via `brew`, a handy package manager for _Mac OS X_. If you don't have `brew` installed, do:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Then install `gcc` with:

```bash
brew install gcc
```

Test if `gcc` is the default C complier. You can say:

```bash
which gcc
gcc --version
```

to check if `clang` (system default) occupies the namespace. To fix it, try:

```bash
brew link gcc
```

> You may need to `unlink gcc` first before `link` again.

<br/>

* #### Set environment variable `DATAPATH` for thermodynamic tables.

Edit file `~/.bash_profile`, add a line:

```bash
export DATAPATH=/path/to/RNAstrucutre/data_tables/
```

> Use any text editor you prefer, e.g. `vim`, `nano` (easiest), `emacs`.

> Make sure you replace the path to your 'real' path!

Now close the terminal window and start a new one. (This allows the `~/.bash_profile` to take effect.)

<br/>

* #### Compile RNAstructure locally.

Check `/path/to/RNAstructure/compiler.h` to make sure `CXX = g++`.

Now run the following command to compile the code:

```bash
cd /path/to/RNAstructure/
make clean
cd RNA_class/
make clean
cd ..
make all
make install
```

<hr/>

## VARNA

* #### Download VARNA **.jar** file and place on your desktop.

> Any of the _types_ listed on the [download page](http://varna.lri.fr/index.php?lang=en&page=downloads&css=varna) works. The minimal _Binaries_ suffices.

* #### Change VARNA path in _MATLAB_.

Copy `Scripts/get_varna.m.example` into `Scripts/get_varna.m`. Edit it following the instructions in these files. The `VARNA_DIR` and `VARNA_JAR` point to your **.jar** file on desktop.

* #### _Java_ Security Fix

Follow the instructions [here](http://varna.lri.fr/index.php?lang=en&page=securityfix&css=varna) to add the certificate to your browser.

> You can only use _Firefox_ for the VARNA applet. As we have tested, neither _Chrome_ nor _Safari_ supports it (or _Java_).

* #### System Whitelist

Last, you need to add the generated **.html** files to security whitelist, or they would be blocked. Admittedly, this is a pain.

Go to **System Preference** -> **Java** -> **Security**. Add 
`file:///Users/yourname/` to the whitelist.

<br/>

Now you are all set. So when you open a **.html** file, follow this procedure:

* Move the **.html** file to your desktop.

* Open it with _Firefox_. 

> You may want to set _Firefox_ as default for **.html** files, if you do this a lot.

* Click **OK** for the security warning.

> We found that if you open another such **.html** files in the same browser window, the security warning would not show up. So as a tip, do not close the browser window, use more tabs.



