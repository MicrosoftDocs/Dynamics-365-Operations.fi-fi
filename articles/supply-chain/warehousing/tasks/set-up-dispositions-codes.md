---
title: Määritä käsittelykoodit
description: Menettely koskee sellaista palautustilauksen vastaanottoprosessin käsittelykoodin määritystä, jota voidaan käyttää mobiililaitteella.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558004"
---
# <a name="set-up-dispositions-codes"></a>Määritä käsittelykoodit

[!include [task guide banner](../../includes/task-guide-banner.md)]

Menettely koskee sellaista palautustilauksen vastaanottoprosessin käsittelykoodin määritystä, jota voidaan käyttää mobiililaitteella. Käsittelykoodit ovat sääntökokoelma, joita voidaan käyttää nimikkeitä vastaanotettaessa. Kun esimerkiksi työn käyttäjä vastaanottaa vioittuneita nimikkeitä mobiililaitteella, käyttäjän on skannattava vioittuneiden nimikkeiden käsittelykoodi. Vastaanotettujen tavaroiden, työmallin ja sijaintidirektiivin varastotila voidaan määrittää skannatusta käsittelykoodista. Käsittelykoodin käyttö ei ole pakollista ostotilausten vastaanottoprosessissa eikä tuotantotilauksen valmiiksi ilmoittamisprosessissa. Käsittelykoodin käyttö on pakolista myyntitilauksen palautuksen vastaanottoprosessissa, jos nimikkeet on rekisteröity mobiililaitteella.  Tämän oppaan luomisessa käytetty demotietojen yritys on USMF. Tämä menettely on tarkoitettu varastopäällikölle. 

1. Valitse Varastonhallinta > Asetukset > Mobiililaite > Käsittelykoodit.
2. Valitse Uusi.
    * Luo asiakaspalautuksille uusi käsittelykoodi.  
3. Kirjoita arvo Käsittelykoodi-kenttään.
4. Valitse Varaston tila -kentässä varastotila, jossa on varastoesto.
    * Jos USMF on käytössä, valitse Esto. Voit lisätä varaston tilan käsittelykoodiin. Se ohittaa tilausriveillä olevan oletustilan.  
5. Kirjoita Työmalli-kenttään arvo.
    * Valinnainen: Valitse palautustilaukseen liitetty työmallikoodi. Jos arvoa ei ole annettu, työmalli selvitetään käyttämällä järjestelmään määritettyjä vakiosääntöjä. Työmallin valitseminen rajoittaa prosesseja, joiden kanssa käsittelykoodia voidaan käyttää. Jos esimerkiksi käsittelykoodissa on työmalli, joka työtilaustyyppi on ostotilaus, sillä ei voi rekisteröidä asiakkaiden palauttamia nimikkeitä.  
6. Kirjoita arvo Palauta käsittelykoodi -kenttään.
    * Palautuksen käsittelykoodi määrittää rekisteröityjen nimikkeiden jäljellä olevat palautustilausprosessit. Tässä esimerkissä asiakkaan pitäisi saada hyvityslasku. Lisää palautuksen käsittelykoodi, joka sisältää hyvitystoiminnon.  

