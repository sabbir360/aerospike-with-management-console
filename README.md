### Aerospike Database and with Console
##### AeroSpike Sever config
To make your first aerospike database
1. First pull "docker pull aerospike/aerospike-server"
2. Run this or create bash file with it 

	docker run -tid \   
	-v /sabbir/docker_lab/containers/thunder_charm/aerospike/data:/opt/aerospike/data \
	--name aerospike_server -p 3000:3000 -p 3001:3001 -p 3002:3002 -p 3003:3003 \
	aerospike/aerospike-server

3. Pull aerospike AMC Web Console 
	
	docker pull sabbir1cse/amc_aerospike_web_console

4. Run it 
	run -itd -p 1001:8081 --name aerospike_web_console sabbir1cse/amc_aerospike_web_console

5. Exec in it 
	
	docker exec -it aerospike_web_console bash
	./entrypoint.sh

6. Hit your host:1001 and follow instruction