---
title: Konsernin sisäisten hintojen ja alennusten synkronointi
description: Tässä aiheessa käsitellään konsernin sisäisten myynti- ja ostotilausten hintojen ja alennusten synkronointia
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 90fa2244b5947c37b8498d1c70cddf894979f931
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673631"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Konsernin sisäisten hintojen ja alennusten synkronointi

[!include [banner](../../includes/banner.md)]

Alennukset ja hinnat synkronoidaan konsernin sisäisten myyntitilausten ja konsernin sisäisten ostotilausten kesken. Hinnat ja alennukset voidaan synkronoida myös alkuperäiseen myyntitilaukseen nähden, jolloin kaikissa tilauksissa on samat hinnat ja alennukset. Se tehdään **Konsernin sisäinen** -sivulla, joka avataan **Kaikki asiakkaat** -luettelosivun **Yleiset**-välilehdeltä. Kyseessä on joko **Myynti ja markkinointi** tai **Hankinta**.

**Hinta ja alennus** -kenttä synkronoidaan konsernin sisäisen myyntitilausrivin kanssa. Tämä tarkoittaa, että jos **Salli hinnan muokkaus**- ja **Salli alennuksen muokkaus** kenttä valitaan, konsernin sisäisen myyntitilauksen ja konsernin sisäisen ostotilauksen välinen muutos sallitaan. Konsernin sisäisen myyntitilauksen yksikköhinnan, hintayksikön tai myyntikulun muuttaminen määrittää konsernin sisäisen ostotilausrivin hinnan.

Jos **Salli hinnan muutos**- ja **Salli alennuksen muutos** -kentät on otettu käyttöön konsernin sisäisessä myyntitilauksessa tai konsernin sisäisessä ostotilauksessa, hinnan tai alennuksen voi muuttaa manuaalisesti jommassakummassa tilauksessa. Muussa tapauksessa se ei ole mahdollista.

Jos **Salli hinnan muutos**- ja **Salli alennuksen muutos** -kenttiä ei ole otettu käyttöön konsernin sisäisessä myyntitilauksessa, hintaan (tai kuluihin) tai alennukseen ei voi tehdä muutoksia manuaalisesti konsernin sisäisessä myyntitilauksessa.

Jos **Salli hinnan muutos**- ja **Salli alennuksen muutos** -kenttiä ei ole otettu käyttöön konsernin sisäisessä ostotilauksessa, hintaan (tai kuluihin) tai alennukseen ei voi tehdä muutoksia manuaalisesti konsernin sisäisessä ostotilauksessa.

Jos **Salli hinnan muutos**- ja **Salli alennuksen muutos** -kentät on otettu käyttöön sekä konsernin sisäisessä ostotilauksessa että konsernin sisäisessä myyntitilauksessa, manuaalisia muutoksia voi tehdä molempiin tilauksiin. Tämä voi kuitenkin aiheuttaa tilanteen, jossa yhden henkilön tekemät päivitykset korvataan toisen henkilön toisessa yrityksessä samaan tilaukseen tekemillä päivityksillä.

> [!NOTE]
> Jos **Hinta ja alennus** -kenttä on valittu sekä konsernin sisäisessä ostotilauksessa että konsernin sisäisessä myyntitilauksessa, käyttäjä ei voi hallita hinnoittelua.

Tällaiset ristiriidat voidaan välttää parhaiten, kun hintojen ja alennusten muuttaminen sallitaan vain joko konsernin sisäisessä myyntitilauksessa tai konsernin sisäisessä ostotilauksessa. Se tehdään ottamalla **Salli hinnan muokkaus**- ja **Salli alennuksen muokkaus** -kentät käyttöön jommassakummassa tilauksessa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
