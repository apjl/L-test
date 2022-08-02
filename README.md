# L-vertailu
Lämmitystapojen vertailu säädatan perusteella.

## Yleistä
L-vertailu on työkalu keskuslämmityksellä varustetun rakennuksen lämmityskustannusten arviointiin. Sen idea on määritellä rakennukselle ja sen patteriverkostolle lämpöresistanssit tunnetun vuosikulutuksen perusteella ja sen jälkeen soveltaa näitä lämpöresistansseja tunti tunnilta todelliseen menneeseen lämpötila ja sähkönhinta dataan. Tämä mahdollistaa eri investointivaihtoehtojen vertailun ja investointien järkevyyden arvioinnin nimenomaan oman paikallisen säädatan perusteella eli esimerkiksi oman asuinpaikan toteutuneet lämpötilajakaumat ja niiden korrelaatio pörssisähkön hinnanvaihteluiden suhteen tulee otetuksi huomioon.

Säädata omalle sijainnille on saatavissa ilmatieteenlaitokselta:
https://www.ilmatieteenlaitos.fi/havaintojen-lataus

Pörssisähkön menneet hinnat löytyvät ilmaiseksi esim. Vattenfallin sivuilta:
https://www.vattenfall.fi/sahkosopimukset/porssisahko/tuntispot-hinnat-sahkoporssissa/

## Vertailussa olevat lämmitystavat

- Suora sähkölämmitys kiinteä sopimus
   - Suora sähkölämmitys kiinteällä käyttäjän määrittelemällä sähkön hinnalla.
- Suora sähkölämmitys pörssisähkösopimus
   - Suora sähkölämmitys tunneittain päivittyvällä sähkön hinnalla ja käyttäjän määrittelemällä marginaalilla.
- Varaava sähkölämmitys yösähköllä
   - Varaava sähkölämmitys pörssisähköllä ja kahdella eri siirtotariffilla. Varaajan ja pääsulakkeen koko määriteltävissä.
- Varaava sähkölämmitys yösähköllä ja "älykkäällä" ohjauksella
   - Älykäs ohjaus tarkoittaa sitä, että yösähkön alkaessa ekstrapoloidaan sen hetkisestä kulutuksesta arvio yöllä tarvittavasta lämmitystehosta. Tämä yhdistettynä tietoon varaajassa olevasta energiamäärästä ja suurimmasta varaajan lataustehosta kertoo kuinka monena tuntina varaajaa täytyy yön aikana ladata. Koska pörssisähkön hinta seuraavalle päivälle on yötariffin alkaessa jo tiedossa, voidaan varaajan lataus suorittaa halvimpien tuntien aikana.
- VILP pörssisähköllä
   - VILP ilman varaajaa pörssisähköllä. VILP mallinnus perustuu nimimerkin zadah lämpöpumput.info-foorumilla julkaisemaan laskuriin: https://lampopumput.info/foorumi/threads/veden-l%C3%A4mp%C3%B6tilan-vaikutus-coppiin.6311/.
- VILP kiinteä sopimus
   - VILP ilman varaajaa kiinteällä sähkön hinnalla. VILP mallinnus perustuu nimimerkin zadah lämpöpumput.info-foorumilla julkaisemaan laskuriin: https://lampopumput.info/foorumi/threads/veden-l%C3%A4mp%C3%B6tilan-vaikutus-coppiin.6311/.


## Muut käyttökohteet
Työkalua hieman muokkaamalla tai perättäisiä ajoja ajamalla on mahdollista tutkia lisäksi mm. seuraavia asioita:

- Optimaalinen sulakekoko varaavan lämmityksen kanssa. Investoinnin järkevyyden arviointi suhteessa saavutettuun säästöön.
- Optimaalinen energiavaraajan kapasiteetti varaavan lämmityksen kanssa.
- Sisälämpötilan laskemisen vaikutus. Etenkin VILP-tapauksessa tämä ei ole suoraviivaista koska sisälämpötilan laskeminen laskee myös menoveden lämpötilaa ja täten parantaa lämpöpumpun suorituskykyä.

## Tiedossa olevat puutteet / virheet

 - Lämmintä käyttövettä ei käsitelty erikseen.
 - Vaihesiirto ulkoilman lämpötilan muutoksista lämmitystarpeeseen on jätetty mallintamatta. Sekä talon lämpöhäviöt, että patteriverkon toiminta mallinetaan yksinkertaisella lämpöresistanssilla, kapasitansseista ja resistansseista koostuvat tarkemman sijaiskytkennän sijaan.
 - Tuuli on jätetty huomiotta. Tuuli todennäköisesti tylpistäisi tehontarpeen jakaumaa hieman niin, että kaikkein isoin tehontarve ei olisi aivan niin iso kuin nyt on vuosikulutuksesta arvioitu ja vastaavasti lähes kaikkein suurinta tehontarvetta olisi tilastollisesti suurempi osuus kuin nyt vaikuttaa olevan. Tämä päätelmä perustuu siihen, että kaikkein kylmimmillä säillä harvoin tuulee merkittävästi.
