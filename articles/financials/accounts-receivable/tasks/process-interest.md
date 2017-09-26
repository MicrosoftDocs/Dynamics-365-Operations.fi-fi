--- 
title: "Koron käsittely"
description: "Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a53c4deb146d336fdd8ca88a081e6a5af71465a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="process-interest"></a>Koron käsittely

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan. Tässä tehtävässä käytetään esittely-yritystä USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Määritä kirjausprofiilin korko.
1. Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.
2. Valitse Muokkaa.
    * Valitse korkokoodi avattavasta luettelosta. Jos et halua laskea korkoa tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.  
    * Taulurajoitus-välilehden avulla voit muuttaa tapaa, jolla korko käsitellään. Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille lasketaan korko.  

## <a name="calculate-interest"></a>Laske korko
1. Siirry kohtaan Luotonvalvonta > Korko > Luo korkolaskut.
    * Valitse tapahtumalajit, joille korko lasketaan. Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.  
    * Jos valitset arvoksi Korko, korolle lasketaan korkoa. Tutustu koronkoron laskentaa koskeviin lakeihin, ennen kuin otat nämä tapahtumat käyttöön.  
    * Korko lasketaan tästä päivästä Päivämäärään-kentän arvoon asti. Jos Päivämäärästä-kenttään ei ole määritetty arvoa, kaikki kirjaamattomat korkolaskut peruutetaan ja korko lasketaan uudelleen tapahtuman päivämäärästä.  
2. Syötä korkolaskun päivämäärä.
    * Kirjausprofiilivaihtoehtoja on kolme: Tili – Käytä jokaisessa korkolaskussa asiakkaan tiliin liitettyä kirjausprofiilia.   Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.   Tapahtuma – Käytä yksilöllistä kirjausprofiilia tapahtumista, joissa korko lasketaan jokaiselle korkolaskulle. Ne tapahtumat, joihin ei ole määritetty kirjausprofiilia, käyttävät kirjausprofiilia, joka on määritetty Myyntireskontran parametrit -lomakkeen Kirjanpito ja arvonlisävero -alueella.  
    * Valitse kirjausprofiili tässä, jos muutit Käytettävä kirjausprofiili -kohdan arvoksi Valitse.  
3. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
4. Valitse Suodatin.
5. Syötä Ehdot-kenttään asiakkaan tunnus. Syötä arvoksi esimerkiksi US-001.
6. Valitse OK.
7. Valitse OK.

## <a name="print-interest-notes"></a>Tulosta korkolaskut
1. Siirry kohtaan Luotonvalvonta > Korko > Tarkastele ja käsittele korkolaskuja.
2. Valitse Tila-kentässä Luotu.
3. Valitse Tulostettu-kentässä Ei tulostettu.
4. Valitse Tulosta.
5. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
6. Valitse OK.
7. Sulje sivu.

## <a name="post-the-interest-note"></a>Korkolaskun kirjaaminen
1. Valitse korkolasku, joka on valmis kirjattavaksi (tila on Luotu).
2. Valitse Kirjaa.
3. Syötä korkolaskun kirjauspäivämäärä.
    * Valitse Kyllä, kun haluat luoda kullekin korkolaskulle kirjanpitotapahtuman.     Jos et valitse Kyllä-arvoa, kaikkien asiakkaan korkolaskujen korot lasketaan yhteen ja kirjataan kirjanpitoon yhtenä tapahtumana.  
4. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
5. Valitse OK.
6. Valitse Tila-kentässä Kirjattu.


