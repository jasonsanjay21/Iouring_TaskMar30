# Iouring_Task_Mar30

## Update the instance
Install docker and docker compose
Run dockre compose with
docker-commpose up -d --build(to run in detach mode)
Clone the repo and cd to the directory

## Check if the auth_token has been generated inside the redis container 
If not,
&:~ docker exec -it redis_container_name redis-cli
>>GET auth_token
>>(nil)
>> SET auth token = my-secret-token
>>OK

Restart the nginx and flask_app containers
## Test with
&:~ curl -H "X-Auth-Token: my-secret-token" http://localhost/
{"message":"Welcome to the Python Service!"}
&:~ curl -H "X-Auth-Token: my-secret-tokennn" http://localhost/
http://52.65.207.33/
<html>
<head><title>401 Authorization Required</title></head>
<body>
<center><h1>401 Authorization Required</h1></center>
<hr><center>openresty/1.27.1.1</center>
</body>
</html>


