---
title: Integrointi kolmannen osapuolen tuotannonohjausjärjestelmiin
description: Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin integrointia kolmannen osapuolen tuotannonohjausjärjestelmien (MES) kanssa.
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ea39a1fc9092aaa4622c7193f7538acc85aa0f46
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952674"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrointi kolmannen osapuolen tuotannonohjausjärjestelmiin

[!include [banner](../includes/banner.md)]

Jotkin Microsoft Dynamics 365 Supply Chain Managementia käyttävät tuotanto-organisaatiot käyttävät Dynamics 365:n alkuperäisiä toimintoja koneiden, laitteiden ja henkilöstön tuotantotehtävien hallintaan. Sen sijaan toiset tuotanto-organisaatiot käyttävät kolmannen osapuolen tuotannonohjausjärjestelmää (MES), etenkin jos kyse on edistyneistä tuotantovaatimuksista. Organisaatiot saattava valita kolmannen osapuolen MES-ratkaisun myös esimerkiksi siksi, että se on räätälöity nimenomaan heidän toimialalleen.

Integroidussa ratkaisussa tiedonsiirto on täysin automatisoitu ja tapahtuu lähes reaaliaikaisesti. Niinpä tiedot ovat ajantasaisia molemmissa järjestelmissä eikä tietoja tarvitse antaa manuaalisesti. Jos esimerkiksi materiaalin kulutus rekisteröidään MES-ratkaisussa, integrointi varmistaa, että sama kulutus rekisteröidään myös Dynamics 365:ssä. Näin ollen ajantasaiset varastotietueet ovat muiden tärkeiden prosessien, kuten suunnittelun ja myynnin, käytettävissä.

Ratkaisun ansiosta Supply Chain Managementin käyttäjien on entistä nopeampi, kätevämpi ja edullisempi integroitua kolmannen osapuolen MES-ratkaisuihin. Se sisältää seuraavat ominaisuudet:

