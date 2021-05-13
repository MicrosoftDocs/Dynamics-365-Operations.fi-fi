---
title: Mittayksiköiden hallinta
description: Tässä aiheessa kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921338"
---
# <a name="manage-units-of-measure"></a>Mittayksiköiden hallinta

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.

## <a name="open-the-units-page"></a>Avaa Yksiköt-sivu

Jos haluat luoda ja käyttää järjestelmässä käytettävissä olevia mittayksiköitä, siirry kohtaan **Organisaation hallinto \> Asetukset \> Yksiköt \> Yksiköt**.

Tämän ohjeaiheen muut osat kuvaavat, mitä voit tehdä **Yksiköt**-sivulla.

## <a name="create-standard-units-and-conversions"></a>Vakioyksiköiden ja muunnosten luominen

Jos järjestelmä ei sisällä vielä eniten käytettyjä mittayksiköitä metrijärjestelmässä ja/tai USCS-järjestelmässä, ohjatun yksikkömäärityksen avulla voit aloittaa perusyksikkömääritykset ja -muunnokset nopeasti. Voit suorittaa ohjatun toiminnon loppuun valitsemalla toimintoruudusta **Ohjattu yksikköjen luonti** noudattamalla sitten näyttöön tulevia ohjeita.

## <a name="create-or-edit-a-unit-of-measure"></a>Mittayksikön luominen tai muokkaaminen

Voit luoda mittayksikön tai muokata sitä noudattamalla seuraavia vaiheita.

1. Noudata seuraavia ohjeita:

    - Jos haluat muokata aiemmin luotua yksikköä, valitse se luetteloruudusta.
    - Valitse toimintoruudussa **Uusi** luodaksesi uuden yksikön.

1. Määritä tietueen ylätunnisteessa seuraavat kentät:

    - **Yksikkö** – Kirjoita tunnus tai symboli, jota käytetään yksikön viittaamiseen järjestelmän kielellä. Tämä tunnus tai symboli on yleensä yksikköä varten oleva yleinen lyhenne, esimerkiksi *kpl* (kappale) tai *cm* (senttimetri).
    - **Kuvaus** – Syötä yksikölle kuvaava nimi järjestelmän kielellä. Tämä nimi on yleensä yksikön koko nimi, esimerkiksi *Kappale* tai *Senttimetri*.

1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Yksikköluokka** – Valitse ominaisuus, jonka mittayksikkö mittaa (esimerkiksi pituus, alue, massa tai määrä).
    - **Yksikköjärjestelmä** – Valitse mittausjärjestelmä, johon yksikkö kuuluu (*Metrijärjestelmän yksiköt* tai *Yhdysvaltojen yksikköjärjestelmän yksiköt*).
    - **Perusyksikkö** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää nykyistä yksikköä yksikköluokan perusyksikkönä. Tällöin sinun on määritettävä vain perusyksikön ja kunkin yksikköluokan lisäyksikön välinen muuntokerroin. Järjestelmä voi tämän jälkeen muuntaa kaikkien yksikön luokan yksiköiden välillä. Siksi on helpompi määrittää muunnokset.

        Jos esimerkiksi gallona on *Tilavuus*-yksikköluokan perusyksikkö, muuntokertoimet on määritettävä vain neljännesgallonasta gallonaan ja pintista gallonaan. Tämän jälkeen järjestelmä voi myös muuntaa sen neljännesgallonasta pintiin.

        Yhtä yksikköluokkaa kohden voi olla vain yksi perusyksikkö.

    - **Järjestelmäyksikkö** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää nykyistä yksikköä kaikkien yksikköluokan määrittämättömien mittojen oletettuna yksikkönä. Esimerkiksi jos määrän syöttöön käytettävä kenttä ei salli yksikön määrittämistä (tai jos käyttäjä ei valitse yksikköä), järjestelmä käyttää yksikköä, joka on määritetty *Määrä*-yksikköluokan järjestelmäyksiköksi. Yhtä yksikköluokkaa kohden voi olla vain yksi järjestelmäyksikkö.
    - **Desimaalitarkkuus** – Määritä desimaalien määrä, joksi nykyiselle yksikölle määritetyt tai siihen muunnetut arvot pyöristetään.

1. Valitse toimintoruudussa **Tallenna**.

## <a name="define-unit-translations"></a>Yksikkökäännösten määrittäminen

Kun haluat määrittää tunnuksen tai symbolin käännökset ja mittayksikön kuvauksen, noudata seuraavia ohjeita.

