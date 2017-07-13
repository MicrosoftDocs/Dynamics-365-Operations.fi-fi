---
title: "Työhön liitetyn varaston siirtäminen varastonhallinnassa"
description: "Tässä ohjeaiheessa kerrotaan kappaleen keräilyvahvistuksen määrittämisestä ja käyttämisestä mobiililaitteessa."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: d2db0431a3f749cbdaf35cc5108851f1e116bc96
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Työhön liitetyn varaston siirtäminen varastonhallinnassa
<a id="movement-of-inventory-with-associated-work-in-warehouse-management" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Voit päättää varaston siirron avulla, mitä varastotyöntekijät saavat siirtää varattuun varastoon. Tämä parantaa joustavuutta säännellyissä varastoissa, joissa voit olla antamatta työtekijällä mahdollisuuden valita uuden keräilysijainnin aiemmin luodulle keräilytyölle. Sen avulla varastopäälliköt voivat myös hallita, mitä ominaisuuksia kokemattomat työntekijät saavat.

Varastotyöntekijöiden päivittäisten toimenpiteiden hallintaan liittyvästä monipuolisuudesta on hyöytä esimerkiksi seuraavanlaisissa skenaarioissa:

## Skenaario 1
<a id="scenario-1" class="xliff"></a>
Yrityksellä on suhteellisen pieni vastaanottoalue ja se on täynnä poispanoa odottavia kuormalavoja ja laatikoita. Suurta lähetystä odotetaan kuluvana päivänä, joten vastaanottotyöntekijä päättää tyhjentää vastaanottoalueen siirtämällä osan kuormalavoista toissijaiselle saapuvien väliaikaiselle varastoalueelle.

## Skenaario 2
<a id="scenario-2" class="xliff"></a>
Kokenut varastotyöntekijä huomaa mahdollisuuden konsolidoida nimikkeet varastossa yhteen sijaintiin sen sijaan, että ne jaettaisiin kolmeen läheiseen sijaintiin niin, että kussakin on vähän nimikkeitä. Työntekijä haluaa konsolidoida määrän siirtämällä nimikkeet kustakin näistä sijainneista samaan sijaintiin ja samaan rekisterikilpeen.

## Skenaario 3
<a id="scenario-3" class="xliff"></a>
Kuormalava odottaa lähetystä väliaikaisessa sijainnissa, kuten STAGE01, jonka lähellä on BAYDOOR01. Suunnitelmien muutoksen vuoksi kuorma-auto on kuitenkin ajoitettu saapumaan sijaintiin BAYDOOR04. Kuljetustyöntekijä tietää tämän ja hänen on varmistettava, että kuorma-auton ei tarvitse odottaa lastaamista sijainnista STAGE01. Kuljetustyöntekijä päättää siirtää kyseisen lähetyksen nimikkeet sijainnista STAGE01 sijaintiin STAGE04, mikä on lähempänä uutta kohdetta.

### Nykyiset rajoitukset
<a id="current-limitations" class="xliff"></a>

Siirrettävät työrajoituksia ovat vain myyntitilaus, siirtotilauksen varasto-otto, siirtotilauksen vastaanotto, ostotilaus ja täydennystyö.

Nimikkeiden siirtoa on rajoitettu, jotta työrivejä ei jaeta. Jos sinulla on nimikkeen A 100 kappaleen työrivi sijainnista Loc1, et voi siirtää tämän vuoksi vain 30:ntä nimikkeen A kappaletta tästä sijainnista toiseen sijaintiin. Tämä aiheuttaisi aiemmin luodun työrivin jakamisen 30:een ja 70:een, koska sijainnit eivät ole nyt samat.

Väliaikaisvarastoskenaariossa, joissa rekisterikilpi, johon siirrät tavaroita tai josta siirrät tavaroita, on määritetty työtilauksen kohderekisterikilveksi, vain koko rekisterikilven siirto on sallittu, jotta kohderekisterikilpi ei jakaudu.
Tällä hetkellä tuetaan vain ad hoc -siirtoja. Tämän vuoksi et voi siirtää varattua varastoa eteenpäin mallin mobiililaitteen valikkovaihtoehdoilla.

### Varatun varaston siirto-oikeuksien määrittäminen yksittäisille työntekijöille
<a id="set-up-the-permission-to-move-reserved-inventory-for-individual-workers" class="xliff"></a>

Valitse työntekijän, jolle annetaan oikeus siirtää varattua varastoa, **Salli työhön liitetyn varaston siirto** -valintaruutu kohdassa **Varastonhallinta** > **Asetukset** > **Työntekijä**.  

### Takaisinsovitus
<a id="backported" class="xliff"></a>

Tämä toiminto on takaisinsovitettu Microsoft Dynamics AX 2012 R3:een ja on käytettävissä CU12:n osana.
Se voidaan myös ladata erikseen KB-numeron 3192548 kautta. 


