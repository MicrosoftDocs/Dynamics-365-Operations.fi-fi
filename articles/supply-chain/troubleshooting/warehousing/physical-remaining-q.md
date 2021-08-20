---
title: Fyysisen jäljelle jäävän määrän yksikkö ei saa olla nolla
description: Kun luot pakkausluettelon, sen tietojen varastomäärä on muu kuin nolla mutta myyntimäärä on nolla.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 187363db3030ee0741f0c7e7746295b88320162c156120112332bb78593bb673
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744651"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Fyysisen jäljelle jäävän määrän yksikkö ei saa olla nolla

Virhekoodi: SYS19591

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, sen tietojen varastomäärä on muu kuin nolla mutta myyntimäärä on nolla.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Fyysisen jäännösmäärän yksikössä %1 täytyy olla muu kuin nolla.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Järjestelmä arvioi fyysisen jäljellä olevan määrän varastoyksikköinä ja fyysisen jäljellä olevan määrän lähetysyksikössä. Jos järjestelmä havaitsee, että lähetysyksikön fyysinen jäljellä oleva määrä on 0 (nolla), mutta varastoyksikön fyysinen jäljellä oleva määrä ei ole 0, pakkausluetteloa ei voi luoda. Tämä ongelma voi ilmetä esimerkiksi silloin, kun nimikkeen myyntiyksikkö ja varastoyksikkö eivät ole oikein eikä yksiköiden välinen muunnos ole oikein.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.
- Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa.
- Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.
- Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat

Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Huomioi **Työn luontimäärä** -kentän arvo.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.
1. Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa

Tarkista seuraavan ohjeen avulla kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman pyöristysongelmia.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.
1. Valitse  **Kuormitusrivit**-välilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimituksen.
1. Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.
1. Valitse  **Rivin erittely** -välilehdessä **Tilaus**.
1. Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -kentän arvo), jotta lähetysluettelon luontia voidaan jatkaa.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla

Käytä seuraavia vaiheita tarkistaaksesi kuormarivit ja tehdäksesi tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse **Kuormitusrivit**-pikavälilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman. Huomioi **Määrä**- ja **Yksikkö**-kenttien arvot.
1. Valitse **Organisaation hallinta \> Yksiköt \> Yksiköt**.
1. Valitse yksikkö, jota varten pakkausluetteloa ei voi luoda.
1. Säädä **desimaalitarkkuus**-kentän arvoa tarvittaessa.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö

Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö. Harkitse mittayksikön määrittämistä uudelleen nimikkeelle tarpeen mukaan.
