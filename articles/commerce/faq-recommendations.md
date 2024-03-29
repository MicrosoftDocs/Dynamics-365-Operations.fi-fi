---
title: Tuotesuositukset – usein kysytyt kysymykset
description: Tässä artikkelissa on tietoja prosesseista ja työkaluista, joiden avulla voit tehdä tuotesuosituksiin tai niiden tuloksiin liittyvien ongelmien vianmäärityksen.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 77a5532ab1ae3b630bb335aa7cff6dc747184994
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900444"
---
# <a name="product-recommendations-faq"></a>Tuotesuositukset – usein kysytyt kysymykset


[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja prosesseista ja työkaluista, joiden avulla voit tehdä [tuotesuosituksiin](product-recommendations.md) tai niiden tuloksiin liittyvien ongelmien vianmäärityksen.

## <a name="best-practices"></a>Parhaat käytännöt
On erittäin tärkeää käyttää päätuote- ja tuotevariantti-käsitteitä. Päätuotteen päätason varianttien järkevä ryhmittely auttaa algoritmien ja palvelun luetteloinnissa ja parempien mallien luomisessa. Lisäksi palvelua voi käyttää vain yhdessä tuotteessa sen sijaan, että kaikki toisiinsa läheisesti liittyvät variantit kuuluisivat luetteloon. Kun kaikki toisiinsa läheisesti liittyvät variantit asetetaan luetteloon, saattaa tapahtua virheitä tai tuloksissa voi olla kaksoiskappaleita.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Miksi suositusluetteloista puuttuu tuotteita?

Jos tuotesuositusluettelosta puuttuu nimike, kyseessä voi olla tuotteen määritysongelma. Esimerkiksi tuotteen alkamis- tai päättymispäivämäärä voi olla virheellinen, dimensio saattaa olla väärin määritetty tai tuote ei ehkä ole oikeassa kanavavalikoimassa.

Jos nimike puuttuu tekoälyn koneoppimiseen perustuvasta suositusluettelosta, nimike ei ehkä vastaa suositusluettelon ehtoja tai sillä ei ole tarpeeksi ostotapahtumia, jotta suositusluettelo voisi näyttää sen.

Suosittelemme, että tarkistat seuraavat vaiheet:
1. **Varmista, että tuotesuositukset on otettu käyttöön HQ:ssa.** Lisätietoja tämän palvelun käyttöönottamisesta on kohdassa [Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md).
1. **Varmista, että tärkeimmät tuoteominaisuudet on määritetty.** Esimerkiksi tuotevalikoimien arvoksi on määritettävä **Sisältyy**.
1. **Juuri lajiteltujen tuotteiden näkyminen luettelossa voi kestää jopa 3 tuntia.**
1. **Jos tuote ei vieläkään näy Suositut-, Myydyimmät-, Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luetteloissa, tuotteella ei ehkä ole riittävästi tapahtumia.** Tässä tapauksessa voit odottaa, että tuotteella on enemmän tapahtumia, päivittää oletussuositusluettelon parametrit tai muokata suositustuoteluettelon tuloksia manuaalisesti. Lisätietoja suositusparametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).
1. **Varmista, että tuote täyttää luettelon suositusehdot.** Lisätietoja tuotesuositusten parametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Miten voin estää huonojen suositustulosten palauttamisen?

Suositusluettelot vaativat suuren määrän tapahtumia, jotta tuloksia saadaan. Siksi on tärkeää, että käyttäjät antavat kaikki aiemmat tapahtumatiedot.

Lisäksi tuotteilla, joilla ei ole tapahtumia tai jolla on vain vähän tapahtumia, ei yleensä ole **Ihmiset pitävät myös**- tai **Ostetaan usein yhdessä** -tuloksia eivätkä ne näy **Suositut**- tai **Myydyimmät**-suositusluetteloissa. Tämä voi tapahtua usein aivan uusille tuotteille tai vanhoille tuotteille, joita ei osteta paljon. Tämä ongelma ratkeaa helposti suosittujen uusien nimikkeiden kohdalla.

Suosittelemme, että teet seuraavat vaiheet:
1. **Varmista, että tuote täyttää kyseisen luettelon suositusehdot.** Lisätietoja tuotesuositusten parametreista on kohdassa Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten muokkaaminen.
1. **Jos tuote on uusi, muokkaa suositusluetteloa, kunnes tuotteella on lisää tapahtumia.** Lisätietoja suositusluettelon muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).


- **Varmista, että tuote täyttää kyseisen luettelon suositusehdot.** Lisätietoja tuotesuositusten parametreista on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).
- **Jos tuote on uusi, muokkaa suositusluetteloa, kunnes tuotteella on lisää tapahtumia**. Lisätietoja suositusluettelon muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Voinko poistaa tuotteen, mutta silti nähdä sen myymälässä?

Voit tarvittaessa muokata luetteloita, jotka on luotu algoritmien avulla. Jos tuote poistetaan suositusluettelosta, se löytyy yhä myymälästä. Lisätietoja tuotesuositusten tulosten muokkaamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvien tuotesuositusten tulosten hallinta](modify-product-recommendation-results.md).

Jos haluat estää nimikkeen löytymisen myymälästä, muuta **Nimikelajitelma**-kohdan arvoksi **Sulje pois**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Miten voin lisätä luettelon sähköisen kaupankäynnin sivulle?

Lisätietoja tuotesuositussivujen lisäämisestä sähköisen kaupankäynnin sivustoon on kohdassa [Tuotesuositusluetteloiden lisääminen sivuille](./product-recommendations.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Miten otan käyttöön suositukset myyntipisteellä?

Kun olet ottanut käyttöön tuotesuositukset, sinun on lisättävä suositusten paneeli ohjausobjektin myyntipistenäyttöön. Lisätietoja on kohdassa [Suositusten ohjausobjektin lisääminen tapahtumanäyttöön myyntipistelaitteissa](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]