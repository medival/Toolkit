# My Essentials Tools for Working

- Winbox
- Mikrotik Voucher Generator
- Ubiquiti Firmware (XM, XW)
- Ubnt Discovery

### Here how to show compliance test in ubnt radio

_This only works on ubnt firmware < v6.1.6_

1. Set your ip 192.168.1.x
2. Open ssh with [putty](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.74-installer.msi) or using Terminal if using linux
3. Set user **ubnt** and default ip address is **192.168.1.20**
4. Then show prompt, click yes
5. type your password. default is **ubnt**
6. then type `touch /etc/persistent/ct`
7. save your config using command `save`
8. Reboot your ubnt devices `reboot`
9. Login to your ubnt devices
10. There should be Compliance Test in your country

### How to change country in ubnt devices without reset

1. Open ssh tools like [putty](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.74-installer.msi) or terminal if using linux
2. Login to your ubnt devices
3. Then show prompt, click yes
4. Type your password
5. You will be in console of ubnt
6. Add compliance test by running command `touch /etc/persistent/ct`
7. Get code of current country with command `cat /tmp/system.cfg | grep code`
8. Then code will show like this

   > radio.1.countrycode=360

   > radio.countrycode=360

9. Then find country code u want to set
10. Change country code in system.cfg by using command `sed -i 's/countrycode=360/countrycode=511/g' /tmp/system.cfg`
11. Change country code in running.cfg by using command `sed -i 's/countrycode=360/countrycode=511/g' /tmp/running.cfg`
12. Then check country code has changed with command `cat /tmp/system/cfg`
13. If country code has changed will be like this

    > radio.1.countrycode=511

    > radio.countrycode=511

14. Save config by running command `save`
15. Reboot devices to apply new config by running command `reboot`
16. Then country will be changed.

Full of country code available here
|Country Code |Country |
|---------------|-------------------------|
|32 | Argentina |
|51 | Armenia |
|533 | Aruba |
|36 | Australia |
|40 | Austria |
|31 | Azerbaijan |
|48 | Bahrain |
|52 | Barbados |
|112 | Belarus |
|56 | Belgium |
|84 | Belize |
|68 | Bolivia |
|70 | Bosnia and Herzegovina |
|76 | Brazil |
|96 | Brunei Darussalam |
|100 | Bulgaria |
|116 | Cambodia |
|124 | Canada |
|152 | Chile |
|156 | China |
|170 | Colombia |
|511 | Compliance Test |
|188 | Costa Rica |
|191 | Croatia |
|196 | Cyprus |
|203 | Czech Republic |
|208 | Denmark |
|214 | Dominican Republic |
|218 | Ecuador |
|818 | Egypt |
|222 | El Salvador |
|233 | Estonia |
|246 | Finland |
|250 | France |
|268 | Georgia |
|276 | Germany |
|300 | Greece |
|304 | Greenland |
|308 | Grenada |
|316 | Guam |
|320 | Guatemala |
|332 | Haiti |
|340 | Honduras |
|344 | Hong Kong |
|348 | Hungary |
|352 | Iceland |
|356 | India |
|360 | Indonesia |
|368 | Iraq |
|372 | Ireland |
|376 | Israel |
|380 | Italy |
|388 | Jamaica |
|400 | Jordan |
|404 | Kenya |
|410 | Korea Republic |
|414 | Kuwait |
|428 | Latvia |
|422 | Lebanon |
|438 | Liechtenstein |
|440 | Lithuania |
|442 | Luxembourg |
|446 | Macau |
|807 | Macedonia |
|458 | Malaysia |
|470 | Malta |
|484 | Mexico |
|492 | Monaco |
|504 | Morocco |
|524 | Nepal |
|528 | Netherlands |
|530 | Netherlands Antilles |
|554 | New Zealand |
|566 | Nigeria |
|578 | Norway |
|512 | Oman |
|586 | Pakistan |
|591 | Panama |
|598 | Papua New Guinea |
|604 | Peru |
|608 | Philippines |
|616 | Poland |
|620 | Portugal |
|630 | Puerto Rico (U.S. territory)|
|634 | Qatar |
|642 | Romania |
|643 | Russia |
|646 | Rwanda |
|652 | Saint Barthelemy |
|682 | Saudi Arabia |
|891 | Serbia and Montenegro |
|702 | Singapore |
|703 | Slovakia |
|705 | Slovenia |
|710 | South Africa |
|724 | Spain |
|144 | Sri Lanka |
|752 | Sweden |
|756 | Switzerland |
|158 | Taiwan |
|764 | Thailand |
|780 | Trinidad and Tobago |
|788 | Tunisia |
|792 | Turkey |
|804 | Ukraine |
|784 | United Arab Emirates |
|826 | United Kingdom |
|840 | United States |
|858 | Uruguay |
|860 | Uzbekistan |
|862 | Venezuela |
|704 | Viet Nam |

