---
title: Tuo toimittajan tuoteluettelot
description: Tässä ohjeaiheessa käsittään toimittajan tuoteluettelon tietojen tuontia.
author: kamaybac
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ee709d72098b4304cf7748cae1a328736fa16188
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825227"
---
# <a name="import-vendor-catalogs"></a>Tuo toimittajan tuoteluettelot

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Toimittajan tuoteluetteloiden tuonti

Oston asiantuntijat voivat luoda ja ylläpitää Dynamics 365 Supply Chain Managementissa luetteloita, joita yrityksen työntekijät voivat käyttää tilatessaan nimikkeet ja palvelut sisäiseen käyttöön. Voit luoda tuotteiden hankintaluettelon lisäämällä työntekijöiden käyttöön tarkoitettuja nimikkeitä ja palveluja joko tuomalla tuoteluettelon tietoja tai lisäämällä tuoteluettelon tiedot manuaalisesti päätuotteeseen. 

Voit ladata toimittajan lähettämät luettelotiedot Microsoft Dynamics 365 -asiakasohjelmasta.

Toimittajan sinulle CMR-tiedostona eli luettelon ylläpitopyyntönä lähettämien tuotetietojen tiedostomuodon on oltava XML. CMR-tiedostossa on oltava toimittajan yritykselle toimittamien tuotteiden tiedot.

## <a name="import-vendor-catalog-data"></a>Toimittajan tuoteluettelon tietojen tuominen

Jos haluat tuoda toimittajan tuoteluettelon tietoja, sinun on suoritettava seuraavat tehtävät:

1. Määritä projekti siinä Tietojen hallinta -työtilassa, jossa olet määrittänyt tietojen yhdistämissäännöt. Valitse ensin **Tietojen hallinta** ja sitten **Määritä tietoprojektien roolit**.

2. Määritä hankintaluokkahierarkia ja määritä toimittajat hankintaluokkiin. Jos käytät kauppatavarakoodeja, lisää nämä koodit hankintaluokkiin. Lisätietoja hankintaluokkahierarkian määrittämisestä on kohdassa [Hankintaluokkahierarkian määrittäminen](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Konfiguroi toimittaja luettelon tuontia varten Valitse ensin toimittaja ja sitten **Hankinta** > **Asetukset** > **Konfiguroi toimittaja luettelon tuontia varten**.

4. Määritä luettelon tuonnin työnkulku. Luo CMR-tiedostomalli ja jaa se toimittajan kanssa.

5. Luo toimittajan tuoteluettelot valitsemalla **Hankinta** \> **Yleinen** \> **Luettelot** \> **Toimittajan tuoteluettelot**. Toimittajalta vastaanotetut CMR-tiedostot eli luettelon ylläpitopyynnöt ryhmitetään tässä luettelossa. 

6. Lataa CMR-tiedosto palvelimeen.

7. Arvioi, hyväksy tai hylkää toimittajan tuoteluettelon tuotteet. Tuotteet yhdistetään automaattisesti hankintaluokkiin. 

Hyväksytyt tuotteet lisätään päätuotteeseen ja vapautetaan valituille oikeushenkilöille. Vain hyväksytyt tuotteen voidaan lisätä hankintaluetteloon.

## <a name="generate-a-catalog-import-file-template"></a>Luettelon tuontitiedostomallin luominen

Luettelon tuontitiedostomalli on XSD-tiedosto, jonka avulla voit luoda CMR-tiedoston toimittajan tuotteille. Voit käyttää CMR-tiedostoa uuden luettelon luomiseen, aiemmin luodun luettelon korvaamiseen tai olemassa olevan luettelon muokkaamiseen.

1. Valitse **Hankinta** \> **Luettelot** \> **Toimittajan tuoteluettelot** ja kaksoisnapsauta käsiteltävää luetteloa.

2. Lataa nykyisen luettelon tuontimalli (XSD-tiedosto). Valitse **Päivitä luettelo** -sivun **toimintoruudun** **Luettelot**-välilehden **Aiheeseen liittyviä tietoja** -ryhmässä ensin **Luo luettelomalli** ja sitten **Hankintamalli**.

    - Voit luoda **Hankintaluokka**-asetuksella luettelomallin, jonka sisältämissä hankintaluokissa toimittaja saa tarjota tuotteita.

3. Valitse **Tallenna nimellä** -valintaruudussa sijainti, johon haluat tallentaa luettelotiedostomallin, ja tallenna tiedosto.

Seuraavassa blogikirjoituksessa on lisätietoja ja esimerkkejä: [Dynamics AX:n toimittajien tuoteluettelot](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]