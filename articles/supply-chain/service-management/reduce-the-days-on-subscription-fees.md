---
title: Ylläpitosopimusmaksujen päivien vähentäminen
description: Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014819"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Ylläpitosopimusmaksujen päivien vähentäminen 

[!include [banner](../includes/banner.md)]


Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Ylläpitosopimusmaksujen päivien vähentäminen

1.  Valitse **Palveluiden hallinta** \> **Huoltotilaukset** \> **Kaikki huoltotilaukset**. Valitse huollon ylläpitosopimus ja valitse toimintoruudussa **Ylläpitosopimusmaksut**

2.  Valitse **Ylläpitosopimustyyppi**-kentässä **Vähennyspäivät**.

3.  Kirjoita **Aloituspäivämäärä** - ja **Päättymispäivämäärä**-kenttiin sen ylläpitosopimusmaksun päivämääräväli, josta haluat poistaa kauden, ja valitse **OK**.

Voit katsella luotua tapahtumaa **Ylläpitosopimus**-lomakkeessa valitsemalla **Maksutapahtumat**.

## <a name="example"></a>Esimerkki

Jos ylläpitosopimustapahtuman kausi on 1.–31.1. ja haluat vähentää kautta 10 päivällä, luo uusi tapahtuma, jossa vähennyskausi on 1.–10.1. (Vähennyskausi voi olla myös 5.–15.1 tai mikä tahansa muu kymmenen päivän jakso).

Jos vähennyskauden **Aloituspäivämäärä**-arvo on 21.1. (31 miinus 10), voit määrittää **Päättymispäivämäärä**-kentän arvoksi minkä tahansa tammikuun 31. päivän jälkeisen päivän. Tällöinkin maksutapahtuman kaudesta vähennetään 10 päivää.

## <a name="see-also"></a>Lisätietoja

[Esimerkki vähennyspäivistä](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]