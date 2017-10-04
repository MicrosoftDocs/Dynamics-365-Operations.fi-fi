---
title: Tuotedimensiot
description: "Tuotedimensioita on neljä: Väri, Konfigurointi, Koko ja Tyyli. Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin. Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e6409db92b929eebca70d6d0176dd9b54a5f9b9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="product-dimensions"></a>Tuotedimensiot

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


Tuotedimensioita on neljä: Väri, Konfigurointi, Koko ja Tyyli. Tuotedimensiot yhdistetään dimensioryhmiksi ja dimensioryhmät liitetään päätuotteisiin. Tuotedimensioiden yhdistelmät määrittävät sen, kuinka tuotevariantit määritetään.

Tuotedimensiot ovat ominaisuuksia, joilla voidaan määrittää tuotemallin muuttuja. Voit käyttää tuotevarianttien määrittämiseen tuotedimensioiden yhdistelmiä. Sinun on määritettävä päätuotteelle vähintään yksi tuotedimensio, jotta voit luoda tuotevariantin.
Tuotevariantit
----------------

Tuotemallin muuttujien kutsutaan myös nimikkeinä. Nimike on aineellinen tuote eikä tarkoita samaa kuin palvelu. Päätuotteen voi kuitenkin määrittää myös palvelutyypin kanssa. Käyttämällä Palvelu-tyyppiä voit määrittää tuotevariantit, jotka sisältävät palveluita. Voit esimerkiksi määrittää konsultointityölle päätuotteen ja tuotevariantit kokeneempien ja nuorempien konsulttien suorittamalle työlle.

## <a name="product-dimensions"></a>Tuotedimensiot
Tuotedimensioita on neljä: Konfigurointi, Väri, Koko ja Tyyli. Tuotevariantit voidaan luoda tuotedimensioarvojen perusteella.

Tuotedimensioiden arvot, kuten Koko, Väri ja Tyyli, voidaan luoda **Koko**-, **Väri**- ja **Tyyli**-sivuilla, jotka voi avata valitsemalla **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Dimensio ja varianttiryhmät** &gt; **Koot/Värit/Tyylit**. Konfiguraatiodimension tuotedimension arvot luodaan yleensä käyttämällä joko tuotekonfiguraatiota tai dimensioihin perustuvaa konfiguraatiota. Tuotedimensioita voi luoda ja ylläpitää myös **Tuotedimensiot**-sivulla, jonka voi avata seuraavista sijainneista:
-   Valitse **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Päätuotteet**. Valitse **toimintoruudussa** **Tuotedimensiot**.
-   Valitse **Tuotetietojen hallinta** &gt; **Tuotteet** &gt; **Kaikki tuotteet ja päätuotteet**. Valitse päätuote. Valitse **toimintoruudussa** **Tuotedimensiot**.
-   Valitse **Tuotetietojen hallinta** &gt; **Vapautetut tuotteet**. Valitse päätuote. Valitse **toimintoruudusta** **Tuote**. Valitse **Päätuote**-ryhmästä **Tuotedimensiot**.

Tälle nimikkeelle luotavien varianttien lukumäärää rajoittaa mahdollisten tuotedimensioiden yhdistelmien määrä.
| **Vihje**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jos käytät tuotetta esimerkiksi tilausrivillä, voit valita tuotedimensiot määrittämään tuotevariantit, joita haluat käsitellä. |

## <a name="example"></a>Esimerkki
Yritys myy farmarihousuja. Farkut-nimikkeessä on käytössä Väri- ja Koko-tuotedimensiot. Myytäviä farmarihousuja on kolmea eri väriä ja kuutta eri kokoa. Värit: Sininen, musta, ruskea Koot: XS S, M, L, XL, XXL Kaikkia kokoja ei ole saatavana kolmena värinä. Jos kaikki yhdistelmät olivat käytettävissä, ne loisivat 18 eri farmarihousutyyppiä. Tässä esimerkissä tuotetaan vain seuraavat yhdeksän tuotevarianttia.

| Väri | Koko |
|-------|------|
| Sininen  | XS   |
| Sininen  | L    |
| Sininen  | M    |
| Musta | M    |
| Musta | L    |
| Musta | XL   |
| Ruskea | L    |
| Ruskea | XL   |
| Ruskea | XXL  |





