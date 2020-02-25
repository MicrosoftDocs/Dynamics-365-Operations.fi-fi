---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (21. tammikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c0c303ec5d009fce0c975eb797f018b5e27a41eb
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982404"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (21. tammikuuta 2020)

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Talentin uusia tai muuttuneita toimintoja.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia. Olemme lisänneet toimintoja Attractiin tukemaan viime ilmoitustamme, [Menestyvämmän työvoiman rakentaminen Dynamics 365 Human Resourcesin avulla](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Lataa ympäristön tiedot

Järjestelmänvalvojat voivat ladata ympäristönsä tiedot. Tiedot viedään standardi-JSON-muodossa, jossa kaikki työt, ehdokkaat ja konfiguroinnit ovat zip-tiedostona. Lisätietoja on kohdassa [Tietojen vieminen Attractiin ja Onboardiin](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)avulla.

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Muiden kuin järjestelmänvalvoja-käyttäjien ympäristöjen käyttöoikeuksien rajoittaminen

Järjestelmänvalvojat voivat nyt rajoittaa muiden kuin järjestelmänvalvoja-käyttäjien ympäristön käyttöä. Tätä toimintoa ei voi kumota. Lisätietoja on ohjeaiheessa [Attractin käyttöoikeus](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

### <a name="exporting-onboarding-guides"></a>Vie perehdytysoppaat

Käyttäjät voivat nyt viedä kaikki perehdytysoppaansa ja perehdytysmallinsa Word-dokumentin muodossa. Lisätietoja on kohdassa [Tietojen vieminen Attractiin ja Onboardiin](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)avulla.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2726. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Viimeisimmän Vahvista työ -lomakkeen vuosittainen kompensaatiokenttä ei ole yhdenmukainen (392092)

Tämä versio sisältää muutoksen, joka näyttää viimeisimmän valuutan, joka perustuu **Vahvista työ** -lomakkeen yrityksen valitsimeen.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Tunnettu kenttä lisätään palautteen vastaanottajan hakuun (407789)

Kun työntekijöiden haku suoritetaan suorituskyvyn parantamiseksi, haku ei toimittanut riittävästi tietoja, joiden perusteella se voi määrittää, päätyykö palaute oikealle henkilölle. Lisäsimme **Tunnettu**-sarakkeen, joka auttaa tunnistamaan työntekijän yksilöllisen nimen.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo-tietue luodaan ilman liitosta työntekijään (394526)

Tämä julkaisu sisältää muutoksen, jonka mukaan HCMWorkerPayrollInfo-tietuetta ei tarvitse kirjoittaa ilman viittausta työntekijään.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Osaa muokata osastoa siirtyessäsi sijaintihierarkiasta (341001)

Kun suojaus on määritetty estämään muokkausosastojen käyttäminen, muokkaus poistetaan käytöstä, kun siirrytään **Osastot** -lomakkeeseen kaikissa skenaarioissa.

## <a name="coming-soon"></a>Tulossa pian

Uusi Common Data Service -ratkaisu tulee pian saataville seuraavin muutoksin:

| Kuvaus | Muutos |
| --- | --- |
| **Työn/toimen** yksikön muutokset | <ul><li>**Kompensaatioalue** lisätty</li><li>**Taloushallinnon dimensiot** lisätty</li></ul> |
| **Työntekijä**-yksikön muutokset | <ul><li>**Nimien järjestys** lisätty</li><li>**Työskentelee kotoa** lisätty</li><li>**Kieliä** lisätty</li><li>**Ikälisäpäivä** lisätty</li><li>**Vuosipäivän päivämäärä** lisätty</li><li>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty</li></ul> |
| **Työsuhde**-yksikön muutokset | <ul><li>**Taloushallinnon dimensiot** lisätty</li><li>**Irtisanomisen syy** lisätty</li><li>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</li><li>**Koeajan päivämäärä** lisätty</li></ul> |
| **Työntekijän osoite**-yksikön muutokset | <ul><li>**Katuosoite** lisätty</li><li>**Osoiterivi 1**, **Osoiterivi 2**ja **Osoiterivi 3**, jotka on merkitty poistettaviksi</li></ul> |
| Uudet muuttuvat kompensaatioasetusten entiteetit | <ul><li>**Muuttuvan kompensaatiosuunnitelman tyyppi**</li><li>**Muuttuva kompensaatiosuunnitelma**</li><li>**Hyvityssäännöt**</li><li>**Muuttuvan kompensaatiosuunnitelman taso**</li></ul> |
| Uusi **Työntekijäkalenterin työ**-yksikkö | <ul><li>**Työkalenteriyksikkö** lisätty</li></ul> |
