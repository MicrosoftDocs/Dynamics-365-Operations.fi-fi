---
title: "Puhelinkeskuksen kanavien määrittäminen"
description: "Tässä ohjeaiheessa on tietoja puhelinkeskusten tilausten käsittelystä Dynamics 365 for Retailin avulla."
author: josaw1
manager: AnnBe
ms.date: 04/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: d849279a642363d9cb591cd7a3b20c2883bb4a3b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-call-center-channels"></a>Puhelinkeskuksen kanavien määrittäminen

[!include [banner](includes/banner.md)]

Yritys voi määrittää useita puhelinkeskuskanavia Microsoft Dynamics 365 for Retailissa. Puhelinkeskukset määritetään valitsemalla **Retail** \> **Kanavat** \> **Puhelinkeskukset** \> **Kaikki puhelinkeskukset**. Ne ovat yrityskohtaisia.

Kun uusi puhelinkeskuskanava luodaan, sille määritetään järjestelmällisesti toimintayksikkönumero. Koska puhelinkeskukset luodaan toimintayksiköinä, käyttäjät voivat linkittää puhelinkeskuskanavat moniin Retail-ominaisuuksiin, kuten valikoimiin, luetteloihin ja tiettyihin toimitustapoihin.

Puhelinkeskuskanavassa voidaan määrittää oletusvarasto. Kun kanavassa sitten luodaan myyntitilauksia, oletusvarasto annetaan automaattisesti myyntitilauksen otsikossa ellei jotain toista varastoa ole määritetty myyntitilauksessa valitulle asiakkaalle. Siinä tapauksessa asiakkaan varasto annetaan oletusarvoisesti.

Käyttäjät on linkitettävä puhelinkeskuskanavaan, jotta he voivat käyttää puhelinkeskuksen ominaisuuksia. Käyttäjän Retailissa luoma myyntitilaus linkitetään automaattisesti käyttäjän puhelinkeskuskanavaan. Tällä hetkellä käyttäjää ei voi linkittää samanaikaisesti useisiin puhelinkeskuskanaviin.

Puhelinkeskuskanavassa voi määrittää myös sähköposti-ilmoitusprofiilin. Profiilin määrittää joukon sähköpostimalleja, joita käytetään, kun puhelinkeskuskanavan kautta tilauksen tekeville asiakkaille lähetetään sähköpostiviesti. Sähköpostin käynnistimet voidaan määrittää järjestelmän tapahtumien perusteella esimerkiksi tilauksen lähettämisen tai tilauksen toimittamisen yhteyteen.

Ennen kuin myynti voidaan käsitellä asianmukaisesti puhelinkeskuskanavassa, kanavalle on määritettävä oikeat [maksutavat](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-payments) ja toimitustavat.

Voit määrittää puhelinkeskuskanavan tasolla muita taloushallinnon dimensioon liittyviä oletusarvoja, jotka linkitetään kyseisen kanavan luomiin tilauksiin.

## <a name="options-for-order-processing-behavior"></a>Tilauksen käsittelyasetukset

Puhelinkeskusta määritettäessä kolmella asetuksella on merkittävä vaikutus puhelinkeskuksessa luotavien myyntitilausten käytössä oleviin ominaisuuksiin ja toimintoihin: **Ota käyttöön tilausten viimeistely**, **Ota ohjattu myynti käyttöön** ja **Ota käyttöön hintasäätely**.

### <a name="enable-order-completion"></a>Ota käyttöön tilausten viimeistely

Puhelinkeskuskanavan **Ota käyttöön tilauksen viimeistely** -asetus vaikuttaa merkittävästi kanavaan vietyjen myyntitilausten käsittelyyn. Kun tämä asetus on otettu käyttöön, kaikkien myyntitilausten on läpäistävä tietyt kelpoisuussäännöt, ennen kuin ne voidaan vahvistaa. Voit suorittaa nämä säännöt valitsemalla myyntitilaussivun toimintoruutuun lisätyn **Viimeistele**-painikkeen. Kaikkien tilausten, joita luotaessa **Ota käyttöön tilausten viimeistely** -asetus on ollut käytössä, on läpäistävä tilauksen viimeistelyprosessi. Tämä prosessi pakottaa tarkistamaan maksun ja maksun tarkistuslogiikan. Maksun pakottamisen lisäksi tilauksen lähetysprosessi voi käynnistää järjestelmään määritetyt [petostarkistukset](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-fraud-alerts). Tilaukset, joiden maksu tai petostarkistukset epäonnistuvat asetetaan pitoon eikä niitä voi vapauttaa käsittelyn jatkamista varten (kuten poimittavaksi tai lähetettäväksi), ennen kuin pidon aiheuttanut ongelma on ratkaistu.

