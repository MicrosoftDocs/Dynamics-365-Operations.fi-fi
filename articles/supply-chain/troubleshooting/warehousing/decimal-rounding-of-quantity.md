---
title: Fyysisen päivitysmäärän desimaalipyöristys on virheellinen
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ei vastaa yksikön määrittämää desimaalitarkkuutta.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726558"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Fyysisen päivitysmäärän desimaalipyöristys on virheellinen

Virhekoodi: SYS19589

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ei vastaa yksikön määrittämää desimaalitarkkuutta.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Yksikön %1 fyysisen päivitysmäärän desimaalipyöristys on virheellinen.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Järjestelmä arvioi, vastaako lähetysmäärän desimaalipyöristys lähetysyksikölle määritettyä desimaalitarkkuutta. Kun järjestelmä pyöristää lähetysmäärän määritettyyn desimaalien määrään ja havaitsee, että pyöristetty lähetysmäärä ei vastaa varsinaista lähetysmäärää, pakkausluetteloa ei voi luoda. Tämä ongelma voi ilmetä esimerkiksi silloin, kun myyntimäärä on 1,75 kilogrammaa (kg), mutta desimaalitarkkuus on *1*.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa.
- Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa

Tarkista seuraavan ohjeen avulla kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.
1. Valitse  **Kuormitusrivit**-välilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.
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
