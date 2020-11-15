# My Essentials Tools for Working

- Winbox
- Mikrotik Voucher Generator
- Ubiquiti Firmware (XM, XW)
- Ubnt Discovery

### Here how to show compliance test in ubnt radio

*This only works on ubnt firmware < v6.1.6*

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


###  How to change country in ubnt devices without reset

1. Open ssh tools like  [putty](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.74-installer.msi)  or terminal if using linux
2. Login to your ubnt devices
3. Then show prompt, click yes
4. Type your password
5. You will be in console of ubnt
6. Add compliance test by running command `touch /etc/persistent/ct`
7. Get code of current country with command `cat /tmp/system.cfg | grep code`
8. Then code will show like this
	>radio.1.countrycode=360
	>radio.countrycode=360
9. Then find country code u want to set
10. Change country code in system.cfg by using command `sed -i 's/countrycode=360/countrycode=511/g' /tmp/system.cfg`
11. Change country code in running.cfg by using command `sed -i 's/countrycode=360/countrycode=511/g' /tmp/running.cfg`
12. Then check country code has changed with command `cat /tmp/system/cfg` 
13. If country code has changed will be like this
	>radio.1.countrycode=511
	>radio.countrycode=511
14. Save config by running command `save`
15. Reboot devices to apply new config by running command `reboot`
16. Then country will be changed.

Full of country code available here
|Country Code	  |Country			            |
|---------------|-------------------------|
|32				      | Argentina		            |
|51				      | Armenia			            |
|533			      | Aruba				            |
|36				      | Australia		            |
|40				      | Austria			            |
|31				      | Azerbaijan	            |
|48				      | Bahrain		            	|
|52				      | Barbados	            	|
|112			      | Belarus		            	|
|56				      | Belgium		            	|
|84				      | Belize		            	|
|68				      | Bolivia		            	|
|70				      | Bosnia and Herzegovina  |
|76				      | Brazil			            |
|96				      | Brunei Darussalam	      |
|100			      | Bulgaria		           	|
|116			      | Cambodia			          |
|124			      | Canada			            |
|152			      | Chile				            |
|156			      | China				            |		
|170			      | Colombia		           	|
|511			      | Compliance Test       	|
|188			      | Costa Rica	          	|
|191			      | Croatia			            |
|196			      | Cyprus		            	|
|203			      | Czech Republic	        |
|208			      | Denmark		            	|
|214			      | Dominican Republic      |
|218			      | Ecuador			            |
|818			      | Egypt			            	|
|222			      | El Salvador		          |
|233			      | Estonia		            	|
|246			      | Finland			            |
|250			      | France		            	|
|268			      | Georgia		            	|
|276			      | Germany		            	|
|300			      | Greece		            	|
|304			      | Greenland		            |
|308			      | Grenada		            	|
|316			      | Guam			            	|
|320			      | Guatemala			          |
|332			      | Haiti			            	|
|340			      | Honduras			          |
|344			      | Hong Kong			          |
|348			      | Hungary		            	|
|352			      | Iceland		            	|
|356			      | India			            	|
|360			      | Indonesia			          |
|368			      | Iraq			            	|
|372			      | Ireland		            	|
|376			      | Israel		            	|
|380			      | Italy			            	|
|388			      | Jamaica		            	|
|400			      | Jordan		            	|
|404			      | Kenya			            	|
|410			      | Korea Republic        	|
|414			      | Kuwait			            |
|428			      | Latvia		            	|
|422			      | Lebanon		            	|
|438			      | Liechtenstein	          |
|440			      | Lithuania			          |
|442			      | Luxembourg		          |
|446			      | Macau			            	|
|807			      | Macedonia			          |
|458			      | Malaysia			          |
|470			      | Malta			            	|
|484			      | Mexico		            	|
|492			      | Monaco		            	|
|504			      | Morocco		            	|
|524			    | Nepal				              |
|528			    | Netherlands	            	|
|530			    | Netherlands Antilles      |
|554			    | New Zealand	            	|
|566			    | Nigeria			              |
|578			    | Norway			              |
|512			    | Oman				              |	
|586		    	| Pakistan		            	|
|591			    | Panama			              |	
|598			    | Papua New Guinea	        |
|604			    | Peru				              |
|608			    | Philippines	            	|
|616			    | Poland			              |
|620			    | Portugal		            	|
|630			    | Puerto Rico (U.S. territory)|
|634			    | Qatar				              |
|642			    | Romania			              |
|643			    | Russia			              |
|646			    | Rwanda			              |
|652			    | Saint Barthelemy	        |
|682			    | Saudi Arabia		          |
|891			    | Serbia and Montenegro     |
|702			    | Singapore		            	|
|703			    | Slovakia		            	|
|705			    | Slovenia		            	|
|710			    | South Africa		          |
|724			    | Spain				              |
|144			    | Sri Lanka		            	|
|752			    | Sweden			              |
|756			    | Switzerland           		|
|158			    | Taiwan			              |
|764			    | Thailand		            	|
|780			    | Trinidad and Tobago       |
|788			    | Tunisia			              |
|792			    | Turkey			              |
|804			    | Ukraine		            	  |
|784			    | United Arab Emirates      |
|826			    | United Kingdom	          |
|840			    | United States		          |
|858			    | Uruguay			              |
|860		    	| Uzbekistan		            |
|862			    | Venezuela			            |
|704		    	| Viet Nam			            |
