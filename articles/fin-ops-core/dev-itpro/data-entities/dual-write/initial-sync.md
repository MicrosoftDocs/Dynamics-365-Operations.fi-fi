---
title: Yksikön riippuvuusketju (synkronointijärjestys)
description: Tässä ohjeaiheessa määritetään synkronoinnin järjestys, jota on noudatettava alkuperäisten tietojen luomiseen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275484"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Yksikön riippuvuusketju (synkronointijärjestys)

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe määrittää synkronoinnin järjestyksen, jota on noudatettava, kun alkutiedot luodaan, jos et käytä **alkuperäinen synkronointi** -toiminnon määrittämiä yksikköriippuvuuksia. Jos et käytä **alkuperäinen synkronointi** -vaihtoehtoa, sinun on suoritettava kukin yksikön yhdistämistoiminto yksitellen.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management -yksiköt

Seuraavat Supply Chain Management -yksiköt ovat siinä järjestyksessä, missä ne on otettava käyttöön.

| Nimien yhdistäminen kaksoiskirjoitussivulla | Yksikön metatietojen nimi Supply Chain Managementissa | Yksikön metatietojen nimi Common Data Servicessä | Muistiinpanot |
|---|---|---|---|
| Yksiköt ... mittayksiköiksi                                                                      | UnitOfMeasureEntity                                    | mittayksikkö                                          | |
| Yksikkömuunnokset ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Kaikki tuotteet ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Tuotedimensioryhmät ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Varastodimensioryhmät ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Seurantadimensioryhmät ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Värit ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Koot ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Tyylit ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Määritykset ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Vapautetut tuotteet V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service on vapauttanut erilliset tuotteet ... tuotteisiin                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | tuote                                      | |
| Tuotenumeron tunnistava viivakoodi ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Tuotteen oletusarvoiset tilausasetukset ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Tuotteen oletusarvoiset tilausasetukset V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Tuotekohtaiset yksikkömuunnokset ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Toimipaikat ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Varastot ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Katso [huomautus 1](#scm-notes). |
| Päätuotteen värit ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Päätuotteen koot ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Päätuotteen tyylit ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Päätuotemääritykset ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Tuoteluokat ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Katso [huomautus 2](#scm-notes). |
| Tuoteluokkamääritykset ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Tuoteluokkahierarkiat ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Tuoteluokkahierarkian roolit ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Inventory aisle ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Varastovyöhykkeet ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Varastovyöhykeryhmät ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Varaston sijainnit ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Katso [huomautus 3](#scm-notes). |
| Varastotyön otsikot ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Varastotyön rivit ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Katso [huomautus 4](#scm-notes). |
| Toimitustavat ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Toimitusehdot ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Myyntitilauksen alkuperäkoodit ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Servicen myyntitilauksen otsikot ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | myyntitilaus                                   | |
| Common Data Service -myyntitilausrivit ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service -myyntitarjouksen otsikko ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | tarjous                                        | |
| Common Data Service -myyntitarjousrivit ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Myyntilaskun otsikot V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | lasku                                      | |
| Myyntilaskun rivit V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Yhdistämisen yksilöidyt huomautukset

1. Riippumattomuuden vuoksi ensimmäinen synkronointi on ehkä suoritettava kahdesti.
2. Oletusarvoisesti ensimmäinen synkronointi poistetaan käytöstä ylä- ja alatason välisen suhteen vuoksi ("älykäs" tilaus ei ole alustan käsiteltävissä). Tämän vuoksi aiemmin luodut tuoteluokat ovat synkronoitavissa manuaalisesti (esimerkiksi päivittämällä luokan kuvaus) oikeassa järjestyksessä (ensisijainen luokka, sitten alatasot ja alatasojen alatasot). Valitse **Tuotetietojen hallinta \> Asetukset \> Luokat ja määritteet \> Luokkahierarkiat**. **Luokkahierarkiat**-sivulla voit valita kunkin hierarkian ja tarkastella sen tuoteluokkia.
3. Tyhjien **ItemNumberInLocation**-hakukenttien ja ensimmäisen, toisen ja kolmannen lisävarastovyöhykkeen yhdistäminen aiheuttaa ensimmäisen synkronoinnin epäonnistumisen. Näin ollen nämä yhdistämismääritykset poistetaan nyt.
4. Tyhjän **CaptureWeight**-kentän yhdistäminen aiheuttaa sen, että ensimmäinen synkronointi epäonnistuu. Näin ollen tämä yhdistämismääritys poistetaan nyt.

### <a name="setup-related-information"></a>Asennukseen liittyviä tietoja

+ Kun **Tuote**-yksikköön luodaan ensimmäisen kerran tietueita Dynamics 365 -järjestelmän mallipohjaisille sovelluksille, niiden tila on **Luonnos**. Jos haluat muuttaa tilaksi **Aktiivinen**, siirry kohtaan **Asetukset \> Hallinta \> Järjestelmäasetukset \> Myynti** mallipohjaisessa sovelluksessa ja määritä **Luo tuotteet aktiivisessa tilassa** -asetuksen arvoksi **Kyllä**.
+ Jos luot mallipohjaisia sovelluksia Dynamics 365- tai Common Data Service -sovelluksessa **Tuote**-entiteettiin, ennen kuin otat kaksoiskirjoituksen käyttöön, nämä tiedot päivitetään vain, jos koko avain, **Yritys** mukaan lukien, vastaa Finance and Operations -sovelluksen tietoja.
+ **Tuotteet**-yksikön synkronointi on yksisuuntainen Finance and Operations -sovelluksista Common Data Serviceen. Jos Dynamics 365:n mallipohjaiset sovellukset -kohteen **Tuotteet**-yksikössä oleva yhdistetty kenttä päivitetään, päivitys korvataan Finance and Operations -sovelluksen seuraavan synkronoinnin aikana.

### <a name="known-issues"></a>Tunnetut ongelmat

- Virhe ilmenee, kun yksikkö poistetaan Finance and Operations -sovelluksesta. Kun mittayksiköt synkronoidaan Finance and Operations -sovelluksesta Common Data Service -järjestelmään, tietyn luokan ensimmäinen yksikkö luodaan ensisijaiseksi yksiköksi ja se estää poiston.

    **Lieventäminen:** Poista ensin yksikkö Common Data Servicessä. Sen jälkeen se voidaan poistaa Finance and Operations -sovelluksessa.

- Virhe ilmenee, kun toimintapaikka poistetaan Common Data Servicestä. Virhesanomassa todetaan, "Infoloki: Varoitus: ensisijaista osoitetta ei voi poistaa.; Varoitus: yksikkötietuetta ei voitu poistaa, koska seuraavan tietolähteen oikeellisuustarkistus epäonnistui: InventSiteLogisticsLocation (InventSiteLogisticsLocation)." Tämän virheen aiheuttaa Finance and Operations -sovelluksen tietoyksikön ongelma.

    **Lieventäminen** : Voit poistaa sivuston Finance and Operations -sovelluksessa. Sivusto poistetaan Common Data Servicessä, jos vastaava kaksoiskirjoituksen yhdistäminen on meneillään.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance -yksiköt

Seuraavat Dynamics 365 Finance -yksiköt ovat siinä järjestyksessä, missä ne on otettava käyttöön.

| Nimien yhdistäminen kaksoiskirjoitussivulla | Yksikön metatietojen nimi Taloudessa | Yksikön metatietojen nimi Common Data Servicessä | Muistiinpanot |
|---|---|---|---|
| Valuutat ... transactioncurrencies                                            | CurrencyEntity                              | Valuutta                                   | |
| Vaihtokurssin tyypit ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Vaihtokurssin valuuttapari ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service -vaihtokurssit ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Katso [huomautus 1](#fin-notes). |
| Kirjanpidon kalenterivuoden integrointiyksikkö ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Kirjanpidon kalenterivuoden integrointiyksikkö ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Kirjanpidon kalenterikausi ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organisaatiohierarkiatyyppi ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Katso [huomautus 1](#fin-notes). |
| Organisaatiohierarkiatarkoitukset ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Katso [huomautus 1](#fin-notes). |
| Yritykset ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Katso [huomautus 1](#fin-notes). |
| Yritykset ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Toimintayksikkö ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Katso [huomautus 1](#fin-notes). |
| Organisaatiohierarkia – julkaistu ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Katso [huomautus 1](#fin-notes). |
| Nimien liitteet ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Maksupäivät Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Maksupäivärivit Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Maksuaikataulu ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Maksuaikataulurivit ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Maksuehdot ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Asiakkaan maksutapa ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Toimittajan maksutapa ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Asiakasryhmät ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Toimittajaryhmät ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Arvonlisäveroryhmät ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Nimikkeen arvonlisäveroryhmät ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Arvonlisäveron kirjanpidon kirjausryhmät V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Arvonlisäveron verovapauskoodiyksikkö Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Arvonlisäveroviranomaiset ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Arvonlisäverokoodi ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Katso [huomautus 1](#fin-notes). |
| Taloushallinnon dimension muoto ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Taloushallinnon dimensiot ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Ennakonpidätysryhmät ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Ennakonpidätyskoodit ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Tilikartta ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Kirjanpito ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Katso [huomautus 1](#fin-notes). |
| Päätililuokat ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Päätili ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Asiakkaat V3 ... tilit                                                       | CustCustomerV3Entity                        | tili                                    | Katso [huomautus 2](#fin-notes). |
| Asiakkaat V3 ... yhteyshenkilöt                                                       | CustCustomerV3Entity                        | yhteystiedot                                    | Katso [huomautus 3](#fin-notes). |
| Toimittajat V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Katso [huomautus 2](#fin-notes). |
| Common Data Service -kontaktit V2 ... yhteyshenkilöt                                    | SmmcontachpersonCommon Data ServiceV2Entity | yhteystiedot                                    | Katso [huomautus 4](#fin-notes). |
| Common Data Service -kontaktit V2 ... yhteyshenkilöt                                    | SmmcontachpersonCommon Data ServiceV2Entity | yhteystiedot                                    | Katso [huomautus 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Yhdistömisen yksilöidyt huomautukset

1. Yksisuuntainen synkronointi tapahtuu Finance and Operations -sovelluksista Common Data Service -järjestelmään.
2. Riippumattomuuden vuoksi ensimmäinen synkronointi on ehkä suoritettava useammin kuin kerran. Muista valita suhdetyypiksi **Asiakas**, kun luot tilin käyttämällä **Tilit**-sivua Common Data Service -järjestelmässä. Jos **Ensisijainen yhteyshenkilö** -kentän kanssa ilmenee ongelmia ensimmäisen synkronoinnin aikana, poista kenttä yhdistämismäärityksestä ja suorita sitten ensimmäinen synkronointi uudelleen. Kun ensimmäinen synkronointi on suoritettu onnistuneesti, pysäytä yhdistämismääritys ja lisää **Ensisijainen yhteystieto** -kenttä uudelleen. Käynnistä sitten yhdistämismääritys, mutta ohita ensimmäinen synkronointi. **Ensisijainen yhteyshenkilö** -kentän arvoa ei sisällytetä ensimmäiseen synkronointiin ja arvot on siirrettävä manuaalisesti.
3. Muista määrittää **Myytävissä oleva** -kohdan asetukseksi **Kyllä** **Yhteyshenkilöt**-sivulla Common Data Servicessä, kun yrität luoda **Henkilö**-tyyppisen asiakkaan.
4. Tämän yhdistämismäärityksen molemmilla puolilla on suodatin, joka linkittää asiakaskontaktit. Avaa yhdistämistiedot, valitse suodatinpainike (suppilosymboli) **Sales.Contact**-yksikkönimen vieressä ja varmista, että tiedostoehdot sisältävät tekstin **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Tämän yhdistämismäärityksen molemmilla puolilla on suodatin, joka linkittää toimittajakontaktit. Avaa yhdistämistiedot, valitse suodatinpainike (suppilosymboli) **Sales.Contact**-yksikkönimen vieressä ja varmista, että suodatinehdot sisältävät tekstin **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources -yksiköt

Seuraavat Dynamics 365 Human Resources -yksiköt ovat siinä järjestyksessä, missä ne on otettava käyttöön.

| Nimien yhdistäminen kaksoiskirjoitussivulla | Yksikön metatietojen nimi henkilöstöhallinnossa | Yksikön metatietojen nimi Common Data Servicessä | Muistiinpanot |
|---|---|---|---|
| cdm_jobfunction - Työtehtävä                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Työlajit                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Työpaikat                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Työn tiedot                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Perustoimi                              | HcmPositionBaseEntity             | cdm_jobposition                  | Katso [huomautus 1](#hr-notes). |
| cdm_jobposition - Toimitiedot                            | HcmPositionDetailEntity           | cdm_jobposition                  | Katso [huomautus 1](#hr-notes). |
| cdm_jobposition - Toimen kesto                           | HcmPositionDurationEntity         | cdm_jobposition                  | Katso [huomautus 1](#hr-notes). |
| cdm_jobposition - Toimihierarkiat                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Katso [huomautus 1](#hr-notes). |
| cdm_veteranstatus - Veteraanitila                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Etninen alkuperä                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Kielikoodi                              |                                   | cdm_languagecode                 | |
| cdm_worker - Työntekijä                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Työsuhteet                                 |                                   | cdm_employments                  | |
| cdm_employments - Työsuhdetieto                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Toimen työntekijämääritys | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Katso [huomautus 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Yhdistämiseen yksilöidyt huomautukset

1. Yksi Common Data Service -yksikkö on yhdistetty useisiin Finance and Operations -sovellusyksiköihin.
2. Tällä yhdistämisellä on oma viittaus.

## <a name="asset-management-entities"></a>Resurssien hallinnan yksiköt

Seuraavat Dynamics 365 Supply Chain Management -resurssien hallintayksiköt ovat siinä järjestyksessä, missä ne on otettava käyttöön.

| Nimien yhdistäminen kaksoiskirjoitussivulla | Yksikön metatietojen nimi resurssien hallinnassa | Yksikön metatietojen nimi Common Data Servicessä | Muistiinpanot |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Resurssien hallinnan resurssien elinkaaritilat               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Resurssien hallinnan resurssien elinkaarimallit               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Resurssien hallinnan toiminnallisen sijainnin elinkaarimallit | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Resurssien hallinnan toiminnallisen sijainnin elinkaaritilat | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Resurssien hallinnan resurssityypit                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Resurssien hallinnan toiminnallisen sijainnin tyypit            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Resurssien hallinnan toiminnalliset sijainnit                 | msdyn_functionallocations                | Katso [huomautus](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Resurssien hallinnan resurssit                               | msdyn_customerassets                     | Katso [huomautus](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Resurssien hallinnan valmistajat                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Resurssien hallinnan mallit                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Resurssien hallinnan takuu                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Yhdistämiseen yksilöidyt huomautukset

- Riippumattomuuden vuoksi ensimmäinen synkronointi on ehkä suoritettava useammin kuin kerran.
