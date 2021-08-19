---
title: Suunnittelun optimoinnin sopivuusanalyysi
description: Tässä ohjeaiheessa käsitellään, miten nykyisten asetusten ja tietojen yhteensopivuus suunnittelun optimointitoiminnon ominaisuuksien kanssa varmistetaan.
author: ChristianRytt
ms.date: 07/07/2021
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 52048ea6cced6f670faf13ef07f1288183e6d9b67a016608030f9e192a98faa7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751095"
---
# <a name="planning-optimization-fit-analysis"></a>Suunnittelun optimoinnin sopivuusanalyysi

[!include [banner](../../includes/banner.md)]

Suunnittelun optimoinnin sopivuusanalyysin tulos on analysoitava osana siirtoprosessia. Huomaa, että suunnittelun optimoinnin laajuus ei vastaa nykyistä sisältyvää pääsuunnittelutoimintoa. Siirtoon kannattaa valmistautua tekemällä yhteistyötä kumppanin kanssa ja tutustumalla ohjeisiin. 

Suunnittelun optimoinnin sopivuusanalyysin auttaa määrittämään, missä kohdissa sisältyvän pääsuunnittelumoduulin ja suunnittelun optimoinnin välillä voi olla eroja. Tämä analyysi tehdään nykyisten asetusten ja tietojen perusteella. 

Saat suunnittelun optimoinnin sopivuusanalyysin tulokset valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin sopivuusanalyysi** ja valitsemalla sitten **Suorita analyysi**. Jos analyysissa havaitaan ristiriitoja, ne mainitaan samalla sivulla. (Analyysin suorittaminen voi kestää muutaman minuutin.)

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

