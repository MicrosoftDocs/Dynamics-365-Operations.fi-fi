---
title: Keräilyrivin ryhmittely
description: Tässä ohjeaiheessa on keräilyrivin yhteenveto.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234630"
---
# <a name="pick-line-grouping"></a>Keräilyrivin ryhmittely

[!include [banner](../includes/banner.md)]

Keräilyrivin ryhmittelyssä useita työrivejä, joilla on sama nimike ja sijainti, voidaan yhdistää yhdeksi keräilyksi, joka näytetään käyttäjälle mobiililaitteessa. Tämän vuoksi varastotyöntekijät voivat saada mahdollisimman tehokkaat ohjeet samalla, kun tarvittava työrivien erottelu (esimerkiksi eri kontteihin ja tilauksiin) voidaan säilyttää järjestelmässä.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Työn keräilyrivien ryhmittelytoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa toiminnon tilan ja ottaa sen tarvittaessa käyttöön. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Keräilyrivin ryhmittely*

## <a name="set-up-pick-line-grouping"></a>Määritä keräilyrivin ryhmittely

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse **Valikkovaihtoehdon nimi** -kenttä ja anna *Myyntiryhmän rivikeräily*.
1. Valitse **Otsikko** -kenttä ja anna *Myyntiryhmän rivikeräily*. Tämä otsikko näkyy matkalaitteen valikossa.
1. Valitse **Tila**-kentässä *Työ*.
1. Valitse **Käytä nykyistä työtä** -asetukseksi *Kyllä*.
1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - Valitse **Ohjaaja**-kentässä *Järjestelmäohjattu*.
    - Määritä **Luo rekisterikilpi** -valinnan asetukseksi *Kyllä*.
    - Määritä **Ryhmäkeräily** -asetukseksi *Kyllä*.
    - Hyväksy jäljellä olevien vaihtoehtojen oletusarvot.

1. Määritä mobiililaitteen valikkovaihtoehdon kelvolliset työluokat seuraavasti:

    1. Valitse **Työluokat**-pikavälilehdessä **Uusi**.
    2. **Työluokan tunnus** -kentässä voi valita joko *Myynti* tai *Myyntitilauksen keräily* sen mukaan, mikä varasto on käytössä. Valitse tässä skenaariossa *Myyntitilauksen keräily*.

        **Työtilaustyyppi**-kentän arvoksi määritetään automaattisesti *Myyntitilaukset*.

### <a name="set-up-a-mobile-device-menu"></a>Määritä varaston mobiililaitteen valikko

Juuri luotu valikkovaihtoehto lisätään **Lähtevät**-valikkoon seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Luetteloruudussa näkyy kaikki aiemmin luodut mobiililaitevalikot. Valitse luettelossa *Lähtevät*.
1. Etsi ja valitse juuri luotu *Myyntiryhmän rivikeräily* -valikkovaihtoehto **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelossa.
1. Siirrä *Myyntiryhmän rivikeräily* -valikkovaihtoehto **Valikkorakenne** -luetteloon oikealla nuolipainikkeella.
1. Siirrä valikkovaihtoehto haluttuun kohtaan valikkorakenteessa ylä- ja alanuolipainikkeella.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-a-work-template"></a>Määritä työmalli

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.
1. Etsi ja valitse **Yleiskatsaus**-ruudukossa työmalli, jota on käytettävä tässä toiminnossa. Valitse tässä skenaariossa *51 Poiminta* -malli.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Valitse kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä **Lisää** ja määritä sitten seuraavat arvot uudelle riville:

    - Valitse **Taulu**-sarakkeessa *Väliaikaiset työtapahtumat*.
    - Valitse **Johdettu taulu**-sarakkeessa *Väliaikaiset työtapahtumat*.
    - Valitse **Kenttä**-sarakkeessa *Nimikkeen numero*.
    - Valitse **Hakusuunta**-sarakkeessa *Laskeva*.

1. Sulje valintaikkuna ja tallenna valinta valitsemalla **OK**.
1. Seuraava sanoma avautuu: Ryhmittely nollataan. Haluatko jatkaa? Jatka valitsemalla **Kyllä**.

> [!IMPORTANT]
> Jotta poimintarivin ryhmittelytoiminto toimisi, työrivit on lajiteltava nimiketunnuksen mukaan. Jos rivejä, joilla on samat nimikkeet, ei ole järjestetty yksitellen, niitä ei ryhmitellä.

## <a name="example"></a>Esimerkki

### <a name="create-picking-work"></a>Luo keräystyö

