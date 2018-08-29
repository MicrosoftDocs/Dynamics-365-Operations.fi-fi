--- 
title: "Valmistele tietomalleja käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a>Valmistele tietomalleja käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


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


