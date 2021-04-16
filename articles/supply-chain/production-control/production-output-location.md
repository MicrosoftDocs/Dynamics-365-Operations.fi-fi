---
title: Tuotannon tuotossijainti
description: Tässä ohjeaiheessa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814629"
---
# <a name="production-output-location"></a>Tuotannon tuotossijainti

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.

Tuotannon tuotossijainti on sijainti, jossa valmista tavaraa säilytetään heti valmistuksen jälkeen. Yleensä tämä sijainti on valmiin tavaran tuottavan tuotantoprosessin lähellä. Tuotannon tuotossijaintia käytetään materiaalin välivarastona, ennen kuin se esimerkiksi siirretään lähetysalueelle, varastosijaintiin, tuotantovirran tuotantoprosessin tuotannon tuotossijaintiin. 

Tuotannon oletustuotossijainti määritetään, kun valmiit tuotteet ilmoitetaan tuotantotilauksessa tai erätilauksessa. Tämä tuotossijainti ilmoitetaan seuraavan hierarkian avulla:

1. Käytä tuotanto- tai erätilauksen otsikossa määritettyä tuotossijaintia.
2. Jos sijainti ei ole siellä, käytä siinä resurssissa määritettyä tuotossijaintia, jota tuotantoreitissä määritetty viimeisin toiminto käyttää.
3. Jos sijainti ei ole siellä, käytä siinä resurssiryhmässä määritettyä tuotossijaintia, jota tuotantoreitissä määritetyn viimeisimmän toiminnon resurssi käyttää.
4. Jos sijainti ei ole siellä, käytä sitä tuotossijaintia, joka on määritetty tuotantotilaukselle määritetyssä varastossa.

Tuotannon oletustuotossijainti määritetään vain tuotteille, jotka on määritetty edistyksellisellä varastoprosessilla. Kun tämän tyyppinen nimike määritetään valmiiksi, **Valmiiden tuotteiden poispano**- tai **Rinnakkaistuotteen ja sivutuotteen poispano** -tyyppinen varastotyö luodaan. Tämän tyyppinen työ käyttää tuotannon tuotossijaintia keräyssijaintia. Sijaintidirektiivi määrittää poispanosijainnin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]