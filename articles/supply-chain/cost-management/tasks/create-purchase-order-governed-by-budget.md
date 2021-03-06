---
title: Ostotilauksen luonti budjetin mukaan
description: Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821366"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Ostotilauksen luonti budjetin mukaan

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]