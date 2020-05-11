Oura Ring with Metabase

Oura is a great tool for tracking your sleeping and seeing how you are doing now.
Metabase is open source BI-tool that connects to multiple databases and you can crunch your data however you want.

Requirements for this combo
- Oura Ring and access to Oura cloud
- CSV of all your Oura data https://cloud.ouraring.com/trends
- Docker and Docker-compose installed

Steps
1. Install Docker & Docker-compose
2. Download Oura data. From the download "choose all" columns
3. Move the downloaded csv to this folder, "oura_metabase", and rename it to "oura_org.csv"
4. Run "docker-compose up -d && sh install.sh && docker-compose exec postgres psql -U postgres -d postgres -a -f /tmp/commands.sql"
7. Navigate to http://localhost:3000/ and wait for Metabase to be ready
8. Create user 
9. Add your data
- Choose PostgreSQL
- Name = My Oura
- host = postgres
- port = 5432
- database name = postgres
- database username = metabase
- database password = metabase
10. Complete the process
11. View your Oura Data!