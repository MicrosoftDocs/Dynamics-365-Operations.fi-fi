---
title: Suodattimien käyttäminen suunnitelmaan
description: Tässä ohjeaiheessa käsitellään suodattimien käyttöä suunnitelmassa suunnittelun optimointitoimintoa käytettäessä.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 73e4a045ff5a9912b898a7115d3d8f530846ebdd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209786"
---
# <a name="apply-filters-to-a-plan"></a>Suodattimien käyttäminen suunnitelmaan

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Kun suunnittelun optimointitoimintoa käytetään, voit käyttää suunnitelmassa suodatinta. **Suunnitelma**n suodatinta käytetään aina pääsuunnitteluajon aikana. **Suunnitelman suodattimella** voi rajoittaa suunnitelman kätevästi tiettyyn nimikeryhmään ja varmistaa, ettei muita nimikkeitä sisällytetä tuloksena olevaan pääsuunnitteluun.

Jos **suunnitelman suodatinta** käytetään ja jos pääsuunnitteluajon aikana käytetään myös suorituksenaikaista suodatinta, suunnitteluajossa otetaan huomioon vain kahden suodattimen leikkauskohta.

**Suunnitelman suodatinta** voi käyttää **pääsuunnitelmista**, kun suunnittelun optimointia käytetään.

## <a name="example-scenario"></a>Esimerkkiskenaario

Määritettävä suunnitelman suodatin sisältää nimekkeet A, B ja C. Samalla suunnitelmalle suoritetaan sitten pääsuunnitteluajoja niin, että käytössä on erilaiset suorituksenaikaiset suorittimet:

- **Suorituksenaikainen suodatin, joka sisältää nimikkeen D**: nimikkeitä ei suunnitella, koska suunnitelman suodattimen ja suorituksenaikaisen suodattimen välillä ei ole leikkauskohtaa.
- **Suorituksenaikainen suodatin, joka sisältää nimikkeen A ja D**: vain nimike A sisältyy suunnitteluajoon, koska nimike D ei sisälly suunnitelman suodattimeen.
- **Suorituksenaikainen suodatin, joka sisältää nimikkeen B**: vain nimike B sisältyy suunnitteluajoon ja nimikkeen A edellinen suunnittelutulos säilytetään.
- **Suorituksenaikainen suodatin, joka sisältää kaikki nimikkeet (tyhjä suodatin)**: nimikkeet A, B ja C sisältyvät suunnitteluajoon ja nimikkeiden A ja B edelliset suunnittelutulokset korvataan.

> [!NOTE]
> Suunnitelman suodattimen määrittämistä kannattaa välttää, jos suunnitelma on valittu **Pääsuunnittelun parametrit** -sivulla **nykyiseksi dynaamiseksi pääsuunnitelmaksi**. Muussa tapauksessa dynaaminen pääsuunnitelmattoiminto rajoittuu suodatettuihin nimikkeisiin. Jos esimerkiksi nettotarpeet päivitetään nimikkeelle, joka ei sisälly suunnitelman suodattimeen, tulosta ei muodostu.

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)