Ennen kuin voit määrittää keräilyrivin ryhmittelyn, sinun on luotava joitakin tukikelpoisia lähteviä töitä.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Valitse **Asiakastili**-kentässä *US-004*.
1. Valitse **Yleinen**-pikavälilehden **Varasto**-kentässä *51*.
1. Valitse **OK**.
1. Lisää seuraavat kuusi riviä **Myyntitilausrivit**-pikavälilehdessä:

    - Valitse **Rivi 1:** **Nimikkeen numero** -kentässä *M9200*. Kirjoita **Määrä**-kenttään *3*.
    - Valitse **Rivi 2:** **Nimikkeen numero** -kentässä *M9201*. Kirjoita **Määrä**-kenttään *3*.
    - Valitse **Rivi 3:** **Nimikkeen numero** -kentässä *M9202*. Kirjoita **Määrä**-kenttään *2*.
    - Valitse **Rivi 4:** **Nimikkeen numero** -kentässä *M9200*. Kirjoita **Määrä**-kenttään *1*.
    - Valitse **Rivi 5:** **Nimikkeen numero** -kentässä *M9200*. Kirjoita **Määrä**-kenttään *3*.
    - Valitse **Rivi 6:** **Nimikkeen numero** -kentässä *M9202*. Kirjoita **Määrä**-kenttään *7*.

    Tässä on yhteenveto kunkin nimikkeen kokonaismääristä:

    - **Nimike M9200:** *7* kpl
    - **Nimike M9201:** *3* kpl
    - **Nimike M9202:** *9* kpl

1. Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa kaikkien tilausten kaikille nimikkeille. Tarkista **Toimipaikkadirektiivin** asetus ja määritä, mitä keräilysijainteja myyntitilausten keräilyyn käytetään. Jos käytössä on varaston *51* Contoso-esittelytietoympäristö, vahvista varaston saatavuus.

    Kullekin riville on nyt varattava varastoa.

1. Valitse **Myyntitilausrivit**-pikavälilehdessä yksi varattavista riveistä.
1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Tee varaus valitsemalla **Varaus**-sivun toimintoruudussa **Varaa erä**. Sulje sitten sivu.
1. Toista vaiheet 8–10 muille varattaville riveille.

    Myyntitilaus on vapautettava varastoon.

1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Avautuva sanoma ilmoittaa, että lähetys ja aalto on luotu ja että aalto on lähetetty suoritettavaksi eränä.

    Kuun aalto ja kaikki sen jälkeiset työt on suoritettu, työlle luotavassa työtunnuksessa on kuusi riviä. Rivit lajitellaan nimiketunnuksen mukaan.

1. Voit tarkastella luotua työtä valitsemalla **Varastonhallinta \> Työ \> Kaikki työt**. Kirjoita **Työtunnus**-arvo muistiin, sillä sitä tarvitaan seuraavassa menettelyssä.

### <a name="initiate-picking-from-the-mobile-device"></a>Keräilyn käynnistäminen mobiililaitteesta

1. Kirjaudu mobiililaitteeseen käyttäjänä, joka on määritetty varastoon *51*.
1. Valitse mobiililaitteessa valikko, joka sisältää uuden mobiililaitteen valikkovaihtoehdon. Valitse tässä skenaariossa **Lähtevä**.
1. Käynnistä keräily valitsemalla **Myyntiryhmän rivikeräily** -valikkovaihtoehto.
1. Anna edellisessä menettelyssä muistiin kirjoitettu **Työtunnus**-arvo.

    Keräilyvaiheen, jossa kaikki nimikkeen *M9200* keräilyrivit on ryhmitelty, pitäisi olla näkyvissä, ja ohjeena pitäisi olla poimia *7* kappaletta nimikettä *M9200*.

    > [!IMPORTANT]
    > Kolmen keräilyrivin keräilytyö on koottu käyttäjälle yhdeksi keräilyvaiheeksi mobiililaitteessa.

1. Vahvista ensimmäinen vaihe.
1. Siirry työtunnuksen työsivulla, jossa huomaat, että nimikkeen *M9200* kaikki kolme keräilyriviä suljettiin samanaikaisesti.
1. Palaa mobiililaitteeseen ja jatka keräämistä. Nimikkeen *M9201* työrivin 4 pitäisi olla esillä. Koska tilauksessa on vain yksi työrivi, mitään koostettavaa ei ole.
1. Vahvista ensimmäinen vaihe.
1. Matkaviestimen viimeinen poimintavaihe kokoaa yhteen kaksi viimeistä poimintariviä työtilauksesta.
1. Tee nimikkeen *M9202* *9* kappaleen keräysvaihe.
1. Vahvista laittovaihe ja mahdolliset muut poiminta-/laittovaiheet töiden suorittamiseen.

> [!IMPORTANT]
>
> - Työrivit voidaan ryhmitellä vain, jos ne ovat järjestyksessä.
> - Seuraavaa toimintoa ei tueta:
>
>   - Todellisen painon nimikkeet
>
>    Jos työssä on mitään todellisen painon nimikkeitä, näyttöön tulee virhesanoma, ennen kuin aloitat poiminnan.
>
>   - Kappaleen keräily
>   - Työrivit, joilla on keskeneräinen täydennystyö
>   - Ylikeräily
>   - Nimikkeen uudelleenkohdistaminen lyhyen keräilyn avulla


[!INCLUDE[footer-include](../../includes/footer-banner.md)]