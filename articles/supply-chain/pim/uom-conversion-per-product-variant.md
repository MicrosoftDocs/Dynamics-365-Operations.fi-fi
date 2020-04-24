---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204490"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mittayksiköiden tuotevarianttikohtaiset muunnokset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia. Siinä on myös määritysesimerkki.

Tämän ominaisuuden ansiosta yritykset voivat määrittää yksikkömuunnokset saman tuotteen varianttien välillä. Tässä ohjeaiheessa käytetään seuraavaa esimerkkiä. Yritys myy t-paitoja, joiden koot ovat S, M, L ja XL. T-paita määritetään tuotteena ja eri koot määritetään tuotteen variantteina. T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle. Yritys haluaa seurata t-paitojen eri variantteja **Kappaletta**-yksikkönä, vaikka niitä myydään **Laatikot**-yksikkönä. Varastoyksikön ja myyntiyksikön välinen muunto on 1 laatikko = 5 kappaletta. XL-variantin muunto on kuitenkin 1 laatikko = 4 kappaletta.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen

Tuotevariantit voidaan luoda vain **Tuotteen alatyyppi**: **Päätuote** -tuotteille. Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md).

Tätä ominaisuutta ei ole otettu käyttöön tuotteille, jotka on määritetty todellisen painon prosesseille. 

Kun luodaan päätuote, jolla on julkaistuja tuotevariantteja, varianttikohtaiset yksikkömuunnokset voidaan määrittää. Yksikön muunnossivun avaava valikkovaihtoehto on tuotteen tai tuotevariantin yhteydessä seuraavilla sivuilla.

-   **Tuotteen tiedot** -sivut
-   **Julkaistujen tuotteiden tiedot** -sivu
-   **Vapautetut tuotevariantit** -sivu

Kun avaat **Yksikkömuunnos**-sivun päätuotteen tai vapautetun tuotevariantin yhteydessä, voit valita, haluatko määrittää tuotteelle tai tuotevariantille yksikkömuunnoksen. Tee se valitsemalla joko **Tuotevariantti** tai **Tuote** **Luo muunnos kohteelle** -kentässä.

### <a name="product-variant"></a>Tuotevariantti

Jos valitset **Tuotevariantti**, voit sitten valita, minkä variantin yksikkömuunnoksen haluat määrittää **Tuotevariantti**-kentässä.

### <a name="product"></a>Tuote

Jos valitset **Tuote**, voit määrittää päätuotteen yksikkömuunnoksen. Tätä yksikkömuunnosta käytetään kaikissa tuotevarianteissa, joissa yksikkömuunnosta ei ole määritetty.

### <a name="example"></a>Esimerkki

Päätuotteella, **T-paita**, on neljä vapautettua tuotevarianttia: S, M, L ja XL. T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle.

Avaa ensin **Yksikkömuunnos**-sivu **t-paidan** Vapautetun tuotteen tiedot -sivulla.

Määritä **Yksikkömuunnos**-sivulla vapautetun XL-tuotevariantin yksikkömuunnos.

| **Kenttä**             | **Asetus**             |
|-----------------------|-------------------------|
| Luo muunnos kohteelle | Tuotevariantti         |
| Tuotevariantti       | T-paita : : XL : : |
| Yksiköstä             | Laatikot                   |
| Kerroin                | 4                       |
| Yksikköön               | Kappaletta                  |

Vapautetuilla S-, M- ja L-tuotevarianteilla on sama yksikkömuunnos laatikon ja kappaleen välillä, joten voit määrittää näiden tuotevarianttien yksikkömuunnoksen päätuotteessa.

| **Kenttä**             | **Asetus** |
|-----------------------|-------------|
| Luo muunnos kohteelle | Tuote     |
| Tuote               | T-paita     |
| Yksiköstä             | Laatikot       |
| Kerroin                | 5           |
| Yksikköön               | Kappaletta      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Yksikkömuunnosten päivittäminen Excelin avulla

Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä **Yksikkömuunnos**-sivulta Excel-laskentataulukkoon, päivittää sitten muunnokset ja julkaista ne lopuksi takaisin Supply Chain Mangementiin.

Exceliin viennin ja muokkausten takaisin Supply Chain Mangementiin julkaisemisen asetus otetaan käyttöön **Yksikkömuunnos**-sivun toimintoruudun **Avaa Microsoft Officessa** -valikkovaihtoehdossa.
