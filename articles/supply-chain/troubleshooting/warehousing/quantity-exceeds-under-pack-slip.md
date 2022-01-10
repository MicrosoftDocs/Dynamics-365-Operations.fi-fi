---
title: Määrä ylittää alitoimitusprosentin pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää alitoimitusprosentin.
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
ms.openlocfilehash: 7cdc22eeabda6cf9f08484d698e5096f66af4a12
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920695"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Määrä ylittää alitoimitusprosentin pakkausluettelon luonnin aikana

Virhekoodi: SYS24921

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää alitoimitusprosentin.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Rivin alitoimitus on %1 prosenttia, mutta sallittu alitoimitus on vain %2 prosenttia.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Kuorman tai lähetyksen keräysmäärä on vähemmän kuin tilattu määrä eikä se ole alitoimitusprosentin alueella.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Muokkaa alitoimitusprosenttia.
- Palauta ja tee tarvittavat oikaisut.

### <a name="adjust-the-under-delivery-percentage"></a>Muokkaa alitoimitusprosenttia

Seuraavia ohjeita noudattamalla voit säätää alitoimitusprosenttia.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.
1. Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.
1. Valitse **Myyntitilausrivit**-välilehdessä nimikkeelle myyntitilausrivi, joka ylittää alitoimitusprosentin.
1. Valitse **Rivin erittely** -välilehdessä **Toimitus**.
1. Määritä **Alitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysluettelon luonti voi jatkua.

### <a name="reverse-and-make-adjustments"></a>Palauta ja tee tarvittavat oikaisut

Peruuta kaikki kuormitukselle kirjatut tiedot (esimerkiksi pakkausluettelo, lähetysvahvistus ja työ), tee myyntitilauksen oikaisut, vapauta tilaus uudelleen varastoon ja suorita lähetysmenettely valmiiksi.

Seuraavia ohjeita noudattamalla voit peruuttaa pakkausluettelon.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun **Lähetys ja vastaanotto** -välilehden **Pakkausluettelon peruutus** **Käänteinen**-ryhmässä.

Seuraavia ohjeita noudattamalla voit peruuttaa lähetyksen vahvistuksen.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun **Lähetys ja vastaanotto** -välilehden **Käänteisen lähetyksen vahvistus** **Käänteinen**-ryhmässä.

Seuraavia ohjeita noudattamalla voit peruuttaa työn.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse toimintoruudun **Kuormitukset**-välilehden **Työ**-ryhmässä **Peruuta työ**.
