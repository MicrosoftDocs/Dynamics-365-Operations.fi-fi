---
title: "Painotettu keskiarvo, fyysinen arvo ja merkintä"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cdbca6d9c71c901a1f4e7a8e5a2f9be1d3efb355
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Painotettu keskiarvo, fyysinen arvo ja merkintä

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



Kun suoritat varaston sulkemisen, kaikki vastaanotot täsmäytetään suhteessa virtuaalivarastostaottoon, joka sisältää vastaanotetun kokonaismäärän ja -arvon. Tällä virtuaalivarastostaotolla on vastaava virtuaalivastaanotto, josta varastostaotot täsmäytetään. Näin kaikille varastostaotoille tulee sama keskimääräinen kustannus. Virtuaalivarastostaoton ja -vastaanoton voi nähdä virtuaalisiirtona, jota kutsutaan painotetun keskiarvon varastonsulkemissiirroksi.

Jos vastaanottoja on vain yksi, kaikki varastostaotot voi täsmäyttää siitä, eikä virtuaalisiirtoa luoda. 

Painotettua keskiarvoa käytettäessä varastotapahtumat merkitään siten, että tietty nimikkeen vastaanotto täsmäytetään suhteessa tiettyyn varastostaottoon painotetun keskiarvon säännön käyttämisen sijaan. 

Käytettäessä painotetun keskiarvon varastomallia on suositeltavaa käyttää kuukausittaista varaston sulkemista. 

Varaston painotetun keskiarvon kustannuslaskentamenetelmä lasketaan seuraavalla kaavalla:
-   Painotettu keskiarvo = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Varasto-otoista lähtevät varastotapahtumat Sisältää myyntitilaukset, varastokirjauskansiot ja tuotantotilaukset, jotka tapahtuvat arvioituun kustannushintaan kirjauspäivämääränä. Tätä arvioitua kustannushintaa kutsutaan myös keskiarvoksi. Varaston sulkemisen yhteydessä järjestelmä analysoi edellisen ja nykyisen kauden varastotapahtumat ja määrittää, kumpaa seuraavista sulkemisperiaatteista käytetään.
-   suora täsmäytys
-   yhteenvetotäsmäytys.

Selvitykset ovat varaston sulkemiskirjauksia, jotka säätävät varastostaotot sulkemispäivän oikean painotetun keskiarvon mukaisiksi. Seuraavissa esimerkeissä kuvataan painotetun keskiarvon käytön vaikutusta viidessä eri konfiguraatiossa:
-   Painotetun keskiarvon suora täsmäytys ilman Sisällytä fyysinen arvo -vaihtoehtoa
-   Painotetun keskiarvon yhteenvetotäsmäytys ilman Sisällytä fyysinen arvo -valintaa
-   Painotetun keskiarvon suora täsmäytys ja Sisällytä fyysinen arvo -valinta
-   Painotetun keskiarvon yhteenvetotäsmäytys ja Sisällytä fyysinen arvo -valinta
-   Painotettu keskiarvo ja merkintä

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Painotetun keskiarvon suora täsmäytys ilman Sisällytä fyysinen arvo -valintaa
Suoran täsmäytyksen periaate on sama kuin se, jota edellisissä versioissa käytettiin painotetun keskiarvon yhteydessä. Järjestelmä tekee suoran selvityksen vastaanottojen ja varastostaottojen välillä. Järjestelmä käyttää tätä suoran selvityksen periaatetta seuraavissa määrätyissä tilanteissa:
-   Kauden aikana on kirjattu yksi vastaanotto ja vähintään yksi varastostaotto.
-   Kauden aikana on kirjattu vain varastostaottoja, ja varasto sisältää käytettävissä olevia nimikkeitä aiemmasta sulkemisesta.

Seuraavien kohtien skenaariossa on kirjattu vastaanotto ja varastostaotto, jotka on päivitetty kirjanpitoon. Varaston sulkemisen aikana järjestelmä selvittää vastaanoton suoraan varastostaottoa vasten, eikä varastostaottoa varten tarvita kustannushinnan muutosta. Graafisessa esityksessä on kuvattu seuraavat tapahtumat.
-   1a. Varaston fyysinen vastaanotto päivitetty määrälle 5 yksikköhintaan 10,00 USD
-   1b. Varaston taloudellinen vastaanotto päivitetty määrälle 5 yksikköhintaan 10,00 USD
-   2a. Fyysinen varasto-otto päivitetty määrälle 2 yksikköhintaan 10,00 USD
-   2b. Rahoituksellinen varasto-otto päivitetty määrälle 2 yksikköhintaan 10,00 USD
-   3. Varaston sulkeminen suoritetaan suoran täsmäytyksen menetelmällä. Tällöin rahoituksellinen varastovastaanotto täsmäytetään rahoituksellisen varasto-oton kanssa.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja suoran täsmäytysperiaatteen vaikutusta tähän tapahtumien sarjaan, kun Sisällytä fyysinen arvo -vaihtoehtoa ei käytetä. 

