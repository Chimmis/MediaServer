Need docker and docker-compose installed.

Basic steps:
1. Configure file paths to your liking in .env file
2. Run docker-compose up
3. Configure jacket with the rss feeds you want
4. localhost:8080 - configure torrent client
5. Connect radarr and sonarr to jacket (localhost:9117 should work) via settings
6. Connect radarr and sonarr to torrent client via settings
7. Configure radarr/sonarr/plex however you like. 


Service map:

Plex - localhost:32400
Sonarr - localhost:8989
Radarr - localhost:7878
Client - localhost:8080
Jackett - localhost:9117

How it works: 

Use Sonarr and Radarr to search for the shows and movies of wanted quality. These services use Jackett aggregated rss feed to search for the files, then use the client to download them. Then the shows are stored in a categorized fashion for plex to consume. 