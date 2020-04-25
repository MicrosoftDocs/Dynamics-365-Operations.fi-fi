---
title: Luo ostotilaus kertatoimittajalle
description: Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76915772809d736cac9e8a9439d9e693a4490eec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204904"
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

