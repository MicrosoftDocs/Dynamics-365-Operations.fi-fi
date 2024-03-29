---
title: Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen
description: Tässä artikkelissa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712105"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Commerce-sovelluksen versioiden 10.0.5 ja 10.0.6 välillä lisättiin itsepalvelutukkutapahtumien (kuten myynti ja palautus) ja kassanhallintatapahtumien (kuten liukuva merkintä ja maksuvälineen poisto) muokkauksen tuki. Commerce-sovelluksen versiossa 10.0.7 lisättiin online-tilaustapahtumien ja asynkronisten asiakastilaustapahtumien muokkauksen tuki.

## <a name="edit-and-audit-order-transactions"></a>Tilaustapahtumien muokkaaminen ja tarkistaminen

Voit muokata ja tarkistaa Commerce headquarters ‑sovelluksen tapahtumia seuraamalla alla olevia ohjeita.

1. Asenna [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Määritä **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Commercen parametrit** -sivun **Tilauksen synkronointivirheiden estokoodi** -kohdassa estokoodi.
2. Keskeytä muut tilausten synkronointityöt, jotka ovat ristiriidassa muokkauksen ja seurannan ajoituksen kanssa.
3. Avaa **Myymälän myyntitiedot** -työtila. **Online-tilauksen synkronointivirheet**- ja **Asiakastilauksen synkronointivirheet** ‑ruuduissa on vähittäismyyntitapahtuman sivun esisuodatettu näkymä. Ne näyttävät tapahtumatietueet, joiden vastaavan tilaustyypin synkronointi epäonnistui.
4. Avaa **Online-tilauksen synkronointivirheet**- tai **Asiakastilauksen synkronointivirheet** -sivu. Valitse tietue, jonka synkronointivirheen tietoja haluat tarkastella. **Synkronoinnin tila** -pikavälilehdessä ovat seuraavat virhetiedot:

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
    > [!NOTE]
    > Jos muokattavaa kenttää ei löydy, lisää puuttuva kenttä laskentataulukkoon noudattamalla seuraavia ohjeita.
    >   1. Valitse tietoyhdistimessä **Rakenne**.
    >   1. Valitse kynäkuvake sen taulun vieressä, johon haluat lisätä kentän.
    >   1. Valitse kenttä **Käytettävissä olevat kentät** ‑osassa ja valitse sitten **Lisää**.
    >   1. Lisää tarvittava määrä kenttiä ja valitse sitten **Päivitä**.
    >   1. Kun päivitys on valmis, sinun tarvitsee ehkä päivittää arvot valitsemalla **Päivitä**.

3. Voit tarkastella muutosten täydellistä seurantaketjua valitsemalla otsikkotason muutoksille **Näytä seurantaketju** ‑kohdan **Vähittäismyyntitapahtuma**-otsikossa soveltuvan tapahtumasivun osassa ja tietueessa. Esimerkiksi kaikki myyntiriveihin liittyvät muutokset näkyvät **Myyntitapahtumat**-sivulla ja maksuihin liittyvät muutokset **Maksutapahtumat**-sivulla. Seuraavia tarkistustietoja muutetaan:

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
