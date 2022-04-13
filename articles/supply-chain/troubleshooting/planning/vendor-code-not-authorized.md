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
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489053"
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

Lisätietoja on kohdassa [Toimittajien hyväksyminen tiettyihin tuotteisiin](../../procurement/tasks/approve-vendors-specific-products.md).
