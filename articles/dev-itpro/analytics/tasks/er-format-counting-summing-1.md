---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f925ef8d772189a505f2793de1176756866bf4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362254"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1-create-format"></a>ER Määritä muoto suorittamaan laskenta ja summaus (osa 1: muodon luominen)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Saat luettelon Microsoftin tarjoamista kokoonpanoista
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, että Litware, Inc. -lähde on käytettävissä ja merkitty aktiiviseksi.  
2. Valitse Litware, Inc. -tarjoaja.
3. Valitse Säilöt.
    * Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.  
4. Avaa valintaikkuna valitsemalla Lisää.
5. Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.
6. Valitse Luo säilö.
7. Valitse OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Hae Microsoftin Intrastat-kokoonpanot
1. Valitse Avaa.
2. Valitse puusta "Intrastat model\Intrastat (DE)"
3. Valitse Tuo.
    * Valitse Tuo valitulle kokoonpanoversiolle 1.1  
4. Valitse Kyllä.
5. Sulje sivu.
6. Sulje sivu.
7. Valitse Raportointikonfiguraatiot.
8. Laajenna puussa solmu "Intrastat model".
9. Valitse puusta "Intrastat model\Intrastat (DE)"

