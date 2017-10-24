---
title: "Määritä petoshälytyksiä"
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a>Määritä petoshälytyksiä

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon. 

Ennen kuin määrität ja käytät petosten tarkistussääntöjä, salli petosten tarkistaminen ja määritä petostarkistusten perusarvot puhelinkeskusparametreissa. Petossääntöjä on kahdenlaisia:

-   **Staattiset säännöt** käyttää tiettyä arvoa, kuten mustalle listalle asetettua puhelinnumeroa.
-   **Dynaamiset säännöt** voivat koostua muuttujista ja ehdoista.

Ennen kuin luot dynaamisen säännön, sinun on luotava muuttujat ja ehdot, jotka määrittävät, ketä sääntö koskee ja milloin sääntöä käytetään. Voit esimerkiksi luoda säännön, joka edellyttää, että kun asiakas 1202 tekee vähintään 1 000,00 arvoisen tilauksen, myyntitilaus tulee asettaa pitoon, kunnes asiakkaan maksu voidaan varmistaa. Tässä tapauksessa muuttujat ovat asiakas 1202 ja tilauksen kokonaissumma 1 000,00. Ehto määrittää, että jos asiakas 1202 suorittaa tilauksen ja tilauksen kokonaissumma on yhtä suuri tai enemmän kuin 1 000,00, myyntitilaus on asetettava pitoon, kunnes asiakkaan maksu voidaan vahvistaa.




