# ReBirth 338 v2.01

[ProTools 2020.12](https://avidtech.my.salesforce-sites.com/pkb/articles/en_US/Knowledge/Pro-Tools-Operating-System-Compatibility-Chart?retURL=%2Fpkb%2Farticles%2Fcompatibility%2FPro-Tools-Supported-Apple-Computers-and-Operating-Systems&popup=true) works with [ReBirth 338 v2.01](https://en.wikipedia.org/wiki/ReBirth_RB-338) + [ReWire](https://en.wikipedia.org/wiki/ReWire_(software_protocol)) V3Sync [v1.30](https://scottbrio.com/rewire-64-32-a-handy-rewire-tool-for-ableton-10/) 32-Bit to 64-Bit Bridge  </br> ﻿https://web.archive.org/web/20121221204754/http://blogs.yahoo.co.jp/alipapa_p/63025279.html </br>
﻿in Windows 8.1x64 + [WinHelp](﻿https://support.microsoft.com/en-us/topic/error-opening-help-in-windows-based-programs-feature-not-included-or-help-not-supported-3c841463-d67c-6062-0ee7-1a149da3973b) [x86](https://www.microsoft.com/en-us/download/details.aspx?id=47667) / [x64](https://www.microsoft.com/en-us/download/details.aspx?id=47671) </br>
 
Win8.1x64 tested with: </br>
[ASRock Z790 LiveMixer](https://www.asrock.com/mb/Intel/Z790%20LiveMixer/Specification.asp) EFi v9.03 + Thunderbolt 4 AIC v1 + i3-12100 + GTX 1050 Ti + Chipset Drivers 10.1.19600.8418 </br>
[ASRock X670e PG Lightning](https://pg.asrock.com/MB/AMD/X670E%20PG%20Lightning/index.asp) UEFI 1.21 + [Thunderbolt 4 AIC v1](https://download.asrock.com/Manual/Thunderbolt%204%20AIC.pdf) + 7600x + M6000 + Chipset Drivers [4.08.09](https://www.amd.com/en/support/downloads/previous-drivers.html/chipsets/am5/x670e.html) 7zip .exe to folder to install drivers.</br>
should also work in a Virtual Machine like: [VirtualBox6](https://www.virtualbox.org/wiki/Download_Old_Builds) or VMWare OSX Fusion Player 10.2.1 / Win: Workstation Player </br>

ReBirth 338 v2.01 [.iso](https://archive.org/search?query=rebirth&and%5B%5D=mediatype%3A%22software%22) is required at start, works with [MagicIso / MagicDisc](https://web.archive.org/web/20210516111743/http://www.magiciso.com/tutorials/miso-magicdisc-overview.htm?=mdisc_hlp106) Virtual CD/DVD.</br>
MagicISO driver requires to Reboot Windows in SafeMode to Dissable 7 Driver Enforcement, install as Administrator and/or allow Windows to load testsigned drivers with cmd "bcdedit /set testsigning on" </br>
 
ReBirth for PC was Discontinued & Released as Freeware in [2005](https://web.archive.org/web/20051130043931/http://www.rebirthmuseum.com/) replaced by ReBirth for iPad, Discontinued in [2017](https://help.reasonstudios.com/hc/en-us/articles/360002216853-ReBirth-for-iPad-has-been-discontinued)</br>
ReWire worked with [Reason 10](https://docs.propellerheads.se/reason10/wwhelp/wwhimpl/js/html/wwhelp.htm#href=ReWire.24.3.html).[1](https://reverb.com/news/how-to-combine-2-daws-with-rewire) or older </br>
There is No ReWire support in [Cubase 12](https://forums.steinberg.net/t/i-didnt-see-where-is-rewire-menu/914704) onwards, Only [11](https://archive.steinberg.help/cubase_pro/v11/en/cubase_nuendo/topics/rewire/rewire_c.html) & older. </br>

ReBirth when running for the 1st time requires a Benchmark: </br>
i3-12100 No-HT gives 23543 points Balanced power settings, </br>
![rebirth-test-i3-12100-4NoHT-23543](https://github.com/user-attachments/assets/2b056c45-57f0-43fd-8bf3-1be3c5454bf3) </br>
Q6600 gives 6917 high performance settings,</br> 
both 4-core No-HyperThreading on the i3. </br>

AMD Ryzen 7600x is slower for 32-Bit vs. Intel i3-12100 in ReBirth test </br>
gives 10798 points No-SMT 6-cores, </br>
![rebirth-7600x-10798](https://github.com/user-attachments/assets/892a5cdb-795a-4043-b288-cdb620ae170e) </br>
Older 2010-2012 AMD Operon 6308 4-cores or 6328 8-cores </br>
![rebirth-test-1x6328x8-1600-8169](https://github.com/user-attachments/assets/0e3b1318-9e3d-4d12-ae0b-c8add7b78b7b) </br>
or 6386 16-cores </br>
![rebirth-test-2x6386x16-1600-7781](https://github.com/user-attachments/assets/3f8236f4-1018-4731-ae68-fab3fee74ca4) </br>

When initial Benchmark is complete, opens a help file, </br>
select audio drivers in configuration settings & close Rebirth. </br>

### WARNING: </br>
ReBirth cannot be opened in ReWire mode, when running for the 1st time "without initial Benchmark". </br>
ReBirth cannot be opened if help file does Not open / gives error. </br>
IF ReWire does Not work in ProTools AAE Error -20038 </br>
![Avid AAE Error -20038](https://github.com/user-attachments/assets/791a07b2-53ab-42f9-9007-95d1c7607d49) </br>
is because has a conflict with other ReWire plugin like Waves Tune LT </br>
requires to Delete "installedAaxplugins" cache file. </br>
Windows8.1x64: </br>
C:\Users\Name\AppData\Roaming\Avid\Pro Tools\InstalledAAXPlugIns </br>
OSX:
user/Library/Preferences/Avid/Pro Tools/InstalledAAXPlugIns </br>
~/Library/Preferences/Avid/Pro Tools/InstalledAAXPlugIns </br>

To Force ProTools Re-Scan plugins at Start "like a New install" </br>
Also Open ReWire 64-32 before to detect Waves LT ReWire. </br>

ReWire requires large Buffer size 1024 in ProTools or audio will have glitches; </br>
Open ProTools, create a session, 48KHz, Open ReBirth, ReWire drivers are auto-detected by ProTools as mono channel instrument. </br>
Cubase requires to activate channel in Devices drop down menu, after creating or opening a session. </br>

ReWire is similar to Roland [TR-09](https://www.roland.com/us/products/tr-09/) / [TR-08](https://www.roland.com/us/products/tr-08/) USB multi-channel audio driver. </br>
Roland also sells a more advanced modern software version of the [909](https://www.roland.com/us/products/rc_tr-909/), [808](https://www.roland.com/us/products/rc_tr-808/), [606](https://www.roland.com/us/products/rc_tr-606/).

ReBirth works in [Linux](https://ubuntuforums.org/showthread.php?t=846551).[1](https://cdm.link/how-to-install-rebirth-in-linux-get-a-free-rack-of-beat-machines/) but there is No ProTools for Linux, and there is No Wine/ReWire to Jack Audio, like WineAsio. </br>
maybe using Carla + Wine + ReWire VST plugin </br>
Having multi-channel output for mixing audio on a DAW, is the goal of ReWire. </br>
ReWire + DAW can be used to convert Digital Audio to Analog Outs + 16-channel External Mixer. </br>

[ReWire VST plugin](https://web.archive.org/web/20181102050538/http://energy-xt.com/rewire-vst.html) released in [2009](https://rekkerd.org/xt-software-releases-xt-rewire-vst/) and discontinued in [2022](https://web.archive.org/web/20210927230559/http://energy-xt.com/shop.html) </br>
Waves also has a [ReWire plugin](https://www.waves.com/support/rewire-link-cannot-be-established-in-waves-tune) for [Tune](https://www.waves.com/plugins/waves-tune) . [v9.3](https://www.waves.com/downloads/v9#v9_3) . [v9.6](https://www.waves.com/downloads/v9#v9_6) . [v9.92](https://www.waves.com/downloads/v9#v9_92) . [v10](https://www.waves.com/downloads/v10#plugins) for W8.1 Untested. </br>

[ReMaker v1.32](https://nordbeat.com/en/download-center/) converts Rebirth songs to MIDI </br>

Other: </br>
[PSP Audioware MasterQ](https://web.archive.org/web/20110207212139/http://pspaudioware.com/plugins/equalizers/psp_masterq/) 1.0.2 - 1.5.2 VST works with [DDMF metaplugin](https://ddmf.eu/metaplugin-chainer-vst-au-rtas-aax-wrapper/) in AAX </br>
DX version works with [VB-Audio FFX4](http://vincent.burel.free.fr/download/index.htm), DX-VST sounds a bit more transparent vs. VST </br>
v1.0.2 does Not have latency when FAT Mode is OFF, later versions have Fixed Latency. </br>
v1.5.2 does Not have DX version, but has RTAS version. </br>
[MasterQ1](https://web.archive.org/web/20110207212139/http://pspaudioware.com/plugins/equalizers/psp_masterq/) was Discontinued in 2015 and replaced with [MasterQ2](https://www.pspaudioware.com/products/psp-masterq2), MQ1 still for sale if ask support. </br>
[MasterQ2](https://www.pspaudioware.com/products/psp-masterq2) has a bit different algorithms "80-bit Foating Point", i prefer v1.0.2 "64-Bit DP FP" </br>
has medium size Q curves vs. Waves REQ "Narrow Q" or McDSP Channel G </br>
there is 4 or 5 Q curve types that most Hardware EQ´s follow from Wide to Narrow,  </br>
Symmetric Boost & Cut or Asymetric Boost & Cut like Waves REQ, or Constant Q Boost & Cut. </br>
Avid d2/d3 very nice for DSP. </br>

Links: </br>
[2003 propellerheads & digidesign announce ReWire2 for ProTools](https://www.mixonline.com/recording/propellerhead-digidesign-announce-rewire2-pro-tools-375894)
[2003 propellerheads.se Website](https://web.archive.org/web/20030429221427/http://www.propellerheads.se/products/rebirth/index.html)
[2004](https://web.archive.org/web/20060703072755/http://www.propellerheads.se/technologies/rewire/index.cfm) - [1](https://web.archive.org/web/20040620015356fw_/http://www.propellerheads.se/technologies/rewire/index.cfm?fuseaction=get_article&article=developer&nc=7618874) - [2](https://web.archive.org/web/20040621040002/http://www.propellerheads.se/developer/index.cfm?fuseaction=mainframe) - [3](https://web.archive.org/web/*/http://propellerheads.se/developer/files/*)
[2006 archive.digidesign.com](https://web.archive.org/web/20060613095751/https://archive.digidesign.com/download/)
[2008 ReWire v1.7](https://web.archive.org/web/20080918060928/http://www.propellerheads.se/download/updates_rewire/index.cfm?fuseaction=displaymain) [2010](https://web.archive.org/web/20100417072540/http://www.propellerheads.se/download/updates_rewire/index.cfm?fuseaction=displaymain)
[What is](https://web.archive.org/web/20100506002107/http://www.propellerheads.se/products/reason/index.cfm?fuseaction=get_article&article=rewire)
[dev.propellerheads.se](https://web.archive.org/web/20040825054454/http://dev.propellerheads.se:80/technologies/index.cfm?fuseaction=mainframe)
[ftp.propellerheads.se/downloads/*](https://web.archive.org/web/*/ftp.propellerheads.se/downloads/*) 404
[Technical](https://web.archive.org/web/20140203073256/http://www.propellerheads.se/developer/index.cfm?fuseaction=get_article&article=rewiretechinfo) - [2010 Request](https://web.archive.org/web/20100830053830/http://www.propellerheads.se/developer/request/index.cfm?fuseaction=displaymain)

[Tools Downloads](https://web.archive.org/web/20090216203806/http://rebirth.cz/downloads.html)
