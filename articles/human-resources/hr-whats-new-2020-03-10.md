---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (10. maaliskuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 10. maaliskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526909"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (10. maaliskuuta 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2985. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Osaamiseroanalyysiraporttia ei voi käyttää (394460)

Tätä raporttia ei tueta Dynamics 365 Human Resources -sovelluksessa. SSRS-raportin tulostamisen valikkonimike on poistettu.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Virheellinen sanoma Aloitus-sivun käyttämiselle (417950)

Tämän muutoksen vuoksi suojaus piilottaa valikkonimikkeen, jos sinulla ei ole lomakkeen käyttöoikeutta.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Työntekijöiden tehtävien ylläpidon tehostaminen (380538)

Työntekijöiden tehtävien ylläpidon lomakkeessa ovat kaikki työntekijän tehtävät perehdyttämisestä irtisanomiseen, siirtymisiin ja liiketoimintaprosesseihin. Voit poistaa, delegoida uudelleen tai päivittää tehtävien tilan.

Esimerkki: Benjamin Martin on etujen järjestelmänvalvoja. Työntekijän perehdytyksen aikana tehtävät luodaan Benjaminille, joka tarkistaa uuden työntekijän etuvalinnat. Benjaminilla on aiemmin tehtyjä tehtäviä sekä tulevia tehtäviä, jotka on vielä tekemättä. Benjamin päättää poistua yrityksestä, joten hänen tehtävänsä on joko delegoitava uudelleen tai poistettava. Tehtävien ylläpitolomake (**Työntekijä**-lomakkeen toimintoruudussa) antaa mahdollisuuden delegoida kaikki Benjaminin tehtävät uudelleen toiselle työntekijälle tai poistaa ne.  

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
| Uusi **Otsikko**-yksikkö | <ul><li>**Otsikko** lisätty</li></ul> Uusi **Otsikko**-entiteetti sisältyy Common Data Serviceen, mutta siihen ei viitata **Työtehtävä**- tai **Työ**-yksiköissä tällä hetkellä. |

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

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat käytettävissä 3. helmikuuta 2020:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Tulossa pian

### <a name="platform-update-33"></a>Ympäristön update 33 -päivitys

- Koko sivun sovellukset (esikatselu) - Tässä esikatselutoiminnossa, joka edellyttää Tallennetut näkymät -toiminnon käyttöönottoa, Power Apps ja kolmannen osapuolen sovellukset voidaan lisätä koko sivun kokemuksina koontinäytön kautta.

- Tallennetut näkymät (esikatselu) - Tämä esikatselutoiminto ottaa käyttöön tallennetut näkymät, jotka parantavat merkittävästi mukauttamisen alijärjestelmää. Tämän toiminnon avulla käyttäjillä voi olla useita nimettyjä mukautusjoukkoja sivulla. Voit myös julkaista näkymiä käyttöoikeusrooleihin.

- Optimoitu On eräs -suodatuskokemus - Tämä toiminto ottaa käyttöön optimoidun On eräs -suodatuskokemuksen, jonka avulla on helpompi syöttää useita suodatusarvoja. Se sisältää yksinkertaisemman mekanismin yksittäisten tai kaikkien suodatusarvojen poistamista varten. Siinä on myös kompakti ja intuitiivinen suodatusarvojen visualisointitoiminto.

- Suositeltavat kentät - Käyttäjien on usein lisättävä kenttiä ruudukkoon tai sivulle. Tämä voi olla vaikeaa, jos kenttiä on paljon. Tämän toiminnon avulla järjestelmä voi hakea suositeltujen kenttien joukon sen sijaan, että käyttäjän olisi selattava pitkää luetteloa. Järjestelmä määrittää kentät sen perusteella, mitä käyttäjä useimmiten lisäävät samanlaisiin skenaarioihin.

- Lukitut oletustoiminnot ruudukoissa - Tämä toiminto varmistaa, että ruudukon oletustoiminto linkitetään tiettyyn sarakkeeseen ruudukossa siitä huolimatta, onko saraketta siirretty vai onko se piilotettu.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]