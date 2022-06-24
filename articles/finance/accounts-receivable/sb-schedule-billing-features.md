---
title: Laskutusaikataulujen ominaisuudet
description: Tässä artikkelissa on tietoja laskutusaikataulujen ominaisuuksista, kuten hinnoittelumenetelmistä, eskalaatioista ja alennuksista, kohdistuspäivämääristä, suhteellisesta jaosta, laskutuksen peruutuksesta ja jaetuista nimikeryhmistä.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853580"
---
# <a name="billing-schedule-features"></a>Laskutusaikataulujen ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja laskutusaikataulujen ja laskutusaikataulurivien ominaisuuksista. Siinä kuvataan hinnoitteluun käytettävät menetelmät, eskalointien ja alennusten käyttö sekä laskutuskauden palautustavat. Mukana on myös esimerkkejä suhteellisen jaon laskelmista ja jaetuista nimikeryhmistä.

## <a name="pricing-methods"></a>Hinnoittelumenetelmät

Voit laskea nimikkeen yksikköhinnan jollakin seuraavista hinnoittelumenetelmistä:

* Tasoita
* Vakio
* Taso
* Kiinteä taso

### <a name="flat-pricing"></a>Kiinteä hinnoittelu

Kun kiinteä hinnoittelumenetelmä on käytössä, **Kaikki laskutusaikataulut** -sivun laskutusaikataulun rivinimikkeen yksikköhintaa voidaan muokata haluamaani arvoon. **Yksikkökustannus**-arvo on aina **1**. Siksi **Yksikköhinta**- ja **nettosumma**-arvot ovat samat.

### <a name="standard-pricing-without-a-trade-agreement"></a>Vakiohinta (ilman kauppasopimusta)

Kun vakiohinnoittelumenetelmää käytetään ilman kauppasopimusta, määritä laskutusaikataulun rivinimikkeen yksikköhinta valitsemalla **Tuotetietojen hallinta** **Julkaistun tuotteen tiedot** -sivulla. Yksikköhinta näkyy **Perusmyyntihinta**-osassa. Se lasketaan *Hinta* &divide; *Hinnan määrä*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Vakiohinta (kauppasopimuksen kanssa)

Seuraavissa esimerkeissä näytetään vakiohinnoittelulaskelmat, kun kauppasopimus on olemassa. Voit luoda kauppasopimuksia **Vapauta tuotetiedot** -sivulla.

Molemmissa esimerkeissä käytetään nimikettä, jolla on seuraavat hintasulkeet.

| Määrästä | Määrälle | U/M | Hinta | Hintayksikkö |
|---|---|---|---|---|
| 0 | 100 | Kukin | 1.50 | 1 |
| 100 | 200 | Kukin | 1.25 | 1 |
| 200 | 999999 | Kukin | 1.00 | 1 |

**Esimerkki 1**

Laskun määrä on 250 ja käytetään vakiohinnoittelumenetelmää. Koska määrä on hinta-alueella 200 – 999 999, yksikköhinta on 1,00. 

Nettosummat lasketaan seuraavasti:

*Nettosumma* = (*Määrä* &times; *Hinta*) &divide; *Hintayksikkö* = (250 &times; 1,00) &divide; 1 = 250

**Esimerkki 2**

Laskun määrä on 100 ja käytetään vakiohinnoittelumenetelmää. Koska laskutusmäärä on hinta-alueella 0 – 100, yksikköhinta on 1,50.

> [!NOTE]
> Laskun määrä on 0 –100-arvovälillä eikä 100–200-alueella, koska määrän vakiovastaavuuden osalta määrä vastaa sitä, onko määrä *suurempi tai yhtä suuri kuin* "Alkaen" ja *pienempi kuin* "määrään".

Nettosummat lasketaan seuraavasti:

*Nettosumma* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Tier-hinnoittelu

Seuraavassa esimerkissä nimikkeellä on seuraavat hintasulkeet.

| Määrästä | Määrälle | U/M | Hinta | Hintayksikkö |
|---|---|---|---|---|
| 0 | 100 | Kukin | 1.50 | 10 |
| 100 | 200 | Kukin | 1.25 | 10 |
| 200 | 999999 | Kukin | 1.00 | 10 |

Jos laskun määrä on 250 ja käytetään hinnoittelumenetelmää, nimikkeiden hinnat lasketaan seuraavasti hinnoittelun hakasulkeiden perusteella:

