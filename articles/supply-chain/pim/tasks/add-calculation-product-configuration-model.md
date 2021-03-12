---
title: Lisää laskelma tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987051"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Lisää laskelma tuotemääritysmalliin

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin. Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille. Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.


## <a name="add-a-calculation"></a>Lisää laskelma

## <a name="create-calculation-expression"></a>Luo laskelmalauseke
1. Valitse Muokkaa lauseketta.
2. Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].
3. Valitse Vahvista.
4. Valitse Sulje.
5. Valitse OK.

