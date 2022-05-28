---
title: Kustannusobjektien luominen
description: Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734127"
---
# <a name="create-cost-objects"></a>Kustannusobjektien luominen 

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä. Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja. 


## <a name="create-new-cost-objects"></a>Luo uudet kustannusobjektit
1. Valitse **Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimi**-kenttään.
4. Syötä tai valitse arvo **Dimension jäsenten tietoyhdistin** -kentässä.
5. Kirjoita **Kuvaus**-kenttään arvo.
6. Valitse **Tallenna**.

## <a name="configure-the-data-connector"></a>Määritä tietoyhdistin
1. Valitse **Määritä dimension jäsenen lähde**.
    * Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.  
2. Valitse **Dimension nimi** -kentässä Kustannuspaikka.
3. Valitse **OK**.

## <a name="import-cost-centers"></a>Tuo kustannuspaikat
1. Valitse **Tuo dimension jäsenet**.
2. Valitse **OK**.

## <a name="view-the-imported-cost-centers"></a>Näytä tuodut kustannuspaikat
1. Valitse **Näytä dimension jäsenet**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