- **Ensimmäiset 100 nimikettä:** 100 &times; 1,50 = 150,00
- **Toiset 100 nimikettä:** 100 &times; 1,25 = 125,00
- **Jäljellä olevat nimikkeet:** 50 &times; 1,00 = 50,00

Nettosummat lasketaan seuraavasti:

*Nettosumma* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Kun nettosumma on laskettu, yksikköhinta lasketaan jakamalla nettosumma määrällä:

*Yksikköhinta* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Kiinteän tason hinnoittelu

Seuraavassa esimerkissä nimikkeellä on seuraavat hintasulkeet.

| Määrästä | Määrälle | U/M | Kiinteän tason summa | Hintayksikkö |
|---|---|---|---|---|
| 0 | 50 | Kukin | 100.00 | 50 |
| 50 | 200 | Kukin | 150.00 | 200 |

Seuraavassa taulukossa näkyvät ostettujen määrien laskut ja yksikköhinnat. Nettosumma lasketaan ensin, ja sitten yksikköhinta.

| Lasku | Ostettu määrä | Yksikköhinta | Nettosumma |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskaloinnit ja alennukset

*Eskalointi* on tulevan laskutuskauden hinnankorotus, jolle ei ole vielä luotu laskua. *Alennus* on tulevan laskutuskauden hinnanalennus, jolle ei ole vielä luotu laskua.

Ylläpitosopimuksen laskuttamisen eskalointeja ja alennuksia ei voi soveltaa takautuvasti laskutusaikatauluun. Et esimerkiksi voi ottaa eskalointia käyttöön laskutusaikataulussa kolme kuukautta aiemmin ja käsitellä sitä. Et siis voi ottaa käyttöön kolme kuukautta sitten tapahtunutta hinnankorotusta.

Eskaloinnin tai alennuksen voi ottaa käyttöön laskutusaikataulussa tai laskutusaikataulun rivillä seuraavissa tapauksissa:

- **Kaikki/aktiiviset laskutusaikataulut** -luettelosivu
- Tietty laskutusaikataulu
- Tietty laskutusaikataulurivi

### <a name="apply-an-escalation-or-discount"></a>Eskaloinnin tai alennuksen kohdistaminen

Eskaloinnin tai alennuksen voi ottaa käyttöön laskutusaikataulussa noudattamalla seuraavia ohjeita.

1. Valitse laskutusaikataulu tai laskutusaikataulun rivi.
2. Valitse **Eskalointi ja alennus** joko **Eskalointi ja alennus** välilehdessä tai laskutusaikataulun rivillä.
3. Jos eskaloinnin tai alennuksen laskemiseen käytetään kuluttajahintaindeksiä, valitse arvo **Kuluttajahintaindeksin laskenta** -kentästä.
4. Lisää eskalointi- tai alennusrivi valitsemalla **Uusi**.
5. Jos haluat käyttää alennusta, valitse **Alennus**-valintaruutu. Jos haluat eskaloinnin, jätä **Alennus**-valintaruutu tyhjäksi.
6. Määritä **Aloituspäivä**- ja **Taajuus**-kentät.
7. Jos käytetään jaksottamatonta tuottotoimintoa, määritä **päättymispäivä**-kenttä.
8. Määritä **Prosentti**-, **Summa**- tai **Kuluttajahintaindeksisuunnitelma**-kenttä.
9. Määritä **Päättymispäivämäärä**-kenttä.
10. Valitse **OK**.
11. Toista vaiheet 4-10 jokaiselle tarvitsemallesi eskalointi- tai alennuslisäriville.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Laskutusaikataulurivit-sivun kentät

