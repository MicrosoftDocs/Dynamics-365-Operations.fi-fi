---
title: Puskuriprofiili ja -tasot
description: Tässä artikkelissa on tietoja puskuriprofiileista ja -tasoista, joiden perusteella määritetään kussakin erotuspisteessä pidettävistä enimmäis- ja vähimmäistasoista.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd72332abefd31fd391ff66931a5abae0efb08de
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186662"
---
# <a name="buffer-profile-and-levels"></a>Puskuriprofiili ja -tasot

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Kun erotuspisteet (tärkeät nimikkeet, joiden pitämiselle varastossa on strategiset syyt) on määritetty, kullekin niistä on määritettävä varastossa pidettävä määrä (puskuri). Tämä tehtävä on toinen kysyntäperustaisen tarvelaskennan (DDMRP) vaihe.

## <a name="buffer-levels-and-zones"></a>Puskuritasot ja -vyöhykkeet

DDMRP:ssä kukin varastopuskueri määritetään kolmen arvon avulla: vähimmäismäärä, enimmäismäärä ja uudelleentilauspiste. Näiden arvojen avulla muodostuu kolme vyöhykettä, joilla on seuraavat värikoodit:

- **Punainen vyöhyke** – Vähimmäismäärän alittava alue. Vähimmäismäärään viitataan myös punaisen ylärajana, ja suunnittelustrategia pitäisi suunnitella varmistamaan, että varastotasot ovat aina tämän pisteen yläpuolella.
- **Keltainen vyöhyke** – Vähimmäismäärän ja uudelleentilauspisteen välinen alue. Uudelleentilauspistettä kutsutaan myös keltaisen ylärajaksi. Kun tämä piste saavutetaan, järjestelmän on tehtävä uudelleentilaus.
- **Vihreä vyöhyke** – Uudelleentilauspisteen ja enimmäismäärän välinen alue. Enimmäismäärään kutsutaan myös vihreän ylärajaksi. Tämä piste on enimmäistaso, johon varasto täydennetään.

Seuraavassa kuvassa ovat nämä kolme vyöhykettä sekä niiden suhde vähimmäismäärään, enimmäismäärään ja uudelleentilauspisteeseen.

![DDMRP:n puskuritasot ja -vyöhykkeet](media/ddmrp-buffer-levels.png "DDMRP:n puskuritasot ja -vyöhykkeet")

## <a name="calculating-the-buffer-zones"></a>Puskurivyöhykkeiden laskeminen

Tässä osassa käsitellään kunkin puskurivyöhykkeen korkeuden laskentaa.

Keltainen vyöhyke lasketaan yleensä ensimmäisenä. Tämä vyöhyke ilmaisee määrän, joka kulutetaan tilauksen tekemishetkestä tilauksen vastaanottamiseen. Se on siis toisin sanoen odotettu kulutus täydennyksen läpimenoajan aikana. Se lasketaan seuraavasti:

- **Keltainen vyöhyke** = *Keskimääräinen päivittäinen käyttö (ADU)* × *Erotettu läpimenoaika*

*Erotettu läpimenoaika* ilmaisee ajan, joka tarvitaan nimikkeen tuottamiseen tai vastaanottamiseen, jos erotuspisteet ovat aina varastossa. Se on yleensä lyhyempi kuin *kumulatiivinen läpimenoaika*, joten perinteisesti käytettiin pääsuunnittelussa. Oikeat puskuriasetukset ovat välttämättömiä, jotta voidaan varmistaa, että erotuspisteet ovat aina varastossa olevassa määrässä mutta ylivarastointia ei synny.

Punainen vyöhyke lasketaan seuraavien laskutoimitusten avulla:

- **Punainen perusarvo** = *ADU* × *Erotettu läpimenoaika* × *Läpimenoajan kerroin*
- **Turvallinen punainen** = *Punainen perusarvo* × *Vaihtuvuuskerroin*
- **Punainen vyöhyke** = *Punainen perusarvo* + *Turvallinen punainen*

Vihreä vyöhyke lasketaan seuraavan kolmen laskutoimituksen enimmäistuloksena:

- *Tilauksen vähimmäismäärä*
- *ADU* × *Tilaussykli*
- *ADU* × *Erotettu läpimenoaika* × *Läpimenoajan kerroin*

