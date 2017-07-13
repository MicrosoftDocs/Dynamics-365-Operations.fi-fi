---
title: Kustannuslaskennan sanasto
description: "Tässä aiheessa määritetään kustannuslaskennassa käytettyjä keskeisiä termejä."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 35b8e510e7e2c13aebb73f46d20b16275d097432
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Kustannuslaskennan sanasto
<a id="cost-accounting-terminology" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä aiheessa määritetään kustannuslaskennassa käytettyjä keskeisiä termejä.

**Kustannuslaskenta**

Kustannuslaskentaan voidaan kerätä tietoja useista eri lähteistä, kuten kirjanpidosta, alareskontrista, budjeteista ja tilastotiedoista. Kustannustietoja voidaan analysoida, arvioida ja tehdä yhteenvetoja, jotta yritysjohto voi tehdä tarvittavat päätökset esimerkiksi hinnanpäivityksistä, budjeteista ja kustannusseurannasta. Lähdetietoja, joita käytetään kustannusten analysoimisessa, käsitellään itsenäisesti kustannuslaskennassa. Kustannuslaskennan päivitykset eivät tämän vuoksi vaikuta lähdetietoihin. Kun keräät kustannustietoja eri paikoista ja erityisesti tuotaessa päätilit kirjanpidosta kustannustasoina Microsoft Dynamics 365 for Finance and Operations Enterprise edition -ratkaisuun, sillä on päällekkäisiä tietoja koska samat tiedot ovat sekä kirjanpidossa että kustannuslaskennassa. Toistoa tarvitaan, koska taloushallintoa käytetään ulkoiseen raportointiin ja kustannuslaskentaa sisäistä raportointia varten.

**Kustannuslaskennan kirjanpito**

Kustannuslaskennan kirjanpito on erityinen kehikko, joka määrittää, miten prosessit, määrät ja arvot kirjataan ja esitetään kustannuslaskennan tietyllä alueella. Kustannuslaskennan kirjanpito määrittää prosessit ja säännöt kustannusten mittaukselle kustannusobjekteissa. Se käsittelee kustannustapahtumia ja hallitsee tiedostoja, joihin kirjataan muutokset arvoissa ja määrissä, joita kustannustapahtumat tuottavat.

**Kustannusmerkintä**

Kustannustapahtumat muodostuvat siirroista, jotka tehdään tietoyhdistimillä kirjanpidon merkinnöistä, kustannusten kohdistuksista ja kustannusten kirjauskansioihin kirjatuista kustannustapahtumista.

**Kustannusobjekti**

Kustannusobjektit ovat mitä tahansa objektityyppejä, joille kohdistetaan kustannuksia. Tyypillisiä kustannusobjekteja ovat:

-   Tuotteet
-   Projektit
-   Resurssit
-   Osastot
-   Kustannuspaikat
-   Maantieteelliset alueet

Yritysjohto käyttää kustannusobjekteja kustannusten määrittämiseen ja kannattavuusanalyysin tekemiseen.

**Kustannustaso**

Kustannustasoja käytetään seurattaessa ja luokiteltaessa, mihin kustannukset siirtyvät. Kustannustasoja on kahdenlaisia: ensisijaiset ja toissijaiset kustannukset. **Ensisijaiset kulut** Ensisijaiset kustannustasot edustavat kustannusvirtaa kirjanpidosta kustannuslaskentaan. Kustannustasorakenne vastaa kirjanpidon tuloksen tilirakennetta, jossa kustannustaso voi vastata päätiliä. Liiketoiminnan vaatimusten mukaisesti kaikkia päätilejä ei voida merkitä kustannustasoiksi. Seuraavassa on esimerkkejä ensisijaisista kustannustasoista:

-   Myytyjen tuotteiden kustannukset (COG)
-   Epäsuorat materiaalikustannukset
-   Henkilökunnan kustannukset
-   Energiakustannukset

**Toissijainen kustannustaso** 

Toissijaiset kustannustasot edustavat sisäistä kustannusvirtaa, koska nämä kustannukset luodaan ja niitä käytetään ainoastaan kustannuslaskennassa. Toissijaisten kustannustasojen avulla taataan kustannuslähteiden jäljitettävyys. Näitä kustannustasoja käytetään kustannusten kohdistuksiin ja yleiskustannuslaskelmiin. Seuraavassa on esimerkkejä toissijaisista kustannustasoista:

-   Tuotantokustannukset
-   Tuotannon, materiaalien ja markkinoinnin yleiskustannukset

