---
title: Katkelmien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914697"
---
# <a name="work-with-fragments"></a>Katkelmien käyttäminen 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Osat mahdollistavat koko sivustossa uudelleenkäytettävien moduulin määritysten keskitetyn muokkauskokemuksen. Esimerkiksi ylä- ja alatunnisteet sekä ilmoituspalkit määritetään usein osiksi, koska ne jaetaan useille sivuille. Voit ajatella osia pienoisverkkosivuina, jotka voidaan lisätä sivuston muihin sivuihin. Osilla on oma elinkaarensa. Toisin sanoen ne luodaan, päivitetään, niihin viitataan ja ne poistetaan yksittäisinä entiteetteinä muokkaustyökaluissa.

Kun osat on määritetty, niitä voidaan käyttää aina, kun moduuleja voi käyttää sivuston rakenteessa. Osiin voi viitata sivuilla, asetteluissa, malleissa ja muissa osissa.

> [!NOTE]
> Osat voivat olla sisäkkäisiä jopa seitsemän tason syvyyteen muissa osissa.

Jos haluat edistää esimerkiksi kausiluonteista tapahtumaa useilla sivuston sivuilla, voit käyttää osia. Uuden osan luontiprosessin ensimmäinen vaihe on valita sen moduulin tyyppi, jolla haluat aloittaa. Tässä esimerkissä voit muodostaa osan hero-moduulista.

> [!NOTE]
> Osia voi muodostaa mistä tahansa moduulityypistä.

Tämän jälkeen voit määrittää hero-osaan määritetyn kampanjasisällön. Voit myös lokalisoida sen tarpeen mukaan. Uutta erillistä hero-osaa voi tämän jälkeen kuluttaa esimääritettynä moduulina koko sivustossa. Voit helposti lisätä sen malleihin, tiettyihin sivuihin tai muihin osiin, joissa voi olla hero-moduuleita.

Kaikki paikat, joihin osa lisätään, ovat viittauksia luotuun, keskitettyyn hero-osaan. Jos julkaiset osan muutokset, ne vaikuttavat heti kaikissa sivuston paikoissa, joissa osaan viitataan. Tämän vuoksi osat ovat tehokas tapa käyttää uudelleen moduulin määrityksiä sivustossa ja hallita niitä keskitetysti. Tämä tehostettu käyttö ketteröittää toimintoja ja auttaa vähentämään sivuston hallintaan liittyviä kustannuksia.

Seuraavassa kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.

![Kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Osan luominen

Voit luoda uuden osan tai tallentaa olemassa olevan osan määrityksen osana.

### <a name="create-a-new-fragment"></a>Uuden osan luominen

Voit luoda uuden osan seuraavien vaiheiden avulla.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.
1. Valitse **Uuden sivun osa**. Näyttöön tulee valintaikkuna, jossa näkyvät kaikki käytettävissä olevat moduulityypit. Osat voi luoda mistä tahansa moduulityypistä, kuten aiemmin jo mainittiin.
1. Valitse osalle moduulityyppi ja valitse sitten **OK**.

    > [!TIP]
    > Kun valitset yleisen säilömoduulin tyypin, osan päivittäminen ja määrittäminen sujuu joustavasti myöhemmin.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Aiemmin luodun moduulin määrityksen tallentaminen osana

Voit muuntaa aiemmin määritetyn moduulin uudelleenkäytettäväksi osaksi seuraavasti.

1. Avaa sivu tai malli, joka sisältää osaksi muunnettavan moduulin.
1. Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan moduulin nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten **Tallenna osana**. Näyttöön tulee valintaikkuna.
1. Anna osan nimi ja metatiedot.
1. Valitse **OK**, jos haluat tallentaa moduulin määrityksen osana, joka voidaan lisätä muille sivuille.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Osien lisääminen sivulle tai niiden poistaminen tai muokkaaminen

Seuraavissa ohjeissa kuvataan, miten osia lisätään, poistetaan ja muokataan.

### <a name="add-a-fragment"></a>Osan lisääminen

Voit lisätä osan sivulle seuraavasti.

1. Valitse vasemmalla olevasta jäsennysruudusta säilö tai paikka, johon alimoduulit voidaan lisätä.
1. Valitse säilön tai paikan vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää osa**. Näyttöön tulee valintaikkuna.

    > [!NOTE]
    > Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää osa** -vaihtoehto ei ole käytettävissä.

1. Hae valintaikkunassa lisättävä osa ja valitse se. Jos käytettävissä olevia osia ei ole näkyvissä, sinun on ehkä ensin luotava osa moduulityypistä, jota valittu säilö tai paikka tukee.
1. Valitse **OK**, jos haluat lisätä valitun osan sivun valittuun säilöön tai paikkaan.

> [!NOTE]
> Moduulit, jotka sallitaan säilössä tai paikassa, määräytyvät sivun mallin tai moduulien omien määritysten mukaan.

### <a name="remove-a-fragment"></a>Osan poistaminen

Voit poistaa sivun osan paikasta tai säilöstä seuraavasti.

1. Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan osan nimen vieressä oleva kolmen pisteen painike ja valitse sitten roskakoripainike.
1. Kun sinua pyydetään vahvistamaan osan poistaminen, valitse **OK**.

> [!NOTE]
> Kun poistat osan sivulta, poistat vain viittauksen kyseiseltä sivulta. **Et** poista osaa sivustosta. Jos haluat poistaa osia sivustosta, käytä osan tarkistusohjelman käyttöliittymää. Voit poistaa osia sivustosta vain, jos niihin ei tällä hetkellä viitata sivuissa, malleissa tai muissa osissa.

### <a name="edit-a-fragment"></a>Osan muokkaaminen

Jos haluat muokata osia, sinun on käytettävä osan muokkausohjelman käyttöliittymää. Tämä on suunniteltu rajoitus. Sen avulla voidaan varmistaa, että tekijät eivät sekoita tietyn sivun moduulien muokkausprosessia sellaisten osien muokkausprosessiin, joita voidaan jakaa useille sivuille.

Voit muokata osaa seuraavien vaiheiden avulla.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.
1. Valitse **Osat**-kohdassa muokattava osa.
1. Muokkaa osan moduulin ominaisuuksia ja rakennetta tarpeen mukaan. Prosessi muistuttaa moduulien muokkausprosessia, jossa moduuleja muokataan sivueditorinäkymässä.

Voit muokata osaa myös valitsemalla sen sivulla, mallissa tai pääosassa ja valitsemalla sitten **Muokkaa osaa** -kohdan oikeanpuoleisessa ominaisuusruudussa.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Mallien käyttö](work-with-templates.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)
