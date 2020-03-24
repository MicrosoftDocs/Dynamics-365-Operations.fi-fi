---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092749"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.2927. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Palvelupyyntöjen hallinnan siirtymisen ja tietojen hallinnan kehyksen (DMF) yksikön (414754) käyttöönotto

Tämä esikatselutoiminto ottaa käyttöön lisänavigoinnin palvelupyyntöjen hallinnan palvelupyyntöjä varten. Voit ottaa tämän esikatselutoiminnon käyttöön **Toimintojen hallinta** -työtilassa. Nämä valikkovaihtoehdot näkyvät **Yhteensopivuus**-työtilassa  Dynamics 365 Human Resources -sovelluksessa. Tämän muutoksen avulla Human Resources voi tehdä seuraavaa:

- Kaikki tapaukset
- Omat tapaukset
- Omat avoimet tapaukset
- Erääntyneet tapaukset
- Työnkulun avulla minulle määritetyt tapaukset

Näiden uusien palvelupyyntönäkymien avulla käytettävissä on myös **Palvelupyynnön tiedot** -DMF-yksikkö.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Suhteen määritysten käyttöönotto yleisessä osoitekirjassa (414762)

Yhteydet ovat nyt käytössä yleisessä osoitekirjassa. Ennen tämän viikon julkaisua **Suhde**-tietoruutu näytti kaikki järjestelmän määrittämät suhteet. Nyt voit määrittää nämä suhteet yleisen osoitekirjan sivulla.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Toimi voidaan poistaa, kun toimella on aktiivisia kompensaatiotietueita (414568)

Tämän muutoksen myötä näkyviin tulee varoitus, jos yrität poistaa toimen ja työntekijällä on aktiivinen kompensaatiotietue samaa toimea varten. Jos näin käy, työntekijän kiinteä kompensaatiotietue on päivitettävä ennen toimen poistamista.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Suorituskyvyn tarkistuksen työnkulku lisää joskus kuittaukset henkilöiltä, jotka eivät ole prosessin osa (414171)

Tämä muutos korjaa ongelman, jossa kirjausten lisäosallistujat lisätään suorituskyvyn arvioon.

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a>Työntekijän toimen tehtävää ei luoda Common Data Servicessä, kun valinta tehdään Uusi työntekijä -valintaikkunassa (413479)

Tämä muutos korjaa ongelman, kun uusi työntekijä palkataan ja tämä liitetään toimeen **Uusi työntekijä** -valintaikkunassa. Nyt toimen tehtävä näkyy Common Data Service -sovelluksessa.

## <a name="coming-soon"></a>Tulossa pian

### <a name="updated-common-data-service-solution"></a>Päivitetty Common Data Service -ratkaisu

Uusi Common Data Service -ratkaisu tulee pian saataville seuraavin muutoksin:

| Kuvaus | Muutos |
| ----------------------------------------- | --- |
| **Työn/toimen** yksikön muutokset | **Kompensaatioalue** lisätty</br>**Taloushallinnon dimensiot** lisätty |
| **Työntekijä**-yksikön muutokset | **Nimien järjestys** lisätty</br>**Työskentelee kotoa** lisätty</br>**Kieliä** lisätty</br>**Ikälisäpäivä** lisätty</br>**Vuosipäivän päivämäärä** lisätty</br>**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty |
| **Työsuhde**-yksikön muutokset | **Taloushallinnon dimensiot** lisätty</br>**Irtisanomisen syy** lisätty</br>**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</br>**Koeajan päivämäärä** lisätty |
| **Työntekijän osoite**-yksikön muutokset | **Katuosoite** lisätty</br>**Osoiterivi 1**, **Osoiterivi 2**ja **Osoiterivi 3**, jotka on merkitty poistettaviksi |
| Uudet muuttuvat kompensaatioasetusten entiteetit | **Muuttuvan kompensaatiosuunnitelman tyyppi**</br>**Muuttuva kompensaatiosuunnitelma**</br>**Hyvityssäännöt**</br>**Muuttuvan kompensaatiosuunnitelman taso** |
| Uusi **Työntekijäkalenterin työ**-yksikkö | **Työkalenteriyksikkö** lisätty |
| Uusi **Palkanlaskennan toimen tiedot** -yksikkö | **Palkanlaskennan toimen tiedot** lisätty |
| Uusi **Otsikko**-yksikkö | **Otsikko** lisätty. Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Common Data Service -sovellusten välillä. Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä. |

Seuraavien viikkojen aikana nämä yksikön muutokset ovat käytettävissä kaikissa ympäristöissä. Voit asentaa Human Resources -sovelluksen uusimman Common Data Service -ratkaisun manuaalisesti seuraavasti:

1.  Siirry [Power Platform-hallintakeskukseen](https://admin.powerplatform.microsoft.com).

2.  Valitse **Ympäristö**.

3.  Etsi ympäristö, jonka haluat päivittää. Tämän on vastattava Human Resources -sovelluksen **ympäristön nimeä** **Common Data Service -tiedot** -osan **Tietoja**-lomakkeessa.

4.  Valitse ympäristö, jos haluat tarkastella ympäristön tietoja.

5.  Valitse **Hallitse ratkaisuja** -painike yläosan toimintopalkista. Näyttöön avautuu uusi selainikkuna. Siirry **Dynamics 365 -hallintakeskukseen** ympäristössäsi.

6.  Valitse **Ratkaisu**-luettelossa **Dynamics 365 Human Resources -ankkuri**.

7.  Ota uusin ratkaisu käyttöön valitsemalla **Päivitä versio**.

## <a name="in-preview"></a>Esiversiossa

Seuraavat esikatseluominaisuudet ovat olleet käytettävissä 3. helmikuuta 2020 alkaen:

- Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).