---
title: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
description: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760921"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.

Virhekoodi: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Osaa kuormaan %1 tarvittavista nimikkeistä ei ole vielä kerätty eikä siirretty lopulliseen lähetyssijaintiin.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormitusta tai lähetystä ei voi vahvistaa nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:

- Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.
- Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.
- Sijaintidirektiivi on määritetty pakkauspaikaksi lopulliseksi toimituspaikaksi aaltomallin säiliöintiä käytettäessä.

## <a name="resolution"></a>Ratkaisu

Kuorma tai lähetys on tilassa, jossa lähetysvahvistus epäonnistuu. Voit korjata ongelman tekemällä yhden seuraavista toimista:

- Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.
- Peruuta työtunnukset, jotka on luotu pakkaussijainniksi lopulliseksi toimitussijainniksi, konfiguroi sijaintitiedot uudelleen ja aseta kuormitus uudelleen.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat

Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Huomioi **Työn luontimäärä** -kentän arvo.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.
1. Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Peruuta työtunnukset, jotka on luotu pakkaussijainniksi lopulliseksi toimitussijainniksi, konfiguroi sijaintitiedot uudelleen ja aseta kuormitus uudelleen

Noudata seuraavaa menettelyä peruuttaaksesi työtunnukset, joissa pakkauspaikka on viimeinen sijoituspaikka, kun automaattinen säilytys on paikallaan.

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.
1. Näyttöön tulee **Peruuta työ** -valintaikkuna. Määritä **Työtunnus**-kenttään peruutettavan työn tunnus. Valitun työtunnuksen **työtilan** arvona on oltava *Avoin*, *Käynnissä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.
1. Valitse **OK**.
1. Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.
1. Toista nämä vaiheet tarvittaessa muille työtunnuksille.

Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).

Seuraavia ohjeita noudattamalla voit määrittää sijaintitiedot uudelleen, jotta pakkaussijaintia ei voi käyttää lopullisena lähetyssijainnina, kun mallille määritetään automaattinen konttimääritys.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.
1. Valitse sijaintidirektiivi, jota käytät automaattista konttiinpakkausta varten.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehden työkalupalkista **Muokkaa kyselyä**.
1. Etsi kyselyeditorin valintaikkunassa **Alue**-välilehdestä rivi, jonka **kentän** arvoksi on määritetty *Sijaintiprofiili*, ja varmista, että rivin **kriteeri**-kenttää ei ole määritetty sijaintiprofiiliksi, jonka **sijaintityyppinä** on *Pakkaus*. Korjaa lopullinen hyllysijainti muokkaamalla **Kriteeri**-kenttää.

Seuraavia ohjeita noudattamalla voit ottaa kuorman uudelleen käyttöön ja luoda työtunnukset, joilla on oikea lopullinen toimitussijainti.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Etsi **Kuormitukset**-osassa vapautettava kuormitus.
1. Vapauta valittu kuorma varastoon valitsemalla **Kuormat**-osan työkalupalkista **Vapautus \> Vapauta varastoon**.
1. Toista nämä vaiheet tarvittaessa muille kuormituksille.
