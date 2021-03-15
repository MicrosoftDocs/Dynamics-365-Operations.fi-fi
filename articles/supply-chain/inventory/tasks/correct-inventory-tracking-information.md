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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c70dba7d21eab372cec235efa5a4be19587a409
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000131"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]