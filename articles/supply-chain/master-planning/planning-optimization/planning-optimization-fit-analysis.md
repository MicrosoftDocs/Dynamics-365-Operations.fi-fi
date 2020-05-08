---
title: Suunnittelun optimoinnin sopivuusanalyysi
description: Tässä ohjeaiheessa käsitellään, miten nykyisten asetusten ja tietojen yhteensopivuus suunnittelun optimointitoiminnon ominaisuuksien kanssa varmistetaan.
author: ChristianRytt
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0382e78942e6cb2047e37b76f1daf5725638d5c3
ms.sourcegitcommit: 915ee7c59ef5fbd4927c10840e5c5e8652f667a9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3277795"
---
# <a name="planning-optimization-fit-analysis"></a>Suunnittelun optimoinnin sopivuusanalyysi

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Voit tarkistaa, kuinka yhteensopivia nykyiset asetukset ja tiedot ovat suunnittelu optimointitoiminnon kanssa valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin sopivuusanalyysi** ja valitse sitten **Suorita analyysi**. Jos analyysissa havaitaan ristiriitoja, ne mainitaan samalla sivulla. (Analyysin suorittaminen voi kestää muutaman minuutin.)

> [!NOTE]
> Jos ristiriitoja löytyy, suunnittelun optimointia voi silti käyttää. Sopivuusanalyysin tulokset vain osoittavat, missä suunnittelupalvelu ei noudata nykyisiä asetuksia. Ne siis näyttävät kohdat, joissa joitakin prosesseja voidaan ohittaa tai joissa niitä ei ehkä tueta.

## <a name="analysis-results-example-1"></a>Analyysin tulokset: Esimerkki 1

- **Toiminto:** Tuotanto
- **Ongelma:** Nimikkeet, joiden tuoterakennetaso (BOM) on suurempi kuin nolla: 56
- **Selitys:** Sopivuusanalyysi löysi 56 nimikettä, joissa on tuotannon BOM-asetuksia. Koska suunnittelun optimoinnin nykyinen versio ei tue tuotantoa, suunnittelun optimointi luo suunniteltuja ostotilauksia eikä suunniteltuja tuotantotilauksia. Näkyviin tulee myös varoitus, jossa mainitaan nimikkeet, joita ongelma koskee.

## <a name="analysis-results-example-2"></a>Analyysin tulokset: Esimerkki 2

- **Toiminto:** Toimenpiteet
- **Ongelma:** Kattavuusryhmät, joissa toimenpidelaskelma on otettu käyttöön: 6
- **Selitys:** Sopivuusanalyysi havaitsi kuusi kattavuusryhmää, joissa toimenpidelaskelma on otettu käyttöön. Koska suunnittelun optimoinnin nykyinen versio ei tue toimenpiteitä, toimenpiteitä ei luoda pääsuunnittelun aikana.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Yhteenveto sopivuusanalyysin mahdollisista tuloksista

