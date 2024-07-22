# installed ruby, docker
# prepared docker to run a postgres container
```sh
docker network create some-network
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' some-postgres

# test the connection
psql -h 172.18.0.2 -U postgres

# installed ruby 2.7.3 using rbenv
# also configured as show in documentation examples

# important to run this (and set on profile for further references): 
export GEM_HOME=$HOME/.gem

# All tests on both tasks passed successfully without changing the job_spec files.

```