#Public NTP Client

### Google Public NTP [AS15169]:

time.google.com

time1.google.com

time2.google.com

time3.google.com

time4.google.com

### Cloudflare NTP [AS13335]:

time.cloudflare.com

### Facebook NTP [AS32934]:

time.facebook.com

time1.facebook.com

time2.facebook.com

time3.facebook.com

time4.facebook.com

time5.facebook.com

### Microsoft NTP server [AS8075]:

time.windows.com

### Apple NTP server [AS714, AS6185]:

time.apple.com

time.euro.apple.com

### DEC/Compaq/HP:

clepsydra.dec.com/clepsydra.labs.hp.com/clepsydra.hpl.hp.com

### NIST Internet Time Service (ITS) [AS49, AS104]:

time-a-g.nist.gov

time-b-g.nist.gov

time-c-g.nist.gov

time-d-g.nist.gov

time-a-wwv.nist.gov

time-b-wwv.nist.gov

time-c-wwv.nist.gov

time-d-wwv.nist.gov

time-a-b.nist.gov

time-b-b.nist.gov

time-c-b.nist.gov

time-d-b.nist.gov

time.nist.gov

utcnist.colorado.edu

utcnist2.colorado.edu

### VNIIFTRI:

#### Stratum 1:

ntp1.vniiftri.ru

ntp2.vniiftri.ru

ntp3.vniiftri.ru

ntp4.vniiftri.ru

ntp1.niiftri.irkutsk.ru

ntp2.niiftri.irkutsk.ru

vniiftri.khv.ru

vniiftri2.khv.ru

#### Stratum 2:

ntp21.vniiftri.ru

### Mobatime:

#### Stratum 1:

ntp.mobatime.ru

### NTP SERVERS:

#### Stratum 1:

ntp1.stratum1.ru

ntp2.stratum1.ru

ntp3.stratum1.ru

ntp4.stratum1.ru

ntp5.stratum1.ru

#### Stratum 2:

ntp2.stratum2.ru

ntp3.stratum2.ru

ntp4.stratum2.ru

ntp5.stratum2.ru

### Stratum1:

#### Stratum 1:

stratum1.net

### Company Delfa Co. Ltd. [AS8915]:

ntp.ru

### ACO.net [AS1853]:

ts1.aco.net

ts2.aco.net

### Berkeley [AS25]:

#### Stratum 1:

ntp1.net.berkeley.edu

ntp2.net.berkeley.edu

### Georgia State University [AS10631]:

ntp.gsu.edu

### University of Saskatchewan [AS22950]:

tick.usask.ca

tock.usask.ca

### NSU [AS3335]:

#### Stratum 2:

ntp.nsu.ru

### RSU [AS47124]:

#### Stratum 1:

ntp.rsu.edu.ru

### National Institute of Information and Communications Technology [AS9355]:

ntp.nict.jp

### HE.net [AS6939]:

clock.nyc.he.net

clock.sjc.he.net

### TRC Fiord [AS28917]:

ntp.fiord.ru

### Netnod NTP service [AS57021]:

#### Stratum 1:

Göteborg:

gbg1.ntp.se

gbg2.ntp.se

Malmö:

mmo1.ntp.se

mmo2.ntp.se

Stockholm:

sth1.ntp.se

sth2.ntp.se

Sundsvall:

svl1.ntp.se

svl2.ntp.se

Anycast address for nearest NTP server of the above:

ntp.se

### YYCIX NTP [AS396515]:

ntp.yycix.ca

### MSK-IX NTP [AS43832]:

#### Stratum 1:

ntp.ix.ru

### Trabia-Network [AS43289]:

time-a.as43289.net

time-b.as43289.net

time-c.as43289.net

### RIPE [AS3333]:

ntp.ripe.net

### Internet Systems Consortium [AS1280]:

clock.isc.org (prev ntp.isc.org)

### TimeNL/SIDN Labs [AS1140]:

