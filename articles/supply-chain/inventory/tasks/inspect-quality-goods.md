---
title: Tarkista tavaroiden laatu
description: Tässä ohjeaiheessa kerrotaan, kuinka laatutilauksia käsitellään.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956131"
---
# <a name="inspect-the-quality-of-goods"></a>Tarkista tavaroiden laatu

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka laatutilauksia käsitellään. Laatuassistentti suorittaa yleensä laatutarkastukset.

Jos vakioesittely on asennettu, voit suorittaa sen avulla tässä ohjeaiheessa olevat toimenpiteet. Valitse *USMF*-yritys ennen kuin aloitat, jotta voit käyttää esittelytietoja. Sen jälkeen on vahvistettava ostotilaus *000016* ja kirjattava tuotteen vastaanotto. Laatutilaus luodaan automaattisesti.

## <a name="step-1-select-a-quality-order"></a>Vaihe 1: Valitse laatutilaus

Voit luoda laatutilauksen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.

## <a name="step-2-record-test-results"></a>Vaihe 2: Testitulosten tallentaminen

Voit tallentaa testitulokset noudattamalla seuraavia vaiheita.

1. Valitse **Tulokset**.
1. Valitse **Muokkaa**.
1. Syötä numero **Tulosmäärä**-kenttään.
1. Etsi haluamasi tietue **Tulos**-kentästä. Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen. Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.
1. Valitse **Tallenna**.
1. Sulje sivu.

## <a name="step-3-validate-the-quality-order"></a>Vaihe 3: Vahvista laatutilaus

Voit vahvistaa laatutilauksen seuraavasti.

1. Valitse **Tarkista**.
1. Valitse **Vahvistaja**-kentästä tarkastuksen tehnyt käyttäjä.
1. Valitse **Valitse**.
1. Valitse **OK**.
1. Sulje sivu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
