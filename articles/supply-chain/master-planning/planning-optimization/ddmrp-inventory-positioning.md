---
title: Varaston asemointi
description: Tässä artikkelissa on tietoja varaston strategisesta asemoinnista, mikä tarkoittaa toimitusketjun erotuspisteiden määrittämistä. Näihin erotuspisteisiin voidaan muodostaa käytettävissä oleva varasto, joka auttaa lyhentämään läpimenoaikoja ja vaimentaa toimitusketjuun kohdistuvia haasteita.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186684"
---
# <a name="inventory-positioning"></a>Varaston asemointi

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Varaston strategisessa asemoinnissa määritetään toimitusketjuun erotuspisteitä, joihin voidaan muodostaa käytettävissä oleva varasto. Tätä menetelmää käytetään lähinnä lyhentämään läpimenoaikoja ja vaimentamaan toimitusketjuun kohdistuvia haasteita. Sen avulla voidaan lieventää piiskavaikutusta, koska kysynnän vaihtelua ei vaikuta koko toimitusketjuun. (*Piiskavaikutuksella* tarkoitetaan tilannetta, jossa pienet vähittäismyyntitason kysynnän vaihtelut aiheuttavat vähitellen suurenevaa kysynnän vaihtelua tukkumyynti-, jakelu-, valmistaja- ja raaka-ainetoimittajatasoilla.)

Varaston asemointi on ensimmäinen kysyntäperustaisen tarvelaskennan (DDMRP) vaihe.

## <a name="inventory-positioning-for-manufacturing"></a>Varaston asemointi valmistusteollisuudessa

Tässä osassa oleva esimerkki näyttää, miten varaston asemointipäätöksiä tehdään, jos kyse on tavanomaisen tyynytuotteen valmistuksesta. Tyynyllä on monitasoisen tuoterakenne, joka näkyy seuraavassa kuvassa.

![Esimerkki tyynytuotteen monitasoisesta tuoterakenteesta](media/ddmrp-bom-example.png "Esimerkki tyynytuotteen monitasoisesta tuoterakenteesta")

### <a name="choose-your-decoupling-points"></a>Erotuspisteiden valitseminen

Eropisteiden sijoituspaikkoja valittaessa seuraavia seikkoja kannattaa pohtia ehtoina kunkin tuoterakenteen nimikkeen osalta:

- Ulkoinen vaihtuvuus
- Varaston suorituskykykerroin ja joustavuus
- Tärkeiden toimintojen suojaaminen
- Asiakkaan toleranssiaika
- Myyntitilauksen näkyvyyshorisontti
- Markkinapotentiaalin läpimenoaika

Tyynyesimerkissä ensimmäinen erotuspiste voidaan sijoittaa *vaahtomuovipaloihin* seuraavien syiden vuoksi:

- Vaahtomuovipalojen valmistuksessa käytettyjen materiaalien hankkiminen on hankalaa ja saatavuus vaihtelee. Näin ollen *ulkoista vaihtuvuutta* koskeva ehto täyttyy.
- Vaahtomuovipalat voidaan leikata erimuotoisiksi ja -kokoisiksi, ja niistä voidaan luoda vaahtomuovitäytteitä muihin valmistettaviin tuotteisiin tyynyjen lisäksi. Niinpä *varaston suorituskykykerrointa ja joustavuutta* koskeva ehto täyttyy.

Seuraava erotuspiste voidaan sijoittaa *kangastarvikesarjaan*, joka on valmiiksi leikattu tyynykangas. Tämä erotuspiste voidaan valita esimerkiksi siksi, että käytössä on vain kankaanleikkuulaite. Se siis täyttää *tärkeiden toimintojen suojausta* koskevan ehdon.

Viimeinen erotuspiste voidaan sitten sijoittaa valmistuneen tyynynimikkeen kohdalle. Tämä erotuspiste voidaan valita siksi, että myynnissä on hyvin alhainen *asiakkaan toleranssiaika* ja koska *myyntitilauksen näkyvyyshorisontti* on melko lyhyt. Tämän vuoksi halutaan varmistaa, että varastoa on käytettävissä saapuvia tilauksia varten. Myös hinta voi olla korkeampi, kun läpimenoaika on näin lyhyt, ja juuri tähän *markkinapotentiaalin läpimenoaika* viittaa.

