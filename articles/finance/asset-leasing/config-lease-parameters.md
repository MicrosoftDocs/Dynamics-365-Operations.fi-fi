---
title: Vuokrasopimuksen parametrien määrittäminen (esiversio)
description: Tässä ohjeaiheessa kuvataan resurssin vuokrauksen asetukset. Niitä ovat esimerkiksi suojauksen tiedot ja kirjanpidon asetukset.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442970"
---
# <a name="configure-lease-parameters"></a>Vuokrasopimuksen parametrien määrittäminen

[!include [banner](../includes/banner.md)]

Useat määritysasetukset vaikuttavat siihen, miten resurssin vuokraus toimii. Näitä asetuksia ovat esimerkiksi kirjauskansioiden nimet, yleiset parametrit ja kirjausprofiilin asetukset.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.
2. Valitse **Vuokrasopimukset**-välilehdessä **Yleistiedot**-pikavälilehti.

    **Salli manuaalisen luokituksen ohitus** -parametri määrittää, voidaanko vuokrauksen luokitus ohittaa, ennen kuin maksuaikataulu on vahvistettu.

    **Yksiköiden välinen erä** -parametri määrittää, voitko kirjata muita yrityksiä nykyisestä yrityksestä. Jos tämä parametri on käytössä, voit luoda sille yritykselle kirjauskansiovientejä, jonka käyttöoikeus sinulla on.

3. Määritä **Salli vahvistettujen vuokrasopimusten poistaminen** -vaihtoehdon arvoksi **Kyllä**, jos haluat sallia vahvistetut maksuaikataulut omaavien vuokrasopimusten poistamisen. Vuokrasopimuksia ei voi poistaa, jos niihin liittyy kirjattuja tai kirjaamattomia tapahtumia tämän asetuksen määrityksestä huolimatta. Et voi palauttaa vuokrasopimuksen tietuetta sen poistamisen jälkeen. Jos lataat kaikki poistetun vuokrasopimuksen tietueet joko manuaalisesti tai tietoentiteettien kautta, ladattuja tietoja käsitellään uusina, ei aiemmin luodun vuokrasopimuksen päivityksinä.

    Jos määrität tämän asetuksen arvoksi **Kyllä** ja kirjan siirtymätyyppi on **Kumulatiivinen päivitysvaihto A tai B**, järjestelmä määrittää **Inkrementaalinen lainakorko** -kentän arvoksi **Inkrementaalinen lainakorko siirtymässä** -kentän arvon **Kirjan asetukset** -sivulla. Jos tämän asetuksen arvoksi on määritetty **Ei**, päävuokrasopimuksen määräksi annetaan **Inkrementaalinen lainakorko** -kentän arvo **Kirjan tiedot** -sivulla riippumatta kirjan siirtymätyypistä.

4. Määritä **Salli poistojen peruutukset suljetun kirjan versiossa** -vaihtoehdon arvoksi **Kyllä**, jos poistokulutapahtumia voi peruuttaa. Kulutapahtumat voidaan peruuttaa myös kirjan version sulkemisen jälkeen.

    > [!NOTE]
    > On suositeltavaa säilyttää tämän asetuksen arvona **Ei**. Tämän asetuksen määritystä käytetään tarkistuksessa ja ohjausobjektissa, jotta suljettua kirjan versiota ei poisteta vahingossa. Jos säilytät asetuksen arvona **Ei**, voit säilyttää nettokirjanpitoarvon ja tulevien poistojen laskelmat ajantasalla.
