---
title: Fyysisesti vastaanotetut ostotilaukset eivät näy varaston sulkemisraportissa
description: Fyysisesti vastaanotetut ostotilaukset eivät näy varaston Tarkista avoimet määrät -sulkemisraportissa.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026473"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Fyysisesti vastaanotetut ostotilaukset eivät näy varaston sulkemisraportissa

Tietopankin numero: 4612595

## <a name="symptoms"></a>Oireet

Fyysisesti vastaanotetut ostotilaukset eivät näy varaston **Tarkista avoimet määrät** -sulkemisraportissa.

## <a name="resolution"></a>Ratkaisu

**Tarkista avoimet määrät** -raportissa näkyvät varasto-ottotapahtumat, joita ei voi selvittää kirjanpitoon päivitettyjen varastovastaanottojen kanssa valittuna sulkemispäivämääränä. Voit sisällyttää fyysiset vastaanotot raporttiin. Tässä tapauksessa fyysiset vastaanotot näkyvät, jos ne voivat kattaa ne varasto-ottotapahtumat, joita ei voida selvittää. Lisätietoja on kohdassa [Varaston sulkemisen valmisteleminen](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