ntp.time.nl (ntp1.time.nl)

### Kantonsschule Zug [AS34288]:

ntp0.as34288.net

ntp1.as34288.net

### INTERNET MULTIFEED CO. [AS7521]:

ntp1.jst.mfeed.ad.jp

ntp2.jst.mfeed.ad.jp

ntp3.jst.mfeed.ad.jp

### NTP Pool:

pool.ntp.org

0.pool.ntp.org

1.pool.ntp.org

2.pool.ntp.org

3.pool.ntp.org

europe.pool.ntp.org

0.europe.pool.ntp.org

1.europe.pool.ntp.org

2.europe.pool.ntp.org

3.europe.pool.ntp.org

asia.pool.ntp.org

0.asia.pool.ntp.org

1.asia.pool.ntp.org

2.asia.pool.ntp.org

3.asia.pool.ntp.org

ru.pool.ntp.org

0.ru.pool.ntp.org

1.ru.pool.ntp.org

2.ru.pool.ntp.org

3.ru.pool.ntp.org

0.gentoo.pool.ntp.org

1.gentoo.pool.ntp.org

2.gentoo.pool.ntp.org

3.gentoo.pool.ntp.org

0.arch.pool.ntp.org

1.arch.pool.ntp.org

2.arch.pool.ntp.org

3.arch.pool.ntp.org

0.fedora.pool.ntp.org

1.fedora.pool.ntp.org

2.fedora.pool.ntp.org

3.fedora.pool.ntp.org

0.opensuse.pool.ntp.org

1.opensuse.pool.ntp.org

2.opensuse.pool.ntp.org

3.opensuse.pool.ntp.org

0.centos.pool.ntp.org

1.centos.pool.ntp.org

2.centos.pool.ntp.org

3.centos.pool.ntp.org

0.debian.pool.ntp.org

1.debian.pool.ntp.org

2.debian.pool.ntp.org

3.debian.pool.ntp.org

0.askozia.pool.ntp.org

1.askozia.pool.ntp.org

2.askozia.pool.ntp.org

3.askozia.pool.ntp.org

0.freebsd.pool.ntp.org

1.freebsd.pool.ntp.org

2.freebsd.pool.ntp.org

3.freebsd.pool.ntp.org

0.netbsd.pool.ntp.org

1.netbsd.pool.ntp.org

2.netbsd.pool.ntp.org

3.netbsd.pool.ntp.org

0.openbsd.pool.ntp.org

1.openbsd.pool.ntp.org

2.openbsd.pool.ntp.org

3.openbsd.pool.ntp.org

0.dragonfly.pool.ntp.org

1.dragonfly.pool.ntp.org

2.dragonfly.pool.ntp.org

3.dragonfly.pool.ntp.org

0.pfsense.pool.ntp.org

1.pfsense.pool.ntp.org

2.pfsense.pool.ntp.org

3.pfsense.pool.ntp.org

0.opnsense.pool.ntp.org

1.opnsense.pool.ntp.org

2.opnsense.pool.ntp.org

3.opnsense.pool.ntp.org

0.amazon.pool.ntp.org

1.amazon.pool.ntp.org

2.amazon.pool.ntp.org

3.amazon.pool.ntp.org

## Other:

### .mil:

tick.usno.navy.mil

tock.usno.navy.mil

ntp2.usno.navy.mil

### .edu:

utcnist2.colorado.edu

timekeeper.isi.edu

rackety.udel.edu

mizbeaver.udel.edu

otc1.psu.edu

gnomon.cc.columbia.edu

navobs1.gatech.edu

navobs1.wustl.edu

now.okstate.edu

ntp.colby.edu

ntp-s1.cise.ufl.edu

### .com:

ntpstm.netbone-digital.com

nist1.symmetricom.com

### .net:

t2.timegps.net

gps.layer42.net

ntp-ca.stygium.net

sesku.planeacion.net

ntp0.nl.uu.net

ntp1.nl.uu.net

navobs1.oar.net

ntp-galway.hea.net

### .org:

ntp1.ona.org

## .de:

time.fu-berlin.de

atom.uhr.de

ntps1-0.cs.tu-berlin.de

ntps1-1.cs.tu-berlin.de

ntps1-0.uni-erlangen.de

ntps1-1.uni-erlangen.de

ntp1.fau.de

ntp2.fau.de

ntp.dianacht.de

zeit.fu-berlin.de

