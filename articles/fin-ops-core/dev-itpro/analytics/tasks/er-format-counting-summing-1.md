---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)
description: Tässä artikkelissa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 1)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable
ms.openlocfilehash: b9e0128e55ba6ab356d6942020a34e5e74d6b7e2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290691"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
