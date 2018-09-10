This example allows for passing secret to service

Steps followed
1. Initialize swarm cluster:  
  `docker swarm init`
1. Create secret database credentials:  
  `echo "yourpassword" | docker secret create db_password -`
  `echo "host" | docker secret create db_host -`
  `echo "database name" | docker secret create db_database -`
  `echo "user" | docker secret create db_user -`
  `echo "port" | docker secret create db_port -`

1. Build image:  
  `docker build . -t santam-claimcards`
1. Run stack service:  
  `docker stack deploy -c docker-compose.yml santam-claimcards-stack`

## Expected output:
Output:  
```
Wait for a min or two and the service will be up
```