**Laskutusaikataulurivit**-sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|---|---|
| Nimiketunnus | Laskutusaikataulurivin nimikenumero. Tämä kenttä on käytettävissä vain, kun sivu avataan laskutusaikataulun rivinimikkeestä. |
| Kuluttajahintaindeksin laskenta | <p>Valitse menetelmä, jota käytetään kulutushintaindeksin eskaloinnin laskemiseen:</p><ul><li>**Edellinen hintaindeksi** – Käytä eskalointilaskelmassa aiempaa kuluttajahintaindeksin arvoa.</li><li>**Peruskuluttajahintaindeksi** – Käytä eskalointilaskelmassa peruskuluttajahintaindeksin arvoa.</li></ul> |
| **Rivi**-ruudukko | |
| Alennus | <p>Valitse valintaruutu, kun haluat määrittää, onko summan muutos eskalointi vai alennus:</p><ul><li>**Valittu** – Muutos soveltaa alennusta laskutusaikatauluun tai laskutusaikataulun riviin.</li><li>**Tyhjä** – Muutos koskee laskutusaikataulun tai aikataulurivin eskalointia.</li></ul><p>Tämän valintaruudun asetusta ei voi muuttaa nimikkeille, jotka käyttävät laskuttamatonta tuotto-ominaisuutta. Lisäksi alennuksia ei voi käyttää nimikkeisiin, jotka käyttävät tuottojen jakoa.</p> |
| Aloituspäivämäärä | Valitse eskaloinnin tai alennuksen alkamispäivä. |
| Tiheys | Valitse eskaloinnin tai alennuksen taajuus: **Ei mitään**, **Kuukausittain**, **Neljännesvuosittain**, **Puolivuosittain** tai **Vuosittain**. |
| Prosentti | Määritä eskaloinnin tai alennuksen prosenttimäärä. |
| Määrä | Määritä eskaloinnin tai alennuksen määrä. |
| Kuluttajahintaindeksin aikataulu | Valitse laskelmissa käytettävä kuluttajahintaindeksin aikataulu. |
| Päättymispäivä | <p>Valitse eskaloinnin tai alennuksen päättymispäivä.</p><p>**Huomautus:** Tämä kenttä on pakollinen tuotteille, jotka käyttävät laskuttamattomien tuottojen ominaisuutta.</p> |
| Lykkäysaikataulun numero | <p>Lykkäysaikataulun numero.</p><p>Tämä kenttä on käytettävissä vain, kun sivu avataan laskutusaikataulun rivistä.</p> |
| Kirjauskansion eränumero | <p>Kirjauskansion eränumero.</p><p>Tämä kenttä on käytettävissä vain, kun sivu avataan laskutusaikataulun rivistä.</p> |
| Alennuksen kokonaissumma | <p>Ruudukon kaikkien rivien alennussummat yhteensä.</p><p>Tämä kenttä on käytettävissä vain, kun sivu avataan laskutusaikataulun rivistä.</p> |
| Nykyinen lyhytaikainen laskuttamaton tuoton summa | <p>Nykyinen lyhytaikainen laskuttamaton tuoton summa.</p><p>Tämä summa näkyy, kun **Toistuvan sopimuksen laskutusparametrit** -sivulla on valittu lyhytkestoinen lykkäysmenetelmä ja rivinimikkeen tilit määritetään **Laskuttamaton tuottomääritys** -sivulla.</p> |
| Nykyinen pitkäaikainen laskuttamaton tuoton summa | <p>Nykyinen pitkäaikainen laskuttamaton tuoton summa.</p><p>Tämä summa näkyy, kun **Toistuvan sopimuksen laskutusparametrit** -sivulla on valittu lyhytkestoinen lykkäysmenetelmä ja rivinimikkeen tilit määritetään **Laskuttamaton tuottomääritys** -sivulla.</p> |

## <a name="proration-examples"></a>Esimerkkejä suhteellisesta jaosta

Suhteellisen jaon laskennat voivat perustua päivien tai kuukausien lukumäärään. Suhteellisen jaon laskennassa käytettävä menetelmä määritetään **Toistuvat sopimuksen laskutusparametrit** -sivulla. Laskutusaikataulun suhteellisen jaon menetelmä vaikuttaa siihen, miten summat lasketaan seuraavissa tilanteissa:

- Ensimmäinen luonti
- Eskaloinnin tai alennuksen käyttö
- Irtisanominen
- Pitopaikan sijoittaminen tai poistaminen
- Tuen tai uudistuksen lisäys

Suhteellisen jaon menetelmä vaikuttaa myös kuukausittaisen toistuvan tuoton (MRR) raporttiin.

### <a name="example-1"></a>Esimerkki 1

Laskutusaikataulun vuosittainen summa $5 000. Alkamispäivämäärä on 12.8.2019 ja päättymispäivä on 22.12.2019. Laskutustaajuus on vuosittain. Laskettu summa lasketaan seuraavilla tavoilla sen mukaan, käytetäänkö päivittäistä vai kuukausittaista laskentatapaa:

