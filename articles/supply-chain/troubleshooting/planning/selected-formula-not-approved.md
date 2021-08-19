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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712907"
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
