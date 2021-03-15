---
title: Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla
description: Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbb4da093cd8a0fc6cd85e1f93dfb91f0fb8a382
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981128"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla

[!include [banner](../../includes/banner.md)]

Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella. Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.


## <a name="create-a-production-order"></a>Luo tuotantotilaus
1. Valitse siirtymisruudussa **Moduulit >Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset**.
2. Valitse **Uusi tuotantotilaus**.
3. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Valitse nimiketunnus **D0001**.  
4. Valitse **Luo**.

## <a name="schedule-operations-for-the-production-order"></a>Ajoita tuotantotilauksen työvaiheet.
1. Merkitse juuri luotu rivi.      
2. Valitse toimintoruudussa **Ajoitus**.
3. Valitse **Ajoita työvaiheet**.
4. Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.
5. Anna **Ajoituspäivämäärä**-kentässä päivämäärä. Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua. Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.  
6. Valitse **OK**.
7. Merkitse valittu rivi luettelossa. Huomaa, että tila on nyt **Ajoitettu**. 
8. Valitset **Kaikki työt**. Huomaa, että työvaiheiden ajoituksella ei luoda töitä.  
9. Sulje sivu.

## <a name="schedule-jobs-for-the-production-order"></a>Ajoita tuotantotilauksen työt.
1. Valitse toimintoruudussa **Ajoitus**.
2. Valitse **Ajoita työt**.
3. Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.
4. Anna **Ajoituspäivämäärä**-kentässä päivämäärä. Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua. Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.  
5. Valitse **OK**.
6. Valitse toimintoruudussa **Tuotantotilaus**.
7. Valitset **Kaikki työt**. Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]