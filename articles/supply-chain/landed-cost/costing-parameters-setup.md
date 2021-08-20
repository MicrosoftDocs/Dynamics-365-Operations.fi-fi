---
title: Kustannuslaskennan parametriarvojen määrittäminen
description: Kun määrität Aiheutunut kustannus -moduulia, voit määrittää useita yhteisten arvojen joukkoja, jotka ovat käytettävissä, kun valitset tietyntyyppisiä kustannuslaskennan parametriarvoja sovelluksen muissa osissa. Tässä ohjeaiheessa selitetään, kuinka nämä arvojoukot määritetään.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: dada2f9a3ae13f41b7f63d1f0907002860d0717ff9d8c2453fc6f3ad123cbf78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736740"
---
# <a name="costing-parameter-values-setup"></a>Kustannuslaskennan parametriarvojen määrittäminen

[!include [banner](../../includes/banner.md)]

Kun määrität **Aiheutunut kustannus** -moduulia, voit määrittää useita yhteisten arvojen joukkoja ja arvokohtaisia asetuksia. Nämä arvot ovat käytettävissä, kun valitset tietyntyyppisiä kustannuslaskennan parametriarvoja sovelluksen muissa osiossa. Tässä ohjeaiheessa selitetään, kuinka nämä arvojoukot määritetään.

## <a name="set-up-cost-type-codes"></a>Kustannustyyppien koodien määrittäminen

Kustannustyyppien koodit määrittävät tyypin kustannuksille, joita syntyy tavaroiden saapuessa varastoon, tai merikuljetuksen aiheutuneille kustannuksille. Vaikka ne tavallisesti nostavat tavaroiden arvoa, niitä voidaan käyttää myös summien siirtämiseksi kirjanpitoon. Kirjanpidon oikaisuja käytetään, kun kustannus kertyy ajan myötä, tai merikuljetusten sarjan ja siirtymän aikana yhdessä tapahtumassa.

> [!NOTE]
> Jos yrityksillä on yhteinen kustannustyyppien taulukko, niillä on oltava myös yhteinen tilikartta. Muussa tapauksessa kirjaustapahtumat eivät toimi oikein.

Voit määrittää kustannustyyppien koodit valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Kustannustyyppien koodit**. Toimintoruudun painikkeiden avulla voit luoda uusia kustannustyyppien koodeja, muokata nykyisiä koodeja tai poistaa valitun kustannustyypin.

