--- 
title: Luo ostotilaus kertatoimittajalle
description: "Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Luo ostotilaus kertatoimittajalle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle. Toimittaja luodaan automaattisesti ostotilauksen yhteydessä, sen sijaan, että toimittajatili pitäisi luoda manuaalisesti. Ostotilaukset luo yleensä ostoedustaja. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Luomisen edellytys on, että kertatoimittajan tili on määritetty Ostoreskontran parametrit -sivulla.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Luo ostotilaus kertatoimittajalle
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Valitse Kertatoimittaja-kentän arvoksi Kyllä.
    * Ostotilaukselle luodaan ja määritetään automaattisesti toimittajatili. Toimittajatili luodaan Ostoreskontran parametrit -sivun Yleiset-välilehdellä määritetyn mallin mukaisesti.  
4. Kirjoita Nimi-kenttään toimittajan yksilöivä nimi.
5. Valitse OK.
    * Ostotilauksen nyt viedä loppuun ja käsitellä kuin minkä tahansa tilauksen. Tämän suorittamisessa ei ole mitään erityisominaisuuksia. Laskulla tulee ilmi erääntyvä tapahtuma toimittajan tilille, joka on luotu tilausta luotaessa, jonka jälkeen maksu käsitellään. Kun tämä on tehty, toimittajan tilin voi poistaa. Tämän suorittaa yleensä ostoreskontraosaston työntekijä.  


