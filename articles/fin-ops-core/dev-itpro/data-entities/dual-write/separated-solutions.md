---
title: Erillinen kaksoiskirjoitussovelluksen hallintapaketti
description: Kaksoiskirjoitussovelluksen hallintapaketti ei ole enää yksittäinen paketti, mutta se on jaettu pienempiin paketteihin. Tässä aiheessa kerrotaan kunkin paketin sisältämät ratkaisut ja määritykset sekä sen riippuvuus muista paketeista.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924867"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Erillinen kaksoiskirjoitussovelluksen hallintapaketti

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aiemmin kaksoiskirjoitussovelluksen hallintapaketti oli vain yksi paketti, joka sisälsi seuraavat ratkaisut:

- Dynamics 365 Notes
- Dynamics 365 Finance and Operations Common Anchor
- Dynamics 365 Finance and Operations Dual Write Entity Maps
- Dynamics 365 resurssien hallintasovellus
- Dynamics 365 resurssien hallinta
- HCM, yhteinen
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Common
- Dynamics 365 Company
- Currency Exchange Rates
- Field Service Common

Koska paketti oli yksittäinen paketti, se loi asiakkaille "kaikki tai ei mitään" -tilanteen. Microsoft on kuitenkin nyt jakanut sen pienempiin paketteihin. Siksi asiakas voi valita vain ne paketit, joiden ratkaisuja tarvitsee. Jos olet esimerkiksi Microsoft Dynamics 365 Supply Chain Management -asiakas etkä tarvitse integrointia Dynamics 365 Human Resourcesin, huomautusten tai omaisuudenhallinna kanssa, voit sulkea nämä ratkaisut pois asennetuista ratkaisuista. Koska pohjana olevat ratkaisun nimet, julkaisija- ja määritysversiot säilyvät samana, tämä muutos ei riko ratkaisuja. Aiemmin luodut asennukset päivitetään.

![Erillinen paketti.](media/separated-package-1.png)

Tässä aiheessa kerrotaan kunkin paketin sisältämät ratkaisut ja määritykset sekä sen riippuvuus muista paketeista.

## <a name="dual-write-application-core"></a>Kaksoiskirjoituksen sovellusydin

Kaksoiskirjoituksen sovellusydinpaketin avulla käyttäjät voivat asentaa ja konfiguroida kaksoiskirjoituksen ilman customer engagement -sovellusta. Se sisältää seuraavat viisi ratkaisua.

| Yksilöivä nimi                           | Näyttönimi                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | Currency Exchange Rates                    |
| msdyn_DualWriteAppCoreMaps            | Kaksoiskirjoituksen sovellusytimen entiteettien yhdistämismääritykset   |
| msdyn_DualWriteAppCoreAnchor          | Kaksoiskirjoituksen sovellusytimen ankkuri        |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations -sovellukset     | Asiakkaiden aktivointisovellukset                    |
|---------------------------------|---------------------------------------------|
| Toimintayksikkö                  | msdyn_internalorganizations                 |
| Organisaatiohierarkia          | msdyn_internalorganizationhierarchies       |
| Oikeushenkilöt                  | msdyn_internalorganizations                 |
| Oikeushenkilöt                  | cdm_companies                               |
| Organisaatiohierarkian tarkoitukset | msdyn_internalorganizationhierarchypurposes |
| Vaihtokurssivaluuttapari     | msdyn_currencyexchangeratepairs             |
| Nimen jälkiliitteet                    | msdyn_nameaffixes                           |
| Vaihtokurssin tyyppi              | msdyn_exchangeratetypes                     |
| CDS-vaihtokurssit              | msdyn_currencyexchangerates                 |
| Organisaatiohierarkian tyyppi     | msdyn_internalorganizationhierarchytypes    |
| Valuutat                      | transactioncurrencies                       |
| Yhdistetyn todellisuuden oppaiden yksikkö     | msmrw_guides                                |

**Riippuvuustiedot**

Kaksoiskirjoituksen sovellusytimen paketilla ei ole riippuvuussuhdetta muihin paketteihin.

## <a name="dual-write-human-resources"></a>Human Resourcesin kaksoiskirjoitus

Human Resourcesin kaksoiskirjoituspaketti sisältää Human Resources -tietojen synkronoinnissa tarvittavat ratkaisut ja yhdistämismääritykset. Se sisältää seuraavat kolme ratkaisua.