Seuraavassa taulukossa esitetään eri tulokset, jotka voidaan näyttää sopivan analyysin jälkeen. Numeromerkit (_\#_) korvataan numerolla, joka ilmaisee luettelossa olevan varasto-oton sisältävien tietojen määrän.

| Ominaisuus | Lueteltu ongelma | Selitys |
| --- | --- | --- |
| Toimet | Kattavuusryhmät, joissa toimintojen laskenta on käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä toimintoja ei luoda pääsuunnittelun aikana, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. Toimenpiteiden pääasiallinen tarkoitus on ehdottaa muutoksia aiemmin luotuihin tilauksiin. |
| Peruskalenterit | Kalenterit, joissa käytetään peruskalenteria: _\#_ | Tämä ominaisuus odottaa. Peruskalenteri ohitetaan sillä hetkellä, kun suunnittelun optimointi on käytössä. |
| Erän käsittelykoodit | Ei-netottavissa olevan erän käsittelykoodin päätiedot: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä erän käsittelykoodit ohitetaan, kun suunnittelun optimointi on otettu käyttöön. |
| Saatavuus (CTP) | Tilauksen oletusasetukset, joiden toimituspäivämäärä on asetettu saatavuuteen (CTP): _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä CTP ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. |
| Kopioi staattinen dynaamiseen suunnitelmaan | Staattisen kopioiminen ja dynaamiseen suunnitelmaan on käytössä pääsuunnitteluparametreissa. | Suunnittelun optimointi ei kopioi staattista suunnitelmaa dynaamiseen suunnitelmaan riippumatta tästä asetukseen. Yleensä tämä käsite ei ole yhtä merkityksellinen, koska suunnittelu optimointi tarjoaa nopeuden ja täydellisen uudistamisen. Jos käytössä on vähintään kaksi suunnitelmaa, pääsuunnittelu on käynnistettävä kunkin suunnitelman osalta. |
| Vahvistus | Automaattisen vahvistuksen aikaraja ja kattavuusryhmiä määritetty: _\#_ | Version 10.0.7 ja uudempien versioiden vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. |
| Vahvistus | Automaattisen vahvistuksen määrittäminen ja nimikekattavuustietueet: _\#_ | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. |
| Vahvistus | Määritä pääsuunnitelmat ja automaattinen vahvistus: _\#_ | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. |
| FitAnalysisPlanningItems | Suunnittelunimikkeet: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä suunnittelunimikkeitä käsitellään tavallisten nimikkeiden tapaan, kun suunnittelun optimointi on käytössä. |
| Ennusteet | Kattavuusryhmät, joiden "sisällytetyt konsernitilaukset" ovat käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä pääsuunnitteluun ei kuulu loppupään suunniteltua kysyntää, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. Huomaa, että vapautetut/vahvistetut tilaukset toimivat säännöllisesti konsernin sisäisissä toiminnoissa ja kattavat useimmat skenaariot. |
| Ennusteet | Kattavuusryhmät, joiden ennuste on "Pienennä ennustetta"-asetuksen arvoksi on määritetty eri arvo kuin "Tilaukset": _\#_ | Oletusarvon mukaan suunnittelun optimointi käyttää tilauksille "Pienennä ennustetta" -asetusta tästä asetuksesta riippumatta. |
| Ennusteet | Ennustemallit, joissa osamalleja: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä alamalleja käyttäviä ennusteita ei tueta, kun suunnittelun optimointi on käytössä. Ne ohitetaan riippumatta tästä asetuksesta. |
| Ennusteet | Pääsuunnitelmat, joiden "sisältää tarjontaennusteen" -asetukset ovat käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjontaennusteita ei tueta, kun suunnittelun optimointi on käytössä. Ne ohitetaan riippumatta tästä asetuksesta. |
| Lukitusaikaraja | Kattavuusryhmät, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. |
| Lukitusaikaraja | Kohteen kattavuustietueet, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. |
| Lukitusaikaraja | Pääsuunnitelmat, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. |
| Konsernin sisäinen | Pääsuunnitelmat, mukaan lukien suunniteltu tuotantovirran kysyntä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä pääsuunnitteluun ei kuulu loppupään suunniteltua kysyntää, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. Huomaa, että vapautetut/vahvistetut tilaukset toimivat normaalisti konsernin sisäisissä toiminnoissa ja kattavat useimmat skenaariot. |
| Kanban | Kohteen kattavuusrekisterit, joissa on suunniteltu tilaustyyppi kanban: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kanbaniin määritetty nimikekattavuus ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-suunnitellun tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. |
| Kanban | Nimikkeet, joiden oletusjärjestystyyppi on kanban: _\#_ | Tällä hetkellä kanbaniin määritetty oletustilaustyyppi ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-oletuksen tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. |
| Tuotantoympäristö | Tuoterakennerivit, joilla on pyöristys tai useita asetuksia: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä pyöristystä ja useita asetuksia ei oteta huomioon tuoterakenneriveillä, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on kaavan mittaus: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kaavan mittaa ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään nimikkeen korvausta (suunnitteluryhmät): _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä nimikkeen korvausta (suunnitteluryhmät) ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on negatiivinen määrä: _\#_ | Tämä ominaisuus odottaa. Tuoterakenne- ja kaavarivit, joilla on negatiivinen määrä, sisällytetään määrään 0 (nolla), ja järjestelmä antaa varoituksen, kun suunnittelun optimointi on otettu käyttöön. |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään resurssin kulutusta: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä resurssien kulutusta käyttävät tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään vaiheittaista kulutusta: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä vaiheenkulutusta ei oteta huomioon, kun tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Tuoterakenteet, joille on määritetty vakiohävikki tai muuttuva hävikki: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tuoterakenteissa määritetyt vakiohävikki ja muuttuva hävikki ohitetaan, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Tuoterakenteet, joissa käytetään alihankintaa: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä alihankinta-asetus ohitetaan tuoterakenteissa, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. |
| Tuotantoympäristö | Tuoterakenteet ilman sivustoa: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tuoterakenteet ilman sivustoa ohitetaan, kun suunnittelun optimointi on otettu käyttöön. |
| Tuotantoympäristö | Kysyntä tietyillä määritetyillä tuoterakenne- tai reititysvaatimuksilla: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kysyntään määritetyt tuoterakenne- tai reititysvaatimukset (kuten alituoterakenne tai myyntitilauksen alireititys) ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Vakiotuoterakennetta tai -reittiä käytetään tähän asetukseen katsomatta. |
| Tuotantoympäristö | Kaavan versiot, joissa on oheis-/sivutuotteita: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kaavaversioon liittyvät oheistuotteet ja sivutuotteet ohitetaan, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Kaavan versiot ja saanto: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tuotto, joka liittyy kaavaversioon ohitetaan, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Suunnitelmat, joissa käytetään järjestystä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä järjestys ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. |
| Tuotantoympäristö | Aloittamattomat vapautetut tuotantotilaukset, joiden aikataulutettu aloitus on ennen kuluvaa päivää: _\#_ | Tämä ominaisuus odottaa. |
| Tuotantoympäristö | Aikataulutetut resurssit, joilla on rajallinen kapasiteetti: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä rajallisella kapasiteetilla ajoitetut resurssit ohitetaan, kun suunnittelun optimointi on käytössä. Ajoittaminen tapahtuu tuotteen oletusläpimenoajan perusteella. |
| Tuotantoympäristö | Suunnittelussa käytetyt reitit: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä reitit ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Käytetään tuotteen oletusläpimenoaikaa. |
| Tuotantoympäristö | Hajotusta käyttävä myyntirivin varaus: _\#_ | Hajotustoimintoa käyttävä myyntirivin varaus ei ole tuettu, kun suunnittelun optimointi on käytössä. |
| Tuotantoympäristö | Aikataulutus tuotantotilausten hajotuksen kanssa: _\#_ | Aikataulu, joka käyttää tuotantotilausten räjähdystä ei ole tuettu, kun suunnittelun optimointi on käytössä. Tuotantotilaukset voidaan ajoittaa yksitellen. |
| Tarjouspyyntö | Pääsuunnitelmat ja tarjouspyyntö käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjouspyyntöjä (RFQs) ei pidetä vaatimuksina, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. |
| Ehdotukset | Pääsuunnitelmat, joissa ehdotukset on otettu käyttöön: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä vaatimuksia ei oteta huomioon, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. |
| Varmuusmarginaalit | Kattavuusryhmät varmuusmarginaalin kanssa: _\#_ | Tämä ominaisuus odottaa. Turvamarginaali ohitetaan sillä hetkellä, kun suunnittelun optimointi on käytössä. Voit kompensoida tämän ongelman suurentaen läpimenoaikaa niin, että se sisältää turvamarginaalin. |
| Varmuusmarginaalit | Pääsuunnitelmat varmuusmarginaalin kanssa: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä turvamarginaali ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. Voit kompensoida tämän ongelman suurentaen läpimenoaikaa niin, että se sisältää turvamarginaalin. |
| Varmuusvaraston täyttäminen | Nimikkeiden kattavuustiedot, joissa on "täytä vähimmäisvaatimukset", poikkeavat tämän päivän päivämäärästä ja hankinta-ajasta: _\#_ | Suunnittelun optimointi käyttää aina *kuluvan päivän päivämäärää ja hankinta-aikaa*. Tämä muutos tehdään, kun halutaan valmistautua yksinkertaistettuihin suunnitteluasetuksiin tulevaisuudessa. Jos toimitusaika ei sisälly varmuusvarastoon, nykyiselle alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. Tämä voi aiheuttaa merkittäviä meluongelmia ja ei-toivottuja suunniteltuja tilauksia. Paras käytäntö on muuttaa asetusta siten, että *kuluvan päivän päivämäärää + hankinta-aikaa* käytetään. |
| Myyntitarjoukset | Pääsuunnitelmat ja myyntitarjoukset käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjouksia ei oteta huomioon, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. |
| Säilyvyysaika | Pääsuunnitelmat, joissa säilyvyysaika on otettu käyttöön: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä säilyvyysaikaa ei oteta huomioon, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. |

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)
