---
title: Mallien käyttö
description: Tässä ohjeaiheessa käsitellään mallien käsittelemistä Microsoft Dynamics 365 Commercessa.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4ed3b6797127113450949aa957437125f37394f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995713"
---
# <a name="work-with-templates"></a>Mallien käyttö


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään mallien käsittelemistä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Mallit määrittävät tietoja verkosta tietoja lataavien tekijöiden käytettävissä olevat asetusjoukot, kuten ohjeaiheessa [Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md) kerrotaan. Mallit ovat hyödyllisiä yrityksen verkkoluontiryhmälle useiden syiden vuoksi. Hyvin suunnitellut mallit voivat auttaa seuraavien tavoitteiden saavuttamisessa:

- Päivittäisen sisällön muokkaajien roolin luontikokemuksen yksinkertaistaminen.

    - Moduuliasetusten suodattaminen niin, että vain tarvittavat moduulit näkyvät sivun tietyssä osassa. (Esimerkiksi mallin markkinointiosa voidaan määrittää suodattamaan pois tarpeettomat moduulit, joita ei koskaan tule käyttää kyseisessä kontekstissa ja jotka vain monimutkaistavat sisällön muokkaamiseen liittyviä tehtäviä.)
    - Määritä moduulin oletusasetukset niin, että muokkaaminen on tehokasta.
    - Voit parantaa muokkaamisen tehoa määrittämällä sivun oletusosia. (Esimerkiksi mallin ylä-ja alatunnisteiden osat näkyvät automaattisesti jokaisella tietoja verkosta tietoja lataavalla sivulla.)

- Pidä yrityksen sivustojen yrityskuvaa yllä määrittämällä hyväksytty joukko moduulien järjestely- ja määritysasetuksia.

    > [!TIP] 
    > Onnistuneet sähköisen kaupan sivustot tarjoavat asiakkaille tuttuja ja toistuvia yrityskuvakokemuksen malleja. Mallien avulla voit hallita sivuston yhdenmukaisuutta.

- Paranna Hakukoneoptimoinnin tuloksia varmistamalla toistuvuus ja ohjelmallisesti määritetyn sivun määritykset ja metatiedot.

> [!NOTE]
> Vaikka mallit on suunniteltu valvomaan sivuston yhtenäisyyttä, ne voidaan teoriassa määrittää niin, että ne eivät pakota yhdenmukaisuuteen. Yrityskuvan ja sivuston järjestelmänvalvojat voivat määrittää sivuston sivuille haluamansa määrän vaihtelevuutta. Esimerkiksi malli voidaan jättää kokonaan avoimeksi niin, että sisällöntekijät voivat luoda haluamansa sivurakenteen. Tässä tapauksessa mitkään edellisen luettelon eduista eivät ole käytettävissä.

## <a name="modify-a-template"></a>Mallin muokkaaminen

Malleja muokataan mallieditorin avulla.

Voit avata mallieditorin suorittamalla jommankumman seuraavista vaiheista:

- Valitse sivuston siirtymisruudussa **Mallit** ja valitse sitten muokattava malli.
- Valitse olemassa olevan sivueditorissa vasemmalla olevan jäsennyspuun ylin solmu. Valitse sitten oikealla olevassa ominaisuusruudussa **Muokkaa mallia**.

Vasemmalla olevassa jäsennyspuussa on moduuliasetukset ja -rakenteet, jotka ovat käytettävissä alatason asetuksia ja sivuja varten. Kun valitset moduulin jäsennyspuusta, näkyviin tulevat valitun moduulin malliominaisuudet oikealla olevaan ominaisuusruutuun. Joitakin näistä ominaisuuksista käytetään vain mallin muokkaamisessa. Seuraavassa taulukossa kuvataan nämä ominaisuudet.

