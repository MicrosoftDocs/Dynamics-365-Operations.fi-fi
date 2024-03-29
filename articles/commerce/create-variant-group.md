---
title: Varianttiryhmän luominen
description: Tässä artikkelissa kuvataan, miten tuotteelle luodaan koko-, tyyli- tai värivarianttiryhmiä Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270097"
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

![Kokoryhmän luominen.](media/Size-Groups.png)

## <a name="additional-resources"></a>Lisäresurssit

[Tuotetietojen yleiskatsaus](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Vähittäismyyntituotteiden määrittäminen](set-up-retail-products.md)

[Tuotedimensiot](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
