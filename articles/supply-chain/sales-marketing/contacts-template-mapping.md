---
title: "Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin"
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin yhteyshenkilöt (yhteyshenkilöt) ja yhteyshenkilöt (asiakkaat) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi. 

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin (Sales) Yhteyshenkilö (yhteyshenkilöt) -yksiköt ja yhteyshenkilöt (asiakkaat) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations).

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin yhteyshenkilö (yhteyshenkilöt) Finance and Operationsin yhteyshenkilöön (asiakkaat):

- **Mallien nimi:**

    - Yhteyshenkilöt (Salesista Fin and Opsiin)
    - Yhteyshenkilöstä asiakkaaseen (Salesista Fin and Opsiin)

- **Projektin tehtävien nimet:**

    - Yhteyshenkilöt
    - Yhteyshenkilö asiakkaaseen

Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Fin and Opsiin)

## <a name="entity-sets"></a>Yksikköjoukot

| Myynti    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Yhteyshenkilöt | Kontakti | CDS-yhteyshenkilöt           |
| Yhteyshenkilöt | Tili | Asiakkaat V2           |

## <a name="entity-flow"></a>Yksikön työnkulku

Yhteyshenkilöitä hallitaan Salesissa ja ne synkronoidaan Common Data Serviceen (CDS) ja Finance and Operationsiin.

Salesin yhteyshenkilöstä voi tulla CDS:n ja Finance and Operationsin yhteyshenkilö. Vaihtoehtoisesti siitä voi olla CDS:n tili ja Finance and Operationsin asiakas. Järjestelmä määrittää seuraavien Salesin yhteyshenkilöiden ominaisuuksien perusteella, poimitaanko yhteyshenkilö Salesista CDS:ään ja Finance and Operationsiin synkronoitavaksi (kuten Yhteyshenkilöt Salesissa &gt; Yhteyshenkilö CDS:ssä &gt; Yhteyshenkilöt Finance and Operationsissa):

- **Synkronoi tili CDS:ssä ja asiakas Finance and Operationsissa:** yhteyshenkilöt, kun **On aktiivinen asiakas** -asetuksena on **Kyllä**
- **Synkronoi yhteyshenkilö CDS:ssä ja yhteyshenkilö Finance and Operationsissa:** Yhteyshenkilöt, kun **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai asiakas) viittaa tiliin (eikä yhteyshenkilöön)

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi 

Uusi **On aktiivinen asiakas** -kenttä on lisätty yhteyshenkilöön. Tämän kentän avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole. **On aktiivinen asiakas** -asetuksena on **Kyllä** vain asiakkaille, joilla on liittyviä tarjouksia, tilauksia tai laskuja. Vain nämä yhteyshenkilöt synkronoidaan Finance and Operationsiin asiakkaina.

Uusi **IsCompanyAnAccount**-kenttä on lisätty yhteyshenkilöön. Tämä kenttä osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö). Näillä tiedoilla tunnistetaan yhteystiedot, jotka on synkronoitava Finance and Operationsiin yhteyshenkilöinä.

Uusi **Yhteyshenkilön numero** -kenttä on lisätty yhteyshenkilöön takaamaan integroinnin luonnollinen ja yksilöllinen avain. Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **CON-01000-BVRCPS**

Kun Salesin integrointiratkaisu lisätään Salesiin, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -kentän käyttämällä edellä mainittua numerosarjaa. Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -kentän arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.

## <a name="in-finance-and-operations"></a>Finance and Operationsissa 

Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella. Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti. Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="contact-to-contact"></a>Yhteyshenkilöstä yhteyshenkilöön

- Päivitä **CDS-organisaation tunnus** **Lähde &gt; CDS** -yhdistämismääritykseksi.

    - Mallin **Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.
    - Mallin **PrimaryAccount_Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.

- **Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Operations** -yhdistämismäärityksessä. Oletusarvo käytetään, jos kenttä on tyhjä Salesissa. Mallin **PrimaryAddressCountryRegionISOCode** oletusarvo on **USA**.
- Varmista, että seuraavassa Finance and Operationsin kentässä on arvo. Jos tietoja ei tarvita Finance and Operationsissa, voit poistaa yhdistämismäärityksen **CDS &gt; Kohde** -määrityksestä.

    - **Finance and Operationsin kentän nimi:** päätös
    - **Yhdistämismääritys:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

- Päivitä **CDS-organisaation tunnus** **Lähde &gt; CDS** -yhdistämismääritykseksi. Mallin **Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.
- **Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä. Oletusarvo käytetään, jos kenttä on tyhjä Salesissa. Mallin **PrimaryAddressCountryRegionISOCode** oletusarvo on **USA**.
- **CustomerGroup** tarvitaan Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä. Oletusarvo käytetään, jos kenttä on tyhjä Salesissa. Mallin **CustomerGroupId** oletusarvo on **10**.
- Kun seuraavat yhdistämismääritykset lisätään kohdasta **CDS &gt; Kohde**, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä. Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.

    - **SiteId** – oletustoimipaikka voidaan määrittää myös Finance and Operationsin tuotteissa. Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa. Mallin **SiteId** arvoa ei ole määritetty.
    - **WarehouseId** – oletusvarasto voidaan määrittää myös Finance and Operationsin tuotteissa. Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa. Mallin **WarehouseId** arvoa ei ole määritetty.
    - **LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa. Mallin **LanguageId** oletusarvo on **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

### <a name="contact-to-contact"></a>Yhteyshenkilöstä yhteyshenkilöön

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen yhteyshenkilöitä varten tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Yhteishenkilöstä asiakkaaseen

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen yhteyshenkilöitä varten tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Liittyvät aiheet

[Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin](products-template-mapping.md)

[Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin](accounts-template-mapping.md)

[Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin](sales-quotation-template-mapping.md)

[Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-order-template-mapping.md)

[Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin](sales-invoice-template-mapping.md)

