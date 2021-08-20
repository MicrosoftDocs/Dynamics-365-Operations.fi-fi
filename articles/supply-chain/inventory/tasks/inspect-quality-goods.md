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
ms.openlocfilehash: ceb5547b6c1d4c44e53faba0d6e2c1f0368fb95768a2520ecc39066ff73a03d2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755358"
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
