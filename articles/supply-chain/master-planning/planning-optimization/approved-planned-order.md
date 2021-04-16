---
title: Hyväksy suunnitellut tilaukset
description: Tässä ohjeaiheessa kuvataan suunnittelun optimoinnin tukemien suunniteltujen tilausten hyväksyntä.
author: ChristianRytt
ms.date: 08/21/2020
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
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825888"
---
# <a name="approve-planned-orders"></a>Hyväksy suunnitellut tilaukset

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tilan päivittämisestä.

Huomaa, että suunniteltujen tilausten hyväksyminen on valinnainen vaihe. Se tehdään luotaessa vahvistettu tilaus suunnitellusta tilauksesta. On suositeltavaa hyväksyä muutetut suunnitellut tilaukset. Muussa tapauksessa muokkaukset ohitetaan, ja seuraava suunnittelun suoritus korvaa ne.

![Suunniteltu tilausten työnkulku](media/approved-planned-orders-1.png)

**Tila**-kentän avulla voit seurata edistymistä käyttämällä seuraavia arvoja:

- **Käsittelemätön:** Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on *Käsittelemätön*. Tässä tilassa olevat suunnitellut tilaukset poistetaan seuraavan suunnittelun suorittamisen aikana.
- **Valmis:** Jos päätät olla vahvistamatta suunniteltua tilausta, voit muuttaa tilaksi *Valmis*. Näin osoitat, että tämän suunnitellun tilauksen arvioiminen on tehty. Huomaa, että *Käsittelemätön*- ja *Valmis*-tiloja käsitellään järjestelmässä samalla tavalla.
- **Hyväksytty:** Jos haluat säilyttää muokkaukset tai suunnittelet suunnitellun tilauksen vahvistamista, muuta tilaksi *Hyväksytty*. Suunniteltuja tilauksia, joiden tila on *Hyväksytty*, pidetään valmiina. Niiden toimitusta odotetaan pääsuunnittelussa. Niitä ei muokata tai poisteta myöhemmin pääsuunnittelun suorituksissa. Tämän saavuttamiseksi suunnittelulogiikka kopioi *hyväksytyt* suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana. Huomaa, että *hyväksyttyjä* suunniteltuja tilauksia pidetään tarjontana vain tietyssä pääsuunnitelmassa.

Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luetteloissa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]