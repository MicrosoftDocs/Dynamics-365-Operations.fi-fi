---
title: Suunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön peruuttamista.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833326"
---
# <a name="cancel-a-planning-job"></a>Suunnittelutyön peruuttaminen

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementissa voi peruuttaa suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön. Kun valitset **Peruuta** valintaikkunassa, kun suunnittelun optimointityö käynnistetään suoraan käyttöliittymästä (eli sitä ei ajeta taustalla), tämä ei peruuta suunnittelun optimointityötä. Vaikka saat varoituksen, kuten Toiminto peruutettu, sinun on silti peruutettava suunnittelutyö suunnittelun optimoinnin avulla seuraavasti.


Aktiivinen suunnittelutyö peruutetaan seuraavien ohjeiden mukaan. 

> [!NOTE]
> Vain aktiiviset työt voidaan peruuttaa.

1. Valitse **Pääsuunnittelu \> Asetukset \> Suunnitelmat**.
2. Valitse suunnitteluajoon sopiva suunnitelma.
3. Valitse **Historia**.
4. Valitse peruutettava suunnittelutyö
5. Valitse **Peruuta**.

Työn tila on **Peruutetaan**, kunnes suunnittelun optimointipalvelu vahvistaa, että työ on peruutettu. Tilaksi vaihdetaan sitten **Peruutettu**.

> [!NOTE]
> Tilan muutokset tulevat näkyviin, kun sivu päivitetään **Päivitä**-painikkeella.

## <a name="additional-resources"></a>Lisäresurssit

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]