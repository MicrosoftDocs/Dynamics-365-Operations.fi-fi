---
title: Tuoterakenneversion hajottaminen
description: Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbdfc169365cb73e13383b11efcd8983aef4bbca
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815315"
---
# <a name="explosion-of-a-bom-version"></a>Tuoterakenneversion hajottaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.

Tuoterakenneversion kysynnän hajotus luo kysynnän kullekin tuoterakennerivin nimikkeelle määritetyssä toimipaikassa ja mahdollisesti tietyssä varastossa. Toimipaikkakohtaisen tuoterakenteen kullekin tuoterakenneriville voidaan määrittää tietty varasto. Lisäksi kunkin tuoterakennerivin nimikkeen dimensioasetukset määrittävät, onko varasto tarpeen. Kunkin tuoterakennerivin nimikkeen tuloksena syntyvä kysyntä muodostaa jatkossa aloituspisteen lisäkysynnän hajotukselle. Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Toimipaikkadimensio on pakollinen ja se on määritettävä tarvetapahtumalle.
-   Toimipaikkadimensio on yhdenmukainen. Näin ollen alemman tason tarpeen toimipaikka on sama kuin alkuperäisen tarvetapahtuman toimipaikka.

Seuraava kuva ilmaisee, miten pääsuunnittelun kysynnän hajotus etenee. ![Kysynnän hajottaminen tuoterakenneversion avulla](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Lisäresurssit
--------

[Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)

[Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)



