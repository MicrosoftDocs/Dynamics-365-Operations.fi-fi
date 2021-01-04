---
title: Luo raportit
description: Tässä aiheessa on tietoja talousraporttien luonnista.
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e8b688cb1e4589eb076015d01dc4f0f0db14787e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688314"
---
# <a name="generate-financial-reports"></a>Luo raportit

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja talousraporttien luonnista.

Luo raportti avaamalla raportin määritys ja valitsemalla sitten Luo-painike työkalurivillä. Näytölle avautuu Raporttijonon tila -ikkuna, joka näyttää raporttisi paikan jonossa. Luotu raportti avautuu oletuksena Web Viewerissä.

Seuraavat raporttien luontivaihtoehdot ovat saatavilla:

- Määritä aikataulu raportin tai raporttiryhmän automaattista luontia varten
- Tarkista, ettei raportista puutu tilejä tai tietoja ja vahvista raportin virheettömyys

Raportteja luotaessa käytetään Raportin määritys -välilehdissä määritettyjä asetuksia.

## <a name="generate-a-financial-report"></a>Luo raportti

Voit luoda talousraportin valitsemalla **Kirjanpito** \> **Kyselyt ja raportit** \> **Talousraportit**.

- Valitse luotava raportti ja valitse sitten **Luo**.
- Täytä **Raportin päivämäärä** -kenttä ja valitse **OK**.

Kun raportti on luotu, sitä voi tarkastella **Raportit**-osassa.

Voit **tarkastella** raporttia tai **poistaa** sen.

Voit luoda raportti **raporttien suunnitteluohjelman** avulla avaamalla raporttimäärityksen ja valitsemalla sitten työkalupalkin Luo-painikkeen. Näytölle avautuu Raporttijonon tila -ikkuna, joka näyttää raporttisi paikan jonossa. Luotu raportti avautuu oletuksena Web Viewerissä.

## <a name="schedule-report-generation"></a>Raporttien luonnin ajoittaminen
Useissa yrityksissä on tietty raporttijoukko, joka suoritetaan tietyin aikavälein liiketoimintaprosessien tarpeiden mukaan. Voit ajoittaa raportin muodostumaan säännöllisesti, esim. päivittäin, viikoittain, kuukausittain tai vuosittain. Voit ajoittaa yksittäisiä raportteja tai raporttiryhmiä, jotka sisältävät useita yrityksiä. Jokaiselle sisällytettävälle yritykselle on määritettävä tunnistetiedot, jotka voivat olla esimerkiksi samat kuin raporttipuumäärityksessä. Jos tunnistetietosi eivät ole voimassa, raportti näyttää sinulle vain ne tiedot, joihin sinulla on käyttöoikeus, kuten yritys, johon olet kirjautunut kyseisellä hetkellä. Tuotostiedot luetaan ensin raporttiryhmästä ja sen jälkeen yksittäisistä raporteista.

Kun raporttien aikatauluja luodaan ja tallennetaan, ne näytetään siirtymisruudun kohdassa Raporttien aikataulut. Voit luoda kansioita raporttien järjestämistä varten. Jos aikataulun yksittäistä raporttia ei voida suorittaa, muut raportit silti suoritetaan.

> [!IMPORTANT]
> Voit luoda, muokata ja poistaa raporttien ajoituksia, jos sinulla on suunnittelijan tai järjestelmänvalvojan rooli. Kun raportti on ajettu, sen luomiseen käytetään sen käyttäjän tunnistetietoja, joka on luonut raportin.

### <a name="create-a-report-schedule"></a>Raporttiaikataulun luominen

