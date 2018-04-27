---
title: Tuo toimittajan tuoteluettelot
description: "Tässä ohjeaiheessa käsittään toimittajan tuoteluettelon tietojen tuontia."
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a56e6ea0a8470f205b1c74379c887c0cac85a6b4
ms.openlocfilehash: c290bcd4787144fb4dd4232c06d2fb9e1e67ca3e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="import-vendor-catalogs"></a>Tuo toimittajan tuoteluettelot
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Toimittajan tuoteluetteloiden tuonti

Microsoft Dynamics 365 for Finance and Operationsin avulla ostajat voivat luoda ja ylläpitää luetteloita, joita yrityksen työntekijät voivat käyttää tilatessaan nimikkeitä ja palveluja sisäiseen käyttöön. Voit luoda tuotteiden hankintaluettelon lisäämällä työntekijöiden käyttöön tarkoitettuja nimikkeitä ja palveluja joko tuomalla tuoteluettelon tietoja tai lisäämällä tuoteluettelon tiedot manuaalisesti päätuotteeseen. 

Voit ladata toimittajan lähettämät luettelotiedot Microsoft Dynamics 365 -asiakasohjelmasta.

Toimittajan sinulle CMR-tiedostona eli luettelon ylläpitopyyntönä lähettämien tuotetietojen tiedostomuodon on oltava XML. CMR-tiedostossa on oltava toimittajan yritykselle toimittamien tuotteiden tiedot.

## <a name="import-vendor-catalog-data"></a>Toimittajan tuoteluettelon tietojen tuominen

Jos haluat tuoda toimittajan tuoteluettelon tietoja, sinun on suoritettava seuraavat tehtävät:

1.  Määritä projekti siinä Tietojen hallinta -työtilassa, jossa olet määrittänyt tietojen yhdistämissäännöt. Valitse ensin **Tietojen hallinta** ja sitten **Määritä tietoprojektien roolit**. 

2.  Määritä hankintaluokkahierarkia ja määritä toimittajat hankintaluokkiin. Jos käytät kauppatavarakoodeja, lisää nämä koodit hankintaluokkiin. Lisätietoja hankintaluokkahierarkian määrittämisestä on kohdassa [Hankintaluokkahierarkian määrittäminen](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3.  Konfiguroi toimittaja luettelon tuontia varten Valitse ensin toimittaja ja sitten **Hankinta** > **Asetukset** > **Konfiguroi toimittaja luettelon tuontia varten**.

4.  Määritä luettelon tuonnin työnkulku. Luo CMR-tiedostomalli ja jaa se toimittajan kanssa.

5.  Luo toimittajan tuoteluettelot valitsemalla **Hankinta** \> **Yleinen** \> **Luettelot** \> **Toimittajan tuoteluettelot**. Toimittajalta vastaanotetut CMR-tiedostot eli luettelon ylläpitopyynnöt ryhmitetään tässä luettelossa. 

6.  Lataa CMR-tiedosto palvelimeen.

7.  Arvioi, hyväksy tai hylkää toimittajan tuoteluettelon tuotteet. Tuotteet yhdistetään automaattisesti Dynamics 365 for Finance and Operationsin hankintaluokkiin. 
    
Hyväksytyt tuotteet lisätään päätuotteeseen ja vapautetaan valituille oikeushenkilöille. Vain hyväksytyt tuotteen voidaan lisätä hankintaluetteloon.

## <a name="generate-a-catalog-import-file-template"></a>Luettelon tuontitiedostomallin luominen

Luettelon tuontitiedostomalli on yleisesti käytettävä XSD-tiedosto, jonka avulla voit luoda CMR-tiedoston toimittajan tuotteille. Voit käyttää CMR-tiedostoa uuden luettelon luomiseen, aiemmin luodun luettelon korvaamiseen tai olemassa olevan luettelon muokkaamiseen.

1.  Valitse **Hankinta** \> **Luettelot** \> **Toimittajan tuoteluettelot** ja kaksoisnapsauta käsiteltävää luetteloa.

2.  Lataa nykyisen luettelon tuontimalli (XSD-tiedosto). Valitse **Päivitä luettelo** -sivun **toimintoruudun** **Luettelot**-välilehden **Aiheeseen liittyviä tietoja** -ryhmässä ensin **Luo luettelomalli** ja sitten **Hankintamalli**.

    -   Voit luoda **Hankintaluokka**-asetuksella luettelomallin, jonka sisältämissä hankintaluokissa toimittaja saa tarjota tuotteita.

3. Valitse **Tallenna nimellä** -valintaruudussa sijainti, johon haluat tallentaa luettelotiedostomallin, ja tallenna tiedosto.

Seuraavassa blogikirjoituksessa on lisätietoja ja esimerkkejä: [Dynamics AX:n toimittajien tuoteluettelot](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).

