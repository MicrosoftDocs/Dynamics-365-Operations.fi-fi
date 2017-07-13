---
title: Vuoron- ja kassanhallinta
description: "Tässä artikkelissa käsitellään kahden vähittäismyynnin myyntipistetyypin vuoron määrittämistä ja käyttöä. Vuoro voi olla jaettu tai erillinen. Useat käyttäjät voivat käyttää jaettuja vuoroja useassa paikassa, kun taas vain yksi työntekijä voi käyttää erillistä vuoroa."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0d5e05e8f1edcc01af985c25459d93de0bc2acf1
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017



---

# Vuoron- ja kassanhallinta
<a id="shift-and-cash-drawer-management" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä artikkelissa käsitellään kahden vähittäismyynnin myyntipistetyypin vuoron määrittämistä ja käyttöä. Vuoro voi olla jaettu tai erillinen. Useat käyttäjät voivat käyttää jaettuja vuoroja useassa paikassa, kun taas vain yksi työntekijä voi käyttää erillistä vuoroa.

Vähittäismyynnin myyntipistevuoroja on kahdenlaisia: erillinen ja jaettu. Yksi työntekijä kerrallaan voi käyttää erillistä vuoroa. Useat käyttäjät voivat käyttää jaettua vuoroa useassa paikassa. Niillä voikin luoda tehokkaasti yhden vuoron useille myymälän työntekijöille.

## Erilliset vuorot
<a id="standalone-shifts" class="xliff"></a>
Erillisiä vuoroja käytetään perinteisissä kiinteissä myyntipisteskenaarioissa, joissa kassa täsmätään erikseen jokaisessa myyntipisteen kassakoneessa. Esimerkiksi elintarvikemyymälässä on tavallisesti useita kiinteitä myyntipisteen kassakoneita ja kullekin kassakoneelle on määritetty kassa. Tässä tapauksessa jokaisessa kassakoneessa käytetään todennäköisesti erillistä vuoroa ja kassa vastaa kassasta tai kassakoneen fyysisestä kassasta. Erillinen vuoro käsittää kaikki kassakoneen tapahtumat kassan työvuoron aikana. Tehtäviä voivat olla kassaan talletettu alkusumma, kaikki poistot ja lisäykset kassaan eri toiminnoilla, kuten toimitukset pankkiin ja liukuva merkintä, ja kassan laskeminen maksuvälineittäin vuoron lopussa.

### Määritä erillinen vuoro
<a id="set-up-a-stand-alone-shift" class="xliff"></a>

Erillinen vuoro määritetään kassatasolla. Tässä menettelyssä käsitellään erillisen vuoron määrittäminen myyntipisteen kassakoneessa.

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteiden asetukset** &gt; **Myyntipisteiden profiilit** &gt; **Laiteprofiilit**.
2.  Valitse erillisessä vuorossa käytettävä laiteprofiili.
3.  Vahvista **Kassa**-pikavälilehdessä, että **Jaetun vuoron kassa** -asetukseksi on valittu **Ei**.
4.  Valitse **Tallenna**.
5.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
6.  Valitse ensin kassakone, jossa käytetään erillistä vuoroa, ja sitten **Muokkaa**.
7.  Valitse **Laiteprofiili**-kentässä sama laiteprofiili, jonka valitsit vaiheessa 2.
8.  Valitse **Tallenna**.
9.  Valitse **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
10. Synkronoi myyntipisteen muutokset valitsemalla ensin **1090**-jakeluaikataulu ja sitten **Suorita nyt**.

### Käytä erillistä vuoroa
<a id="use-a-stand-alone-shift" class="xliff"></a>

1.  Kirjaudu myyntipisteeseen.
2.  Jos yhtään avointa vuoroa ei ole, valitse **Avaa uusi vuoro**.
3.  Valitse **Tilitä aloitussumma** -toiminto ja määritä kassaan työpäivän alussa lisättävän kassan määrä.
4.  Tee muutamia tapahtumia.
5.  Laske jäljellä oleva kassa valitsemalla päivän lopussa **Laske kassa maksuvälineittäin**.
6.  Anna kassan summa ja tallenna maksuvälineittäin laskettu kassa valitsemalla **Tallenna**.
7.  Sulje vuoro valitsemalla **Sulje vuoro**.

