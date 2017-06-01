---
title: Suunnittele kuormia keskusten konsolidoinnilla
description: "Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e0bd837a441a17e53982d5c5a7a7983f40e471c5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="plan-loads-using-hub-consolidation"></a>Suunnittele kuormia keskusten konsolidoinnilla

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon.

Lähetykset kannattaa ehkä konsolidoida keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun useat toimittajat toimittavat hyödykkeitä samaan varastoon.

## <a name="building-loads"></a>Kuormien muodostaminen
Ennen konsolidointia keskukseen **Kuljetussuunnittelu**-vaihtoehto on otettava käyttöön **Kuljetustenhallintaparametrit**-sivulla. Sinun on myös luotava keskukset, joissa konsolidointi tapahtuu. Seuraavassa kaaviossa on esimerkki konsolidoinnista keskukseen. Tässä tapauksessa eri varastoista tulevilla myyntitilauksilla on sama asiakas. Peruskuormat luodaan myyntitilausten perusteella tavalliseen tapaan **Kuormasuunnittelun työtila** -sivulla. Voit konsolidoida kaksi kuormaa keskuksessa ennen niiden toimittamista asiakkaalle valitsemalla **Kuormasuunnittelun työtila** -sivun **Kuljetus**-kentässä **Keskusten konsolidointi**. Kun valitset kullekin kuormalle oikean keskuksen, keskus on kuormien jättökohde. Lisäksi **Kuormasuunnittelun työtila** -sivun **Tarjonta ja kysyntä** -osassa on kaksi kuljetuspyynnön riviä. Voit sitten lisätä nämä kaksi riviä uuteen kuormaan. Tässä uudessa kuormassa on molemmat myyntitilausrivit. Lisäksi keskus on keräilyosoitteena ja asiakas A jättökohteena. Kolme kuormaa ovat sitten valmiita hinnoittelua ja reititystä varten muiden kuormien tavoin. Voit valita kullekin kuormalle järjestelmän ehdottaman lähetyksen rahdinkuljettajan. [![Keskusten konsolidointi](./media/hubconsol.jpg)](./media/hubconsol.jpg) Voit konsolidoida kuormia samalla menetelmällä useille siirtotilauksille. Tässä tapauksessa edellisen kaavion asiakas A on varasto. Voit vaihtoehtoisesti konsolidoida useiden ostotilausten kuormat tilanteessa, jossa eri toimittajat toimittavat kuormat samaan varastoon. Sinulla on useita konsolidointikeskuksia ja voit konsolidoida eri varastoita tulevia kuormia useissa keskuksissa. Kun olet muodostanut peruskuormat ja käytät keskuksen konsolidointiasetusta, voit muodostaa uusia kuormia konsolidoimalla kuljetuspyynnön rivit. Voit sitten hinnoitella ja reitittää kuormat.




