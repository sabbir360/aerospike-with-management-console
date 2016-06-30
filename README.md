### Aerospike Database and with Console
##### AeroSpike Sever config
To make your first aerospike database
- Open your favourite console
- Pull AeroSpike Server from docker hub using this command `docker pull aerospike/aerospike-server`
- Run below command 
   For Linux/Mac
    `mkdir ~/aerospike && mkdir ~/aerospike/data`
    and then 
	`docker run -tid \   
	-v /home/ubuntu/aerospike/data:/opt/aerospike/data \
	--name aerospike_server -p 3000:3000 -p 3001:3001 -p 3002:3002 -p 3003:3003 \
	aerospike/aerospike-server`. 
	Notice that **/home/ubuntu** is your user directory. **aerospike/data** is directory where AeroSpike data will be stored.	
    For windows 
    `mkdir C:\aerospike\data`
    and then 
    `docker run -tid \   
	-v C:\aerospike\data:/opt/aerospike/data \
	--name aerospike_server -p 3000:3000 -p 3001:3001 -p 3002:3002 -p 3003:3003 \
	aerospike/aerospike-server`.

- Pull aerospike AMC Web Console 
	`docker pull sabbir1cse/amc_aerospike_web_console`
- Run it 
	`run -itd -p 1001:8081 --name aerospike_web_console sabbir1cse/amc_aerospike_web_console`
- Get inside Console Container
	`docker exec -it aerospike_web_console bash`
	and then
	`./entrypoint.sh`
- Hit your host:1001 and follow instruction 