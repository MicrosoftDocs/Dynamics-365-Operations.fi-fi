---
title: Vuokrasopimuksen parametrien määrittäminen (esiversio)
description: Tässä artikkelissa kuvataan resurssin vuokrauksen asetukset. Niitä ovat esimerkiksi suojauksen tiedot ja kirjanpidon asetukset.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e878fa7634cfdcc6c0db19a91e771757c545505b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895077"
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

4. Määritä **Salli poistojen peruutukset suljetussa kirjassa** -vaihtoehdon arvoksi **Kyllä**, jos poistokulutapahtumia voi peruuttaa. Kulutapahtumat voidaan peruuttaa myös kirjan version sulkemisen jälkeen.

    > [!NOTE]
    > On suositeltavaa säilyttää tämän asetuksen arvona **Ei**. Tämän asetuksen määritystä käytetään tarkistuksessa ja ohjausobjektissa, jotta suljettua kirjan versiota ei poisteta vahingossa. Jos säilytät asetuksen arvona **Ei**, voit säilyttää nettokirjanpitoarvon ja tulevien poistojen laskelmat ajantasalla.

5. Määritä **Salli maksun summa -erittely**-asetuksen arvoksi **Kyllä**, jos haluat sallia maksusummista erittelyn **Vuokra**-sivun **Maksusuunnitelma-rivien** pikavälilehdessä. Maksuerittelytyypit määritetään **Maksusumman tyypit** -sivun **Asetukset**-kohdassa. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
