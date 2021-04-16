---
title: Määritä päätilien luokat
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää päätilien luokat Dynamics 365 Financessa.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815113"
---
# <a name="set-up-main-account-categories"></a>Määritä päätilien luokat

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit määrittää päätilien luokat. Päätilin luokkia käytetään raportoinnin oletusraporteissa ja Power BI:ssa. Oletusarvoisesti luodut päätilin luokille voidaan määrittää uusi nimi mutta niitä ei voi poistaa. Tililuokkia voidaan luoda lisää raportointia ja analysointia varten. Tässä aiheessa käytetään USMF-esittely-yritystä.

## <a name="create-a-main-account-category"></a>Luo päätilin luokka
1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Tilit > Päätililuokat**.
2. Valitse **Uusi**.
3. Anna **Päätililuokka**-kentässä yksilöivä nimi.
4. Kirjoita päätilin luokan kuvaus **Kuvaus**-kenttään.
5. Valitse **Päätilin tyyppi** -kentässä luokkaan linkitettävä päätilin tyyppi.

## <a name="link-main-accounts-to-account-category"></a>Linkitä päätilit tililuokkiin
1. Valitse **Linkitä päätilit**.
2. Valitse luettelosta päätilit, jotka liitetään päätililuokkaan, merkitsemällä **Linkitetty**-sarakkeen valintaruudut. Päätilien määrittäminen päätilin luokkaan koostaa tilien saldot, kun kyseistä luokkaa käytetään raportointiin ja analysointiin.  
3. Valitse päätilit valitsemalla **Linkitetty**-vaihtoehto tai poistamalla sen valinta.
4. Valitse **OK**.
5. Valitse **Kyllä**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]