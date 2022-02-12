# Dell Boomi Atom on Mac OS

The Dell Boomi Atom can be installed on Window, Linux, Docker, PCF or Kubernetes (see [link]: https://github.com/anthonyrabiaza/BoomiKubernetes/	"Kubernetes") and also on an Apple computer.


These are the steps required:

1. Install java 11 jdk 
   wget https://corretto.aws/downloads/latest/amazon-corretto-11-x64-macos-jdk.pkg

2. Install the Atom by downloading the Linux-64bits version and getting a token

```
$ chmod u+x atom_install64.sh 
$ ./atom_install64.sh

Please read the following important information before continuing.

The following will be installed when you choose to continue.

```

3. Update pref_jre.cfg with the path of the freshly installed JDK

```
   $ vim /Applications/Boomi_AtomSphere/Atom/atom_"atom name"/.install4j/pref_jre.cfg
   
   /Library/Java/JavaVirtualMachines/amazon-corretto-11.jdk/Contents/Home

```
4. Backup unpack200

```
cp /Applications/Boomi_AtomSphere/Atom/atom_"atom name"/jre/bin/unpack200 /Applications/Boomi_AtomSphere/Atom/Atom_MacBookPro55/jre/bin/unpack200.bak
```
5. Copy unpack200 from the freshly installed JDK/JRE
```
cp /Library/Java/JavaVirtualMachines/amazon-corretto-11.jdk/Contents/Home/bin/unpack200 /Applications/Boomi_AtomSphere/Atom/Atom_MacBookPro55/jre/bin/unpack200 
```
6. Run the Atom

```
$ /Applications/Boomi_AtomSphere/Atom/Atom_Macbookpro/bin/atom start or 
$ /Applications/Boomi_AtomSphere/Atom/Atom_Macbookpro/bin/atom stop
```

7. Connect to AtomSphere and validate that the Atom is RUNNING (blue icon)