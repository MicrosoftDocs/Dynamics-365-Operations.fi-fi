---
title: Varaston erä- ja sarjavaraushierarkioiden vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun käytetään varaushierarkioita, jotka käyttävät erä- tai sarjadimensioita.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022543"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Varaston erä- ja sarjavaraushierarkioiden vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun käytetään varaushierarkioita, jotka käyttävät erä- tai sarjadimensioita.

Lisätietoja on kohdassa [Joustava varastotason dimensioiden varauskäytäntö](flexible-warehouse-level-dimension-reservation.md).

Nimikkeen varaushierarkia määrittää tarpeen varastodimensioille, jotka on täytettävä, jotta sijainti voidaan liittää kysyntätilaukseen. Näitä dimensioita voidaan kuvata *sijainnin yläpuolella oleviksi dimensioiksi* kaikille niille dimensioille, jotka on täytettävä ennen sijainnin määrittämistä, ja *dimensioiksi sijainnin alapuolella* niille dimensioille, jotka voidaan kohdistaa sen jälkeen, kun sijainti on liitetty kysyntätilaukseen. Näitä varaushierarkioita kutsutaan myös *erä-yllä*- ja *erä-alla*-varaushierarkioiksi tai *sarja-yllä*- ja *sarja-alla*-varaushierarkioiksi.

Varasto voidaan kohdistaa onnistuneesti vain, jos sijainnin yläpuolella olevissa dimensioissa ei ole aukkoja. Esimerkiksi *erä-yllä*-varaushierarkiassa odotat, että **Toimipaikka**-, **Varasto**- ja **Eränumero**-dimensiot määritetään kysyntätilauksessa. Jos jokin näistä dimensioista puuttuu, kohdistusprosessi epäonnistuu. Sen sijaan alla *erä-alla* tai *sarja-alla*-varaushierarkiassa erä- tai sarjanumero voidaan määrittää kysyntätilauksessa, mutta kohdistusprosessi ei edellytä sitä.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Seuraava virhesanoma avautuu: Jotta kuormituksen rivit voidaan määrittää aaltoon, niiden on määritettävä dimensiot sijainnin yläpuolelle. Voit määrittää nämä dimensiot varaamalla kuormituksen rivin ja luomalla sen uudelleen.

### <a name="issue-description"></a>Ongelman kuvaus

Jos käytät nimikettä, jossa käytetään *erä-yllä*-varaushierarkiaa osittaisen määrän **Kuormasuunnittelun työtila** -sivun **Vapauta varastoon** -komento ei toimi, jos yrität vapauttaa kuorman. Sait tämän virhesanoma eikä osittaiselle määrälle luoda yhtään työtä.

Jos käytät kuitenkin nimikettä, jossa käytetään *erä-alla*-varaushierarkiaa, voit vapauttaa kuorman osittaisen määrän **Kuormasuunnittelun työtila** -sivulta.

### <a name="issue-cause"></a>Ongelman syy

Jos dimensio on **Sijainti**-dimension yläpuolella varaushierarkiassa, se on määritettävä ennen vapautusta varastoon. Osittaisia määriä ei voi vapauttaa, jos vähintään yhtä **Sijainti**-dimension yläpuolella olevaa dimensiota ei ole määritetty.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Eränumeron automaattinen varauskehote käynnistyy, vaikka varastoa on käytettävissä.

### <a name="issue-description"></a>Ongelman kuvaus

Kun käytät nimikettä, jolla on *erä-yllä*-varaushierarkia varastossa, joka ei ole ottanut fyysisen varastoinnin prosesseja käyttöön, ja automaattinen varaus on käytössä, eränumeron automaattinen varauskehote tulee näyttöön, vaikka keräilyyn olisi käytettävissä vain yksi erä.

Kun käytät samaa nimikettä varastossa, jossa fyysisen varastoinnin prosessit ovat käytössä, automaattista varauskehotetta ei näytetä.

### <a name="issue-cause"></a>Ongelman syy

Jos varaushierarkiaksi on määritetty *erä-yllä* tai *sarja-yllä*, viitattu dimensio (**Eränumero** tai **Sarjanumero**) on aina määritettävä kysyntätilauksissa. Fyysisen varastoinnin prosessit voivat ehkä täydentää tietoja, jos käytettävissä on yksi erä- tai sarjanumero. Koska varastolle ei kuitenkaan ole otettu käyttöön fyysisen varastoinnin prosesseja, käyttäjän on aina määritettävä kaikki **Sijainti**-kentän yläpuolella olevat dimensiot.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Paikannusmallit, joilla on Ota huomioon käytettävissä oleva varasto -paikkaehto, eivät ota huomioon nykyistä käytettävissä olevaa varastoa nimikkeille, joille erä on otettu käyttöön.

Lisätietoja on kohdassa [Varastopaikoitus](warehouse-slotting.md).

### <a name="issue-description"></a>Ongelman kuvaus

Paikannusmallit, joilla on *Ota huomioon käytettävissä oleva varasto* -paikkaehto, eivät ota huomioon nykyistä käytettävissä olevaa varastoa *erä-yllä*-nimikkeille. Ne ottavat se huomioon vain, jos eränumero on määritetty myyntitilausrivillä.

Kun käytät alla *erä-alla*-nimikkeitä, nykyistä käytettävissä olevaa varastoa pidetään oletettuna.

### <a name="issue-cause"></a>Ongelman syy

Paikannusmallin otsikko voidaan määrittää *Tilattu*-, *Varattu*- tai *Vapautettu*-kysyntästrategialle. *Tilattu*-kysyntästrategiassa käytetään samoja varaushierarkian vaatimuksia, jotka koskevat varauksen tai varastoon vapautuksen prosesseja. Siksi erä- tai sarjanumero on määritettävä kysyntätilaukseen (myynti- tai siirtotilaus) niiden nimikkeiden osalta, joissa on *erä-yllä*- tai *erä-alla*-varaushierarkia. Vaihtoehtoisesti *Varattu*-kysyntästrategian avulla voidaan valita erä- tai sarjanumero, ennen kuin varaston paikannustarve luodaan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
