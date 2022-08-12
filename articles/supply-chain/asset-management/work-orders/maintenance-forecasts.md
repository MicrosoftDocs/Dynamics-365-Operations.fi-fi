---
title: Ylläpitoennusteet
description: Tässä artikkelissa kerrotaan ylläpitoennusteista resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4e3da8ab9a739c8455d2c1d2720f94f91a42927d
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111597"
---
# <a name="maintenance-forecasts"></a>Ylläpitoennusteet

[!include [banner](../../includes/banner.md)]



Kun luot työtilauksen, luot työtilaustehtäviä, joilla on siihen liittyvät resurssit ja ylläpitotyötyypit. Kun ylläpitoennusteita sisältävä ylläpitopitotöiden tyyppi valitaan, ennusteet kopioidaan automaattisesti työtilaukseen.

Saatat voida lisätä ennusterivejä työtilaukseen tai poistaa niitä työtilauksesta. Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata ennusterivejä. Lisätietoja työtilausten elinkaaritiloista ja niihin liittyvistä projektin vaiheista on kohdassa [Ennusteet, työtilaukset ja projektit](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Valitse **Resurssien hallinta** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta ja sitten toimintoruudun > **Työtilaus**-välilehden > **Projekti**-ryhmässä **Ennuste**. **Työtilauksen ylläpitoennuste** -sivulla näytetään työtilaustehtävässä valitun ylläpitotyön tyypin ennusterivit.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Tuntiennusteen lisääminen työtilaukseen

1. Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.

2. Luo uusi rivi valitsemalla **Tunnit**-pikavälilehdellä **Lisää**.

3. Valitse luokka **Luokka**-kentässä.

4. Lisää ennustettujen tuntien määrä **Tunnit**-kenttään.

5. Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.


## <a name="add-an-items-forecast-to-a-work-order"></a>Nimike-ennusteen lisääminen työtilaukseen

Työtilauksen ylläpitoennusteeseen voi lisätä nimikkeitä kolmella tavalla. Voit luoda rivejä nimikkeille (varaosille), jotka eivät sisälly varaosaluetteloon tai resurssirakenteeseen (BOM), voit valita varaosia hyväksytystä varaosaluettelosta tai voit valita nimikkeitä resurssirakenteesta.

- Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.

- Lisää **Nimikkeet**-pikavälilehdessä nimikkeitä ylläpitoennusteeseen käyttämällä asianmukaista menetelmää.

Voit luoda rivin varaosalle, joka ei ole varaosaluettelossa tai resurssirakenteessa, seuraavalla tavalla:

1. Valitse **Lisää**.
2. Valitse **Nimiketunnus**-kentässä nimike.
3. Syötä määrä **Myyntimäärä**-kenttään.
4. Valitse määrän mittayksikkö **Yksikkö**-kentästä.
5. Valitse **Kustannushinta**- ja **Valuutta**-kenttiin asianmukaiset arvot.
6. Valitse rivin ominaisuus kentästä **Rivin ominaisuus**.
7. Jos haluat muuttaa nimikeriveillä näkyvien dimensioiden luetteloa, valitse **Varasto** > **Näytä dimensiot**,valitse dimensiot ja aseta sitten **Tallenna määritys** -asetuksen arvoksi **Kyllä**.

Voit lisätä varaosan hyväksytystä varaosaluettelosta seuraavasti:

1. Valitse **Lisää varaosia**.
2. Valitse varaosa ja muokkaa siihen liittyviä tietoja tarpeen mukaan.
3. Valitse **OK**.

Voit lisätä nimekkeen resurssirakenteesta seuraavasti:

1. Valitse **Lisää resurssirakennenimikkeitä**.
2. Valitse nimike ja muokkaa siihen liittyviä tietoja tarpeen mukaan.
3. Valitse **OK**.

Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**. Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Kuluennusteen lisääminen työtilaukseen

1. Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.

2. Luo rivi valitsemalla **Kulu**-pikavälilehdellä **Lisää**.

3. Valitse luokka **Luokka**-kentässä.

4. Anna määrä **Määrä**-kenttään.

5. Syötä asianmukaiset arvot kenttiin **Kustannushinta**, **Myyntivaluutta** ja **Myyntihinta**.

6. Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.

>[!NOTE]
>**Ylläpitoennusteen summat** -pikavälilehdessä näkyy yhteenveto kussakin pikavälilehdessä luotujen rivien määrästä valitussa työtilaustehtävässä ja työtilauksessa. Voit myös tarkastella työtilaustyön ja työtilauksen ennustettujen työtuntien summaa.

Seuraavassa kuvassa on esimerkki **Työtilauksen ylläpitoennuste** -sivusta.

![Kuva 1.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Työtilausennusteiden automaattinen päivitys

Jos tuntikustannuksia, nimikekustannuksia ja kuluja päivitetään muissa moduuleissa, resurssien hallinnan työtilausten ennusteet voidaan päivittää automaattisesti kyseisten muutosten mukaisesti. Tämä ominaisuus auttaa varmistamaan, että työtilausennusteissa käytetään aina viimeisimpiä kustannushintoja. Samanlaisia päivityksiä voidaan tehdä myös [kunnossapitotöiden tyyppien ennusteille.](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

1. Valitse **Resurssienhallinta** > **Kausittainen** > **Ennuste** > **Päivitä työtilauksen ennuste**.

2. Voit tarvittaessa lisätä tiettyjä työtilauksia tai työtilaustehtäviä koskevia valintoja **Päivitä työtilauksen ennuste** -valintaikkunan **Sisällytettävät tietueet** -pikavälilehdessä Tee tarvittavat valinnat valitsemalla **Suodata**.

3. **Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.

4. Käynnistä ennusteen päivitys valitsemalla **OK**.


Seuraavassa kuvassa on esimerkki **Päivitä työtilauksen ennuste** -valintaikkunasta.

![Kuva 2.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
