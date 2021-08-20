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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777740"
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
