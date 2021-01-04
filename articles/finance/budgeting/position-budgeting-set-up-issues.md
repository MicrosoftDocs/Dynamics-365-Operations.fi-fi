---
title: Sijoita budjetoinnin vianmääritys
description: Tässä artikkelissa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität toimen budjetointia. Se vastaa usein kysyttyyn kysymykseen, kuinka budjetin kustannustasoja, kompensaatioryhmiä ja kompensaatioruudukoita luodaan.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afddc9815ee3864236f93c8400bcf116d5b6cc89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442858"
---
# <a name="position-budgeting-troubleshooting"></a>Sijoita budjetoinnin vianmääritys

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität toimen budjetointia. Se vastaa usein kysyttyyn kysymykseen, kuinka budjetin kustannustasoja, kompensaatioryhmiä ja kompensaatioruudukoita luodaan. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Miksi ennusteen toimen sivua ei löydy henkilöstöhallinnosta?
---------------------------------------------------------------

Ennusteen toimet on siirretty budjetointiin.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Miksi en voi poistaa budjetin kustannuselementtiä?
Et voi poistaa budjetin kustannustasoa, koska se on määritetty ennusteen toimeen. Ennen kuin voit poistaa budjetin kustannustason, se on poistettava kaikista ennusteen toimista. **Vihje:** Jos haluat etsiä kaikki toimet, jotka on määritetty budjetin kustannustasolle, valitse kustannustaso **Budjetin kustannustasot** -sivulla ja valitse sitten **Päivitä toimet**. Ylemmässä ruudukossa näkyvät kustannustasoa käyttävät toimet.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Kuinka voin poistaa kustannustason useista ennusteen toimista avaamatta jokaista?
Kustannustasoa ei voi poistaa. Jos kuitenkin muutat alkamis- ja päättymispäivän budjettisuunnittelujakson päivämäärien ulkopuolelle, kustannustasoa ei enää määritetä ennusteen toimiin kyseisessä budjettisuunnittelujaksossa. Voit tehdä tämän avaamalla budjetin kustannustason. Valitse sitten **Kustannuslaskenta**-pikavälilehdellä **Muuta päivämääriä** ja muuta voimassaolopäivämäärää tai vanhentumispäivämäärää. Päivitä kaikki ennusteen toimet, joihin kustannustaso liittyy valitsemalla **OK**. **Vihje:** Jos käytät tätä tapaa, huomaa, että se poistaa budjetoidut kustannuselementit **kaikista** ennusteen toimista, joissa alku- ja loppupäivämäärät eivät enää sijoitu määrätyn alueen sisään. Jos tämä ei ole aikomuksesi, sinun pitää avata kunkin ennusteen toimi, josta haluat poistaa budjetin kustannuselementin, ja tehdä muutos manuaalisesti.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Miksi en voi syöttää vuosittaista summaa budjetin kustannuselementin Kustannuslaskenta-pikavälilehdessä?
Et voi kirjoittaa vuosittaista määrää, jos **Laskuperuste**-pikavälilehdellä on budjetin kustannustasoja, koska järjestelmä edellyttää prosenttiosuutta arvon laskemiseksi. Jos haluat muuttaa arvoa, poista kaikki budjetin kustannustasot **Laskuperuste**-pikavälilehdestä.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Miksi en voi muuttaa budjetin kustannustyyppiä Ansio-tyypistä toiseksi budjetin tyypiksi?
Eräät budjetin kustannustasoista ovat Ansio-kustannustasoja laskennan perusteella. Jos haluat muuttaa **Budjetin kustannustyyppi** -kenttää, poista ansion kustannustaso kaikkien budjetin kustannustasojen **Laskuperuste**-pikavälilehdestä.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Miksi en voi muuttaa budjetin kustannuselementin rivien päivämäärää budjetin kustannuselementissä?
Et voi muuttaa budjettikustannustason rivin päivämäärää, kun ennusteen toimi käyttää budjetin kustannustasoa. Tämä rajoitus auttaa varmistamaan, että ennusteen toimet noudattavat aina budjetin kustannustasojen määrittämiä ohjeita. Jos haluat muuttaa päivämäärää, valitse **Kustannuslaskenta**-pikavälilehdessä **Muuta päivämääriä** ja lisää uudet päivämäärät. Päivitä kaikki toimet, joihin kustannustaso liittyy valitsemalla **OK**.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Miksi en voi muuttaa budjetin kustannustasoa kompensaatioryhmän sivulla?
Voit luoda ja muuttaa budjetin kustannustasoja vain **Budjetin kustannustasot** -sivulla.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Miksi näyttöön tulee virhesanoma, kun muutan kustannustason päivämäärää ennusteen toimessa?
Ennusteen toimen kustannustasorivin päivämäärien tulee olla seuraavien alueiden sisällä:

-   Toimen aktivointi- ja päättymispäivämäärät.
-   Budjetin kustannustason voimaantulo- ja vanhentumispäivämäärät.
-   Ennusteen toimen budjettisuunnitteluprosessin kanssa liitetyn budjettijakson alku- ja loppupäivämäärät.




