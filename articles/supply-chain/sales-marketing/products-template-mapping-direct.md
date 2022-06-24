---
title: Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin
description: Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.
author: Henrikan
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 5195368f3de12c7e361905c3cca442067e39e000
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855958"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin

[!include [banner](../includes/banner.md)]



> [!NOTE]
> Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan suoraan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan tuotteet Supply Chain Managementista Salesiin.

- **Mallin nimi tietojen integroinnissa:** Tuotteet (Supply Chain Managementista Salesiin) – suora
- **Tehtävän nimi tietojen integrointiprojektissa:** Tuotteet

Synkronointitehtävät on suoritettava, ennen kuin tuotteen synkronointi on mahdollista.

## <a name="entity-set"></a>Yksikköjoukko

| Toimitusketjun hallinta    | Myynti    |
|----------------------------|----------|
| Myytävät vapautetut tuotteet | Tuotteet |

## <a name="entity-flow"></a>Yksikön työnkulku

Tuotteita hallitaan Supply Chain Managementissa ja synkronoidaan Salesiin. **Myytävät vapautetut tuotteet** -tietoyksikkö Supply Chain Managementissa vie vain tuotteet, jotka ovat *myytävissä*. Myytävissä olevat tuotteet ovat tuotteita, joille on määritetty tiedot myyntitilauksessa käyttämistä varten. Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnon avulla.

Tuotenumeroa käytetään avaimena. Tämän vuoksi jokaisella tuotevariantilla on oltava yksilöivä tuotetunnus, kun tuotevariantit synkronoidaan Salesiin.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti. Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana. Käytettävissä ovat seuraavat arvot:

- **Kyllä** – Tuote on peräisin Supply Chain Managementista eikä sitä voi muokata Salesissa.
- **Ei** – tuote kirjataan suoraan Salesissa.
- **(Tyhjä)** – tuote sijaitsi Salesissa ennen Prospektista käteiseksi -ratkaisun käyttöönottoa.

**On ulkoisesti ylläpidetty** -kenttä auttaa varmistamaan, että Supply Chain Managementiin synkronoidaan vain tarjoukset ja myyntitilaukset, joissa on ulkoisesti ylläpidettyjä tuotteita.

Ulkoisesti ylläpidetyt tuotteet lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan hinnastoon. Hinnastot järjestetään aakkosjärjestykseen nimen mukaan. Tuotteen Supply Chain Managementin myyntihintaa käytetään hinnaston hintana. Tämän vuoksi Salesissa on oltava hinnasto jokaiselle Supply Chain Managementin tuotteen myyntivaluutalle. Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.

> [!NOTE]
> - Tuotteen synkronointi ei onnistu, jos hinnastossa ei ole vastaavaa valuuttaa.
> - Voit määrittää integroinnissa käytettävän hinnaston yhdistämällä pricelevelid.name [oletus hinnasto (nimi)] tietojen integrointiprojektiin. Syötteen on oltava pienillä kirjaimilla. Esimerkiksi oletusarvoinen myynnin Vakio-niminen hinnasto voisi olla kohdekenttä: pricelevelid.name [Oletusarvoinen hinnasto (Nimi)] ja karttatyyppi: [ { ”transformType”: ”Default", "defaultValue": "standard} ].

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- Täytä Supply Chain Managementin aiemmin luotujen tuotteiden erillisen tuotteen taulu ennen ensimmäistä synkronointia. Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.

    1. Etsi **Täytä erillisen tuotteen taulu** Supply Chain Managementin hakutoiminnolla.
    2. Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**. Tämän työn voi suorittaa vain kerran.

- Varmista, että Supply Chain Managementin ja Salesin välillä on myynnin mittayksikön arvokartta **SalesUnitSymbol**- ja **DefaultUnit (Name)**-kohteen väliselle yhdistämismääritykselle.
- Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) arvomääritys siten, että se vastaa Salesin **yksikköryhmiä**.

    Oletusmallin arvo on **Oletusyksikkö**.

- Varmista, että kaikkien Supply Chain Managementin tuotteiden myynnin mittayksiköt ovat Salesissa.
- Varmista, että Salesissa on hinnasto jokaiselle Supply Chain Managementin tuotteen myyntivaluutalle.
- Kun tuotteet luodaan Salesissa, niiden tila on **Luonnos** tai **Aktiivinen**. Toimintaa ohjataan Salesissa kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales**.

    Tuotteet, joiden tila on **Luonnos** luomisen jälkeen, on aktivoitava ennen tarjouksiin tai myyntitilauksiin lisäämistä.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Supply Chain Managementiin.

![Mallin yhdistäminen tietojen integrointiohjelmassa.](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-articles"></a>Liittyvät artikkelit

[Prospektista käteiseksi](prospect-to-cash.md)

[Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin](accounts-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä](sales-order-template-mapping-direct-two-ways.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]