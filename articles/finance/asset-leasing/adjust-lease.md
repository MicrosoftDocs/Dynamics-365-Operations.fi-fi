---
title: Vuokrasopimusten muuttaminen
description: Ohjeaiheessa kerrotaan, miten vuokrasopimusta muutetaan. Oikaisu voi olla tarpeen, jos vuokra-aikoja muutetaan, vuokrasopimusta pidennetään tai muita ehtoja muutetaan.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442981"
---
# <a name="adjust-leases"></a>Vuokrasopimusten muuttaminen

[!include [banner](../includes/banner.md)]

Ohjeaiheessa kerrotaan, miten vuokrasopimusta muutetaan. Oikaisu voi olla tarpeen, jos vuokra-aikoja muutetaan, vuokrasopimusta pidennetään tai muita ehtoja muutetaan. Resurssin vuokraus noudattaa ASC 842:n ja IFRS 16:n ohjeita vuokrasopimuksen muokkauksesta. ASC 842-20-15-1 määrittää vuokrasopimuksen muokkauksen miksi tahansa sopimuksen ehtojen muutokseksi, jos se muuttaa vuokrasopimuksen laajuutta tai kohdetta. IFRS 16:n kappale 39 määrittää, että vuokralle ottajan on uudelleenarvostettava vuokrasopimusvelka niin, että se vastaa vuokrien muutoksia.

ASC 842- ja IFRS 16 -säädöksiä noudattavissa organisaatioissa vuokrasopimus arvioidaan uudelleen niin, että se vastaa tulevan vähimmäisvuokran nykyisen arvon muutosta. Jos tämä arvo kasvaa, luotu kirjauskansiovienti veloitetaan käyttöoikeusomaisuuserästä ja hyvitetään vuokrasopimusvelalle uuden ja edellisen arvon välisenä erona. Jos arvo pienenee, kirjauskansiovienti veloitetaan vuokrasopimusvelasta ja ero hyvitetään käyttöoikeusomaisuuserälle.

Js oikaisu vähentää käyttöoikeusomaisuuserän alle arvon 0 (nolla), jäljellä oleva osa hyvitetään vuokrasopimuksen muokkauksen kirjaustilin voittoon. Se on määritetty **Vuokrasopimuksen kirjaustilit** -sivulla. Järjestelmä ottaa huomioon nämä tapahtumat ja muut oikaisuviennit, kuten vuokrasopimuksen muokkauksen aiheuttamat luokittelun muutokset, alkuvaiheen välittömät menot, vuokrasopimukseen liittyvät kannustimet, ennakkomaksut ja purkamiskustannukset.

Lisäohjeita vuokrasopimuksen oikaisutapahtumia varten on IFRS 16- ja ASC 842 -ohjeissa.

Voit muuttaa vuokrasopimusta noudattamalla seuraavia vaiheita. Muokatut tiedot päivittävät vuokrausaikatauluja aikataulun luontiprosessin suorittamisen jälkeen.

1. Siirry kohtaan **Resurssin leasing \> Vuokrasopimukset \> Vuokrasopimusyhteenveto**.
2. Valitse **Vuokrasopimusyhteenveto**-sivulla muokattava vuokrasopimus ja valitse sitten **Muokkaa vuokrasopimusta**.
3. Syötä **Muokkaa vuokrasopimusta** -sivulla muokatun vuokrasopimuksen uusia tietoja.

    Huomaa, että **Muokkaa vuokrasopimusta** -sivu muistuttaa **Lisää vuokrasopimus** -sivua. Vuokrasopimuksen lisäämisen yhteydessä määritetty aloituspäivämäärä määrittää, milloin vuokrasopimus alkaa. Samoin **Muokkauspäivämäärä**-kenttä **Muokkaa vuokrasopimusta** -sivulla määrittää, milloin muokattu vuokrasopimus alkaa. Tämä päivämäärä ei voi olla maksuaikataulurivien alkamispäivän jälkeen.

    > [!NOTE]
    > **Käyttöoikeusomaisuuserän tietoja** -kenttä koskee vuokrasopimuksen oikaisua. Jos muokattuun vuokrasopimukseen ei liity alkuperäisiä suoria kustannuksia vuokrasopimukseen liittyviä kannustimia, ennakkomaksuja tai purkamiskustannuksia, jätä nämä kentät tyhjiksi. Alkuperäiset summat eivät koske päivitettyä vuokrasopimusta. Muut kustannukset, jotka tapahtuvat vuokrasopimuksen muokkauksen jälkeen, syötetään **Muokkaa vuokrasopimusta** -sivulla.
    > 
    > Esimerkiksi vuokralle antaja antaa 1 000 dollarin kannustimen, jotta vuokrasopimus hyväksytään. Kun tässä tapauksessa vuokrasopimusta muutetaan niin, että se ottaa laajennuksen huomioon, syötä **1 000** **Vuokrasopimukseen liittyvät kannustimet** -kenttään. Jos vuokrasopimuksen oikaisuun ei liity kannustimia, tyhjennä kaikki tähän kenttää aikaisemmin syötetyt arvot. Samaa logiikkaa sovelletaan myös muihin käyttöoikeusomaisuuden tietoihin.

    Oikaistun vuokrasopimuksen maksuaikataulurivit luodaan mahdollisina riveinä. Maksuaikataulurivit, joiden luontiperustana on käytetty mahdollisuutta, eivät voi alkaa ennen kuin vuokrasopimuksen muokkaukset ovat voimassa.

    Seuraavat vaiheet ovat lähes samat kuin vuokrasopimuksen alkuperäisessä tunnistamisessa.

