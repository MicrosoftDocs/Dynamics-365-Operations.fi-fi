---
title: Päivitettävä määrä ylittää vastaanotettavan/toimitetun määrän.
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ylittää työmäärän, joka oli kerätty ja varattu myyntitilaukselle.
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
ms.openlocfilehash: 25507a482b2db7c01f56679bf3e8454249de3a6b9965f9c359a2ebe2cc8445ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711684"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Päivitettävä määrä ylittää vastaanotettavan/toimitetun määrän

Virhekoodi: SYS7676

## <a name="symptoms"></a>Oireet

Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ylittää työmäärän, joka oli kerätty ja varattu myyntitilaukselle.

Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:

> Määrä, jota yrität päivittää, ylittää vastaanotetun/toimitetun määrän.

Et siis voi luoda lähetysluetteloa kuormaa varten.

## <a name="cause"></a>Syy

Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää. Tämä ongelma voi ilmetä esimerkiksi silloin, kun kuormarivin määrä, luodun määrän tai kerätty määrä ei ole oikein.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.
- Muokkaa kuormitusrivin määrää.
- Palauta kaikki keräilymerkinnät ja tee keräys uudelleen.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat

Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi luoda lähetystä.
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

Jos joku käyttää keräysrekisteröintiä kuormarivin sulkemiseen ilman työtä, kuormarivin määrän ja kerätyn määrän välillä voi olla ristiriita. Tässä tapauksessa manuaalinen keräilyrekisteröinti on peruutettava, ja keräily on sitten suoritettava käyttämällä Warehouse Management -mobiilisovellusta.

Seuraavia ohjeita noudattamalla voit peruuttaa keräilyrekisteröinnin.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.
1. Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.
1. Valitse  **Myyntitilausrivit**-välilehdestä myyntitilausrivi, jota varten rekisteröinti on tehty.
1. Voit poistaa nimikkeet valitsemalla **Päivitä rivi \> Kerää**.
