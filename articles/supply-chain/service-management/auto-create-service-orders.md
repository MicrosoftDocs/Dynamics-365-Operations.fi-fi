---
title: Automaattisesti luodut huoltotilaukset
description: Voit luoda huoltosopimuksiin perustuvia huoltotilauksia huoltosopimuksen voimassaoloaikana.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675792"
---
# <a name="automatically-create-service-orders"></a>Automaattisesti luodut huoltotilaukset 

[!include [banner](../includes/banner.md)]


Voit luoda huoltosopimuksiin perustuvia huoltotilauksia huoltosopimuksen voimassaoloaikana.

Huoltosopimuksista luotavat huoltotilaukset liitetään huoltosopimukseen.

Huoltotilaukset luodaan automaattisesti seuraavista asetuksista:

  - Huoltosopimuksen välin asetukset huoltosopimusriveillä. Huoltosopimuksen väli ilmaisee huoltotilausrivien luomisen tiheyden. Lisätietoja on kohdassa [Huoltovälit](service-intervals.md).

  - Huoltojakson määritys **Alkupäivämäärä**- ja **Loppupäivämäärä** -kentissä **Luo huoltotilauksia** -lomakkeessa. Lisätietoja on kohdassa [Luo huoltotilaukset automaattisesti](create-service-orders-automatically.md).

  - **Yhdistä huoltotilaukset** -vaihtoehto huoltosopimuksen otsikossa. Tämä asetus määrittää, yhdistetäänkö huoltotilauksen rivit huoltosopimuksesta työntekijän, huoltotehtävän, huoltokohteen vai huoltosopimuksen mukaan. Lisätietoja on kohdassa [Huoltotilausten yhdistäminen](combine-service-orders.md).

  - Huoltosopimusrivin **Aikaikkuna**-asetus. Aikaikkuna määrittää, miten kauas huoltotilausrivi voi siirtyä suhteessa sen laskettuun päivämäärään. Lisätietoja on kohdassa [Aikaikkunat](time-windows.md).


> [!NOTE]
> <P>Jos huoltotilauksessa määritetty päivä ei ole avoin <STRONG>Huollon hallintaparametrit</STRONG> -lomakkeessa määritetyssä kalenterissa, järjestelmä ilmoittaa kalenteriristiriidasta. Voit ohittaa sanoman, sillä huoltotilaus luodaan, vaikka päivä olisikin suljettu kalenterissa.</P>

## <a name="example-1"></a>Esimerkki 1

Huoltosopimus on voimassa 1. tammikuuta 2012 – 31. joulukuuta 2012. Jos **Luo huoltotilauksia** -lomakkeessa määritetty huoltojakso on 1.11.2012 – 1.2.2013, huoltotilaukset luodaan ajalta 1.11.2012 – 31.12.2012.

## <a name="example-2"></a>Esimerkki 2

Huoltosopimus on voimassa 1. tammikuuta 2012 – 31. joulukuuta 2012. Huoltosopimukseen on liitetty kaksi huoltosopimusriviä. Ensimmäisen huoltosopimusrivin alkamispäivä on 2.1.2012 ja päättymispäivä 1.3.2012. Toisen huoltosopimusrivin alkamispäivä on 1.4.2012 ja päättymispäivä 31.12.2012. Määrität **Luo huoltotilauksia** -lomakkeessa jaksoksi 1.10.2012–31.12.2012. Tällöin huoltotilaukset luodaan vain toiselle huoltosopimusriville, sillä ensimmäisen sopimusrivin alkamis- ja päättymispäivä on ennen huoltotilaukselle määritettyä jaksoa.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]