| Yksilöivä nimi                | Näyttönimi                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM, yhteinen                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources – entiteettien yhdistämismääritykset |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources -ankkuri      |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset         |
|-----------------------------|----------------------------------|
| Etniset alkuperät              | cdm_ethnicorigins                |
| Kompensaation työtehtävä   | cdm_jobfunctions                 |
| Toimet V2                | cdm_jobpositions                 |
| Työt                        | cdm_jobs                         |
| Kompensaation työn tyyppi       | cdm_jobtypes                     |
| Kielikoodit              | cdm_languages                    |
| Toimityyppi               | cdm_positiontypes                |
| Position työntekijämääritykset | cdm_positionworkerassignmentmaps |
| Sotaveteraanitila              | cdm_veteranstatuses              |
| Työntekijä                      | cdm_workers                      |
| Työsuhteita yritystä kohti      | cdm_employments                  |

**Riippuvuustiedot**

Human Resourcesin kaksoiskirjoituspaketti on riippuvainen kaksoiskirjoituksen sovellusytimen paketista. Sen vuoksi kaksoiskirjoituksen sovellusytimen paketti pitää asentaa, ennen kuin asennetaan Human Resourcesin kaksoiskirjoituspaketti.

## <a name="dual-write-supply-chain"></a>Toimitusketjun kaksoiskirjoitus

Toimitusketjun kaksoiskirjoituspaketti sisältää Supply Chain Management -tietojen synkronoinnissa tarvittavat ratkaisut ja yhdistämismääritykset. Se sisältää seuraavat kolme ratkaisua.

| Yksilöivä nimi                                | Näyttönimi                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Managementin laajennetut entiteettien yhdistämismääritykset |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Managementin laajennettu ankkuri      |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations -sovellukset                 | Asiakkaiden aktivointisovellukset                      |
|---------------------------------------------|-----------------------------------------------|
| Yksiköt                                       | uoms                                          |
| CDS-myyntitilauksien otsikot                     | salesorders                                   |
| CDS-myyntitilausrivit                       | salesorderdetails                             |
| CDS-myyntitarjouksen otsikko                  | tarjoukset                                        |
| CDS-myyntitarjousrivit                   | quotedetails                                  |
| CDS-vapautetut erilliset tuotteet              | tuotetta                                      |
| Varastovyöhykkeet                             | msdyn_warehousezones                          |
| Varastovyöhykeryhmät                       | msdyn_warehousezonegroups                     |
| Varaston työrivit                        | msdyn_warehouseworklines                      |
| Varaston työotsikot                      | msdyn_warehouseworkheaders                    |
| Varastot                                  | msdyn_warehouses                              |
| Varastokäytävä                             | msdyn_warehouseaisles                         |
| Yksikkömuunnokset                            | msdyn_unitofmeasureconversions                |
| Toimitusehdot                           | msdyn_termsofdeliveries                       |
| Toimitustavat                           | msdyn_shipvias                                |
| Päätuotteen tyylit                       | msdyn_sharedproductstyles                     |
| Myyntilaskun rivit V2                      | invoicedetails                                |
| Myyntilaskun otsikot V2                    | laskut                                      |
| Päätuotteen koot                        | msdyn_sharedproductsizes                      |
| Vapautetut tuotteet V2                        | msdyn_sharedproductdetails                    |
| Päätuotteen konfiguraatiot               | msdyn_sharedproductconfigurations             |
| Päätuotteen värit                       | msdyn_sharedproductcolors                     |
| Myyntitilausten alkuperän koodit                    | msdyn_salesorderorigins                       |
| Tuotteen vastaanoton otsikko                      | msdyn_purchaseorderreceipts                   |
| Tuotteen vastaanottorivi                        | msdyn_purchaseorderreceiptproducts            |
| Ostotilausotsikot V2                   | msdyn_purchaseorders                          |
| CDS-ostotilausrivin poistettavaksi merkitty yksikkö | msdyn_purchaseorderproducts                   |
| CDS-ostotilausrivin yksikkö              | msdyn_purchaseorderproducts                   |
| Seurantadimensioryhmät                   | msdyn_producttrackingdimensiongroups          |
| Tyylit                                      | msdyn_productstyles                           |
| Varastodimensioryhmät                    | msdyn_productstoragedimensiongroups           |
| Tuotekohtaiset yksikkömuunnokset           | msdyn_productspecificunitofmeasureconversions |
| Tuotteen oletustilausasetukset V2           | msdyn_productspecificdefaultordersettings     |
| Koot                                       | msdyn_productsizes                            |
| Tuotedimension ryhmät                    | msdyn_productdimensiongroups                  |
| Tilauksen oletusasetukset                      | msdyn_productdefaultordersettings             |
| Konfiguraatiot                              | msdyn_productconfigurations                   |
| Kaikki tuotteet                                | msdyn_globalproducts                          |
| Värit                                      | msdyn_productcolors                           |
| Tuoteluokkahierarkian roolit            | msdyn_productcategoryhierarchyroles           |
| Tuoteluokkahierarkiat                | msdyn_productcategoryhierarchies              |
| Tuoteluokan määritykset                | msdyn_productcategoryassignments              |
| Tuoteluokat                          | msdyn_productcategories                       |
| Varaston sijainnit                         | msdyn_inventorylocations                      |
| CDS-varasto                            | msdyn_inventoryonhandentries                  |
| Tuoteluokat                          | msdyn_productcategories                       |
| CDS-varasto                            | msdyn_inventoryonhandrequests                 |
| Tuotenumeron viivakoodi           | msdyn_productbarcodes                         |
| Kanta-asiakaskortti                                | msdyn_loyaltycards                            |
| Kanta-asiakkaan palkkiopisteet                       | msdyn_loyaltyrewardpoints                     |
| Hintaperusteiset asiakasryhmät                       | msdyn_pricecustomergroups                     |
| Toimipaikat                                       | msdyn_operationalsites                        |
| CDS-myyntitarjousrivit                   | quotedetails                                  |
| CDS-myyntitilausrivit                       | salesorderdetails                             |