1. Luo tai valitse yksikkö, jolle käännökset luodaan.
1. Valitse toimintoruudussa **Yksikön tekstit**.

    **Yksikkötekstit**-sivu avautuu. Tällä sivulla voit määrittää valitun yksikön tunnuksen tai symbolin käännökset. Käännöksiä voidaan tämän jälkeen käyttää ulkoisille tiedostoille asiakas- tai toimittajakohtaisissa kielissä.

1. Valitse toimintoruudussa **Uusi**.
1. Valitse **Kieli**-kentässä kieli, jolle yksikön tunnus tai symboli käännetään.
1. Kirjoita **Teksti**-kenttään yksikön tunnuksen tai symbolin käännös valitulla kielellä.
1. Valitse toimintoruudussa **Tallenna**.
1. Sulje sivu.
1. Valitse **toimintoruudussa** **Käännetyt yksiköiden kuvaukset**.

    **Käännetyt yksiköiden kuvaukset** -sivu tulee näkyviin. Tämän sivun avulla voit määrittää valitun yksikön kielikohtaiset kuvaukset.

1. Valitse toimintoruudussa **Uusi**.
1. Valitse **Kieli**-kentässä kieli, jolle yksikön kuvaus käännetään.
1. Kirjoita **Kuvaus**-kenttään yksikön kuvauksen käännös valitulla kielellä.
1. Valitse toimintoruudussa **Tallenna**.
1. Sulje sivu.

## <a name="define-unit-conversion-rules"></a>Yksikön muunnössääntöjen määrittäminen

Noudata seuraavia ohjeita, kun haluat määrittää mittayksiköiden välisten muunnosten säännöt.

1. Luo tai valitse yksikkö, jolle muunnosten säännöt määritetään.
1. Valitse toimintoruudussa **Yksikkömuunnokset**.

    **Yksikkömuunnokset**-sivu avautuu. Tällä sivulla voit määrittää valitun yksikön muuntamisen säännöt muihin yksiköihin ja muista yksiköistä yksikköluokassa.

1. Valitse jokin seuraavista välilehdistä määritettävän muuntotyypin mukaan:

    - **Vakiomuunnokset** – Määritä kaikkien tuotteiden vakiomuuntosäännöt.
    - **Luokansisäiset muunnokset** – Määritä tuotekohtaiset muuntosäännöt saman yksikköluokan yksiköille.
    - **Luokkienväliset muunnokset** – Määritä tuotekohtaiset muuntosäännöt eri yksikköluokkien yksiköille.

1. Noudata seuraavia ohjeita:

    - Valitse työkalurivillä **Uusi** luodaksesi uuden muunnoksen.
    - Jos haluat muokata aiemmin luotua muunnosta, valitse muunnos ruudukosta ja valitse sitten työkaluriviltä **Muokkaa**.

1. Näyttöön tulevassa avattavassa valintaikkunassa kuvaillaan seuraavat kentät:

    - **Tuote** – Valitse tietty tuote, jota muunnos koskee. Tämä kenttä on käytettävissä vain luokansisäisissä ja luokkienvälisissä muunnoksissa.
    - **Kaavan asettelu** – Jätä tämän kentän asetukseksi *Yksinkertainen*, jos haluat määrittää yksinkertaisen muunnoksen, jolla on yksi kerroin. Määritä sen arvoksi *Lisäasetukset*, jos haluat määrittää monimutkaisemman yhtälön. Edistyneiden yhtälöiden muoto vaihtelee yksikköluokan mukaan.
    - **Yksiköstä** – Tässä kentässä näkyy valittu yksikkö. Yleensä arvoa ei pitäisi muuttaa. (Jos muutat arvoa, avaa valitun yksikön **Yksikkömuunnokset**-sivu, jos haluat tarkastella uutta muunnosta sen tallentamisen jälkeen.)
    - **Yksikköön** – Valitse yksikkö, johon muunnetaan.
    - **Pyöristys** – Valitse, kuinka murtoluvut pyöristetään valitun yksikön **Desimaalitarkkuus**-arvon perusteella (*Lähimpään*, *Ylös* tai *Alas*).
    - **Muuntokaava** – Määritä avattavan valintaikkunan yläosassa olevien kenttien avulla kaava muuntamiseen näiden kahden yksikön välillä. Käytettävissä olevat kentät vaihtelevat valitsemasi yksikköluokan ja kaavan asettelun mukaan.

1. Valitse **OK**.
1. Sulje sivu.

> [!TIP]
> Voit myös määrittää yksikkömuunnoksia tuotevarianttia kohti. Lisätietoa on kohdassa [Mittayksiköiden tuotevarianttikohtaiset muunnokset](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
