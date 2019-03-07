---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "318784"
---
# <a name="set-up-segregation-of-duties"></a>Määritä tehtävien eriyttäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle. Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset. Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan. Lue sääntö seuraavalla menettelyllä. Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn. Tämän menettelyn luomisessa käytetty esittely-yritys on DAT. 

1. Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
    * Anna säännön nimi.  
4. Avaa haku napsauttamalla Ensimmäinen tehtävä -kentässä avattavan valikon painiketta.
5. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse ensimmäinen säännön ohjaama tehtävä.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Avaa haku napsauttamalla Toinen tehtävä -kentässä avattavan valikon painiketta.
8. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse toinen säännön ohjaama tehtävä.  
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Valitse vaihtoehto Vakavuusaste-kentässä.
    * Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.  
11. Kirjoita Suojausriski-kenttään arvo.
    * Anna turvallisuusriskin kuvaus.  
12. Kirjoita Suojauksen mitätöinti -kenttään arvo.
    * Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä. Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.  
13. Valitse Tallenna.