ptbtime1.ptb.de

ptbtime2.ptb.de

rustime01.rus.uni-stuttgart.de

rustime02.rus.uni-stuttgart.de

### .nl:

chime1.surfnet.nl

ntp.vsl.nl

### .at:

asynchronos.iiss.at

### .cz:

ntp.nic.cz

time.ufe.cz

### .pl:

ntp.fizyka.umk.pl

tempus1.gum.gov.pl

tempus2.gum.gov.pl

### .ro:

ntp1.usv.ro

ntp3.usv.ro

### .se:

timehost.lysator.liu.se

time1.stupi.se

### .ca:

time.nrc.ca

clock.uregina.ca

### .mx:

cronos.cenam.mx

ntp.lcf.mx

### .es:

hora.roa.es

minuto.roa.es

### .it:

ntp1.inrim.it

ntp2.inrim.it

### .be:

ntp1.oma.be

ntp2.oma.be

### .hu:

ntp.atomki.mta.hu

### .eus:

ntp.i2t.ehu.eus

### .ch:

ntp.neel.ch

### .cn:

ntp.neu.edu.cn

### .jp:

ntp.nict.jp

### .br:

ntps1.pads.ufrj.br

### .cl:

ntp.shoa.cl

### .int:

time.esa.int

time1.esa.int

http://support.ntp.org/bin/view/Servers/StratumOneTimeServers

http://support.ntp.org/bin/view/Servers/StratumTwoTimeServers

http://support.ntp.org/bin/view/Servers/NTPPoolServers

http://www.pool.ntp.org/zone/@

http://www.pool.ntp.org/zone/asia

http://www.pool.ntp.org/zone/europe

http://www.pool.ntp.org/zone/north-america

http://www.pool.ntp.org/zone/oceania

http://www.pool.ntp.org/zone/south-america

https://time.nl/

https://time.nl/index_en.html

### Auto Backup via Email

1. Set email
   ```
   /tool  e-mail
   set  address=mail.pro2pray.com from=auto_backup@pro2pray.com password=\
   passowrd port=587 start-tls=yes user=\
   auto_backup@pro2pray.com
   ```
2. Create script auto-backup-email

   ```
   /system  script
   add dont-require-permissions=no name=Auto-Backup-Email owner=ubnt10 policy=\
   ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source=":\
   log info \"Auto Backup Started\"\r\
   \n:global date [/system clock get date]\r\
   \n:global d [:pick \$date 4 6]\r\
   \n:global m [:pick \$date 0 3]\r\
   \n:global y [:pick \$date 7 11]\r\
   \n:global id [/system identity get name]\r\
   \n\r\
   \n:global backupfile (\"Auto Backup \" .\$id.\"  \".[/system clock get time\
   ].\"@\".\"\$d-\$m-\$y\")\r\
   \n/system backup save name=\$backupfile\r\
   \n:log info \"backup pausing for 10s\"\r\
   \n:delay 10s\r\
   \n:log info \"backup will send to mail\"\r\
   \n/tool e-mail send to=\"dev.adipurnomo@gmail.com\" subject=\"Auto Backup \
   \$id\" from=\"auto_backup@pro2pray.com\" file=\$backupfile server=103.251.\
   44.209\r\
   \n:delay 30s\r\
   \n/file remove \$backupfile\r\
   \n:log info \"Auto Backup Finished\""
   ```

3. Create scheduer (auto repeat every 7 days)

   ```
   /system scheduler
   add interval=1w name="Weekly Backup" on-event=Auto-Backup-Email policy=\
   ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
   start-date=dec/01/2020 start-time=07:00:00
   ```

4. Essentials Source native script
   ```
   :log info "Auto Backup Started"
   :global date [/system clock get date]
   :global d [:pick $date 4 6]
   :global m [:pick $date 0 3]
   :global y [:pick $date 7 11]
   :global id [/system identity get name]
   :global backupfile ("Auto Backup " .$id." ".[/system clock get time]."@"."$d-$m-$y")
   /system backup save name=$backupfile
   :log info "backup pausing for 10s"
   :delay 10s
   :log info "backup will send to mail"
   /tool e-mail send to="dev.adipurnomo@gmail.com" subject="Auto Backup $id" from="auto_backup@pro2pray.com" file=$backupfile server=103.251.44.209
   :delay 30s
   /file remove $backupfile
   :log info "Auto Backup Finished"
   ```
