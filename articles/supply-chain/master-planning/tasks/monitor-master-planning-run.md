---
title: Pääsuunnitteluajon valvonta
description: Tuotannon suunnittelija haluaa nähdä, onko pääsuunnitteluajo käynnissä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845110"
---
# <a name="monitor-a-master-planning-run"></a>Pääsuunnitteluajon valvonta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tuotannon suunnittelija haluaa nähdä, onko pääsuunnitteluajo käynnissä. Käytä menettelyn täytössä USMF-yrityksen demotietoja.


## <a name="run-master-planning"></a>Pääsuunnittelun suorittaminen
1. Valitse Pääsuunnittelu.
    * Löydät tämän oletuskoontinäytöltä.  
2. Anna tai valitse Suunnitelma-kentässä arvo.
    * Esimerkki: StaticPlan  
3. Valitse Suorita.
4. Valitse Seuraa käsittelyaikaa -kentässä Kyllä.
    * Jos tämä kenttä on jo valittu, voit ohittaa tämän vaiheen.  
5. Syötä Säikeiden määrä -kenttään numero.
6. Laajenna Tietueet-kohta ja sisällytä osaan.
7. Valitse Suodatin.
8. Merkitse valittu rivi luettelossa.
    * Merkitse rivi, jossa Kenttä = Nimiketunnus.  
9. Syötä tai valitse arvo Ehdot-kenttään.
    * Esimerkki: T0001  
10. Valitse OK.
11. Valitse OK.

## <a name="monitor-the-master-planning-run"></a>Pääsuunnitteluajon valvonta
1. Valitse Historia.
2. Valitse Kyselyt.
3. Valitse Käsittelytehtävän kesto.
4. Etsi haluamasi tietue luettelosta ja valitse se.
    * Saat kullekin nimikkeelle yhteenvedon jokaiseen suunnitteluvaiheeseen kuluneesta ajasta.  

