# Lilee STS-1000 Docker Diag Shell container service reference design

## Reference only - Please repackage the image with private access credentials for production deployment!!

* **Prepackaged tools**</br>
  * Ubuntu 18.04 base OS
  * sshd (mapped to TCP port 2222)
  * docker-ce-cli 18.09.9
  * basic network tools
  * basic ps tool
* **Prepackaged access credentials**</br>
  * user - docker
  * password - ChangePassword!!!
* **Enabling Diag Shell service**</br>
  * Refer to the Prerequisite sevction in https://github.com/lileesystems-com/sts-1000/tree/master/profiles
  * Procedure through STS-1020 LileeOS CLI
  <pre>
  localhost.localdomain > create application name diagshell
  localhost.localdomain > update application name diagshell profile package https://github.com/lileetechnology/sts-1000/raw/master/profiles/diagshell.zip
  localhost.localdomain > config application name diagshell enable
  localhost.localdomain > save configuration
  localhost.localdomain > show application all
  Name       | State   | Started At                    
  -------------------------------------
  diagshell   running   2021-03-03T22:25:44.453628954Z
  </pre>
