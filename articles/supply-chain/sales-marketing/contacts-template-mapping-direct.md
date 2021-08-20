---
title: Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin
description: Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 084030ab6ff06a1140621bb91435edf6cff4f82cc4bbc13813ab46f76e42174d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756844"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -taulut synkronoidaan suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin Yhteyshenkilö (Yhteyshenkilöt) -taulut Supply Chain Managementin Yhteyshenkilö (Asiakkaat) -tauluun.

- **Mallien nimet tietojen integroinnissa**

    - Yhteyshenkilöt (Salesista Supply Chain Managementiin) – suora
    - Yhteyshenkilöistä asiakkaaseen (Salesista Supply Chain Managementiin) - suora

- **Tietojen integrointiprojektin tehtävien nimet**

    - Yhteyshenkilöt
    - Yhteyshenkilö asiakkaaseen

Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Supply Chain Managementiin)

## <a name="entity-sets"></a>Yksikköjoukot

| Myynti    | Toimitusketjun hallinta |
|----------|------------------------|
| Yhteyshenkilöt | Dataversen yhteyshenkilöt           |
| Yhteyshenkilöt | Asiakkaat V2           |

## <a name="entity-flow"></a>Yksikön työnkulku

Yhteyshenkilöitä hallitaan Salesista ja synkronoidaan Supply Chain Managementiin.

Salesin yhteyshenkilöstä voi tulla Supply Chain Managementin yhteyshenkilö tai asiakas. Järjestelmä etsii Salesista seuraavat ominaisuudet ja määrittää synkronoidaanko Salesin yhteyshenkilö Supply Chain Managementiin yhteyshenkilönä vai asiakkaana:

- **Synkronointi Supply Chain Managementin asiakkaaseen:** yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Kyllä**
- **Synkronointi Supply Chain Managementin yhteyshenkilöön:** Yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai yhteyshenkilö) viittaa tiliin (eikä yhteyshenkilöön)

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

Uusi **On aktiivinen asiakas** -sarake on lisätty yhteyshenkilöön. Tämän sarakkeen avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole. **On aktiivinen asiakas** -asetuksena on **Kyllä** vain yhteyshenkilöille, joilla on liittyviä tarjouksia, tilauksia tai laskuja. Vain nämä yhteyshenkilöt synkronoidaan Supply Chain Managementiin asiakkaina.

Uusi **IsCompanyAnAccount**-sarake on lisätty yhteyshenkilöön. Tämä sarake osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö). Näillä tiedoilla tunnistetaan yhteyshenkilöt, jotka on synkronoitava Supply Chain Managementiin yhteyshenkilöinä.

Uusi **Yhteyshenkilön numero** -sarake on lisätty yhteyshenkilöön, jotta integroinnin luonnollinen ja yksilöllinen avain voidaan taata. Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **CON-01000-BVRCPS**

Kun Salesin integrointiratkaisu otetaan käyttöön, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -sarakkeen käyttämällä edellä mainittua numerosarjaa. Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -sarakkeen arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.

## <a name="in-supply-chain-management"></a>Supply Chain Managementiin

Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella. Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti. Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

- **CustomerGroup** on pakollinen Supply Chain Managementissa. Voit estää synkronointivirheet määrittämällä yhdistämismäärityksen oletusarvon. Oletusarvoa käytetään, jos sarake on tyhjä Salesissa.

    Oletusmallin arvo on **10**.

- Kun seuraavat yhdistämismääritykset lisätään, Supply Chain Managementissa tarvitaan vähemmän manuaalisia päivityksiä. Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.

    - **SiteId** – oletustoimipaikka voidaan määrittää myös Supply Chain Managementin tuotteissa. Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.

        Mallin **SiteId** arvoa ei ole määritetty.

    - **WarehouseId** – Oletusvarasto voidaan määrittää myös Supply Chain Managementin tuotteissa. Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.

        Mallin **WarehouseId** arvoa ei ole määritetty.

    - **LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.
    
        Oletusmallin arvo on **fi-fi**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä sarakkeen tiedot synkronoidaan Salesista Supply Chain Managementiin.

### <a name="contact-to-contact"></a>Yhteyshenkilöstä yhteyshenkilöön

![Mallin yhdistäminen tietojen integrointiohjelmassa.](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

![Mallin yhdistäminen tietojen integrointiohjelmassa.](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)

[Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin](accounts-template-mapping-direct.md)

[Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin](products-template-mapping-direct.md)

[Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä](sales-order-template-mapping-direct-two-ways.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]