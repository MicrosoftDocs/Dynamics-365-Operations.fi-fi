---
title: Myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottaminen käyttöön
description: Tässä artikkelissa käsitellään myyntitilausten tilasarakkeiden määrittämistä kaksoiskirjoitusta varten.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 2035985f16b5972e02f1ed60c6f02d306217f3be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288881"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottaminen käyttöön

[!include [banner](../../includes/banner.md)]

Ostotilauksen tilan ilmoittavilla sarakkeilla on erilaiset luettelointiarvot Microsoft Dynamics 365 Supply Chain Managementissa ja Dynamics 365 Salesissa. Näiden sarakkeiden yhdistämismääritys kaksoiskirjoituksessa edellyttää lisämäärityksiä.

## <a name="columns-in-supply-chain-management"></a>Supply Chain Managementin sarakkeet

Supply Chain Managementissa myyntitilauksen tilaan liittyy kaksi saraketta. Sarakkeet, joille on suoritettava yhdistämismääritys ovat **Tila** ja **Asiakirjan tila**.

**Tila**-luettelointi määrittää tilauksen yleisen tilan. Tämä tila näkyy tilauksen otsikossa.

**Tila**-luetteloinnilla on seuraavat arvot:

- Avoin tilaus
- Toimitettu
- Laskutettu
- Peruutettu

**Asiakirjan tila** -luettelointi määrittää viimeisimmän tilaukselle luodun asiakirjan. Jos tilaus on esimerkiksi vahvistettu, tämä asiakirja on myyntitilauksen vahvistus. Jos myynti tilaus on laskutettu osittain ja jäännösrivi vahvistetaan, asiakirjan tilana pysyy **Lasku**, koska lasku luodaan myöhemmin prosessissa.

**Asiakirjan tila** -luetteloinnilla on seuraavat arvot:

- Vahvistus
- Keräysluettelo
- Pakkausluettelo
- Lasku

## <a name="columns-in-sales"></a>Salesin sarakkeet

Salesissa myyntitilauksen tilaan liittyy kaksi saraketta. Sarakkeet, joille on suoritettava yhdistämismääritys, ovat **Tila** ja **Käsittelytila**.

**Tila**-luettelointi määrittää tilauksen yleisen tilan. Sillä on seuraavat arvot:

- Aktiiviset
- Lähetetty
- Täytetty
- Laskutettu
- Peruutettu

**Käsittelytila**-luettelointi otettiin käyttöön, jotta tilalle voidaan suorittaa tarkempi yhdistämismääritys Supply Chain Managementin kanssa.

Seuraavassa taulukossa esitetään **Käsittelytila**-arvon yhdistämismääritys Supply Chain Managementissa.

| Käsittelyn tila   | Tila Supply Chain Managementissa | Asiakirjan tila Supply Chain Managementissa |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktiiviset              | Avoin tilaus                        | None                                       |
| Vahvistettu           | Avoin tilaus                        | Vahvistus                               |
| Keräilty              | Avoin tilaus                        | Keräysluettelo                               |
| Osittain toimitettu | Avoin tilaus                        | Pakkausluettelo                               |
| Toimitettu           | Toimitettu                         | Pakkausluettelo                               |
| Osittain laskutettu  | Toimitettu                         | Lasku                                    |
| Laskutettu            | Laskutettu                          | Lasku                                    |
| Peruutettu           | Peruutettu                         | Ei käytettävissä                             |

Seuraavassa taulukossa esitetään **Käsittelytila**-arvon yhdistämismääritys Salesin ja Supply Chain Managementin välillä.

| Käsittelyn tila   | Tila Salesissa | Tila Supply Chain Managementissa |
|---------------------|-----------------|-----------------------------------|
| Aktiiviset              | Aktiiviset          | Avoin tilaus                        |
| Vahvistettu           | Lähetetty       | Avoin tilaus                        |
| Keräilty              | Lähetetty       | Avoin tilaus                        |
| Osittain toimitettu | Aktiiviset          | Avoin tilaus                        |
| Osittain laskutettu  | Aktiiviset          | Avoin tilaus                        |
| Osittain laskutettu  | Täytetty       | Toimitettu                         |
| Laskutettu            | Laskutettu        | Laskutettu                          |
| Peruutettu           | Peruutettu       | Peruutettu                         |

## <a name="setup"></a>Luo perustiedot

Voit määrittää myyntitilauksen tilasarakkeiden yhdistämismäärityksen ottamalla käyttöön määritteet **IsSOPIntegrationEnabled** ja **isIntegrationUser**.

Voit ottaa **IsSOPIntegrationEnabled**-määritteen käyttöön seuraavasti.

1. Siirry selaimessa osoitteeseen `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Korvaa **\<test-name\>** yrityksesi Sales-linkillä.
2. Etsi avatulla sivulla **organizationid** ja kirjoita arvo muistiin.

    ![organizationid-arvon etsiminen.](media/sales-map-orgid.png)

3. Avaa selainkonsoli Salesissa ja suorita seuraava komentosarja. Käytä vaiheen 2 **organizationid**-arvoa.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-koodi selainkonsolissa.](media/sales-map-script.png)

4. Varmista, että **IsSOPIntegrationEnabled**-arvona on **tosi**. Tarkista arvo vaiheen 1 URL-osoitteen avulla.

    ![IsSOPIntegrationEnabled-arvona on tosi.](media/sales-map-integration-enabled.png)

Voit ottaa **isIntegrationUser**-määritteen käyttöön seuraavasti.

1. Valitse Salesissa **Asetus \> Mukauttaminen \> Järjestelmän mukauttaminen**, valitse **Käyttäjätaulu** ja avaa sitten **Lomake \> Käyttäjä**.

    ![Käyttäjälomakkeen avaaminen.](media/sales-map-user.png)

2. Etsi kenttähaussa **Integrointikäyttäjän tila** ja lisää se lomakkeeseen kaksoisnapsauttamalla. Tallenna muutos.

    ![Integrointikäyttäjän tila -sarakkeen lisääminen lomakkeeseen.](media/sales-map-field-explorer.png)

3. Siirry Salesissa kohtaan **Asetus \> Suojaus \> Käyttäjät** ja vaihda näkymästä **Käytössä olevat käyttäjät** näkymään **Sovelluksen käyttäjät**.

    ![Näkymän vaihtaminen käytössä olevista käyttäjistä sovelluksen käyttäjiin.](media/sales-map-enabled-users.png)

4. Valitse kohdan **DualWrite IntegrationUser** kaksi merkintää.

    ![Sovelluksen käyttäjien luettelo.](media/sales-map-user-mode.png)

5. Muuta **Integrointikäyttäjän tila** -sarakkeen arvoksi **Kyllä**.

    ![Integrointikäyttäjän tila -sarakkeen arvon muuttaminen.](media/sales-map-user-mode-yes.png)

Myyntitilauksillesi on nyt suoritettu yhdistämismääritys.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
