---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 25. helmikuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d9ff9b524a5812bd309fc33d6aa4ba4a92d687b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051182"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Työntekijän toimen tehtävää ei luoda Dataversessä, kun valinta tehdään Uusi työntekijä -valintaikkunassa (413479)

Tämä muutos korjaa ongelman, kun uusi työntekijä palkataan ja tämä liitetään toimeen **Uusi työntekijä** -valintaikkunassa. Nyt toimen tehtävä näkyy Dataverse -sovelluksessa.

## <a name="coming-soon"></a>Tulossa pian

### <a name="updated-dataverse-solution"></a>Päivitetty Dataverse -ratkaisu

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

3.  Etsi ympäristö, jonka haluat päivittää. Tämän on vastattava Human Resources -sovelluksen **ympäristön nimeä** **Common Data Service -tiedot** -osan **Tietoja**-lomakkeessa.

4.  Valitse ympäristö, jos haluat tarkastella ympäristön tietoja.

5.  Valitse **Hallitse ratkaisuja** -painike yläosan toimintopalkista. Näyttöön avautuu uusi selainikkuna. Siirry **Dynamics 365 -hallintakeskukseen** ympäristössäsi.

6.  Valitse **Ratkaisu**-luettelossa **Dynamics 365 Human Resources -ankkuri**.

7.  Ota uusin ratkaisu käyttöön valitsemalla **Päivitä versio**.

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