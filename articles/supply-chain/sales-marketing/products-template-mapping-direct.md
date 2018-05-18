---
title: Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ae50372edcd473f2288f8172b71eac33e24b636
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Salesiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan tuotteet Finance and Operationsista Salesiin.

- **Mallin nimi tietojen integroinnissa:** Tuotteet (Fin and Opsista Salesiin) – suora
- **Tehtävän nimi tietojen integrointiprojektissa:** Tuotteet

Synkronointitehtävät on suoritettava, ennen kuin tuotteen synkronointi on mahdollista.

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations     | Myynti    |
|----------------------------|----------|
| Myytävät vapautetut tuotteet | Tuotteet |

## <a name="entity-flow"></a>Yksikön työnkulku

Tuotteita hallitaan Finance and Operationsissa ja synkronoidaan Salesiin. **Myytävät vapautetut tuotteet** -tietoyksikkö Finance and Operationsissa vie vain tuotteet, jotka ovat *myytävissä*. Myytävissä olevat tuotteet ovat tuotteita, joille on määritetty tiedot myyntitilauksessa käyttämistä varten. Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnon avulla.

Tuotenumeroa käytetään avaimena. Tämän vuoksi jokaisella tuotevariantilla on oltava yksilöivä tuotetunnus, kun tuotevariantit synkronoidaan Salesiin.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti. Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana. Käytettävissä ovat seuraavat arvot:

- **Kyllä** – tuote on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.
- **Ei** – tuote kirjataan suoraan Salesissa.
- **(Tyhjä)** – tuote sijaitsi Salesissa ennen Prospektista käteiseksi -ratkaisun käyttöönottoa.

**On ulkoisesti ylläpidetty** -kentän avulla voidaan varmistaa, että vain sellaiset tarjoukset ja myyntitilaukset, joissa on ulkoisesti ylläpidettyjä tuotteita, synkronoidaan Finance and Operationsiin.

Ulkoisesti ylläpidetyt tuotteet lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan hinnastoon. Hinnastot järjestetään aakkosjärjestykseen nimen mukaan. Tuotteen Finance and Operationsin myyntihintaa käytetään hinnaston hintana. Tämän vuoksi Salesissa on oltava hinnasto jokaiselle Finance and Operationsin tuotteen myyntivaluutalle. Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.

> [!NOTE]
> Tuotteen synkronointi ei onnistu, jos hinnastossa ei ole vastaavaa valuuttaa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- Täytä Finance and Operationsin aiemmin luotujen tuotteiden erillisen tuotteen taulu ennen ensimmäistä synkronointia. Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.

    1. Etsi **Täytä erillisen tuotteen taulu** Finance and Operationsin hakutoiminnolla.
    2. Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**. Tämän työn voi suorittaa vain kerran.

- Varmista, että Finance and Operationsin ja Salesin välillä on myynnin mittayksikön arvokartta **SalesUnitSymbol**- ja **DefaultUnit (Name)**-kohteen väliselle yhdistämismääritykselle.
- Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) arvomääritys siten, että se vastaa Salesin **yksikköryhmiä**.

    Oletusmallin arvo on **Oletusyksikkö**.

- Varmista, että kaikkien Finance and Operationsin tuotteiden myynnin mittayksiköt ovat Salesissa.
- Varmista, että Salesissa on hinnasto jokaiselle Finance and Operationsin tuotteen myyntivaluutalle.
- Kun tuotteet luodaan Salesissa, niiden tila on **Luonnos** tai **Aktiivinen**. Toimintaa ohjataan Salesissa kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales**.

    Tuotteet, joiden tila on **Luonnos** luomisen jälkeen, on aktivoitava ennen tarjouksiin tai myyntitilauksiin lisäämistä.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin](accounts-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-order-template-mapping-direct-two-ways.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-invoice-template-mapping-direct.md)




