---
title: Suunnittelun optimoinnin sopivuusanalyysi
description: Tässä artikkelissa käsitellään, miten nykyisten asetusten ja tietojen yhteensopivuus suunnittelun optimointitoiminnon ominaisuuksien kanssa varmistetaan.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 15ec53c1f13b3017fb6e829bd1c8e99fbb938ce3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689991"
---
# <a name="planning-optimization-fit-analysis"></a>Suunnittelun optimoinnin sopivuusanalyysi

[!include [banner](../../includes/banner.md)]

Suunnittelun optimoinnin sopivuusanalyysin tulos on analysoitava osana siirtoprosessia. Huomaa, että suunnittelun optimoinnin laajuus ei vastaa nykyistä sisältyvää pääsuunnittelutoimintoa. Siirtoon kannattaa valmistautua tekemällä yhteistyötä kumppanin kanssa ja tutustumalla ohjeisiin. 

Suunnittelun optimoinnin sopivuusanalyysin auttaa määrittämään, missä kohdissa sisältyvän pääsuunnittelumoduulin ja suunnittelun optimoinnin välillä voi olla eroja. Tämä analyysi tehdään nykyisten asetusten ja tietojen perusteella. 

Saat suunnittelun optimoinnin sopivuusanalyysin tulokset valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin sopivuusanalyysi** ja valitsemalla sitten **Suorita analyysi**. Jos analyysissa havaitaan ristiriitoja, ne mainitaan samalla sivulla. (Analyysin suorittaminen voi kestää muutaman minuutin.)

> [!NOTE]
>
> - Suunnittelun optimoinnin sopivuusanalyysi ei tunnista tiettyjä epäjohdonmukaisuuksia. Lisätietoja on kohdassa [Perinteisen pääsuunnittelun ja suunnittelun optimoinnin erot](planning-optimization-differences-with-built-in.md).
>
> - Jos ristiriitoja löytyy, suunnittelun optimointia voi silti käyttää. Sopivuusanalyysin tulokset vain osoittavat, missä suunnittelupalvelu ei noudata nykyisiä asetuksia. Ne siis näyttävät kohdat, joissa joitakin prosesseja voidaan ohittaa tai joissa niitä ei ehkä tueta.

## <a name="analysis-results-example-1"></a>Analyysin tulokset: Esimerkki 1

- **Toiminto:** Tuotanto
- **Ongelma:** Nimikkeet, joiden tuoterakennetaso (BOM) on suurempi kuin nolla: 56
- **Selitys:** Sopivuusanalyysi löysi 56 nimikettä, joissa on tuotannon BOM-asetuksia. Koska suunnittelun optimoinnin nykyinen versio ei tue tuotantoa, suunnittelun optimointi luo suunniteltuja ostotilauksia eikä suunniteltuja tuotantotilauksia. Näkyviin tulee myös varoitus, jossa mainitaan nimikkeet, joita ongelma koskee.

## <a name="analysis-results-example-2"></a>Analyysin tulokset: Esimerkki 2

- **Toiminto:** Toimenpiteet
- **Ongelma:** Kattavuusryhmät, joissa toimenpidelaskelma on otettu käyttöön: 6
- **Selitys:** Sopivuusanalyysi havaitsi kuusi kattavuusryhmää, joissa toimenpidelaskelma on otettu käyttöön. Koska suunnittelun optimoinnin nykyinen versio ei tue toimenpiteitä, toimenpiteitä ei luoda pääsuunnittelun aikana.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Yhteenveto sopivuusanalyysin mahdollisista tuloksista