1. Napsauta raportin suunnitteluohjelman Tiedosto-valikossa Uusi ja valitse sitten Raporttiaikataulu. Näyttöön avautuu valintaikkuna Uusi raporttiaikataulu.
2. Valitse kohdassa Asetukset yksittäinen ajastettava raportti tai raporttiryhmä. Käytettävissä ovat vain sellaisen yrityksen tai rakenneosavalikoiman raportit tai raporttiryhmät, johon olet kirjautuneena.
3. Ota raporttiaikataulu käyttöön valitsemalla Aktiivinen-valintaruutu. Vain raportin luonut käyttäjä tai järjestelmänvalvoja voi ottaa raporttiaikataulun käyttöön tai poistaa sen käytöstä.
4. Määritä yrityksen tunnistetiedot valitsemalla Käyttöoikeudet-painike. Oletusarvon mukaan sinun kirjautumistietojasi käytetään yritykselle, johon olet kirjautuneena. Jos muita yrityksiä on sisällytetty (esimerkiksi raporttipuumäärityksissä), valitse Käytä erillisiä tunnistetietoja ja anna sitten raporttiaikatauluun sisällytettyjen muiden yritysten tunnistetiedot. Voit valita Windows-todennus tai kirjoittaa kunkin yrityksen käyttäjänimen ja salasanan. Tallenna näiden yhtiöiden tunnistetiedot valitsemalla Tallenna tunnistetiedot -valintaruutu ja napsauta sitten OK sulkeaksesi valintaikkunan.
5. Valitse päivä, jolloin aikataulun tulee alkaa, kohdassa Tiheys kentässä Aloita toisto. Oletusarvon mukaan valitaan asiakastietokoneen järjestelmäpäivämäärä.
6. Valitse Suorita raportti -kentästä aika, jolloin raportti suoritetaan. Jos määrität ajan, joka on ennen kuluvaa järjestelmän aikaa, raportti suoritetaan seuraavana ajoitettuna päivänä.
7. Määritä Toistumisen kuvio -alueeseen, miten usein raportti suoritetaan. Oletuksena valitaan Päivittäin ja Aikaväli (päivinä) -arvoksi 1. Muut vaihtoehdot ovat Viikoittain, Kuukausittain ja Vuosittain.
8. Valitse Toistojen alue -alueesta, milloin raporttia ei enää luoda.

    - Päättymispäivä puuttuu – Raporttiaikataulua toistetaan jatkuvasti.
    - Määritä toistojen määrä – Raporttiaikataulua suoritetaan määritetty määrä kertoja, minkä jälkeen se poistetaan käytöstä.
    - Päättyy mennessä – Raporttiaikataulu päättyy määritettynä päivämääränä.

9. Napsauta työkalurivin Tallenna-painiketta. Syötä Tallenna nimellä -valintaikkunaan yksilöivä nimi ja raporttiaikataulun kuvaus.

Voidaksesi kopioida raporttiaikataulun, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli. Vaikka järjestelmänvalvoja muokkaisi raporttiaikataulua, raportilla säilyy raportin luojan tunnistetiedot.

### <a name="copy-a-report-schedule"></a>Kopioi raporttiaikataulu

1. Valitse raportin suunnitteluohjelman siirtymisruudussa Raporttiaikataulut ja avaa kopioitavat raporttiaikataulut.
2. ValitseTiedosto-valikosta Tallenna nimellä ja kirjoita aikataulun uusi nimi ja kuvaus Tallenna nimellä -valintaikkunaan. Kun valitset OK, uusi raporttiaikataulu tulee näkyviin siirtymisruutuun.
3. Muokkaa uuden aikataulun kenttiä ja tietoja tarpeen mukaan ja valitse sitten työkalurivissä Tallenna, tai valitse Tallenna Tiedosto-valikossa.

Sinun on oltava raporttiaikataulun omistaja tai sinulla on oltava järjestelmänvalvojan rooli poistaaksesi raporttiaikataulun.

### <a name="delete-a-report-schedule"></a>Raporttiaikataulun poistaminen

1. Valitse raportin suunnitteluohjelman siirtymisruudussa Raporttiaikataulu.
2. Valitse poistettava raporttiaikataulu ja valitse sitten Poista tai paina Delete-näppäintä.
3. Vahvista raporttiaikataulun poistaminen pysyvästi valitsemalla poistamisen vahvistusvalintaikkunassa Kyllä. Jos sinulla ei ole oikeuksia poistaa aikataulua, näyttöön tulee sanoma eikä raporttia poisteta.

