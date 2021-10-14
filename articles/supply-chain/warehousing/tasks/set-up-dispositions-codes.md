---
title: Määritä käsittelykoodit
description: Menettely koskee sellaista palautustilauksen vastaanottoprosessin käsittelykoodin määritystä, jota voidaan käyttää mobiililaitteella.
author: Mirzaab
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb83108c934e864da0df39ec4ee36a0bc7ba7588
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574062"
---
# <a name="set-up-dispositions-codes"></a>Määritä käsittelykoodit

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]