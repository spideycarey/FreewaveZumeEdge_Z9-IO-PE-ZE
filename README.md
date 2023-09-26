# FreewaveZumeEdge_Z9-IO-PE-ZE
Configure Zum Edge Z9-IO-PE-ZE
1. Log into Web GUI via ethernet
   - Use Web Browser
     - LAN Default IP is `192.168.111.110`
     - Use Port `80`
     - username/password is admin/admin
    
1. SSH into device via ethernet
   - Use Putty software
     - LAN 2 Default IP is `192.168.111.110`
     - Use Port `22`

2. Enter Username and Password
   - default username is `devuser`
   - default password is `devuser`

3. Enter Following commands
   - Type `sudo mount –o remount,size=200000000 /tmp`
   - Type `sudo apt-get update`
   - Type `sudo apt-get upgrade`
   - Type `sudo apt install python3-django`
   - Type `sudo apt install python3-jsonschema`
   - Type `sudo apt-get clean`
     
5. Move install file onto device
   - From windows PC, open CMD
   - navigate to directory in windows where file is
   - Type `pscp -scp autosol.deb devuser@10.106.1.225:/home/devuser/`
   - Enter password for devuser and file should transfer
  
6. Install eACM
    - In Putty type `sudo apt install /home/devuser/autosol.deb`
    - 
