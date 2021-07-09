---
title: Toimittajan koodia ei ole valtuutettu tietylle tuotteelle ja päivämäärälle
description: Kun yrität vahvistaa suunnitellun tilauksen tai lisätä rivin ostotilaukseen, näyttöön tulee virhesanoma, jossa todetaan, että toimittajan koodi ei ole valtuutettu tuotteen ja päivämäärän osalta.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294068"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Toimittajan koodia ei ole valtuutettu tietylle tuotteelle ja päivämäärälle

Virhekoodi: SYP4881415

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa suunnitellun tilauksen tai lisätä rivin ostotilaukseen, näyttöön tulee seuraava virhesanoma:

> Toimittajan koodia %1 ei ole valtuutettu kohteelle %2 kohteessa %3.

## <a name="cause"></a>Syy

Virhe ilmenee, koska hyväksytyn **toimittajan tarkistusmenetelmän** kentän arvoksi on määritetty *Vain varoitus* tai *Ei sallittu* määritetylle tuotteelle eikä toimittajalla ole tällä hetkellä oikeutta toimittaa tätä tuotetta.

## <a name="resolution"></a>Ratkaisu

Voit korjata tämän ongelman poistamalla toimittajan valintaruudun käytöstä tai hyväksymällä toimittajan.

Jos haluat poistaa tuotteen toimittajan tarkistuksen käytöstä, noudata seuraavia ohjeita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa asiaankuuluva tuote.
1. Määritä **Osto**-pikavälilehdessä **Hyväksytyn toimittajan tarkistusmenetelmä** -kentän arvoksi jokin muu kuin *Vain varoitus* tai *Ei sallittu*.

Jos haluat hyväksyä tuotteen toimittajan, noudata seuraavia ohjeita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa asiaankuuluva nimike.
1. Valitse Toimintoruudussa **Osto**-välilehdellä **Hyväksytty toimittaja** -ryhmässä **Asetukset**.
1. Lisää rivi ruudukkoon **Hyväksytty toimittaja** -luettelosivulla ja määritä sitten sille seuraavat arvot:

    - **Toimittaja** – Valitse toimittaja, joka hyväksytään nykyiselle tuotteelle.
    - **Voimaantulopäivä** – Valitse ensimmäinen päivä, jona toimittaja on hyväksytty.
    - **Erääntymispäivä** – Valitse viimeinen päivä, jona toimittaja on hyväksytty.

Lisätietoja on kohdassa [Toimittajien hyväksyminen tiettyihin tuotteisiin](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
