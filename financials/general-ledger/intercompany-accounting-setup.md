---
title: "Konserniyritysten välisen laskennan asetuksista"
description: "Tässä ohjeaiheessa kerrotaan, kuinka konserniyritysten välisen laskennan määrittäminen niin, että voit käyttää Konsernin päiväkirjojen kirjanpidon kohdistuksissa ja taloushallinnon päiväkirjoissa, esimerkiksi päivittäisten kirjauskansioiden, toimittajan laskun Ostopäiväkirjat ja Maksupäiväkirjat."
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
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Konserniyritysten välisen laskennan asetuksista

Tässä ohjeaiheessa kerrotaan, kuinka konserniyritysten välisen laskennan määrittäminen niin, että voit käyttää Konsernin päiväkirjojen kirjanpidon kohdistuksissa ja taloushallinnon päiväkirjoissa, esimerkiksi päivittäisten kirjauskansioiden, toimittajan laskun Ostopäiväkirjat ja Maksupäiväkirjat.

Konsernin päiväkirjojen voidaan luoda eri tilanteissa, kuten päivittäisten kirjauskansioiden, toimittajan laskujen kirjauskansioiden, kirjanpidon kohdistuksissa ja keskitettyjä maksuja varten. Mahdollistaaksesi nämä skenaariot, perusta konsernikirjanpito.

## <a name="define-main-accounts"></a>Määritä päätilit
Ensin on luotava kirjanpidon merkinnöistä konsernin ensisijaisesti käytettävät tilit maksettavien ja saatavien eräpäiville. On hyvä idea käyttää yksilöllisiä päätilejä kullekin yritykselle, helpottamaan täsmäyttämistä ja konsernin sisäisten kirjauksien eliminointia. Jos käytät kauppakumppanin tai vastaava dimensio, konsernin osapuolten tunnistamiseen, voit määrittää tämän dimension päätilille, joka on määritetty konserniyritysten välisen laskennan kiinteä dimensiona. Kun määrität päätilit, ne tulisi asettaa **Main tyyppi** kentän arvoksi **taseen** - **tärkeimmät asiakkaat** sivun.

## <a name="define-journal-names"></a>Määritä kirjauskansioiden nimet
Seuraavaksi on määritettävä kirjauskansion nimi. Määrittää **tyyppi** kentän arvoksi **päivittäin** - **kirjauskansioiden nimet** sivulla. On suositeltavaa käyttää konsernin sisäiseen laskutukseen tiettyä kirjauskansion nimeä.

## <a name="define-intercompany-accounting-setup"></a>Määritä konserniyritysten välisen laskennan asetuksista
**Konserniyritysten välisen laskennan** sivun luomisessa käytettävä oikeussubjektit, jotka voidaan transact parien toistensa kanssa. Konsernin laskenta-asetukset on jaettu, joten asetukset on näkyvissä kaikki oikeushenkilöt. Luotaessa uusi yritys parin, varmista, että olet tietoinen alkuperäisen yrityksen tai kohdeyrityksen määritellään mitkä oikeushenkilö. Kun määrität konserniyritysten välisiä tapahtumia, tapahtuman määrittää mitä oikeushenkilön aloittamisen tai tapahtuma on peräisin. Esimerkiksi yritysten joukossa on määritetty USSI (kohde) ja USMF (peräisin). Jos käyttäjä on aktiivinen USSI ja siirtyy konsernin tapahtuma, jossa USMF, tapahtumaa ei kirjaa konserniyritysten välisen laskennan määritellään vain USMF koska aloittaja on. Jos joko yritys voi peräisin tapahtuma, tarvitset toisen oikeushenkilön pari vastavuoroinen asetusten luomiseen. 

Valitse **veloittaa tililtä (maksaja)** ja **kredit-tili (vastaanottaja)** sekä ja Kohdevaraston oikeushenkilölle. Määritellä, millä **Kirjauskansionimi** käytetään, kun tapahtuma luodaan kohdeyrityksessä. Alkuperäisen yrityksen kirjauskansio on jo tiedossa, koska se on valittu käyttäjä konserniyritysten välisen tapahtuman luomisessa. 

Valitse lopuksi mitä oikeushenkilön saavat kirjanpidollinen tukeminen summia, kuten käteisalennuksen tai realisoituneet voitot/tappiot keskitettyjä maksuja varten. 

Vastavuoroinen suhde voit helposti voi määrittää **konserniyritysten välisen laskennan** sivua käyttämällä **Luo vastavuoroinen suhde** -painiketta sen jälkeen, kun ensimmäinen pari oikeushenkilö on luotu. Kun luodaan vastavuoroinen pari, kohdeyrityksen tiedot kopioidaan alkuperäisen yrityksen ja päinvastoin. Kohdeyrityksen määritetty kirjauskansion säilyy. Useimmissa organisaatioissa käyttää samaa nimeämiskäytäntöä kirjauskansioiden nimet, kirjauskansionnimi on sama. Jos kirjauskansionnimi on eri, Varoitus ilmestyy ilmoitus, joka voidaan valita eri päiväkirjan ja päiväkirja ei ole kenttää.


