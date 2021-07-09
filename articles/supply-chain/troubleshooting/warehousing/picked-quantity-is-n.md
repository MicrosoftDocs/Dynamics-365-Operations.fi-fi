---
title: Kerätyt määrät eivät riitä pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää kerätyn määrän, joka ei vastaa kuormituslinjalla luotua työmäärää.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249096"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Kerätyt määrät eivät riitä pakkausluettelon luonnin aikana

Virhekoodi: SYS54073

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, lähtevä kuorma sisältää kerätyn määrän, joka ei vastaa kuormituslinjalla luotua työmäärää.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Koska %1 on keräily, kohteen %2 päivittäminen ei riitä, jos jäännöksen on oltava %3.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Pakkausluetteloa ei voi luoda nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:

- Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.
- Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.
- Kuormituslinjan määrä, työn luoma määrä ja poimittu määrä eivät täsmää.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.
- Muokkaa kuormitusrivin määrää.
- Palauta kaikki keräilymerkinnät ja tee keräys uudelleen.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat

Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Huomioi **Työn luontimäärä** -kentän arvo.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.
1. Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.

### <a name="adjust-the-load-line-quantity"></a>Muokkaa kuormitusrivin määrää

Seuraavia ohjeita noudattamalla voit säätää kuormarivin määrää.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.
1. Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.
1. Valitse  **Kuormitusrivit**-välilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.
1. Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.
1. Määritä **Pienennä kuormitusrivi** -kenttä vastaamaan kuormitusrivin oikaisuja.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Palauta kaikki keräilymerkinnät ja tee keräys uudelleen

Ongelma saattaa ilmetä, koska henkilö on käyttänyt valintarekisteröintiä kuormarivin sulkemiseen ilman työtä. Tässä tapauksessa manuaalinen keräilyrekisteröinti on peruutettava, ja keräily on sitten suoritettava käyttämällä Warehouse Management -mobiilisovellusta.

Seuraavia ohjeita noudattamalla voit peruuttaa keräilyrekisteröinnin.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.
1. Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.
1. Valitse  **Myyntitilausrivit**-välilehdestä myyntitilausrivi, jota varten rekisteröinti on tehty.
1. Voit poistaa nimikkeet valitsemalla **Päivitä rivi \> Kerää**.
