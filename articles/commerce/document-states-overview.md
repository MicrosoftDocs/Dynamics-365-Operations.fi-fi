---
title: Asiakirjan tilat ja elinkaari
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914884"
---
# <a name="document-states-and-lifecycle"></a>Asiakirjan tilat ja elinkaari

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.

## <a name="document-state-descriptions"></a>Asiakirjan tilan kuvaukset

[Sivuelementit](page-elements-overview.md)-ohjeaiheessa on sisällönhallintajärjestelmän (CMS) eri asiakirjatyyppejä. Näillä asiakirjatyypeillä voi olla useita tiloja muokkaustyökalussa. Asiakirjan tilat auttavat estämään tietoristiriitoja ja ottavat käyttöön versionhallinnan. Ne määrittävät, ketkä voivat muuttaa asiakirjoja, milloin asiakirjoja voi muuttaa ja milloin muut voivat tarkastella muutoksia.

Seuraavassa taulukossa esitetään sivuelementtien mahdolliset asiakirjojen tilat Commercessa.

| Asiakirjan tila | Kuvaus |
|---|---|
| Kuitattu ulos | Kun CMS-nimike on kuitattu ulos sinulle, mikään muu todennettu järjestelmäkäyttäjä ei voi muokata sitä. Kaikki nimikkeeseen tekemäsi muutokset näkyvät vain sinulle. |
| Kuitattu sisään | Kun CMS-nimike kuitataan sisään, kaikki muutokset näkyvät muille todennetuille järjestelmäkäyttäjille. Käyttäjät voivat kuitata nimikkeen ulos ja muokata sitä. Jokainen sisäänkuittaus luo asiakirjaversiotietueen nimikkeen historiaan. |
| Julkaistu | Kun CMS-nimike julkaistaan, se siirretään live-sivustoon. Todentamattomat ulkoiset käyttäjät voivat löytää sen verkossa. Nimikkeet voidaan julkaista vain, jos ne on kuitattu sisään. |
| Tallennettu | Uloskuitattuun CMS-nimikkeeseen tehdyt muutokset voidaan tallentaa CMS:ään ennen kuin nimike kuitataan sisään tai julkaistaan. Nämä tallennetut muutokset eivät näy muille todennetuille järjestelmäkäyttäjille ennen kuin nimike kuitataan sisään. Ulkoiset käyttäjät eivät näe niitä, ennen kuin nimike on julkaistu. |
| Hylätty uloskuittaus | Kun uloskuitattu CMS-nimike hylätään, kaikki tallennetut muutokset poistetaan ja nimike palautuu viimeksi sisäänkuitattuun versioon. |

## <a name="additional-resources"></a>Lisäresurssit

[Tapoja lisästä sisältöä](add-manage-content.md)

[Sivumallisanasto](page-elements-overview.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)

[Moduulien käyttäminen](work-with-modules.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Sivuston selauksen mukauttaminen](customize-site-navigation.md)
