---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688170"
---
# <a name="set-up-segregation-of-duties"></a>Määritä tehtävien eriyttäminen

[!include [banner](../../includes/banner.md)]

Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle. Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset. Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan. Lue sääntö seuraavalla menettelyllä. Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn. Tämän menettelyn luomisessa käytetty esittely-yritys on DAT. 

1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt**.
2. Valitse **Uusi**.
3. Kirjoita säännön arvo **Nimi**-kenttään.
4. Avaa haku napsauttamalla **Ensimmäinen tehtävä** -kentästä avattavan valikon painiketta.
5. Etsi haluamasi tietue luettelosta ja valitse se. Valitse ensimmäinen säännön ohjaama tehtävä.
6. Avaa haku napsauttamalla **Toinen tehtävä** -kentästä avattavan valikon painiketta. 
7. Etsi haluamasi tietue luettelosta ja valitse se. Valitse toinen säännön ohjaama tehtävä.
10. Valitse vaihtoehto **Vakavuusaste**-kentästä. Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.  
11. Kirjoita **Suojausriski**-kenttään arvo. Anna turvallisuusriskin kuvaus.  
12. Kirjoita **Suojauksen mitätöinti** -kenttään arvo. Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä. Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.     
13. Valitse **Tallenna**.

