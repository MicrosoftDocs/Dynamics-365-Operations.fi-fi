---
title: Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa
description: Kun yrität vahvistaa suunnitellun tilauksen, saat virhesanoman, jossa todetaan, että tilaus on ajoitettava, ennen kuin se voidaan vahvistaa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294069"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa

Virhekoodi: SYS309802

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee seuraava virhesanoma:

> Suunniteltu tuotantotilaus on ajoitettava ennen kuin se voidaan vahvistaa.

## <a name="cause"></a>Syy

Ajoitetut aloitus- ja päättymispäivät eivät voi olla tyhjiä.

## <a name="resolution"></a>Ratkaisu

Voit määrittää suunnitellun tilauksen alkamis- ja päättymispäivät noudattamalla seuraavia ohjeita.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**.
1. Avaa asianmukainen suunniteltu tilaus.
1. Määritä **Yleiset**-pikavälilehden **Ajoitettu**-osassa päivämäärät **Aloitus**- ja **Päättymispäivä**-kenttiin.