Tähän analyysiin perustuva tyynyn tuoterakenne näkyy seuraavassa kuvassa. Keltaiset varastosymbolit osoittavat erotuspisteet.

![Tuoterakenne-esimerkki ja korostetut erotuspisteet](media/ddmrp-bom-decoupling-example.png "Tuoterakenne-esimerkki ja korostetut erotuspisteet")

### <a name="calculate-your-decoupled-lead-time"></a>Erotetun läpimenoajan laskeminen

Tässä osassa käsitellään uusien läpimenoaikojen laskemista erotuspisteiden käyttöönottamisen jälkeen.

Seuraavassa kuvassa on edellisessä osassa aloitettu tyynyesimerkki, jossa läpimenoajat näkyvät harmaissa ruuduissa kunkin tuoterakennekomponentin vasemmassa yläkulmassa. Ruudun punainen ääriviiva osoittaa nimikkeet, jotka määrittävät kumulatiivista läpimenoaikaa (pisimpien läpimenoaikojen summa kullakin tuoterakennetasolla). Läpimenoaika on 21 päivää alusta aloitettaessa.

![Tuoterakenne-esimerkki ja läpimenoajat](media/ddmrp-bom-lead-times-example.png "Tuoterakenne-esimerkki ja läpimenoajat")

Aiemmin valittuja erotuspisteitä käytettäessä erotettuja nimikkeitä on kuitenkin aina varastossa. Niinpä niiden läpimenoaika on 0 (nolla). Tyynyn uusi läpimenoaika on nyt vain viisi päivää: kaksi päivää langan ostamiseen ja kolme päivää tyynyn valmistamiseen. Läpimenoaikaa kutsutaan nyt *erotetuksi läpimenoajaksi*.

![Esimerkki erotetusta läpimenoajasta](media/ddmrp-bom-decoupled-lead-time-example.png "Esimerkki erotetusta läpimenoajasta")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Varaston strateginen asemointi vähittäismyyntimallissa

Koska vähittäismyyjillä on varastossa vain valmiita tuotteita, tuoterakenne ei ole ongelma. Vähittäismyyjät voivat silti käyttää DDMRP:tä määrittämällä varaston strategisen asemoinnin ja puskuritasot sen perusteella, mikä on varaston sijainti jakeluverkostossa.

Seuraavassa kuvassa on esimerkkinä yritys, jonka jakelukeskus on Seattlessa ja jolla on myymälöitä Bostonissa, Atlantassa ja Portlandissa.

![Sijaintiin perustuvat erotuspisteet vähittäismyyntimallissa](media/ddmrp-retail-decoupl-points-example.png "Sijaintiin perustuvat erotuspisteet vähittäismyyntimallissa")

Voidaan esimerkiksi päätellä, että peitteen kuljetusaika jakelukeskuksen ja myymälöiden välillä ei ole *asiakkaan toleranssiajan* mukainen, sillä asiakkaat odottavat peitteen olevan varastossa käyntihetkellä. Siinä tapauksessa peitteen erotuspiste määritetään jokaisessa kolmessa myymälässä. Kussakin myymälässä on erilaiset puskuritasot, jotka perustuvat esimerkiksi myymäläkohtaisiin läpimenoaikoihin ja kysyntämalleihin.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Varaston asemoinnin toteuttaminen Dynamics 365 Supply Chain Managementissa

Tässä osassa käsitellään varaston asemoinnin toteuttamista Microsoft Dynamics 365 Supply Chain Managementissa.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Erotuspisteitä luovien nimikkeen kattavuusryhmien määrittäminen

