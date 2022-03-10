---
title: Peruuta huoltotilaukset
description: Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cca6c34bb43702e2c33935a73dc24f1a630065c0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571518"
---
# <a name="cancel-service-orders"></a>Peruuta huoltotilaukset   

[!include [banner](../includes/banner.md)]


Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn.


> [!NOTE]
> <P>Huoltotilauksia ei voi peruuttaa, jos huoltotilauksen tila ei salli peruuttamista, jos huoltotilauksella on nimiketarpeita tai jos huoltotilaus on jo kirjattu.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Huoltotilauksen peruuttaminen Huoltotilaukset-lomakkeessa

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**. Valitse huoltotilaus ja valitse sitten **Peruuta tilaus** toimintoruudusta.

## <a name="cancel-a-service-order-line"></a>Huoltotilausrivin peruuttaminen

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**. Kaksoisnapsauta huoltotilausta, joka sisältää peruutettavan rivin.

2.  Valitse huoltotilausrivi, jonka haluat peruuttaa ja valitse sitten **Peruuta tilausrivi**, niin rivin tilaksi muuttuu **Peruutettu**.


> [!TIP]
> <P>Voit kumota huoltotilausrivin peruutuksen ja muuttaa tilan takaisin <STRONG>Luotu</STRONG>-tilaan valitsemalla <STRONG>Kumoa peruutus</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Useiden huoltotilausten peruuttaminen

1.  Valitse **Huoltohallinta** \> **Kausittainen** \> **Huoltotilaukset** \> **Peuuta huoltotilaukset**

2.  Napsauta **Valitse**-painiketta.

3.  Valitse peruutettavat huoltotilaukset **Kysely**-lomakkeen **Ehdot**-sarakkeessa.

4.  Sulje **Kysely**-lomake valitsemalla **OK**.

5.  Valitse **Näytä infoloki** -valintaruutu, jos haluat luoda infolokin, jossa näkyvät peruutetut huoltotilaukset.

6.  Valitse **Kumoa peruutus** -valintaruutu, jos haluat peruuttaa huoltotilauksen **Peruutettu**-tilan.

7.  Napsauta **OK**.

Valitut huoltotilaukset on joko peruutettu tai niiden **Peruutettu**-tila on palautettu tilaksi **Käsittelyssä**.


> [!NOTE]
> <P>Jos valitset <STRONG>Kumoa peruutus</STRONG> -valintaruudun, tilassa <STRONG>Peruutettu</STRONG> olevat huoltotilaukset palautetaan, eikä <STRONG>Käsittelyssä</STRONG>-tilassa olevia huoltotilauksia peruuteta.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]