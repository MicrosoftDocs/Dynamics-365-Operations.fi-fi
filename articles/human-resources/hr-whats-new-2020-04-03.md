---
title: Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 3, 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 02243b2c75a4f50683a51c1d9d811f2e2a2d413f
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555048"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 3, 2020)

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.3111. Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Ominaisuudet, jotka ovat yleensä saatavilla 6. huhtikuuta viikolla

- **Lomien ja poissaolojen ominaisuudet** - Lisätietoja lomista ja poissaoloista on kohdassa [Lomien ja poissaolojen yleiskatsaus](hr-leave-and-absence-overview.md).

- **Etujen hallinnan yleiskuvaus** - Lisätietoja on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Henkilöstöhallinnon ympäristörajoitukset perustuvat nyt päivitettyihin lisensseihin (394595)

LCS:n projektikohtainen raja-arvo on muuttunut. Edellinen raja oli kaksi ympäristöä. LCS:n henkilöresursseihin voidaan luoda tuotanto- ja eristysympäristöjen enimmäismäärä, joka perustuu nyt päivitettyihin lisensseihin. Voit nyt luoda niin monta ympäristöä LCS-projektia kohden kuin on tarpeen riippuen ostettujen lisenssien määrästä. Uusi käyttöoikeussopimus, joka päivitettiin 1. helmikuuta 2020, sallii asiakkaiden ostaa lisäympäristöjä. Lisätietoja lisäympäristöjen käyttöoikeusvaatimuksista on kohdassa [Dynamics 365-lisensointiopas](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Virhe yritettäessä poistaa kyselylomaketta (428603)

Tämän viikon päivitys korjaa ongelman, jossa kyselylomaketta poistettaessa näyttöön tulee seuraava virhe:

Havaittiin epäsymmetrinen X++ TTSBEGIN/TTSCOMMIT-pari.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Suorituskykykirjauskansion ja ammattisertifikaattien tietoturvaongelma (428499)

Tämä muutos rajoittaa sekä suorituskykykirjauskansioiden että ammatillisten sertifikaattien näkyvyyttä niiden yritysten perusteella, joihin heillä on käyttöoikeus. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Québecin ja Manitoban lyhenne (387510)

Aloitustiedot on päivitetty kuvaamaan Manitoban ja Quebecin oikeaa lyhennettä.

## <a name="new-entities-available-in-data-management-framework"></a>Uusia yksiköitä käytettävissä Data Management Frameworkissa

Seuraavat yksiköt ovat nyt käytettävissä. Jos nämä yksiköt eivät näy yksikköluettelossa, käytä **Päivitä yksiköt** -asetusta kohdassa **Framework-parametrit > Yksikköasetukset > Päivitä yksikköluettelo**.

 - Loma- ja poissaolopankin tapahtuma V2
 - Loman ja poissaolon rekisteröinti V2
 - Loma- ja poissaolosuunnitelman taso V2
 - Loma- ja poissaolosuunnitelma V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service -ratkaisu on nyt käytettävissä seuraavin muutoksin:

| kuvaus | Vaihda |
| --- | --- |
| **Työn/toimen** yksikön muutokset | <ul><li>**Kompensaatioalue** lisätty</li>|
| **Työtehtävän dimensio** -yksikkö lisätty | <ul><li>**Taloushallinnon dimensiot** lisätty</li>
| **Työntekijä**-yksikön muutokset | <ul><li>**Nimien järjestys** lisätty</li><li>**Työskentelee kotoa** lisätty</li><li>**Kieliä** lisätty</li><li>**Ikälisäpäivä** lisätty</li><li>**Vuosipäivän päivämäärä** lisätty</li><li>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty</li></ul> |
| **Työsuhde**-yksikön muutokset | <ul><li>**Taloushallinnon dimensiot** lisätty</li><li>**Irtisanomisen syy** lisätty</li><li>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</li><li>**Koeajan päivämäärä** lisätty</li></ul> |
| **Työntekijän osoite**-yksikön muutokset | <ul><li>**Katuosoite** lisätty</li><li>**Osoiterivi 1**, **Osoiterivi 2**ja **Osoiterivi 3**, jotka on merkitty poistettaviksi</li></ul> |
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

## <a name="in-preview"></a>Esiversiossa

## <a name="leave-suspension"></a>Loman keskeytys

Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Siirtokirjauksen suorituksen säännöt

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Tulossa pian

## <a name="new-production-release-cadence"></a>Uusi tuotantojulkaisunopeus

Huhtikuussa julkaistavan henkilöresurssien julkaisurytmi siirtyy viikoittaisesta päivityksestä kahden viikon välein tapahtuvaan päivitykseen. Kaikkien alueiden palvelupäivitysten käyttöönottoprosessi kestää kaksi viikkoa, jotta varmistetaan yhdenmukaisuus turvallisten käyttöönottokäytäntöjen kanssa ja ylläpidetään palvelun korkeaa vakautta ja luotettavuutta. Lisätestejä ja -näyttöjä otetaan käyttöön, jotta varmistetaan onnistunut käyttöönotto prosessin kaikissa vaiheissa. Lisätietoja julkaisurytmin prosessista on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Tunnetut ongelmat

## <a name="employment-detail-entity"></a>Työsuhteen tiedot -yksikkö

**Työsuhteen tiedot** -yksikköön on päivitetty seuraavat kentät: **Maksutiheys**, **Työsuhteen luokan tunnus**, **Työsuhteen tyyppi**, **Työnsuhteen tyypin tunnus** ja **Etujen työsuhdetila**. Näiden kenttien asetustiedot perustuvat siihen, että ominaisuuksien hallinnassa otetaan käyttöön toimintojen hallinta. Näitä kenttiä ei saa täyttää tai päivittää **Työsuhteen tiedot** -yksiköstä, koska ne aiheuttavat virheitä tuonnin aikana.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-esikatselu ei toimi joissakin ympäristöissä

Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:

1. Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti. Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa. Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi. Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa. Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä. Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.

2. Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.

3. Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.

4. Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)