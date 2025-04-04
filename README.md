# Oma pilvi

Tämä sisältää kaikki Docker compose filut mitä olen käyttänyt oman "pilven" rakentamiseen.

Tämä tulee elämään jonkun verran ja koitan muistaa dokumentoida tätä suht. hyvin.

## Vaatimukset

Palvelin minne tämä asennetaan. Sinne laitettu Docker ja Docker compose.

Oma domain. 

## Setuppi

Tässä tehdään seuraavanlainen setuppi:

### Immich

Kuvia varten Immich kontti.  
Osoite: `kuvat.domain.tld`

### Nextcloud 

Tiedostoja varten Nextcloud kontti.  
Osoite: `tiedostot.domain.tld`

### Traefik

Traefik hoitaa reverse proxyn ja SSL sertifikaatit.  
Osoite: `traefik.domain.tld`

### Calibre web

Kirjoille oma paikka.  
Osoite: `kirjat.domain.tld`

### Open WebUI

Open WebUI AI platform
Osoite: `ai.domain.tld`

### Glance

Etusivu koko "pilvelle".  
Osoite: `domain.tld`

## Asennus

Asenna docker ja docker compose palvelimelle.

Luo seuraavat docker verkot:

```
docker network create traefik-network

docker network create nextcloud-network

docker network create immich-network

docker network create glance-network

docker network create calibre-network

docker network create openwebui-network
```

Kloonaa repo palvelimelle.  

Määritä .env tiedostot

Aja kontit ylös komennolla:

```docker compose up -d```

## Linkkejä

- https://github.com/heyvaldemar/nextcloud-traefik-letsencrypt-docker-compose
- https://immich.app/docs/install/docker-compose
- https://immich.app/docs/administration/reverse-proxy/
- https://github.com/crocodilestick/Calibre-Web-Automated