Seuraavassa taulukossa esitetään eri tulokset, jotka voidaan näyttää sopivan analyysin jälkeen. Numeromerkit (_\#_) korvataan numerolla, joka ilmaisee luettelossa olevan varasto-oton sisältävien tietojen määrän. Tuotetut tai esiversion toiminnot ovat saatavana versiossa 10.0.9 tai sitä uudemmassa versiossa (ellei Odotettu käytettävyys -sarakkeessa ole mainittu suurempi versionumero).

| Ominaisuus | Lueteltu ongelma | Selitys | Odotettu käytettävyys |
| --- | --- | --- | --- |
| Toimenpiteet | Kattavuusryhmät, joissa toimintojen laskenta on käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä toimintoja ei luoda pääsuunnittelun aikana, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. Toimenpiteiden pääasiallinen tarkoitus on ehdottaa muutoksia aiemmin luotuihin tilauksiin. Arvioi, onko toimia käytetty aktiivisesti osana liiketoimintaprosessejasi vai ovatko tilauksiin liittyvät viivetiedot riittäviä. | Huhtikuun 2022. |
| Peruskalenterit | Kalenterit, joissa käytetään peruskalenteria: _\#_ | Tämä ominaisuus odottaa. Peruskalenteri ohitetaan sillä hetkellä, kun suunnittelun optimointi on käytössä. Arvioi, onko peruskalenteri tarpeen liiketoimintaprosessiesi kannalta vai riittääkö suora määritys kalentereissa. | Huhtikuun 2022. | 
| Erän käsittelykoodit | Ei-netottavissa olevan erän käsittelykoodin päätiedot: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä erän käsittelykoodit ohitetaan, kun suunnittelun optimointi on otettu käyttöön. | Lokakuu 2022 tai myöhemmin |
| Saatavuus (CTP) | Tilauksen oletusasetukset, joiden toimituspäivämäärä on asetettu saatavuuteen (CTP): _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä CTP ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. | 2022. lokakuuta |
| Kopioi staattinen dynaamiseen suunnitelmaan | Staattisen kopioiminen ja dynaamiseen suunnitelmaan on käytössä pääsuunnitteluparametreissa. | Suunnittelun optimointi ei kopioi staattista suunnitelmaa dynaamiseen suunnitelmaan riippumatta tästä asetukseen. Yleensä tämä käsite ei ole yhtä merkityksellinen, koska suunnittelu optimointi tarjoaa nopeuden ja täydellisen uudistamisen. Jos käytössä on vähintään kaksi suunnitelmaa, pääsuunnittelu on käynnistettävä kunkin suunnitelman osalta. | 2022. lokakuuta |
| Vahvistus | Automaattisen vahvistuksen aikaraja ja kattavuusryhmiä määritetty: _\#_ | Version 10.0.7 ja uudempien versioiden vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| Vahvistus | Automaattisen vahvistuksen määrittäminen ja nimikekattavuustietueet: _\#_ | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| Vahvistus | Määritä pääsuunnitelmat ja automaattinen vahvistus: _\#_ | Version 10.0.7 ja uudempien versioiden automaattista vahvistamista tuetaan erillisenä kiinteyttämiserätyönä, kun pääsuunnittelu on suoritettu (jos _suunnittelun optimoinnin automaattinen vahvistus_ -toiminto on otettu käyttöön [ominaisuuksien hallinnassa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Huomaa, että suunnittelun optimoinnin automaattinen vahvistus perustuu tilauspäivämäärään (aloituspäivämäärä), ei tarvepäivämäärään (päättymispäivämäärä). Näin varmistetaan, että suunniteltujen tilausten vahvistaminen tapahtuu ajallaan ilman, että läpimenoaikaa tarvitsee sisällyttää vahvistuksen aikarajakohtaan. | Tuettu |
| FitAnalysisPlanningItems | Suunnittelunimikkeet: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä suunnittelunimikkeitä käsitellään tavallisten nimikkeiden tapaan, kun suunnittelun optimointi on käytössä. | Lokakuu 2022 tai myöhemmin |
| Ennuste | Kattavuusryhmät, joiden "sisällytetyt konsernitilaukset" ovat käytössä: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Konsernin sisäinen suunnittelu](Intercompany-planning.md) | Tuettu |
| Ennuste | Kattavuusryhmät, joiden ennuste on "Pienennä ennustetta"-asetuksen arvoksi on määritetty eri arvo kuin "Tilaukset": _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja: [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md) | Tuettu |
| Ennuste | Ennustemallit, joissa osamalleja: _\#_ |  Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja: [Pääsuunnittelu ja kysyntäennusteet](demand-forecast.md) | Tuettu |
| Ennuste | Pääsuunnitelmat, joiden "sisältää tarjontaennusteen" -asetukset ovat käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjontaennusteita ei tueta, kun suunnittelun optimointi on käytössä. Ne ohitetaan riippumatta tästä asetuksesta. | Lokakuu 2022 tai myöhemmin |
| Lukitusaikaraja | Kattavuusryhmät, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Ei saatavilla |
| Lukitusaikaraja | Kohteen kattavuustietueet, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Ei saatavilla |
| Lukitusaikaraja | Pääsuunnitelmat, joissa on lukittu aikaraja määritetty: _\#_ | Jäädytysaikarajaa ei käytetä usein, eikä sitä ole vielä suunniteltu suunnitteluoptimointia varten. Tällä hetkellä jäädytysaikarajan asetus ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Ei saatavilla |
| Konsernin sisäinen | Pääsuunnitelmat, mukaan lukien suunniteltu tuotantovirran kysyntä: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Konsernin sisäinen suunnittelu](Intercompany-planning.md) | Tuettu |
| Kanban | Kohteen kattavuusrekisterit, joissa on suunniteltu tilaustyyppi kanban: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kanbaniin määritetty nimikekattavuus ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-suunnitellun tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. | Lokakuu 2022 tai myöhemmin |
| Kanban | Nimikkeet, joiden oletusjärjestystyyppi on kanban: _\#_ | Tällä hetkellä kanbaniin määritetty oletustilaustyyppi ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Kanban-oletuksen tilauksen tyyppi luo varoituksen pääsuunnittelun aikana, ja suunnitellut ostotilaukset luodaan kattamaan liittyvä kysyntä. | Lokakuu 2022 tai myöhemmin |
| Tuotteen elinkaaren tila | Tuotteen elinkaaren tilat eivät ole aktiivisia suunnittelulle: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Sulje pois tuotteita, joissa on tietty tuotteen elinkaaren tila](product-lifecycle-state.md) | Tuettu |
| Tuotantoympäristö | Tuoterakennerivit, joilla on pyöristys tai useita asetuksia: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä pyöristystä ja useita asetuksia ei oteta huomioon tuoterakenneriveillä, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | 2021. lokakuuta |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on kaavan mittaus: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kaavan mittaa ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään nimikkeen korvausta (suunnitteluryhmät): _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä nimikkeen korvausta (suunnitteluryhmät) ei oteta huomioon tuoterakenneriveillä ja kaavassa, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen liittyvästä asetuksesta. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla on negatiivinen määrä: _\#_ | Tämä ominaisuus odottaa. Tuoterakenne- ja kaavarivit, joilla on negatiivinen määrä, sisällytetään määrään 0 (nolla), ja järjestelmä antaa varoituksen, kun suunnittelun optimointi on otettu käyttöön. Päivitä päätiedot ja varoitusten välttämiseksi. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään resurssin kulutusta: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä resurssien kulutusta käyttävät tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. Kun tätä toimintoa tuetaan, materiaalitarve määritetään tuotannon alkamispäivälle. Ennen tämän toiminnon tukemista tarpeita ei luoda sellaisille materiaaleille, jotka on merkitty resurssinkäyttömerkinnällä. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteen/kaavan rivit, joilla käytetään vaiheittaista kulutusta: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä vaiheenkulutusta ei oteta huomioon, kun tuoterakenne- ja kaavarivit ohitetaan, kun suunnittelun optimointi on käytössä. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteet, joille on määritetty vakiohävikki tai muuttuva hävikki: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tuoterakenteissa määritetyt vakiohävikki ja muuttuva hävikki ohitetaan, kun suunnittelun optimointi on käytössä. | 2022. lokakuuta |
| Tuotantoympäristö | Tuoterakenteet, joissa käytetään alihankintaa: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä alihankinta-asetus ohitetaan tuoterakenteissa, kun suunnittelun optimointi on käytössä riippumatta tästä asetuksesta. | Huhtikuun 2022. |
| Tuotantoympäristö | Tuoterakenteet ilman sivustoa: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Tuotannon suunnittelu](production-planning.md) | Tuettu |
| Tuotantoympäristö | Kysyntä tietyillä määritetyillä tuoterakenne- tai reititysvaatimuksilla: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kysyntään määritetyt tuoterakenne- tai reititysvaatimukset (kuten alituoterakenne tai myyntitilauksen alireititys) ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Vakiotuoterakennetta tai -reittiä käytetään tähän asetukseen katsomatta. | 2022. lokakuuta |
| Tuotantoympäristö | Kaavan versiot, joissa on oheis-/sivutuotteita: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä kaavaversioon liittyvät oheistuotteet ja sivutuotteet ohitetaan, kun suunnittelun optimointi on käytössä. | 2022. lokakuuta |
| Tuotantoympäristö | Kaavan versiot ja saanto: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tuotto, joka liittyy kaavaversioon ohitetaan, kun suunnittelun optimointi on käytössä. | 2022. lokakuuta |
| Tuotantoympäristö | Suunnitelmat, joissa käytetään järjestystä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä järjestys ohitetaan, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. | 2022. lokakuuta |
| Tuotantoympäristö | Aloittamattomat vapautetut tuotantotilaukset, joiden aikataulutettu aloitus on ennen kuluvaa päivää: _\#_ | Tämä ominaisuus odottaa. Jos tuotantotilaus tällä hetkellä viivästyy, pääsuunnittelu olettaa, että se valmistuu saman päivän aikana. Tällä on merkitystä vapautetuille tuotantotilauksille, joiden toimituspäivä on menneisyydessä mutta joita ei ole vielä saatu valmiiksi. | 2022. lokakuuta |
| Tuotantoympäristö | Aikataulutetut resurssit, joilla on rajallinen kapasiteetti: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä rajallisella kapasiteetilla ajoitetut resurssit ohitetaan, kun suunnittelun optimointi on käytössä. Ajoittaminen tapahtuu tuotteen oletusläpimenoajan perusteella. | 2022. lokakuuta |
| Tuotantoympäristö | Suunnittelussa käytetyt reitit: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä reitit ohitetaan, kun suunnittelun optimointi on otettu käyttöön. Käytetään tuotteen oletusläpimenoaikaa. | Esiversio: Tuettu (10.0.20), GA: Lokakuu 2021 |
| Tuotantoympäristö | Hajotusta käyttävä myyntirivin varaus: _\#_ | Hajotustoimintoa käyttävä myyntirivin varaus ei ole tuettu, kun suunnittelun optimointi on käytössä. | 2022. lokakuuta |
| Tuotantoympäristö | Aikataulutus tuotantotilausten hajotuksen kanssa: _\#_ | Aikataulu, joka käyttää tuotantotilausten räjähdystä ei ole tuettu, kun suunnittelun optimointi on käytössä. Tuotantotilaukset voidaan ajoittaa yksitellen. | 2022. lokakuuta |
| Tarjouspyyntö | Pääsuunnitelmat ja tarjouspyyntö käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjouspyyntöjä (RFQs) ei pidetä vaatimuksina, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. | 2022. lokakuuta |
| Ehdotukset | Pääsuunnitelmat, joissa ehdotukset on otettu käyttöön: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä. Lisätietoja on kohdassa [Ostoehdotukset](purchase-requisitions.md) | Tuettu |
| Varmuusmarginaalit | Kattavuusryhmät varmuusmarginaalin kanssa: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä osittain. Lisätietoja on kohdassa [Varmuusmarginaalit](safety-margins.md) | Vastaanottomarginaali: tuetaan. Uudelleentilausmarginaali ja toimitusmarginaali: tammikuu 2022 |
| Varmuusmarginaalit | Pääsuunnitelmat varmuusmarginaalin kanssa: _\#_ | Tätä ominaisuutta tuetaan tällä hetkellä osittain. Lisätietoja on kohdassa [Varmuusmarginaalit](safety-margins.md) | Vastaanottomarginaali: tuetaan. Uudelleentilausmarginaali ja toimitusmarginaali: tammikuu 2022 |
| Varmuusvaraston täyttäminen | Nimikkeiden kattavuustiedot, joissa on "täytä vähimmäisvaatimukset", poikkeavat tämän päivän päivämäärästä ja hankinta-ajasta: _\#_ | Suunnittelun optimointi käyttää aina *kuluvan päivän päivämäärää ja hankinta-aikaa*. Tämä muutos tehdään, kun halutaan valmistautua yksinkertaistettuihin suunnitteluasetuksiin tulevaisuudessa. Jos toimitusaika ei sisälly varmuusvarastoon, nykyiselle alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. Tämä voi aiheuttaa merkittäviä meluongelmia ja ei-toivottuja suunniteltuja tilauksia. Paras käytäntö on muuttaa asetusta siten, että *kuluvan päivän päivämäärää + hankinta-aikaa* käytetään. Päivitä päätiedot ja varoitusten välttämiseksi. | Ei saatavilla |
| Myyntitarjoukset | Pääsuunnitelmat ja myyntitarjoukset käytössä: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä tarjouksia ei oteta huomioon, kun suunnittelun optimointi on otettu käyttöön. Ne ohitetaan riippumatta tästä asetuksesta. | Lokakuu 2022 tai myöhemmin |
| Säilyvyysaika | Pääsuunnitelmat, joissa säilyvyysaika on otettu käyttöön: _\#_ | Tämä ominaisuus odottaa. Tällä hetkellä säilyvyysaikaa ei oteta huomioon, kun suunnittelun optimointi on käytössä riippumatta tästä asetukseen. | Huhtikuun 2022. |

## <a name="additional-resources"></a>Lisäresurssit

[Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
