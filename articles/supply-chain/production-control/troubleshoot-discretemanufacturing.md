---
title: Erillisen valmistuksen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita erillisen valmistuksen käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 604e0c3406b15d885991fcb067e93ef83533e3b0
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516772"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Erillisen valmistuksen vianmääritys

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita erillisen valmistuksen käytössä voi esiintyä.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Seuraava virhesanoma avautuu: Varastonhallintaprosesseja käytetään parhaillaan. Jos työrivejä ei ole vielä rekisteröity, voit peruuttaa luodun työn sekä mahdolliset kuorma- tai toimitusrivit ja jatkaa sitten keräily- tai lähetysprosessin kanssa.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma esiintyy, jos rivin työtä yritetään varata tai vapauttaa, kun varastotapahtuman tila on *Keräilty*, mikä ilmaisee, että materiaali on keräilty.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Ongelma korjataan jollakin seuraavista tavoista:

- Muuta tuotantotilauksen tilaksi jälleen *Ennakkolaskettu* tai *Vapautettu*.
- Avaa kyseisen tuotantotilauksen tietosivu. Kumoa kaikkien kerättyjen tapahtumien keräys valitsemalla toimintoruudun **Varasto**-välilehden **Pysäytä**-ryhmässä **Pysäytä ja kumoa keräys**. Käsittele sitten tuotantotilaus valitsemalla **Poista pysäytys**.

*Kumoa keräys*- ja *Pysäytä*-toimintojen selitys:

- **Kumoa keräys** – Tämä toiminto kumoaa niiden tuoterakennerivien ja kaavarivien varastotapahtumien tilan, joissa tilana on *Kerätty*, *Tilauksessa* ja niiden väliin jäävät tilat. Kun raaka-aineiden keräilytyö on valmis, rivien tilaksi määritetään *Kerätty*. Tämä tila estää tuotantotilauksen palauttamisen *Luotu*-tilaan. Tässä tapauksessa tapahtuman voi palauttaa *Kumoa keräys* -toiminnolla *Kerätty*-tilasta ja palauttaa tuotantotilauksen *Luotu*-tilaan.
- **Pysäytä** – Tämä toiminto määrittää **Pysäytetty**-merkinnän tuotantotilaukseen, jolloin tilauksen tilaa ei voi päivittää. **Pysäytetty**-merkintä näkyy tuotantotilauksen tietosivun **Varasto**-pikavälilehdessä.

> [!NOTE]
>
> - Painikkeet ovat näkyvät vain silloin, kun tuotantotilaus luodaan nimikkeille, joissa varastoprosessit on otettu käyttöön.
> - **Pysäytä**-ryhmä näkyy vain tuotantotilauksen tietosivun toimintoruudun **Varasto**-välilehdessä. Se ei näy **Tuotantotilaukset**-luettelosivun **Varasto**-pikavälilehdessä.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Vastaavaa resurssin nimeä ei päivitetä, kun työntekijän nimi on vaihdettu yleisessä osoitekirjassa

### <a name="issue-description"></a>Ongelman kuvaus

Jos työntekijän nimeä muutetaan yleisessä osoitekirjassa, vastaavaa resurssin nimeä ei päivitetä pääresurssiryhmässä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tätä skenaariota ei tueta tällä hetkellä. Ongelma korjataan päivittämällä resurssin nimi manuaalisesti.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Uutta tuotantotilausta luodessa seuraava sanoma ei avaudu: Lisätäänkö tuoterakenteen ja reitin aktiivinen versio?

### <a name="issue-description"></a>Ongelman kuvaus

Kun uusi tuotantotilaus luodaan, nimiketunnuksen antamisen jälkeen **Toimipaikka**- ja **Varasto**-kenttien arvoksi määritetään automaattisesti valmiin tuotteen **Tilauksen oletusasetukset** -sivulla määritetty oletustoimipaikka ja -varasto. Tämän lisäksi myös aktiivinen tuoterakennenumero ja reittinumero annetaan automaattisesti. Näitä arvoja kysyvä seuraava sanoma ei tämän vuoksi avaudu:

> Lisätäänkö tuoterakenteen ja reitin aktiivinen versio?

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tuoterakenteen ja reitin numeroa ei pyydetään antamaan, jos valitulle tuotteelle on määritetty toimipaikka ja varasto **Tilauksen oletusasetukset** -sivulla. Näitä arvoja kysytään vain siinä tapauksessa, että niitä ei ole määritetty valitulle tuotteelle.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Tuotantotilaukset eivät näy Merkintä-sivulla

### <a name="issue-description"></a>Ongelman kuvaus

**Merkintä**-sivu ei näy kaikissa tuotantotilauksissa.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tuotteissa, joissa on seuraava määritys, ei käyttää merkintää. Niinpä **Merkintä**-sivu ei näy niissä:

- Tuotteet, jotka on määritetty *todellinen paino* -tyyppisiksi tuotteiksi.
- Edistykselliset varastoprosessit on otettu niissä käyttöön.
- Ne on määritetty hallittaviksi *standardikustannuksen* mukaisesti.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Tuotantotilauksen lopettamista yritettäessä avautuu seuraava virhesanoma: Lasketaan kulutus tuoterakenteen mukaan Varasto-oton kustannusarvon on oltava negatiivinen.

Tämä ongelma korjattiin versiossa 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Kun tuotantotilauksen Ilmoitettu valmiiksi -tila vaihtuu tilaksi Lopetus, seuraavat virhesanomat avautuvat: Päivitysristiriita. Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen. ja Vakava virhe toiminnossa InventCostMovement.checkVariance.

