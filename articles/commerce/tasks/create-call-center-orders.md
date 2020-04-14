---
title: Luo puhelinkeskustilauksia
description: Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141427"
---
# <a name="create-call-center-orders"></a>Luo puhelinkeskustilauksia

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta. Tässä menettelyssä käytetään esittely-yritystä USRT. Tämä on tarkoitettu myyntitilauksia käsittelevälle assistentille. Edellytykset: Menettelyn suorittava käyttäjä on määritetty puhelinkeskuksen käyttäjiksi. Julkaistussa Fabrikamin puolivuosittaisessa luettelossa on vähintään yksi lähdekoodi.

1. Valitse Retail ja Commerce > Asiakkaat > Asiakaspalvelu.
2. Syötä SearchText-kenttään hakuehdot, joilla etsit asiakasta.
    * Valitse tässä esimerkissä menettelytyypiksi Nieminen ja paina sarkainnäppäintä.  
3. Valitse Haku.
    * Koska esittelytiedoissa on vain yksi asiakas nimeltä Nieminen, hänet valitaan automaattisesti.  
4. Valitse Uusi myyntitilaus.
5. Laajenna tai tiivistä Myyntitilauksen otsikko -osa.
6. Valitse luettelon lähdekoodi.
    * Jos aktiivisia lähdekoodeja ei ole, voit sulkea Lähde-kentän ja ohittaa tämän vaiheen.  
7. Valitse Lisää rivi.
8. Syötä Nimiketunnus-kenttään nimikkeen hakuehto.
    * Syötä tässä mallimenettelyssä osittainen nimikenumero 8111 ja paina sarkainnäppäintä. Nimike tulee esille hakuikkunaan.  
9. Myyntitilaukseen lisättävän tuotteen valitseminen
10. Syötä myyntimäärä.
11. Valitse Luo.
12. Valitse Valmis, kun haluat tarkistaa asiakkaan maksun.
13. ValitseLisää.
    * Lisää-linkki löytyy Maksut-välilehdestä. Laajenna Maksut-välilehti, jos se on tiivistetty.  
14. Valitse maksutapa.
    * Valitse tässä menettelyssä käteismaksutapa.  
15. Sulje sivu.
16. Anna määrä.
    * Syötä tässä menettelyssä tilaussummaksi summa, joka löytyy Myyntitilauksen yhteenveto -sivun summakentän vasemmalta puolelta. Näin voit määrittää tilauksen kokonaan maksetuksi.  
17. Valitse OK.
18. Valitse Lähetä.

