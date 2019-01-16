---
title: Finance and Operationsin varastotasotietojen synkronointi Field Serviceen
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Finance and Operationsin varastotasotietojen synkronointi Field Serviceen 

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin käsillä olevat varastotasot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

**Mallin nimi Tietojen integroinnissa:**
- Tuotevarasto (Finance and Operationsista Field Serviceen)
  
**Tehtävien nimet tietojen integrointiprojektissa:**
- Tuotevarasto

Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:
- Varastot (Finance and Operationsista Field Serviceen) 
- Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin) 

## <a name="entity-set"></a>Yksikköjoukko

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Käytettävissä oleva CDS-varasto varaston mukaan     |

## <a name="entity-flow"></a>Yksikön työnkulku
Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen- Varastotasotietoja ovat seuraavat: 
- Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)
- Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä eli myyntitilaukset)
- Tilattu määrä (tilattu kirjattu kokonaismäärä eli ostotilaukset)

Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.

Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Finance and Operationsin tasoja.

Finance and Operations toimii päävarastotasona. Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicestä Finance and Operationsiin määritetään, jos tätä toimintoa käytetään Field Servicessä yhdessä Finance and Operationsin varastotasojen kanssa.

Jos tuotteiden ja varastojen varastotasoja hallitaan Finance and Operationsista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).

Huomautus: Field Servicessä voi luoda useita varastoja (kun On ulkoisesti ylläpidetty = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista. Lisätietoja on kohdissa Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin ja Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Ulkoinen tuotevarasto -yksikkö on uusi yksikkö, jota käytetään integroinnissa vain taustatoiminnossa. Se vastaanottaa integroinnissa varastotasoarvot Finance and Operationsista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa. 

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="in-the-data-integration-project"></a>Tietojen integrointiprojektissa
Voit määrittää kyselyn ja suodatuksen lisäasetusten suodattimilla, että vain valitut tuotteet ja varastot lähettävät varastotasotietoja Finance and Operationsista Field Serviceen.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Tuotevarasto (Finance and Operationsista Field Serviceen): tuotevarasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