## <a name="calculating-average-daily-usage"></a>Keskimääräisen päivittäisen käytön laskeminen

Järjestelmällä on kolme tapaa, jolla se voi laskea päivässä kulutetun määrän:

- **Keskimääräinen päivittäinen käyttö (mennyt)** – tämä menetelmä perustuu toteutuneeseen aiempaan kulutukseen.
- **Keskimääräinen päivittäinen käyttö (tuleva)** – tämä menetelmä perustuu ennustettuun tulevaan kulutukseen.
- **Keskimääräinen päivittäinen käyttö (sekoitettu)** – tämä menetelmä perustuu painotettuun mennen ja tulevan kulutuksen sekoitukseen.

### <a name="average-daily-usage-past"></a>Keskimääräinen päivittäinen käyttö (mennyt)

Mennyt ADU lasketaan keskiarvona lisäämällä määrät, jotka on kulutettu kunakin päivänä (määritetty määrä päiviä menneisyydessä), ja jakamalla summa päivien määrällä. Seuraava kuva näyttää, miten tämä menetelmä toimii, kun laskelma kattaa kolme edellistä päivää.

![Keskimääräinen päivittäinen käyttö (mennyt) -kaavio](media/ddmrp-adu-past.png "Keskimääräinen päivittäinen käyttö (mennyt) -kaavio")

Jos edellisessä kuvassa kuluva päivä on aamu 11. kesäkuuta, edellisen kolmen päivän (8.–10. kesäkuuta) ADU on 21.

- **ADU (mennyt)** = (29 + 11 + 23) ÷ 3 = 21

### <a name="average-daily-usage-forward"></a>Keskimääräinen päivittäinen käyttö (tuleva)

Jos kyse on uudesta tuotteesta, aiempia kulutustietoja ei ehkä ole. Niinpä käytössä onkin ehkä ennustettu ADU tulevaisuudessa (joka perustuu esimerkiksi ennustettuun kysyntään). Seuraava kuva näyttää, miten tämä menetelmä toimii, kun laskelma kattaa kolme tulevaa päivää (kuluva päivä mukaan lukien).

![Keskimääräinen päivittäinen käyttö (tuleva) -kaavio](media/ddmrp-adu-forward.png "Keskimääräinen päivittäinen käyttö (tuleva) -kaavio")

Jos edellisessä kuvassa kuluva päivä on aamu 11. kesäkuuta, seuraavan kolmen päivän (11.–13. kesäkuuta) ADU on 21,66.

- **ADU (tuleva)** = (18 + 18 + 29) ÷ 3 = 21,66

### <a name="average-daily-usage-blended"></a>Keskimääräinen päivittäinen käyttö (sekoitettu)

Sekoitettu ADU yhdistää keskimääräisen menneen ja tulevan kulutuksen, kuten seuraavassa kuvassa.

![Keskimääräinen päivittäinen käyttö (sekoitettu) -kaavio](media/ddmrp-adu-blended.png "Keskimääräinen päivittäinen käyttö (sekoitettu) -kaavio")

Jos edellisessä kuvassa kuluva päivä on aamu 11. kesäkuuta, edellisen ja seuraavan kolmen päivän (8.–13. kesäkuuta) sekoitettu ADU on 21,33.

