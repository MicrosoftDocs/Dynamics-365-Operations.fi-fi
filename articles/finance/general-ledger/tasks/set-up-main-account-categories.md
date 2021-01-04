---
title: Määritä päätilien luokat
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää päätilien luokat Dynamics 365 Financeissa.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442694"
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