Nimikkeistä tulee erotuspisteitä, kun ne kuuluvat kattavuusryhmään, jonka määrityksissä **Kattavuuskoodi**-arvoksi on valittu *Erotuspiste*. Niinpä DDMRP-määritysprosessiin ensimmäinen vaihe on päättää, missä kattavuusryhmissä on toteutettava DDMRP-strategiaan, ja luoda ne sitten seuraavien ohjeiden mukaisesti.

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Kattavuusryhmät**.
1. Luo kattavuusryhmä valitsemalla toimintoruudussa **Uusi**.
1. Anna kattavuusryhmän määrittävät tiedot ja valitse sitten käytettävä kalenteri.
1. Valitse **Yleiset**-välilehden **Kattavuuskoodi**-kentässä *Erotuspiste*. Tämän asetuksen myötä kaikkia kyseiseen kattavuusryhmään kuuluvia nimikkeitä käsitellään DDMRP:n erotuspisteinä. Se on myös kaikki DDMRP-asetukset käyttöön tässä ryhmässä myöhemmin kuvattavalla tavalla.
1. Määritä **Muu**-välilehden **DDMRP-parametrit**-osassa seuraavat kentät:

    - **Läpimenoajan kerroin** – Määritä kerroin (desimaaliarvo 0–1), jolla hallitaan läpimenoajan vaikutusta laskettaessa tämän kattavuusryhmän nimikkeiden varaston vähimmäis- ja enimmäistasoa. Yleisesti ottaen mitä pidempi läpimenoaika nimikkeellä on, sitä alhaisempi läpimenoajan kertoimen on oltava. Alhainen läpimenoajan kerroin tuottaa alhaisemmat varaston vähimmäis- ja enimmäistasot, minkä vuoksi tilausten koko on pienempi ja tilauksia tehdään useammin. DDMRP-menetelmä suosittelee käytettäväksi arvoa 0,20–0,40, jos nimikkeellä on pitkä läpimenoaika, ja arvoa 0,41–0,60, jos nimikkeellä keskitason läpimenoaika. Arvoa 0,61–1,00 käytetään, jos nimikkeellä on lyhyt läpimenoaika. Lisätietoja on kohdassa [Puskuriprofiilit ja -tasot](ddmrp-buffer-profile-and-levels.md).
    - **Vaihtuvuuskerroin** – Määritä kerroin (desimaaliarvo 0–1), jolla hallitaan vaihtuvan kysynnän vaikutusta laskettaessa tämän kattavuusryhmän nimikkeiden varaston vähimmäistasoa. Yleisesti ottaen mitä enemmän nimikkeen kysyntä vaihtelee, sitä suurempi vaihtuvuuskertoimen on oltava. Suuren vaihtuvuuskertoimen tuloksena on varaston korkeampi vähimmäistaso. DDMRP-menetelmä suosittelee käytettäväksi arvoa 0,00–0,40, jos nimikkeellä on alhainen vaihtuvuus, ja arvoa 0,41–0,60, jos nimikkeellä keskitason vaihtuvuus. Arvoa 0,61–1,00 käytetään, jos nimikkeellä on suuri vaihtuvuus. Lisätietoja on kohdassa [Puskuriprofiilit ja -tasot](ddmrp-buffer-profile-and-levels.md).
    - **Vähimmäis-, enimmäis- ja uudelleentilauspistekausi** – määritä, kuinka usein puskuriarvot lasketaan (*Päivittäin* tai *Viikoittain*).

