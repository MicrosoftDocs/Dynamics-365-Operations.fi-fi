---
title: Mittayksiköiden tuotevarianttikohtaiset muunnokset
description: Tässä ohjeaiheessa käsitellään tuotevarianttien mittayksiköiden muunnosten määrittämistä. Siinä on myös määritysesimerkki.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c02252abcaf82cb2aab928949827e25ef7cce8c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579565"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mittayksiköiden tuotevarianttikohtaiset muunnokset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään eri tuotevarianttien mittayksiköiden muunnosten määrittämistä.

Tuotevarianttien avulla yksittäisestä tuotteesta voi luoda variaatioita sen sijaan, että luotaisiin useita ylläpidettäviä yksittäisiä tuotteita. Tuotevariantti voi olla esimeriksi tietyn kokoinen ja värinen T-paita.

Aiemmin yksikkömuunnokset voitiin määrittää vain päätuotteissa. Tämän vuoksi kaikilla tuotevarianteilla oli samat yksikön muunnossäännöt. Jos *Tuotevarianttien mittamuunnosten yksikkö* -toiminto on kuitenkin otettu käyttöön ja jos T-paitoja myydään laatikoittain ja laatikkoon pakattavien T-paitojen määrä määräytyy T-paitojen koon mukaan, yksikkömuunnokset voidaan nyt määrittää T-paitojen eri kokojen ja pakkauksessa käytettyjen laatikoitten mukaan,

## <a name="turn-on-the-feature-in-your-system"></a>Toiminnon ottaminen käyttöön järjestelmässä

Jos toiminto ei vielä näy järjestelmässä valitse [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Tuotevarianttien mittamuunnosten yksikkö* -toiminto käyttöön.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Tuotteen varianttikohtaisen yksikkömuunnoksen määrittäminen

Tuotevariantteja voidaan luoda vain tuotteille, jotka ovat päätuotteita. Lisätietoja on kohdassa [Päätuotteen luominen](tasks/create-product-master.md). *Tuotevarianttien mittamuunnosten yksikkö* -toimintoa ei voi käyttää tuotteissa, joihin on määritetty todellisen painon prosesseja.

Päätuote määritetään tukemaan varianttikohtaista yksikkömuunnosta seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.
1. Päätuotteen voi luoda tai avata tuotteen **Tuotteen tiedot** -sivulla.
1. Määritä **Ota käyttöön mittayksiköiden muunnokset** -asetukseksi *Kyllä*.
1. Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Yksikkömuunnokset**.
1. **Yksikkömuunnokset** -sivu avautuu. Valitse yksi seuraavista välilehdistä:

    - **Luokansisäiset muunnokset** – valitse tämä välilehti, kun haluat muuntaa samaan yksikköluokkaan kuuluvia yksiköitä.
    - **Luokkienväliset muunnokset** – valitse tämä välilehti, kun haluat muuntaa eri yksikköluokkiin kuuluvia yksiköitä.

1. Lisää uusi yksikkömuunto valitsemalla **Uusi**.
1. Määritä **Luo muunnos kohteelle** -kentän arvoksi jokin seuraavista:

    - **Tuote** – Jos valitset tämän arvon, voit määrittää päätuotteen yksikkömuunnoksen. Tätä yksikkömuunnosta käytetään kaikkien niiden tuotevarianttien varalla olevan muunnoksena, jos mitään yksikkömuunnosta ei ole määritetty.
    - **Tuotevariantti** – Jos valitset tämän arvon, voit määrittää tietyn tuotevariantin yksikkömuunnoksen. Valitse variantti **Tuotevariantti**-kentän avulla.

    ![Uuden yksikkömuunnoksen lisääminen.](media/uom-new-conversion.png "Uuden yksikkömuunnoksen lisääminen")

1. Käytä muita käytettävissä olevia kenttiä yksikkömuunnoksen määrittämiseen.
1. Tallenna uusi yksikkömuunnos valitsemalla **OK**.

> [!TIP]
> Voit avata tuotteen tai tuotevariantin **Yksikkömuunnokset**-sivun seuraavilta sivuilta:
> 
> - Tuotteen tiedot
> - Vapautettujen tuotteiden tiedot
> - Vapautetut tuotevariantit

## <a name="example-scenario"></a>Esimerkkiskenaario

Tässä skenaariossa yritys myy t-paitoja, joiden koot ovat S, M, L ja XL. T-paita määritetään tuotteena ja eri koot määritetään kyseisen tuotteen variantteina. T-paidat pakataan laatikkoihin. Kussakin laatikossa voi olla viisi S-, M- ja L-kokoista T-paitaa. XL-kokoisia T-paitoja voi laatikossa olla vain neljä.

Yritys haluaa seurata eri variantteja *Kappaletta*-yksikkönä, vaikka niitä myydään *Laatikot*-yksikkönä. S-, M- ja L-kokojen varastoyksikön ja myyntiyksikön muunnos on 1 laatikko = 5 kappaletta. XL-kokoisten muunnos on 1 laatikko = 4 kappaletta.

1. Avaa **Yksikkömuunnokset**-sivu **T-paita**-tuotteen **Vapautetun tuotteen tiedot** -sivulla.
1. Määritä **Yksikkömuunnokset**-sivulla seuraava vapautetun **XL**-tuotevariantin yksikkömuunnos.

    | Kenttä                 | Asetus                 |
    |-----------------------|-------------------------|
    | Luo muunnos kohteelle | Tuotevariantti         |
    | Tuotevariantti       | T-paita : : XL : : |
    | Yksiköstä             | Laatikot                   |
    | Kerroin                | 4                       |
    | Yksikköön               | Kappaletta                  |

1. Koska **S**-, **M**- ja **L**-tuotevarianteilla on kaikilla sama yksikkömuunnos *Laatikko*- ja *Kappaleet*-yksikköjen välillä, voit määrittää niiden seuraavan yksikkömuunnoksen päätuotteessa.

    | Kenttä                 | Asetus |
    |-----------------------|---------|
    | Luo muunnos kohteelle | Tuote |
    | Tuote               | T-paita |
    | Yksiköstä             | Laatikot   |
    | Kerroin                | 5       |
    | Yksikköön               | Kappaletta  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Yksikkömuunnosten päivittäminen Excelin avulla

Jos tuotteella on useita tuotevariantteja, joilla on erilaiset yksikkömuunnokset, yksikkömuunnokset kannattaa viedä Microsoft Excel -työkirjaan, päivittää ne siellä ja julkaista ne lopuksi takaisin Dynamics 365 Supply Chain Managementiin.

Yksikkömuunnokset viedään Exceliin valitsemalla **Yksikkömuunnokset**-sivun toimintoruudussa **Avaa Microsoft Officessa**.

## <a name="additional-resources"></a>Lisäresurssit

[Mittayksiköiden hallinta](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]