Tämä ongelma esiintyy, koska toinen prosessi on muuttanut taustalla olevia tietoja. Prosessi yrittää päivittää tiedot enintään viisi kertaa. Jos ristiriita esiintyy vielä viidennen yrityksen jälkeen, seuraavat virhesanomat avautuvat:

> Päivitysristiriita. Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen.

> Vakava virhe toiminnossa InventCostMovement.checkVariance.

Tämä on suunniteltu ominaisuus. Korjaa ongelma jatkamalla erätyötä. Se suorittamisen pitäisi onnistua.

Jos erätyön suorittaminen epäonnistuu toistuvasti jatkamisen jälkeen, tarkista, että kirjanpidon oletusvaluutan pyöristystarkkuus on yhteensopiva InventSum-taulukossa käytettyjen arvojen pyöristyksen kanssa. Jos pyöristystarkkuus on vaihdettu ei-yhteensopivaksi arvoksi, se on luultavasti muutettava takaisin yhteensopivaksi arvoksi. Etsi **ModifiedDateTime**. Tässä tapauksessa arvo yleensä näyttää, että pyöristystarkkuutta on muutettu äskettäin.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Varastoon vapautettaessa avautuu seuraava virhesanoma: Nimikettä RM ei voitu varata täysin. Varmista, että koko määrä on käytettävissä, tai varaa nimikkeet manuaalisesti, mikäli tuoterakennerivin Varaus-kentän arvoksi on määritetty Manuaalinen tai Aloitettu. Tilausta ei voitu vapauttaa varastoon, koska kaikkia materiaaleja ei voitu varata. Tilaksi kuitenkin päivitetään Vapautettu.

### <a name="issue-description"></a>Ongelman kuvaus

Jos kaikki tuoterakennerivinimikkeet eivät ole käytettävissä, kun tuotantotilaus vapautetaan, ja **Vapauta varastoon** -käytännöksi on määritetty tuotantotilauksessa *Edellytä täyttä varaamista*, seuraava virhesanoma avautuu.

> Nimikettä RM ei voitu varata täysin. Varmista, että koko määrä on käytettävissä, tai varaa nimikkeet manuaalisesti, mikäli tuoterakennerivin Varaus-kentän arvoksi on määritetty Manuaalinen tai Aloitettu. Tilausta ei voitu vapauttaa varastoon, koska kaikkia materiaaleja ei voitu varata.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus, ja se toimii odotetulla tavalla.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Kun tuotantotilausta yritetään lopettaa ja ilmoittaa valmiiksi, seuraavat virhesanoma avautuu: Tuotannon valmiiksi ilmoitettujen hyväksytty määrä on %1. Palaute viimeistä toimintoa varten on yhteensä 0,00.

### <a name="issue-description"></a>Ongelman kuvaus

Kun raportti yritetään tuotantotilauksessa valmiiksi ilmoitettujen kirjauskansioon, seuraava virhesanoma avautuu:

> Tuotannon valmiiksi ilmoitettujen hyväksytty määrä on %1. Palaute viimeistä toimintoa varten on yhteensä 0,00.

### <a name="possible-cause"></a>Mahdollinen syy

Tämä ongelma esiintyy, jos viimeisissä toiminnoissa kirjatut määrät olivat virheellisiä. Jos tuotanto esimerkiksi aloitettiin mutta aloitettavaa määrää ei kohdistettu, reitityskortin kirjauskansio kirjataan ilman rivejä. Tarkista tilanne avaamalla tuotantotilaus ja valitsemalla sitten toimintoruudun **Näytä**-välilehdessä **Reitityskortti**.

### <a name="workaround"></a>Ongelman kiertäminen

Voit korjata ongelma kirjaamalla lisäkirjauskansiot niille toiminnoille, joiden kirjauskansioita ei kirjattu oikein. Käynnistä tuotantotilaus uudelleen ja valitse lisäkirjauskansioiden kirjaaminen. Tämä toiminto ei käynnistä tuotantotilausta vaan kirjaa kirjauskansiot. Kirjattujen määrien pitäisi näkyä sitten reitityskortissa ja tuotantotilausten lopettaminen pitäisi olla mahdollista.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Voidaanko tuotantotilaus ilmoittaa valmiiksi, kun virhemäärä ilmoitetaan, mutta ei silloin, kun ajan tai materiaalin määrä ilmoitetaan?

Tuotantotilauksen virhemäärää ei voi ilmoittaa ellei myös hyväksyttyjen määrää ilmoiteta. Tätä skenaariota **ei** tueta. Valmiiksi ilmoittamispäivitys epäonnistuu siinä vaiheessa, kun tuotantotilaus yritetään lopettaa, ja seuraava virhesanoma avautuu:

> Valmiiksi ilmoitettu määrä puutuu.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Voiko valmiiksi ilmoitettujen tuotteiden sarjanumeroita jäljittää kulutettujen tuotteiden sarjanumeroiden perusteella?

Valmiiden tuotteiden sarjanumeroita ei voi jäljittää käyttämällä niiden materiaalien sarjanumeroita, joita tuotantotilaus käyttää kyseisten valmiiden tuotteiden valmistamiseen. Tätä skenaariota ei tueta tällä hetkellä. Ongelman voi kiertää luomalla tuotantotilauksia, joiden määrä on 1.
