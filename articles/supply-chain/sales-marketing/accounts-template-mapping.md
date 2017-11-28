---
title: Sales-tilien synkronointi Finance and Operationsin asiakkaille
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin tilit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Sales-tilien synkronointi Finance and Operationsin asiakkaille

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi. 

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin tilit (Sales) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations).

## <a name="template-and-task"></a>Malli ja tehtävä

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan tilit Salesista Finance and Operationsiin:

- **Mallin nimi:** tilit (Salesista Fin and Opsiin)
- **Projektin tehtävän nimi:** tilit – tili – asiakkaat

Ennen tilin tarvittavat tehtävät synkronoidaan / asiakkaan synkronoida: ei mitään

## <a name="entity-set"></a>Yksikköjoukko

| Myynti    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Tilit | Tili | Asiakkaat              |

## <a name="entity-flow"></a>Yksikön työnkulku

Summia hallitaan Salesissa ja synkronoidaan Finance and Operationsiin asiakkaina. Näiden asiakkaiden **On ulkoisesti ylläpidetty** -ominaisuuden arvoksi on määritetty **Kyllä**, jotta Salesista peräisin olevia asiakkaita voidaan jäljittää. Näitä tietoja käytetään suodattamaan Salesiin synkronoitavat laskut laskutuksen aikana.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Tilinumero**-kenttä on käytettävissä **Tili**-sivulla. Se on nyt luontainen ja yksilöllinen integrointia tukeva avain. Asiakkuudenhallinta- eli CRM-ratkaisun luonnollinen avain -ominaisuudella voi olla vaikutusta asiakkaisiin, jotka käyttävät jo **Tilinumero**-kenttää mutta eivät yksilöllisiä tilikohtaisia **Tilinumero**-arvoja. Integrointiratkaisu ei tue tätä tapausta tällä hetkellä.

Jos **Tilinumero**-arvoa ei ole vielä luotu, kun uusi tili luodaan, se luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **ACC**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **ACC-01000-BVRCPS**

Kun Salesin integrointiratkaisua käytetään, päivityskomentosarja määrittää aiemmin Salesissa luotujen tilien **Tilinumero**-kentän. Jos **Tilinumero**-arvoja ei ole, käytetään edellä kuvattua numerosarjaa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- **CustomerGroupId**-yhdistämismääritys **CDS &gt; Kohde** on päivitettävä Finance and Operationsin kelvolliseksi arvoksi. Voit määrittää oletusarvon. Vaihtoehtoisesti voit määrittää arvon arvomäärityksellä. Oletusmallin arvo on **10**.
- **Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä. Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.

    - Mallin **AddressCountryRegionISOCode** oletusarvo on **USA**.
    - Mallin **DeliveryAddressCountryRegionISOCode** oletusarvo on **USA**.

- Kun seuraavat yhdistämismääritykset lisätään kohdasta **CDS &gt; Kohde**, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä. Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.

    - **SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa. Oletustoimipaikka voidaan ottaa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta. Mallin **SiteId** oletusarvo on **1**.
    - **WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa. Oletusvarasto voidaan ottaa Finance and Operationsissa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta. Mallin **WarehouseId** oletusarvo on **13**.
    - **LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa. Oletusarvoisesti käytetään asiakkaan tilausotsikon kieltä. Mallin **LanguageId** oletusarvo on **en-us**.

- Päivitä CDS-organisaation tunnus (**Organization_OrganizationId**) **Lähde &gt; CDS** -yhdistämismäärityksessä. Oletusmallin arvo on **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien yhdistämistä varten on määritettävä arvomääritys. Arvomääritykset koskevat niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/accounts-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tilejä varten tietojen integrointiohjelmassa](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin](products-template-mapping.md)

[Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping.md)

[Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin](sales-quotation-template-mapping.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-order-template-mapping.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-invoice-template-mapping.md)