**Huomautus:** Vuoron aikana on käytettävissä muita toimintoja sen mukaan, mitä liiketoimintaprosesseja on käytössä. **Toimitus kassakaappiin**-, **Toimitus pankkiin**- ja **Maksuvälineen poisto** -toiminnoilla voidaan poistaa rahaa kassasta päivän aikana tai ennen vuoron sulkemista. Jos kassa käy vähiin, kassaa voidaan lisätä **Liukuva merkintä** -toiminnolla.

## Jaetut vuorot
<a id="shared-shifts" class="xliff"></a>
Jaettua vuoroa käytetään ympäristössä, jossa kassalla tai kassaryhmällä on useita käyttäjiä työpäivän aikana. Jaettua vuoroa käytetään yleensä mobiilimyyntipisteympäristöissä. Mobiiliympäristössä kassoja ei määritetä henkilökohtaisesti eikä yksittäinen henkilö vastaa tietystä kassasta. Sen sijaan kaikkien kassojen on voitava hoitaa myynti ja täydentää kassaa heitä lähimmässä kassassa. Tässä skenaariossa jaetut kassat sisältyvät jaettuun vuoroon. Kaikki jaetun vuoron kassat sisältyvät samaan vuoroon, jotta vuoron kassanhallintaan liittyvät toimet voidaan hoitaa. Vuoron alkusumman pitäisikin siksi sisältää kaikkien jaettuun vuoroon sisältyvin kassojen yhteiskassavarat. Samoin kassan laskeminen maksuvälineittäin on kaikkien jaettuun vuoroon sisältyvin kassojen yhteiskassavarat. **Huomautus:** Kussakin myymälässä voi olla avoinna samanaikaisesti vain yksi jaettu vuoro. Samassa myymälässä voi käyttää jaettuja vuoroja ja erillisiä vuoroja.

### Määritä jaettu vuoro
<a id="set-up-a-shared-shift" class="xliff"></a>

1.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteiden asetukset** &gt; **Myyntipisteiden profiilit** &gt; **Laiteprofiilit**.
2.  Valitse jaetussa vuorossa käytettävä laiteprofiili.
3.  Valitse **Kassa**-pikavälilehdessä **Jaetun vuoron kassa** -asetukseksi **Kyllä**.
4.  Valitse **Tallenna**.
5.  Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.
6.  Valitse ensin kassakone, jossa käytetään jaettua vuoroa, ja sitten **Muokkaa**.
7.  Valitse **Laiteprofiili**-kentässä sama laiteprofiili, jonka valitsit vaiheessa 2.
8.  Valitse **Tallenna**.
9.  Valitse **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.
10. Synkronoi myyntipisteen muutokset valitsemalla ensin **1090**-jakeluaikataulu ja sitten **Suorita nyt**.

### Käytä jaettua vuoroa
<a id="use-a-shared-shift" class="xliff"></a>

1.  Kirjaudu myyntipisteeseen.
2.  Jos myyntipistettä ei ole vielä liitetty laiteasemaan, aktivoi jaetun vuoron laiteasema valitsemalla ensin **Muu kuin kassatoiminto** ja sitten **Valitse laiteasema** -toiminto. Tämä vaihe on tarvittava tehdä vain, kun kassakone lisätään ensimmäisen kerran jaettuun vuoroympäristöön.
3.  Kirjaudu ulos myyntipisteestä ja kirjaudu takaisin sisään.
4.  Valitse **Luo uusi vuoro**.
5.  Valitse **Tilitä aloitussumma**.
6.  Anna myymälän kaikkien jaettuun vuoroon sisältyvien kassojen aloitussumma ja valitse sitten **Tallenna**.
    -   Lisää aloitussumman osa jokaiseen seuraavaan kassaan, aktivoi laiteasema **Valitse laiteasema**-toiminnolla.
    -   Voit lisätä tietyn kassan kassaan **Avaa kassa** -toiminnolla.
    -   Jatka, kunnes kaikilla jaetun vuoron kassoilla on osa aloitussummaa.

7.  Avaa päivän lopussa kukin kassa ja poista kassavarat.
8.  Kun olet poistanut kassavarat viimeisestä kassasta, laske kaikki kassat.
9.  Laske kaikkien jaetun vuoron kassojen kokonaiskassa **Laske kassa maksuvälineittäin** -toiminnolla.
10. Sulje jaettu vuoro **Sulje vuoro** -toiminnolla.





