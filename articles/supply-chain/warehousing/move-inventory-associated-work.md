---
title: Työhön liitetyn varaston siirtäminen varastonhallinnassa
description: Tässä ohjeaiheessa kerrotaan kappaleen keräilyvahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aee3af8da6610c16fc2d98091bfa3f01f1bd0f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427037"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Työhön liitetyn varaston siirtäminen varastonhallinnassa

[!include [banner](../includes/banner.md)]

Voit päättää varaston siirron avulla, mitä varastotyöntekijät saavat siirtää varattuun varastoon. Tämä parantaa joustavuutta säännellyissä varastoissa, joissa voit olla antamatta työtekijällä mahdollisuuden valita uuden keräilysijainnin aiemmin luodulle keräilytyölle. Sen avulla varastopäälliköt voivat myös hallita, mitä ominaisuuksia kokemattomat työntekijät saavat.

Varastotyöntekijöiden päivittäisten toimenpiteiden hallintaan liittyvästä monipuolisuudesta on hyöytä esimerkiksi seuraavanlaisissa skenaarioissa:

## <a name="scenario-1"></a>Skenaario 1
Yrityksellä on suhteellisen pieni vastaanottoalue ja se on täynnä poispanoa odottavia kuormalavoja ja laatikoita. Suurta lähetystä odotetaan kuluvana päivänä, joten vastaanottotyöntekijä päättää tyhjentää vastaanottoalueen siirtämällä osan kuormalavoista toissijaiselle saapuvien väliaikaiselle varastoalueelle.

## <a name="scenario-2"></a>Skenaario 2
Kokenut varastotyöntekijä huomaa mahdollisuuden konsolidoida nimikkeet varastossa yhteen sijaintiin sen sijaan, että ne jaettaisiin kolmeen läheiseen sijaintiin niin, että kussakin on vähän nimikkeitä. Työntekijä haluaa konsolidoida määrän siirtämällä nimikkeet kustakin näistä sijainneista samaan sijaintiin ja samaan rekisterikilpeen.

## <a name="scenario-3"></a>Skenaario 3
Kuormalava odottaa lähetystä väliaikaisessa sijainnissa, kuten STAGE01, jonka lähellä on BAYDOOR01. Suunnitelmien muutoksen vuoksi kuorma-auto on kuitenkin ajoitettu saapumaan sijaintiin BAYDOOR04. Kuljetustyöntekijä tietää tämän ja hänen on varmistettava, että kuorma-auton ei tarvitse odottaa lastaamista sijainnista STAGE01. Kuljetustyöntekijä päättää siirtää kyseisen lähetyksen nimikkeet sijainnista STAGE01 sijaintiin STAGE04, mikä on lähempänä uutta kohdetta.

### <a name="current-limitations"></a>Nykyiset rajoitukset

Siirrettävät työrajoituksia ovat vain myyntitilaus, siirtotilauksen varasto-otto, siirtotilauksen vastaanotto, ostotilaus ja täydennystyö.

Nimikkeiden siirtoa on rajoitettu, jotta työrivejä ei jaeta. Jos sinulla on nimikkeen A 100 kappaleen työrivi sijainnista Loc1, et voi siirtää tämän vuoksi vain 30:ntä nimikkeen A kappaletta tästä sijainnista toiseen sijaintiin. Tämä aiheuttaisi aiemmin luodun työrivin jakamisen 30:een ja 70:een, koska sijainnit eivät ole nyt samat.

Väliaikaisvarastoskenaariossa, joissa rekisterikilpi, johon siirrät tavaroita tai josta siirrät tavaroita, on määritetty työtilauksen kohderekisterikilveksi, vain koko rekisterikilven siirto on sallittu, jotta kohderekisterikilpi ei jakaudu.
Tällä hetkellä tuetaan vain ad hoc -siirtoja. Tämän vuoksi et voi siirtää varattua varastoa eteenpäin mallin mobiililaitteen valikkovaihtoehdoilla.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Varatun varaston siirto-oikeuksien määrittäminen yksittäisille työntekijöille

Valitse työntekijän, jolle annetaan oikeus siirtää varattua varastoa, **Salli työhön liitetyn varaston siirto** -valintaruutu kohdassa **Varastonhallinta** > **Asetukset** > **Työntekijä**.  

### <a name="backported"></a>Takaisinsovitus

Tämä toiminto on takaisinsovitettu Microsoft Dynamics AX 2012 R3:een ja on käytettävissä CU12:n osana.
Se voidaan myös ladata erikseen KB-numeron 3192548 kautta. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]