---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (24. maaliskuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 24. maaliskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87b7ea660d94c6d564a8f09d4133b098e0ecedf9
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526908"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (24. maaliskuuta 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.3073. Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Henkilöstöhallinnon ympäristörajoitukset perustuvat nyt päivitettyihin lisensseihin (394595)

Lifecycle Servicesin (LCS) projektikohtainen raja-arvo on muuttunut. Edellinen raja oli kaksi ympäristöä. LCS:n henkilöresursseihin voidaan luoda tuotanto- ja eristysympäristöjen enimmäismäärä, joka perustuu nyt päivitettyihin lisensseihin. Voit nyt luoda niin monta ympäristöä LCS-projektia kohden kuin on tarpeen riippuen ostettujen lisenssien määrästä. Uusi käyttöoikeussopimus, joka päivitettiin 1. helmikuuta 2020, sallii asiakkaiden ostaa lisäympäristöjä. Lisätietoja lisäympäristöjen käyttöoikeusvaatimuksista on kohdassa [Dynamics 365-lisensointiopas](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Alustan muutokset

- Koko sivun sovellukset (esikatselu) - Tässä esikatselutoiminnossa, joka edellyttää Tallennetut näkymät -toiminnon käyttöönottoa, Power Apps ja kolmannen osapuolen sovellukset voidaan lisätä koko sivun kokemuksina koontinäytön kautta.

- Tallennetut näkymät (esikatselu) - Tämä esikatselutoiminto ottaa käyttöön tallennetut näkymät, jotka parantavat merkittävästi mukauttamisen alijärjestelmää. Tämän toiminnon avulla käyttäjillä voi olla useita nimettyjä mukautusjoukkoja sivulla. Voit myös julkaista näkymiä käyttöoikeusrooleihin.

- Optimoitu On eräs -suodatuskokemus - Tämä toiminto ottaa käyttöön optimoidun On eräs -suodatuskokemuksen, jonka avulla on helpompi syöttää useita suodatusarvoja. Se sisältää yksinkertaisemman mekanismin yksittäisten tai kaikkien suodatusarvojen poistamista varten. Siinä on myös kompakti ja intuitiivinen suodatusarvojen visualisointitoiminto.

- Suositeltavat kentät - Käyttäjien on usein lisättävä kenttiä ruudukkoon tai sivulle. Tämä voi olla vaikeaa, jos kenttiä on paljon. Tämän toiminnon avulla järjestelmä voi hakea suositeltujen kenttien joukon sen sijaan, että käyttäjän olisi selattava pitkää luetteloa. Järjestelmä määrittää kentät sen perusteella, mitä käyttäjä useimmiten lisäävät samanlaisiin skenaarioihin.

- Lukitut oletustoiminnot ruudukoissa - Tämä toiminto varmistaa, että ruudukon oletustoiminto linkitetään tiettyyn sarakkeeseen ruudukossa siitä huolimatta, onko saraketta siirretty vai onko se piilotettu.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Loman saldoa ei voida säätää suunnitelmalle, jolla ei ole kertymiä, ja joka luotiin usean lomatyypin ominaisuuden avulla (419635)

Tämän muutoksen avulla voit säätää lomasuunnitelmien saldoja, jotka on luotu ominaisuuksien hallinnassa käyttämällä Usean lomatyypin (esikatselu) -ominaisuuutta.

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat olleet käytettävissä 3. helmikuuta 2020 alkaen:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service -ratkaisu on nyt käytettävissä seuraavin muutoksin:

| kuvaus | Vaihda |
| --- | --- |
| **Työn/toimen** yksikön muutokset | <ul><li>**Kompensaatioalue** lisätty</li>|
| **Työtehtävän dimensio** -yksikkö lisätty | <ul><li>**Taloushallinnon dimensiot** lisätty</li>
| **Työntekijä**-yksikön muutokset | <ul><li>**Nimien järjestys** lisätty</li><li>**Työskentelee kotoa** lisätty</li><li>**Kieliä** lisätty</li><li>**Ikälisäpäivä** lisätty</li><li>**Vuosipäivän päivämäärä** lisätty</li><li>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty</li></ul> |
| **Työsuhde**-yksikön muutokset | <ul><li>**Taloushallinnon dimensiot** lisätty</li><li>**Irtisanomisen syy** lisätty</li><li>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</li><li>**Koeajan päivämäärä** lisätty</li></ul> |
| **Työntekijän osoite**-yksikön muutokset | <ul><li>**Katuosoite** lisätty</li><li>**Osoiterivi 1**, **Osoiterivi 2** ja **Osoiterivi 3**, jotka on merkitty poistettaviksi</li></ul> |
| Uudet muuttuvat kompensaatioasetusten entiteetit | <ul><li>**Muuttuvan kompensaatiosuunnitelman tyyppi**</li><li>**Muuttuva kompensaatiosuunnitelma**</li><li>**Hyvityssäännöt**</li><li>**Muuttuvan kompensaatiosuunnitelman taso**</li></ul> |
| Uusi **Työntekijäkalenterin työ**-yksikkö | <ul><li>**Työkalenteriyksikkö** lisätty</li></ul> |
| Uusi **Palkanlaskennan toimen tiedot** -yksikkö | <ul><li>**Palkanlaskennan toimen tiedot** lisätty</li></ul> |
| Uusi **Otsikko**-yksikkö | <ul><li>**Otsikko** lisätty</li></ul>Uusi **Otsikko**-entiteetti sisältyy Common Data Serviceen, mutta siihen ei viitata **Työtehtävä**- tai **Työ**-yksiköissä tällä hetkellä. |

> [!NOTE]
> Taloushallinnon dimensiot sekä toimissa että työsuhteessa mahdollistavat yksisuuntaisen integroinnin päivityksille Human Resourcesista Common Data Serviceen. Taloushallinnon dimensioiden päivityksiä ei tällä hetkellä synkronoida Common Data Service -sovelluksesta Human Resources -sovellukseen.

Seuraavien viikkojen aikana nämä yksikön muutokset ovat käytettävissä kaikissa ympäristöissä. Voit asentaa Human Resources -sovelluksen uusimman Common Data Service -ratkaisun manuaalisesti seuraavasti:

1.  Siirry [Power Platform-hallintakeskukseen](https://admin.powerplatform.microsoft.com).

2.  Valitse **Ympäristö**.

3.  Etsi ympäristö, jonka haluat päivittää. Ympäristön on vastattava Human Resources -sovelluksen **ympäristön nimeä** **Common Data Service -tiedot** -osan **Tietoja**-lomakkeessa.

4.  Valitse ympäristö, jos haluat tarkastella ympäristön tietoja.

5.  Valitse **Hallitse ratkaisuja** -painike yläosan toimintopalkista. Näyttöön avautuu uusi selainikkuna. Siirry **Dynamics 365 -hallintakeskukseen** ympäristössäsi.

6.  Valitse **Ratkaisu**-luettelossa **Dynamics 365 Human Resources -ankkuri**.

7.  Ota uusin ratkaisu käyttöön valitsemalla **Päivitä versio**.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-esikatselu ei toimi joissakin ympäristöissä

Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:

1. Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti. Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa. Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi. Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa. Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä. Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.

2. Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.

3. Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.

4. Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.

## <a name="coming-soon"></a>Tulossa pian

## <a name="new-production-release-cadence"></a>Uusi tuotantojulkaisunopeus

Huhtikuussa julkaistavan henkilöresurssien julkaisurytmi siirtyy viikoittaisesta päivityksestä kahden viikon välein tapahtuvaan päivitykseen. Kaikkien alueiden palvelupäivitysten käyttöönottoprosessi kestää kaksi viikkoa, jotta varmistetaan yhdenmukaisuus turvallisten käyttöönottokäytäntöjen kanssa ja ylläpidetään palvelun korkeaa vakautta ja luotettavuutta. Lisätestejä ja -näyttöjä otetaan käyttöön, jotta varmistetaan onnistunut käyttöönotto prosessin kaikissa vaiheissa. Lisätietoja julkaisurytmin prosessista on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Tunnetut ongelmat

## <a name="employment-detail-entity"></a>Työsuhteen tiedot -yksikkö

**Työsuhteen tiedot** -yksikköön on päivitetty seuraavat kentät: **Maksutiheys**, **Työsuhteen luokan tunnus**, **Työsuhteen tyyppi**, **Työnsuhteen tyypin tunnus** ja **Etujen työsuhdetila**. Näiden kenttien asetustiedot perustuvat siihen, että ominaisuuksien hallinnassa otetaan käyttöön toimintojen hallinta. Näitä kenttiä ei saa täyttää tai päivittää **Työsuhteen tiedot** -yksiköstä, koska ne aiheuttavat virheitä tuonnin aikana.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]