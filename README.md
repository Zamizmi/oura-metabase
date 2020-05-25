# Oura Ring with Metabase

Oura is a great tool for tracking your sleeping and seeing how you are doing now.
Metabase is open source BI-tool that connects to multiple databases and you can crunch your data however you want.

## Requirements for this combo
- Oura Ring and access to Oura cloud
- CSV of all your Oura data https://cloud.ouraring.com/trends
- Docker and Docker-compose installed

## Running Metabase locally
1. Install [Docker](https://docs.docker.com/get-docker/) & [docker-compose](https://docs.docker.com/compose/install/)
2. Download Oura data [here](https://cloud.ouraring.com/trends). From the download "choose all" columns
3. Move the downloaded csv file to the root folder, and rename it to "oura_org.csv"
4. Run ```docker-compose up -d && sh install.sh && docker-compose exec postgres psql -U postgres -d postgres -a -f /tmp/commands.sql```
7. Navigate to http://localhost:3000/ and wait for Metabase to be ready

## First setup
1. Create user 
2. Setup a PostgreSQL DB
- Choose PostgreSQL
- Name = My Oura
- host = postgres
- port = 5432
- database name = postgres
- database username = metabase
- database password = metabase
<img width="657" alt="Näyttökuva 2020-5-25 kello 21 26 27" src="https://user-images.githubusercontent.com/22411478/82836608-7e251600-9ecf-11ea-974a-6a5d347d7ef1.png">
3. Complete the process

## Understanding why you shouldn't have that 10th cup of coffee at 9pm!
1. View your Oura Data in Metabase!
