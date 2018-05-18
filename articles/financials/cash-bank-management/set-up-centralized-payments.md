---
title: "Keskitettyjen maksujen määrittäminen"
description: "Näiden ohjeiden avulla voit valmistella yhden yrityksen maksujen käsittelyn organisaation muiden yritysten puolesta."
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2e309655bbc1d0fe7a088062b90fab34c642ab29
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-centralized-payments"></a>Keskitettyjen maksujen määrittäminen

[!include [banner](../includes/banner.md)]

Näiden ohjeiden avulla voit valmistella yhden yrityksen maksujen käsittelyn organisaation muiden yritysten puolesta. Ennen kuin voit aloittaa, varmista, että seuraavat määritykset on tehty:

-   Luo oikeushenkilöt.
-   Määritä kirjanpitoparametrit ja tilikartat.
-   Määritä ostoreskontran ja myyntireskontran parametrit (keskitettyjen maksujen moduulien mukaan).
-   Määritä konsernin sisäinen laskenta.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Keskitettyjen maksujen organisaatiohierarkian määrittäminen
Määritä keskitettyjen maksujen organisaatiohierarkia. Samaa organisaatiohierarkiaa käytetään sekä toimittajien että asiakkaiden keskitetyissä maksuissa. **Huomautus:** Hierarkian rakenteella ei ole merkitystä keskitettyjen maksujen käsittelyssä. Mikä tahansa hierarkian yritys voi käsitellä maksuja hierarkian toisten yritysten puolesta. Voit luoda uuden organisaatiorakenteen **Organisaatiohierarkiat**-sivulla. Valitse **Tarkoitus**-kenttään **Keskitetyt maksut**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Keskitettyjen maksujen konsernitilin määrittäminen
Kun nykyisen yrityksen maksutapahtumat selvitetään muiden yritysten laskuja vastaan, jokaiselle yritykselle luodaan asianmukaiset erääntymiskohteen ja -lähteen tapahtumat. Määritä yritys, johon sovellettavissa olevat käteisalennukset ja realisoituneet voitto- tai tappiosummat kirjataan. Ennen kuin aloitat, päätä, mitä yritystä toimittajan ja asiakkaan maksujen käsittelyssä käytetään. Jos yksi yritys käsittelee toimittajan maksut ja toinen asiakkaan maksut, sinun on siirryttävä yritysten välillä. Valitse **Konsernin sisäinen laskenta** -sivulla sen yrityksen konsernin sisäisen suhteen tietue, jonka puolesta käsittelet maksut. 

**Keskitetyt maksut** -välilehdessä voit määrittää, kirjataanko käteisalennukset maksutapahtuman (tai muun toimittajatilin saldoa pienentävän tapahtuman) yritykseen vai laskutapahtuman (tai muun toimittajatilin saldoa suurentavan tapahtuman) yritykseen. Tämä valinta toimii yhdessä **Käteisalennuksen hallinta**- ja **Ostoreskontran parametrit** -sivun **Käteisalennuksen hallinta** -kentän kanssa. Liikamaksuissa ja pyöristyseroissa käytetään maksutapahtuman yrityksen asetuksia. Liian pienissä maksuissa sekä pyöristyseroissa käytetään laskun yrityksen asetuksia.

## <a name="map-vendor-accounts-across-legal-entities"></a>Eri yritysten toimittajatilien yhdistäminen
Jos suoritat toimittajalle maksun yhdestä yrityksestä ja haluat valita kyseisen toimittajan laskuja muista yrityksistä, varmista, että kunkin yrityksen kaikki vastaavat toimittajatilit käyttävät samaa osoitekirjan tunnusta. Jos vastaanotat maksun asiakkaalta, joka maksaa laskut useaan yritykseen, sinun on varmistettava, että kaikki vastaavat asiakastilit käyttävät samaa osoitekirjatunnusta jokaisessa yrityksessä.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Keskitettyjen maksujen kirjausprofiilien määrittäminen
Kun luot yhdelle yritykselle maksun, joka selvittää muiden yritysten laskut, kummallakin yrityksellä tulee olla sama kirjausprofiilin tunnus. Voit varmistaa, että maksut luodaan oikein, määrittämällä jokaiselle laskun yritykselle kirjausprofiilin, joka vastaa maksun yrityksen kirjausprofiileja. Siirry laskun ensimmäiseen yritykseen ja luo sitten uusi kirjausprofiili **Toimittajan kirjausprofiilit** -sivulla tai muokkaa aiemmin luotua kirjausprofiilia. Laskun yrityksen kirjausprofiilin valintojen ei tarvitse vastata maksun yrityksen kirjausprofiilin asetuksia.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Keskitettyjen maksujen maksutapojen määrittäminen
Kun luot yhdelle yritykselle maksun, joka selvittää muiden yritysten laskut, kummallakin yrityksellä tulee olla sama maksutapa. Voit varmistaa, että maksut luodaan oikein, määrittämällä jokaiselle laskun yritykselle maksutavan, joka vastaa maksun yrityksen maksutapoja. Siirry laskun ensimmäiseen yritykseen ja luo sitten uusi maksutapa **Maksutavat**-sivulla tai muokkaa aiemmin luotua maksutapaa. Laskun yrityksen maksutavan valintojen ei tarvitse vastata maksun yrityksen maksutavan asetuksia.

## <a name="set-up-default-descriptions"></a>Oletuskuvausten määrittäminen
Voit määrittää yritystenvälisten selvitystositteiden oletuskuvaukset. Tämä oletuskuvaus sisällytetään erääntymiskohteen ja erääntymislähteen tapahtumiin yritystenvälisen selvitysprosessin aikana. **Oletuskuvaukset**-sivulla voit luoda uudet kuvaukset sekä **konserniasiakkaan tilitykselle** että **konsernitoimittajan tilitykselle** valitsemalla kielen ja syöttämällä sitten tekstin.




