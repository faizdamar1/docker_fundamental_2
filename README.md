download regsitry psql

perintah untuk membuat images psql dan env
sudo docker run -d \
-p 5433:5432 --name docker_fullstack\ 
-e POSTGRES_USER=postgres \
-e POSTGRES_PASSWORD=postgres \
-e POSTGRES_DB=docker_fullstack \
-v $(pwd)/postgres/init.sql:/docker-entrypoint-initdb.d/initsql.sql postgres


perintah untuk menjalankan cmd local di docker
sudo docker exec 
-it nice_carver[nama_kontainer] psql 
-U postgres 
-W docker_fullstack[nama_database] [enter password] postgres

perintah export env
export DB_HOST=localhost
export DB_PORT=5433
export DB_USER=postgres
export DB_PASSWORD=postgres
export DB_DATABASE=docker_fullstack
