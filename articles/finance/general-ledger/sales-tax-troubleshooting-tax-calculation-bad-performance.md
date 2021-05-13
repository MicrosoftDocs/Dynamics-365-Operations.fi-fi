---
title: Verolaskennan suorituskyky vaikuttaa tapahtumiin
description: Tässä aiheessa on verotuslaskennan suorituskykyyn ja tapahtumiin liittyviä vianmääritystietoja.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947635"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Verolaskennan suorituskyky vaikuttaa tapahtumiin

[!include [banner](../includes/banner.md)]

Joskus verolaskennan suorituskykyyn liittyvät suorituskykyongelmat vaikuttavat tapahtumaan. Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.

## <a name="review-the-transaction-line-count"></a>Tarkastele tapahtuman rivimäärää

Määritä, onko tapahtumalla suuri määrä rivejä (esimerkiksi enemmän kuin useita satoja). Jos näin ei ole, siirry seuraavaan osaan. Jos tapahtumalla on useita satoja rivejä, viivytä veron laskentaa. Lisätietoja on kohdassa [Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa](enable-delayed-tax-calculation.md). 

Seuraavaksi voit määrittää, täyttyykö jokin seuraavista ehdoista:

- Suurista tiedostoista on tuontitapahtumia.
- Useat istunnot käsittelevät saman tapahtumaveron laskennan samanaikaisesti.
- Tapahtumalla on useita rivejä, ja näkymät päivitetään reaaliaikaisesti. Esimerkiksi **Kirjauskansio**-sivun **Laskettu arvonlisäverosumma** -kenttä päivitetään reaaliaikaisesti, kun rivin kenttiä muutetaan.

   [![Laskettu arvonlisäveron summa -kenttä kirjauskansion tositesivulla](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Jos jokin näistä ehdoista täyttyy, viivytä veron laskentaa.

## <a name="review-the-call-stack"></a>Kutsupinon tarkasteleminen

Tarkista kutsupino ja määritä, kutsutaanko verolaskentaa useita kertoja. Jos näin ei ole, siirry seuraavaan osaan. Jos kutsupinoa kutsutaan useita kertoja, voit vähentää veron laskenta-aikoja noudattamalla näitä vaiheita.

1. Jos kirjauskansio on harkinnut tapahtumaa, viivytä veron laskentaa. Lisätietoja on kohdassa [Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa](enable-delayed-tax-calculation.md).
2. Jos tapahtuma on ostotilaus ja sovellusversio on uudempi kuin 10.0.15, voit viivyttää veron laskentaa lopulliseen laskentaan ottamalla käyttöön väliversiotestauksen kohteelle **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Kutsupinon aikajanan tarkasteleminen

Tarkista kutsupinon aikajana ja määritä, esiintyykö seuraavia ongelmia. Jos tunnukset ovat käytössä, voit korjata ongelman aktivoimalla väliversiotestauksen kohteelle **TaxUncommittedDoIsolateScopeFlighting**.

- Tapahtuma aiheuttaa järjestelmän lopettavan vastaamisen, kunnes istunto päättyy. Näin ollen tapahtuma ei voi laskea veron tulosta. Seuraavassa kuvassa näkyy vastaanottamasi Istunto päättynyt -sanomaruutu.

    [![Istunto päättynyt -sanoma](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted**-menetelmät vievät enemmän aikaa kuin muut menetelmät. Esimerkiksi seuraavassa kuvassa **TaxUncommitted::updateTaxUncommitted()**-menetelmä kestää 43,347.42 sekuntia, mutta muiden menetelmien käyttö kestää 0,09 sekuntia.

    [![Menetelmän kestot](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Veron laskennan mukauttaminen ja kutsuminen

Kun muokkaat, älä kutsu veron laskentaa jokaisen rivin **lisää()**- tai **päivitä()**-menetelmässä. Verolaskentaa tulee kutsua tapahtumatasolla.

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa

Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
