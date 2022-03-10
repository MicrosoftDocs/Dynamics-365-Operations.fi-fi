---
title: Et voi vahvistaa lähetystä, koska kuormituksen rivien määrä on nolla
description: Et voi vahvistaa lähetystä, koska kuormituksen rivien määrä on nolla.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344231"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Et voi vahvistaa lähetystä, koska kuormituksen rivien määrä on nolla

Virhekoodi: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Kaikilla kuorman %1 riveillä on nollamäärä.  
> Kuorman %1 lähetystä ei voitu vahvistaa.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Järjestelmä arvioi, voidaanko kuormarivi lähettää, luotujen työtunnuksien, kuormitusrivin määrän ja alitoimitusprosentin perusteella. Jos järjestelmä havaitsee, ettei työtunnuksia ole ja jos alitoimitusprosentiksi on määritetty 100 prosenttia, et voi vahvistaa lähetystä.

Tämä ongelma voi ilmetä esimerkiksi, jos työ on peruutettu ja kuormitusrivin alitoimitusprosentti on 100 prosenttia.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysvahvistus epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.
- Tarkista kuormitusrivit ja varmista, että alitoimitusprosentti ja määrät ovat suhteessa kerättyyn työhön.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Tarkista kuormarivit varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat

Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Avaa kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Huomioi **Työn luontimäärä** -kentän arvo.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.
1. Jos huomaat ristiriidan, peruuta vastaava työ, määritä sijaintidirektiivi uudelleen ja vapauta kuormitus uudelleen. Katso ohjeet kohdasta [Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty](picked-quantity-is-not-on-final.md).
1. Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Tarkista kuormitusrivit ja varmista, että alitoimitusprosentti ja määrät ovat suhteessa kerättyyn työhön

Seuraa näitä ohjeita tarkistaaksesi kuormitusrivit ja varmistaaksesi, että alitoimitusprosentti ja määrät ovat suhteessa kerättyyn työhön.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Avaa kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.
1. Muuta tarvittaessa **Alitoimitus**-kentän tai **Määrä**-kentän arvoa.

> [!TIP]
> Jos ongelmaa ei ole vielä korjattu, liittyvien myyntitilausten tai siirtotilausten keräystöitä on ehkä vielä jatkettava, kunnes käytettävissä oleva määrä on kohdistettu kuormituksen tai lähetyksen kanssa.
