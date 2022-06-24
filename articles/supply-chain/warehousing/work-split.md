---
title: Työn jako
description: Tässä artikkelissa on tietoja työn jakotoiminnosta. Tällä toiminnolla voidaan jakaa suuret työtilaukset useiksi pieniksi työtilauksiksi, jotka voidaan sitten määrittää useille varastotyöntekijöille. Tällä tavoin useat varastotyöntekijät voivat keräillä samaa työtä samanaikaisesti.
author: Mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 83333f4d8c755bc0ca4b2d141a5591ef43501b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857022"
---
# <a name="work-split"></a>Työn jako

[!include [banner](../includes/banner.md)]

Työnjakotoiminnolla voidaan jakaa suuret työtunnukset (eli useita rivejä sisältävät työtilaukset) useiksi pieniksi työtunnuksiksi, jotka voidaan sitten määrittää useille varastotyöntekijöille. Tällä tavoin useat varastotyöntekijät voivat keräillä samaa työn luontinumeroa samanaikaisesti.

> [!IMPORTANT]
> Vain sellaiset työtilaukset, joiden tila on *Avoin* tai *Käsittelyssä*, voidaan jakaa.

## <a name="turn-on-the-work-split-functionality"></a>Työn jakotoiminnon ottaminen käyttöön

Ennen kuin työn jakotoimintoa voidaan käyttää, se ja sen edellytyksenä oleva toiminto on otettava käyttöön. Järjestelmänvalvojat voivat tarkistaa [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa toimintojen tilan ja ottaa ne tarvittaessa käyttöön.

Jos edellytyksenä oleva *Organisaation laajuinen työn esto* -toiminto ei ole vielä käytössä, se on otettava käyttöön. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä. Ominaisuus on kuitenkin edelleen mainittu [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) seuraavasti:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Organisaation laajuinen työn esto*

> [!NOTE]
> Kun tämä toiminto on aktivoitu, tietojen päivitys tapahtuu automaattisesti, kun toiminto on otettu käyttöön kaikissa yrityksissä.

Ota seuraavaksi *Työn jako* -toiminto, joka ilmaistaan seuraavasti:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon jako:** *Työn jako*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Työn tiedot- ja Kaikki työt -sivujen laajennukset

*Työn jako* -toiminto lisää seuraavat kaksi painiketta **Työn tiedot**- ja **Kaikki työt** -sivujen toimintoruudun **Työ**-välilehteen:

- **Jaa työ** – jaa nykyinen työtunnus useiksi pieniksi työtunnuksiksi, joita eri työntekijät voivat käsitellä.
- **Peruuta työn jakoistunto** – peruuta työn jakoistunto ja anna mahdollisuus työn käsittelyyn.

![Jaa työ- ja Peruuta työn jakoistunto -painikkeet.](media/Work_split_buttons.png "Jaa työ- ja Peruuta työn jakoistunto -painikkeet")

> [!IMPORTANT]
> **Jaa työ** -painike ei ole käytettävissä, jos jokin seuraavista ehdoista toteutuu.
>
> - Työn tila on jokin muu kuin *Avoin* tai *Käsittelyssä*.
> - Konttitunnus on liitetty työtunnukseen. (Konttia ei voi jakaa järjestelmässä, sillä se edellyttää fyysisiä toimia.)
> - Työ on liitetty klusteriin.
> - Työtilauksen tyyppi ei ole jokin seuraavista:
>
>    - Myyntitilaukset
>    - Raaka-aineiden keräily
>    - Siirtovarasto-otto
>
> - Toinen käyttäjä jakaa parhaillaan työtä. Jos yrität avata sellaisen työn jakosivun, jota toinen käyttäjä jo jakaa, seuraava virhesanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan. Yritä uudelleen muutaman minuutin kuluttua. Jos näet tämän sanoman uudelleen, ota yhteys työnjohtajaan.

Uusi työn estosyy, *Jaa työ*, ilmaisee, kun työtunnusta ollaan jakamassa. Se näkyy sekä **Jaa työt** -sivulla että varastonhallinnan mobiilisovelluksessa, jos käyttäjä yrittää suorittaa työn. Jos eston syitä käytetään, työtunnuksen **Estetty aalto** -kentän arvoksi vaihtuu **Estetty**.

## <a name="initiate-a-work-split"></a>Työn jaon aloittaminen

Toiminto lisää uuden **Jaa työ** -sivun, jossa käyttäjät voivat jakaa työtunnuksen työrivejä. Kun sivu avataan ensimmäisen kerran, siinä on näkyvissä rivit, joiden työn tila on *Avoin* ja jotka ovat jaettavissa. Käsittele valittu työ valitsemalla toimintoruudussa **Jaa työ**.

Työ jaetaan seuraavasti:

1. Avaa jokin seuraavista työsivuista:

    - **Työn tiedot** (**Varastonhallinta \> Työ \> Työn tiedot**)
    - **Kaikki työt** (**Varastonhallinta \> Työ \> Kaikki työt**)

1. Valitse ruudukossa jaettava työtunnus. **Työtilaustyyppi**-kentän arvoksi on määritettävä jokin seuraavista arvoista:

    - Myyntitilaukset
    - Raaka-aineiden keräily
    - Siirtovarasto-otto

1. Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Jaa työ**.

    **Jaa työ** -sivu avautuu, ja näkyvissä on avoimet ja jaettavissa olevat työrivit. Oletusarvoisesti vain käytettävissä olevat työrivit näytetään. Voit tarkastella kaikki työtunnuksen rivit (kuten rivit, joiden työtyyppi on *Aseta*) valitsemalla **Näytä kaikki rivit** -valintaruudun ruudukon yläpuolella.

    Seuraava sanoma avautuu: Käyttäjät eivät voi käsitellä työn rivejä, ennen kuin jakaminen on lopetettu ja tämä sivu suljettu.

    Nykyisen työn **Työn eston syy** -kentän asetukseksi määritetään *Jaa työ* ja työ estetään.

    ![Eston syy.](media/Blocking_reason.png "Eston syy")

1. Valitse nykyisestä työtunnuksesta poistettavat rivit ja lisää uusi työtunnus. Seuraavat tapahtumat:

    - Kun työ jaetaan, alkuperäisestä työtunnukset valitut rivit peruutetaan ja kopioidaan sitten uuteen työtunnukseen.
    - Aiemmin luodun työmallin rakenne ja asettamisen sijainti (sekä tulevat keräily/hyllytys-parit) säilytetään. Seuraavien työtunnuskenttien arvot kopioidaan alkuperäisestä työstä uuteen työhön:

        - Kuormatunnus
        - Lähetyksen tunnus
        - Työtilaustyyppi
        - Tilauksen numero
        - Toimipaikka
        - Varasto
        - Työn prioriteetti
        - Työpoolin tunnus
        - Aallon tunnus
        - Työn luontinumero

    - Seuraavia kenttiä ei kopioida uuteen työtunnukseen:

        - **Työtunnus** – uusi työtunnus luodaan soveltuvasta numerosarjasta.
        - **Työn tila** – tämän kentän arvoksi määritetään *Avoin*.
        - **Lukitsija** – tämä kenttä jää aluksi tyhjäksi.
        - **Kohderekisterikilven tunnus** – tämä kenttä jätetään tyhjäksi.
        - **Luonnin päivämäärä ja aika** – tämän kentän asetuksena on kuluva päivämäärä ja aika.
        - **Estetty aalto / lukittu** – tämä kenttä lasketaan uudelleen alkuperäiselle työtunnukselle ja uudelle työtunnukselle.

1. Valitse toimintoruudussa **Jaa työ**.

Työtä jaettaessa avautuu seuraava sanoma: Käsitellään toimintoa – jaa työ. Kun tämä sanoma on näkyvissä, voit peruuttaa toiminnon valitsemalla sanomaruudussa **Peruuta**.

Jos **Näytä kaikki rivit** -valintaruutua ei ole valittu, jaettu ja peruutettu rivi ei enää näy ruudukossa. Jos valintaruutu on valittu, kyseisen rivin **Työn tila** -kentän arvoksi olisi pitänyt vaihtua *Peruutettu*.

Seuraava ilmoitus näytetään osoittamaan, että uusi työtunnus on luotu: Työ \#\#\#\# on luotu jakamalla se alkuperäisestä työstä \#\#\#\#.

Muut alkuperäisen työtunnuksen työrivit (kuten *Aseta*-rivit) oikaistaan tarvittaessa ilmaisemaan peruutetut työn rivit. Jos esimerkiksi alkuperäisen työntunnuksen *Aseta*-rivin määrä oli 15 ja *Keräily*-rivien yhteismäärä oli 10 ja ne peruutettiin, alkuperäisen työtunnuksen uusi *Aseta*-määrä on nyt 5.

Uutta työtä ei määritetä heti yhdellekään käyttäjälle. Voit kuitenkin määrittää sen nyt tarvittaessa käyttäjälle käyttämällä **Työn tiedot** -sivun vakiotoimintoa.

> [!IMPORTANT]
> Vain sellaiset työtunnukset voidaan jakaa, joissa on vähintään kaksi käytettävissä olevaa työriviä. Jos valitse **Jaa työ**, kun käytössä on vain yksi työrivi, seuraava virhesanoma avautuu: Alkuperäiseen työhön on jäätävä vähintään yksi työrivi. Tässä tapauksessa jakoa ei tehdä.

## <a name="finish-a-work-split"></a>Työn jaon lopettaminen

Työn jakamisen lopettaminen edellyttää, että *Jaa työ* eston syynä on poistettava. Sen voi tehdä kahdella tavalla:

- Työn jakava käyttäjä sulkee **Jaa työ** -sivun valitsemalla **Sulje**-painikkeen (**X**) sivun oikeassa yläkulmassa. Kun sivu suljetaan, *Jaa työ* eston syynä poistetaan. Tämän työn *Estetty*-tila käsitellään uudelleen ja jos työllä ei ole muita eston syitä, työn esto poistetaan.
- Joku käyttäjä avaa työtunnuksen ja valitsee toimintoruudussa **Peruuta työn jakoistunto** -painikkeen. *Jaa työ* poistetaan eston syynä ja työn *Estetty*-tila käsitellään uudelleen samalla tavoin kuin **Jaa työ** -sivua suljettaessa.

Kun *Jaa työ* on poistettu eston syynä, työ voidaan suorittaa mobiililaitteessa, mikäli **Estetty**-tilan asetuksena on työtunnuksessa *Ei*.

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a>Käyttäjien esto varastonhallinnan mobiilisovelluksessa

Jos yrität suorittaa keräilytyön varastonhallinnan mobiilisovelluksessa sellaisen tunnuksen osalta, jota jaetaan, seuraava virhesanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan. Jos tämä sanoma avautuu, valitse **Peruuta**. Voit sitten jatkaa muiden töiden käsittelyä.

## <a name="other-blocked-operations"></a>Muut estetyt toiminnot

Kaikki sellaiset jaettavaan työhön liittyvät toiminnot, jotka muokkaavat työrivejä, työn varastotapahtumia tai täydennyslinkkejä, epäonnistuvat ja seuraava sanoma avautuu: Työtä, jonka tunnus on \#\#\#\#, jaetaan parhaillaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]