--- 
title: "Käsittele maksukehotuksia"
description: "Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Käsittele maksukehotuksia

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan. Tässä tehtävässä käytetään esittely-yritystä USMF.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Määritä maksukehotusjärjestys kirjausprofiilissa
1. Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.
2. Valitse Muokkaa.
    * Valitse maksukehotussarja avattavasta luettelosta. Jos et halua luoda maksukehotuksia tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.  
    * Voit muuttaa Taulurajoitus-välilehdessä tapaa, jolla maksukehotuksia käsitellään. Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille luodaan maksukehotus.  
3. Sulje sivu.

## <a name="create-collection-letters"></a>Luo maksukehotukset
1. Siirry kohtaan Luotonvalvonta > Maksukehotus > Luo maksukehotukset.
    * Valitse tapahtumatyypit, joissa käytetään maksukehotuksia. Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.  
2. Valitse asetus Maksukehotus-kentästä.
3. Anna maksukehotuksen päiväys.
    * Kirjausprofiilivaihtoehtoja on kaksi: Tili – käytä jokaisessa korkolaskussa asiakkaan tiliin liitettyä kirjausprofiilia.   Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.  
    * Valitse kirjausprofiili, jos muutit Käytettävä kirjausprofiili -asetukseksi Valitse.  
4. Laajenna Tietueet-kohta ja sisällytä osaan.
5. Valitse Suodatin.
6. Anna Ehdot-kentässä asiakastunnus. Syötä arvoksi esimerkiksi US-001.
7. Valitse OK.
8. Valitse OK.

## <a name="print-collection-letters"></a>Tulostaa maksukehotukset
1. Valitse Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia.
2. Valitse Tila-kentässä Luotu.
3. Valitse Tulostettu-kentässä Ei tulostettu.
4. Valitse Tulosta.
5. Valitse Maksukehotus.
6. Laajenna Tietueet-kohta ja sisällytä osaan.
7. Anna kirjausten katkaisupäivämäärä
8. Tulosta maksukehotus valitsemalla OK.

## <a name="post-the-collection-letter"></a>Kirjaa maksukehotus
1. Valitse Kirjaa.
2. Anna maksukehotuksen kirjauspäivämäärä.
3. Laajenna Tietueet-kohta ja sisällytä osaan.
4. Valitse OK.
5. Valitse Tila-kentässä Kirjattu.
6. Valitse vaihtoehto Tulostettu-kentässä.


