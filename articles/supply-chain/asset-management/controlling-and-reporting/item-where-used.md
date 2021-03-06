---
title: Nimike, missä käytetty
description: Tässä ohjeaiheessa selitetään, miten voit saada yleiskuvan siitä, missä nimikettä käytetään resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 262a5a9d83767599f6e15183d6afcacf4b5901fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808637"
---
# <a name="item-where-used"></a>Nimike, missä käytetty

[!include [banner](../../includes/banner.md)]

 

Voit tehdä tietyn nimikkeen laskennan saadaksesi yhteenvedon siitä, missä nimikettä on käytetty käyttöomaisuuden hallinnassa. Tuloksissa näkyy konteksti, jossa nimikettä on käytetty sen elinkaaren aikana. **Nimike, missä käytetty** -sivu voidaan avata resurssienhallinnan päävalikosta, ja sitä voi käyttää myös seuraavilta sivuilta:

- [Resurssien tuoterakenteet](../objects/object-BOM.md)

- [Varaosat oletusresurssityypeissä](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Ylläpitoennuste](../work-orders/maintenance-forecasts.md)

- [Osto ja hankinta](../work-orders/procurement.md)

- [Työtilaus osto](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Nimike, missä käytetty -laskelman suorittaminen.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike, missä käytetty** tai valitse **Nimike, missä käytetty** -painike on jollakin edellä mainituista sivuista.

2. Valitse **Nimike, missä käytetty** -valintaikkunassa nimike, jolle haluat tehdä laskun **Nimiketunnus**-kentässä.

3. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimikeriveistä haluat liittyen toiminnallisiin sijainteihin. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin nimikerivit näkyvät ylimmällä tasolla. Tämän vuoksi rivin suhde/määrä voidaan lisätä toiminnallisista sijainneista, jotka sijaitsevat alemmalla tasolla. 
    
    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki nimikerivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

4. Valitse **Sisällytä** -osan vaihtopainikkeissa arvoksi Kyllä, jos haluat sisällyttää kohteen laskelmiin.

5. Aloita laskenta valitsemalla **OK**.

6. Valitse **Nimike, missä käytetty** -välilehden asiaankuuluvat **Ryhmittely ...**-painikkeet tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

7. Jos haluat näyttää nimikkeeseen liittyvät dimensiot, valitse **Näytä dimensiot** ja valitse näytettävät dimensiot.

## <a name="example"></a>Esimerkki

Alla olevassa näyttökuvassa on esimerkki nimikkeestä, jossa on laskettu Nimike, missä käytetty -lasku nimiketunnukselle "1000".

![Esimerkki nimikkeen käyttöpaikan laskennasta](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]