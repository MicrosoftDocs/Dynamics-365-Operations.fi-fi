--- 
title: "Koron käsittely"
description: "Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a>Koron käsittely

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


