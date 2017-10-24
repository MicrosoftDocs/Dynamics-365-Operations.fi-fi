---
title: Tuotantotilauksen kustannusarvio
description: "Tämä artikkeli sisältää tietoja tuotannon kustannusarviosta. Tuotannon kustannusarvio sisältää arvioidut materiaalin ja kapasiteetin kulutuksesta aiheutuneet kustannukset, jotka syntyvät kun nimikettä tuotetaan suunniteltu tuotantotilausmäärä."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 172bb55358c20ba80b1c32b05f1ae8e6aff8901f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="production-order-cost-estimation"></a>Tuotantotilauksen kustannusarvio

[!include[banner](../includes/banner.md)]


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





