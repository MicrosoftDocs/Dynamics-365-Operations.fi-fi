---
title: Ostotilauksen kuitti ei sisällä kaikkia maksuja
description: Ostotilauksen kuitti ei sisällä kaikkia maksuja
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476186"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ostotilauksen kuitti ei sisällä kaikkia maksuja

## <a name="symptoms"></a>Oireet

kun vastaanotat ostotilauksen, kuitti ei sisällä kaikkia veloituksia.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Varmista **Osto- ja hankintaparametrit** -sivun **Toimitus**-välilehdessä, että **Luo maksuja tuotteen vastaanottamisen yhteyteen** -asetuksen arvona on *Kyllä*.
1. Luo ostotilaus, joka sisältää maksuja.
1. Vahvista ostotilaus.
1. Vastaanota ostotilaus.
1. Tarkista kuitin kokonaissumma ja vertaa sitä odotettuun summaan.
1. Huomaa, että kaikki maksut eivät sisälly ostotilauksen kuittiin.

## <a name="resolution"></a>Ratkaisu

Ratkaisu riippuu siitä, miten muut maksut on määritetty. Lisätietoja muiden maksujen määrittämisestä vastaamaan tarpeitasi on seuraavassa blogikirjoituksessa: [Kirjaa muut kulut tuotteen vastaanoton yhteydessä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
