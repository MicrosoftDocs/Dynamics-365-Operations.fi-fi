---
title: Kuormien suunnittelu keskusten konsolidoinnin avulla – yleiskatsaus
description: Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon.
author: MarkusFogelberg
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0e7ae8db62ce374b991ac5f117e3d1d33534df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828463"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Kuormien suunnittelu keskusten konsolidoinnin avulla – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon.

Lähetykset kannattaa ehkä konsolidoida keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun useat toimittajat toimittavat hyödykkeitä samaan varastoon.

## <a name="building-loads"></a>Kuormien muodostaminen
Ennen konsolidointia keskukseen **Kuljetussuunnittelu**-vaihtoehto on otettava käyttöön **Kuljetustenhallintaparametrit**-sivulla. Sinun on myös luotava keskukset, joissa konsolidointi tapahtuu. Seuraavassa kaaviossa on esimerkki konsolidoinnista keskukseen. Tässä tapauksessa eri varastoista tulevilla myyntitilauksilla on sama asiakas. Peruskuormat luodaan myyntitilausten perusteella tavalliseen tapaan **Kuormasuunnittelun työtila** -sivulla. Voit konsolidoida kaksi kuormaa keskuksessa ennen niiden toimittamista asiakkaalle valitsemalla **Kuormasuunnittelun työtila** -sivun **Kuljetus**-kentässä **Keskusten konsolidointi**. Kun valitset kullekin kuormalle oikean keskuksen, keskus on kuormien jättökohde. Lisäksi **Kuormasuunnittelun työtila** -sivun **Tarjonta ja kysyntä** -osassa on kaksi kuljetuspyynnön riviä. Voit sitten lisätä nämä kaksi riviä uuteen kuormaan. Tässä uudessa kuormassa on molemmat myyntitilausrivit. Lisäksi keskus on keräilyosoitteena ja asiakas A jättökohteena. Kolme kuormaa ovat sitten valmiita hinnoittelua ja reititystä varten muiden kuormien tavoin. Voit valita kullekin kuormalle järjestelmän ehdottaman lähetyksen rahdinkuljettajan. [![Keskusten konsolidointi](./media/hubconsol.jpg)](./media/hubconsol.jpg) Voit konsolidoida kuormia samalla menetelmällä useille siirtotilauksille. Tässä tapauksessa edellisen kaavion asiakas A on varasto. Voit vaihtoehtoisesti konsolidoida useiden ostotilausten kuormat tilanteessa, jossa eri toimittajat toimittavat kuormat samaan varastoon. Sinulla on useita konsolidointikeskuksia ja voit konsolidoida eri varastoita tulevia kuormia useissa keskuksissa. Kun olet muodostanut peruskuormat ja käytät keskuksen konsolidointiasetusta, voit muodostaa uusia kuormia konsolidoimalla kuljetuspyynnön rivit. Voit sitten hinnoitella ja reitittää kuormat.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]