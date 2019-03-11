---
title: Aikaikkunat
description: Voit optimoida huoltotilausrivien ajoittamisen aikaikkunoiden avulla.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f748268f6cb85ff835919485da2828689eee23c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "347212"
---
# <a name="time-windows"></a>Aikaikkunat  

[!include [banner](../includes/banner.md)]

Voit optimoida huoltotilausrivien ajoittamisen aikaikkunoiden avulla. Voit määrittää järjestelmän siten, että huoltotilaukset luodaan automaattisesti. Voit liittää aikaikkunan määrittämien ehtojen perusteella mahdollisimman monta huoltotilausriviä mahdollisimman harvoihin huoltotilauksiin.

Aikaikkunat määrittävät, miten pitkälle huoltotilausrivi voidaan siirtää lasketusta päivämäärästä. Laskettu päivämäärä on päivämäärä, jolloin huoltotilausrivi on ajoitettu tapahtumaan. Päivämäärä perustuu sen väliasetukseen ja huoltojaksoon, jonka määritit **Luo huoltotilaukset**-sivulla. Aikaikkuna määritetään käyttämällä seuraavan taulun arvoja.

| Tapa | kuvaus                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viikko   | Päivämäärä, jona huoltotilausrivi voidaan siirtää mille tahansa avoimelle päivälle, joka on samalla viikolla kuin alkuperäinen laskettu päivämäärä.                                                                                                                                                                                    |
| Kuukausi  | Päivämäärä, jona huoltotilausrivi voidaan siirtää mille tahansa avoimelle päivälle, joka on samana kuukautena kuin alkuperäinen laskettu päivämäärä. Huoltotilausrivin laskettu päivämäärä on esimerkiksi 15.3.2017. Huoltotilausrivi voidaan ajoittaa mille tahansa viikonpäivälle 1.–28.2.2017. |
| Manuaalinen | Voit määrittää huoltotilausrivin siirron päivien enimmäismäärän ennen alkuperäistä laskettua päivämäärää tai sen jälkeen.                                                                                                                                                                           |

Jos huoltosopimuksen riville ei ole määritetty aikaikkunaa, huoltosopimuksesta johdettu huoltotilausrivi on suoritettava täsmälleen sinä päivänä, jolle se on alun perin ajoitettu.

## <a name="related-topics"></a>Liittyvät aiheet

[Aikaikkunoiden luominen](create-time-windows.md)

