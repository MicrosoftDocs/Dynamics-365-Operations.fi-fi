--- 
title: Ostotilauksen luonti budjetin mukaan
description: "Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f9b82db94d98fb19c67888a1f8a35b2fe62c98fe
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>Ostotilauksen luonti budjetin mukaan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan. Tämä tallenne käyttää esittelytietojen USMF-yritystä.


## <a name="review-the-budget-control-configuration"></a>Budjetin hallinnan konfiguraation tarkistaminen
1. Valitse Budjetointi > Asetukset > Budjetin hallinta > Budjetin hallinnan konfiguraatio.
2. Valitse Käytettävissä olevat budjettivarat -välilehti.
3. Valitse Tiedostot ja kirjauskansiot -välilehti.
4. Valitse Määritä budjetin hallintasäännöt -välilehti.
5. Valitse Määritä budjettiryhmät -välilehti.
6. Sulje sivu.

## <a name="create-the-purchase-order-header"></a>Luo ostotilauksen otsikko
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Anna tai valitse arvo Toimittajatili-kentässä.
4. Laajenna Yleinen-osa.
5. Määritä Kirjauspäivä-kentässä päivämääräksi 1.1.2016.
6. Valitse OK.

## <a name="add-a-purchase-order-line"></a>Ostotilausrivin lisääminen
1. Kirjoita tai valitse arvo Hankintaluokka-kenttään.
2. Määritä Määrä-kenttään arvo 2.
3. Syötä tai valitse arvo Yksikkö-kenttään.
4. Aseta yksikköhinnaksi 10 000.
5. Valitse Myyntitiedot.
6. Valitse Jaa summat.
7. Määritä Kirjanpitotili-kentässä haluamasi arvo 601300-001-023--.
8. Sulje sivu.

## <a name="perform-budget-checking"></a>Tarkista budjetti
1. Valitse Myyntitiedot.
2. Valitse Tarkista budjetti.
3. Valitse Myyntitiedot.
4. Valitse Budjetin tarkistusvirheet tai -varoitukset.
5. Valitse Sulje.


