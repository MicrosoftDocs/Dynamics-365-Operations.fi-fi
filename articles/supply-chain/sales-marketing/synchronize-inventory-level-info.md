---
title: Finance and Operationsin varastotasotietojen synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535695"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Finance and Operationsin varastotasotietojen synkronointi Field Serviceen 

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin käsillä olevat varastotasot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.

**Tietojen integroinnin malli**
- Tuotevarasto (Fin and Opsista Field Serviceen)
  
**Tietojen integrointiprojektin tehtävä**
- Tuotevarasto

Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:
- Varastot (Fin and Opsista Field Serviceen) 
- Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Salesiin) 

## <a name="entity-set"></a>Yksikköjoukko

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Käytettävissä oleva CDS-varasto varaston mukaan     |

## <a name="entity-flow"></a>Yksikön työnkulku
Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen. Varastotasotietoja ovat seuraavat: 
- Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)
- Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä, kuten myyntitilaukset)
- Tilattu määrä (tilattu kirjattu kokonaismäärä, kuten ostotilaukset)

Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.

Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Finance and Operationsin tasoja.

Finance and Operations toimii päävarastotasona. Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicestä Finance and Operationsiin määritetään, jos tätä toimintoa käytetään Field Servicessä yhdessä Finance and Operationsin varastotasojen kanssa.

Jos tuotteiden ja varastojen varastotasoja hallitaan Finance and Operationsista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).

> [!NOTE]
> Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti = Ei**) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista. Lisätietoja on kohdissa [Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Uutta **Ulkoinen tuotevarasto** -yksikköä käytetään integroinnissa vain taustatoiminnossa. Tämä entiteetti vastaanottaa integroinnissa varastotasoarvot Finance and Operationsista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="data-integration"></a>Tietojen integrointi
Jotta projekti toimisi, on varmistettava, että integrointiavain päivitetään msdynce_externalproductinventories-mallia varten.
1.  Siirry **Tietojen integrointi > Yhteysjoukot**.
2.  Valitse käytetty yhteysjoukko.
3.  Varmista, että **Integroinnin avain** -välilehdessä seuraavat avaimet lisätään msdynce_externalproductinventories:
      - msdynce_productnumber (Product Number)
      - msdynce_warehouseid (Warehouse ID)
      
### <a name="data-integration-project"></a>Tietojen integrointiprojekti
Voit käyttää kyselyn ja suodatuksen lisäasetusten suodattimia siten, että vain tietyt tuotteet ja varastot lähettävät varastotasotietoja Finance and Operationsista Field Serviceen.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Tuotevarasto (Fin and Opsista Field Serviceen): tuotevarasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