- **Sekoitettu ADU** = (*Mennyt ADU* + *Tuleva ADU*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Puskurin laskennan kertoimet

Kullekin nimikkeelle voidaan määrittää kaksi kerrointa määrittämään punaisen ja vihreän vyöhykkeen koon. Tällä tavoin voidaan kompensoida odotetun läpimenoajan ja kysynnän vaihtuvuutta.

![Läpimenoaika- ja vaihtuvuuskertoimet](media/ddmrp-zone-factors.png "Läpimenoaika- ja vaihtuvuuskertoimet")

Ensimmäinen kerroin on *läpimenoaikakerroin*. Sen arvo desimaaliarvo 0–1. Mitä pidempi läpimenoaika on, sitä pienemmän arvon pitäisi olla. Demand Driven Institute suosittaa seuraavia arvoalueita:

- **Pitkä läpimenoaika:** 0,20–0,40
- **Keskitason läpimenoaika:** 0,41–0,60
- **Lyhyt läpimenoaika:** 0,61–1,00

Toinen kerroin on *vaihtuvuuskerroin*. Sen arvo desimaaliarvo 0–1. Mitä suurempi kysynnän vaihtuvuus on, sitä pienemmän arvon pitäisi olla. Demand Driven Institute suosittaa seuraavia arvoalueita:

- **Alhainen vaihtuvuus:** 0,20–0,40
- **Keskitason vaihtuvuus:** 0,41–0,60
- **Suuri vaihtuvuus:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Puskurin laskentaesimerkkejä

Tämä esimerkki jatkaa tyynyn tuotantoesimerkkiä, jota käytettiin kohdassa [Varaston asemointi](ddmrp-inventory-positioning.md). Kyseisessä esimerkissä valittiin erotuspisteet, jotka lyhensivät läpimenoajan 21 päivästä viiteen päivään, kuten seuraavassa kuvassa.

![Esimerkki erotetusta läpimenoajasta](media/ddmrp-bom-decoupled-lead-time-example.png "Esimerkki erotetusta läpimenoajasta")

Tässä esimerkissä oletetaan, että ADU on laskettu 23 kappaleeseen ja, kuten edellisessä kuvassa nähtiin, erotuksen erotettu läpimenoaika on viisi päivää. Näiden arvojen avulla voidaan laskea keltainen vyöhyke seuraavasti:

- **Keltainen vyöhyke** = *ADU* × *Erotettu läpimenoaika* = 115

![Esimerkki keltaisen vyöhykkeen laskelmasta](media/ddmrp-example-calc-yellow.png "Esimerkki keltaisen vyöhykkeen laskelmasta")

Punaisen vyöhykkeen laskema muistuttaa keltaisen vyöhykkeen laskelmaa, mutta sen vaihtuvuutta ja läpimenoaikaa täydennetään. Tässä esimerkissä oletetaan, että käytössä keskitason läpimenoaika (kerroin = 0,50) ja suuri kysynnän vaihtuvuus (kerroin = 0,8). Kun näitä arvoja käytetään yhdessä keltaisen vyöhykkeen laskelman osien kanssa, punainen vyöhyke voidaan laskea seuraavasti:

- **Punainen perusarvo** = *ADU* × *Erotettu läpimenoaika* × *Läpimenoajan kerroin* = 57,5
- **Turvallinen punainen** = *Punainen perusarvo* × *Vaihtuvuuskerroin* = 46
- **Punainen vyöhyke** = *Punainen perusarvo* + *Turvallinen punainen* = 103,5

Järjestelmä pyöristää punaiseen vyöhykkeen 104 kappaleeseen (kpl), koska kappaleet lasketaan kokonaislukuina.

![Esimerkki punaisen vyöhykkeen laskelmasta](media/ddmrp-example-calc-red.png "Esimerkki punaisen vyöhykkeen laskelmasta")

Myös vihreän vyöhykkeen laskelma sisältää keltaisen vyöhykkeen laskelman osia, mutta se sallii vähimmäistilauksen koon, tilausjakson ja läpimenoaikakertoimen käytön. Tässä esimerkissä oletetaan, että tilaussykliä ei (joten tilausvälejä koskevia aikarajoituksia ei tarvita) ja vähimmäismäärä on 10 kappaletta. Vihreä vyöhyke lasketaan sitten seuraavan kolmen laskutoimituksen enimmäistuloksena:

- *Tilauksen vähimmäismäärä* = 10
- *ADU* × *Tilaussykli* = 0
- *ADU* × *Erotettu läpimenoaika* × *Läpimenoajan kerroin* = 57,5

Järjestelmä pyöristää vihreän vyöhykkeen 58 kappaleeseen (kpl), koska kappaleet lasketaan kokonaislukuina.

![Esimerkki vihreän vyöhykkeen laskelmasta](media/ddmrp-example-calc-green.png "Esimerkki vihreän vyöhykkeen laskelmasta")

Seuraavassa kuvassa näiden vyöhykelaskelmien yhteenveto suppilokaaviona, jota käytetään usein DDMRP:ssä.

![Vyöhykelaskennan tulosten yhteenveto](media/ddmrp-example-calc-summary.png "Vyöhykelaskennan tulosten yhteenveto")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynaamiset oikaisut

Dynaamisten oikaisujen avulla voidaan käyttää *kysynnän oikaisukerrointa* suuren tai alhaisen kysynnän aikana. Tämä kerroin kertoo ADU:n kaikissa valitun kauden laskelmissa. Puskurivyöhykkeitä muokataan sitten vastaavasti. Tätä kerrointa käytetään yleensä sen jälkeen, kun ensimmäiset puskuriarvot on luotu, sillä tällä tavoin niitä voidaan tarkentaa ajan kuluessa ja muuttuvien tilanteiden vuoksi. Tämä tehtävä on DDMRP:n kolmas vaihe.

Tyynytuotteille saattaa olla esimerkiksi enemmän kysyntää kesällä, kun ihmiset lähtevät lomalle. Niinpä myynnin odotetaan olevan suurempi. Tässä tapauksessa tuotteen **Kysynnän oikaisukerroin** -arvoksi voidaan vaihtaa *1,5* kesäkuukausien ajaksi.

Tällä tavoin voidaan laskea puskuriarvoja ajan kuluessa ja oikaista niitä sitten järjestelmän ulkopuolisten lisätietojen perusteella. Täysimääräisessä DDMRP-toteutuksessa uudet puskuriarvot lasketaan päivittäin erätyönä, ja arvot hyväksytään automaattisesti. Suunnittelu suoritetaan sitten erätyönä ja suunnittelut tilaukset tarkistetaan päivittäin puskurien täydentämistä varten.

## <a name="implement-buffers-in-supply-chain-management"></a>Puskureiden toteuttaminen Supply Chain Managementissa

Tässä osassa käsitellään puskurivyöhykestrategian toteuttamista Microsoft Dynamics 365 Supply Chain Managementissa. Oletuksena on, että artikkelin alkupuolella käsitellyt analyysit ja laskelmat on jo tehty.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Erotuspistenimikkeen puskurien määrittäminen

Erotuspisteen puskuriarvot määritetään seuraavien ohjeiden mukaisesti.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse erotuspisteeksi määritetty vapautettu nimike. (Lisätietoja on kohdassa [Varaston asemointi](ddmrp-inventory-positioning.md).)
1. Valitse toimintoruudun **Suunnitelma**-välilehdessä **Nimikekattavuus**.
1. Valitse **Nimikkeen kattavuus** -sivulla erotuspisteen luova nimikkeen kattavuustietue. (Tämä tietue näyttää erotuspisteet luomaan määritetyn kattavuusryhmän nimen.)
1. Valitse **Yleinen**-välilehti.
1. Jos haluat järjestelmän laskevan puskuriarvot uudelleen päivittäin tai viikoittain myyntihistorian, ennusteiden tai kattavuusryhmän asetusten perusteella, toimi seuraavasti:

    1. Määritä **Puskuriarvot ajan kuluessa** -asetukseksi *Kyllä*.
    1. Sanomaruutu ilmoittaa, että manuaaliset puskuriasetukset (**Vähimmäisarvo**, **Uudelleentilauspiste** ja **Enimmäisarvo**), nollataan, jos jatkat. Säilytä uusi asetus valitsemalla **Kyllä**.

    Jos puolestaan haluat laskea tai antaa puskuriasetukset vain kerran, toimi seuraavasti:

    1. Määritä **Puskuriarvot ajan kuluessa** -asetukseksi *Ei*.
    1. Määritä **Vähimmäisarvo**-, **Uudelleentilauspiste**- ja **Enimmäisarvo**-kenttiin nimikkeelle aiemmin tässä artikkelissa kuvatulla tavalla lasketut puskuriarvot.

1. Viimeistele nimikkeen DDMRP-laskelmien määrittäminen määrittämällä seuraavat kentät:

    - **Tilaussykli** – Määritä, kuinka monta päivää on oltava nimikkeen ostotilausten välillä. Määritä arvoksi *0* (nolla), jos tilausrajoituksia ei ole. Tämä kenttä vaikuttaa enimmäismäärän puskuriin aiemmin tässä artikkelissa käsitellyllä tavalla.
    - **Keskimääräinen päivittäinen käyttö** – Nimikkeelle voidaan antaa arvioitu ADU (valinnainen). Tämä kenttä on tarkoitettu vain tiedoksi. Arvo lasketaan yleisesti automaattisesti puskurilaskelmien osana.
    - **Tilauspiikin raja-arvo** – Määritä nimikkeen päivittäisen myynnin vähimmäisarvo, joka ilmaisee myyntipiikin (epätavallisen suuren kysynnän). Järjestelmä nostaa suunniteltujen tilausten uudelleentilausmäärään tämän kentän perusteella suuren kysynnän aikana. Lisätietoja on kohdassa [Kysyntäperustainen suunnittelu](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Erotettujen läpimenoaikojen laskeminen tai syöttäminen

Erotuspistenimikkeen erotettu läpimenoaika lasketaan tai syötetään seuraavasti niille nimikkeille, joille järjestelmä saa [laskea puskurivyöhykkeet automaattisesti](#set-up-buffers).

1. Avaa erotuspistenimikkeen **Nimikkeen kattavuus** -sivu. (Lisätietoja on kohdassa [Erotuspistenimikkeen puskurien määrittäminen](#set-up-buffers).)
1. Valitse erotuspisteen luova nimikkeen kattavuustietue.
1. Valitse **Puskuriarvot**-välilehti.
1. Jos ruudukossa ei ole aikajaksoja, valitse toimintoruudun **Puskuriarvot**-välilehdessä **Lisää aikajaksot**. Järjestelmä täyttää ruudukkoon rivin kullekin päivittäiselle tai viikoittaiselle aikajaksolle sen mukaan, onko [kattavuusryhmän](ddmrp-inventory-positioning.md) **Vähimmäis-, enimmäis- ja uudelleentilauspistekausi** -kentän asetuksena *Päivittäin* vai *Viikoittain*. Järjestelmä lisää niin paljon rivejä, että nimikkeelle määritetyn kattavuusryhmän määritetty aikaraja saavutetaan.
1. Valitse aikajakso, jossa erotettu läpimenoaika halutaan laskea. (Yleensä tämä aikajakso on kuluvan päivän sisältävä jakso.)
1. Valitse toimintoruudun **Puskuriarvot**-välilehdessä **Laske erotettu läpimenoaika**.
1. Määritä **Laske erotettu läpimenoaika** -valintaikkunassa seuraavat kentät:

    - **Tuoterakenne** – valitse tuoterakenne, jossa laskelma halutaan suorittaa.
    - **Päivämäärä** – Valitse päivämäärä, jota suoritettava laskelma koskee. Käytettävissä olevat tuoterakenteet suodatetaan siten, että vain valittuna päivänä aktiiviset tuoterakenteet näytetään.
    - **Määrä** – Anna määrä, jota suoritettava laskelma koskee. Käytettävissä olevat tuoterakenteet suodatetaan siten, että vain määritettyä määrää koskevat tuoterakenteet näytetään.

1. Suorita laskelma valitsemalla **OK** ja sulje **Laske erotettu läpimenoaika** -valintaikkuna. Valitun ajanjakson **Erotettu läpimenoaika** -sarakkeessa näkyy nyt laskettu arvo.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Keskimääräisen päivittäisen käytön laskeminen tai syöttäminen

Erotuspistenimikkeen ADU lasketaan tai syötetään seuraavasti niille nimikkeille, joille järjestelmä saa [laskea puskurivyöhykkeet automaattisesti](#set-up-buffers).

1. Avaa erotuspistenimikkeen **Nimikkeen kattavuus** -sivu. (Lisätietoja on kohdassa [Erotuspistenimikkeen puskurien määrittäminen](#set-up-buffers).)
1. Valitse erotuspisteen luova nimikkeen kattavuustietue.
1. Valitse **Puskuriarvot**-välilehti.
1. Jos ruudukossa ei ole aikajaksoja, valitse toimintoruudun **Puskuriarvot**-välilehdessä **Lisää aikajaksot**. Järjestelmä täyttää ruudukkoon rivin kullekin päivittäiselle tai viikoittaiselle aikajaksolle sen mukaan, onko [kattavuusryhmän](ddmrp-inventory-positioning.md) **Vähimmäis-, enimmäis- ja uudelleentilauspistekausi** -kentän asetuksena *Päivittäin* vai *Viikoittain*. Myös **Läpimenoajan kerroin**- ja **Vaihtuvuuskerroin**-kenttien oletusarvot saadaan kattavuusryhmästä. Näitä arvoja muokata tarpeen mukaan kullakin rivillä.
1. Valitse ajanjakso, jossa ADU halutaan laskea.
1. Valitse toimintoruudun **Puskuriarvot**-välilehdessä **Laske keskimääräinen päivittäinen käyttö**. Järjestelmä yrittää kerätä ADU-laskelmaa varten tarvittavia tietoja [kattavuusryhmälle](ddmrp-inventory-positioning.md) tehtyjen määritysten mukaan.
1. Noudata seuraavia ohjeita:

    - Jos tarvittavat tiedot ovat saatavana, laskelman tulokset lisätään **Keskimääräinen päivittäinen käyttö** -sarakkeeseen. Tässä tapauksessa lisätoimia ei tarvita.
    - Jos tarvittavat tiedot eivät ole saatavana, mitään arvoja ei lisätä automaattisesti. Siinä tapauksessa arvioidut arvot on annettava manuaalisesti kullekin riville, jossa on tarkoitus laskea puskuriarvot.

### <a name="calculate-and-apply-buffer-values"></a>Puskuriarvojen laskeminen ja käyttäminen

Puskuriarvojen laskenta voidaan käynnistää seuraavien ohjeiden mukaan manuaalisesti niille nimikkeille, joille järjestelmä saa [laskea puskurivyöhykkeet automaattisesti](#set-up-buffers).

1. Aiemmin tässä artikkelissa on käsitelty, miten erotuspistenimikkeelle voidaan [määrittää puskurilaskelma](#set-up-buffers), [laskea tai syöttää erotetut läpimenoajat](#calc-lead-time) ja [laskea tai syöttää keskimääräinen päivittäinen käyttö](#calc-adu) kunkin aikajakson osalta.
1. Avaa erotuspistenimikkeen **Nimikkeen kattavuus** -sivu.
1. Valitse **Puskuriarvot**-välilehti, jossa pitäisi näkyä aikajaksoluettelo.
1. Valitse aikajakso, jota koskevat puskuriarvot halutaan laskea. (Yleensä tämä aikajakso on kuluvan päivän sisältävä jakso.) Valittavalla rivillä on oltava muita kuin nolla-arvoja **Keskimääräinen päivittäinen käyttö**- ja **Erotettu läpimenoaika** -sarakkeissa.
1. Muokkaa rivin **Kysynnän oikaisukerroin** -kenttä tarvittaessa. Järjestelmä käyttää tätä kerrointa kaikkien niiden puskurilaskelmien **Keskimääräinen päivittäinen käyttö** -arvoon, joissa kyseistä arvoa käytettiin. Tämän kertoimen avulla kysynnän vaihtelua voidaan oikaista päivämäärän mukaan (esimerkiksi loma- tai kausinimikkeiden osalta).
1. Valitse toimintoruudun **Puskuriarvot**-välilehdessä **Laske vähimmäis-, enimmäis- ja uudelleentilausmäärät**. Järjestelmä laskee ja täyttää **Nimikkeen kattavuus** -sivulla olevan ruudukon **Laskettu vähimmäismäärä**-, **Laskettu uudelleentilauspiste**- ja **Laskettu enimmäismäärä** -sarakkeet.
1. Kun lasketut arvot on tarkastettu, ne on otettava käyttöön. Muutoin niillä ei ole mitään vaikutusta. Kun laskelmaa käytetään riveillä, **Laskettu vähimmäismäärä**-, **Laskettu uudelleentilaus**- ja **Laskettu enimmäismäärä** -kenttien arvot kopioidaan vastaaviin **Vähimmäisarvo**-, **Uudelleentilauspiste**- ja **Enimmäisarvo**-sarakkeisiin. Valitse toimintoruudun **Puskuriarvot**-välilehden **Tee toiminto** -ryhmässä jokin seuraavista painikkeista:

    - **Hyväksy kaikki laskelmat** – käytä kaikkia laskettuja arvoja ruudukossa.
    - **Hyväksy valittujen rivien laskelmat** –käytä laskettuja arvoja vain valituilla riveillä.
    - **Hylkää kaikki laskelmat** – hylkää kaikki ruudukon vähimmäismääriä, enimmäismääriä ja uudelleentilauspisteitä koskevat lasketut arvot.
    - **Hylkää valittujen rivien laskelmat** – hylkää valittujen rivien vähimmäismääriä, enimmäismääriä ja uudelleentilauspisteitä koskevat lasketut arvot.

### <a name="schedule-automatic-buffer-value-calculations"></a>Puskuriarvolaskelmien automaattinen aikatauluttaminen

Kun DDMRP-asetukset on määritetty ja niiden on varmistettu toimivan odotetusti, haluat varmaankin määrittää erätyön laskemaan ADU:n ja liittyvät puskuriarvot tarvittaessa säännöllisesti uudelleen toteutuneiden kulutustietojen ja/tai päivitettyjen ennusteiden perusteella. Tämä menetelmä koskee vain nimikkeitä, joissa järjestelmä saa [laskea puskurivyöhykkeet automaattisesti](#set-up-buffers).

Puskuriarvolaskelmat aikataulutetaan automaattisesti seuraavasti.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Laske puskuriarvot**.
1. Määritä **Laske puskuriarvot** -valintaikkunassa seuraavat kentät:

    - **Laske keskimääräinen päivittäinen käyttö** – Kun asetuksena on *Kyllä*, erotuspistenimikkeiden ADU lasketaan uudelleen aina, kun kyseinen työ suoritetaan. Tämä laskelma ohitetaan valitsemalla *Ei*. Yleensä asetukseksi kannattaa valitse *Kyllä*.
    - **Laske erotettu läpimenoaika** – Kun asetuksena on *Kyllä*, erotetut läpimenoajat lasketaan uudelleen aina, kun kyseinen työ suoritetaan. Tämä laskelma ohitetaan valitsemalla *Ei*. Yleensä asetukseksi kannattaa valitse *Kyllä*.
    - **Laske puskuriarvot** – Kun asetuksena on *Kyllä*, puskuriarvot lasketaan uudelleen aina, kun kyseinen työ suoritetaan. Tämä laskelma ohitetaan valitsemalla *Ei*. Yleensä asetukseksi kannattaa valitse *Kyllä*.
    - **Hyväksy vähimmäis-, enimmäis- ja uudelleentilausmäärän laskelmat** – Kun asetuksena on *Kyllä*, uudelleenlasketut puskuriarvot hyväksytään ja niitä käytetään automaattisesti aina, kun kyseinen työ suoritetaan. Kun asetuksena on *Ei*, uudelleenlaskettuja arvoja ei käytetä. Siinä tapauksessa uudelleenlaskettuja arvoja ei käytetä, ellei joku ota niitä käyttöön myöhemmin manuaalisesti kunkin tuotteen **Nimikkeen kattavuus** -sivulla. Yleensä asetukseksi kannattaa valitse *Kyllä*.
    - **Pääsuunnitelma** – Valitse pääsuunnitelma, joka sisältämiin nimikkeisiin laskelmalla on vaikutusta. Laskelmaa käytetään kaikki suunnitelman suodattimessa oleviin nimikkeisiin. Tätä rajoitetaan lisää tämän valintaikkunan **Suodatus**-asetuksilla.

1. Kyseiseen suoritettavaan erätyöhön sisältyviä tietueita voi rajoittaa avaamalla **Kysely**-valintaikkunan valitsemalla **Suodatus** **Sisällytettävät tietueet** -pikavälilehdessä. Valintaikkuna toimii samalla tavalla kuin muissakin Supply Chain Managementin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).
1. Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein valittujen nimikkeiden valitut laskelmat suoritetaan. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Lisää uusi työ eräjonoon suoritettavaksi valitsemalla **OK**.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Kaikkien nimikkeiden erotettujen läpimenoaikojen tarkastaminen ja uudelleenlaskeminen

Kaikki yrityksessä saatavana olevat erotetut läpimenoajat tarkastetaan ja lasketaan seuraavasti.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> DDMRP \> Erotettu läpimenoaika**.
1. Etsi tarvittavat tiedot selaamalla ja suodattamalla luetteloa **Erotettu läpimenoaika** -sivulla. Nimikkeestä saa tätäkin enemmän tietoja valitsemalla sen linkin **Nimiketunnus**-sarakkeessa.
1. Minkä tahansa nimikkeen erotetut läpimenoajan voi laskea uudelleen valitsemalla nimikkeen ja valitsemalla sitten toimintoruudussa **Laske erotettu läpimenoaika**. **Laske erotettu läpimenoaika** -valintaikkuna avautuu. Tämä valintaikkuna toimii samoin kuin [laskettaessa erotettuja läpimenoaikoja](#calc-lead-time) samalle nimikkeelle **Kattavuusryhmä**-sivulla.
