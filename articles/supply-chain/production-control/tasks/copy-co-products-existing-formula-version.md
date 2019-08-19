---
title: Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta
description: Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 626c0fc8a60eeb84060d7279833de583d55a95a2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838748"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon. Edellytyksenä on vähintään, että rinnakkaistuotteisiin on liitetty vähintään yksi reseptiversio. Tämän menettelyn luomisessa käytetty USP2-yrityksen demotietoja.


## <a name="find-a-released-product"></a>Etsi vapautettu tuote
1. Siirry Vapautetut tuotteet -kohtaan.
2. Valitse Näytä suodattimet.
    * Olet lisäämässä Tuotantotyyppi-kentän suodattimen valintaikkunaan.  
3. Lisää Tuotantotyyppi-kenttä napsauttamalla Lisää suodatinkenttä.
    * Seuraavassa vaiheessa kaava on lisättävä manuaalisesti Tuotantotyyppi-kenttään ennen, kuin napsautat Käytä-painiketta. Tämä asettaa julkaistujen tuotteiden luettelon suodatuksen.  
4. Kirjoita kaava manuaalisesti Tuotantotyyppi-kenttään.
5. Valitse Apply.

## <a name="select-a-released-product"></a>Valitse vapautettu tuote
1. Etsi haluamasi tietue luettelosta ja valitse se.
2. Valitse Reseptiversiot.
    * Valitse teknisen suunnittelun toimintoruudussa Reseptiversiot.  

## <a name="copy-co-products"></a>Kopioi oheistuotteet
1. Valitse toimintoruudussa Reseptiversio.
2. Valitse Oheistuotteet.
3. Valitse Kopioi.
4. Syötä tai valitse arvo Nimiketunnus-kentässä.
5. Anna tai valitse arvo Reseptiversio-kentässä.
6. Valitse OK.
7. Sulje sivu.