Kun **Ota käyttöön tilausten viimeistely** on otettu puhelinkeskuskanavassa käyttöön, järjestelmä pakottaa tilauksen viimeistelyprosessin, jos myyntilaukseen annetaan rivinimikeitä tai kanavan käyttäjä yrittää siirtyä pois myyntitilauslomakkeesta valitsematta ensin **Viimeistele**. Tämä tapahtuu avaamalla myyntitilauksen kertaussivun ja pyytämällä käyttäjää lähettämään tilaus oikein. Jos tilausta ei voi lähettää oikein maksun kanssa, käyttäjä voi asettaa tilauksen pitoon [tilausten pidon](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds) toiminnoilla. Jos käyttäjä yrittää peruuttaa tilauksen, hänen on peruutettava se oikein käyttämällä joko peruutus- tai poistotoimintoa sen mukaan, minkä toiminnon käytön käyttäjän käyttöoikeuden sallivat.

Jos **Ota käyttöön tilausten viimeistely** on otettu käyttöön puhelinkeskuskanavassa, tilauksen **Maksun tila** -kenttää seurataan. Järjestelmä laskee **Maksun tilan**, kun myyntitilaus on lähetetty. Vain tilaukset, joiden maksun tila on hyväksytty, saavat siirtyä järjestelmässä tilauksen muihin käsittelyvaiheisiin, kuten poimintaan ja lähetykseen. Jos maksut hylätään, **älä käsittele** -merkintä otetaan käyttöön tilauksen eritellyssä tilassa, jolloin tilaus asetetaan pitoon maksuongelman ratkaisemiseen saakka.

Jos **Ota käyttöön tilausten viimeistely** -asetus on otettu käyttöön, kun käyttäjät luovat myyntitilauksia ja ovat rivinimikkeen merkintätilassa, myös **Lähde**-kenttä on käytössä päämyyntitilauksen otsikossa. **Lähde**-kenttään tallennetaan [luettelon lähdekoodi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/call-center-catalogs) suoramarkkinoinnin myyntiskenaariossa. Tämä koodi voi sitten ohjata erikoishintoja ja kampanja-alennuksia.

Vaikka **Ota käyttöön tilausten viimeistely** -asetus olisi poistettu käytöstä, käyttäjät voivat silti käyttää lähdekoodia myyntitilauksessa. Heidän on kuitenkin ensin avattava myyntitilauksen otsikon tiedot, jotta he pääsevät käyttämään **Lähde**-kenttää. Toisin sanoen heidän on tehtävä muutama ylimääräinen toimi. Sama menettely koskee myös sellaisia ominaisuuksia, kuten Valmis lähetettäväksi ja Nopeutetut tilaukset. Näitä ominaisuuksia voi käyttää kaikissa puhelinkeskuksessa luoduissa tilauksissa. Kun **Ota käyttöön tilausten viimeistely** -asetus on otettu käyttöön, käyttäjät voivat kuitenkin nähdä näiden ominaisuuksien määritykset myynnin otsikossa, kun he ovat rivimerkintänäkymässä. Heidän ei tarvitse porautua etsimään asetuksia ja kenttiä myyntitilauksen otsikon tietoihin.

### <a name="enable-direct-selling"></a>Ota ohjattu myynti käyttöön

