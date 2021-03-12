---
title: Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tilejä synkronoidaan suoraan Dynamics 365 Salesista Supply Chain Managementiin.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0499f604049240a226b4002710817034598b1e66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977710"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](https://docs.microsoft.com/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tilejä synkronoidaan suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa.  Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration). Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan tilit Salesista Supply Chain Managementiin:

- **Mallin nimi tietojen integroinnissa:** tilit (Salesista Fin and Opsiin) – suora
- **Projektin tehtävän nimi:** tilit – asiakkaat

Synkronointitehtävät on suoritettava, ennen kuin tilin ja asiakkaan synkronointi on mahdollista.

## <a name="entity-set"></a>Yksikköjoukko

| Myynti    | Toimitusketjun hallinta |
|----------|------------------------|
| Tilit | Asiakkaat V2           |

## <a name="entity-flow"></a>Yksikön työnkulku

Tilejä hallitaan Salesista ja synkronoidaan Supply Chain Managementiin asiakkaina. Näiden asiakkaiden **On ulkoisesti ylläpidetty** -ominaisuuden arvoksi on määritetty **Kyllä**, jotta Salesista peräisin olevia asiakkaita voidaan jäljittää. Näitä tietoja käytetään suodattamaan Salesiin synkronoitavat laskut laskutuksen aikana.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilinumero**-sarake on käytettävissä **Tili**-sivulla. Se on nyt luontainen ja yksilöllinen avain, joka tukee integrointia. Asiakkuudenhallinta- eli CRM-ratkaisun luonnollinen avain -ominaisuudella voi olla vaikutusta asiakkaisiin, jotka käyttävät jo **Tilinumero**-saraketta mutta eivät yksilöllisiä tilikohtaisia **Tilinumero**-arvoja. Integrointiratkaisu ei tue tätä tapausta tällä hetkellä.

Jos **Tilinumero**-arvoa ei ole vielä luotu, kun uusi tili luodaan, se luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **ACC**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **ACC-01000-BVRCPS**

Kun Salesin integrointiratkaisua käytetään, päivityskomentosarja määrittää aiemmin Salesissa luotujen tilien **Tilinumero**-sarakkeen. Jos **Tilinumero**-arvoja ei ole, käytetään edellä mainittua numerosarjaa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- **CustomerGroupId**-yhdistämismääritys on päivitettävä Supply Chain Managementin kelvolliseksi arvoksi. Voit määrittää oletusarvon. Vaihtoehtoisesti voit määrittää arvon arvomäärityksellä.

    Oletusmallin arvo on **10**.

- Kun seuraavat yhdistämismääritykset lisätään, Supply Chain Managementissa tarvitaan vähemmän manuaalisia päivityksiä. Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.

    - **SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Supply Chain Managementissa. Oletustoimipaikka voidaan ottaa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.

        Oletusmallin arvo on **1**.

    - **WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Supply Chain Managementissa. Oletusvarasto voidaan ottaa Supply Chain Managementissa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.

        Oletusmallin arvo on **13**.

    - **LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa. Oletusarvoisesti käytetään asiakkaan tilausotsikon kieltä.

        Oletusmallin arvo on **fi-fi**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-sarakkeet eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden sarakkeiden määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä taulukko synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä. 

> [!NOTE]
> Yhdistämismääritys osoittaa, minkä sarakkeen tiedot synkronoidaan Salesista Supply Chain Managementiin.

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Liittyvät aiheet


[Prospektista käteiseksi](prospect-to-cash.md)

[Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin](accounts-template-mapping-direct.md)

[Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping-direct.md)

[Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä](sales-order-template-mapping-direct-two-ways.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin](sales-invoice-template-mapping-direct.md)

