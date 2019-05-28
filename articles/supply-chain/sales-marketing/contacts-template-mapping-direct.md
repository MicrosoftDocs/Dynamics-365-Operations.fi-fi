---
title: Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin
description: Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 5363c64cd1a475f0047c079d9166718ddc765f02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562356"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Common Data Service for Appsin tietojen integrointiin](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä. Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin yhteyshenkilön (yhteyshenkilöt) yksiköt Finance and Operationsin yhteyshenkilön (asiakkaat) yksikköön:

- **Mallien nimet tietojen integroinnissa:**

    - Yhteyshenkilöt (Salesista Fin and Opsiin) - suora
    - Yhteyshenkilöistä asiakkaaseen (Salesista Fin and Opsiin) - suora

- **Tehtävien nimet tietojen integrointiprojektissa:**

    - Yhteyshenkilöt
    - Yhteyshenkilö asiakkaaseen

Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Fin and Opsiin)

## <a name="entity-sets"></a>Yksikköjoukot

| Myynti    | Finance and Operations |
|----------|------------------------|
| Yhteyshenkilöt | CDS-yhteyshenkilöt           |
| Yhteyshenkilöt | Asiakkaat V2           |

## <a name="entity-flow"></a>Yksikön työnkulku

Yhteyshenkilöitä hallitaan Salesissa ja ne synkronoidaan Finance and Operationsiin.

Salesin yhteyshenkilöstä voi tulla Finance and Operationsin yhteyshenkilö tai asiakas. Järjestelmä etsii Sales-sovelluksesta seuraavat ominaisuudet ja määrittää synkronoidaanko Salesin yhteyshenkilö Finance and Operationsiin yhteyshenkilönä vai asiakkaana:

- **Synkronointi asiakkaaksi Finance and Operationsissa:** yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Kyllä**
- **Synkronointi yhteyshenkilöksi Finance and Operationsissa:** Yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai asiakas) viittaa tiliin (eikä yhteyshenkilöön)

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

Uusi **On aktiivinen asiakas** -kenttä on lisätty yhteyshenkilöön. Tämän kentän avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole. **On aktiivinen asiakas** -asetuksena on **Kyllä** vain yhteyshenkilöille, joilla on liittyviä tarjouksia, tilauksia tai laskuja. Vain nämä yhteyshenkilöt synkronoidaan Finance and Operationsiin asiakkaina.

Uusi **IsCompanyAnAccount**-kenttä on lisätty yhteyshenkilöön. Tämä kenttä osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö). Näillä tiedoilla tunnistetaan yhteyshenkilöt, jotka on synkronoitava Finance and Operationsiin yhteyshenkilöinä.

Uusi **Yhteyshenkilön numero** -kenttä on lisätty yhteyshenkilöön, jotta integroinnin luonnollinen ja yksilöllinen avain voidaan taata. Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **CON-01000-BVRCPS**

Kun Salesin integrointiratkaisu otetaan käyttöön, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -kentän käyttämällä edellä mainittua numerosarjaa. Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -kentän arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.

## <a name="in-finance-and-operations"></a>Finance and Operationsissa

Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella. Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti. Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

- **CustomerGroup** tarvitaan Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä yhdistämismäärityksen oletusarvon. Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.

    Oletusmallin arvo on **10**.

- Kun seuraavat yhdistämismääritykset lisätään, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä. Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.

    - **SiteId** – oletustoimipaikka voidaan määrittää myös Finance and Operationsin tuotteissa. Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.

        Mallin **SiteId** arvoa ei ole määritetty.

    - **WarehouseId** – oletusvarasto voidaan määrittää myös Finance and Operationsin tuotteissa. Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.

        Mallin **WarehouseId** arvoa ei ole määritetty.

    - **LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.
    
        Oletusmallin arvo on **fi-fi**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.

### <a name="contact-to-contact"></a>Yhteyshenkilöstä yhteyshenkilöön

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin](accounts-template-mapping-direct.md)

[Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin](products-template-mapping-direct.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-order-template-mapping-direct-two-ways.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin](sales-invoice-template-mapping-direct.md)


