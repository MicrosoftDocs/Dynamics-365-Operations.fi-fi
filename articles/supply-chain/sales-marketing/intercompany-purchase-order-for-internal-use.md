---
title: Konsernin sisäisen ostotilauksen luominen ja laskuttaminen sisäistä käyttöä varten
description: Tässä aiheessa käsitellään konsernin sisäisen ostotilauksen luomista ja laskuttamista sisäistä käyttöä varten
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 52b58b2dcecd5d9a83a47b425d6fb13b36c40b60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675876"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Konsernin sisäisen ostotilauksen luominen ja laskuttaminen sisäistä käyttöä varten

[!include [banner](../../includes/banner.md)]

Konsernin sisäisen ostotilaus voidaan luoda konsernin sisäiselle toimittajalle. Tämä luo automaattisesti konsernin sisäisen myyntitilauksen konsernin sisäisessä toimittajassa.

![Konsernin sisäinen ostoprosessi](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Konsernin sisäisen ostotilauksen ja sitä vastaavan konsernin sisäisen myyntitilauksen luominen

Suorita nämä vaiheet yrityksessä AAA kuvassa esitetyllä tavalla.

1. Valitse **Ostoreskontra** \> **Ostotilaukset** \> **Kaikki ostotilaukset**.
1. Luo **Kaikki ostotilaukset** -luettelosivulla ostotilaus konsernin sisäiselle toimittajalle. Kentän arvot kopioidaan toimittajan tililtä ostotilaukseen.

    Koska töitä tehdään konsernin sisäisen toimittajan kanssa, konsernin sisäinen myyntitilaus luodaan toimittajaa vastaavassa yrityksessä. Konsernin sisäisen myyntitilauksen numero voi olla sama kuin konsernin sisäisen ostotilauksen numero, ja se voi sisältää yrityksen tunnuksen. Käytettävä numerorakenne määräytyy sen mukaan, mitä on valittu **Konsernin sisäinen** -sivun **Myyntitilauksen numerointi** -kentässä. Jos esimerkiksi ostotilaus 00029\_064 luodaan yrityksessä AAA, myyntitilauksen numero yrityksessä BBB on AAA00029\_64.

    Tietosanoma ilmaisee, että konsernin sisäinen ostotilaus ja myyntitilaus on luotu. Sanoma antaa tiedoksi konsernin sisäisen myyntitilauksen numeron.

1. Lisää rivinimikkeitä ostotilaukseen. Vastaavat rivinimikkeet lisätään automaattisesti konsernin sisäiseen myyntitilaukseen. Jos nimikettä ei ole toisessa yrityksessä, näyttöön tulee sanoma eikä nimikettä voi lisätä ostotilaukseen. Korjaa tämä ongelma siirtymällä toiseen oikeushenkilöön ja vapauttamalla tuote kyseiselle oikeushenkilölle. Nimike on sitten käytettävissä lisättäväksi myyntitilauksiin kyseisessä yrityksessä. Siirry sitten takaisin ostotilauksen yritykseen ja jatka rivinimikkeiden lisäämistä.
1. Kun olet antanut ostotilauksen tiedot, vahvistaa se.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Konsernin sisäisen pakkausluettelon ja myyntilaskun käsitteleminen

Suorita nämä vaiheet yrityksessä BBB kuvassa esitetyllä tavalla.

1. Valitse **Myyntireskontra \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse konsernin sisäinen myyntitilaus **Kaikki myyntitilaukset** -luettelosivulla.
1. Valitse toimintoruudussa **Kerää ja pakkaa** -välilehti ja valitse sitten **Pakkausluettelo**.
1. Valitse **Kirjaus**-valintaruutu.
1. Valitse **OK**. Pakkausluettelo kirjataan yrityksessä BBB.
1. Valitse konsernin sisäinen myyntitilaus **Kaikki myyntitilaukset** -luettelosivulla.
1. Valitse toimintoruudussa **Lasku**-välilehti ja valitse sitten **Lasku**.
1. Valitse **Kirjaus**-valintaruutu.
1. Valitse **OK**.

    Konsernin sisäisen myyntitilauksen myyntilasku kirjataan yrityksessä BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Konsernin sisäisen tuotteen vastaanoton ja toimittajan laskun käsittely

Suorita nämä vaiheet yrityksessä AAA kuvassa esitetyllä tavalla.

1. Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse konsernin sisäinen ostotilaus **Kaikki ostotilaukset** -luettelosivulla.
1. Valitse toimintoruudussa **Vastaanotto**-välilehti ja valitse sitten **Tuotteen vastaanotto**. Tuotteen vastaanotto luodaan. Tuotteen vastaanottonumero on sama kuin konsernin sisäisen pakkausluettelon numero.
1. Valitse **Kirjaus**-valintaruutu.
1. Valitse **OK**.
1. Valitse konsernin sisäinen ostotilaus **Kaikki ostotilaukset** -luettelosivulla.
1. Valitse toimintoruudussa **Lasku** ja valitse sitten **Lasku**. Toimittajan lasku luodaan. Toimittajan laskun numero on sama kuin konsernin sisäisen myyntilaskun numero.
1. Lopeta toimittajan laskun kirjoittaminen ja kirjaa se.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