**Kustannusseurantayksikkö**

Kustannusseurantayksikkö edustaa kustannusrakennetta. Se täytyy liittää kustannusobjektin dimensioihin kustannuslaskennan kirjanpidossa.

**Versio**

Versioita käytetään eri tulosten simulointiin, tarkasteluun ja vertailuun. Oletusarvoisesti kaikkia toteutuneita kustannuksia tarkastellaan yhdessä perusversiossa, josta käytetään nimitystä *toteutunut*. Budjeteista ja laskelmista voit käsitellä niin monta versiota kuin tarvitset. Voit esimerkiksi tuoda budjetin tiedot alkuperäiseen versioon ja korjata budjettia uudessa versiossa. Voit luoda laskelmista useita versioita. Näihin eri versioihin voit luoda laskelmia käyttämällä erilaisia laskentasääntöjä, jota käytetään kustannusten kohdistamiseen.

**Laskelma**

Laskelmat näkyvät esimiehille, jotka ovat vastuussa kustannusten hallinnasta. Kustannusten vastuuhenkilöt määrittävät laskelmat, joista saadaan yleiskatsaus todellisista ja budjetoiduista kustannuksista, poikkeamista ja laskelmaversioista. Laskelmissa näkyviin tietoihin sovelletaan käyttöoikeussääntöjä sen takaamiseksi, että esimiehet näkevät vain tiedot, joista he ovat vastuussa.

**Data Connector -sovellus**

Tiedot voidaan tuoda kustannuslaskentaan ulkoisista järjestelmistä tietoyhdistimien kautta. Voit esimerkiksi tuoda tilirakenteet, dimensiot, kirjanpidon tapahtumat ja budjettitapahtumat. Voit käyttää esimääritettyjä tietoyhdistimiä tai mukautettuja yhdistimiä tiedon tuontiin ja tietoyhteyksien luontiin.

**Kustannusluokittelu**

Kustannusluokittelu ryhmittää kustannukset yhteisten ominaisuuksien perusteella. Esimerkiksi kustannukset voidaan ryhmitellä tason, jäljitettävyyden ja käyttäytymisen perusteella.

-   **Tasot**: materiaali, työ ja kulut.
-   **Jäljitettävyys**: välittömät ja välilliset kustannukset. Välittömät kustannukset määritetään kustannusobjekteiksi. Välilliset kustannukset eivät ole suoraan jäljitettävissä kustannusobjekteihin. Epäsuorat kustannukset kohdistetaan kustannusobjekteihin.
-   **Käyttäytyminen**: kiinteät, muuttuvat ja puolimuuttuvat.

**Kustannusten käyttäytyminen**

Kustannusten käyttäytyminen luokittelee kustannukset sen mukaan, miten ne käyttäytyvät suhteessa keskeisen liiketoiminnan muutoksiin. Tehokas kustannusten hallinta edellyttää yrityksen johdolta kustannusten käyttäytymisen ymmärtämistä. Kustannusten käyttäytyminen jaetaan kolmeen tyyppiin: kiinteät, muuttuvat ja puolimuuttuvat kustannukset.

- **Kiinteä kustannus** - Kiinteä kustannus tarkoittaa kustannuksia, jotka eivät vaihtele lyhyellä aikavälillä riippumatta tuotannon muutoksista. Kiinteät kustannukset voivat olla esimerkiksi yrityksen perustoimintojen kuluja, kuten vuokra, johon tuotannon kasvu tai lasku ei vaikuta.

- **Muuttuva kustannut** - Muuttuva kustannus vaihtelee toiminnan muutosten mukaan. Esimerkiksi tietyt suorat materiaalikustannukset liittyvät jokaiseen myytävään tuotteeseen. Materiaalikustannukset ovat sitä suuremmat, mitä enemmän tuotteita myydään.

- **Puolimuuttuva kustannus** - Puolimuuttuvat kustannukset ovat osittain kiinteitä ja osittain muuttuvia kustannuksia. Esimerkiksi Internetin käyttökustannukset sisältävät kuukausittaisen perusmaksun ja laajakaistan käyttömaksun. Kuukausittainen perusmaksu on kiinteä kustannus, kun taas laajakaistan käyttömaksu on muuttuva kustannus.

**Yleiskustannus**

Yleiskustannuksilla tarkoitetaan liiketoiminnan juoksevia toimintakustannuksia. Ne ovat kustannuksia, joita ei voi yhdistää suoraan yrityksen liiketoimintoihin. Seuraavassa on joitakin esimerkkejä yleiskustannuksista:

