---
title: Kirjojen määrä kirjauskansiota kohti
description: Tässä ohjeaiheessa on tietoja kirjauskansioiden ja resurssin kirjojen välisistä suhteista, kun käyttöomaisuushankinta tai poistoehdotus tehdään erätyön kautta. Voit määrittää kuhunkin hankintaan ja poistoon sisällytettävien kirjojen enimmäismäärän.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d8c6a3aab9063e1f2143c10f9e442001660dc121bfee0b3b2c9e17ade5f762e2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767029"
---
# <a name="number-of-books-per-journal"></a>Kirjojen määrä kirjauskansiota kohti

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja kirjauskansioiden ja resurssin kirjojen välisistä suhteista, kun käyttöomaisuushankinta tai poistoehdotus tehdään erätyön kautta. Voit määrittää kuhunkin hankintaan ja poistoon sisällytettävien kirjojen enimmäismäärän käyttämällä **Kirjojen määrä kirjauskansion mukaan** -osan **Yleistiedot**-välilehden **Käyttöomaisuusparametrit**-sivun kenttiä (**Käyttöomaisuus \> Asetukset \> Käyttöomaisuusparametrit**). Näiden kenttien avulla voit jakaa käyttöomaisuuskirjojen määrän hankintakirjauskansiota ja poistokirjauskansiota kohden.

Hankintaehdotuksen oletusarvo on vähintään 10 000 kirjaa. Poistoehdotuksen oletusarvo on vähintään 2 000 kirjaa.

Jos käyttöomaisuuseriä on esimerkiksi 4 000, kuhunkin erään liitetään kaksi kirjaa. Yksi kirja kirjataan nykyiselle tasolle ja toinen verotasolle. Jos hankit 4 000 käyttöomaisuuserää eräkäsittelyn avulla, erätyö, joka luo yhden käyttöomaisuuserän hankintakirjauskansion, sisältää 4 000 käyttöomaisuuskirjaa.

> [!NOTE]
> Luotua kirjauskansiota käytetään edelleen, kunnes erätyö on päättynyt.
>
> Johdetut kirjat eivät sisälly kirjauskansion kirjauskansiokohtaiseen enimmäismäärään.

Eräkäsittelyn avulla voidaan suorittaa poistot samasta hankittujen käyttöomaisuuserien joukosta. Erätyö luo esimerkiksi kaksi poistokirjauskansiota, joista jokainen sisältää 2 000 käyttöomaisuuskirjaa. Ensimmäinen kirjauskansio sisältää kirjoja, jotka on liitetty käyttöomaisuuseriksi, joiden numero on 1-2 000. Toinen kirjauskansio sisältää kirjoja, jotka on liitetty käyttöomaisuuseriksi, joiden numero on 2 001–4 000.

Eräkäsittelytyö sulkee pois suljetut kirjat. Esimerkiksi poistojen eräajossa 10 ensimmäistä kirjaa 2 000 kirjasta on suljettu. Tässä tapauksessa ensimmäinen kirjauskansio sisältää kirjoja, jotka on liitetty käyttöomaisuuseriksi, joiden numero on 1-2 011. Toinen kirjauskansio sisältää kirjoja, jotka on liitetty käyttöomaisuuseriksi, joiden numero on 2 012–4 000.

> [!NOTE]
> Jos sinulla on käyttöomaisuustunnuksen, joilla on eri erottimet (kuten – tai /), ja luot käyttöomaisuustapahtumia eräajoissa, kullekin erotintyypille on tehtävä erillinen eräajo. Järjestelmä ei voi käsitellä eri erottimia samassa eräajossa.

Kirjojen määrää rajoitetaan, jos samassa kirjauskansiossa ei ole päällekkäisiä käyttöomaisuuerien tunnuksia. Jos käyttöomaisuuserän tunnus on kuitenkin sama kuin kirjan tunnus, kirjauskansion kirjojen määrä voidaan ylittää, jotta käyttöomaisuustunnus säilyy samassa kirjauskansiossa.

Jos esimerkiksi käyttöomaisuustunnuksia on 5 001, kuhunkin käyttöomaisuustunnukseen liitetään kolme kirjaa ja kukin käyttöomaisuuskirja kirjataan samalle kirjaustasolle. Poisto suoritetaan kolmen peräkkäisen kuukauden ajan ilman yhteenvetoa.  Poistokirjauskansio luodaan erätyönä, ja järjestelmä luo seitsemän kirjauskansiota, joissa on 667 käyttöomaisuustunnusta ja kolme kirjaa kutakin käyttöomaisuustunnusta kohden. Tuloksena on 2 001 kirjaa. Tämän vuoksi kolmen kuukauden aikana on 6 003 kirjauskansioriviä ylläpitävät samoja käyttöomaisuustunnuksia samassa kirjauskansiossa. Järjestelmä luo myös yhden kirjauskansion, jossa on 332 käyttöomaisuustunnusta ja kolme kirjaa kutakin käyttöomaisuustunnusta kohden. Kolmessa kuukaudessa saadaan 2 988 riviä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