Seuraava taulukko kuvaa kustannustyyppien koodeille käytettävissä olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Kustannustyypin koodi | Syötä kustannustyypin koodin nimi. |
| kuvaus | Syötä kustannustyypin koodin kuvaus. |
| Käytä lähetyshintaa | Valitse täksi vaihtoehdoksi *Kyllä*, jos näiden kustannusten arvon laskennassa on käytettävä merikuljetuksen vaihtokurssia (jota kutsutaan joskus hallintokurssiksi). Tässä tapauksessa vieraita valuuttoja käyttävien laskujen muuntamiseen käytetään kuljetuksen vaihtokurssia oletusarvoisen vaihtokurssin tai avistakurssin sijaan. |
| Raportointiluokka | Tämä kenttä määrittää kustannustyypin raportointiluokan. Raportit voidaan tulostaa joko raportointiluokkien tai kustannustyypin mukaan. |
| Veloituslaji | Valitse, tulisiko kustannustyyppi veloittaa nimikkeeltä, kirjanpitotililtä vai toimittajalta. |
| Veloituksen kirjaus | Jos **Veloituslaji**-kentän arvoksi on määritetty *Kirjanpitotili*, valitse kirjauksen kuvaus. |
| Debet-tili | Jos **Veloituslaji**-kentän arvoksi on määritetty *Kirjanpitotili*, valitse käytettävä kirjanpitotili. |
| Luottotyyppi | Valitse, tulisiko tämä kustannustyyppi hyvittää nimikkeelle, kirjanpitotilille vai toimittajalle. |
| Hyvityksen kirjaus | Jos **Luottotyyppi**-kentän arvoksi on määritetty *Kirjanpitotili*, valitse kirjauksen kuvaus. |
| Kredit-tili | Jos **Luottotyyppi**-kentän arvoksi on määritetty *Kirjanpitotili*, valitse käytettävä kirjanpitotili. |
| Selvitystili | Valitse kustannustyypin selvitystili. Suosittelemme, että valitset jokaiselle kustannustyypille erillisen selvitystilin täsmäytyksen helpottamiseksi. |
| Standardikustannusten kirjastyyppi | Jos käytät standardikustannuslaskentaa, valitse kirjauksen kuvaus. |
| Vakiokustannusten varianssitili | <p>Jos käytät vakiokustannuslaskentaa, tässä määritettyä tiliä käytetään kaikkien varianssien kirjaamiseen. Tämä tili käyttää aiheutuneiden kustannusten erittelyä **Nimikehinnat**-sivulla. Tämä erittely luodaan käyttämällä säännöllistä rutiinia hintojen päivittämiseen.</p><p>Oletetaan esimerkiksi, että nimikkeen standardikustannus on 15,00 $, FOB on 13,00 $ ja rahti on 2,00 $. Kun lasku vastaanotetaan varastosta, nimike vastaanotetaan 15,00 $ hinnalla, mutta nimikkeellä on 2,00 $ standardikustannusten varianssi, koska todellinen FOB on 13,00 $. Tämä varianssi kirjataan nimikkeen kirjausprofiilissa määritetylle vakiohinnan varianssitilille. Koska arvioitu rahti on 2,00 $, varianssia ei ole, kun varastolasku kirjataan. Kun rahtilasku vastaanotetaan, rahti on kuitenkin 2,50 $ per yksikkö. Määritettyyn kustannukseen kirjataan siis 0,50 $ varianssi. |
| Liukuvan keskiarvon varianssitili | <p>Jos käytät liukuvan keskiarvon kustannuslaskentaa, tässä määritettyä tiliä käytetään kaikkien varianssien kirjaamiseen.</p><p>Oletetaan esimerkiksi, että arvioitu rahti on 2,00 $. Kun rahtilasku vastaanotetaan, rahti on kuitenkin 2,50 $ per yksikkö. Tästä syystä 0,50 $ varianssi kirjataan.</p><p>Kun **Kirjaa oikaisut varianssina** -vaihtoehdoksi on määritetty **Aiheutuneen kustannuksen parametrit** -sivulla *Kyllä*, kaikki arvioitujen ja todellisten kuljetuskustannusten väliset varianssit kirjataan tässä määritetylle liukuvan keskiarvon varianssitilille. Kun **Kirjaa oikaisut varianssina** -vaihtoehdoksi on määritetty *Ei*, käytetään vakiotoimintoa, ja varianssi kirjataan joko varastoon tai tässä määritetylle liukuvan keskiarvon varianssitilille, riippuen käytettävissä olevasta varastosta.</p> |
| Veloituksen jaksotustili | Valitse tili, jota käytetään kustannusarvioiden jaksottamiseen, kun ostolasku kirjataan. Tätä kenttää käytetään vain, kun **Käytä kustannustyypin veloituksen jaksotustiliä** -vaihtoehdoksi on määritetty **Aiheutuneen kustannuksen parametrit** -sivun **Yleiset**-välilehden **Kustannuslaskenta**-pikavälilehdessä *Kyllä*. |
| Veloitustili | Valitse tili, jota käytetään toimittajan laskuttamien saapuvien kuljetuskustannusten taltiointiin. Summa kirjataan veloituksena. Vastatili on varaston varianssitili. Tätä kirjausta käytetään vain, kun **Kirjaa kirjanpidon veloitustilille** -vaihtoehdoksi on määritetty **Ostoreskontran parametrit** -sivulla *Kyllä*. |
| Varianssitili | Tili, jota käytetään veloituksen jaksotusten vastakirjaamiseen, kun ostolaskun kirjataan. Tätä kenttää käytetään vain, kun **Käytä kustannustyypin veloituksen jaksotustiliä** -vaihtoehdoksi on määritetty **Aiheutuneen kustannuksen parametrit** -sivun **Yleiset**-välilehden **Kustannuslaskenta**-pikavälilehdessä *Kyllä*. |

## <a name="vendor-cost-type-groups"></a>Toimittajan kustannustyyppiryhmät

