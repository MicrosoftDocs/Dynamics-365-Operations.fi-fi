---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29c13e729223a98d7f45244c5a796bca6e3baaf3
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550830"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

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

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Hae Microsoftin toimittamat myyntilaskumallin konfiguraatiot
1. Valitse Näytä suodattimet.
2. Käytä seuraavia suodattimia: anna suodattimeksi "Operatiivisen resurssit" Nimi-kenttään ja käytä "alkaa"-suodatinoperaattoria; kirjoita suodatinarvoksi "" Kuvaus-kenttään ja käytä "alkaa"-suodatinoperaattoria.
3. Valitse Näytä suodattimet.
4. Valitse Avaa.
5. Valitse puussa solmu "Customer invoice model".
    * Valitse tuotavaksi mallikonfiguraatio "Myyntilaskumalli".  
6. Valitse Tuo.
    * Valitse Tuo valitulle kokoonpanoversiolle 1  
7. Valitse Kyllä.
8. Sulje sivu.
9. Sulje sivu.
10. Valitse Raportointikonfiguraatiot.
11. Valitse puussa solmu "Customer invoice model".

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Luo johdettu malli, joka tukee tiedostonhallinnan tiedostojen käyttämistä.
    * Luot oman myyntilaskumallin konfiguraation johtamalla sen Microsoftin tarjoamasta konfiguraatiosta. Tätä konfiguraatiota käytetään tiedostonhallinnan käytön toteuttamiseen ja tiedostojen saattamiseen tällä mallilla luotavien sähköisten asiakirjojen käyttöön.  
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Kirjoita Uusi-kenttään "Derive from Name: Customer invoice model, Microsoft".
3. Syötä Nimi-kenttään "Customer invoice model (custom)".
    * Myyntilaskumalli (mukautettu)  
4. Valitse Luo konfiguraatio.

