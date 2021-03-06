---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745738"
---
# <a name="set-up-segregation-of-duties"></a>Määritä tehtävien eriyttäminen

[!include [banner](../../includes/banner.md)]

Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät. Tätä kutsutaan tehtävien eriyttämiseksi. Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle. Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset. Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan. Lue sääntö seuraavalla menettelyllä. Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn.

1. Valitse **Järjestelmänhallinta** > **Suojaus** > **Tehtävien eriyttäminen** > **Tehtävien eriyttämisen säännöt**.
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

> [!IMPORTANT] 
> Tehtävien eriyttämisen sääntöjen noudattamista ei ole tarkistettu sääntöä luotaessa. Voit luoda säännön, joka luo ristiriidan aiemmin luoduille rooleille. Myös aiemmin luodut käyttäjän roolimääritykset voivat olla ristiriidassa uuden säännön kanssa. Vaatimustenmukaisuus on tarkistettava, kun sääntö luodaan tai sitä muokataan. Lisätietoja on kohdassa [Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]