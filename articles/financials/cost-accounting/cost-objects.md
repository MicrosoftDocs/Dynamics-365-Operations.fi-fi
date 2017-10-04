---
title: Kustannusobjektin dimensiot
description: "Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde. Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää. Tässä aiheessa on tietoja kustannusobjektin dimensioista."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c121300877c5835bfe023c11040310dcddff052
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="cost-object-dimensions"></a>Kustannusobjektin dimensiot

[!include[banner](../includes/banner.md)]


Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde. Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää. Tässä aiheessa on tietoja kustannusobjektin dimensioista.

Kustannusobjektit ovat mitä tahansa objektityyppejä, joita arvioidaan, mitataan suoraan tai joihin kohdistetaan kustannuksia. Tyypillisiä kustannusobjekteja ovat tuotteet, projektit, resurssit, osastot, kustannuspaikat ja maantieteelliset alueet. Yritysjohto käyttää kustannusobjekteja kustannusten määrittämiseen ja kannattavuusanalyysin tekemiseen.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kustannusobjektin dimensiot ja kustannusobjektin dimension jäsenet
Kustannusobjekteja kutsutaan *kustannusobjektin dimensioiksi*. Kun olet päättänyt, mihin yksikköön kustannusobjektin dimensio viittaa, on annettava yksittäisen dimension arvot tai tuotava ne toisista lähdejärjestelmistä kustannuslaskentaan. Yksittäisten dimensioiden arvoja kutsutaan *kustannusobjektin dimension jäseniksi*. Esimerkiksi haluat käyttää kustannusobjektin dimensiona taloushallinnon dimensiota, jonka nimi on kustannuspaikka. Voidaksesi nähdä, miten kustannukset siirtyvät yksittäisiin kustannuspaikkoihin, sinun on tuotava kustannusobjektin dimensiojäsenet. Tällöin kustannusobjektin dimensiojäsenet ovat todellisia kustannuspaikkoja, kuten myynti, tuotanto, hallinto, maantieteellinen sijainti. Seuraavassa kuvankaappauksessa on esimerkki kustannuspaikoista kustannusobjektin dimensioina ja todellisista kustannuspaikoista kustannusobjektidimension jäseninä. 

[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kustannusobjektin dimension jäsenten tuominen tietoyhdistimillä
Voit helpottaa kustannusobjektin dimensiojäsenten tuontia käyttämällä tietoyhdistimiä, joiden avulla voidaan noutaa arvot yksiköistä, joita haluat käyttää kustannusobjektin dimensioina. Voit käyttää valmiita tietoyhdistimiä tai itse muokattuja tietoyhdistimiä.



