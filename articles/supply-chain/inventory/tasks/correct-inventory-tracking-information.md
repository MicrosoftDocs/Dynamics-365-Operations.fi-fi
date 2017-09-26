---
title: Oikeat varaston seurantatiedot
description: "Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf8c67d315666edfffe86e459bc7a4478697f07
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="correct-inventory-tracking-information"></a>Oikeat varaston seurantatiedot

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

