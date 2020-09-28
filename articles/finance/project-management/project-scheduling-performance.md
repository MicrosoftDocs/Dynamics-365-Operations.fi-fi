---
title: Projektiresurssin ajoituksen suorituskyky
description: Tässä ohjeaiheessa on tietoja suurten projektimäärien resurssien ajoituksen suorituskyvyn parantamisesta.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760539"
---
# <a name="project-resource-scheduling-performance"></a>Projektiresurssin ajoituksen suorituskyky

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Resurssien ajoitukseen liittyviä suorituskykyongelmia voi esiintyä, jos projekteja on tuhansia. Resurssien ajoituksen suorituskyvyn parantamiseksi on käytettävissä ominaisuus, jonka avulla käyttäjät voivat vähentää resurssin käytettävyyslomakkeen käynnistykseen kuluvaa aikaa. Tämä poistaa erityisesti resurssin kapasiteetin koonnin synkronointiprosessia ja nopeuttaa resurssin hakua käyttämällä **ResProjectResource**-taulua. Huomaa, että **ResRollup**-taulua ei enää käytetä.

> [!IMPORTANT]
> Jos resurssin kapasiteetin koonnin synkronointiprosessissa tai **ResProjectResource**-taulussa on riipppuvuus, älä käytä tätä ominaisuutta.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön
Voit ottaa resurssien aikataulutuksen suorituskyvyn parantamisen käyttöön seuraavasti.

1. Siirry kohtaan **Ominaisuuksien hallinta** > **Kaikki** ja etsi ominaisuusluettelosta **Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön** -ominaisuus.
2. Valitse **Ota käyttöön nyt**.

> [!NOTE]
> Jos et löydä ominaisuutta luettelosta, päivitä luettelo valitsemalla **Tarkista päivitykset**.

3. Päivitä selain ja siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektiresurssit** > **Synkronoi resurssikalenterien kapasiteetti kaikissa yrityksissä**.
4. Määritä **Poista olemassa olevat kapasiteettitietueet** -kohdan arvoksi **Kyllä**, jos haluat poistaa aiemmat tiedot. Jos haluat luoda lisää tietoja, määritä arvoksi **Ei**.
5. Valitse **Kausikoodi**-kentässä kausi, jolle tietoja luodaan. Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.
6. Jos jätät **Kausikoodi**-kentän tyhjäksi, valitse tietyt aloitus- ja päättymispäivämäärät tietojen luontia varten.
7. Valitse **OK**.

 > [!NOTE]
 > Tämä jakaa yleiset tiedot **ResCalendarCapacity**-tauluun ympäristön kaikissa yrityksissä. Tällöin erätyö on suoritettava vain yhdessä yrityksessä. Tämän erätyön tietoja tarvitaan laskettaessa resurssikapasiteetti liittyvän kalenterin avulla.

8. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Projektiresurssit** > **Täytä projektiresurssit kaikissa yrityksissä** ja valitse sitten **OK**. Tämä on tietojen päivityskomentosarja yleisiä tietoja varten **ResProjectResource**-, **ResCalendarDateTimeRange**- ja **ResEffectiveDateTimeRange**-tauluissa. **PSAPRojSchedRole.RootActivity**-kentän arvot päivitetään myös. Jos tätä ei suoriteta, näyttöön tulee varoitus, kun yrität suorittaa resurssien ajoituksen toimintoja.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Resurssin ajoituksen suorituskyvyn parantamisen poistaminen käytöstä

1. Siirry kohtaan **Ominaisuuksien hallinta** > **Kaikki** ja hae ominaisuusluettelosta **Resurssin ajoituksen suorituskyvyn parantamisen ottaminen käyttöön** -ominaisuus.
2. Valitse ominaisuus ja valitse sitten **Poista käytöstä** -painike.
3. Päivitä selain.
4. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Kausittainen** > **Kapasiteetin synkronointi** > **Synkronoi resurssin kapasiteetin koonnit**.
5. Määritä **Kapasiteetin koonnin synkronointi** -sivulla **Poista olemassa olevat kapasiteettitietueet** -kohdan arvoksi **Kyllä**, jos haluat poistaa aiemmat tiedot. Jos haluat luoda lisää tietoja, määritä arvoksi **Ei**.
6. Valitse **Kausikoodi**-kentässä kausi, jolle tietoja luodaan. Jos valitset kausikoodin, aloitus- ja päättymispäivämäärää ei tarvitse määrittää.
7. Jos jätät **Kausikoodi**-kentän tyhjäksi, valitse tietyt aloitus- ja päättymispäivämäärät tietojen luontia varten.
8. Valitse **OK**.

> [!NOTE]
> Tämä jakaa yleiset tiedot **ResRollup**-tauluun ympäristön kaikissa yrityksissä. Tällöin erätyö on suoritettava vain yhdessä yrityksessä. Tätä erätyötä tarvitaan kaikissa **Resurssin saatavuus** -näkymissä. Jos tätä eräajoa ei suoriteta, **ResRollup**-tiedot luodaan prosessien aikana. Tämä voi kestää kauan.
