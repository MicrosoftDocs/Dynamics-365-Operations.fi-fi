---
title: Kustannusobjektin dimensiot
description: Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde. Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää. Tässä aiheessa on tietoja kustannusobjektin dimensioista.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5d91fc52b184fda73fcf36175598aa514945db48
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355128"
---
# <a name="cost-object-dimensions"></a>Kustannusobjektin dimensiot

[!include [banner](../includes/banner.md)]

Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde. Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää. Tässä aiheessa on tietoja kustannusobjektin dimensioista.

Kustannusobjektit ovat mitä tahansa objektityyppejä, joita arvioidaan, mitataan suoraan tai joihin kohdistetaan kustannuksia. Tyypillisiä kustannusobjekteja ovat tuotteet, projektit, resurssit, osastot, kustannuspaikat ja maantieteelliset alueet. Yritysjohto käyttää kustannusobjekteja kustannusten määrittämiseen ja kannattavuusanalyysin tekemiseen.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kustannusobjektin dimensiot ja kustannusobjektin dimension jäsenet
Kustannusobjekteja kutsutaan *kustannusobjektin dimensioiksi*. Kun olet päättänyt, mihin yksikköön kustannusobjektin dimensio viittaa, on annettava yksittäisen dimension arvot tai tuotava ne toisista lähdejärjestelmistä kustannuslaskentaan. Yksittäisten dimensioiden arvoja kutsutaan *kustannusobjektin dimension jäseniksi*. Esimerkiksi haluat käyttää kustannusobjektin dimensiona taloushallinnon dimensiota, jonka nimi on kustannuspaikka. Voidaksesi nähdä, miten kustannukset siirtyvät yksittäisiin kustannuspaikkoihin, sinun on tuotava kustannusobjektin dimensiojäsenet. Tällöin kustannusobjektin dimensiojäsenet ovat todellisia kustannuspaikkoja, kuten myynti, tuotanto, hallinto, maantieteellinen sijainti. Seuraavassa kuvankaappauksessa on esimerkki kustannuspaikoista kustannusobjektin dimensioina ja todellisista kustannuspaikoista kustannusobjektidimension jäseninä. 

[![Näyttökuva, jossa kustannuspaikat näytetään kustannusobjektin dimensiona.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kustannusobjektin dimension jäsenten tuominen tietoyhdistimillä
Voit helpottaa kustannusobjektin dimensiojäsenten tuontia käyttämällä tietoyhdistimiä, joiden avulla voidaan noutaa arvot yksiköistä, joita haluat käyttää kustannusobjektin dimensioina. Voit käyttää valmiita tietoyhdistimiä tai itse muokattuja tietoyhdistimiä.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]