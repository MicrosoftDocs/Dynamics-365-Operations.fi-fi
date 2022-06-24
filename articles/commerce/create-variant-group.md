---
title: Varianttiryhmän luominen
description: Tässä artikkelissa kuvataan, miten tuotteelle luodaan koko-, tyyli- tai värivarianttiryhmiä Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a46dc9fd5cdb848818964e771d373924b217147a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874958"
---
# <a name="create-a-variant-group"></a>Varianttiryhmän luominen


[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miten tuotteelle luodaan koko-, tyyli- tai värivarianttiryhmiä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce tukee tuotteelle useita variantteja. Varianttiryhmien määrittäminen eri tuoteluokille on paras ratkaisu. Esimerkiksi t-paidoille voidaan luoda kokoryhmä, joka sisältää koot XS, S, M, L ja XL, tai väriryhmä, joka sisältää kaikki tuotteen saatavilla olevat värivaihtoehdot. Varianttiryhmät kannattaa lisätä ennen tuotteiden lisäämistä.

Tässä artikkelissa luodaan ja määritetään kokoryhmä. Vastaavia menettelyjä voidaan käyttää tyyli- ja väriryhmien lisäämiseen ja määrittämiseen.

## <a name="create-a-size-group"></a>Kokoryhmän luominen

Luo kokoryhmä noudattamalla seuraavia ohjeita.
 
1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Varianttiryhmät \> Kokoryhmät**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Kokoryhmä**-ruudussa kokoryhmän yksilöivä nimi.
1. Kirjoita soveltuva kuvaus **Kuvaus**-ruutuun.
1. Valitse toimintoruudussa **Tallenna**.

## <a name="add-attributes-to-the-size-group"></a>Määritteiden lisääminen kokoryhmään

Voit lisätä määritteitä kokoryhmään seuraavasti.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Varianttiryhmät \> Kokoryhmät**
1. Valitse kokoryhmä siirtymisruudussa.
1. Valitse **Kokoryhmärivit**-kohdassa **Lisää**.
1. Kirjoita **Koko**-ruutuun merkkijono, joka edustaa kokoa (esim. XL).
1. Kirjoita **Koon nimi** -ruutuun koon nimi (esimerkiksi Extra Large).
1. Syötä **Täydennyspaino**-ruutuun numero, joka edustaa täydennyspainoa.
1. Syötä **Viivakoodin numero**-ruutuun viivakoodia edustava numero.
1. Syötä **Näyttöjärjestys**-ruutuun numero, joka edustaa näyttöjärjestystä.
1. Kun olet lisännyt tarvittavat koot, valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki rentojen paitakokojen kokoryhmästä.

![Kokoryhmän luominen.](media/create-variant-group.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotetietojen yleiskatsaus](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Vähittäismyyntituotteiden määrittäminen](set-up-retail-products.md)

[Tuotedimensiot](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]