- **Päivittäin**

    - *Päivien määrä* = *Päättymispäivämäärä* – *Aloituspäivämäärä* + 1 = 133 päivää
    - *Vuoden päivien määrä* = 11.8.2020 – 12.8.2019 + 1 = 366 päivää
    - *Suhteellisen jaon summa* = 5 000 &times; (133 &divide; 366) = 1 816,94

- **Kuukausittain**

    - *Aloituskuukauden osa* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Keskikuukausia* = 3
    - *Kuukauden loppuosa* = 22 &divide; 31
    - Suhteellisen jaon summa = 5 000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Esimerkki 2

Laskutusaikataulun vuosittainen summa $12 000. Alkamispäivämäärä on 1.8.2019 ja päättymispäivä on 31.12.2019. Laskutustaajuus on vuosittain. Laskettu summa lasketaan seuraavilla tavoilla laskentatavan mukaan:

- **Päivittäin**

    - *Päivien määrä* = *Päättymispäivämäärä* – *Aloituspäivämäärä* + 1 = 153 päivää
    - *Vuoden päivien määrä* = 31.7.2020 – 1.8.2019 + 1 = 366 päivää
    - *Suhteellisen jaon summa* = 12 000 &times; (153 &divide; 366) = 5 016,39

- **Kuukausittainen (Täysi kuukausi)**

    - *Kuukausien määrä* = 5
    - *Kuukaudet yhteensä* = 12
    - *Suhteellisen jaon summa* = (12 000 &times; 5) &divide; 12 = 5 000

## <a name="reversing-a-period-billing"></a>Kauden laskutuksen peruuttaminen

Tässä esimerkissä laskutusaikataulussa on vain yksi rivi:

- Laskutus tehdään kuukausittain 12 kuukauden ajan tammikuusta joulukuuhun.
- Kaikille kausille on luotu laskuja huhtikuuhun saakka.

Haluat peruuttaa huhtikuun laskutuskauden laskun.

Jos myyntilaskua ei ole vielä luotu huhtikuun laskutuskaudella, voit poistaa myyntitilauksen. Tällöin tiedon **laskutettu**-tila poistetaan. Koska laskutusjaksolle on luotu lasku, erittelyn **Laskutettu**-tilaa ei voi poistaa. Huhtikuun laskutuksen peruutusta varten riville on luotava vastakirjaus.

1. Luo aikataulurivi samalle nimikkeelle **Kaikki laskutusaikataulut** -sivulla.
2. Muuta nimikkeen **Määrä**-arvoksi alkuperäisen määrän negatiivinen arvo.
3. Määritä **Laskutusväli**-kentän arvoksi **Kerran**.
4. Päivitä alkamis- ja päättymispäivät niin, että ne ovat samat kuin laskutustietojen päivämäärät, jota varten haluat luoda hyvityslaskun. Tässä esimerkissä alkamispäivämääräksi määritetään 1.4.2019 ja päättymispäiväksi 30.4.2019.
5. Tallenna muutokset.
6. Avaa **Luo lasku** -sivu ja luo myyntitilaus, jossa on hyvityslasku määritettynä ajanjaksona.
7. Vaihtoehtoinen: Kirjaa lasku.

Kun tarkistat laskutusaikataulun rivit, huomaat, että uudella rivillä on linkki hyvityslaskuun. Alkuperäisellä rivillä on edelleen linkki alkuperäiseen huhtikuun laskuun.

## <a name="split-item-group-examples"></a>Jaetun nimikeryhmän esimerkkejä

Tässä esimerkissä on käytössä seuraavat määritykset:

- **Toistuvat sopimuksen laskutusparametrit** -sivulla valitaan **Jako nimikeryhmän mukaan** ja **Yksilöivä ajoitustyyppi** -kentän arvoksi määritetään **Asiakas**.
- On luotu kolme nimikeryhmää: **ETULIITE**, **DATAHUB** ja **SPP**.
- Asiakkaalla US-001 on useita laskutusaikatauluja, joissa nimikeryhmä on ETULIITE tai DATAHUB.
- Asiakkaalla US-002 on useita laskutusaikatauluja, joissa nimikeryhmä on ETULIITE tai SPP.

| Laskutusaikataulun numero | Asiakas | Nimikeryhmä |
|---|---|---|
| SCH001 | US-001 | ETULIITE |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | ETULIITE |
| SCH004 | US-002 | SPP |