**Riippuvuustiedot**

Toimitusketjun kaksoiskirjoituspaketti riippuu seuraavista kolmesta paketista. Nämä paketit on näin ollen asennettava ennen toimitusketjun kaksoiskirjoituspaketin asennusta.

- Kaksoiskirjoituksen sovellusydinpaketti
- Financen kaksoiskirjoituspaketti
- Human Resourcesin kaksoiskirjoituspaketti

## <a name="dual-write-finance"></a>Financen kaksoiskirjoitus

Financen kaksoiskirjoituspaketti sisältää Dynamics 365 Finance -tietojen synkronoinnissa tarvittavat ratkaisut ja yhdistämismääritykset. Se sisältää seuraavat neljä ratkaisua.

| Yksilöivä nimi                            | Näyttönimi                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance Extended – entiteettien yhdistämismääritykset |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance Extended – ankkuri      |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations -sovellukset             | Asiakkaiden aktivointisovellukset        |
|-----------------------------------------|---------------------------------|
| Ennakonpidätysryhmät                  | msdyn_withholdingtaxgroups      |
| CDS-yhteyshenkilöt V2 (asiakas)              | yhteyshenkilöt                        |
| CDS-yhteyshenkilöt V2 (toimittaja)                | yhteyshenkilöt                        |
| Asiakkaat V3                            | yhteyshenkilöt                        |
| Ennakonpidätyskoodit                   | msdyn_withholdingtaxcodes       |
| Toimittajat V2                              | msdyn_vendors                   |
| Toimittajan maksutapa                   | msdyn_vendorpaymentmethods      |
| Toimittajaryhmät                           | msdyn_vendorgroups              |
| Tilikartta                       | msdyn_chartofaccountses         |
| Arvonlisäveron kirjanpidon kirjausryhmät V2      | msdyn_taxpostinggroups          |
| Nimikkeen arvonlisäveroryhmä                    | msdyn_taxitemgroups             |
| Arvonlisäveroryhmät                        | msdyn_taxgroups                 |
| Arvonlisäveron verovapauskoodin yksikkö CDS:lle        | msdyn_taxexemptcodes            |
| Asiakasryhmät                         | msdyn_customergroups            |
| Asiakkaan maksutapa                 | msdyn_customerpaymentmethods    |
| Taloushallinnon dimensiot                    | msdyn_dimensionattributes       |
| Alv-viranomaiset                   | msdyn_taxauthorities            |
| Taloushallinnon dimensiomuoto              | msdyn_financialdimensionformats |
| Kirjanpidon vuosikalenterin kausi                  | msdyn_fiscalcalendarperiods     |
| Kirjanpidon vuosikalenterin integraation yksikkö      | msdyn_fiscalcalendars           |
| Kirjanpidon kalenterivuoden integraation yksikkö | msdyn_fiscalcalendaryears       |
| Maksuehdot                        | msdyn_paymentterms              |
| Maksuaikataulu                        | msdyn_paymentschedules          |
| Maksusuunnitelmarivit                  | msdyn_paymentschedulelines      |
| CDS-maksupäivät                        | msdyn_paymentdays               |
| CDS V2 -maksupäivärivit                | msdyn_paymentdaylines           |
| Päätili                            | msdyn_mainaccounts              |
| Päätililuokat                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Asiakkaat V3                            | tilit                        |