4. Valitse **Luo aikataulut**, jos haluat luoda oikaistun maksuaikataulun. Näyttöön tulee sanoma, joka ilmaisee, että vuokrasopimukselle on luotu maksuaikataulu.

    > [!IMPORTANT]
    > Ennen kuin valitset **Luo aikataulut**, varmista, että muokkauspäivämäärä ja maksuaikataulurivit on määritetty oikein. Varmista myös, että kaikki alkuvaiheen välittömät menot, vuokrasopimukseen liittyvät kannustimet, ennakkomaksut tai purkamiskustannukset vastaavat vain oikaisusta koituneita kustannuksia.

5. Voit tarkastella juuri luotua maksuaikataulua valitsemalla **Kirjat** ja avaamalla sitten **Maksuaikataulu**-sivun.
6. **Maksuaikataulu**-sivulla voit muokata oikaistuja maksusummia, ennen kuin vahvistat maksuaikataulun. Vahvista aikataulu valitsemalla **Vahvista aikataulu**.

    Kun maksuaikataulu on vahvistettu, uusi resurssin poisto ja uudet vuokrasopimusvelan aikataulut on luotu.

7. Voit tarkastella uutta vuokrasopimusvelan kuoletusaikataulua, joka luotiin uusista syötteistä, sulkemalla **Maksuaikataulu**-sivun ja avaamalla **Velan kuoletusaikataulu** -sivun.
8. Voit tarkastella juuri luotua resurssin poistoaikataulua avaamalla **Resurssin poistoaikataulu** -sivun **Kirjan tiedot** -sivulla.
9. Jos haluat luoda oikaisukirjauskansioviennin, valitse **Toiminto \> Vuokrasopimuksen oikaisu**. Näyttöön tulee sanoma, joka ilmaisee, että oikaisukirjauskansiovienti on luotu. 
10. Voit tarkastella kirjauskansiovientiä valitsemalla **Kirjauskansiot \> Resurssin leasingkirjauskansio**.
11. Voit kirjata kirjauskansioviennin valitsemalla rivin ja valitsemalla sitten **Kirjaa**.

## <a name="view-lease-versions"></a>Vuokrasopimusversioiden tarkasteleminen

Jos vuokrasopimusta on muokattu, voit tarkastella sen eri versioita. Voit myös tarkastella aiempia aikatauluja ja aiempien vuokrasopimusten tietoja.

1. Valitse **Vuokrasopimusyhteenveto**-sivu ja valitse sitten toimintoruudussa **Vuokrasopimuksen versiohistoria**.

    Jos valittu vuokrasopimus on oikaistu, **Vuokrasopimuksen versiohistoria** -sivulla näkyvät sen eri versiot. Alkuperäisen vuokrasopimuksen otsikko on **1**. Seuraavien versioiden numerot ovat suurempia.

    Voit tarkastella valitun vuokrasopimusversion taloushallinnon dimensioita, sopimustietoja, sijaintia ja maksuaikataulurivejä.

2. Jos haluat tarkastella aiempia aikatauluja, avaa muokattu vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla, valitse haluttu kirja ja valitse sitten toimintoruudussa **Kirjan versiohistoria**.
3. Valitse **Kirjan versio** -sivulla haluttu versio ja aikataulu tarkastelemista varten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]