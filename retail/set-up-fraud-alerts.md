---
title: "Määritä petoshälytyksiä"
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Määritä petoshälytyksiä

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon. 

Ennen kuin määrität ja käytät petosten tarkistussääntöjä, salli petosten tarkistaminen ja määritä petostarkistusten perusarvot puhelinkeskusparametreissa. Petossääntöjä on kahdenlaisia:

-   **Staattiset säännöt** käyttää tiettyä arvoa, kuten mustalle listalle asetettua puhelinnumeroa.
-   **Dynaamiset säännöt** voivat koostua muuttujista ja ehdoista.

Ennen kuin luot dynaamisen säännön, sinun on luotava muuttujat ja ehdot, jotka määrittävät, ketä sääntö koskee ja milloin sääntöä käytetään. Voit esimerkiksi luoda säännön, joka edellyttää, että kun asiakas 1202 tekee vähintään 1 000,00 arvoisen tilauksen, myyntitilaus tulee asettaa pitoon, kunnes asiakkaan maksu voidaan varmistaa. Tässä tapauksessa muuttujat ovat asiakas 1202 ja tilauksen kokonaissumma 1 000,00. Ehto määrittää, että jos asiakas 1202 suorittaa tilauksen ja tilauksen kokonaissumma on yhtä suuri tai enemmän kuin 1 000,00, myyntitilaus on asetettava pitoon, kunnes asiakkaan maksu voidaan vahvistaa.




