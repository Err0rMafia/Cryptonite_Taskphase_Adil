## an-epic-filesystem-quest
# Procedure
Followed the process as mentioned in pwn.college
# Bash
`hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
SNIPPET  challenge  flag  lib32   media  opt   run   sys  var
bin      dev        home  lib64   mnt    proc  sbin  tmp
boot     etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat tmp
cat: tmp: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ cat SNIPPET
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/jupyter_server/gateway

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/jupyter_server/gateway
cat: /usr/local/lib/python3.8/dist-packages/jupyter_server/gateway: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/local/lib/python3.8/dist-packages/jupyter_server/gateway
NOTE-TRAPPED  __pycache__     gateway_client.py  managers.py
__init__.py   connections.py  handlers.py
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/jupyter_server/gateway/NOTE-TRAPPED
Lucky listing!
The next clue is in: /usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ ls
LEAD  main_rkt.dep  main_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat LEAD
Tubular find!
The next clue is in: /opt/radare2/shlr/capstone/msvc/test_xcore

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ ls /opt/radare2/shlr/capstone/msvc/test_xcore
TIP-TRAPPED  test_xcore.vcxproj
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat /opt/radare2/shlr/capstone/msvc/test_xcore/TIP-TRAPPED
Lucky listing!
The next clue is in: /opt/ghidra/Ghidra/Features/Base/data/typeinfo/win32/msvcrt

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ ls -a /opt/ghidra/Ghidra/Features/Base/data/typeinfo/win32/msvcrt
.  ..  .NUGGET  clsids.txt  guids.txt  iids.txt  syntaxes.txt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat /opt/ghidra/Ghidra/Features/Base/data/typeinfo/win32/msvcrt/.NUGGET
Tubular find!
The next clue is in: /opt/linux/linux-5.4/Documentation/devicetree/bindings/iio/resolver
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ ls /opt/linux/linux-5.4/Documentation/devicetree/bindings/iio/resolver
GIST  ad2s90.txt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/iio/resolver/ad2s90.txt
Analog Devices AD2S90 Resolver-to-Digital Converter

https://www.analog.com/en/products/ad2s90.html

Required properties:
  - compatible: should be "adi,ad2s90"
  - reg: SPI chip select number for the device
  - spi-max-frequency: set maximum clock frequency, must be 830000
  - spi-cpol and spi-cpha:
        Either SPI mode (0,0) or (1,1) must be used, so specify none or both of
        spi-cpha, spi-cpol.

See for more details:
    Documentation/devicetree/bindings/spi/spi-bus.txt

Note about max frequency:
    Chip's max frequency, as specified in its datasheet, is 2Mhz. But a 600ns
    delay is expected between the application of a logic LO to CS and the
    application of SCLK, as also specified. And since the delay is not
    implemented in the spi code, to satisfy it, SCLK's period should be at most
    2 * 600ns, so the max frequency should be 1 / (2 * 6e-7), which gives
    roughly 830000Hz.

Example:
resolver@0 {
        compatible = "adi,ad2s90";
        reg = <0>;
        spi-max-frequency = <830000>;
        spi-cpol;
        spi-cpha;
};
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/iio/resolver/GIST
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/twisted/trial/_dist/test

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ ls -a /usr/lib/python3/dist-packages/twisted/trial/_dist/test
.        __init__.py           test_disttrial.py  test_workerreporter.py
..       __pycache__           test_options.py    test_workertrial.py
.README  test_distreporter.py  test_worker.py
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cat /usr/lib/python3/dist-packages/twisted/trial/_dist/test/.README
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/compatibility-lib/mzscheme/compiled$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular$ ls
All.js  MEMO  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular$ cat MEMO
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/angr/analyses/variable_recovery
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular$ ls /usr/local/lib/python3.8/dist-packages/angr/analyses/variable_recovery
WHISPER         engine_ail.py    variable_recovery.py
__init__.py     engine_base.py   variable_recovery_base.py
__pycache__     engine_vex.py    variable_recovery_fast.py
annotations.py  irsb_scanner.py
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX/Variants/Regular$ cat /usr/local/lib/python3.8/dist-packages/angr/analyses/variable_recovery/WHISPER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{EOOGq0bahgDere185SILIH0xoiv.dljM4QDLxgTN1czW}`
# Reference
pwn.college
