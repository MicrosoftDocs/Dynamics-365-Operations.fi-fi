---
title: Peruuta huoltotilaukset
description: Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228b76d6f6f0bb048662c8e82df76f51b7cb3652
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017373"
---
# <a name="cancel-service-orders"></a>Peruuta huoltotilaukset   

[!include [banner](../includes/banner.md)]


Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn.


> [!NOTE]
> <P>Huoltotilauksia ei voi peruuttaa, jos huoltotilauksen tila ei salli peruuttamista, jos huoltotilauksella on nimiketarpeita tai jos huoltotilaus on jo kirjattu.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Huoltotilauksen peruuttaminen Huoltotilaukset-lomakkeessa

1.  Valitse **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**. Valitse huoltotilaus ja valitse sitten **Peruuta tilaus** toimintoruudusta.

## <a name="cancel-a-service-order-line"></a>Huoltotilausrivin peruuttaminen

1.  Valitse **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**. Kaksoisnapsauta huoltotilausta, joka sisältää peruutettavan rivin.

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