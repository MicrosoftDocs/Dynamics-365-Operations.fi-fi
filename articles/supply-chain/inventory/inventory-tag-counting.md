---
title: Varaston tunnisteiden inventointi
description: Tässä ohjeaiheessa on tietoja tunnisteiden inventoinnista. Sitä käytetään varaston todellisen sisällön ja käytettävissä olevan varaston vertailemiseen.
author: MarkusFogelberg
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1df4a97dee3dc24856a1b40f3dc8dd095338b614
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825960"
---
# <a name="inventory-tag-counting"></a>Varaston tunnisteiden inventointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja tunnisteiden inventoinnista. Sitä käytetään varaston todellisen sisällön ja käytettävissä olevan varaston vertailemiseen.

Luomalla rivejä **Tunnisteiden laskenta** -sivulla, varaat tunnistenumeron kullekin varastonimikkeelle, esimerkiksi numero 1 ja 500 väliltä. Laskennan aikana syötetään nimiketunnus ja määrä sitä vastaavaan tunnisteeseen. Tunnistetta voidaan sitten käyttää perustana syötettäessä tunnisteita kirjauskansioon. Sen jälkeen kun tunnisteiden kirjauskansio on kirjattu, järjestelmä luo uuden inventointikirjauskansion **Laskenta**-sivulle. Uusi kirjauskansio perustuu tunnisteiden laskenta kirjauskansioriveihin, jotka olet luonut. Laskeaksesi nimikkeet tunnisteita käyttäemn tiettyyn varastodimensioon, valitse dimensio **Näytä dimensio** -sivulla, joka tulee näyttöön, kun luot tunnisteiden inventointikirjauskansion. Esimerkiksi, laskeaksesi nimikkeitä tietyssä varastossa, valitse **varaston** valintaruutu. Jos **Lukitse nimikkeet inventoinnin ajaksi** -liukusäädin **inventointi- ja varastonhallintaparametrit** -sivulla on valittuna, nimikkeitä ei voi päivittää fyysisesti inventoinnin aikana. Nimikkeitä ei kuitenkaan lukita tunnisteiden inventointikirjauskansioissa inventoinnin ajaksi. Ennen tunnisteiden inventointikirjauskansion rivien kirjaamista ja siirtämistä inventointikirjauskansioon, varastotapahtumia ei luoda. Jos tunnisteet syötetään satunnaisesti ja haluat tunnistaa mahdollisesti puuttuvat tunnisteet, lajittele rivit valitsemalla **tunniste**-kenttä.

## <a name="additional-resources"></a>Lisäresurssit

[Inventointi](../warehousing/cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]