---
title: Luo ostotilaus kertatoimittajalle
description: Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a55cd8f21b99589a44f7509123d3417fd9dc07f6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147431"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Luo ostotilaus kertatoimittajalle

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle. Toimittaja luodaan automaattisesti ostotilauksen yhteydessä, sen sijaan, että toimittajatili pitäisi luoda manuaalisesti. Ostotilaukset luo yleensä ostoedustaja. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Luomisen edellytys on, että kertatoimittajan tili on määritetty Ostoreskontran parametrit -sivulla.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Luo ostotilaus kertatoimittajalle
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Valitse Kertatoimittaja-kentän arvoksi Kyllä.
    * Ostotilaukselle luodaan ja määritetään automaattisesti toimittajatili. Toimittajatili luodaan Ostoreskontran parametrit -sivun Yleiset-välilehdellä määritetyn mallin mukaisesti.  
4. Kirjoita Nimi-kenttään toimittajan yksilöivä nimi.
5. Valitse OK.
    * Ostotilauksen nyt viedä loppuun ja käsitellä kuin minkä tahansa tilauksen. Tämän suorittamisessa ei ole mitään erityisominaisuuksia. Laskulla tulee ilmi erääntyvä tapahtuma toimittajan tilille, joka on luotu tilausta luotaessa, jonka jälkeen maksu käsitellään.

