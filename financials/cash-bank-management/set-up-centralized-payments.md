---
title: "Keskitettyjen maksujen määrittäminen"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Keskitettyjen maksujen määrittäminen



Valmistella voit käsitellä maksuja yhden oikeushenkilön organisaation muiden oikeushenkilöiden puolesta seuraavasti. Ennen kuin aloitat, on täytettävä seuraavat asetukset:

-   Luo oikeushenkilöt.
-   Määritä kirjanpitoparametrit ja tilikartat.
-   Määritä ostoreskontran ja myyntireskontran parametrit (keskitettyjen maksujen moduulien mukaan).
-   Määritä konsernin sisäinen laskenta.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Keskitettyjen maksujen organisaatiohierarkian määrittäminen
Määritä keskitettyjen maksujen organisaatiohierarkia. Samaa organisaatiohierarkiaa käytetään sekä toimittajien että asiakkaiden keskitetyissä maksuissa. **Huomautus:** Hierarkian rakenteella ei ole merkitystä keskitettyjen maksujen käsittelyssä. Mikä tahansa hierarkian yritys voi käsitellä maksuja hierarkian toisten yritysten puolesta. Voit luoda uuden organisaatiorakenteen **Organisaatiohierarkiat**-sivulla.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Keskitettyjen maksujen konsernitilin määrittäminen
Kun nykyisen yrityksen maksutapahtumat selvitetään muiden yritysten laskuja vastaan, jokaiselle yritykselle luodaan asianmukaiset erääntymiskohteen ja -lähteen tapahtumat. Määritä yritys, johon sovellettavissa olevat käteisalennukset ja realisoituneet voitto- tai tappiosummat kirjataan. Ennen kuin aloitat, päätä, mitä yritystä toimittajan ja asiakkaan maksujen käsittelyssä käytetään. Jos yksi yritys käsittelee toimittajan maksut ja toinen asiakkaan maksut, sinun on siirryttävä yritysten välillä. - **Konserniyritysten välisen laskennan** -sivulla voit valita konsernin sisäisen suhteen tietue oikeushenkilölle, jonka puolesta maksut on tarkoitus käsitellä. - **Keskitetty maksujen** -välilehdestä voit valita, käytetäänkö rahaa kirjaa alennukset maksutapahtuman (tai muun toimittajatilin saldoa suurentavan tapahtuman), yritys tai oikeushenkilö lasku (tai muun sellaisen tapahtuman, joka lisää toimittajatilin saldon). Tämä valinta toimii yhdessä **Käteisalennuksen hallinta**- ja **Ostoreskontran parametrit** -sivun **Käteisalennuksen hallinta** -kentän kanssa. Liikamaksuissa ja pyöristyseroissa käytetään maksutapahtuman yrityksen asetuksia. Liian pienissä maksuissa sekä pyöristyseroissa käytetään laskun yrityksen asetuksia.

## <a name="map-vendor-accounts-across-legal-entities"></a>Eri yritysten toimittajatilien yhdistäminen
Jos suoritat toimittajalle maksun yhdestä yrityksestä ja haluat valita kyseisen toimittajan laskuja muista yrityksistä, varmista, että kunkin yrityksen kaikki vastaavat toimittajatilit käyttävät samaa osoitekirjan tunnusta. Jos vastaanotat maksun asiakkaalta, joka maksaa laskut useaan yritykseen, sinun on varmistettava, että kaikki vastaavat asiakastilit käyttävät samaa osoitekirjatunnusta jokaisessa yrityksessä.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Keskitettyjen maksujen kirjausprofiilien määrittäminen
Kun luot yhdelle yritykselle maksun, joka selvittää muiden yritysten laskut, kummallakin yrityksellä tulee olla sama kirjausprofiilin tunnus. Voit varmistaa, että maksut luodaan oikein, määrittämällä jokaiselle laskun yritykselle kirjausprofiilin, joka vastaa maksun yrityksen kirjausprofiileja. Ensimmäinen yritys laskun, ja valitse sitten Siirry **toimittajan kirjausprofiilit** sivun, voit luoda uuden kirjausprofiilin tai muokata aiemmin määritettyä kirjausprofiilia. Jotka teet laskun oikeushenkilön kirjausprofiilin valintojen ei tarvitse vastata toisiaan maksun oikeushenkilö kirjausprofiilin asetuksista.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Keskitettyjen maksujen maksutapojen määrittäminen
Kun luot yhdelle yritykselle maksun, joka selvittää muiden yritysten laskut, kummallakin yrityksellä tulee olla sama maksutapa. Voit varmistaa, että maksut luodaan oikein, määrittämällä jokaiselle laskun yritykselle maksutavan, joka vastaa maksun yrityksen maksutapoja. Siirry laskun ensimmäiseen yritykseen ja luo sitten uusi maksutapa **Maksutavat**-sivulla tai muokkaa aiemmin luotua maksutapaa. Laskun yrityksen maksutavan valintojen ei tarvitse vastata maksun yrityksen maksutavan asetuksia.

## <a name="set-up-default-descriptions"></a>Oletuskuvausten määrittäminen
Voit määrittää yritystenvälisten selvitystositteiden oletuskuvaukset. Tämä oletuskuvaus sisällytetään erääntymiskohteen ja erääntymislähteen tapahtumiin yritystenvälisen selvitysprosessin aikana. **Oletuskuvaukset**-sivulla voit luoda uudet kuvaukset sekä **konserniasiakkaan tilitykselle **että **konsernitoimittajan tilitykselle** valitsemalla kielen ja syöttämällä sitten tekstin.


