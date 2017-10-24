---
title: Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista Microsoft Dynamics 365 for Salesiin."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi. 

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista Microsoft Dynamics 365 for Salesiin.

## <a name="template-and-task"></a>Malli ja tehtävä

Seuraavat mallit ja tehtävät, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista (Finance and Operations) Microsoft Dynamics 365 for Salesiin (Sales).

-   Mallin nimi: tuotteet (Fin and Opsista Salesiin)

-   Projektin tehtävän nimi: tuotteet

Ennen tuotteen synkronointia synkronoitavat tehtävät: ei mitään

## <a name="entity-set"></a>Yksikköjoukko

| **Finance and Operations** | **CDS** | **myynti**  |
|----------------------------|---------|------------|
| Myytävät vapautetut tuotteet | Tuote | Tuotteet   |

## <a name="entity-flow"></a>Yksikön työnkulku

Tuotteita hallitaan Finance and Operationsissa ja synkronoidaan Salesiin. Finance and Operationsin tietoyksikkö **Myytävät vapautetut tuotteet** vie vain myytävät tuotteet, joten tuotteissa on tietoja, joita tarvitaan myyntitilauksessa. Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnolla.

**Tuotenumero** toimii avaimena; toisin sanoen tuotevariantit synkronoidaan CDS:ään ja Salesiin siten, kullakin **tuotevariantilla** on oma **tuotetunnus**.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti. Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana.

-   **On ulkoisesti ylläpidetty = Kyllä**: tuote on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.

-   **On ulkoisesti ylläpidetty = Ei**: tuote kirjataan suoraan Salesissa.

-   **On ulkoisesti ylläpidetty = tyhjä**: tuote sijaitsee Salesissa ennen ratkaisua prospektista käteiseksi.

**On ulkoisesti ylläpidetty** -tiedoilla voidaan varmistaa, että vain sellaiset **tarjoukset** ja **myyntitilaukset**, joissa on valittu **Ulkoisesti ylläpidetyt tuotteet**, synkronoidaan Finance and Operationsiin.

**Ulkoisesti ylläpidetyt tuotteet** lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan **hinnastoon**. Huomaa, että luettelo on järjestetty aakkosjärjestykseen **nimen** mukaan. Tuotteen Finance and Operationsin myyntihintaa käytetään **hinnaston** hintana. Tämän vuoksi Salesissa on oltava **hinnasto** jokaiselle Finance and Operationsin **tuotteen myyntivaluutalle**. Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.

> [!NOTE]
> Tuotteen synkronointi ei onnistu, jos **hinnaston** valuutta ei täsmää.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

-   Täytä Finance and Operationsin aiemmin luotujen tuotteiden **Erillisen tuotteen taulu** ennen ensimmäistä synkronointia. Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.

    -   Etsi **Täytä erillisen tuotteen taulu** Finance and Operationsin hakutoiminnolla.

    -   Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**. Tämä työ on suoritettava vain kerran.

-   Varmista, että tarvittava Finance and Operationsin myynnin **mittayksikön** **ValueMap** sijaitsee kohdassa **Lähde -\> CDS-yhdistäminen SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Päivitä **CDS-organisaation tunnus Organization_OrganizationId** valitsemalla **Lähde -\> CDS**.

    -   Oletusmallin arvo palautetaan oletusarvoon ORG001.

-   Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) **ValueMap** kohdassa **CDS -\> Kohde** siten, että se vastaa Salesin **Yksikköryhmiä**.

    -   Mallin arvo palautetaan oletusarvoon **Oletusyksikkö**.

-   Varmista **CDS-keräilyluettelot**-arvon avulla, että kaikkien Finance and Operationsin tuotteiden myynnin mittayksiköt ovat Salesissa.

-   Varmista, että Salesissa on **hinnasto** jokaiselle Finance and Operationsin tuotteen myyntivaluutalle.

-   Salesissa luotavien tuotteiden tila voi olla **Luonnos** tai **Aktiivinen**. Sitä hallitaan valitsemalla Salesissa **Järjestelmäasetukset** **Sales**-kohdassa.

    -   Luonnos-tilassa olevat luodut tuotteet on aktivoitava, ennen kuin ne voidaan lisätä **tarjoukseen** tai **myyntitilaukseen**.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

![mallin yhdistäminen tietojen integrointiohjelmassa](./media/products-template-mapping-data-integrator-1.png)

![mallin yhdistäminen tuotteita varten tietojen integrointiohjelmassa](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin](accounts-template-mapping.md)

[Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping.md)

[Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin](sales-quotation-template-mapping.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-order-template-mapping.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-invoice-template-mapping.md)


