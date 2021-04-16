---
title: Aikaikkunat
description: Voit optimoida huoltotilausrivien ajoittamisen aikaikkunoiden avulla.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a958c76e8bd31b57e3f89b2be45028c0597a58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824291"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]