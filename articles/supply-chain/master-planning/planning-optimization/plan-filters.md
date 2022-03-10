---
title: Suodattimien käyttäminen suunnitelmaan
description: Tässä ohjeaiheessa käsitellään suodattimien käyttöä suunnitelmassa suunnittelun optimointitoimintoa käytettäessä.
author: ChristianRytt
ms.date: 01/08/2020
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
ms.openlocfilehash: 3612dd45a3f4b8c3597c81962a66c21ed14fb206
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729024"
---
# <a name="apply-filters-to-a-plan"></a>Suodattimien käyttäminen suunnitelmaan

[!include [banner](../../includes/banner.md)]

Kun suunnittelun optimointitoimintoa käytetään, voit käyttää suunnitelmassa suodatinta. **Suunnitelma** n suodatinta käytetään aina pääsuunnitteluajon aikana. **Suunnitelman suodattimella** voi rajoittaa suunnitelman kätevästi tiettyyn nimikeryhmään ja varmistaa, ettei muita nimikkeitä sisällytetä tuloksena olevaan pääsuunnitteluun.

Jos **suunnitelman suodatinta** käytetään ja jos pääsuunnitteluajon aikana käytetään myös suorituksenaikaista suodatinta, suunnitteluajossa otetaan huomioon vain kahden suodattimen leikkauskohta.

**Suunnitelman suodatinta** voi käyttää **pääsuunnitelmista**, kun suunnittelun optimointia käytetään.

## <a name="example-scenario"></a>Esimerkkiskenaario

Määritettävä suunnitelman suodatin sisältää nimekkeet A, B ja C. Samalla suunnitelmalle suoritetaan sitten pääsuunnitteluajoja niin, että käytössä on erilaiset suorituksenaikaiset suorittimet:

- **Suorituksenaikainen suodatin, joka sisältää nimikkeen D**: nimikkeitä ei suunnitella, koska suunnitelman suodattimen ja suorituksenaikaisen suodattimen välillä ei ole leikkauskohtaa.
- **Suorituksenaikainen suodatin, joka sisältää nimikkeen A ja D**: vain nimike A sisältyy suunnitteluajoon, koska nimike D ei sisälly suunnitelman suodattimeen.
- **Suorituksenaikainen suodatin, joka sisältää nimikkeen B**: vain nimike B sisältyy suunnitteluajoon ja nimikkeen A edellinen suunnittelutulos säilytetään.
- **Suorituksenaikainen suodatin, joka sisältää kaikki nimikkeet (tyhjä suodatin)**: nimikkeet A, B ja C sisältyvät suunnitteluajoon ja nimikkeiden A ja B edelliset suunnittelutulokset korvataan.

> [!NOTE]
> Jos suunnitelman suodatin määritetään suunnitelmassa, joka on valittu **nykyiseksi dynaamiseksi pääsuunnitelmaksi** **Pääsuunnittelun parametrit** -sivulla, dynaamisen pääsuunnittelun toiminnot rajoittuvat suodatettuihin nimikkeisiin. Jos esimerkiksi nettotarpeet päivitetään nimikkeelle, joka ei sisälly suunnitelman suodattimeen, tulosta ei muodostu.

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
