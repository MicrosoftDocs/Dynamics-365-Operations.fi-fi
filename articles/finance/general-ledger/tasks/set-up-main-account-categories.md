---
title: Päätilin luokkien määritys
description: Tässä artikkelissa kuvataan, kuinka voit määrittää päätilien luokat Dynamics 365 Financessa.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c48011c9988bdca694851476540db574efef7909
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879560"
---
# <a name="set-up-main-account-categories"></a>Päätilin luokkien määritys

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit määrittää päätilien luokat. Päätilin luokkia käytetään raportoinnin oletusraporteissa ja Power BI:ssa. Oletusarvoisesti luodut päätilin luokille voidaan määrittää uusi nimi mutta niitä ei voi poistaa. Tililuokkia voidaan luoda lisää raportointia ja analysointia varten. Artikkelissa käytetään USMF-demoyritystä.

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
