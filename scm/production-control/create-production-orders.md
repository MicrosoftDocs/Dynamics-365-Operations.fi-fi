---
title: Luo tuotantotilauksia
description: "Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b55c4c729350fbe8311953cc21f85bb4122f39f8
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="create-production-orders"></a>Luo tuotantotilauksia

[!include[banner](../includes/banner.md)]


Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.

Tuotantotilaus etenee tuotannon elinkaaren vaiheesta toiseen. Kun tilaus luodaan, sen tilaksi määritetään **Luotu**. Kun tilaus on valmis, sen tilaksi määritetään **Päättynyt**. Käyttäjä voi määrittää kunkin vaiheen kyseisen vaiheen parametriasetuksella. Asetus voidaan määrittää yhdelle käyttäjälle tai kaikille käyttäjille.

Tuotannon tuoterakenne ja tuotantoreititys ovat tuotantotilauksen tärkeimmät yksiköt. Ne kopioidaan tuotantotilaukseen tuotettavaksi valitun nimikkeen ja määrän perusteella. Tuotannon tuoterakennetta ja reititystä voidaan muokata ennen tuotantotilauksen aloittamista.

Tuotantotilaus voidaan luoda seuraavilla tavoilla:

-   Luotu toteuttamalla materiaaliin kysyntään perustuva pääsuunnittelu.
-   Luotu suoraan myyntitilausriviltä tai luotaessa ja arvioitaessa ylemmän tason tuotantotilaus (tarvekohdistus).
-   Luo manuaalisesti.





