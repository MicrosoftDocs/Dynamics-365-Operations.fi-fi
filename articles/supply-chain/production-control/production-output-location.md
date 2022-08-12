---
title: Tuotannon tuotossijainti
description: Tässä artikkelissa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.
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
ms.openlocfilehash: 130db343c4d09f2b8d31bf8acad3dcceec2be32e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067938"
---
# <a name="production-output-location"></a>Tuotannon tuotossijainti

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.

Tuotannon tuotossijainti on sijainti, jossa valmista tavaraa säilytetään heti valmistuksen jälkeen. Yleensä tämä sijainti on valmiin tavaran tuottavan tuotantoprosessin lähellä. Tuotannon tuotossijaintia käytetään materiaalin välivarastona, ennen kuin se esimerkiksi siirretään lähetysalueelle, varastosijaintiin, tuotantovirran tuotantoprosessin tuotannon tuotossijaintiin. 

Tuotannon oletustuotossijainti määritetään, kun valmiit tuotteet ilmoitetaan tuotantotilauksessa tai erätilauksessa. Tämä tuotossijainti ilmoitetaan seuraavan hierarkian avulla:

1. Käytä tuotanto- tai erätilauksen otsikossa määritettyä tuotossijaintia.
2. Jos sijainti ei ole siellä, käytä siinä resurssissa määritettyä tuotossijaintia, jota tuotantoreitissä määritetty viimeisin toiminto käyttää.
3. Jos sijainti ei ole siellä, käytä siinä resurssiryhmässä määritettyä tuotossijaintia, jota tuotantoreitissä määritetyn viimeisimmän toiminnon resurssi käyttää.
4. Jos sijainti ei ole siellä, käytä sitä tuotossijaintia, joka on määritetty tuotantotilaukselle määritetyssä varastossa.

Tuotannon oletustuotossijainti määritetään vain tuotteille, jotka on määritetty varastonhallintaprosesseilla (WMS). Kun tämän tyyppinen nimike määritetään valmiiksi, **Valmiiden tuotteiden poispano**- tai **Rinnakkaistuotteen ja sivutuotteen poispano** -tyyppinen varastotyö luodaan. Tämän tyyppinen työ käyttää tuotannon tuotossijaintia keräyssijaintia. Sijaintidirektiivi määrittää poispanosijainnin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]