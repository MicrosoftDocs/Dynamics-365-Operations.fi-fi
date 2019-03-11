---
title: Projektisopimusten ja projektien synkronointi Project Service Automationista suoraan Finance and Operationsiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektisopimuksia ja projekteja synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "312114"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projektisopimusten ja projektien synkronointi Project Service Automationista suoraan Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektisopimuksia ja projekteja synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin.

> [!NOTE] 
> Jos käytät Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin versiota 7.3.0, sinun on asennettava KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tiedonkulku Project Service Automationista Finance and Operationsiin

> [!NOTE]
> Ennen Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisun käyttöä on tutustuttava Microsoft Dynamics 365:n tietojen integrointiominaisuuteen.

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuuteen sisältyvä integrointimalli mahdollistaa projektisopimuksia, projekteja, projektisopimuksen rivejä ja projektisopimuksen rivien välitavoitteita koskevien tietojen siirtymisen Project Service Automationista Finance and Operationsiin.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektisopimukset ja projektit Project Service Automationista Finance and Operationsiin:

- **Mallin nimi tietojen integroinnissa:** Projektit ja sopimukset (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Projektisopimukset PSA:sta Fin and Opsiin
    - Projektit PSA:sta Fin and Opsiin
    - Projektisopimuksen rivit PSA:sta Fin and Opsiin
    - Projektisopimuksen rivien välitavoitteet PSA:sta Fin and Opsiin

Tilit on synkronoitava, ennen kuin projektit ja projektisopimukset voidaan synkronoida.

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Tilaukset                           | Projektin sopimuksen integrointiyksikkö                |
| Projektit                         | Projektin integrointiyksikkö                         |
| Tilausrivit                      | Projektin sopimusrivin integrointiyksikkö           |
| Projektin sopimusrivien välitavoitteet | Projektin sopimusrivin välitavoitteen integrointiyksikkö |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektisopimuksia hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektisopimuksina. Voit määrittää integrointimallissa projektisopimuksen integrointilähteen Finance and Operationsissa.

Aikaan, materiaaliprojektiin ja kiinteään hintaan perustuvia projekteja hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projekteina. Voit määrittää integrointimallissa projektin integrointilähteen Finance and Operationsissa.

Projektisopimuksen rivejä hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektisopimuksen laskutussääntöinä. Synkronointi päivittää sopimusrivin projektin ja projektiryhmän projektityypin, jos laskutustapa on jokin muu kuin oletusprojektityyppi.

Projektisopimuksen rivien välitavoitteita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektisopimuksen laskutussäännön välitavoitteina.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automationiin ja Finance and Operationsin välinen integrointiratkaisu

**Projektisopimuksen tunnus** -kenttää voi käyttää **Projektisopimukset**-sivulla. Kenttä on nyt luontainen ja yksilöllinen avain, joka tukee integrointia.

Jos **Projektisopimuksen tunnus**-arvoa ei ole vielä luotu, kun uusi projektisopimus luodaan, se luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **ORD**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **ORD-01022-Z4M9Q0**.

**Projektinumero**-kenttä on käytettävissä **Projektit**-sivulla. Kenttä on nyt luontainen ja yksilöllinen avain, joka tukee integrointia.

Jos **Projektinumero**-arvoa ei ole vielä luotu, kun uusi projekti luodaan, se luodaan automaattisesti numerosarjan avulla. Arvossa on ensimmäisenä **PRJ**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite. Esimerkki: **PRJ-01049-CCNID0**.

Kun Project Service Automationin ja Finance and Operationsin välistä integrointiratkaisua käytetään<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, päivityskomentosarja määrittää **Projektisopimuksen tunnus** -kentän arvoiksi aiemmin luodut projektisopimukset ja **Projektinumero**-kentän arvoksi aiemmin Project Service Automationissa luodut projektit.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

- Tilit on synkronoitava, ennen kuin projektit ja projektisopimukset voidaan synkronoida.
- Lisää yhteysjoukossa kohteen **msdyn\_organizationalunits** integraatioavainkentään määritykseksi **msdyn\_name \[Name\]**. Projekti on ehkä lisättävä ensin yhteysjoukkoon. Lisätietoja on kohdassa [Tietojen integrointi Common Data Service for Apps -ratkaisuun](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Lisää yhteysjoukossa kohteen **msdyn\_projects** integraatioavainkentään määritykseksi **msdynce\_projectnumber \[Project Number\]**. Projekti on ehkä lisättävä ensin yhteysjoukkoon. Lisätietoja on kohdassa [Tietojen integrointi Common Data Service for Apps -ratkaisuun](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Projektisopimusten ja projektien **SourceDataID**-arvoksi voidaan määrittää jokin muu arvo. Se voidaan myös poistaa yhdistämismäärityksestä. Mallin oletusarvo on **Project Service Automation**.
- **PaymentTerms**-määritys on päivitettävä vastaamaan kelvollisia Finance and Operationsin maksuehtoja. Voit myös poistaa projektitehtävän yhdistämismäärityksestä. Oletusarvon määritys sisältää esittelytietojen oletusarvot. Seuraava taulukko sisältää Project Service Automationin arvot.

    | Arvo | kuvaus   |
    |-------|---------------|
    | 1     | Netto 30        |
    | 2     | 2 % 10, netto 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Power Query

Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Query for Exceliä:

- Microsoft Dynamics 365 for Salesissa on myyntitilauksia.
- Project Service Automationissa on useita organisaatioyksiköitä, jotka yhdistetään useisiin Finance and Operationsin yrityksiin.

Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:

- Projektisopimukset (PSA:sta Fin and Opsiin) -mallissa on oletussuodatin, joka sisältää vain **Työnimike (msdyn\_ordertype = 192350001)** -tyypin myyntitilaukset. Tämä suodatin auttaa takaamaan, että myyntitilauksille ei luoda myyntitilauksia Finance and Operationsissa. Jos luot oman mallin, tämä suodatin on lisättävä.
- Sinun on luotava Power Query -suodatin, joka sisältää vain integroinnin yhteysjoukon yritykseen synkronoitavat sopimusorganisaatiot. Esimerkiksi projektisopimukset, joita on tehty sopimuksen Contoso US:n organisaatioyksikön kanssa, on synkronoitava USSI-yritykseen, kun sen sijaan projektisopimukset, jotka on tehty Contoso Globalin sopimuksen organisaatioyksikön kanssa, on synkronoitava USMF-yritykseen. Jos et lisää tätä suodatinta tehtävän yhdistämiseen, kaikki projektisopimukset synkronoidaan yhteysjoukossa määritettyyn yritykseen sopimuksen organisaatioyksiköstä riippumatta.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

> [!NOTE] 
> **CustomerReference**-, **AddressCity**-, **AddressCountryRegionID**-, **AddressDescription**-, **AddressLine1-**, **AddressLine2**-, **AddressState**- ja **AddressZipCode**-kentät eivät sisälly projektisopimusten oletusyhdistämiseen Voit lisätä yhdistämismääritykset, jos nämä projektisopimusten tiedot on synkronoitava.
>
> **Description**-, **ParentID**-, **ProjectGroup**-, **ProjectManagerPersonnelNumber**- ja **ProjectType**-kentät eivät sisälly projektien oletusyhdistämismääritykseen. Voit lisätä yhdistämismääritykset, jos nämä projektien tiedot on synkronoitava.

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mallin yhdistäminen](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mallin yhdistäminen](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mallin yhdistäminen](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