- Liiketoimintatapahtumat ja liittymät tukevat [keskeisiä tuotannonohjausprosesseja](#processes-available-for-mes-integration).
- Keskitetyssä koontinäytössä voi seurata tapahtuman käsittelyhistoriaa sekä tehdä epäonnistuneiden prosessien vianmäärityksen ja korjata ne.

Seuraavassa kuvassa on tavanomainen integroidussa ratkaisussa siirrettävä liiketoimintatapahtumien, prosessien ja sanomien yhdistelmä.

![Tavanomainen integrointiskenaario](media/3p-mes-scenario.png "Tavanomainen integrointiskenaario")

## <a name="turn-on-the-mes-integration-feature"></a>MES-integrointiominaisuuden ottaminen käyttöön

Ennen kuin voit käyttää tätä toimintoa, järjestelmänvalvojan on otettava se käyttöön järjestelmässä seuraavien ohjeiden mukaisesti.

1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. Varmista, että **Aika ja läsnäolo** -käyttöoikeusavain on käytössä (tarkista valintamerkki). Tämä käyttöoikeusavain on pakollinen, koska se ohjaa valmistuksen suoritusjärjestelmän toimintoja ja tietoja. Jos avain ei ole käytössä, toimi seuraavasti:
    1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
    1. Valitse **Käyttöoikeuksien konfigurointi** -sivulla **Aika ja läsnäolo** -valintaruutu.
    1. Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla
1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Ota luetteloitu ominaisuus käyttöön seuraavalla tavalla (katso myös [Ominaisuuksien hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Moduuli:** *Tuotannonhallinta*
    - **Ominaisuuden nimi:** *Tuotannonohjausjärjestelmän integrointi*

## <a name="processes-available-for-mes-integration"></a>MES-integroinnin käytettävissä olevat prosessit

Mikä tahansa seuraavista prosesseista (tai kaikki prosessit) voidaan integroida.

| Prosessin nimi | Kuvaus |
|---|---|
| Tuotantotilausten vapauttamisen ja tuotantotilauksen tilan muutoksen liiketoimintatapahtumat | Tämä prosessi tuottaa liiketoimintatapahtuman, jota MES voi kuunnella ja saada tällä tavoin tietoja tuotettavista tuotantotilauksista. Tuotantotilaukseen liittyvät viitetiedot. Oletuksena on, että tällainen tuotantotilaus jaetaan Supply Chain Managementista MES-järjestelmään OData (Open Data Protocol) -protokollan tai tietoyksiköiden kautta. |
| Käynnistä tuotantotilaus | Tämä prosessi tuottaa Supply Chain Managementiin tietoja tuotantotilauksista, joita aloitetaan MES-järjestelmän avulla. Se varmistaa, että molemmissa järjestelmissä on kaikkien tuotantotehtävien ajantasainen näkymä. |
| Tuotetun määrän tai hävikin ilmoittaminen | Tämä prosessi tuottaa Supply Chain Managementiin tietoja hyvien ja viallisten tuotteiden määrästä, jotka ilmoitetaan tuotantotyössä MES-järjestelmän avulla. Se varmistaa, että työnjohtajilla on ajantasainen näkymän tuotantosuunnitelman edistymisestä. |
| Materiaalin kulutuksen ilmoittaminen | Tämän prosessin avulla Supply Chain Management saa MES-järjestelmästä tietoja kulutetun materiaalin määrästä. Sen ansiosta ajantasaiset varastotietueet ovat muiden tärkeiden prosessien, kuten suunnittelun ja myynnin, käytettävissä. |
| Työvaiheeseen kulutetun ajan ilmoittaminen | Tämän prosessin avulla Supply Chain Management saa tietoja tiettyyn työvaiheeseen käytetystä ajasta. |
| Tuotantotilauksen lopetus | Tämä prosessi ilmaisee Supply Chain Managementille, että MES on päivittänyt tuotantotilauksen viimeiseen *Päättynyt*-vaiheeseen. Tämä tila ilmaisee, että mitään määriä ei enää tuoteta tuotantotilauksen perusteella. |

## <a name="monitor-incoming-messages"></a>Saapuvien sanomien seuranta

Järjestelmään saapuvia sanomia voi seurata avaamalla **Tuotannonohjausjärjestelmän integrointi** -sivun. Tällä sivulla voi tarkastella ja käsitellä ongelmia sekä tehdä niiden vianmäärityksen.

## <a name="call-the-api"></a>Ohjelmointirajapinnan kutsuminen

MES-integroinnin ohjelmointirajapinnan voi kutsua lähettämällä `POST`-pyynnön seuraavaan päätepisteen URL-osoitteeseen:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Lähetettävän pyynnön tekstiosan pitäisi olla seuraavan esimerkin kaltainen. Vaihda tarvittaessa `_companyId`-, `_messageType`- ja `_messageContent`-arvot. Lisätietoja ohjelmointirajapinnan tukemista erilaisista sanomatyypeistä ja niiden sisällön suunnittelusta on seuraavassa osassa.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>Ohjelmointirajapinnan sanomatyypit ja sanoman sisältö

Tässä osassa käsitellään kutakin sanomatyyppiä, joka voidaan lähettää MES-integroinnin ohjelmointirajapinnan kautta.

### <a name="start-production-order-message"></a>Käynnistä tuotantotilaus -sanoma

*Käynnistä tuotantotilaus* -sanoman `_messageType`-arvo on `ProdProductionOrderStart`. Seuraavassa taulukossa on tämän sanoman tukemat kentät:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ProductionOrderNumber` | Pakollinen | Merkkijono |
| `StartedQuantity` | Valinnainen | Reaaliluku |
| `StartedDate` | Valinnainen | Päivämäärä |
| `AutomaticBOMConsumptionRule` | Valinnainen | Valintalista (FlushingPrincip \|Always \|Never) |

### <a name="report-as-finished-message"></a>Ilmoita valmiiksi -sanoma

*Ilmoita valmiiksi* -sanoman `_messageType`-arvo on `ProdProductionOrderReportFinished`. Seuraavassa taulukossa on tämän sanoman tukemat kentät:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ProductionOrderNumber` | Pakollinen | Merkkijono |
| `ReportFinishedLines` | Pakollinen | Riviluettelo (ainakin yksi rivi), jossa kullakin rivillä on seuraavassa taulukossa kuvatut tiedot. |

Seuraavassa taulukossa on kentät, joita kukin `ProdProductionOrderReportFinished`-sanoman `ReportFinishedLines`-osan rivi tukee:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `LineNumber` | Valinnainen | Reaaliluku |
| `ItemNumber` | Valinnainen | Merkkijono|
| `ProductionType` | Valinnainen | Valintalista (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None), laajennettava |
| `ReportedErrorQuantity` | Valinnainen | Reaaliluku|
| `ReportedGoodQuantity` | Valinnainen | Reaaliluku|
| `ReportedErrorCatchWeightQuantity` | Valinnainen | Reaaliluku |
| `ReportedGoodCatchWeightQuantity` | Valinnainen | Reaaliluku |
| `AcceptError` | Valinnainen |Boolen arvo |
| `ErrorCause` | Valinnainen | Valintalista (None \| Material \| Machine \| OperatingStaff), laajennettava |
| `ExecutedDateTime` | Valinnainen | Päivämäärä ja aika |
| `ReportAsFinishedDate` | Valinnainen | Päivämäärä |
| `AutomaticBOMConsumptionRule` | Valinnainen | Valintalista (FlushingPrincip \|Always \|Never) |
| `AutomaticRouteConsumptionRule` | Valinnainen |Valintalista (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | Valinnainen | Boolen arvo |
| `ProductionJournalNameId` | Valinnainen | Merkkijono |
| `PickingListProductionJournalNameId` | Valinnainen | Merkkijono|
| `RouteCardProductionJournalNameId` | Valinnainen | Merkkijono |
| `FromOperationNumber` | Valinnainen | Kokonaisluku|
| `ToOperationNumber` | Valinnainen | Kokonaisluku|
| `InventoryLotId` | Valinnainen | Merkkijono |
| `BaseValue` | Valinnainen | Merkkijono |
| `EndJob` | Valinnainen | Boolen arvo |
| `EndPickingList` | Valinnainen | Boolen arvo |
| `EndRouteCard` | Valinnainen | Boolen arvo |
| `PostNow` | Valinnainen | Boolen arvo |
| `AutoUpdate` | Valinnainen | Boolen arvo |
| `ProductColorId` | Valinnainen | Merkkijono|
| `ProductConfigurationId` | Valinnainen | Merkkijono |
| `ProductSizeId` | Valinnainen | Merkkijono |
| `ProductStyleId` | Valinnainen | Merkkijono |
| `ProductVersionId` | Valinnainen | Merkkijono |
| `ItemBatchNumber` | Valinnainen | Merkkijono |
| `ProductSerialNumber` | Valinnainen | Merkkijono |
| `LicensePlateNumber` | Valinnainen | Merkkijono |
| `InventoryStatusId` | Valinnainen | Merkkijono |
| `ProductionWarehouseId` | Valinnainen | Merkkijono |
| `ProductionSiteId` | Valinnainen | Merkkijono |
| `ProductionWarehouseLocationId` | Valinnainen | Merkkijono |
| `InventoryDimension1` – `InventoryDimension12` | Valinnainen | Merkkijono |

12 laajennettavaa dimensiota (`InventoryDimension1`– `InventoryDimension12`) edellyttävät mukauttamista, eikä niitä aina käytetä. Lisätietoja niistä on kohdassa [Uusien varastodimensioiden lisääminen laajennuksen avulla](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Materiaalikulutus (keräysluettelo) -sanoma

*Materiaalikulutus (keräysluettelo)* -sanoman `_messageType`-arvo on `ProdProductionOrderPickingList`. Seuraavassa taulukossa on tämän sanoman tukemat kentät:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ProductionOrderNumber` | Pakollinen | Merkkijono |
| `JournalNameId` | Valinnainen | Merkkijono |
| `PickingListLines` | Pakollinen | Riviluettelo (ainakin yksi rivi), jossa kullakin rivillä on seuraavassa taulukossa kuvatut tiedot. |

Seuraavassa taulukossa on kentät, joita kukin `ProdProductionOrderPickingList`-sanoman `PickingListLines`-osan rivi tukee:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ItemNumber` | Pakollinen | Merkkijono |
| `ConsumptionBOMQuantity` | Valinnainen | Reaaliluku |
| `ProposalBOMQuantity` | Valinnainen | Reaaliluku |
| `ScrapBOMQuantity` | Valinnainen | Reaaliluku |
| `BOMUnitSymbol` | Valinnainen | Merkkijono |
| `ConsumptionInventoryQuantity` | Valinnainen | Reaaliluku |
| `ProposalInventoryQuantity` | Valinnainen | Reaaliluku |
| `ConsumptionCatchWeightQuantity` | Valinnainen | Reaaliluku |
| `ProposalCatchWeightQuantity` | Valinnainen | Reaaliluku |
| `ConsumptionDate` | Valinnainen | Päivämäärä |
| `OperationNumber` | Valinnainen | Kokonaisluku |
| `LineNumber` | Valinnainen | Reaaliluku |
| `PositionNumber` | Valinnainen | Merkkijono |
| `IsConsumptionEnded` | Valinnainen | Boolen arvo |
| `ErrorCause` | Valinnainen | Valintalista (None \| Material \| Machine \| OperatingStaff), laajennettava |

### <a name="time-used-for-operation-route-card-message"></a>Työvaiheeseen käytetty aika (reitityskortti) -sanoma

*Työvaiheeseen käytetty aika (reitityskortti)* -sanoman `_messageType`-arvo on `ProdProductionOrderRouteCard`. Seuraavassa taulukossa on tämän sanoman tukemat kentät:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ProductionOrderNumber` | Pakollinen | Merkkijono |
| `JournalNameId` | Valinnainen | Merkkijono |
| `RouteCardLines` | Pakollinen | Riviluettelo (ainakin yksi rivi), jossa kullakin rivillä on seuraavassa taulukossa kuvatut tiedot. |

Seuraavassa taulukossa on kentät, joita kukin `ProdProductionOrderRouteCard`-sanoman `RouteCardLines`-osan rivi tukee:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `OperationNumber` | Pakollinen | Kokonaisluku |
| `OperationPriority` | Valinnainen | Valintalista (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | Valinnainen | Merkkijono |
| `OperationsResourceId` | Valinnainen | Merkkijono |
| `Worker` | Valinnainen | Merkkijono |
| `HoursRouteCostCategoryId` | Valinnainen | Merkkijono |
| `QuantityRouteCostCategoryId` | Valinnainen | Merkkijono |
| `HourlyRate` | Valinnainen | Reaaliluku |
| `Hours` | Valinnainen | Reaaliluku |
| `GoodQuantity` | Valinnainen | Reaaliluku |
| `ErrorQuantity` | Valinnainen | Reaaliluku |
| `CatchWeightGoodQuantity` | Valinnainen | Reaaliluku |
| `CatchWeightErrorQuantity` | Valinnainen | Reaaliluku |
| `QuantityPrice` | Valinnainen | Reaaliluku |
| `ProcessingPercentage` | Valinnainen | Reaaliluku |
| `ConsumptionDate` | Valinnainen | Päivämäärä |
| `TaskType` | Valinnainen | Valintalista (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | Valinnainen | Valintalista (None \| Material \| Machine \| OperatingStaff), laajennettava |
| `OperationCompleted` | Valinnainen | Boolen arvo |
| `BOMConsumption` | Valinnainen | Boolen arvo |
| `ReportAsFinished` | Valinnainen | Boolen arvo |

### <a name="end-production-order-message"></a>Lopeta tuotantotilaus -sanoma

*Lopeta tuotantotilaus* -sanoman `_messageType`-arvo on `ProdProductionOrderEnd`. Seuraavassa taulukossa on tämän sanoman tukemat kentät:

| Kentän nimi | Tila | Tyyppi |
|---|---|---|
| `ProductionOrderNumber` | Pakollinen | Merkkijono |
| `ExecutedDateTime` | Valinnainen | Päivämäärä ja aika |
| `EndedDate` | Valinnainen | Päivämäärä |
| `UseTimeAndAttendanceCost` | Valinnainen | Boolen arvo |
| `AutoReportAsFinished` | Valinnainen | Boolen arvo |
| `AutoUpdate` | Valinnainen | Boolen arvo |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Sanoman tilaa koskevan palautteen vastaanottaminen

Sen jälkeen kun MES on lähettänyt sanoman Supply Chain Managementiin, Supply Chain Managementin on ehkä lähetettävä sanoman tilaa koskevaa palautetta. Seuraavassa on esimerkkejä tilanteista, joita tämä toiminta voi koskea:

- Kukaan ei ole vastuussa MES-integroinnin jatkuvasta valvonnasta.
- MES-integroinnin valvonnasta vastaava henkilö haluaa sähköposti-ilmoituksen epäonnistuneesta sanomasta, jotta jatkotoimiin ryhdytään.
- MES-järjestelmän on näytettävä virhesanoma, jotta tuotannon työntekijä tai IT-osaston työntekijä saa tietää toimenpiteiden tarpeesta.
- MES-järjestelmän on laskettava tilauksen aikataulutus uudelleen virhesanoman vastaanottamisen jälkeen. (Kyse voi olla esimerkiksi siitä, että tuotantotilauksen aloittaminen epäonnistui.)

Näissä tilanteissa voidaan hyödyntää Supply Chain Managementin vakiohälytysominaisuutta. Lisätietoja vakiohälytysten käytöstä on seuraavissa resursseissa:

- Ohjeaihe: [Hälytysten yleiskuvaus](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Dynamics 365 for Finance and Operationsin hälytyssääntövaihtoehdot](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Esimerkiksi seuraavat hälytykset voidaan määrittää antamaan palautetta sanoman tilasta:

- Luo liiketoimintapahtuma (Lähetä ulkoisesti), jota käytetään, kun sanoman tila on *Epäonnistui*.
- Lähetä ilmoitus ja sähköpostiviesti IT-järjestelmänvalvojalle tai tuotannon esimiehelle.
