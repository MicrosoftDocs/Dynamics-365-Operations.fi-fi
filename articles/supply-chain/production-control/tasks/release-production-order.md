---
title: Tuotantotilauksen vapauttaminen
description: Tässä menettelyssä näytetään, miten tuotantotilaus vapautetaan.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2676d9fd98ce7166f011cf55d043c6f48fc4cc93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836186"
---
# <a name="release-a-production-order"></a>Tuotantotilauksen vapauttaminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten tuotantotilaus vapautetaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on neljäs seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.

1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
    * Valitse ruudukossa tuotantotilaus, jonka tila on Ajoitettu.  
2. Valitse toimintoruudussa Tuotantotilaus.
3. Valitse Vapauta.
    * Voit vahvistaa tällä sivulla valittujen tuotantotilausten vapautuksen. Lisää tilauksia valitsemalla Valitse.  
    * Vapautusvaihe osoittaa, milloin tuotantotilaus vapautetaan tuotannon työnohjaukseen. Tällöin työnohjauksen käyttäjät voivat raportoida tuotannon töiden etenemisestä. Töiden käsittelyä koskevaa tärkeää tietoa sisältävät tuotannon dokumentit voidaan luoda. Raaka-aineiden keräilyä koskeva varastotyö luodaan nimikkeille, jotka on määritetty varastoprosessia varten.  
4. Valitse Yleiset-välilehti.
    * Määritä, mitkä tuotantoraportit tulostetaan. Työkortti-raportti tulostaa sivun jokaisesta ajoitetusta työstä. Se vaatii tuotantotilauksen ajoituksen työtasolla. Raportti sisältää tietoja ajoituksen aloitus- ja päättymisajasta, tuotettavasta määrästä ja työn suorittavasta resurssista. Reititystyöt-raportti kerää samat tiedot samalla sivulla, mutta ei tulosta sivua kunkin työn kohdalla. Reitityskortti-raportti näyttää ainoastaan toiminnot, ei töitä. Tämän vuoksi töiden ajoittaminen ei ole pakollista tässä raportissa, mutta sitä voidaan käyttää, kun tuotantotilaukset on ajoitettu työvaiheen tasolla.  
5. Valitse Tulosta reitityskortti -valintaruutu.
6. Valitse OK.
7. Sulje sivu.

