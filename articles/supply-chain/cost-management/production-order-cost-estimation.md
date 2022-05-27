---
title: Tuotantotilauksen kustannusarvio
description: Tämä artikkeli sisältää tietoja tuotannon kustannusarviosta. Tuotannon kustannusarvio sisältää arvioidut materiaalin ja kapasiteetin kulutuksesta aiheutuneet kustannukset, jotka syntyvät kun nimikettä tuotetaan suunniteltu tuotantotilausmäärä.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac658b49109a3fb3f987cf30bfa0b62bbff3d1c2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672259"
---
# <a name="production-order-cost-estimation"></a>Tuotantotilauksen kustannusarvio

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää tietoja tuotannon kustannusarviosta. Tuotannon kustannusarvio sisältää arvioidut materiaalin ja kapasiteetin kulutuksesta aiheutuneet kustannukset, jotka syntyvät kun nimikettä tuotetaan suunniteltu tuotantotilausmäärä. 

Tuotantokustannukset on arvioitava tuotantotilauksen luomisen jälkeen. Tarkoitus on arvioida tuotantoprosessin nimikkeen ja reitityksen kulutus, koska nämä arviot muodostavat perustan seuraaville ajoitus- ja tuotantoprosesseille.

## <a name="production-cost-estimation"></a>Tuotannon kustannusarvio
Tuotantokustannusten arviot perustuvat seuraaviin tietoihin:

-   tuotantotilauksen määrä
-   tuotannon tuoterakenteiden komponentit
-   tuotantoreitityksen reititystyövaiheet
-   komponenttien ja työvaiheiden epäsuorat kustannukset
-   aktiivisten kustannusten tiedot laskentapäivän mukaan.

Jos tuotannon tuoterakenteissa on haamurivin nimike, laskelmat ovat haamun komponenttien ja reititystyövaiheiden mukaisia. Arviointitehtävää voi käyttää laskettaessa arvioidut kustannukset uudelleen niin, että ne vastaavat päivitettyjä tietoja. Päivitetyt tiedot voivat olla esimerkiksi muutoksia tuotantotilauksen määrässä, tuotannon tuoterakenteiden komponenteissa, tuotantoreitityksen reititystyövaiheissa, näitä komponentteja ja työvaiheita koskevissa epäsuorissa kustannuksissa tai laskentapäivämäärän mukaisissa aktiivisten kustannusten tiedoissa. Arvioitujen kustannusten laskelmat ehdottavat myös tuotantonimikkeelle myyntihintaa, joka perustuu hinta+hinnankorotus-malliin. Arvioitujen kustannusten laskelmat voivat koskea vaihtoehtoisesti myös viitetilauksia, jotka vastaavat tuotantotilaukseen linkitettyjä muita tuotantotilauksia.

## <a name="view-the-estimated-costs"></a>Arvioitujen kustannusten tarkasteleminen
Kun arviointi on suoritettu, tulokset näkyvät **Hinnan laskenta** -sivulla. Arviointi laskee seuraavat arvot:

-   **Tuotantokustannukset** – Tuotantokustannukset ovat arvion ylimmällä rivillä. Rivillä näkyvät kaikki tuotantotilauksen suorittamisesta aiheutuvat kustannukset sekä tuotannon kokonaismyyntihinta. Tuotantokustannukset ovat arvion kaikkien kustannusrivien summa.
-   **Reitti- tai resurssikustannukset** – Reitti- tai resurssikustannukset ovat tuotannon työvaiheiden kustannuksia. Ne sisältävät kustannuksia elementeistä, kuten asetusajasta, ajoajasta ja yleiskustannuksista.
-   **Materiaalikustannukset** – Materiaalikustannukset ovat nimikkeen tuottamisessa tarvittavien tuoterakennekomponenttien kustannuksia ja hintoja. Nämä kustannukset on määritetty aiemmin järjestelmään.

## <a name="other-uses-of-cost-estimation"></a>Kustannusarvion muita käyttökohteita
Kustannusarvio sisältää myös seuraavat tiedot:

-   järkevät hintatarjoukset
-   tilauksen kannattavuuden arviointi
-   raaka-aineiden käytön arviointi
-   aikaisempien tuotantojen kustannustietojen vertailu
-   budjetti- ja ennustetiedot
-   tietyn kustannustason ylläpitämiseen tarvittavien tuotantokokojen arviointi.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]