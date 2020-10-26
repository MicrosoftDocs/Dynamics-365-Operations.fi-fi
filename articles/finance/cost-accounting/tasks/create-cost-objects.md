---
title: Kustannusobjektien luominen
description: Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976112"
---
# <a name="create-cost-objects"></a>Kustannusobjektien luominen 

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. 


## <a name="create-new-cost-objects"></a>Luo uudet kustannusobjektit
1. Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Tallenna.

## <a name="configure-the-data-connector"></a>Määritä tietoyhdistin
1. Valitse Määritä dimension jäsenen lähde.
    * Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.  
2. Valitse Dimension nimi -kentässä Kustannuspaikka.
3. Valitse OK.

## <a name="import-cost-centers"></a>Tuo kustannuspaikat
1. Valitse Tuo dimension jäsenet.
2. Valitse OK.

## <a name="view-the-imported-cost-centers"></a>Näytä tuodut kustannuspaikat
1. Valitse Näytä dimension jäsenet.

