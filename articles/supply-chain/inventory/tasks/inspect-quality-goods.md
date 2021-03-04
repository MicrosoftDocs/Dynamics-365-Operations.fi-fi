---
title: Tarkista tavaroiden laatu
description: Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427334"
---
# <a name="inspect-the-quality-of-goods"></a>Tarkista tavaroiden laatu

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään. Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä. Vahvista ostotilaus 000016 ennen tämän esimerkin menettelyn aloittamista ja kirjaa tuotteen vastaanotto. Tällöin laatutilaus luodaan automaattisesti. Laatuassistentti suorittaa yleensä laatutarkastukset.


## <a name="select-a-quality-order"></a>Valitse laatutilaus.
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset**.
2. Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.  

## <a name="record-test-results"></a>Testitulosten tallentaminen
1. Valitse **Tulokset**.
2. Valitse **Muokkaa**.
3. Syötä numero **Tulosmäärä**-kenttään.
4. Valitse **Tulos**-kentässä avattavasta valikosta haluamasi tietue.  
- Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen. Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.  
5. Valitse **Tallenna**.
6. Sulje sivu.

## <a name="validate-the-quality-order"></a>Vahvista laatutilaus
1. Valitse **Tarkista**.
2. Valitse **Vahvistaja**-kentässä avattavasta valikosta käyttäjä, joka suorittaa tarkastuksen.  
3. Klikkaa **Valitse**.
4. Valitse **OK**.
5. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]