Toimittajan kustannustyyppiryhmät auttavat määrittämään, miten *automaattisten kustannusten* veloitukset haetaan ja lisätään merikuljetukseen. Toimittajat, joilla on samankaltaiset tuontikustannukset, linkitetään yhteen. Esimerkiksi kaikki kehittyvien markkinoiden toimittajat maksavat prosentuaalisesti saman tullimaksun samantyyppisestä tuotteesta, joka ostetaan vakiintuneilta markkinoilta.

Voit ylläpitää toimittajien kustannustyyppiryhmiä valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Toimittajien kustannustyyppiryhmät**. **Toimittajien kustannustyyppiryhmät** -sivulla on ruudukko, jossa luetellaan kaikki toimittajien kustannustyyppiryhmät. Voit lisätä, poistaa ja muokata ruudukon rivejä käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä ruudukon kullakin rivillä.

| Kenttä | kuvaus |
|---|---|
| Toimittajan kustannustyyppiryhmät | Syötä toimittajien kustannustyyppiryhmälle yksilöivä nimi (kuten *Kehittyvät markkinat*). |
| kuvaus | Syötä toimittajien kustannustyyppiryhmän kuvaus. Tämä kuvaus voi tarjota tietoja toimittajien ryhmään liitetyn veloituksen tasosta tai tyypistä. |

## <a name="item-cost-type-groups"></a>Nimikkeen kustannustyyppiryhmät

Nimikkeiden kustannustyyppiryhmät auttavat määrittämään, miten *automaattisten kustannusten* veloitukset haetaan ja lisätään merikuljetukseen. Samankaltaiset nimikkeet linkitetään yhteen. Esimerkiksi kaikki nimikkeet, joilla on 5 prosentin tullimaksu, voivat kuulua samaan kustannustyyppiryhmään.

Voit ylläpitää nimikkeiden kustannustyyppiryhmiä valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Nimikkeiden kustannustyyppiryhmät**. **Nimikkeiden kustannustyyppiryhmät** -sivulla on ruudukko, jossa luetellaan kaikki nimikkeiden kustannustyyppiryhmät. Voit lisätä, poistaa ja muokata ruudukon rivejä käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä ruudukon kullakin rivillä.

| Kenttä | kuvaus |
|---|---|
| Nimikkeen kustannustyyppiryhmät | Syötä nimikkeiden kustannustyyppiryhmälle yksilöivä nimi (kuten *Tulli 5 %*). |
| kuvaus | Syötä nimikkeiden kustannustyyppiryhmän kuvaus. Tämä kuvaus voi tarjota tietoja nimikkeiden ryhmään liitetyn veloituksen tasosta tai tyypistä. |

> [!NOTE]
> Nimikkeiden kustannustyyppi linkitetään nimikkeeseen nimikkeen **Vapautettu tuote** -sivun **Osto**-pikavälilehden **Kustannustyyppiryhmä**-kentän kautta.

## <a name="transfer-order-cost-type-groups"></a>Siirtotilausten kustannustyyppiryhmät

Siirtotilausten kustannustyyppiryhmät auttavat määrittämään, miten *automaattisten kustannusten* veloitukset haetaan. Samankaltaiset nimikkeet linkitetään yhteen. Esimerkiksi kaikki nimikkeet, joilla on 7 prosentin tullimaksu, voivat kuulua samaan kustannustyyppiryhmään.

Voit ylläpitää siirtotilausten kustannustyyppiryhmiä valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Siirtotilausten kustannustyyppiryhmät**. **Siirtotilausten kustannustyyppiryhmät** -sivulla on ruudukko, jossa luetellaan kaikki siirtotilausten kustannustyyppiryhmät. Voit lisätä, poistaa ja muokata ruudukon rivejä käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä ruudukon kullakin rivillä.

| Kenttä | kuvaus |
|---|---|
| Siirtotilausten kustannustyyppiryhmät | Syötä siirtotilausten kustannustyyppiryhmälle yksilöivä nimi (kuten *Tulli 7 %*). |
| kuvaus | Syötä siirtotilausten kustannustyyppiryhmän kuvaus. Tämä kuvaus voi tarjota tietoja siirtotilausten kustannustyyppiryhmään liitetyn veloituksen tasosta tai tyypistä. |

> [!NOTE]
> Siirtotilausten kustannustyyppi linkitetään nimikkeeseen nimikkeen **Vapautettu tuote** -sivun **Osto**-pikavälilehden **Siirtotilausten kustannusryhmä** -kentän kautta.

