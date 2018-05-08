---
title: "Tilikartan erottimen on oltava yksilöivä"
description: "Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin. Erotinarvot on muutettava päivityksen jälkeen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>Tilikartan erottimen on oltava yksilöivä

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta. Tilikartan ja dimension arvoilla ei voi olla Dynamics 365 for Finance and Operationsissa sama erotin. Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen. 

Ominaisuuden käytettävyys:
- Dynamics 365 for Finance and Operations versio 8.0
- Dynamics 365 for Finance and Operations versio 7.1, KB 4094701 Taloushallinnon dimensioita ei voi kirjata, kun dimension arvot sisältävät tilikartan erottimen
- Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Aliprojekti ei voi valita dimensiona, kun aliprojektin muoto sisältää dimension erottimen

## <a name="update-delimiter"></a>Erottimen päivitys
Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa. Muita dimension erottimia ei voi muuttaa. 
- Voit muuttaa tilikartan erottimen Finance and Operationsiin tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**. 
- Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Erottimen päivitystarpeen määrittäminen ympäristössä 
Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa. Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.

