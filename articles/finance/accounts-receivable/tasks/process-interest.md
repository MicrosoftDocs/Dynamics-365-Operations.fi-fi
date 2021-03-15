---
title: Koron käsittely
description: Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad30984f55017ee275af15ddb4f1a46c6a50db69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992936"
---
# <a name="process-interest"></a>Koron käsittely

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan. Tässä tehtävässä käytetään esittely-yritystä USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Määritä kirjausprofiilin korko.
1. Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**.
2. Valitse **Muokkaa**.
3. Valitse korkokoodi **Asetukset**-pikavälilehden **Korkokoodi**-kentästä avattavasta luettelosta. Jos et halua laskea korkoa tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi. **Taulurajoitus**-pikavälilehden avulla voit muuttaa tapaa, jolla korko käsitellään. Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille lasketaan korko.  

## <a name="calculate-interest"></a>Laske korko
1. Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Korko > Luo korkolaskut**.
2. Valitse tapahtumalajit, joille korko lasketaan. Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.  
3. Jos valitset **Korko**-kentän arvoksi Kyllä, korolle lasketaan korkoa. Tutustu koronkoron laskentaa koskeviin lakeihin, ennen kuin otat nämä tapahtumat käyttöön.  
4. Anna **Päivämäärästä**-kenttään päivämäärä, josta lähtien korko lasketaan. Jos **Päivämäärästä**-kenttään ei ole määritetty arvoa, kaikki kirjaamattomat korkolaskut peruutetaan ja korko lasketaan uudelleen tapahtuman päivämäärästä.
5. Anna **Päivämäärään**-kenttään päivämäärä, johon asti korko lasketaan.
6. **Käytettävä kirjausprofiili** -kentästä on valittava vaihtoehto. Kirjausprofiilivaihtoehtoja on kolme:
    - Tili – Käytä kunkin korkolaskun asiakastilille määritettyä kirjausprofiilia. 
    - Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.
    - Tapahtuma – Käytä yksilöllistä kirjausprofiilia tapahtumista, joissa korko lasketaan jokaiselle korkolaskulle. Ne tapahtumat, joihin ei ole määritetty kirjausprofiilia, käyttävät kirjausprofiilia, joka on määritetty Myyntireskontran parametrit -lomakkeen Kirjanpito ja arvonlisävero -alueella.  
7. Laajenna **Sisällytettävät tietueet** -pikavälilehti.
8. Valitse **Suodatin**.
9. Anna **Ehdot**-kentässä asiakkaan tunnus. Syötä arvoksi esimerkiksi US-001.
6. Valitse **OK**.
7. Valitse **OK**.

## <a name="print-interest-notes"></a>Tulosta korkolaskut
1. Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Korko > Tarkastele ja käsittele korkolaskuja**.
2. Valitse **Tila**-kentässä Luotu.
3. Valitse **Tulostettu**-kentässä Ei tulostettu.
4. Valitse **Tulosta**.
5. Laajenna **Sisällytettävät tietueet** -pikavälilehti.
6. Valitse **OK**.
7. Sulje sivu.

## <a name="post-the-interest-note"></a>Korkolaskun kirjaaminen
1. Valitse korkolasku, joka on valmis kirjattavaksi (tila on Luotu).
2. Valitse **Kirjaa**.
3. Syötä korkolaskun kirjauspäivämäärä. Valitse Kyllä, kun haluat luoda kullekin korkolaskulle kirjanpitotapahtuman. Jos et valitse Kyllä-arvoa, kaikkien asiakkaan korkolaskujen korot lasketaan yhteen ja kirjataan kirjanpitoon yhtenä tapahtumana.  
4. Laajenna **Sisällytettävät tietueet** -pikavälilehti.
5. Valitse **OK**.
6. Valitse **Tila**-kentässä Kirjattu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]