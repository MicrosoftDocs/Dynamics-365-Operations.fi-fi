---
title: Field Servicen varastosiirtojen ja oikaisujen synkronointi Finance and Operationsiin
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Field Servicen varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin.

**Mallien nimet tietojen integroinnissa:**
- Varasto-oikaisu (Field Servicestä Finance and Operationsiin)
- Varastosiirrot (Field Servicestä Finance and Operationsiin)

**Tehtävien nimet tietojen integrointiprojekteissa:**
- Varasto-oikaisut
- Varastosiirrot

## <a name="entity-set"></a>Yksikköjoukko
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-varasto-oikaisujen kirjauskansioiden otsikot ja rivit |
| msdyn_inventoryadjustmentproducts | CDS-varastosiirtojen kirjauskansioiden otsikot ja rivit   |

## <a name="entity-flow"></a>Yksikön työnkulku
Field Servicessä tehdyt varasto-oikaisut ja -siirrot synkronoidaan Finance and Operationsiin, kun **kirjauksen tilana** Kirjattu eikä Luotu. Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena, sillä Finance and Operationsiin voidaan kirjata oikaisuja ja siirtoja eikä sitä voi sen vuoksi muokata.
Voit määrittää Finance and Operationsissa erätyön, joka kirjaa automaattisesti integraatiolla luodut oikaisujen ja siirron varastokirjauskansiot. Alla olevissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu 
Varastoyksikkö-kenttä on lisätty tuoteyksikköön. Tämä kenttä on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Operationsissa, Operationsin varaston varastoa varten tarvitaan varastoyksikkö.
Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan tuotteiden varastotuotteen arvosta. Jos arvo löydetään, Yksikkö-kenttä lukitaan varasto-oikaisutuotteessa.

Kirjaa tila -kenttä on lisätty sekä Varasto-oikaisu- että Varastosiirto-yksikköihin. Tätä kenttää voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Operationsiin. Kentän oletusarvona on Luotu (1), jolloin sitä ei lähetetä Operationsiin. Kentät, joiden arvoksi on vaihdettu Kirjattu (2), lähetetään Operationsiin. Tämän jälkeen mitään ei kuitenkaan voi enää muuttaa Oikaisu- tai Siirto-kohdassa eikä siihen voi lisätä uusia rivejä.
Numerosarja-kenttä on lisätty varasto-oikaisutuotteen yksikköön. Tämän kentän avulla integraatio saa yksilöivän numeron, joten integraatio tietää, milloin tehdään luonteja ja milloin päivityksiä. Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen automaattisen P2C-numeroinnin yksikön ylläpitämään numerosarjaa ja käytettyä etuliitettä.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="in-finance-and-operations"></a>Finance and Operationsissa
Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla. Se tehdään valitsemalla: Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > CDS-integrointi > Kirjaa integroinnin varastokirjauskansiot

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Varasto-oikaisu (Field Servicestä Finance and Operationsiin): varasto-oikaisu

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Varastosiirto (Field Servicestä Finance and Operationsiin): varastosiirto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSTrans1.png)](./media/FSTrans1.png)

