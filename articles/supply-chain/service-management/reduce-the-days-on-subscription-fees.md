---
title: Ylläpitosopimusmaksujen päivien vähentäminen
description: Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362001"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Ylläpitosopimusmaksujen päivien vähentäminen 

[!include [banner](../includes/banner.md)]


Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Ylläpitosopimusmaksujen päivien vähentäminen

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Kaikki huoltotilaukset**. Valitse huollon ylläpitosopimus ja valitse toimintoruudussa **Ylläpitosopimusmaksut**

2.  Valitse **Ylläpitosopimustyyppi**-kentässä **Vähennyspäivät**.

3.  Kirjoita **Aloituspäivämäärä** - ja **Päättymispäivämäärä**-kenttiin sen ylläpitosopimusmaksun päivämääräväli, josta haluat poistaa kauden, ja valitse **OK**.

Voit katsella luotua tapahtumaa **Ylläpitosopimus**-lomakkeessa valitsemalla **Maksutapahtumat**.

## <a name="example"></a>Esimerkki

Jos ylläpitosopimustapahtuman kausi on 1.–31.1. ja haluat vähentää kautta 10 päivällä, luo uusi tapahtuma, jossa vähennyskausi on 1.–10.1. (Vähennyskausi voi olla myös 5.–15.1 tai mikä tahansa muu kymmenen päivän jakso).

Jos vähennyskauden **Aloituspäivämäärä**-arvo on 21.1. (31 miinus 10), voit määrittää **Päättymispäivämäärä**-kentän arvoksi minkä tahansa tammikuun 31. päivän jälkeisen päivän. Tällöinkin maksutapahtuman kaudesta vähennetään 10 päivää.

## <a name="see-also"></a>Lisätietoja

[Esimerkki vähennyspäivistä](reduction-days-example.md)

  