## <a name="cost-templates"></a>Kustannusmallit

Käytä kustannusmalleja määrittääksesi oletusarvoja asetuksille, joita kustannusarviota hakevat käyttäjät eivät välttämättä tiedä. Kustannusmallit voivat tehdä arviointiprosessista yksinkertaisemman vähentämällä valintoja, joita käyttäjien täytyy tehdä saadakseen tarkan arvion.

Voit työstää kustannusmalleja valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Kustannusmallit**. **Kustannusmallit**-sivun vasemmassa laidassa oleva luetteloruutu näyttää kaikki tämänhetkiset kustannusmallit. Voit lisätä, poistaa ja muokata malleja käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä kullekin mallille.

| Kenttä | kuvaus |
|---|---|
| Kustannusmalli | Syötä kustannusmallille yksilöivä nimi. Nimi kuvaa yleensä mallin kerrointa tai kustannuskerrointa. |
| kuvaus | Syötä kustannusmallille kuvaus. |
| Kuljetusyritys | Valitse kustannusmalliin liitettävä rahdinkuljettajan toimittajatili. |
| Toimitustapa | Valitse toimitustapa, jota kustannusmallin tulisi käyttää, kun nimikkeen arvioitu kustannus lasketaan. Tämä kenttä auttaa määrittämään tavaroihin liittyvät automaattiset kustannukset kustannusarviossa. |
| Lähetyskontin tyyppi | Valitse kustannusmalliin liitettävä konttityyppi. Tämä kenttä auttaa määrittämään tavaroihin liittyvät automaattiset kustannukset kustannusarviossa. |
| Tulliasiamies | Valitse kustannusmalliin liitettävä tulliasiamies (toimittaja). Tämä kenttä auttaa määrittämään kustannusarvioon liitetyt automaattiset kustannukset. |
| Kerroin | Syötä kerroin, jota käytetään tavaroiden lopullisessa kustannusarviossa. Jos haluat lisätä laskettuun kustannusarvioon esimerkiksi 10 prosenttia, syötä arvoksi *1,10*. |

## <a name="volumetric-divisors"></a>Tilavuusjakajat

Tilavuusjakajia käytetään tilavuuspainon laskemiseen. Jokainen kuljetus-/rahtiyritys määrittää omat tilavuusjakajansa. Lisäksi yrityksen jakajat vaihtelevat tavallisesti toimitustavan mukaan. Esimerkiksi lento- ja vesikuljetusten jakajat ovat usein hyvin erilaisia. Yritys voi myös tehdä säännöistään monimutkaisempia riippuen sen lähetyssijainnista.

Oletetaan esimerkiksi, että lentorahtina lähetetyn paketin tilavuus on 3 kuutiometriä (m³). Yritys veloittaa tilavuuspainon mukana ja sen tilavuusjakaja on 6. Tämä jakaja kerrotaan tilavuudella tilavuuspainon määrittämiseksi. Näin ollen tilavuuspaino on tässä esimerkissä 3 × 6 = 18 kilogrammaa (kg).

Voit määrittää tilavuusjakajia valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Tilavuusjakajat**. **Tilavuusjakajat** -sivulla on ruudukko, joka luetellaan kaikki olemassa olevat tilavuusjakajat. Voit lisätä, poistaa ja muokata ruudukon rivejä käyttämällä toimintoruudun painikkeita.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä ruudukon kullakin rivillä.

| Kenttä | kuvaus |
|---|---|
| Kuljetusyritys | Valitse tilavuusjakajaan liittyvä rahdinkuljettajan toimittajatili. |
| Kustannustyypin koodi | Valitse tilavuusjakajaan liittyvä kustannustyypin koodi. Käytä tätä kenttää lajitellaksesi kustannustyypit raportointisäiliöihin. Raportit voidaan tulostaa joko raportointiluokkien tai kustannustyypin mukaan. |
| Lähtösatama | Valitse lähtösatama, jota tilavuusjakaja koskee. |
| Tilavuusjakaja | Valitse riville käytettävä tilavuusjakajan arvo. Syöttämäsi arvo *kerrotaan* kunkin paketin tilavuudella paketin tilavuuspainon määrittämiseksi. |