Asiakas US-001 ostaa uusittavan nimikkeen, joka kuuluu PREFIX-tuoteryhmään. Tämä tapahtuma on uusi myyntitilaus.

| Myyntitilaus # | Asiakas | Päänimike | Uusittu nimike | Uusittu nimikeryhmä | Laskutusaikataulun numero |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | ETULIITE | SCH001 |

Kun myyntitilauksen lasku kirjataan, lisätty lisänimike lisätään asiakkaan aiemmin luotuun laskutusaikatauluun (SCH001) asiakkaalle. Tässä laskutusaikataulussa käytetään ETULIITE-nimikeryhmää. Kaikki samaan tuoteryhmään kuuluvat uusittavat tuotteet sisällytetään samaan laskutusaikatauluun.

**Otsikko**
 
| Laskutusaikataulun numero | Asiakas | Nimikeryhmä |
|---|---|---| 
| SCH001 | US-001 | ETULIITE |

**Rivi**

| Laskutusaikataulun numero | Asiakas | Nimikeryhmä |
|---|---|---|
| SCH001 | US-001 | D0002 |

Asiakas US-001 ostaa nyt uusittavan nimikkeen, joka kuuluu SPP-tuoteryhmään. Tämä tapahtuma on uusi myyntitilaus.

| Myyntitilaus # | Asiakas | Päänimike | Uusittu nimike | Uusittu nimikeryhmä | Laskutusaikataulun numero |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Tällä hetkellä asiakkaalla US-001 ole laskutusaikataulua, joka käyttää SPP-nimikeryhmää. Siksi luodaan uusi laskutusaikataulu.

**Otsikko**

| Laskutusaikataulun numero| Asiakas | Nimikeryhmä |
|---|---|---|
| SCH005 | US-001 | SPP |

**Rivi**

| Laskutusaikataulun numero | Asiakas | Nimikeryhmä |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Saman loppukäyttäjän ja asiakkaan useat laskutusaikataulut

Tässä esimerkissä on käytössä seuraavat määritykset:

- **Toistuvat sopimuksen laskutusparametrit** -sivulla valitaan **Jako nimikeryhmän mukaan** ja **Yksilöivä ajoitustyyppi** -kentän arvoksi määritetään **Loppukäyttäjä**.
- **Loppukäyttäjien** sivulla määritetään seuraavat asiakas- ja loppukäyttäjäsuhteet.

    | Asiakastili | Loppukäyttäjän tili |
    |---|---|
    | US-001 | US-221 |

Asiakkaan ja loppukäyttäjän yhdistelmälle luodaan useita laskutusaikatauluja. Koska **Jaa nimikeryhmän mukaan** -vaihtoehto on valittuna **Toistuvan sopimuksen laskutusparametrit** -sivulla, samalle asiakas- ja loppukäyttäjäsuhteelle voidaan luoda useita laskutusaikatauluja.

| Laskutusaikataulun numero | Asiakas | Loppukäyttäjän tili | Otsikkonimikeryhmä |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

**Nimikkeen asetukset** -sivulla voit luoda tuki- ja uudistusnimikesuhteita.

| Nimikekoodi | Nimikkeen suhde | Tukinimike | Uusittu nimike | Uusittu nimikeryhmä |
|---|---|---|---|---|
| Taulukko | D001 | ITEM27 | D007 | IG1 |
| Taulukko | D002 | ITEM28 | D005 | IG2 |
| Taulukko | D003 | ITEM29 | D006 | IG3 |

Asiakkaalle US-001 luodaan nyt myyntitilaus. Myyntitilauksella on nimikkeitä **Nimikkeen asetus** -sivulla. Kun luot myyntitilauksen, avaa **tuki- ja käyttöoikeusprosessi** -sivu ja määritä **loppukäyttäjätili**-kenttä sekä muut pakolliset tiedot uudistusnimikkeeseen.

Kun tapahtuman lasku luodaan ja kirjataan, luodaan eri laskutusaikataulut asiakkaan ja käyttäjän ja nimikeryhmän yhdistelmälle. Saman myyntitilauksen useita rivejä voi liittää samaan laskutusaikatauluun.

| Myyntitilaus # | Asiakas | Loppukäyttäjän tili | Päänimike | Tukinimike | Uusittu nimike | Laskutusaikataulun numero |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