1. Määritä **Muu**-välilehden **Keskimääräinen päivittäinen käyttö**-osassa seuraavat kentät:

    - **Keskimääräinen päivittäinen käyttö, jonka perusteena on** – valitse ajanjaksot, joihin keskimääräisen päivittäisen käytön (ADU) laskenta perustuu. Valitse jokin seuraavista:

        - *Aiemmat* – Tarkastele vain aiempaa käyttöä **Aiempi kausi (päivinä)** -kentässä määritettyjen päivien ajalta. ADU lasketaan nimikkeen kokonaiskysyntänä laskentakauden aikana (varastoyksiköinä) jaettuna laskentakauden päivien määrällä.
        - *Tuleva* – Tarkastele ennustettua tulevaa käyttöä (mukaan lukien ennusteita) **Tuleva kausi (päivinä)** -kentässä määritettyjen päivien ajalta. ADU lasketaan nimikkeen kokonaiskysyntänä laskentakauden aikana (varastoyksiköinä) jaettuna laskentakauden päivien määrällä. 
        - *Sekoitettu* – Tarkastele sekä aiempaa että tulevaa käyttöä. **Aiempi kausi (päivinä)**- ja **Tuleva kausi (päivinä)** -kenttien asetuksia sekä sekoitusvaihtoehtoja käytetään. 

            *Sekoitettu ADU* = (\[*Aiempi painotus* × *Aiempi ADU*\] + \[*Tuleva painotus* × *Tuleva ADU*\]) ÷ (*Aiempi painotus* + *Tuleva painotus*)

    - **Aiempi kausi (päivinä)** – Anna niiden kuluneiden päivien (kuluva päivä mukaan lukien) määrä, joka järjestelmän on otettava huomioon tämän kattavuusryhmän nimikkeiden ADU:ta laskettaessa. Tätä asetusta käytetään vain, kun **Keskimääräinen päivittäinen käyttö, jonka perusteena on** -kentän asetuksena on *Aiempi* tai *Sekoitettu*.
    - **Tuleva kausi (päivinä)** – Anna niiden tulevien päivien (kuluvasta päivästä määritettyyn päivään asti) määrä, joka järjestelmän on otettava huomioon tämän kattavuusryhmän nimikkeiden ADU:ta laskettaessa. Tätä asetusta käytetään vain, kun **Keskimääräinen päivittäinen käyttö, jonka perusteena on** -kentän asetuksena on *Tuleva* tai *Sekoitettu*.
    - **Aiemman kauden suhteellinen painoarvo sekoitusperiaatteella lasketussa keskimääräisessä päivittäisessä käytössä** – Anna painotus (prosenttiosuutena), jota käytetään aiemmassa kaudessa sekoitettua ADU:ta laskettaessa. Tätä asetusta käytetään vain, kun **Keskimääräinen päivittäinen käyttö, jonka perusteena on** -kentän asetuksena on *Sekoitettu*.
    - **Tulevan kauden suhteellinen painoarvo sekoitusperiaatteella lasketussa keskimääräisessä päivittäisessä käytössä** – Anna painotus (prosenttiosuutena), jota käytetään tulevassa kaudessa sekoitettua ADU:ta laskettaessa. Tätä asetusta käytetään vain, kun **Keskimääräinen päivittäinen käyttö, jonka perusteena on** -kentän asetuksena on *Sekoitettu*.

1. Anna kaikissa muissa välilehdissä ja kentissä yksityiskohtaiset asetukset, joita käytetään tähän kattavuusryhmään linkitettyjen nimikkeiden tarpeiden laskennassa.

### <a name="set-an-item-as-a-decoupling-point"></a>Nimikkeen määrittäminen erotuspisteenä

Nimike määritetään erotuspisteeksi seuraavien ohjeiden mukaan.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi ja valitse vapautettu nimike, jossa halutaan tehdä DDMRP-määritykset.
1. Valitse toimintoruudun **Suunnitelma**-välilehdessä **Nimikekattavuus**.
1. **Nimikekattavuus**-sivulla voi olla luettelossa jo useita nimikekattavuustietueita, joista kukin koskee tiettyä varasto- ja tuotedimensioyhdistelmää. Voit valita aiemmin luodun sellaisia dimensioita koskevan nimikekattavuustietueen, johon haluat luoda erotuspisteen. Vaihtoehtoisesti voit luoda uuden nimikekattavuustietueen valitsemalla toimintoruudusta **Uusi**.
1. Määritä nimikekattavuustietue normaaliin tapaan. Määritä ainakin toimipaikka ja varasto, jossa erotuspistettä käytetään.
1. Valitse **Yleiset**-välilehti, kun kyseinen tietue on edelleen valittuna.
1. Valitse **Käytä erityisasetuksia** -valintaruutu.
1. Määritä **Kattavuusryhmä**-kenttä sille kattavuusryhmälle, joka määritetään luomaan erotuspisteet (edellisessä osassa kuvatulla tavalla).
1. Nimike on nyt määritetty erotuspisteeksi. DDMRP:tä käytettäessä tässä määritetään yleensä myös ne asetukset, jotka vaikuttavat puskurin kokoihin ja uudelleentilauksen määrään. Nämä määritykset voidaan kuitenkin tehdä myöhemmin. Lisätietoja asetuksista on kohdassa [Erotuspistenimikkeen puskurien määrittäminen](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Nimikkeitä, jotka eivät ole erotuspisteitä, voidaan suunnitella samalla tavoin kuin käytettäessä tavanomaista tarvelaskentaa (MRP).
