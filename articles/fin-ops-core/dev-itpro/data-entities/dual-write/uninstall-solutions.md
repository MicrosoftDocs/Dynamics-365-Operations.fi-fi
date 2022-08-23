---
title: Kaksoiskirjoitussovelluksen orkestrointiratkaisujen asennuksen poistaminen
description: Tässä artikkelissa on tietoja kaksoiskirjoitussovelluksen orkestrointiratkaisujen asennuksen poistamisesta.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: fd9dc98ec1323a2ef262a330a400a6bd3833e554
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288727"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Kaksoiskirjoitussovelluksen orkestrointiratkaisujen asennuksen poistaminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on tietoja kaksoiskirjoitussovelluksen orkestrointiratkaisujen asennuksen poistamisesta.

Jotkut asiakkaat asentavat tahattomasti kaksoiskirjoitussovellusorkestrointipaketin, joka asentaa useita ratkaisuja heidän Microsoft Dataverse -ympäristöönsä. Ylimääräisien ratkaisujen asentaminen pakettiin voi aiheuttaa odottamattomia ja epämieluisia ongelmia.

Voit korjata kaksoiskirjoitussovellusten suunnittelupaketin asennukseen liittyvät ongelmat poistamalla ei-toivotut kaksoiskirjoitusratkaisut seuraavassa järjestyksessä:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (jos on olemassa)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Voit poistaa tämän ratkaisun asennuksen avaamalla tukipalvelupyynnön Microsoftin kanssa.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Jos asennettuina ovat osapuolen ratkaisut ja yleiset osoitekirjaratkaisut, poista ratkaisujen asennus seuraavassa järjestyksessä:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Osapuoli
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