Seuraavassa taulukossa esitetään eri tulokset, jotka voidaan näyttää sopivan analyysin jälkeen. Numeromerkit (*\#*) korvataan numerolla, joka ilmaisee luettelossa olevan varasto-oton sisältävien tietojen määrän.

> [!IMPORTANT]
> Seuraava taulukko sisältää arvioidut saatavuustiedot ominaisuuksille, joita ei vielä tueta, tämänhetkisen suunnitelmamme perusteella. Näitä arvioita voidaan muuttaa ilman erillistä ilmoitusta.

| Ominaisuus | Lueteltu ongelma | Selitys | Odotettu käytettävyys |
| --- | --- | --- | --- |
| Toimenpiteet | Kattavuusryhmät, joissa toimenpidelaskenta on käytössä: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. | Tuettu |
| Peruskalenterit | Kalenterit, joissa käytetään peruskalenteria: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. | Tuettu | 
| Erän käsittelykoodit | Ei-netottavissa olevan erän käsittelykoodin päätiedot: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Erien merkitseminen käytettävissä tai ei-käytettävissä oleviksi käsittelykoodien avulla](../../inventory/batch-disposition-codes.md) | Tuettu |
| Saatavuus (CTP) | Tilauksen oletusasetukset, joiden toimituspäivämäärä on asetettu saatavuuteen (CTP): *\#* | Supply Chain Managementin versiossa 10.0.28 ja sitä uudemmassa versiossa on *Saatavuus (CTP) suunnittelun optimointia varten* -prosessi, joka tuo vahvistetut lähetys- ja vastaanottopäivämäärät saataville dynaamisen suunnittelun suorittamisen jälkeen. Supply Chain Managementin vanhojen versioiden saatavuus (CTP) -asetus ohitetaan, kun suunnittelun optimoitu on otettu käyttöön. | Tuettu |
| Kopioi staattinen dynaamiseen suunnitelmaan | Staattisen kopioiminen ja dynaamiseen suunnitelmaan on käytössä pääsuunnitteluparametreissa. | Suunnittelun optimointi ei kopioi staattista suunnitelmaa dynaamiseen suunnitelmaan riippumatta tästä asetukseen. Yleensä tämä käsite ei ole yhtä merkityksellinen, koska suunnittelu optimointi tarjoaa nopeuden ja täydellisen uudistamisen. Jos käytössä on vähintään kaksi suunnitelmaa, pääsuunnittelu on käynnistettävä kunkin suunnitelman osalta. | – |
| Vahvistus | Automaattisen vahvistuksen aikaraja ja kattavuusryhmiä määritetty: *\#* | Version 10.0.7 ja uudempien versioiden vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos *suunnittelun optimoinnin automaattinen vahvistus* -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| Vahvistus | Automaattisen vahvistuksen määrittäminen ja nimikekattavuustietueet: *\#* | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos *suunnittelun optimoinnin automaattinen vahvistus* -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| Vahvistus | Määritä pääsuunnitelmat ja automaattinen vahvistus: *\#* | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos *suunnittelun optimoinnin automaattinen vahvistus* -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| FitAnalysisPlanningItems | Suunnittelunimikkeet: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä suunnittelunimikkeitä käsitellään tavallisten nimikkeiden tapaan, kun suunnittelun optimointi on käytössä. | Vuoden 2022 julkaisuaalto 2 tai sitä uudempi |
| Ennuste | Kattavuusryhmät, joiden "sisällytetyt konsernin sisäiset tilaukset" ovat käytössä: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Konsernin sisäinen suunnittelu](Intercompany-planning.md) | Tuettu |
| Ennuste | Kattavuusryhmät, joiden ennuste on "Pienennä ennustetta"-asetuksen arvoksi on määritetty eri arvo kuin "Tilaukset": *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja: [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md) | Tuettu |
| Ennuste | Ennustemallit, joissa osamalleja: *\#* |  Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja: [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md) | Tuettu |
| Ennuste | Pääsuunnitelmat, joiden "sisältää tarjontaennusteen" -asetukset ovat käytössä: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä tarjontaennusteita ei tueta, kun suunnittelun optimointi on käytössä. Ne ohitetaan riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 tai sitä uudempi |
| Lukitusaikaraja | Kattavuusryhmät, joissa on lukitusaikaraja määritetty: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä lukitusaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Lukitusaikaraja | Kohteen kattavuustietueet, joissa on lukitusaikaraja määritetty: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä lukitusaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Lukitusaikaraja | Pääsuunnitelmat, joissa on lukitusaikaraja määritetty: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä lukitusaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Konsernin sisäinen | Pääsuunnitelmat, mukaan lukien suunniteltu tuotantovirran kysyntä: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Konsernin sisäinen suunnittelu](Intercompany-planning.md) | Tuettu |
| Kanban | Kohteen kattavuusrekisterit, joissa on suunniteltu tilaustyyppi kanban: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä kanbaniin määritetty nimikekattavuus ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-suunnitellun tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. | Tuleva aalto |
| Kanban | Nimikkeet, joiden oletusjärjestystyyppi on kanban: *\#* | Tällä hetkellä kanbaniin määritetty oletustilaustyyppi ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-oletuksen tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. | Tuleva aalto |
| Tuotteen elinkaaren tila | Tuotteen elinkaaren tilat eivät ole aktiivisia suunnittelulle: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Sulje pois tuotteita, joissa on tietty tuotteen elinkaaren tila](product-lifecycle-state.md) | Tuettu |
| Tuotantoympäristö | Tuoterakennerivit, joilla on pyöristys tai useita asetuksia: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä pyöristystä ja useita asetuksia ei oteta huomioon tuoterakenneriveillä, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | Tuleva aalto|
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on kaavan mittaus:*\#* | Tämä ominaisuus odottaa. Tällä hetkellä kaavan mittaa ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään nimikkeen korvausta (suunnitteluryhmät): *\#* | Tämä ominaisuus odottaa. Tällä hetkellä nimikkeen korvausta (suunnitteluryhmät) ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on negatiivinen määrä: *\#* | Tämä ominaisuus odottaa. Tuoterakenne- ja kaavarivit, joilla on negatiivinen määrä, sisällytetään määrään 0 (nolla), ja järjestelmä antaa varoituksen, kun suunnittelun optimointi on otettu käyttöön. Päivitä päätiedot ja varoitusten välttämiseksi. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään resurssin kulutusta: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä resurssien kulutusta käyttävät tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. Kun tätä toimintoa tuetaan, materiaalitarve määritetään tuotannon alkamispäivälle. Ennen tämän toiminnon tukemista tarpeita ei luoda sellaisille materiaaleille, jotka on merkitty resurssinkäyttömerkinnällä. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään vaiheittaista kulutusta: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä vaiheenkulutusta ei oteta huomioon, kun tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteet, joille on määritetty vakiohävikki tai muuttuva hävikki: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä tuoterakenteissa määritetyt vakiohävikki ja muuttuva hävikki ohitetaan, kun suunnittelun optimointi on käytössä. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Tuoterakenteet, joissa käytetään alihankintaa: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. | Tuettu |
| Tuotantoympäristö | Tuoterakenteet ilman sivustoa: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Tuotannon suunnittelu](production-planning.md) | Tuettu |
| Tuotantoympäristö | Kysyntä tietyillä määritetyillä tuoterakenne- tai reititysvaatimuksilla: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä kysyntään määritetyt tuoterakenne- tai reititysvaatimukset (kuten alituoterakenne tai myyntitilauksen alireititys) ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Vakiotuoterakennetta tai -reittiä käytetään tähän asetukseen katsomatta. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Kaavan versiot, joissa on oheis-/sivutuotteita: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä kaavaversioon liittyvät oheistuotteet ja sivutuotteet ohitetaan, kun suunnittelun optimointi on käytössä. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Kaavan versiot ja saanto: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä tuotto, joka liittyy kaavaversioon ohitetaan, kun suunnittelun optimointi on käytössä. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Suunnitelmat, joissa käytetään järjestystä: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä järjestys ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. | Vuoden 2022 julkaisuaalto 2 |
| Tuotantoympäristö | Aloittamattomat vapautetut tuotantotilaukset, joiden aikataulutettu aloitus on ennen kuluvaa päivää: *\#* | Tämä ominaisuus odottaa. Jos tuotantotilaus tällä hetkellä viivästyy, pääsuunnittelu olettaa, että se valmistuu saman päivän aikana. Tällä on merkitystä vapautetuille tuotantotilauksille, joiden toimituspäivä on menneisyydessä mutta joita ei ole vielä saatu valmiiksi. | Tuleva aalto |
| Tuotantoympäristö | Aikataulutetut resurssit, joilla on rajallinen kapasiteetti: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä.| Tuettu |
| Tuotantoympäristö | Suunnittelussa käytetyt reitit: *\#* | Tätä ominaisuutta tuetaan. | Tuettu |
| Tuotantoympäristö | Hajotusta käyttävä myyntirivin varaus: *\#* | Hajotustoimintoa käyttävä myyntirivin varaus ei ole tuettu, kun suunnittelun optimointi on käytössä. | Tuleva aalto |
| Tuotantoympäristö | Aikataulutus tuotantotilausten hajotuksen kanssa: *\#* | Aikataulu, joka käyttää tuotantotilausten räjähdystä ei ole tuettu, kun suunnittelun optimointi on käytössä. Tuotantotilaukset voidaan ajoittaa yksitellen. | Tuleva aalto |
| Tarjouspyyntö | Pääsuunnitelmat ja tarjouspyyntö käytössä: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä tarjouspyyntöjä (RFQs) ei pidetä vaatimuksina, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 |
| Ehdotukset | Pääsuunnitelmat, joissa ehdotukset on otettu käyttöön: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Ostoehdotukset](purchase-requisitions.md) | Tuettu |
| Varmuusmarginaalit | Kattavuusryhmät varmuusmarginaalin kanssa: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Varmuusmarginaalit](safety-margins.md) | Tuettu |
| Varmuusmarginaalit | Pääsuunnitelmat varmuusmarginaalin kanssa: *\#* | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Varmuusmarginaalit](safety-margins.md) |  Tuettu |
| Varmuusvaraston täyttäminen | Nimikkeiden kattavuustiedot, joissa on "täytä vähimmäisvaatimukset", poikkeavat tämän päivän päivämäärästä ja hankinta-ajasta: *\#* | Suunnittelun optimointi käyttää aina *kuluvan päivän päivämäärää ja hankinta-aikaa*. Tämä muutos tehdään, kun halutaan valmistautua yksinkertaistettuihin suunnitteluasetuksiin tulevaisuudessa. Jos toimitusaika ei sisälly varmuusvarastoon, nykyiselle alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. Tämä voi aiheuttaa merkittäviä meluongelmia ja ei-toivottuja suunniteltuja tilauksia. Paras käytäntö on muuttaa asetusta siten, että *kuluvan päivän päivämäärää + hankinta-aikaa* käytetään. Päivitä päätiedot ja varoitusten välttämiseksi. | Ei saatavilla |
| Myyntitarjoukset | Pääsuunnitelmat ja myyntitarjoukset käytössä: *\#* | Tämä ominaisuus odottaa. Tällä hetkellä tarjouksia ei oteta huomioon, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. | Vuoden 2022 julkaisuaalto 2 tai sitä uudempi |
| Säilyvyysaika | Pääsuunnitelmat, joissa säilyvyysaika on otettu käyttöön: *\#* | Tämä ominaisuus odottaa. | Vuoden 2022 julkaisuaalto 2 |

## <a name="additional-resources"></a>Lisäresurssit

[Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Perinteisen pääsuunnittelun ja suunnittelun optimoinnin erot](planning-optimization-differences-with-built-in.md)

[Parametrit, joita ei käytetä suunnittelun optimoinnissa](not-used-parameters.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