### <a name="credentials-and-report-schedules"></a>Tunnistetiedot ja raportin aikataulut

Jos et syötä tarvittavia tunnistetietoja kaikille raportteihin sisältyville yhtiöille, saat seuraavan sanoman tallentaessasi raporttiaikataulun: Sinun on syötettävä tunnistetietosi raporttiaikatauluun sisältyville yhtiöille. Määritä tunnistetiedot valitsemalla Käyttöoikeudet-painike.

Esimerkissä käyttäjä kirjautuu yritykseen A käyttämällä käyttäjänimeä ja salasanaa. Käyttäjä luo aikataulun raportille, joka käyttää raportointipuun määrityksiä tietojen keräämiseen useista yrityksistä. Kun raporttiaikataulu tallennetaan, näyttöön tulee kehote, jossa käyttäjää pyydetään antamaan raporttipuumäärityksessä määritettyjen yritysten tunnistetiedot. Kun tunnistetietojesi voimassaolo päättyy, raporttiaikataulun raportteja ei luoda, kunnes tunnistetiedot on päivitetty. Raporttijonoon tulee sanoma ilmaisemaan, että käyttöoikeudet on päivitettävä. Raporttiaikataulu epäonnistuu, jos mikään seuraavista skenaarioista tapahtuu (koska ne vaativat tunnistetietoja):

- Uusi yritys on lisätty raportointipuun yksittäiseen raporttiin.
- Raporttiryhmän raporttia on muokattu.
- Raporttiryhmään on lisätty eri yritystä koskeva uusi raportti.

Jatka valitsemalla Käyttöoikeudet-painike Raportin ajoitus -valintaikkunassa ja syötä sitten asianmukaiset tunnistetiedot.

## <a name="missing-account-analysis-feature"></a>Puuttuvien tilien analysointitoiminto
Voit etsiä mahdollisesti puuttuvia kirjanpitotilejä ja dimensioita kaikista rivimäärityksistä, raportointipuumäärityksistä ja raporttimäärityksistä rakenneosaryhmässä. Tästä on hyötyä, kun luot tai päivität useita tilejä tai rakenneosia lyhyen ajanjakson aikana ja haluat varmistaa, että kaikki uusi tieto on sisällytetty raportteihisi.

Puuttuvat tilit määritetään käyttämällä rivin tai raportointipuun määrityksen alimpia ja korkeimpia arvoja. Sitten näkyviin tulee luettelo tileistä, joita ei ole rivin tai raportointipuun määrityksessä mutta jotka ovat taloushallinnon tiedoissa. Jos puuttuvan tilin arvo on suurempi tai pienempi kuin rivimäärityksen arvot, tiliä ei sisällytetä puuttuvien tilien luetteloon.

> [!TIP]
> Tämä menettely kannattaa tehdä tarkistusta varten ennen kuukausiraporttien luomista sekä luotaessa uusia rakenneosia.

On epätodennäköisempää, että arvovälejä sisältävissä raporteissa on puuttuvia tilejä. Käytä mahdollisuuksien mukaan rakenneosissa alueita, jotta voit sisällyttää uusia tilejä, kun niitä luodaan. Jos raporttimäärityksessä yritykseksi on määritetty @ANY, voit kirjautua sisään tiettyyn yritykseen ja suorittaa puuttuvien tilien analyysin kyseiselle yritykselle.

> [!NOTE]
> Jos uusi yritys on lisätty, sinun on lisättävä tämä uusi yritys kaikkien aiemmin luotujen raporttien raportointipuihin. Muuten yritystä ei sisällytetä puuttuvien tilien analyysiin.

### <a name="run-missing-account-analysis"></a>Puuttuvien tilien analyysin suorittaminen

