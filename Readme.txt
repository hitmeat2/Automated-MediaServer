Login <-----------			
					The Login: "root" 
					Password: "mediaserver"
					
Chang to the root Directory <------------
													$cd /
		
Install Critical Programs <-----------
													$yum -y install man nano wget perl zip unzip
		
Make Mountable Directory <------------
													$mkdir /MediaServerTools
		
Mount Configuration Drive <------------------
													$mount /dev/sda1 /MediaServerTools
						
Chang to the MediaServerTools Directory <------------
													$cd /MediaServerTools/MediaServer
													
Run Configuration Program <------------------
													$perl MediaServerConfig	