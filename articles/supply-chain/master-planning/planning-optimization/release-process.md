---
title: Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria
description: Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin julkaisuprosessista ja julkaisuhistoriasta.
author: crytt
ms.date: 8/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fcd18341629afcf3092a457ae711e27b0bbfeb2a
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394411"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria

[!include [banner](../../includes/banner.md)]

Microsoft päivittää suunnittelun optimointia kuukausittain. Liiketoimintavaatimusten perusteella ajoitettujen julkaisujen välillä voidaan kuitenkin tehdä lisäpäivityksiä.

Kukin versio julkaistaan yksittäisillä alueilla, joilla suunnittelun optimointi on käytettävissä. Prosessi kestää yleensä kolme päivää.

Suunnittelun optimointia päivitetään, mutta pääsuunnittelu saattaa olla hitaampi kuin tavallisesti.

Ympäristöt, joissa suunnittelu optimointia käytetään, saavat automaattisesti viimeisimmän version. Käyttäjän toimenpiteitä ei tarvita: palvelu päivitetään automaattisesti. Yhtään katkeamistoimintoa ei kuitenkaan aina automaattisesti työnnetä ympäristöihin. Oletusarvon mukaan kaikki katkeamisena pidettävät muutokset on poistettu käytöstä, ja ne on nimenomaisesti otettava käyttöön käyttämällä [ominaisuuksien hallintaa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Muutokset eivät tule näkyviin ympäristöissä, ennen kuin otat muutokset käyttöön.

Koska ilmoitukset eivät näy, kun suunnittelun optimointi päivitetään ympäristössäsi, voit tarkistaa julkaisutiedot seuraavassa taulukossa ja selvittää, milloin muutokset on julkaistu ja mitä toimintoja on otettu käyttöön. Tässä taulukossa näkyvät suunnittelun optimointiin vapautetut muutokset sekä tiedot siitä, liittyvätkö muutokset ominaisuuden hallintaan, ja päivämäärän, jolloin muutokset on tehty.

| Muutokset | Ominaisuuksien hallinnan tiedot | Vapautuspäivä |
|---|---|---|
| <p>Lisättiin **Läpimenoaika**-kenttä suunniteltuihin tilauksiin.</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset.</p> | Ominaisuuksien hallintaa ei tarvita. | 16. elokuuta 2021 |
| <p>Lisättiin rajattoman kapasiteetin ajoituksen resurssityypin vaatimukset.</p><p>Parannettiin rajattoman kapasiteetin ajoituksen resurssin tehokkuutta ja kalenterin tehokkuutta.</p><p>Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md). | <p>Käytettävissä ominaisuuksien hallinnassa versiosta 10.0.20.</p><p>Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus*</p> | 6. heinäkuuta 2021 |
| Yleiset laadun parannukset. | Ominaisuuksien hallintaa ei tarvita. | 6. heinäkuuta 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
