---
title: Suunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön peruuttamista.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076342"
---
# <a name="cancel-a-planning-job"></a>Suunnittelutyön peruuttaminen

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

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
