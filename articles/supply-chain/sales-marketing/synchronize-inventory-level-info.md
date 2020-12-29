---
title: Varastotasotietojen synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varastotasotiedot synkronoidaan Dynamics 365 Field Serviceen.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426956"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Varastotasotietojen synkronointi Supply Chain Managementista Field Serviceen 

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varastotasotiedot synkronoidaan Dynamics 365 Field Serviceen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa käsillä olevia varastotasoja Supply Chain Managementista Field Serviceen.

**Tietojen integroinnin malli**
- Tuotevarasto (Supply Chain Managementista Field Serviceen)
  
**Tietojen integrointiprojektin tehtävä**
- Tuotevarasto

Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:
- Varastot (Supply Chain Managementista Field Serviceen) 
- Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin) 

## <a name="entity-set"></a>Yksikköjoukko

| Field Service                      | Toimitusketjun hallinta                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Käytettävissä oleva CDS-varasto varaston mukaan     |

## <a name="entity-flow"></a>Yksikön työnkulku
Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen. Varastotasotietoja ovat seuraavat: 
- Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)
- Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä, kuten myyntitilaukset)
- Tilattu määrä (tilattu kirjattu kokonaismäärä, kuten ostotilaukset)

Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.

Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Supply Chain Managementin tasoja.

Supply Chain Management toimii päävarastotasona. Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicesta Supply Chain Managementiin määritetään, jos tätä toimintoa käytetään Field Servicessa yhdessä Supply Chain Managementin varastotasojen synkronoinnin kanssa.

Jos tuotteiden ja varastojen varastotasoja hallitaan Supply Chain Managementista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).

> [!NOTE]
> Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti = Ei**) ja ne voi sitten yhdistää yhteen varastoon Supply Chain Managementissa kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicella halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Supply Chain Managementiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Supply Chain Managementista. Lisätietoja on kohdissa [Varasto-oikaisujen synkronointi Field Servicesta Supply Chain Managementiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin linkitettyihin myyntitilauksiin Supply Chain Managementissa](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Uutta **Ulkoinen tuotevarasto** -yksikköä käytetään integroinnissa vain taustatoiminnossa. Tämä entiteetti vastaanottaa integroinnissa varastotasoarvot Supply Chain Managementista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="data-integration"></a>Tietojen integrointi
Jotta projekti toimisi, on varmistettava, että integrointiavain päivitetään msdynce_externalproductinventories-mallia varten.
1.  Siirry **Tietojen integrointi > Yhteysjoukot**.
2.  Valitse käytetty yhteysjoukko.
3.  Varmista, että **Integroinnin avain** -välilehdessä seuraavat avaimet lisätään msdynce_externalproductinventories:
      - msdynce_productnumber (Product Number)
      - msdynce_warehouseid (Warehouse ID)
      
### <a name="data-integration-project"></a>Tietojen integrointiprojekti
Voit käyttää kyselyn ja suodatuksen lisäasetusten suodattimia siten, että vain tietyt tuotteet ja varastot lähettävät varastotasotietoja Supply Chain Managementista Field Serviceen.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Tuotevarasto (Supply Chain Managementista Field Serviceen): Tuotevarasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
