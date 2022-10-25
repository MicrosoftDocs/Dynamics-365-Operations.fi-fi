---
title: Asiakkaiden toimintojen synkronointi headquartersissa
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce headquartersin asiakkaiden toimintojen synkronoinnin tarkistaminen auttaa sivuston käyttäjien mahdollisten ongelmien ratkaisemisessa.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691065"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Asiakkaiden toimintojen synkronointi headquartersissa

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce headquartersin asiakkaiden toimintojen synkronoinnin tarkistaminen auttaa sivuston käyttäjien mahdollisten ongelmien ratkaisemisessa.

Kun organisaatiot ottavat käyttöön mahdollisuuden luoda ja muokata asiakkaiden tietoja asynkronisesti, sivustojen järjestelmänvalvojille on annettava oikeus tarkastella toimintoja ja tehdä niiden vianmäärityksiä sivuston käyttäjien pyyntöjen ja käsittelyvirheiden perusteella. Näissä skenaarioissa sivustojen järjestelmänvalvojien on tarkistettava asiakkaiden luomista ja muokattava toimintoja sekä korjattava mahdollisia virheitä itsepalvelumallin avulla.

## <a name="customer-synchronization-status"></a>Asiakkaan synkronoinnin tila

Kun asiakkaiden hallinnassa otetaan käyttöön asynkroninen tila ja sen vastaavat ominaisuudet, Commerce headquartersin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi. Asiakkaiden hallinnan toimintojen synkronointi tapahtuu, kun nämä työt suoritetaan. Lisätietoja on kohdassa [Asynkroninen asiakkaan luontitila](async-customer-mode.md).

Yrityksen omistaja voi suorittaa seuraavat toiminnot:

- Tarkastele sivuston käyttäjien kaikkia luonti-/muokkaustoimintoja. Tietoja ovat esimerkiksi tila ja aikaleima.
- Suodata toiminnot käyttämällä mitä tahansa asiakkaan taulukon kenttää ja arvoja valvontalokin tarkentamiseksi.
- Tarkastele muutosten lyhyitä kuvauksia yhdessä tilan tietojen kanssa, kun haluat toiminnoista ylätason tietoja.
- Muokkaa ongelmakenttiä ja korjaa niiden virheet. Tämän jälkeen voit tallentaa ja synkronoida tietyt asiakkaiden toiminnot.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Asiakkaan synkronoinnin tila -sivun elementit

Voit tarkastella kaikkien synkronointitoimintojen luetteloa Commerce headquartersissa siirtymällä kohtaan **Commerce ja Retail \> Asiakkaat \> Asiakkaan synkronoinnin tila**. Seuraavassa kuvassa on **Asiakkaan synkronoinnin tila** -sivun esimerkki.

![Asiakkaan synkronoinnin tila -sivu Commerce headquartersissa.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Oletusarvoisesti asiakkaan synkronointitoimintojen luettelo **Asiakkaan synkronoinnin tila** -sivun vasemmalla puolella sisältää seuraavat sarakkeet:

- Kanavan nimi
- Asiakastili
- Asynkroninen asiakastili
- Toimintojen aikaleima
- Asiakkaan synkronoinnin tila

Sivun oikeapuoleisessa yläkulmassa on asiakastilin tiedot, esimerkiksi **asiakastilin**, **Retail Async -toiminnon**, **asiakkaan synkronoinnin tilan** ja **viimeisimmän tunnetun virheen** arvot.

**Muutoksen kuvaus** -osassa on asiakkaiden hallinnan suoritetun toiminnon tyypin kuvaus (esimerkiksi asiakkaan luonti, tilin päivitys tai synkronointivirhe ja tiedot)

**Asiakkaan määritteet** -osassa on ruudukko, jossa ovat kaikki asiakkaan määritteet sekä vanhat ja uudet arvot. Voit muokata tätä osaa, jos haluat muuttaa asiakkaan määritteen arvoja korjataksesi virheet ja synkronoidaksesi tiedot uudelleen.
