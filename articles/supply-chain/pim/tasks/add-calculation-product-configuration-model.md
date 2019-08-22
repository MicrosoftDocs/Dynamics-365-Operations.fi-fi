---
title: Lisää laskelma tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39450b5aef2fb7b57492a52011f4b0db9dc8ff2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845038"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Lisää laskelma tuotemääritysmalliin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin. Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille. Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.


## <a name="add-a-calculation"></a>Lisää laskelma

## <a name="create-calculation-expression"></a>Luo laskelmalauseke
1. Valitse Muokkaa lauseketta.
2. Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].
3. Valitse Vahvista.
4. Valitse Sulje.
5. Valitse OK.