| Ominaisuuden nimi | Kuvaus |
|---|---|
| Toistojen vähimmäismäärä | Tämä ominaisuus määrittää valitun moduulin esiintymiskertojen vähimmäismäärän. Jos arvoksi on määritetty esimerkiksi **1**, vaaditaan moduuli tietoja verkosta tietoja lataavia tekijöitä varten. Jos arvoksi on määritetty **0** (nolla), moduuli on valinnainen. |
| Toistojen enimmäismäärä | Tämä ominaisuus määrittää valitun moduulin esiintymiskertojen enimmäismäärän. Jos arvoksi on määritetty esimerkiksi **1**, moduulin voi lisätä vain kerran. |
| Moduulien vähimmäismäärä (säilöt) | Tämä ominaisuus määrittää muita moduuleja (eli *säilöjen moduuleja*) sisältävien moduulien alitason moduuleina lisättävän vähimmäismäärän. Jos kyseessä on esimerkiksi karusellimoduuli, arvoksi voidaan määrittää luku, joka on suurempi kuin 1. |
| Moduulien enimmäismäärä (säilöt) | Tämä ominaisuus määrittää säilömoduulien enimmäismäärän, joka on lisättävä alitason moduuleina. Jos kyseessä on esimerkiksi karusellimoduuli, arvoksi voidaan määrittää luku, joka on pienempi kuin 10. |
| Lukittu | **Lukittu**-totuusarvo-ohjausobjekti näkyy kaikkien ydinmoduulin ominaisuuksien vieressä. Sen avulla mallin tekijä voi lukita moduulin määrityksen mallissa. Mikään alitason asettelu tai sivu ei voi ohittaa lukitun moduulin määrityksiä. Siitä tulee keskitetysti muokattava ominaisuusarvo kaikille mallia käyttäville asetteluille ja sivuille. |

## <a name="create-a-new-template"></a>Luo uusi malli

Voit luoda uuden mallin seuraavien vaiheiden avulla.

1. Valitse sivuston siirtymisruudussa **Mallit** ja avaa malli tarkistusnäkymässä.
1. Valitse **Uusi malli**.
1. Syötä mallin luonnin valintaruutuun mallin nimi ja kuvaus. Syöttämäsi arvot näkyvät tekijöille, kun ne luovat uusia sivuja. Anna sen vuoksi metatietoja, joista on hyötyä sivujen tekijöille. Kirjoita kuvaukseksi esimerkiksi **Käytä tätä mallia, kun haluat luoda yleisiä markkinointisivuja**. Näitä metatietoja voi muokata myöhemmin.
1. Luo uusi malli ja avaa mallieditori valitsemalla **OK**. Mallieditorissa on vasemmalla puolella jäsennyspuu ja oikealla puolella ominaisuusruutu.
1. Laajenna jäsennyspuun solmut ja valitse **HTML Head** -paikka.
1. Jos tässä paikassa ei ole vielä moduuleja, valitse kolmeen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivun yhteenveto** ja valitse sitten **OK**.
1. Valitse jäsennyspuussa uusi moduuli ja syötä sitten ominaisuusruutuun oletusasetukset, jotka määritetään automaattisesti kaikille mallin alitason sivuille. Jos et halua määrittää oletusasetuksia, jätä arvot tyhjiksi.
1. Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolmeen pisteen painike ja valitse sitten **Lisää moduuli**.
1. Valitse sivun säilömoduuli (käytettävissä voi olla vain yksi vaihtoehto) ja valitse sitten **OK**.

Uuden sivun säilömoduulissa näkyy paikkojen uusi joukko (**Ylätunniste**, **Pää** jne.). Tässä voit lisätä ja määrittää moduuliasetukset. Ne ovat tekijöiden käytettävissä, kun he luovat sivuja tästä mallista. Jos et lisää paikkaan moduuleja, tässä paikassa tuetaan oletusarvoisesti kaikkia moduulityyppejä.

Malli on nyt teknisesti kelvollinen. Sen voi nyt tallentaa, kuitata sisään ja sitä voi käyttää uusien sivujen luomisessa. Seuraavissa kolmessa osassa kuvataan kuitenkin joitakin muita oletusasetuksia, jotka kannattaa määrittää ensin.

## <a name="add-a-header-and-a-footer"></a>Ylä- ja alatunnisteen lisääminen

Jos sivustossa on jo ylätunnisteen osa, lisää malliin ylä- ja alatunniste seuraavien vaiheiden avulla.

1. Laajenna jäsennyspuussa **Tekstiosa**-kohta ja sen alitason sivun moduuli.
1. Valitse **Ylätunniste**-paikka.
1. Valitse **Ylätunniste**-paikan kolmen pisteen painike ja valitse sitten **Lisää osa**.
1. Etsi ja valitse sivuston ylätunnisteen osa ja valitse sitten **OK**.

