---
title: Ylläpitoennusteet
description: Tässä ohjeaiheessa kerrotaan ylläpitoennusteista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875633"
---
# <a name="maintenance-forecasts"></a>Ylläpitoennusteet

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Kun luot työtilauksen, luot työtilaustyöt, joissa on vastaavat käyttöomaisuudet ja kunnossapitotyölajit. Kun huoltoennusteita sisältävä kunnossapitotöiden tyyppi valitaan, ennusteet kopioidaan automaattisesti työtilaukseen.

Voit ehkä lisätä tai poistaa työtilauksen ennusterivejä. Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata ennusterivejä. 

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta ja valitse sitten **Ennuste.** **Työtilauksen ylläpitoennuste** -kohdassa näytetään työtilaustyössä valitun ylläpitotyön tyypin ennusterivit.


## <a name="add-hours-forecast-to-a-work-order"></a>Lisää tuntiennuste työtilaukseen

1. Valitse työtilaustyö, johon haluat lisätä ennusteen.

2. Luo uusi rivi napsauttamalla **Tunnit**-pikavälilehdellä **Lisää**.

3. Valitse luokka **Luokka**-kentässä.

4. Lisää ennustettujen tuntien määrä **Tunnit**-kenttään.

5. Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.


## <a name="add-items-forecast-to-a-work-order"></a>Lisää nimike-ennuste työtilaukseen

Voit lisätä nimikkeitä työtilauksen ylläpitoennusteeseen kolmella tavalla: Voit luoda rivejä nimikkeille (varaosille), jotka eivät sisälly varaosaluetteloon tai käyttöomaisuuden tuoterakenteeseen, voit valita varaosia hyväksytystä varaosaluettelosta ja voit valita nimikkeitä resurssin tuoterakenteesta.

1. Valitse työtilaustyö, johon haluat lisätä ennusteen.

2. Valitse **Nimikkeet**-pikavälilehti.

3. Valitse **Lisää**, jos haluat luoda uuden rivin varaosalle, joka ei ole varaosaluettelossa tai käyttöomaisuuden tuoterakenneluettelossa.

4. Valitse **Nimiketunnus**-kentässä nimike.

5. Lisää määrä **Myyntimäärä**-kenttään ja valitse määrän yksikkö **Yksikkö** -kentässä.

6. Lisää kustannushinta ja valuutta asianmukaisiin kenttiin ja valitse **Rivin ominaisuus**.

7. Jos haluat muuttaa nimikeriveillä näkyvien dimensioiden luetteloa, valitse **Varasto** > **Näytä dimensiot**, valitse dimensiot ja valitse sitten **Tallenna asetukset** -vaihtopainikkeessa Kyllä.

8. Jos haluat lisätä huoltoennusteeseen hyväksytyn varaosan, valitse **Lisää varaosia**, valitse varaosa, muokkaa tietoja tarvittaessa ja valitse **OK.**

9. Jos haluat lisätä käyttöomaisuuden tuoterakennenimikkeitä ennusteeseen, valitse **Lisää tuoterakennenimikkeitä**, valitse nimike, muokkaa siihen liittyviä tietoja tarvittaessa ja valitse **OK.**

10. Valitse **Nimike, missä käytetty**saadaksesi yleiskatsauksen siitä, missä resurssien hallinnassa valitulla rivillä olevaa nimikettä käytetään suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin. 



## <a name="add-expense-forecast-to-a-work-order"></a>Lisää kuluennuste työtilaukseen

1. Tässä ohjeaiheessa selitetään, kuinka voit lisätä kuluennusteen työtilaukseen. Valitse lomakkeen vasemmasta reunasta työtilaustyö, johon haluat lisätä ennusteen.

2. Valitse **Kulu**-pikavälilehti.

3. Luo uusi rivi valitsemalla **Lisää**.

4. Valitse luokka **Luokka**-kentässä.

5. Anna määrä **Määrä**-kenttään.

6. Lisää kustannushinta, myyntivaluutta ja myyntihinta asianmukaisiin kenttiin.

7. Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.

>[!NOTE]
>**Ylläpitoennusteen summat** -pikavälilehdessä näkyy yhteenveto kussakin välilehdessä luotujen rivien määrästä valitussa työtilaustyössä ja työtilauksessa. Voit myös tarkastella työtilaustyön ja työtilauksen ennustettujen työtuntien summaa.

![Kuva 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Työtilausennusteiden automaattinen päivitys

Käyttöomaisuuden hallinnassa voit päivittää automaattisesti työtilausten ennusteiden muutokset, jotka koskevat tuntikustannuksia, nimikekustannuksia ja kuluja, jotka on päivitetty Dynamics 365 for Finance and Operations -järjestelmän muissa moduuleissa. Näin varmistat, että viimeisimpiä kustannushintoja käytetään aina työtilausennusteissa. Samanlaisia päivityksiä voidaan tehdä myös [kunnossapitotöiden tyyppien ennusteille.](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

1. Valitse **Resurssien hallinta** > **Kausittainen** > **Ennuste** > **Päivitä työtilauksen ennuste**.

2. Avattavassa **Päivitä työtilauksen ennuste** -valintaikkunassa voit lisätä tarvittaessa tiettyjä työtilauksia tai työtilaustöitä koskevia valintoja. Tee haluamasi valinnat valitsemalla **Suodata**.

3. **Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.

4. Käynnistä ennusteen päivitys valitsemalla **OK**.


![Kuva 2](media/07-work-orders.png)

