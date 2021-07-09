---
title: Valittua kaavan numeroa ei ole hyväksytty erätilaukseen
description: Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee virhesanoma, jossa todetaan, että valittua kaavan numeroa ei ole hyväksytty erätilauksen osalta.
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
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294061"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Valittua kaavan numeroa ei ole hyväksytty erätilaukseen

Virhekoodi: PRO2614

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa suunnitellun tilauksen, näyttöön tulee seuraava virhesanoma:

> Valittua reseptin numeroa ei ole hyväksytty erätilaukseen.

## <a name="cause"></a>Syy

Järjestelmä tarkistaa vahvistustoiminnon ja varmistaa, että aktiiviselle nimikkeelle on käytettävissä hyväksytty kaava. Kaava on todennäköisesti hyväksyttävä.

## <a name="resolution"></a>Ratkaisu

Voit hyväksyä kaavan seuraavasti.

1. Valitse **Tuotetietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.
1. Valitse haluamasi kaava.
1. Valitse toimintoruudun **Kaava**-välilehden **Ylläpidä**-ryhmässä **Hyväksy kaava**.
1. Valitse **Hyväksy tuoterakenne tai kaava** -valintaikkunassa hyväksyjä ja valitse sitten **OK**.