**Riippuvuustiedot**

Financen kaksoiskirjoituspaketti on riippuvainen kaksoiskirjoituksen sovellusytimen paketista. Sen vuoksi kaksoiskirjoituksen sovellusytimen paketti pitää asentaa, ennen kuin asennetaan Financen kaksoiskirjoituspaketti.

## <a name="dual-write-notes"></a>Muistiinpanojen kaksoiskirjoitus

Muistiinpanojen kaksoiskirjoituspaketti sisältää muistiinpanojen ja huomautusten tietojen synkronoinnissa tarvittavat ratkaisut ja yhdistämismääritykset. Se sisältää seuraavat neljä ratkaisua.

| Yksilöivä nimi                  | Näyttönimi                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365: laajennetut muistiinpanot    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 -muistiinpanojen entiteettien yhdistämismääritykset |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 -muistiinpanojen ankkuri      |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Myyntitilauksen otsikkoasiakirjan liitteet    | huomautukset         |
| Asiakkaan liitteet                       | huomautukset         |
| Toimittajan asiakirjaliitteet                | huomautukset         |
| Ostotilauksen otsikkoasiakirjan liitteet | huomautukset         |

**Riippuvuustiedot**

Muistiinpanojen kaksoiskirjoituspaketti riippuu seuraavista kolmesta paketista. Nämä paketit on näin ollen asennettava ennen muistiinpanojen kaksoiskirjoituspaketin asennusta.

- Kaksoiskirjoituksen sovellusydinpaketti
- Financen kaksoiskirjoituspaketti

## <a name="dual-write-asset-management"></a>Resurssien hallinnan kaksoiskirjoitus

Resurssien hallinnan kaksoiskirjoituspaketti sisältää Supply Chain Managementin tai Dynamics 365 Field Servicen resurssitietojen synkronoinnissa tarvittavat ratkaisut ja yhdistämismääritykset. Se sisältää seuraavat neljä ratkaisua.

| Yksilöivä nimi                          | Näyttönimi                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 resurssien hallinta             |
| Dynamics365AssetManagementApp        | Dynamics365 resurssien hallintasovellus          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 resurssien hallinnan entiteettien yhdistämismääritykset |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 resurssien hallinta -ankkuri      |

Tässä paketissa käytettävissä ovat seuraavat yhdistämismääritykset.

| Finance and Operations -sovellukset                           | Asiakkaiden aktivointisovellukset                |
|-------------------------------------------------------|-----------------------------------------|
| Resurssien hallinnan takuu                             | msdyn_warranties                        |
| Resurssien hallinnan mallit                               | msdyn_models                            |
| Resurssien hallinnan valmistajat                        | msdyn_manufacturers                     |
| Resurssien hallinnan toiminnallisen sijainnin tyypit            | msdyn_functionallocationtypes           |
| Resurssien hallinnan toiminnalliset sijainnit                 | msdyn_functionallocations               |
| Resurssien hallinnan toiminnallisen sijainnin elinkaaritilat | msdyn_functionallocationlifecyclestates |
| Resurssien hallinnan toiminnallisen sijainnin elinkaarimallit | msdyn_functionallocationlifecyclemodels |
| Resurssien hallinnan resurssit                               | msdyn_customerassets                    |
| Resurssien hallinnan resurssityypit                          | msdyn_customerassetcategories           |
| Resurssien hallinnan resurssien elinkaaritilat               | msdyn_assetlifecyclestates              |
| Resurssien hallinnan resurssien elinkaarimallit               | msdyn_assetlifecyclemodels              |

**Riippuvuustiedot**

Resurssien hallinnan kaksoiskirjoituspaketti on riippuvainen kaksoiskirjoituksen sovellusytimen paketista. Sen vuoksi kaksoiskirjoituksen sovellusytimen paketti pitää asentaa, ennen kuin asennetaan resurssien hallinnan kaksoiskirjoituspaketti.

## <a name="packages-required-for-project-operations"></a>Project Operationsin edellyttämät paketit
Project Operations riippuu seuraavista paketeista. Nämä paketit on näin ollen asennettava ennen Project Operationsin asennusta.

- Kaksoiskirjoituksen sovellusydinpaketti
- Financen kaksoiskirjoituspaketti
- Toimitusketjun kaksoiskirjoituspaketti
- Resurssien hallinnan kaksoiskirjoituspaketti
- Human Resourcesin kaksoiskirjoituspaketti
