---
title: "Fyysisen varaston siirtäminen varastossa"
description: "Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Fyysisen varaston siirtäminen varastossa

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä. Ennen aloittamista varastosiirroille on oltava määritettynä varastokirjauskansio. Voit käyttää menettelyssä USMF-yrityksen demotiedoissa näytettyjä esimerkkiarvoja tai omia tietojasi, jos sinulla on määritettyjä tuotteita ja sijainteja. Yleensä varastotyöntekijä tekee nämä tehtävät.


## <a name="create-an-inventory-transfer-journal"></a>Luo varastosiirtokirjauskansio
1. Valitse Siirrä.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
4. Valitse OK.
    * Kunkin kirjauskansion rivin määrittämiseen on lähtö- ja kohdedimensioasetus. Ne ovat välttämättömiä tässä kirjauskansiotyypissä. Voit siirtää nimikkeitä sijainteihin eri säännöillä. Tässä esimerkissä nimike siirretään samassa varastossa rekisterikilvellä ohjatusta sijainnista sijaintiin, jota ei ohjata rekisterikilvellä.   

## <a name="create-journal-lines"></a>Tämän kirjauskansion rivit
1. Valitse Uusi.
2. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Jos käytössä on USMF, voit valita A0001.  
3. Anna tai valitse Toimipaikasta-kentässä arvo.
    * Jos käytössä on USMF, voit valita 2.  
4. Anna tai valitse Toimipaikkaan-kentässä arvo.
    * Jos käytössä on USMF, voit valita 2.  
5. Anna tai valitse Varastosta-kentässä arvo.
    * Jos käytössä on USMF, voit valita 24.  
6. Anna tai valitse Varastoon-kentässä arvo.
    * Jos käytössä on USMF, voit valita 24.  
7. Anna tai valitse Lähtösijainti -kentässä arvo.
    * Jos käytössä on USMF, voit valita FL-001.  
8. Anna tai valitse Kohdesijainti-kentässä arvo.
    * Jos käytössä on USMF, voit valita BULK-001.  
9. Kirjoita numero Määrä-kenttään.
10. Valitse Varastodimensiot-välilehti.
11. Anna tai valitse Rekisterikilpi-kentässä arvo.
    * Jos käytössä on USMF, voit valita 24.  
12. Valitse Tallenna.

## <a name="post-the-inventory-transfer-journal"></a>Kirjaa varastosiirtokirjauskansio
1. Valitse Kirjaa.
2. Valitse OK.

## <a name="view-inventory-transactions"></a>Näytä varastotapahtumat
1. Valitse Varasto.
2. Valitse Tapahtumat.
    * Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.  

