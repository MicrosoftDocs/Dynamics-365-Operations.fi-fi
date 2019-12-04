---
title: ER Lataa kokoonpano Lifecycle Services -palveluun
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 980ce00ae702ea0a3394efa15419e0f7b7dc2530
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182206"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a>ER Lataa kokoonpano Lifecycle Services -palveluun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS).

Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. ja ladataan sen LCS-palveluun. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot. Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista. Näiden vaiheiden suorittamiseen tarvitaan myös LCS:n käyttöoikeudet.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Litware, inc. ja määritä aktiiviseksi.
3. Valitse Konfiguraatiot.

## <a name="create-a-new-data-model-configuration"></a>Uuden tietomallin konfiguraation luominen
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
    * Luodaan konfiguraatio, joka sisältää tietomalliesimerkin sähköisiä asiakirjoja varten. Tämä tietomallin konfiguraatio ladataan LCS:ään myöhemmin.  
2. Syötä Nimi-kenttään Mallikonfiguraation esimerkki.
    * Mallikonfiguraation esimerkki  
3. Syötä Kuvaus-kenttään Mallikonfiguraation esimerkki.
    * Mallikonfiguraation esimerkki  
4. Valitse Luo konfiguraatio.
5. Valitse Mallin suunnittelu.
6. Valitse Uusi.
7. Syötä Nimi-kenttään Tulopaikka.
    * Tulopaikka  
8. ValitseLisää.
9. Valitse Tallenna.
10. Sulje sivu.
11. Voit muuttaa tilaa valitsemalla Muuta.
12. Valitse Valmis.
13. Valitse OK.

## <a name="register-a-new--repository"></a>Rekisteröi uusi säilö
1. Sulje sivu.
2. Valitse Säilöt.
    * Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.  
3. Avaa valintaikkuna valitsemalla Lisää.
    * Näin voit lisätä uuden säilön.  
4. Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi LCS.
5. Valitse Luo säilö.
6. Anna tai valitse Projekti-kentässä arvo.
    * Valitse haluamasi LCS-projekti. Sinulla on oltava käyttöoikeus projektiin.  
7. Valitse OK.
    * Luo uusi säilön merkintä.  
8. Merkitse valittu rivi luettelossa.
    * Valitse LCS-säilön tietue.  
    * Huomaa, että rekisteröity säilö on nykyisen lähteen merkitsemä, eli ainoastaan kyseisen lähteen omistamia konfiguraatioita voidaan sijoittaa tähän säilöön ja sen mukaisesti ladata valittuun LCS-projektiin.  
9. Valitse Avaa.
    * Avaa säilö, jotta voit tarkastella ER-konfiguraatioiden luetteloa. Se on tyhjä, jos projektia ei ole vielä käytetty ER-konfiguraatioiden jakamiseen.  
10. Sulje sivu.
11. Sulje sivu.

## <a name="upload-configuration-into-lcs"></a>Lataa konfiguraatio LCS:ään
1. Valitse Konfiguraatiot.
2. Valitse puussa solmu Mallikonfiguraation esimerkki.
    * Valitse luotu konfiguraatio, joka on jo valmis.  
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse kyseisen konfiguraation versio, joka "Valmis"-tilassa.  
4. Voit muuttaa tilaa valitsemalla Muuta.
5. Valitse Jaa.
    * Konfiguraation tila muutetaan valmiista jaetuksi, kun se julkaistaan LCS:ssä.  
6. Valitse OK.
7. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse konfiguraation versio, jonka tila on "Jaettu".  
    * Huomaa, että valitun version on tila on muuttunut valmiista jaetuksi.  
8. Sulje sivu.
9. Valitse Säilöt.
    * Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.  
10. Valitse Avaa.
    * Valitse LCS-säilö ja avaa se.  
    * Huomaa, että valittu konfiguraatio näytetään resurssina valitussa LCS-projektissa.  
    * Avaa LCS käyttämällä https://lcs.dynamics.com. Avaa aiemmin säilön rekisteröintiin käytetty projekti ja avaa projektin "Omaisuuskirjasto" ja laajenna GER-konfiguraatio -omaisuustyypin sisältö – ladattu ER-konfiguraatio on käytettävissä täällä. Huomaa, että ladattu LCS-konfiguraatio voidaan tuoda toiseen esiintymään, jos tarjoajilla on käyttöoikeus tähän LCS-projektiin.  