Kaikki mallia käyttävät sivut perivät nyt automaattisesti tämän ylätunnisteen osan.

Jos sivustossa ei vielä ole ylätunnisteen osaa, katso lisätietoja sen luomisesta kohdasta [Osan luominen](work-with-fragments.md#create-a-fragment). Tee sitten edelliset vaiheet valmiiksi.

## <a name="change-the-template-theme"></a>Malliteeman vaihtaminen

Voit määrittää kaikkien mallia käyttävien sivujen oletusteeman seuraavasti.

1. Laajenna vasemmanpuoleisen jäsennyspuun **Tekstiosa**-paikka.
1. Valitse **Tekstiosa**-paikassa sivun säilömoduuli (esimerkiksi **Oletussivu**).
1. Valitse oikealla olevan ominaisuusruudun **Teema**-kentässä teema.

Oletusarvoisesti kaikki uudet sivut käyttävät nyt valittua teemaa. Jos haluat estää sivuja ohittamasta tätä asetusta asettelu- tai sivutasolla, määritä **Lukittu**-totuusarvo-ohjausobjektin arvoksi **Tosi**.

## <a name="add-a-script-to-a-template"></a>Komentosarjan lisääminen malliin

Voit lisätä malliin JavaScriptiä sisältäviä HTML:n **&lt;komentosarja&gt;**-elementtejä. Näin voit määrittää sivujen HTML Head ja tekstiosan alku- ja loppuosille komentosarjojen oletustoimintoja.

Voit lisätä malliin komentosarjan seuraavasti:

1. Valitse vasemmalla olevasta jäsennyspuusta paikka, johon haluat lisätä **&lt;komentosarja&gt;**-elementin (esimerkiksi HTML Head tai tekstiosan alku tai loppu).
1. Valitse paikan kolmen pisteen painike ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaruudussa komentosarjamoduuli (esimerkiksi **Ulkoinen komentosarja** tai **Sisäinen komentosarja**).
1. Syötä komentosarja oikealla olevan ominaisuusruudun soveltuvaan komentosarjan ominaisuusohjausobjektiin (esimerkiksi **Sisäinen komentosarja** tai **Komentosarjan tunnukset**).
1. Kirjoita ominaisuusruutuun muut valinnaiset asetukset, jotka haluat määrittää.

> [!TIP]
> Jos haluat käyttää joitakin komentosarjan moduuleita uudelleen muissa malleissa, voit muuntaa ne osiksi. Näin voit tehostaa luontiprosessia ja keskittää päivitysprosessin. Lisätietoja komentosarjan moduulin muuntamisesta osaksi on kohdassa [Aiemmin luodun moduulin määrityksen tallentaminen osaksi](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment)

## <a name="save-check-in-preview-and-publish-a-template"></a>Mallin tallentaminen kirjaaminen sisään, esikatseleminen ja julkaiseminen

Voit tallentaa mallin ja kirjata sen sisään seuraavasti.

1. Valitse **Tallenna** mallieditorin yläosassa. Tallennetut muutokset eivät vaikuta verkosta tietoja lataaviin sivuihin, ennen kuin ne on kuitattu sisään.
1. Valitse **Viimeistele muokkaus**. Tekemäsi muutokset ovat nyt verkosta tietoja lataavien työnkulkujen löydettävissä.

Voit esikatsella muutoksia avaamalla olemassa olevan mallia käyttävän sivun tai luomalla uuden sivun mallista.

Kun olet esikatsellut malliin tehdyt muutokset, julkaise malli live-sivustossa jonkin seuraavan vaiheen avulla.

* Siirry **Mallit**-kohtaan, valitse malli ja valitse sitten **Julkaise**.
* Valitse asettelun nimi avataksesi asettelueditorin ja valitse sitten **Julkaise**.
* Julkaise sivu, joka viittaa julkaisemattomaan malliin. Malli julkaistaan automaattisesti.

> [!WARNING]
> Kun malli tai jokin muu sisällön hallintajärjestelmän (CMS) kohde julkaistaan, se on löydettävissä Internetistä. Älä julkaise asiakirjoja tai resursseja, jos ne eivät ole valmiita julkiseen käyttöön. Asiakirjaversiot, jotka on tallennettu ja kuitattu sisään, mutta joita ei ole julkaistu, ovat vain todennettujen järjestelmäkäyttäjien löydettävissä.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)
