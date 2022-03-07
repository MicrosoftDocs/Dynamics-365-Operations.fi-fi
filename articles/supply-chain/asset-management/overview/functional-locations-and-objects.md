---
title: Toiminnalliset sijainnit ja resurssit
description: Tässä ohjeaiheessa kerrotaan toiminnallisista sijainneista ja resursseista resurssien hallinnassa. Resurssien hallinta on kehittynyt moduuli resurssien ja kunnossapitotöiden hallintaan Dynamics 365 Supply Chain Managementissa.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0bf90d99a8bd093817f9e804e8075e779428f1fadb3128c5a455ca839dece55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750145"
---
# <a name="functional-locations-and-assets"></a>Toiminnalliset sijainnit ja resurssit

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan toiminnallisista sijainneista ja resursseista resurssien hallinnassa. Resurssien hallinta on kehittynyt moduuli resurssien ja kunnossapitotöiden hallintaan Dynamics 365 Supply Chain Managementissa.

## <a name="overview"></a>Yleiskuvaus

Resurssien hallinta on integroitu saumattomasti useisiin moduuleihin muiden Finance and Operations -sovellusten kanssa. Seuraavassa kuvassa näkyvät liittymät muiden moduulien kanssa.

![Kaavio, jossa näkyvät resurssienhallinnan rajapinnat muihin moduuleihin.](media/01-overview-image.png)

Resurssien hallinnan avulla voit tehokkaasti hallita ja suorittaa kaikkia tehtäviä, jotka liittyvät yrityksen monentyyppisten laitteiden hallintaan ja huoltoon. Näihin laitteisiin kuuluvat koneet, tuotantolaitteet ja ajoneuvot. Resurssien hallinta tukee myös ratkaisuja monilla eri aloilla.

Seuraavassa kuvassa on yleiskuvaus päätoiminnoista, jotka kuuluvat resurssien hallintaan.

![Kaavio, jossa näkyy resurssienhallinnan päätoiminto.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Toiminnalliset sijainnit ja resurssit

Toiminnallisia sijainteja käytetään resurssien hallintaan sijainneissa. Tämä hallinta sisältää resurssien kustannusten seurannan toiminnallisissa sijainneissa. Toiminnalliset sijainnit on jäsennelty hierarkkisesti, ja sijainneissa voi olla alisijainteja. Toiminnallisten sijaintien rakenne on staattinen. Toisin sanoen sijainnit eivät voi muuttaa paikkaa. Resurssit voidaan asentaa toiminnallisiin sijainteihin, ja ne voidaan tarvittaessa asentaa muihin toiminnallisiin sijainteihin myöhemmin.

Resurssien kustannukset noudattavat aina resurssin sijaintia. Toisin sanoen, jos asennat resurssin uuteen toiminnalliseen sijaintiin, resurssi käyttää automaattisesti taloushallinnon dimensioita, jotka liittyvät uuteen toiminnalliseen sijaintiin. Tämän vuoksi resurssien kustannukset liittyvät aina siihen toiminnalliseen sijaintiin, johon resurssi on tällä hetkellä asennettu. Tämä taloushallinnon dimensioiden automaattinen käsittely auttaa takaamaan kustannusten täydellisen seurannan, kun yrityksesi tekee projektien hallinnan ja raportoinnin toiminnallisista sijainneista.

Toiminnallisten sijaintien hierarkian koontitapa riippuu yrityksesi vaatimuksista, jotka koskevat sisäisten laitteiden ylläpitoa tai asiakaslaitteiden huoltoa. Seuraavassa kuvassa on esimerkki toiminnallisista sijainneista, jotka perustuvat maantieteellisiin sijainteihin.

![Kaavio, jossa näkyy toiminnallisia sijainteja maantieteellisten sijaintien perusteella.](media/03-overview-image.png)

Seuraavassa kuvassa on esimerkki toiminnallisista sijainneista, jotka perustuvat asiakkaisiin.

![Kaavio, jossa näkyy toiminnallisia sijainteja asiakkaiden perusteella.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]