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
Osoite: `domain.tld`

### Nginx

Sitten nginx kontti, jolla saadaan ns. reverse proxy ja oma domain sekä ssl