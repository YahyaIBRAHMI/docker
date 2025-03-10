docker run --name postgres_container \
  -e POSTGRES_USER=dataiku \
  -e POSTGRES_PASSWORD=dataiku \
  -e POSTGRES_DB=sql_database \
  -p 5432:5432 \
  -itd postgres:latest
