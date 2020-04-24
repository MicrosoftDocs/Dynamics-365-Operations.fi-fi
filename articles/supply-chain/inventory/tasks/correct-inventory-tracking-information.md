---
title: Oikeat varaston seurantatiedot
description: Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204191"
---
# <a name="correct-inventory-tracking-information"></a>Oikeat varaston seurantatiedot

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen. Tässä esimerkissä päivitetään eräohjatun nimikkeen tiedot muuttamalla virheellisesti rekisteröity erä toiseksi eräksi. Tämä käyttää tässä menettelyssä USPI-yrityksen demotietoja tai omia tietoja. Jos käytät omia tietoja, tarvitset nimikkeen, jossa erätoiminnot on otettu käyttöön ja joka ei ole sijaintiohjattu. Lisäksi varastosiirroille on oltava määritettynä varastokirjauskansio. Yleensä varastotyöntekijä tekee nämä tehtävät.


## <a name="create-an-inventory-transfer-journal"></a>Luo varastosiirtokirjauskansio
1. Valitse Siirrä.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
4. Valitse OK.

## <a name="create-journal-lines"></a>Tämän kirjauskansion rivit
1. Valitse Uusi.
2. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Jos käytössä on USPI, valitse nimike M5003.  
3. Kirjoita numero Määrä-kenttään.
4. Valitse Varastodimensiot-välilehti.
5. Anna tai valitse Erätunnus-kentässä arvo.
6. Syötä tai valitse arvo Toimipaikka-kenttään.
7. Anna tai valitse Varasto-kentässä arvo.
8. Anna tai valitse Erätunnus-kentässä arvo.

## <a name="post-the-journal"></a>Kirjaa kirjauskansio
1. Valitse Kirjaa.
2. Valitse OK.

## <a name="check-tracing-information"></a>Tarkista jäljitystiedot
1. Valitse Varasto.
2. Valitse Jäljitys.
3. Valitse OK.
    * Käyttämällä näitä jäljitystietoja, voit jäljittää taaksepäin, mistä erästä korjasit varaston.  Nämä tiedot ovat nähtävissä myös Nimikkeen seuranta -sivulla.  
4. Sulje sivu.

## <a name="check-inventory-transactions"></a>Tarkista varastotapahtumat
1. Valitse Varasto.
2. Valitse Tapahtumat.
    * Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.   

