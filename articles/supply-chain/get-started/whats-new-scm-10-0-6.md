---
title: Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio10.0.6 (marraskuu 2019)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.6 uusia tai muuttuneita ominaisuuksia.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909326"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio10.0.6 (marraskuu 2019)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.6 uusia tai muuttuneita ominaisuuksia. Tämän version koontiversion numero on 10.0.234. Kun yleisen saatavuuden päivämäärä on marraskuussa, uudet toiminnot ovat käytettävissä lokakuun esiversiossa. Lisätietoja versiosta 10.0.6 on kohdassa [Lisäresurssit](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Tuotekonfiguraatiomallien V2:n tietoyksikkö

Toinen tuotekonfiguraatiomallien tietoyksikön versio julkaistaan (nimeltä tuotekonfiguraatiomallit V2). 418-tuotekonfiguraatiomallit-oletusmalli tarvitaan myös. Se käyttää uutta tuotekonfiguraatiomallit V2 -tietoyksikköä tuonnin ja viennin ympäristömalleissa. Mallia ei päivitetä automaattisesti. Se on siis ladattava oletustiedoista manuaalisesti. V2-yksikkö vie yhden rivin erillisenä tiedostona liitteeseen sisäisen rivin sijaan. Näin ratkaistaan V1-yksikön kokorajoitukset. 
 
Mitä tarvitaan, jotta tämä muutos voidaan tehdä?
-    Koska V1-yksikkö on vanhentunut, tulee alkaa siirtyä V1-yksiköstä V2-yksikköön. Jos käytössä on 418-tuotekonfiguraatiomallit-malli, voit valita Lataa oletusmallit -painikkeen ja ladata 418-tuotekonfiguraatiomallit-mallin uudelleen.
-    Jos haluat säilyttää yhteensopivuuden olemassa olevien järjestelmien kanssa, voit nyt jatkaa olemassa olevan mallin ja vanhentuneen V1-yksikön käyttämistä niin kauan, kunnes siirrät integroinnit uuteen malliin. 

## <a name="feature-management-enhancements"></a>Ominaisuuksien hallinnan parannukset
Ominaisuuksien hallinnan avulla voit nyt ottaa käyttöön kaikki uudet toiminnot oletusarvoisesti, pyytää vahvistusta toiminnon käyttöönottoa varten ja ottaa käyttöön kaikki toiminnot, jotka vielä eivät ole käytössä. 


## <a name="purchase-agreement-responsible-party"></a>Ostosopimuksen vastuullinen osapuoli
Nyt voit määrittää ensisijaiset ja toissijaiset vastuulliset osapuolet Ostosopimuksen luokitus -lomakkeessa ja tuloksena olevissa ostosopimuksissa.  Tämä antaa käyttäjille mahdollisuuden valvoa sopimuksia.

## <a name="rfq-link-on-the-purchase-order-line"></a>Tarjouspyynnön linkki ostotilausriviin
Voit lisätä viitelinkin ostotilausriveiltä takaisin vastaaviin tarjouspyyntöriveihin, joista linkit ovat lähtöisin. Näin käyttäjät voivat helposti käyttää tarjousasiakirjan tukipyyntöjä.

## <a name="additional-resources"></a>Lisäresurssit

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset
Saat lisätietoja version 10.0.6 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Ympäristön update 30 -päivitys
Microsoft Dynamics 365 Supply Chain Management 10.0.6 sisältää Platform update 30:n. Lisätietoja Platform update 30:sta on kohdassa [Platform update 30:n uudet ja muuttuneet ominaisuudet](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelma
Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Tutustu kohtaan [Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelma](/dynamics365-release-plan/2019wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]