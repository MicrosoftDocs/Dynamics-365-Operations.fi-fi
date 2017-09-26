--- 
title: "Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla"
description: "Menettely keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 10ccb4ac1088e27f3f5771bcb964bf3cc0a509ab
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla

[!include[task guide banner](../../includes/task-guide-banner.md)]

Menettely keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella. Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.


## <a name="create-a-production-order"></a>Luo tuotantotilaus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
2. Valitse Uusi tuotantotilaus.
3. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Valitse nimiketunnus D0001.  
4. Valitse Luo.

## <a name="schedule-operations-for-the-production-order"></a>Ajoita tuotantotilauksen työvaiheet.
1. Merkitse valittu rivi luettelossa.
    * Valitse juuri luomasi tuotantotilaus. Sen pitäisi olla ensimmäisenä luettelossa.      
2. Valitse toimintoruudussa Aikataulu.
3. Valitse Ajoita työvaiheet.
4. Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.
5. Anna Ajoituspäivämäärä-kentässä päivämäärä.
    * Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua. Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.  
6. Valitse OK.
7. Merkitse valittu rivi luettelossa.
    * Huomaa, että tila on nyt Ajoitettu.  
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Kaikki työt.
    * Huomaa, että työvaiheiden ajoituksella ei luoda töitä.  
10. Sulje sivu.

## <a name="schedule-jobs-for-the-production-order"></a>Ajoita tuotantotilauksen työt.
1. Valitse toimintoruudussa Aikataulu.
2. Valitse Ajoita työt.
3. Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.
4. Anna Ajoituspäivämäärä-kentässä päivämäärä.
    * Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua. Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.  
5. Valitse OK.
6. Valitse toimintoruudussa Tuotantotilaus.
7. Valitse Kaikki työt.
    * Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.  


