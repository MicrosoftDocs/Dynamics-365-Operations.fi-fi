---
title: Tilikartan erottimen muuttaminen yksilöiväksi
description: Tässä ohjeaiheessa selitetään, minkä vuoksi tilikartan ja dimension arvoilla ei voi olla sama erotin. Erotinarvot on muutettava päivityksen jälkeen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2622245c7ce7213665ab32f4020c282df28cb886
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248777"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Tilikartan erottimen muuttaminen yksilöiväksi

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta. Tilikartan ja dimension arvoilla ei voi olla Finance and Operationsin nykyisissä versioissa sama erotin. Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen. 

Tämä toiminto ei ole saatavana seuraavissa versioissa:
- Finance and Operations -versio 8.0
- Finance and Operationsin versio 7.1, KB 4094701 Taloushallinnon dimensioita ei voi kirjata, kun dimension arvot sisältävät tilikartan erottimen
- Finance and Operationsin versio 7.2, KB 4092967 Aliprojekti ei voi valita dimensiona, kun aliprojektin muoto sisältää dimension erottimen

## <a name="update-delimiter"></a>Erottimen päivitys
Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa. Muita dimension erottimia ei voi muuttaa. 
- Voit muuttaa tilikartan erottimen tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**. 
- Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Erottimen päivitystarpeen määrittäminen ympäristössä 
Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa. Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.