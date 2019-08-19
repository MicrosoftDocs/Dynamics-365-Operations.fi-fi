---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844366"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mittayksiköiden tuotevarianttikohtaiset muunnokset

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

Tässä ohjeaiheessa käsitellään tuotevarianteille määritettäviä mittayksiköiden muunnoksia. Siinä on myös määritysesimerkki.

Tämän ominaisuuden ansiosta yritykset voivat määrittää yksikkömuunnokset saman tuotteen varianttien välillä. Tässä ohjeaiheessa käytetään seuraavaa esimerkkiä. Yritys myy t-paitoja, joiden koot ovat S, M, L ja XL. T-paita määritetään tuotteena ja eri koot määritetään tuotteen variantteina. T-paidat pakataan laatikoihin. Laatikossa voi olla viisi t-paitaa, joskin XL-koossa tilaa on kuitenkin vain neljälle t-paidalle. Yritys haluaa seurata t-paitojen eri variantteja **Kappaletta**-yksikkönä, vaikka niitä myydään **Laatikot**-yksikkönä. Varastoyksikön ja myyntiyksikön välinen muunto on 1 laatikko = 5 kappaletta. XL-variantin muunto on kuitenkin 1 laatikko = 4 kappaletta.

## <a name="setup"></a>Luo perustiedot

Voit määrittää parametrit, jolla käytetään ominaisuutta tuotteissa, joissa **Kaikki prosessit** on otettu käyttöön, tai vain tuotteessa, joissa **Varastoprosessit** on otettu käyttöön. Määritys tehdään **Tuotetietojen hallintaparametrit** -sivun **Ota käyttöön mittayksiköiden muunnokset** -asetuksella.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen

Tuotevariantit voidaan luoda vain **Tuotteen alatyyppi**: **Päätuote** -tuotteille. Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md).

Tätä ominaisuutta ei ole otettu käyttöön tuotteille, jotka on määritetty todellisen painon prosesseille. 

Ota mittayksiköiden muunnos käyttöön päätuotteen luonnin aikana valitsemalla **Ota käyttöön mittayksiköiden muunnokset** -asetus **Tuotteen tiedot** -sivulla.

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

Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä **Yksikkömuunnos**-sivulta Excel-laskentataulukkoon, päivittää sitten muunnokset ja julkaista ne lopuksi takaisin Finance and Operationsiin.

Exceliin viennin ja muokkausten takaisin Finance and Operationsiin julkaisemisen asetus otetaan käyttöön **Yksikkömuunnos** -sivun toimintoruudun **Avaa Microsoft Officessa** -valikkovaihtoehdossa.