Jos **Ota ohjattu myynti käyttöön** -asetus on otettu puhelinkeskuskanavassa käyttöön, käyttäjät voivat hyödyntää Retailin lisämyynti- ja ristiinmyyntiominaisuuksia. Siinä tapauksessa tilausten käsittelyn aikana avautuu ponnahdusikkuna ehdottamaan muita tuotteita, joita puhelinkeskuksen käyttäjä voi tarjota asiakkaalle. Ehdotettavat tuotteet perustuvat myyntitilausrivillä juuri tilattuun tuotteeseen. Tällä hetkellä lisä- ja ristiinmyyntiehdotukset määritetään tuotteissa tai luetteloissa nimiketasolla. Jos **Ota ohjattu myynti käyttöön** -asetusta ei ole otettu puhelinkeskuskanavassa käyttöön, ponnahdusikkunat eivät avaudu tilauksen käsittelyn aikana, vaikka tilattavalle nimikkeelle olisi määritetty sopiva lisä- tai ristiinmyynti.

Kun **Ota ohjattu myynti käyttöön** -asetus on otettu käyttöön, myös myyntitilauksen käsittelyn skripti- ja kuvaominaisuudet on otettu käyttöön. Siinä tapauksessa sivun oikeassa reunassa on tietopaneeli tilausten käsittelyn aikana. Tässä paneelissa on yleiseen tilaustenkäsittelyprosessiin liittyviä skriptejä, käytetty luettelon lähdekoodi tai tilattaviin nimikkeisiin liittyviä skriptejä. Lisäksi kuvapaneelissa voi olla tilattavien nimikkeiden tuotekuva, jos kuva nimikkeen kuva on määritetty tuoteasetuksissa.

### <a name="enable-order-price-control"></a>Ota käyttöön hintasäätely

Kun **Ota käyttöön hintasäätely** -asetus on otettu käyttöön, vain valtuutetut käyttäjät voivat muuttaa nimikkeen myyntihintaa tilaustenkäsittelyn aikana. Muutosten on oltava määritettyjen toleranssien mukaisia. Jos käyttäjällä ei ole tarvittavia valtuutuksia, hänen on lähetettävä hinnan muutospyyntö. Pyyntö käsitellään sitten järjestelmän arviointi- ja hyväksyntätyönkulkujen mukaisesti.

## <a name="channel-users"></a>Kanavan käyttäjät

Kun määritä puhelinkeskuskanavan, käyttäjät on linkitettävä puhelinkeskukseen. Muussa tapauksessa puhelinkeskusta ei voi käyttää järjestelmässä. Kun käyttäjät kirjautuvat Retailiin ja antavat myynti- tai palautustilauksia tilaustenkäsittelyyn liittyvällä sivulla, heidän käyttäjätunnuksensa tarkistetaan puhelinkeskuskanavan määrityksissä. Jos käyttäjä on linkitetty tiettyyn puhelinkeskuskanavaan, käyttäjän luomat tilaukset perivät kyseisen kanavan ominaisuudet ja oletusarvot.

Oletusarvoisesti myyntilauksen otsikon **Vähittäismyynti**-merkintä on käytössä kaikissa puhelinkeskuksen käyttäjien luomissa tilauksissa. Tilaukset voivat sitten käyttää järjestelmän vähittäismyyntikohtaisia hinta- ja kampanja-alennusominaisuuksia.

Käyttäjät, joita ei ole linkitetty puhelinkeskuskanavaan, käyttävät Microsoft Dynamics 365 for Finance and Operationsin tilaustenkäsittelyn perusominaisuuksia. Myyntitilauksen käsittelylomakkeen kautta annettavia tilauksia ei tunnisteta järjestelmällisesti vähittäismyyntitilauksiksi. Lisäksi mitkään tilauksen viimeistelyn käsittelysäännöt, vähittäismyynnin hinnoittelulogiikka tai muut tilauksen tarkistukset, jotka voidaan määrittää puhelinkeskuskanavan määrityksissä tai puhelinkeskuksen järjestelmäparametreissa, eivät koske tällaisten käyttäjien antamia tällaisia tilauksia.

Kun puhelinkeskuskanavan määritykset on tehty ja kanavan käyttäjät määritetty, varmista järjestelmä toimiminen odotetulla tavalla tarkistamalla, että kaikki pakolliset puhelinkeskuksen parametrit on määritetty kohdassa **Retail** \> **Kanavan asetukset** \> **Puhelinkeskuksen asetukset** \> **Puhelinkeskuksen parametrit**. Muista määrittää myös liittyvät numerosarjat.

