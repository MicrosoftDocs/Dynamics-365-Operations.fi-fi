---
title: Tuotantotilauksen elinkaari – yleiskatsaus
description: Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: df773cf13b8ccd9ee4f861955b1a4321af38a150
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811795"
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