---
title: Luokitukset ja arvostelut – yleiskatsaus
description: Tämä artikkeli sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.
author: gvrmohanreddy
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 1f0d3ed5d95ad49cb09cf1f89d0f4c8c07620b92
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785132"
---
# <a name="ratings-and-reviews-overview"></a>Luokitukset ja arvostelut – yleiskatsaus

[!include [banner](includes/banner.md)]

Tämä artikkeli sisältää Microsoft Dynamics 365 Commercen luokitukset ja arvostelut.

Luokitukset ja arvostelut ovat tärkeä osa sähköisen kaupankäynnin asiakkaille, jotka haluavat tietää muiden asiakkaiden mielipiteen tuotteesta. Ne voivat myös auttaa kuluttajia tekemään ostopäätöksiä. Dynamics 365 Commerce -sovelluksessa luokitusten ja arvostelujen ratkaisun avulla jälleenmyyjät keräävät tuotearvosteluja ja -luokituksia asiakkailta. Jälleenmyyjät voivat tämän jälkeen näyttää keskimääräiset arvostelujen ja luokitusten tiedot sähköisen kaupankäynnin sivustossa.

Keskimääräiset luokitustiedot näytetään myyntipiste- ja puhelinkeskuskanavissa. Tämän vuoksi myyntikumppanit voivat käyttää niitä auttaessaan käyttäjiä tekemään päätöksiä. Luokitukset ja arvostelut voivat toimia myös palautemekanismina, jota jälleenmyyjät voivat käyttää parantaakseen tuotteen laatua ja kasvattaessaan samalla myyntiä.

Luokitukset ja arvostelut -toiminto Dynamics 365 Commerce -sovelluksessa on monikanavaratkaisu. Se on saatavana ympäristön osana. Luokitukset ja arvostelut -ratkaisu on luotu Microsoft Azuren avulla. Tämä mahdollistaa korkean skaalautuvuuden ja luotettavuuden.

Seuraavassa kuvassa näkyy, miten luokitukset ja arvostelut -ratkaisu toimii Dynamics 365 Commerce -sovelluksessa.

![Luokitukset ja arvostelut Dynamics 365 for Commerce -sovelluksessa.](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

Luokitukset ja arvostelut -ratkaisu Dynamics 365 Commerce -sovelluksessa käyttää Azure Cognitive Services -ratkaisua. Sen avulla tarjotaan sopimattomien sanojen valvontaa 40 kielellä. Koska valvonnassa ei tarvita ihmisiä, valvontakustannukset pienenevät. Järjestelmä tarjoaa myös valvontatyökaluja, joiden avulla voidaan vastata asiakkaiden kyselyihin, palautteeseen ja poistopyyntöihin sekä käyttäjien tietopyyntöihin.

Luokitukset ja arvostelut -ratkaisu sisältää pienoissovelluksia, jotka näyttävät arvostelujen yhteenvedot tuoteluetteloissa, hakutuloksissa, tuotetietosivulla ja muissa paikoissa. Pienoissovellukset näyttävät täydelliset luokitusluettelot ja ne sisältävät myös lajittelu- ja suodatusasetukset.

Luokitukset ja arvostelut -ratkaisu sisältää myös Business Intelligence (BI) -mallin, joka sisältää mittarijoukon. Sen avulla saadaan tietoja luokituksista ja arvosteluista. Luokitusten ja arvostelujen tiedot voidaan viedä tarkempaa analysointia varten.

Seuraavassa videossa on yleiskatsaus Dynamics 365 Commercen arvosteluista ja arvioinneista.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5c2wS]

## <a name="additional-resources"></a>Lisäresurssit

[Luokitusten ja arvostelujen käytön hyväksyminen](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)

[Tuoteluokitusten synkronoiminen Dynamics 365 Commercessa](sync-product-ratings.md)

[Salli valvojan julkaista luokituksia ja arvosteluja manuaalisesti](manual-publish-rating-reviews.md)

[Luokitusten ja arvostelujen tuominen ja vieminen](import-export-reviews.md)

[Palvelujen välisen todennuksen määrittäminen](service-to-service-auth.md)

[Luokitusten ja arvostelujen usein kysytyt kysymykset](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
