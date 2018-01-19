---
title: "Tilausilmoitusten näyttäminen myyntipisteessä"
description: "Tässä aiheessa käsitellään tilausilmoitusten ottamista käyttöön myyntipisteessä ja muiden toimintoihin laajennettavissa olevaa ilmoituskehikkoa."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Ilmoitusten näyttäminen myyntipisteessä

Nykyaikaisessa vähittäismyyntiympäristössä myyjillä on monenlaisissa tehtäviä, kuten asiakaspalvelua, tapahtumien kirjaamista, inventointia ja tilausten vastaanottamista myymälässä. Myyntipisteen asiakasohjelma auttaa myyjiä tekemään nämä tehtävät ja paljon muuta – samassa sovelluksessa. Koska myyjien on tehtävä päivän aikana monenlaisia tehtäviä, heille on ehkä erikseen ilmoitettava, jos heidän on hoidettava jokin tehtävä. Myyntipisteen ilmoituskehikko ratkaisee tämän ongelman niin, että jälleenmyyjät voivat määrittää roolipohjaisia ilmoituksia. Dynamics 365 for Retailin sovelluspäivityksessä 5 nämä ilmoitukset voidaan määrittää vain myyntipistetoiminnoille.

Tällä hetkellä järjestelmässä voi näyttää tilauksen täyttämistoiminnon ilmoituksia. Kehikko on kuitenkin suunniteltu laajennettavaksi, joten jatkossa kehittäjät voivat muodostaa ilmoituskäsittelijän mille tahansa toiminnolle ja näyttää ilmoitukset myyntipisteessä.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Tilauksen täyttämistoimintojen ilmoitusten ottaminen käyttöön

Voit ottaa tilauksen täyttämistoimintojen ilmoituksen käyttöön seuraavien ohjeiden mukaisesti:

 - Siirry **Toiminnot**-sivulle (**Vähittäismyynti** > **Kanavan asetukset** > **POS-asetukset** > **Myyntipisteen** > **Toiminnot**).
 - Etsi tilauksen täyttämistoiminto ja valitse toiminnon **Ota ilmoitukset käyttöön** -valintaruutu. Tämän valinnan jälkeen ilmoituskehikko kuuntelee tilauksen täyttämistoiminnon käsittelijää. Jos käsittelijä on toteutettu, ilmoitukset näytetään myyntipisteessä. Muussa tapauksessa kyseisen toiminnon ilmoituksia ei näytetä.
- Siirry työtekijöihin liitettyihin myyntipisteen käyttöoikeuksiin ja lisää **Ilmoitukset**-pikavälilehdessä tilauksen täyttämistoiminto siten, että sen näyttöjärjestyksen arvo on 1. Jos ilmoituksia on määritetty useita, näyttöjärjestys järjestää ilmoitukset ylhäältä alaspäin siten, että 1 on ylimpänä. Vain ne toiminnot voidaan lisätä, joissa **Ota ilmoitukset käyttöön** -valintaruutu on valittu. Ilmoitukset näytetään lisäksi vain niille toiminnoille, jotka on lisätty tässä välilehdessä, ja vain niille työntekijöille, joille toiminnot on lisätty vastaaviin myyntipisteen käyttöoikeuksiin. 

> [!NOTE]
> Ilmoitukset voidaan ohittaa käyttäjätasolla siirtymällä työntekijän tietueeseen, valitsemalla **Myyntipisteen käyttöoikeudet** ja muokkaamalla siten kyseisen käyttäjän ilmoitusten tilausta.

 - Siirry **Toimintoprofiili**-sivulle (**Vähittäismyynti** > **Kanavan asetukset** > **POS-asetukset** > **POS-profiilit** > **Toimintoprofiilit**). Päivitä **Ilmoitusväli**-ominaisuus määrittämällä minuutteina, kuinka usein ilmoitukset noudetaan. Arvoksi kannattaa valita 10 minuuttia, jotta pääkonttoriin ei synny turhaa viestintää. Jos ilmoitusväliksi valitaan 0, ilmoitukset poistetaan käytöstä.  

 - Valitse **Vähittäismyynti** > **Vähittäismyynnin IT** > **Jakeluaikataulu**. Synkronoi ilmoituksen tilausasetukset valitsemalla 1060, henkilökunta ja valitse sitten **Suorita nyt**. Synkronoi seuraavaksi käyttöoikeusväli valitsemalla 1070, kanavan konfigurointi ja valitse sitten **Suorita nyt**. 

## <a name="view-notifications-in-pos"></a>Ilmoitusten tarkastelu myyntipisteessä

Kun edellä mainitut vaiheet on suoritettu, työntekijät, joille ilmoitukset on määritetty, voivat tarkastella ilmoituksia myyntipisteessä. Voit tarkastella ilmoituksia napsauttamalla ilmoituskuvaketta myyntipisteen otsikkorivillä. Näkyviin tulee ilmoituskeskus, jossa on tilauksen täyttämistoiminnon ilmoitukset. Seuraavien tilauksen täyttämistoiminnon ryhmien pitäisi näkyä ilmoituskeskuksessa: 

- **Odottavat tilaukset** – Tässä ryhmässä näkyy odottavassa tilassa olevien tilausten määrä, kuten tilaukset, jotka myyntipisteen työntekijän on hyväksyttävä ja jolla on riittävät oikeudet myymälän täyttämiseen. Numeron napsauttaminen ryhmässä avaa **Tilauksen täyttäminen** -sivun, joka on suodatettu näyttämään vain odottavat tilaukset, jotka on määritetty täytettäväksi myymälään. Jos myymälän tilaukset hyväksytään automaattisesti, määrä tässä ryhmässä on nolla.

- **Nouto myymälästä** – Tämä ryhmä näyttää niiden tilausten määrän, joiden toimitustapa on **nouto** ja joiden nouto on aikataulutettu nykyisestä myymälästä. Numeron napsauttaminen ryhmässä avaa **Tilauksen täyttäminen** -sivun, joka on suodatettu näyttämään nykyisestä myymälästä noudettavaksi määritetyt aktiiviset tilaukset.

- **Myymälästä lähetys** – Tämä ryhmä näyttää niiden tilausten määrän, joiden toimitustapa on **lähetys** ja joiden lähetys on aikataulutettu nykyisestä myymälästä. Numeron napsauttaminen ryhmässä avaa **Tilauksen täyttäminen** -sivun, joka on suodatettu näyttämään nykyisestä myymälästä lähetettäväksi määritetyt aktiiviset tilaukset.

Kun myymälään on määritetty täyttäväksi uusia tilauksia, muuttuva ilmoituskuvake ilmoittaa uusista ilmoituksista ja vastaavien ryhmien määrät päivittyvät. Käyttäjä voi myös napsauttaa päivityskuvaketta toiminnon nimen vieressä, jolloin ryhmien määrä päivittyy välittömästi. Määrä päivitetään myös määritetyin väliajoin. Kun ryhmässä on uusi nimike, jota nykyinen työntekijä ei ole nähnyt, purskekuvake ilmaisee, että ryhmässä on uusi nimike. Ruudun napsauttaminen ilmoituksessa avaa sen toiminnon, jolle ilmoitus on määritetty. Edellä mainitussa skenaariossa ilmoitusten napsauttaminen avaa **Tilauksen täyttäminen** -sivun ja välittää soveltuvat parametrit: odottavat tilaukset, nouto myymälästä ja myymälästä lähetys. 

> [!NOTE]
> Odottavien tilausten ilmoitukset otetaan käyttöön Dynamics 365 for Retailin tulevassa päivityksessä. 