1. Valitse raportin suunnitteluohjelmassa Työkalut ja napsauta sitten Puuttuvien tilien analyysi.
2. Valitse Yrityssuodatin-kentässä yritys, jonka perusteella tulokset suodatetaan, tai valitse Kaikki (ei suodatinta), jolloin näytetään tulokset kaikista käytettävissä olevista yrityksistä.
3. Valitse Dimensiosuodatin-kentässä dimensio, jonka perusteella tulokset suodatetaan, tai valitse Kaikki (ei suodatinta), jolloin näytetään kaikkien käytettävissä olevien dimensioiden dimensiotiedot.
4. Valitse Ryhmittely-kentässä vaihtoehto tulosten lajittelua varten. Voit lajitella tulokset vaikutuksenalaisen rakenneosan mukaan tai dimension ja arvojoukkojen mukaan.
5. Tarkista näytetyt tulokset. Kun valitset kohteen ylemmässä ruudussa, alemmassa ruudussa näkyy lisätietoja poikkeuksesta. Tietoihin lukeutuvat liittyvät dimensiot, arvot ja raportit.
6. Avaa kohta, johon tämä vaikuttaa, valitsemalla asianmukainen luetteloruudun kuvake tai napsauta kohtaa hiiren kakkospainikkeella ja valitse Avaa. Voit valita useita kohtia pitämällä Ctrl-näppäintä painettuna valitessasi kohdat alaruudussa.
7. Jos tulokseen sisältyy mitään sellaisia arvoja, rakenneosia tai raportteja, joiden ei pitäisi sisältyä analyysiin, napsauta kyseistä kohtaa hiiren kakkospainikkeella ja valitse Sulje pois, tai valitse Sulje pois -valintaruutu kyseisen kohdan vieressä poistaaksesi sen luettelosta. Poissuljettuja nimikkeitä ei sisällytetä, kun luettelo päivitetään. Voit valita useita kohteita pitämällä Ctrl-näppäintä alhaalla valitessasi kohteita alemmassa ruudussa. Saat näkyviin kaikki kohteet, mukaan lukien aiemmin analyysista pois jätettäväksi valitsemasi kohteet, valitsemalla Näytä pois jätetyt rakenneosat ja arvot -valintaruudun ja valitsemalla sitten Päivitä.
8. Valitsemalla Päivitä voit päivittää poikkeukset, jotka olet käsitellyt. Valitsemalla Kyllä voit suorittaa täyden kaikkien tulosten päivityksen ja valitsemalla Ei voit suorittaa osittaisen, käsiteltyjen kohteiden päivityksen.

    > [!NOTE]
    > Lomake päivitetään automaattisesti sen avautuessa, ellei sitä ole avattu viimeisen 15 minuutin aikana.

9. Kun ongelmat on ratkaistu, valitse OK sulkeaksesi valintaruudun.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Puuttuvien tilien analyysin pikanäppäimet
Kun suoritat puuttuvien tilien analyysin, käytettävissä on seuraavat pikanäppäimet.

| Toiminto                           | Käytä tätä pikanäppäinkoodia |
|--------------------------------------|----------------------------|
| Suodata yrityksen mukaan                    | Alt+C                      |
| Suodatus dimension perusteella                  | Alt+D                      |
| Valitse Ryhmittely-kenttä            | Alt+R                      |
| Näytä pois jätetyt rakenneosat ja arvot      | Alt+N                      |
| Päivitä tulokset                      | Alt+P                      |
| Jätä valittu rakenneosa pois  | Alt+J                      |
| Jätä valittu rivimääritys pois  | Ctrl+B                     |
| Jätä valittu dimensioarvo pois | Ctrl+D                     |
| Avaa valittu raporttimääritys  | Ctrl+R                     |
| Avaa valittu rivimääritys     | Ctrl+O                     |


## <a name="additional-resources"></a>Lisäresurssit

[Talousraportointi](financial-reporting-intro.md)

[Raporttien suunnitteluohjelman käyttöliittymä](report-designer-interface.md)
