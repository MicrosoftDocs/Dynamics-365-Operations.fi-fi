---
title: Aika- ja materiaaliprojektien myyntitilaukset
description: Tässä ohjeaiheessa käsitellään projektiin perustuvia myyntitilauksia aika-ja materiaaliprojekteissa.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551199"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Aika- ja materiaaliprojektien myyntitilaukset

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Tämä ohjeaihe kuvaa myyntitilauksen luomisen projektille. Vain **aika- ja materiaali** -tyyppisille projekteille voidaan luoda myyntitilauksia.

Jos aika- ja materiaaliprojektilla on useita rahoituslähteitä projektisopimuksessa, on otettava käyttöön **Salli myyntitilaukset projekteissa, joissa on useita rahoituslähteitä** -parametri **Projektinhallinnan ja kirjanpidon parametrit** -sivulla. 

> [!NOTE]
> - Tuki useiden rahoituslähteiden projektien myyntitilauksille on käytettävissä sovelluksen versiosta 10.0.2 lähtien.
> - Useita rahoituslähteitä sisältävien projektien myyntitilausten tuen parametri poistetaan huhtikuun 2020 julkaisuaallossa, minkä jälkeen toiminto on aina käytössä.

Voit luoda myyntitilauksia projektiin perustuen kahdella tavalla:

- Siirry projektiin. Valitse toimintoruudussa **Hallinta > Nimiketehtävät > Myyntitilaus**. Projektista luotuun myyntitilaukseen täytetään oletusarvoisesti projektin tiedot. Jos projektisopimuksessa on enemmän kuin yksi rahoituslähde, rahoituslähde on valittava, jotta voit määrittää myyntitilauksen asiakkaan. Jos projektissa on vain yksi rahoituslähde, asiakas määritetään automaattisesti.
- Siirry **Kaikki myyntitilaukset** -luettelosivulle ja luo uusi myyntitilaus. Myyntitilaukselle on valittava projekti. Sen jälkeen, kun projekti on valittu, asiakas määritetään rahoituslähteestä tai täytyy valita rahoituslähde, jos projektisopimuksessa on useita rahoituslähteitä.

