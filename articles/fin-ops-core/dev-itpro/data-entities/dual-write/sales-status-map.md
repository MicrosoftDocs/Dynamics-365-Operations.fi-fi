---
title: Myyntitilauksen tilakenttien yhdistämismäärityksen määrittäminen
description: Tässä ohjeaiheessa selitetään, miten myyntitilausten tilakentät määritetään kaksoiskirjoitusta varten.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829282"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>Myyntitilauksen tilakenttien yhdistämismäärityksen määrittäminen

[!include [banner](../../includes/banner.md)]

Ostotilauksen tilan ilmoittavilla kentillä on erilaiset luettelointiarvot Microsoft Dynamics 365 Supply Chain Managementissa ja Dynamics 365 Salesissa. Näiden kenttien yhdistämismääritys kaksoiskirjoituksessa edellyttää lisämäärityksiä.

## <a name="fields-in-supply-chain-management"></a>Kentät Supply Chain Managementissa

Supply Chain Managementissa myyntitilauksen tilaan liittyy kaksi kenttää. Kentät, joille on suoritettava yhdistämismääritys ovat **Tila** ja **Asiakirjan tila**.

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

## <a name="fields-in-sales"></a>Kentät Salesissa

Salesissa myyntitilauksen tilaan liittyy kaksi kenttää. Kentät, joille on suoritettava yhdistämismääritys ovat **Tila** ja **Käsittelytila**.

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

Voit määrittää myyntitilauskenttien yhdistämismäärityksen ottamalla käyttöön määritteet **IsSOPIntegrationEnabled** ja **isIntegrationUser**.

Voit ottaa **IsSOPIntegrationEnabled**-määritteen käyttöön seuraavasti.

1. Siirry selaimessa osoitteeseen `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Korvaa **\<test-name\>** yrityksesi Sales-linkillä.
2. Etsi avatulla sivulla **organizationid** ja kirjoita arvo muistiin.

    ![organizationid-arvon etsiminen](media/sales-map-orgid.png)

3. Avaa selainkonsoli Salesissa ja suorita seuraava komentosarja. Käytä vaiheen 2 **organizationid**-arvoa.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-koodi selainkonsolissa](media/sales-map-script.png)

4. Varmista, että **IsSOPIntegrationEnabled**-arvona on **tosi**. Tarkista arvo vaiheen 1 URL-osoitteen avulla.

    ![IsSOPIntegrationEnabled-arvona on tosi](media/sales-map-integration-enabled.png)

Voit ottaa **isIntegrationUser**-määritteen käyttöön seuraavasti.

1. Siirry Salesissa kohtaan **Asetus \> Mukauttaminen \> Järjestelmän mukauttaminen**, valitse **Käyttäjäyksikkö** ja avaa sitten**Lomake \> Käyttäjä**.

    ![Käyttäjälomakkeen avaaminen](media/sales-map-user.png)

2. Etsi kenttähaussa **Integrointikäyttäjän tila** ja lisää se lomakkeeseen kaksoisnapsauttamalla. Tallenna muutos.

    ![Integrointikäyttäjän tila -kentän lisääminen lomakkeeseen](media/sales-map-field-explorer.png)

3. Siirry Salesissa kohtaan **Asetus \> Suojaus \> Käyttäjät** ja vaihda näkymästä **Käytössä olevat käyttäjät** näkymään **Sovelluksen käyttäjät**.

    ![Näkymän vaihtaminen käytössä olevista käyttäjistä sovelluksen käyttäjiin](media/sales-map-enabled-users.png)

4. Valitse kohdan **DualWrite IntegrationUser** kaksi merkintää.

    ![Sovelluksen käyttäjien luettelo](media/sales-map-user-mode.png)

5. Muuta **Integrointikäyttäjän tila** -kentän arvoksi **Kyllä**.

    ![Integrointikäyttäjän tila -kentän arvon muuttaminen](media/sales-map-user-mode-yes.png)

Myyntitilauksillesi on nyt suoritettu yhdistämismääritys.
