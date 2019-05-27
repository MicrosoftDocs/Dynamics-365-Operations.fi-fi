---
title: Field Servicen varastosiirtojen ja oikaisujen synkronointi Finance and Operationsiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: e94fa87c2f8b66574d6c5b2930cebf2e1b144fea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536293"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varaston oikaisut ja siirrot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Field Servicen varaston oikaisut ja siirrot Microsoft Dynamics 365 for Finance and Operationsiin.

**Tietojen integroinnin mallit**
- Varaston oikaisu (Field Servicestä Fin and Opsiin)
- Varastonsiirrot (Field Servicestä Fin and Opsiin)

**Tietojen integrointiprojektien tehtävät**
- Varasto-oikaisut
- Varastosiirrot

## <a name="entity-set"></a>Yksikköjoukko
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS-varasto-oikaisujen kirjauskansioiden otsikot ja rivit |
| msdyn_inventoryadjustmentproducts | CDS-varastosiirtojen kirjauskansioiden otsikot ja rivit   |

## <a name="entity-flow"></a>Yksikön työnkulku
Field Servicessä tehdyt varasto-oikaisut ja -siirrot synkronoidaan Finance and Operationsiin, kun **kirjauksen tilana** on **Kirjattu** eikä **Luotu**. Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena. Tämän vuoksi Finance and Operationsiin voidaan kirjata oikaisuja ja siirtoja mutta niitä ei voi muokata. Voit määrittää Finance and Operationsissa erätyön, joka kirjaa automaattisesti integraation aikana luodut oikaisujen ja siirron varastokirjauskansiot. Seuraavissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu 
**Varastoyksikkö**-kenttä on lisätty **Tuote**-yksikköön. Tämä kenttä on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Finance and Operationsissa ja Finance and Operationsin varaston varastoa varten tarvitaan varastoyksikkö.
Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan varastotuotteen arvosta. Jos arvo löydetään, **Yksikkö**-kenttä lukitaan varasto-oikaisutuotteessa.

**Kirjaa tila** -kenttä on lisätty sekä **Varasto-oikaisu**- että **Varastosiirto**-yksikköihin. Tätä kenttää voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Finance and Operationsiin. Tämän kentän oletusarvo on Luotu (1), mutta sitä ei kuitenkaan lähetetty Finance and Operationsiin. Kun arvoksi päivitetään Kirjattu (2), se lähetetään Finance and Operationsiin, mutta tämän jälkeen oikaisua tai siirtoa ei voi kuitenkaan voi enää muuttaa eikä uusia rivejä lisätä.

**Numerosarja**-kenttä on lisätty **Varasto-oikaisutuote**-yksikköön. Tämä kenttä varmistaa, että integraatiolla on yksilöivä numero, jotta integraatio voi luoda ja päivittää oikaisun. Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen **automaattisen P2C-numeroinnin** yksikön ylläpitämään numerosarjaa ja käytettyä etuliitettä.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="finance-and-operations"></a>Finance and Operations
Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla. Se tehdään valitsemalla **Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > CDS-integrointi > Kirjaa integroinnin varastokirjauskansiot**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Varasto-oikaisu (Field Servicestä Fin and Opsiin): varasto-oikaisu

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Varastosiirto (Field Servicestä Fin and Opsiin): varastosiirto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSTrans1.png)](./media/FSTrans1.png)
