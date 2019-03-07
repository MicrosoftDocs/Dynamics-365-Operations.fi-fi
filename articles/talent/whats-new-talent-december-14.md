---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (14. joulukuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304136"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (14. joulukuuta 2018)

[!include [banner](includes/banner.md)]

**Koontiversio 8.1.2085**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="changes"></a>Muutokset

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>US - ACA (Affordable Care Act) -tuki verovuoden 2018 1095-B- ja 1095-C-lomakkeille

ALE (Applicable Large Employer) -työnantajien on annetta jokaiselle kokoaikaiselle työntekijälle 1095-C-lomake. Jos työnantaja lisäksi tarjoaa omakustanteisen vakuutuksen, työnantajan on annettava lomake 1095-C (jos ALE-työnantaja) ja 1095-B (jos pienyrittäjä) kaikille koko- ja osa-aikaisille työntekijöille, joita jokin tarjolla olevista sairausvakuutussuunnitelmista koskee. Tämä ominaisuus sisältää tulostettavat 1095-C- ja 1095-B-lomakkeet.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>SubmittedByPersonId-kenttä ohitetaan tuonnin aikana HcmPerfJournalEntity-kohdassa

Kun suorituskyvyn kirjauskansiovientejä tuodaan tai viedään, **Lähettäjä**-kenttä ohitetaan. Tämän muutoksen myötä **tuotu tai viety** arvo vastaa taulukossa viennin aikana olevaa arvoa, kun tuotava järjestelmä päivitetään tuontitiedoston antamalla arvolla.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Loma ja poissaolo -työtilan Analytiikka-välilehdessä on OpenConnectionError-virhe, jos käytössä on jokin muu kuin järjestelmänvalvojan rooli.

Tämän päivityksen myötä virhettä ei anneta, kun **Analytiikka**-välilehti avataan **Loma ja poissaolot** -työtilassa.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Työntekijän itsepalvelussa tehty toimihierarkiaan porautuminen ruudusta ei päädy pääsolmuun

Tehty muutos korjaa Pääsolmun hakeminen epäonnistui -virheen tilanteissa, joissa toimihierarkia on mukautettu näkymään aiemmin luodussa työtilassa ja hierarkiassa on valittu toimi.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Vain järjestelmänvalvoja näkee Toimi-sivun Palkanlaskenta-välilehden

Tehty muutos korjaa aiemmin luodun oikeuden, Ylläpidä palkanlaskennan työntekijöiden ja toimien tietoja, suojauselementit. Tämän muutoksen myötä palkanlaskentakoordinaattorilla on oletusarvoisesti Toimi-sivun Palkanlaskenta-kenttien käyttöoikeudet.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Virhe lähetettäessä suorituskykyarviota esimiehelle ja %Reviews.PerfPeriod%-paikkamerkin käyttö lähetysohjeissa

Tehty muutos korjaa Tyhjä viittaus -virheen, kun %Reviews.PerfPeriod%-paikkamerkkiä käytetään lähetysohjeissa.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Työvoiman Power BI -raportti näyttää virheen, kun työntekijän ikälisäpäivä on karkauspäivänä.

Tämän muutoksen ansiosta Power BI tukee nyt karkauspäiviä.

### <a name="integration-between-core-hr-and-attract"></a>Core HR:n ja Attractin välinen integraatio

Tehty muutos päivittää palkattaviin kandidaatteihin liittyvän Core HR:n ja Attractin välisen integraation. Jos palkattavien ehdokkaiden halutaan näkyvän **Henkilöstön hallinta** -työtilassa, käytössä on seuraavat CDS for Apps (CDS 2.0) -yksiköt:

Työhakemus
- Tilan syyksi on määritettävä Tarjous hyväksytty
-   Ilmaisee hakijan ja avoimen työpaikan

Ehdokas
-   Ilmaisee ehdokkaan tiedot

Avoin työpaikka
-   Ilmaisee avoimen työpaikan tunnuksen ja avoimen työpaikan osallistujat

Avoimen työpaikan osallistujat
-   Ilmaisee työhön ottavan esimiehen

Kun ehdokas on lisätty henkilöstön hallintaan, kyseinen ehdokas voidaan nyt myös hylätä ehdokaskortissa olevalla uudella asetuksella.

## <a name="coming-soon"></a>Tulossa pian

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Loma ja poissaolot: tuleva loma ja lomasaldojen ennustaminen

Koska tehtävät muutokset mahdollistavat sen, että työntekijät voivat ennustaa poissaoloja ja tehdä tulevaisuuteen sijoittuvia poissaolopyyntöjä ilman, että se vaikuttaa heidän nykyisiin poissaolosaldoihinsa, myös poissaolosaldojen näyttäminen on muuttumassa. 

Tällä hetkellä näytettävä käytettävissä oleva saldo on pyyntöjen käytettävissä oleva vapaa-aikasumma, joka sisältää kertymät, kuluva päivä mukaan lukien, ja kaikki hyväksytyt lomapyynnöt ajanjakson loppuun. 

Kun ennustemahdollisuus julkaistaan, saldo näyttää muutokset nykyiseen poissaolosaldoon mukaan lukien kuluvan päivän sisältävät kertymät ja pyynnöt. Työntekijät ja esimiehet näkevät nämä päivitetyt saldot työntekijän ja esimiehen itsepalvelutoiminnossa **Poissaoloaika**-kortissa ja **Poissaolosaldot**-ikkunassa. Henkilöstöpäälliköt näkevät nämä päivitetyt saldot **Henkilöt**-työtilassa ja työntekijän **Määritetyt lomasuunnitelmat** -ikkunassa.

## <a name="known-issue"></a>Tunnettu ongelma

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Finance and Operations -integraatiossa ilmenevät määritysvirheet

Seuraavat ongelmat on havaittu nykyisessä mallissa, jolla Talent integroidaan Dynamics 365 for Finance and Operationsin kanssa. Uusi malli julkaistaan pian, ja sitä käytetään kaikissa uusissa luotavissa integraatioprojekteissa. Aiemmin luoduissa integraatioprojekteissa päivitetään tehtävän yhdistämismääritykset. Lisätietoja on seuraavassa päivitettyjen yhdistämismääritysten taulukossa. 

>[!NOTE]
> Toimet toimien päätyöhön määrittävä tehtävä ei integroi tietoja. Tätä ongelmaa tutkitaan parhaillaan. Ongelmaa ei välttää nykyisessä yhdistämismäärityksessä. 

Osastot toimintayksikköön -tehtävän seuraavat yhdistämismääritykset on päivitettävä.

| Aiemmin luotu lähdekenttä          | Uusi lähdekenttä |
| -------------------------------|------------------|
| cdm_description (kuvaus)  | cdm_name (nimi)  |

Lisäksi on lisättävä lisäyhdistämismääritys. Lisää seuraava yhdistämismääritys valitsemalla viimeinen **Ei mitään**.

| Lähdetaulu                   | Kohdekenttä    |
| -------------------------------|----------------------|
| cdm_description (kuvaus)  | NAMEALIAS (NAMEALIAS)|

Päivitettyjen yhdistämismääritysten pitäisi olla seuraavassa kuvassa olevien kaltaisia.

![Osastot tehtäväyksiköihin -tehtävä](./media/DepartmentMapping.png)


Työt työn tietoihin -tehtävän seuraavat yhdistämismääritykset on päivitettävä.

| Aiemmin luotu lähdekenttä          | Uusi lähdekenttä                   |
| -------------------------------|------------------------------------|
| cdm_name (nimi)                | cdm_description (kuvaus)      |
| cdm_name (kuvaus)         | cdm_jobdescription (työn kuvaus)|


Päivitettyjen yhdistämismääritysten pitäisi olla alla olevassa kuvassa olevien kaltaisia.

![Työt töiden tietoihin -tehtävä](./media/JobMapping.png)

Työntekijät työhön -tehtävän seuraavat yhdistämismääritykset on päivitettävä.

| Aiemmin luotu lähdekenttä                 | Uusi lähdekenttä                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (sähköpostiosoite 1)   | cdm_primaryemailaddress (ensisijainen sähköpostiosoite |
| cdm_telephone1 (puhelinnumero 1)          | cdm_primarytelephone (ensisijainen puhelinnumero)       |

Myös Sukupuoli-kentän muutos on päivitettävä. Valitse sukupuolelle **fn** (toiminto) -määritystyyppi ja päivitä seuraavat arvon yhdistämismääritykset.

| CDS-arvo                   | Finance and Operations -arvo                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Mies                                             |
| 75440001                    | Nainen                                           |
| 75440002                    | Ei mitään                                             | 
| 75440003                    | Yksilöimätön                                      |

Päivitettyjen yhdistämismääritysten pitäisi olla seuraavissa kuvissa olevien kaltaisia.

![Työntekijät työntekijään -tehtävä](./media/WorkerMapping.png)

![Sukupuoli-kentän muutos](./media/WorkerTransform.png)