-   Kirjanpitomaksut
-   Poistot
-   Vakuutus
-   Korot
-   Oikeudenkäyntikulut
-   Verot
-   Julkisten palvelujen kustannukset

**Kustannusten kohdistus**

Kustannusten kohdistus on kustannusten määritys- ja kohdistamisprosessi, joka perustuu yhteiskustannusten alkuperään. Kustannussummat ja -määrät kohdistetaan yhdestä kustannusobjektista yhteen tai useampaan kustannusobjektiin. Esimerkiksi kaikki toimitilan palvelujen kustannukset kohdistetaan eri osastoille, jotka käyttävät samaa toimistorakennusta.

**Kustannusten kohdistuskäytäntö**

Kustannusten kohdistuskäytäntö määrittää kohdistettavat summat ja määrät. Kohdistussääntöihin kuuluvat kohdistuksen lähdesäännöt, jotka määrittävät, mitkä kustannukset kohdistetaan, ja kohdistuksen kohdesäännöt, jotka määrittävät, mihin kustannukset kohdistetaan. Esimerkiksi kaikki toimitilan palvelujen kustannukset ovat kohdistuksen lähde, joka voidaan kohdistaa organisaation eri osastoille (ts. kohdistuksen kohteille).

**Kohdistusperuste**

Kohdistusperuste on perusta, jonka avulla voidaan laskea ja määrittää toimintoja, kuten koneen käyttötunnit, energiankulutus kilowattitunteina, käytetyt työtunnit tai varatut neliömetrit. Sitä käytetään kohdistettaessa kustannuksia yhdelle tai useammalle kustannusobjektille.

**Kohdistusperiaate**

Eräs kohdistusperiaate on kohdistaa kustannukset kustannushinnan perusteella. Voit kohdistaa kustannukset todellisen kausihinnan tai hintahistorian perusteella. Kohdistus, joka käyttää vastavuoroisia tapaa, varmistaa, että kohdistusperuste määräytyy samanaikaisten rinnastusten perusteella ennen kuin kohdistus tehdään todellisen kausihinnan mukaan.

**Kustannusten koonti**

Kustannusten koontilaskelmien tarkoituksena on sisällyttää kaikki tietyn kustannusobjektin kaikki kustannukset. Koostetaso on käyttäjän määrittämä. Kustannusten koontilaskelmien avulla voit yhdistää kustannukset, jotka täytyy kohdistaa kustannusobjektista toiseen. Kun kustannusten koontilaskelmia ei käytetä, jokainen kustannustaso kohdistetaan kustannusobjektista toiseen.

**Kustannushintakäytäntö**

Kustannushintaa käytetään kustannusobjektikohtaisen hinnan laskemiseen. Kustannushintakäytännön avulla on mahdollista määrittää hinnan muodostumisen tekijät. Kustannushintoja on kahta tyyppiä: historiallinen kustannushinta ja suunniteltu kustannushinta. Historiallisten kustannushinta on laskettu hinta, jota käytetään kustannusobjektin kohdistusperusteen kertoimena. Hinta lasketaan edellisen kauden kustannusten kohdistusten perusteella. Suunniteltu hinta on käyttäjän määrittämä hinta.

**Dimensiohierarkia**

Dimensiohierarkioita käytetään raportoinnin rakenteina määritettäessä kohdistuksen, kustannushinnan ja kustannusten koontilaskelmien sääntöjä, tarkasteltaessa selvityksiä tai tietoja Microsoft Excelissä ja määritettäessä yhdistettyjen tietojen käyttöoikeuksia. Dimensiohierarkioita on kaksi: luokkahierarkian ja luokitteluhierarkia. Luokkahierarkia määritetään kustannustasojen perusteella, ja luokitushierarkian määritetään kustannusobjektien perusteella.

**Tilastodimensio**

Tilastodimensio on määrän ilmentymä tai objektin summa, jota käytetään kohdistusperusteena tai kustannushintalaskelmien perusteena. Se on luotu manuaalisesti tai tuotu lähdejärjestelmistä. Tilastodimensioita ovat esimerkiksi työntekijämäärä, laitteen ohjelmistolisenssien lukumäärä, koneen virrankulutus tai kustannuspaikan pinta-ala.

**Muistiovienti**

Muistioviennit sisältävät tietyn tilastodimension kirjatun summan tai lasketun arvon. Kirjatusta summasta tai lasketusta arvosta käytetään myös nimitystä suuruus.




