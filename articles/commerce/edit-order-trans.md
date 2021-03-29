---
title: Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen
description: Tässä aiheessa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fee5ef7ad61e9581e7b2797bb1bd26b1a48ddbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221771"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Commerce-sovelluksen versioiden 10.0.5 ja 10.0.6 välillä lisättiin itsepalvelutukkutapahtumien (kuten myynti ja palautus) ja kassanhallintatapahtumien (kuten liukuva merkintä ja maksuvälineen poisto) muokkauksen tuki. Commerce-sovelluksen versiossa 10.0.7 lisättiin online-tilaustapahtumien ja asynkronisten asiakastilaustapahtumien muokkauksen tuki.

## <a name="edit-and-audit-order-transactions"></a>Tilaustapahtumien muokkaaminen ja tarkistaminen

Voit muokata ja tarkistaa Commerce-pääkonttorisovelluksen tapahtumia seuraamalla alla olevia ohjeita.

1. Asenna [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Määritä **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun **Tilauksen synkronointivirheiden estokoodi** -kohdassa estokoodi.
1. Avaa **Myymälän myyntitiedot** -työtila. **Online-tilauksen synkronointivirheet**- ja **Asiakastilauksen synkronointivirheet** -ruuduissa on vähittäismyyntitapahtuman sivun esisuodatettu näkymä. Ne näyttävät tapahtumatietueet, joiden vastaavan tilaustyypin synkronointi epäonnistui.
1. Avaa **Online-tilauksen synkronointivirheet**- tai **Asiakastilauksen synkronointivirheet** -sivu. Valitse tietue, jonka synkronointivirheen tietoja haluat tarkastella. **Synkronoinnin tila** -pikavälilehdessä ovat seuraavat virhetiedot:

    - Odottavan tilauksen tila
    - Tilausvirheen tiedot
    - Muokkauksen päivämäärä ja aika
    - Uudelleenyrityslaskuri

1. Jos virheen tiedot osoittavat, että tietuetta on korjattava, valitse **Office Add-in** ja valitse sitten **Muokkaa valittua tapahtumaa**. Valitun tapahtuman tiedot sisältävä Excel-tiedosto avataan.

    - Jos muokattava tapahtuma on online-tilaustapahtuma, Excel-tiedosto sisältää seuraavat laskentataulukot:

        - **Tapahtuma** – Tässä laskentataulukossa ovat tapahtuman otsikkotiedot.
        - **Myyntitapahtuma** – Tässä laskentataulukossa ovat tapahtuman rivitiedot.
        - **Maksutapahtumat** – Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.
        - **Alennustapahtumat** – Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.
        - **Verotapahtumat** – Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.
        - **kulutapahtumat** – Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.

    - Jos muokattava tapahtuma on asynkroninen asiakastilaustapahtuma, Excel-tiedosto sisältää seuraavat laskentataulukot:

        - **Rivit** – Tässä laskentataulukossa ovat tapahtuman otsikko- ja rivitiedot.
        - **Maksut** – Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.
        - **Alennukset** – Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.
        - **Verot** –Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.
        - **Kulut** – Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.

1. Syötä Excel-tiedoston **Odottava tilauksen tila** -kenttään **Muokkaus** ja julkaise muutos. Näin voit estää sen, että erätilassa suoritettava **Synkronoi tilaus** -työ ohittaa tämän tietueen käsittelyn aikana.
1. Excel-tiedostossa muokataan soveltuvia kenttiä. Tämän jälkeen tiedot ladataan takaisin Commerce-pääkonttorisovellukseen Dynamics Excel -lisäosan julkaisutoiminnon avulla. Kun tiedot on julkaistu, ne näkyvät järjestelmässä. Julkaisemisen aikana käyttäjien tekemiä muutoksia ei tarkisteta.
1. Voit tarkastella muutosten täydellistä kirjausketjua valitsemalla otsikkotason muutoksille **Näytä kirjausketju** -kohdan **Vähittäismyyntitapahtuma**-otsikossa soveltuvan tapahtumasivun osassa ja tietueessa. Esimerkiksi kaikki myyntiriveihin liittyvät muutokset näkyvät **Myyntitapahtumat**-sivulla ja maksuihin liittyvät muutokset **Maksutapahtumat**-sivulla. Seuraavia tarkistustietoja muutetaan:

    - Muokkauksen päivämäärä ja aika
    - Kenttä
    - Vanha arvo
    - Uusi arvo
    - Muokannut

1. Kun muutokset on tehty ja julkaistu, valitse **Synkronoi tilaus**, jos haluat aloittaa synkronointiprosessin heti. Vaihtoehtoisesti voit odottaa, että erätilassa suoritettava synkronointiprosessi käsittelee tapahtuman.

Kun tilaukset on synkronoitu, ne asetetaan oletusarvoisesti estotilaan Commerce-parametrien määrittämän estokoodin mukaan. Tilausten esto on poistettava, ennen kuin tilaukset voidaan käsitellä edelleen tilauksen täyttämistä tai muuta toimintoa varten.

## <a name="additional-resources"></a>Lisäresurssit

[Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen](edit-cash-trans.md)

[Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen](edit-financial-dim.md)

[Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten](create-excel-edit.md)

[Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]