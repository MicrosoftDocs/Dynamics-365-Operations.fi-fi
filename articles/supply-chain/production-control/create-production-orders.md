---
title: Tuotantotilauksen elinkaari – yleiskatsaus
description: Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68758f4ddf39b4b8f7f0758f9e59e17c3411723a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246306"
---
# <a name="production-order-lifecycle-overview"></a>Tuotantotilauksen elinkaari – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.

Tuotantotilaus etenee tuotannon elinkaaren vaiheesta toiseen. Kun tilaus luodaan, sen tilaksi määritetään **Luotu**. Kun tilaus on valmis, sen tilaksi määritetään **Päättynyt**. Käyttäjä voi määrittää kunkin vaiheen kyseisen vaiheen parametriasetuksella. Asetus voidaan määrittää yhdelle käyttäjälle tai kaikille käyttäjille.

Tuotannon tuoterakenne ja tuotantoreititys ovat tuotantotilauksen tärkeimmät yksiköt. Ne kopioidaan tuotantotilaukseen tuotettavaksi valitun nimikkeen ja määrän perusteella. Tuotannon tuoterakennetta ja reititystä voidaan muokata ennen tuotantotilauksen aloittamista.

Tuotantotilaus voidaan luoda seuraavilla tavoilla:

-   Luotu toteuttamalla materiaaliin kysyntään perustuva pääsuunnittelu.
-   Luotu suoraan myyntitilausriviltä tai luotaessa ja arvioitaessa ylemmän tason tuotantotilaus (tarvekohdistus).
-   Luo manuaalisesti.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]