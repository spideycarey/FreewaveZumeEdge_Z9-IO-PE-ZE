# FreewaveZumeEdge_Z9-IO-PE-ZE
Configure Zum Edge Z9-IO-PE-ZE
1. Log into Web GUI via ethernet
   - Use Web Browser
     - LAN Default IP is `192.168.111.100`
     - Use Port `80`
     - username/password is admin/admin
2. Update NTP Setting
   - Go to 'NTP' and update 'NTP Address1' to 10.254.0.10

3. Update network settings to connect to internet.  Need to update IP, Netmask, Gateway and both name servers manually to connect to internet.
    
4. SSH into device via ethernet
   - Use Putty software
     - Use new IP address that is also internet connected
     - Use Port `22`

5. Enter Username and Password
   - default username is `devuser`
   - default password is `devuser`

6. Enter Following commands
   - Type `sudo mount -o remount,size=200000000 /tmp`
   - Type `sudo apt-get update`
     
7. Move install file onto device
   - From windows PC, open CMD
   - navigate to directory in windows where file is
   - Type `pscp -scp C:\autosol_3.3.5.1-generic_all.deb devuser@10.106.1.225:/home/devuser/`
   - Enter password for devuser and file should transfer
  
8. Install eACM
    - In Putty type `sudo apt install /home/devuser/autosol_3.3.5.1-generic_all.deb`
    - type `sudo -u postgres createdb ASIServerDB`
    - type `sudo -u postgres psql ASIServerDB`
    - type `ALTER USER postgres WITH PASSWORD 'postgres';`
    - type `\q`
    - type `/usr/apps/ASIEdgeManager/core/restart`
    - 
