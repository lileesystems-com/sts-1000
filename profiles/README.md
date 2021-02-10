# Usage instructiuons
* **Prerequisite**</br>
  * Platform: Lilee STS-1000 series with a working disk drive in SATA 0
  * LileeOS version: LileeOS 4.7+
  * Do the following if the application framework is currently in app-engine mode
  <pre>
  localhost.localdomain > show application framework 
  App-Engine
  localhost.localdomain > update application framework container
  ...
  localhost.localdomain > reboot
  </pre>
* **Enabling PulseAudio service**</br>
<pre>
localhost.localdomain > update application storage volume create name paconfig sata 0
localhost.localdomain > create application name pulseaudio
localhost.localdomain > update application name pulseaudio profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/pulseaudio.zip
localhost.localdomain > config application name pulseaudio enable 
localhost.localdomain > show application all
Name       | State       | Started At
-------------------------------------
pulseaudio   running   2020-11-02T23:21:24.835718155Z
</pre>
* **Enabling X.Org service**</br>
<pre>
localhost.localdomain > create application name xorg
localhost.localdomain > update application name xorg profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/xorg.zip
localhost.localdomain > config application name xorg enable 
localhost.localdomain > show application all
Name       | State   | Started At                    
-----------------------------------------------------
pulseaudio   running   2020-11-02T23:21:24.835718155Z
xorg         running   2020-11-02T23:24:31.728142807Z
</pre>
* **Enabling DiagShell service**</br>
<pre>
localhost.localdomain > create application name diagshell
localhost.localdomain > update application name diagshell profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/diagshell.zip
localhost.localdomain > config application name diagshell enable 
localhost.localdomain > show application all
Name       | State   | Started At                    
-----------------------------------------------------
diagshell   running   2021-02-10T04:31:30.944566921Z
</pre>
** Get into the diagshell service (using the packaged credentials and ssh port mapping) - *ssh docker@STS_IP_ADDRESS -p 2222*
