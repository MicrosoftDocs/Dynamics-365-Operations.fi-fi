---
title: Varastosiirtojen ja -oikaisujen synkronointi Field Servicesta Supply Chain Managementiin
description: Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varaston oikaisut ja siirrot synkronoidaan Dynamics 365 Field Serviceen.
author: Henrikan
ms.date: 04/30/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: e59e50a4f54bac749b3d860404a3ecd444d99a89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854091"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Varastosiirtojen ja -oikaisujen synkronointi Field Servicesta Supply Chain Managementiin

[!include[banner](../includes/banner.md)]



Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varaston oikaisut ja siirrot synkronoidaan Dynamics 365 Field Serviceen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa varasto-oikaisuja ja -siirtoja Field Servicesta Supply Chain Managementiin.

**Tietojen integroinnin mallit**
- Varasto-oikaisu (Field Servicesta Supply Chain Managementiin)
- Varastosiirrot (Field Servicesta Supply Chain Managementiin)

**Tietojen integrointiprojektien tehtävät**
- Varasto-oikaisut
- Varastosiirrot

## <a name="table-set"></a>Taulujoukko
| Field Service                     | Toimitusketjun hallinta                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Dataversen varasto-oikaisujen kirjauskansioiden otsikot ja rivit |
| msdyn_inventoryadjustmentproducts | Dataversen varastosiirtojen kirjauskansioiden otsikot ja rivit   |

## <a name="table-flow"></a>Taulutyönkulku
Field Servicessa tehdyt varasto-oikaisut ja -siirrot synkronoidaan Supply Chain Managementiin, kun **Kirjauksen tila** muuttuu **Kirjattu**-tilasta **Luotu**-tilaan. Kun näin tapahtuu, oikaisu- tai siirtotilaus lukitaan vain luku -muotoisena. Tämän vuoksi Supply Chain Managementiin voidaan kirjata oikaisuja ja siirtoja, mutta niitä ei voi muokata. Voit määrittää Supply Chain Managementissa erätyön, joka kirjaa automaattisesti integraation aikana luodut oikaisujen ja siirtojen varastokirjauskansiot. Seuraavissa edellytyksissä on lisätietoja erätyön käyttöönottamisesta.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu 
**Varastoyksikkö**-sarake on lisätty **Tuote**-tauluun. Tämä sarake on välttämätön, sillä myynti- ja varastoyksikkö ei ole aina sama Supply Chain Managementissa, ja Supply Chain Managementin varaston varastoa varten tarvitaan varastoyksikkö.
Kun tuote määritetään varasto-oikaisutuotteessa sekä varasto-oikaisuille että varastosiirroille, yksikkö noudetaan varastotuotteen arvosta. Jos arvo löydetään, **Yksikkö**-sarake lukitaan varasto-oikaisutuotteessa.

**Kirjaa tila** -sarake on lisätty sekä **Varasto-oikaisu**- että **Varastosiirto**-tauluun. Tätä saraketta voi käyttää suodattimena, kun oikaisu tai siirto lähetetään Supply Chain Managementiin. Tämän sarakkeen oletusarvo on Luotu (1), mutta sitä ei kuitenkaan lähetetä Supply Chain Managementiin. Kun arvoksi päivitetään Kirjattu (2), se lähetetään Supply Chain Managementiin, mutta tämän jälkeen oikaisua tai siirtoa ei voi kuitenkaan voi enää muuttaa eikä uusia rivejä lisätä.

**Numerosarja**-sarake on lisätty **Varasto-oikaisutuote**-tauluun. Tämä sarake varmistaa, että integraatiolla on yksilöivä numero, jotta integraatio voi luoda ja päivittää oikaisun. Kun luot ensimmäisen varasto-oikaisutuotteen, se luo uuden tietueen **automaattisen P2C-numeroinnin** -taulussa ylläpitämään numerosarjaa ja käytettyä etuliitettä.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="supply-chain-management"></a>Toimitusketjun hallinta
Integraation luomat integroinnin varastokirjauskansiot voidaan kirjata automaattisesti erätyön avulla. Se tehdään valitsemalla **Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Dataverse-integrointi > Kirjaa integroinnin varastokirjauskansiot**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Varasto-oikaisu (Field Servicesta Supply Chain Managementiin): Varasto-oikaisu

[![Varaston oikaisun integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): varaston oikaisu.](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Varastosiirto (Field Servicesta Supply Chain Managementiin): Varastosiirto

[![Varaston siirron integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): varaston siirto.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]