![Painotettu keskiarvo - suora maksu - fyysistä arvoa ei sisällytetä](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Kaavion selite**
-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Hakasulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman hakasulkeita oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä Inventory Close.
-   Varaston sulkemisen suorittamat täsmäytykset on merkitty punaisilla pistenuolilla, jotka osoittavat vinosti vastaanotosta varasto-ottoon.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Painotetun keskiarvon yhteenvetotäsmäytys ilman Sisällytä fyysinen arvo -valintaa
Painotettu käyttää täsmäytysperiaatteena sitä, että kaikki tietyllä sulkemisjaksolla tapahtuvat vastaanotot lasketaan yhteen Painotetun keskiarvon varaston sulkeminen -nimiseksi tapahtumaksi. Kaikki jakson vastaanotot täsmäytetään luodun uuden varastosiirtotapahtuman varastostaottoa vastaan. Kaikki jakson varastostaotot täsmäytetään uuden varastosiirtotapahtuman vastaanottoa vastaan. Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen positiivinen, käytettävistä olevasta varastosta ja varaston arvosta tehdään yhteenveto uuteen varastosiirtotapahtumaan (vastaanotto). Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen negatiivinen, käytettävissä oleva varasto ja varaston arvo ovat sellaisten yksittäisten varastostaottojen summa, joita ei ole täysin selvitetty. Oheisessa esimerkkitilanteessa on kirjattu useita rahoituksellisesti päivitettyjä vastaanottoja ja yksi varasto-otto. 

Varaston sulkemisen yhteydessä järjestelmä luo ja kirjaa yhteenlasketun varastosiirtotapahtuman sekä täsmäyttää kaikki jakson vastaanotot yhteenlasketun varastosiirron varastostaottotapahtumaa vastaan. Kaikki jaksolle kirjatut varastostaotot täsmäytetään yhteenlasketun varastosiirron vastaanottotapahtumaa vastaan. Painotetuksi keskiarvoksi on laskettu 15,00 USD. Varastostaotto on alun perin kirjattu arvioituun kustannushintaan 14,67 USD. Varastostaottotapahtumalle luodaan ja kirjataan siten 0,33 USD:n negatiivinen oikaisu. Varaston sulkemispäivämääränä käytettävissä olevassa varastossa on 3 kappaletta, ja niiden arvo on 45,00 Yhdysvaltain dollaria (USD). 

Seuraavat tapahtumat on havainnollistettu oheisessa kuvassa:
-   1a. Varaston fyysinen vastaanotto päivitetty määrälle 2 yksikkökustannuksen ollessa 11,00 USD.
-   1b. Varaston taloudellinen vastaanotto päivitetty määrälle 2 yksikkökustannuksen ollessa 14,00 USD.
-   2a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 12,00 USD.
-   2b. Varaston taloudellinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 16,00 USD.
-   3a. Fyysinen varasto-otto päivitetty määrälle 1 yksikkökustannuksen ollessa 14,67 USD (keskiarvo).
-   3b. Rahoituksellinen varasto-otto päivitetty määrälle 1 yksikkökustannuksen ollessa 14,67 USD (keskiarvo).
-   4a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 14,00 USD.
-   4b. Varaston taloudellinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 16,00 USD.
-   5. Varaston sulkeminen on suoritettu.
-   6a. "Painotetun keskiarvon varaston sulkemistapahtuman" rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.
-   6b. "Painotetun keskiarvon varastosulkemistapahtuman” rahoituksellinen varastovastaanotto muodostetaan kohteen 5a vastakirjaukseksi.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun Sisällytä fyysinen arvo -vaihtoehtoa ei käytetä. 

![Painotettu keskiarvo - maksun yhteenveto - fyysistä arvoa ei sisällytetä](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Kaavion selite**
-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Hakasulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman hakasulkeita oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä Inventory Close.
-   Varaston sulkemisen suorittamat täsmäytykset on merkitty punaisilla pistenuolilla, jotka osoittavat vinosti vastaanotosta varasto-ottoon.
-   Punaiset nuolet tarkoittavat vastaanottotapahtumia, jotka täsmäytetään järjestelmän muodostamaan varasto-ottotapahtumaan.
-   Vihreä nuoli tarkoittaa vastakirjauksena toimivaa järjestelmän muodostamaa vastaanottotapahtumaa, johon alun perin kirjatut varasto-ottotapahtumat täsmäytetään

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Painotetun keskiarvon suora täsmäytys ja Sisällytä fyysinen arvo -valinta
Parametri toimii painotetun keskiarvon varastomallin yhteydessä eri tavoin kuin tuotteen aiemmissa versioissa. Valitse Sisällytä fyysinen arvo -valintaruutu nimikkeelle Nimikemalliryhmä-lomakkeesta. Järjestelmä käyttää tämän jälkeen fyysisesti päivitettyjä vastaanottoja arvioidun kustannushinnan tai käyttökeskiarvon laskemiseen. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain rahoituksellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa. On suositeltavaa, että varasto suljetaan painotetun keskiarvon varastomallia käytettäessä joka kuukausi. Tässä painotetun keskiarvon suoran täsmäytyksen esimerkissä nimikemalliryhmä on merkitty sisältämään fyysinen arvo. 

Alapuolella olevassa graafisessa esityksessä on kuvattu seuraavat tapahtumat:
-   1a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 11,00 USD.
-   1b. Varaston taloudellinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 15,00 USD.
-   3a. Fyysinen varasto-ottopäivitys, jossa määrä on 1 ja kappalehinta 12,50 Yhdysvaltain dollaria (USD) (keskimääräinen kustannus, koska fyysisen vastaanoton arvo otetaan huomioon).
-   3b. Rahoituksellinen varasto-ottopäivitys, jossa määrä on 1 ja kappalehinta 12,50 Yhdysvaltain dollaria (USD) (keskimääräinen kustannus, koska fyysisen vastaanoton arvo otetaan huomioon).
-   4. Varaston sulkeminen on suoritettu. Varaston sulkemisen aikana järjestelmä ohittaa kaikki varastotapahtumat, jotka on päivitetty vain fyysisesti. Suoran täsmäytyksen periaatetta noudatetaan sen sijaan, koska rahoituksellisia vastaanottoja on vain yksi. Siihen varastotapahtumaan kirjataan 2,50 Yhdysvaltain dollarin (USD) oikaisu, joka on otettu rahoituksellisesti varaston sulkemispäivämääränä. Varaston sulkemisen jälkeen käytettävissä olevan varaston määrä on 1 ja keskimääräinen kustannushinta 15,00 Yhdysvaltain dollaria.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja suoran täsmäytysperiaatteen vaikutusta tähän tapahtumien sarjaan, kun Sisällytä fyysinen arvo -vaihtoehto on käytössä. 

![Painotettu keskiarvo - suora maksu - fyysinen arvo sisällytetään](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Kaavion selite**
-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Hakasulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman hakasulkeita oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä Inventory Close.
-   Varaston sulkemisen suorittamat täsmäytykset on merkitty punaisilla pistenuolilla, jotka osoittavat vinosti vastaanotosta varasto-ottoon.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Painotetun keskiarvon yhteenvetotäsmäytys ja Sisällytä fyysinen arvo -valinta
Sisällytä fyysinen arvo -parametri toimii painotetun keskiarvon yhteydessä eri tavoin kuin aiemmissa versioissa. Valitse Sisällytä fyysinen arvo -valintaruutu nimikkeelle Nimikemalliryhmä-sivulta. Järjestelmä käyttää tämän jälkeen fyysisesti päivitettyjä vastaanottoja arvioidun kustannushinnan tai käyttökeskiarvon laskemiseen. Varasto-otot kirjataan kauden aikana tätä arvioitua kustannushintaa noudattaen. Varaston sulkemisen aikana vain rahoituksellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa. On suositeltavaa, että varasto suljetaan painotetun keskiarvon varastomallia käytettäessä joka kuukausi. Tässä painotetun keskiarvon yhteenvetotäsmäytyksen esimerkissä varastomalli on merkitty sisältämään fyysinen arvo. 

Seuraavat tapahtumat on havainnollistettu oheisessa kuvassa:
-   1a. Varaston fyysinen vastaanotto päivitetty määrälle 2 yksikkökustannuksen ollessa 11,00 USD.
-   1b. Varaston taloudellinen vastaanotto päivitetty määrälle 2 yksikkökustannuksen ollessa 14,00 USD.
-   2. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   3a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 12,00 USD.
-   3b. Varaston taloudellinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 16,00 USD.
-   4a. Fyysinen varasto-ottopäivitys, jossa määrä on 1 ja kappalehinta 13,50 Yhdysvaltain dollaria (USD) (keskimääräinen kustannus, koska fyysisen vastaanoton arvo otetaan huomioon).
-   4b. Rahoituksellinen varasto-ottopäivitys, jossa määrä on 1 ja kappalehinta 13,50 Yhdysvaltain dollaria (USD) (keskimääräinen kustannus, koska fyysisen vastaanoton arvo otetaan huomioon).
-   5a. Varaston fyysinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 14,00 USD.
-   5b. Varaston taloudellinen vastaanotto päivitetty määrälle 1 yksikkökustannuksen ollessa 16,00 USD.
-   6. Varaston sulkeminen on suoritettu. Varaston sulkemisen aikana järjestelmä ohittaa kaikki varastotapahtumat, jotka on päivitetty vain fyysisesti. Yhteenvetotäsmäytyksen periaatetta noudatetaan, koska rahoituksellisia vastaanottoja on vain yksi. Siihen varastotapahtumaan kirjataan 1,50 Yhdysvaltain dollarin (USD) oikaisu, joka on otettu rahoituksellisesti varaston sulkemispäivämääränä. Varaston sulkemisen jälkeen käytettävissä olevan varaston määrä on 3 ja keskimääräinen kustannushinta 15,00 Yhdysvaltain dollaria.
-   7a. "Painotetun keskiarvon varaston sulkemistapahtuman" rahoituksellinen varasto-otto muodostetaan, jotta saadaan varaston kaikkien rahoituksellisten vastaanottojen täsmäytysten yhteenveto.
-   7b. "Painotetun keskiarvon varastosulkemistapahtuman” rahoituksellinen varastovastaanotto muodostetaan kohteen 5a vastakirjaukseksi.

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun Sisällytä fyysinen arvo -vaihtoehtoa ei käytetä. 

![Painotettu keskiarvo - maksun yhteenveto - fyysinen arvo sisällytetään](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Kaavion selite**
-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Hakasulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman hakasulkeita oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten 1a. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä Inventory Close.
-   Varaston sulkemisen suorittamat täsmäytykset on merkitty punaisilla pistenuolilla, jotka osoittavat vinosti vastaanotosta varasto-ottoon.
-   Punaiset nuolet tarkoittavat vastaanottotapahtumia, jotka täsmäytetään järjestelmän muodostamaan varasto-ottotapahtumaan.
-   Vihreä nuoli tarkoittaa vastakirjauksena toimivaa järjestelmän muodostamaa vastaanottotapahtumaa, johon alun perin kirjatut varasto-ottotapahtumat täsmäytetään

## <a name="weighted-average-with-marking"></a>Painotettu keskiarvo ja merkintä
Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. 

Oletetaan esimerkiksi, että yrityksesi asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voisi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tuotteen kustannuksissa). 

Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Esimerkiksi tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjausta. Tämän jälkeen myytyjen tuotteiden kustannukset ovat 120,00 USD nimikkeen nykyisen keskimääräinen käyttökustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. 

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa. 

Varastostaottotapahtuma merkitään varastostaottotapahtumaan. Tämän jälkeen nimikkeen nimikemalliryhmälle valittu arvostusmenetelmä ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat keskenään. 

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän myyntitilausrivillä Myyntitilauksen tiedot -sivulla. Voit tarkastella avoimia vastaanottotapahtumia Merkintä-sivulla. 

Voit merkitä varastostaottotapahtuman vastaanottoon tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta. 

Alapuolella olevassa graafisessa esityksessä on kuvattu seuraavat tapahtumat:
-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Fyysinen varasto-otto, jossa määrä on 1 ja kustannushinta 21,25 Yhdysvaltain dollaria (USD) (rahoituksellisesti ja fyysisesti päivitettyjen tapahtumien keskiarvo).
-   5b. Rahoituksellinen varasto-otto, jonka määrä on 1, merkitään varastovastaanottoon 2b ennen tapahtuman kirjaamista. Tapahtuma kirjataan, ja sen kustannushinta on 20,00 Yhdysvaltain dollaria (USD).
-   6a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD.
-   7 Varasto suljetaan. Koska rahoituksellisesti päivitetty tapahtuma on merkitty aiempaan vastaanottoon, nämä tapahtumat täsmäytetään keskenään, eikä oikaisuja tehdä.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa kaaviossa havainnollistetaan painotetun keskiarvon varastomallin ja merkinnän käyttämisen vaikutus tähän tapahtumien sarjaan. 

![Painotettu keskiarvo merkinnän kanssa](./media/weightedaveragewithmarking.gif) 

**Kaavion selite**
-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Hakasulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman hakasulkeita oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä Inventory Close.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla pisteviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.






