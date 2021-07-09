---
title: Määrä ylittää ylitoimitusprosentin pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää ylitoimitusprosentin.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249094"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Määrä ylittää ylitoimitusprosentin pakkausluettelon luonnin aikana

Virhekoodi: SYS24920

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää ylitoimitusprosentin.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Rivin ylitoimitus on %1 prosenttia, mutta sallittu ylitoimitus on vain %2 prosenttia.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Kuorman tai lähetyksen keräysmäärä on enemmän kuin tilattu määrä eikä se ole ylitoimitusprosentin alueella.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Muokkaa kuormitusrivin määrää.
- Muokkaa ylitoimitusprosenttia.
- Palauta ja tee tarvittavat oikaisut.

### <a name="adjust-the-load-line-quantity"></a>Muokkaa kuormitusrivin määrää

Seuraavia ohjeita noudattamalla voit säätää kuormarivin määrää.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.
1. Valitse  **Kuormitusrivit**-välilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimitusprosenttia.
1. Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.
1. Valitse  **Rivin erittely** -välilehdessä **Tilaus**.
1. Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -kentän arvo), jotta lähetysluettelon luontia voidaan jatkaa.

### <a name="adjust-the-over-delivery-percentage"></a>Muokkaa ylitoimitusprosenttia

Seuraavia ohjeita noudattamalla voit säätää ylitoimitusprosenttia.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.
1. Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.
1. Valitse  **Myyntitilausrivit**-välilehdessä nimikkeelle myyntitilausrivi, joka ylittää ylitoimitusprosenttia.
1. Valitse  **Rivin erittely** -välilehdessä **Toimitus**.
1. Määritä **Ylitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysluettelon luonti voi jatkua.

### <a name="reverse-and-make-adjustments"></a>Palauta ja tee tarvittavat oikaisut

Peruuta kaikki kuormitukselle kirjatut tiedot (esimerkiksi pakkausluettelo, lähetysvahvistus ja työ), tee myyntitilauksen oikaisut, vapauta tilaus uudelleen varastoon ja suorita lähetysmenettely valmiiksi.

Seuraavia ohjeita noudattamalla voit peruuttaa pakkausluettelon.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Pakkausluettelon peruutus**  **Käänteinen**-ryhmässä.

Seuraavia ohjeita noudattamalla voit peruuttaa lähetyksen vahvistuksen.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.

Seuraavia ohjeita noudattamalla voit peruuttaa työn.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun  **Kuormitukset**-välilehden  **Työ**-ryhmässä  **Peruuta työ**.
