---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (3. maaliskuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 3. maaliskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04ef5e35cdf6ea43e8e655ed6a1e30e8d1bb9038
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692860"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (3. maaliskuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2955. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse -ratkaisu on nyt käytettävissä seuraavin muutoksin:

Uusi Dataverse -ratkaisu tulee pian saataville seuraavin muutoksin:

| Kuvaus | Muutos |
| ----------------------------------------- | --- |
| **Työn/toimen** yksikön muutokset | **Kompensaatioalue** lisätty</br>**Taloushallinnon dimensiot** lisätty |
| **Työntekijä**-yksikön muutokset | **Nimien järjestys** lisätty</br>**Työskentelee kotoa** lisätty</br>**Kieliä** lisätty</br>**Ikälisäpäivä** lisätty</br>**Vuosipäivän päivämäärä** lisätty</br>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty |
| **Työsuhde**-yksikön muutokset | **Taloushallinnon dimensiot** lisätty</br>**Irtisanomisen syy** lisätty</br>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</br>**Koeajan päivämäärä** lisätty |
| **Työntekijän osoite**-yksikön muutokset | **Katuosoite** lisätty</br>**Osoiterivi 1**, **Osoiterivi 2** ja **Osoiterivi 3**, jotka on merkitty poistettaviksi |
| Uudet muuttuvat kompensaatioasetusten entiteetit | **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>**Muuttuva kompensaatiosuunnitelma**</br>**Hyvityssäännöt**</br>**Muuttuvan kompensaatiosuunnitelman taso** |
| Uusi **Työntekijäkalenterin työ**-yksikkö | **Työkalenteriyksikkö** lisätty |
| Uusi **Palkanlaskennan toimen tiedot** -yksikkö | **Palkanlaskennan toimen tiedot** lisätty |
| Uusi **Otsikko**-yksikkö | **Otsikko** lisätty. Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Dataverse -sovellusten välillä. Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä. |

Seuraavien viikkojen aikana nämä yksikön muutokset ovat käytettävissä kaikissa ympäristöissä. Voit asentaa Human Resources -sovelluksen uusimman Dataverse -ratkaisun manuaalisesti seuraavasti:

1.  Siirry [Power Platform-hallintakeskukseen](https://admin.powerplatform.microsoft.com).

2.  Valitse **Ympäristö**.

3.  Etsi ympäristö, jonka haluat päivittää. Ympäristön on vastattava Human Resources -sovelluksen **ympäristön nimeä** **Common Data Service -tiedot** -osan **Tietoja**-lomakkeessa.

4.  Valitse ympäristö, jos haluat tarkastella ympäristön tietoja.

5.  Valitse **Hallitse ratkaisuja** -painike yläosan toimintopalkista. Näyttöön avautuu uusi selainikkuna. Siirry **Dynamics 365 -hallintakeskukseen** ympäristössäsi.

6.  Valitse **Ratkaisu**-luettelossa **Dynamics 365 Human Resources -ankkuri**.

7.  Ota uusin ratkaisu käyttöön valitsemalla **Päivitä versio**.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Tuontiongelmat Lomaympäristö-tietoyksikön kanssa (406082)

Voit nyt ilmoittaa työntekijän uuteen samantyyppiseen lomasuunnitelmaan, jos uusi ilmoittautumispäivämäärä on myöhempi kuin edellisen suunnitelman vanhentunut ilmoittautumispäivämäärä.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Ongelma osuusmäärien viennissä 401k payrollWorkerEnrolledBenefitDetail-yksikköön DMF:ssä (420700)

Tämä muutos korjaa vientitoiminnon **payrollWorkerEnrolledBenefitDetail**-yksikössä vastaamaan työnantajan osuuden nykyisiä arvoja.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Tehostetun työntekijän lomakkeen haku aiheuttaa sanoman, jossa sanotaan Henkilö-kenttä on täytettävä (402525).

Kun haet työntekijää, et enää saa sanomaa, jossa pyydetään täyttämään **Henkilö**-kenttä.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Huomautuskentän arvoa hahmonneta Lisää osaamisalueita -lomakkeessa (380134)

Tämä muutos korjaa ongelman, jos räätälöit **Lisää osaamisalueita** -lomakkeen työntekijän itsepalvelussa.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Useat kiinteät kompensaatiosuunnitelmat eivät vanhene, kun työntekijöitä siirretään (389466)

Kun tämä muutos on käytössä, kaikki vanhan toimen aktiiviset kiinteät kompensaatiotietueet vanhenevat siirtymispäivänä.

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat olleet käytettävissä 3. helmikuuta 2020 alkaen:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]