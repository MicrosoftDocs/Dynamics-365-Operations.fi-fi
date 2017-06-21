---
title: Varaston tunniste laskenta
description: "Tässä artikkelissa on tietoja tunnisteiden inventoinnista. Sitä käytetään varaston todellisen sisällön ja käytettävissä olevan varaston vertailemiseen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 61a48a61963f643c8969e9090c2e84b5499b716a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-tag-counting"></a>Varaston tunniste laskenta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja tunnisteiden inventoinnista. Sitä käytetään varaston todellisen sisällön ja käytettävissä olevan varaston vertailemiseen. 

Luomalla rivejä **Tunnisteiden laskenta** -sivulla, varaat tunnistenumeron kullekin varastonimikkeelle, esimerkiksi numero 1 ja 500 väliltä. Laskennan aikana syötetään nimiketunnus ja määrä sitä vastaavaan tunnisteeseen. Tunnistetta voidaan sitten käyttää perustana syötettäessä tunnisteita kirjauskansioon. Sen jälkeen kun tunnisteiden kirjauskansio on kirjattu, järjestelmä luo uuden inventointikirjauskansion **Laskenta**-sivulle. Uusi kirjauskansio perustuu tunnisteiden laskenta kirjauskansioriveihin, jotka olet luonut. Laskeaksesi nimikkeet tunnisteita käyttäemn tiettyyn varastodimensioon, valitse dimensio **Näytä dimensio** -sivulla, joka tulee näyttöön, kun luot tunnisteiden inventointikirjauskansion. Esimerkiksi, laskeaksesi nimikkeitä tietyssä varastossa, valitse **varaston** valintaruutu. Jos **Lukitse nimikkeet inventoinnin ajaksi** -liukusäädin **inventointi- ja varastonhallintaparametrit** -sivulla on valittuna, nimikkeitä ei voi päivittää fyysisesti inventoinnin aikana. Nimikkeitä ei kuitenkaan lukita tunnisteiden inventointikirjauskansioissa inventoinnin ajaksi. Ennen tunnisteiden inventointikirjauskansion rivien kirjaamista ja siirtämistä inventointikirjauskansioon, varastotapahtumia ei luoda. Jos tunnisteet syötetään satunnaisesti ja haluat tunnistaa mahdollisesti puuttuvat tunnisteet, lajittele rivit valitsemalla **tunniste**
-kenttä.

<a name="see-also"></a>Lisätietoja
--------

[Inventointi](../warehousing/cycle-counting.md)




