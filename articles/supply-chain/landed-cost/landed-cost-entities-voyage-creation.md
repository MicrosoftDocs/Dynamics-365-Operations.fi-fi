---
title: Matkan luonnin yksiköt
description: Tässä artikkelissa on tietoja matkan luonnin tietoyksiköistä, jotka ryhmittelevät toimivan matkan luontiin vaadittavat tietoyksiköt.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6234dfa61a5859e2ecaca75594c69c49ba326629
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167668"
---
# <a name="voyage-creation-entities"></a>Matkan luontiyksiköt

[!include [banner](../includes/banner.md)]

Matkan luonnin tietoyksiköt ryhmittelevät toimivan matkan luontiin vaadittavat tietoyksiköt. Yrityksesi ja huolitsija voivat käyttää näitä tietoyksiköitä matkan, lähetyskontin, pakkauksen ja matkan rivitietueiden luomiseen viitaten aiemmin luotuun ostotilaukseen tai siirtotilausriveihin.

## <a name="voyages-itmtableentity"></a>Matkat (ITMTableEntity)

Matka edustaa saapuvien tuotteiden matkaa ja toimii ylimmän tason kustannusalueena aiheutuneissa kustannuksissa. Se sisältää otsikkotason tietoja, jotka liittyvät alukseen, lähtösatamaan ja kohdesatamaan. Tätä toimintoa tukee `ITMTableEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Toimitustapa | ITMTable.DlvModeId | Nvarchar(10) | En | En |
| Välittäjä neuvoi | ITMTable.ITMBrokerAdvised | Datetime | En | En |
| Asiakastapaaminen | ITMTable.ITMCustomerAppointment | Datetime | En | En |
| Toimitettu varastoon | ITMTable.ITMDelAtWarehouse | Datetime | En | En |
| Toimitusohjeet | ITMTable.ITMDeliveryInstructions | Datetime | En | En |
| Lähtöpäivämäärä | ITMTable.ITMDepartureDate | Datetime | En | En |
| Vapautetut tavarat | ITMTable.ITMGoodsReleased | Datetime | En | En |
| Paikallisen kuljetuksen päivämäärä | ITMTable.ITMLocalTransportDate | Datetime | En | En |
| Paikallisen kuljetuksen aika | ITMTable.ITMLocalTransportTime | Int | En | En |
| Alkuperäinen rahtikirja lähetetty | ITMTable.ITMOriginalBOLSebt | Datetime | En | En |
| Alkuperäiset asiakirjat vastaanotettu | ITMTable.ITMOriginalDocsReceived | Datetime | En | En |
| Ostotilauksen tila | ITMTable.ITMPurchStatus | Int | En | En |
| Tarkistuspäivämäärä | ITMTable.ITMVerificationDate | Datetime | En | En |
| Tullimerkinnän tunnus | ITMTable.ShipCustomsEntryId | Nvarchar(20) | En | En |
| Lähetyspäivä | ITMTable.ShipDate | Datetime | En | En |
| Kuvaus | ITMTable.ShipDescription | Nvarchar(60) | En | En |
| Asiakirjat vastaanotettu | ITMTable.ShipDocReceived | Int | En | En |
| Arvioitu toimituspäivämäärä | ITMTable.ShipEstDlvDate | Datetime | En | En |
| Arvioitu saapumisaika lähetyssatamaan | ITMTable.ShipEstPortDate | Datetime | En | En |
| Lähtösatama | ITMTable.ShipFromPort | Nvarchar(20) | En | En |
| Alalentorahtikirja/rahtikirja | ITMTable.ShipHAWB | Nvarchar(20) | En | En |
| Matka | ITMTable.ShipId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Varausviite | ITMTable.ShipIdExternal | Nvarchar(20) | En | En |
| Matkamalli | ITMTable.ShipJourneyId | Nvarchar(20) | En | En |
| Paikallinen huolitsija | ITMTable.ShipLocalForwarder | Nvarchar(20) | En | En |
| Päälentorahtikirja/rahtikirja | ITMTable.ShipMAWB | Nvarchar(20) | En | En |
| Mittaus | ITMTable.ShipMeasurement | Numeric(32, 6) | En | En |
| Mittayksikkö | ITMTable.ShipMeasurementUnit | Int | En | En |
| Kuormalavojen määrä | ITMTable.ShipNoOfPallets | Int | En | En |
| Odottava matka | ITMTable.ShipPending | Int | En | En |
| Huomautukset | ITMTable.ShipRemarks | Nvarchar(MAX) | En | En |
| Vuokra | ITMTable.ShipRental | Int | En | En |
| Matkan tila | ITMTable.ShipStatusId | Nvarchar(20) | En | En |
| Laskuri kohdassa numero | ITMTable.ShipTallyInNumber | Nvarchar(20) | En | En |
| Satamaan | ITMTable.ShipToPort | Nvarchar(20) | En | En |
| Arvostuspäivämäärä | ITMTable.ShipValuationDate | Datetime | En | En |
| Kuljetusyritys | ITMTable.ShipVendAccount | Nvarchar(20) | En | En |
| Alus | ITMTable.ShipVesselId | Nvarchar(20) | En | **Kyllä** |
| Ulkoisen matkan tunnus | ITMTable.ShipVoyage | Nvarchar(20) | En | En |

### <a name="number-sequences-for-voyages"></a>Matkojen numerosarjat

Matkojen jaettu numerosarja ohjaa matkojen tunnuksien kohdistusta.

Arvoa, joka välitetään tietoyksikköön **Matkan tunnus** (`ShipId`) -arvona, käytetään aiemmin luodun tietueen tunnistamiseksi päivittämistä varten. Jos tietuetta ei ole, toiminta määräytyy sen mukaan, onko määritetty numerosarja määritetty sallimaan manuaalinen syöttö:

- Jos manuaalinen syöttö on otettu käyttöön, luodaan uusi tietue, joka käyttää välitettyä arvoa.
- Jos manuaalista syöttöä ei ole otettu käyttöön, välitetyn arvon asemesta käytetään määritetyn numerosarjan seuraavaa numeroa.

Tuonti-istunnon aikana matkan tunnuksena tuotu paikkamerkin arvo säilytetään. Näin varmistetaan, että lähetyskontti ja matkan rivit, jotka viittaavat kyseiseen paikkamerkkiin, sisällytetään matkaan, ja että ne päivitetään kuvastamaan määritettyä numerosarjan arvoa.

### <a name="automatic-cost-transactions"></a>Automaattiset kustannustapahtumat

Automaattisia kustannuksia voi lisätä matkaan **Automaattiset kustannukset** -sivulta Microsoft Dynamics 365 Supply Chain Managementissa (**Aiheutuneet kustannukset \> Kustannuslaskennan asetukset \>Automaattiset kustannukset**). Automaattisten kustannusten tietueita voidaan luoda myös käyttämällä kustannustapahtumatietojen yksiköitä jokaiselle kustannusalueelle, jota aiheutuneet kustannukset tukevat.

Automaattisia kustannuksia, jotka on määritetty Supply Chain Managementissa, sovelletaan matkaan, kun matkarivi on luotu. Tietueelle ei näy kustannuksia ennen kuin otsikkotietueeseen on liitetty rivitiedot.

## <a name="shipping-containers-itmcontainersentity"></a>Lähetyskontit (ITMContainersEntity)

Lähetyskontti edustaa fyysistä konttia, jossa tuotteet kuljetetaan. Tämä fyysinen kontti voi olla rahtikontti (merirahti) tai yksittäinen kuormalava (lentorahti). Lähetyskontti sisältää otsikkotason tiedot, jotka liittyvät lähetyskontin tunnukseen, sinettinumeroon ja lähetyskontin tyyppiin. (Lähetyskontin tyyppiin kuuluu mittatiedot.) Tätä toimintoa tukee `ITMContainersEntity`-yksikkö. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Lähtöpäivämäärä | ITMContainers.ITMDepartureDate | Datetime | En | En |
| Paikallisen kuljetuksen päivämäärä | ITMContainers.ITMLocalTransportDate | Datetime | En | En |
| Paikallisen kuljetuksen aika | ITMContainers.ITMLocalTransportTime | Int | En | En |
| Alkuperäinen matka | ITMContainers.OrigShipId | Nvarchar(20) | En | En |
| Todellinen paino | ITMContainers.ShipActualWeight | Numeric(32, 6) | En | En |
| Välittäjä neuvoi | ITMContainers.ShipBrokerAdvised | Datetime | En | En |
| Lähetyskontti | ITMContainers.ShipContainerId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Lähetyskontin tyyppi | ITMContainers.ShipContainerTypeId | Nvarchar(20) | En | En |
| Yksikkötyyppi | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | En | En |
| Muunnettu vuokraksi | ITMContainers.ShipConvertedToRental | Int | En | En |
| Asiakastapaaminen | ITMContainers.ShipCustomerAppointment | Datetime | En | En |
| Lähetyspäivä | ITMContainers.ShipDate | Datetime | En | En |
| Toimitettu varastoon | ITMContainers.ShipDelAtWarehouse | Datetime | En | En |
| Toimitusohjeet | ITMContainers.ShipDeliveryInstructions | Datetime | En | En |
| Tarkastustodistuksen kohdistuksen päivämäärä | ITMContainers.ShipECAppliedDate | Datetime | En | En |
| Tarkastustodistuksen vanhenemispäivä | ITMContainers.ShipECExpiryDate | Datetime | En | En |
| Tarkastustodistuksen numero | ITMContainers.ShipECNum | Nvarchar(20) | En | En |
| Tarkastustodistuksen vastaanottopäivämäärä | ITMContainers.ShipECReceivedDate | Datetime | En | En |
| Arvioitu toimituspäivämäärä | ITMContainers.ShipEstDlvDate | Datetime | En | En |
| Arvioitu saapumisaika lähetyssatamaan | ITMContainers.ShipEstPortDate | Datetime | En | En |
| Odotettu kuormauksen päivämäärä | ITMContainers.ShipExpectedLoadingDate | Datetime | En | En |
| Lähtösatama | ITMContainers.ShipFromPort | Nvarchar(20) | En | En |
| Tavaroiden kuvaus | ITMContainers.ShipGoodsDesc | Nvarchar(60) | En | En |
| Vapautetut tavarat | ITMContainers.ShipGoodsReleased | Datetime | En | En |
| GPS-seurantayksikkö | ITMContainers.ShipGPSUnit | Nvarchar(30) | En | En |
| Alalentorahtikirja/rahtikirja | ITMContainers.ShipHAWB | Nvarchar(20) | En | En |
| Matka | ITMContainers.ShipId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Matkamalli | ITMContainers.ShipJourneyId | Nvarchar(20) | En | En |
| Paikallinen huolitsija | ITMContainers.ShipLocalForwarder | Nvarchar(20) | En | En |
| Mittaus | ITMContainers.ShipMeasurement | Numeric(32, 6) | En | En |
| Mittayksikkö | ITMContainers.ShipMeasurementUnit | Int | En | En |
| Laatikoiden määrä | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | En | En |
| Alkuperäinen rahtikirja lähetetty | ITMContainers.ShipOriginalBOLSebt | Datetime | En | En |
| Alkuperäiset asiakirjat vastaanotettu | ITMContainers.ShipOriginalDocsReceived | Datetime | En | En |
| Sinettinumeromme | ITMContainers.ShipOurSealNum | Nvarchar(20) | En | En |
| Käytetty | ITMContainers.ShipPendingUsed | Int | En | En |
| Ostotilauksen tila | ITMContainers.ShipPurchStatus | Int | En | En |
| Kylmäsäilytystyyppi | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | En | En |
| Huomautukset | ITMContainers.ShipRemarks | Nvarchar(MAX) | En | En |
| Vuokra | ITMContainers.ShipRental | Int | En | En |
| Palautettavissa | ITMContainers.ShipReturnable | Int | En | En |
| Matkan tila | ITMContainers.ShipStatusId | Nvarchar(20) | En | En |
| Kuljetusyrityksen sinetin numero | ITMContainers.ShipTheirSealNum | Nvarchar(20) | En | En |
| Satamaan | ITMContainers.ShipToPort | Nvarchar(20) | En | En |
| Tarkistuspäivämäärä | ITMContainers.ShipVerificationDate | Datetime | En | En |
| Alus | ITMContainers.ShipVesselId | Nvarchar(20) | En | **Kyllä** |

### <a name="voyage-id-validation"></a>Matkan tunnuksen vahvistus

Numerosarja ei ohjaa lähetyskontin tunnusta. Se on yksilöllinen vain liittyen siihen matkaan, jossa sitä käytetään.

Jos lähetyskontin yksikköä (`ITMContainersEntity`) käytetään riippumattomasti matkan yksiköstä (`ITMTableEntity`), **Matkan tunnus** (`ShipId`) -arvon on vastattava aiemmin luotua tietuetta matkan taulukossa. Muussa tapauksessa tuonti epäonnistuu.

Jos lähetyskontin yksikköä (`ITMContainersEntity`) ja matkan yksikköä (`ITMTableEntity`) käytetään saman tuonti-istunnon osina, matkan yksikön on oltava ennen lähetyskontin luontia. Muussa tapauksessa **Matkan tunnus** (`ShipId`) -arvoa ei voi vahvistaa onnistuneesti. Jos **Matkan tunnus** (`ShipId`) -arvolle käytetään paikkamerkkiarvoa, liitos voidaan luoda vain, jos samaa paikkamerkkiä käytetään  **Matkan tunnus** (`ShipId`) -arvona lähetyskontin yksikössä.

### <a name="other-field-validations"></a>Muiden kenttien vahvistukset

Seuraavassa taulukossa näkyvät lähetyskontin taulukon (`ITMContainers`) kentät, jotka vahvistetaan aiheutuneiden kustannusten asetustaulukoiden mukaan. Se näyttää myös aiheutuneiden kustannusten tietoyksiköt, joiden avulla huolitsija voi lukea aiemmat arvot ja varmistaa, että ympäristöihin vastaanotetaan kelvollisia arvoja.

| Kenttä ITMContainers-taulukossa | Aiheutuneiden kustannusten tietoyksikkö |
|---|---|
| Lähetyskontin tyyppi | ITMShippingContainerTypeEntity |
| Tavaroiden kuvaus | ITMGoodsDescriptionEntity |
| Kylmäsäilytystyyppi | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Pakkaukset (ITMFolioEntity)

Pakkaus edustaa nimikkeiden ryhmittelyä lähetyskontissa tulli-ilmoituksia varten. Pakkaus sisältää otsikkotason tietoja, jotka liittyvät tulliasioitsijaan ja tuotteiden kuvaukseen. Tätä toimintoa tukee `ITMFolioEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Välittäjä neuvoi | ITMFolioTable.ShipBrokerAdvised | Datetime | En | En |
| Rahdin tarkistusnumero | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | En | En |
| Asiakastapaaminen | ITMFolioTable.ShipCustomerAppointment | Datetime | En | En |
| Tulliasiamies | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | En | En |
| Tullin tunnus | ITMFolioTable.ShipCustomsId | Nvarchar(60) | En | En |
| Yritys | ITMFolioTable.ShipDataArea | Nvarchar(4) | En | **Kyllä** |
| Toimitettu varastoon | ITMFolioTable.ShipDelAtWarehouse | Datetime | En | En |
| Toimitusohjeet | ITMFolioTable.ShipDeliveryInstructions | Datetime | En | En |
| Asiakirjat vastaanotettu | ITMFolioTable.ShipDocReceived | Int | En | En |
| Arvioitu toimituspäivämäärä | ITMFolioTable.ShipEstDlvDate | Datetime | En | En |
| Arvioitu saapumisaika lähetyssatamaan | ITMFolioTable.ShipEstPortDate | Datetime | En | En |
| Viejä | ITMFolioTable.ShipExporterId | Nvarchar(20) | En | En |
| Nimi | ITMFolioTable.ShipExporterName | Nvarchar(60) | En | En |
| Laskun päivämäärä | ITMFolioTable.ShipFolioDate | Datetime | En | En |
| Lasku | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Kyllä** | **Kyllä** |
| Lähtösatama | ITMFolioTable.ShipFromPort | Nvarchar(20) | En | En |
| Tavaroiden kuvaus | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | En | En |
| Vapautetut tavarat | ITMFolioTable.ShipGoodsReleased | Datetime | En | En |
| Alalentorahtikirja/rahtikirja | ITMFolioTable.ShipHAWB | Nvarchar(20) | En | En |
| Matka | ITMFolioTable.ShipId | Nvarchar(20) | En | **Kyllä** |
| Mittaus | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | En | En |
| Mittayksikkö | ITMFolioTable.ShipMeasurementUnit | Int | En | En |
| Laatikoiden määrä | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | En | En |
| Alkuperäinen rahtikirja lähetetty | ITMFolioTable.ShipOriginalBOLSebt | Datetime | En | En |
| Alkuperäiset asiakirjat vastaanotettu | ITMFolioTable.ShipOriginalDocsReceived | Datetime | En | En |
| Ostotilauksen tila | ITMFolioTable.ShipPurchStatus | Int | En | En |
| Huomautukset | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | En | En |
| Matkan tila | ITMFolioTable.ShipStatusId | Nvarchar(20) | En | En |
| Tariffikoodi | ITMFolioTable.ShipTariffCode | Nvarchar(10) | En | En |
| Satamaan | ITMFolioTable.ShipToPort | Nvarchar(20) | En | En |
| Arvostuspäivämäärä | ITMFolioTable.ShipValuationDate | Datetime | En | En |
| Tarkistuspäivämäärä | ITMFolioTable.ShipVerificationDate | Datetime | En | En |
| Toimittajanro | ITMFolioTable.VendAccount | Nvarchar(20) | En | En |

### <a name="number-sequences-for-folios"></a>Pakkausten numerosarjat

Pakkausten numerosarja ohjaa pakkausten tunnuksien kohdistusta.

Arvoa, joka välitetään tietoyksikköön **Pakkauksen tunnus** (`FolioId`) -arvona, käytetään aiemmin luodun tietueen tunnistamiseksi päivittämistä varten. Jos tietuetta ei ole, toiminta määräytyy sen mukaan, onko määritetty numerosarja määritetty sallimaan manuaalinen syöttö:

- Jos manuaalinen syöttö on otettu käyttöön, luodaan uusi tietue, joka käyttää välitettyä arvoa.
- Jos manuaalista syöttöä ei ole otettu käyttöön, välitetyn arvon asemesta käytetään määritetyn numerosarjan seuraavaa numeroa.

Tuonti-istunnon aikana pakkauksen tunnuksena tuotu paikkamerkin arvo säilytetään. Näin varmistetaan, että matkan rivit, jotka viittaavat kyseiseen paikkamerkkiin, on liitetty oikein, ja että ne päivitetään kuvastamaan määritettyä numerosarjan arvoa.

### <a name="field-validations"></a>Kenttien vahvistukset

**Tavaroiden kuvaus** -kenttä pakkaustaulukossa (`ITMFolioTable`) vahvistetaan aiheutuneiden kustannusten samannimisen asetustaulukon mukaan. Huolitsija voi käyttää aiheutuneiden kustannusten `ITMGoodsDescriptionEntity`-tietoyksikköä ja lukea aiemmat arvot ja varmistaa, että ympäristöihin vastaanotetaan kelvollisia arvoja.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Ostotilausten matkarivit (ITMPurchaseLineEntity)

Matkarivi edustaa yksittäistä ostotilausriviä, joka sisältyy matkaan. Tämä suhde perustuu **Ostotilauksen numero**- ja **Ostorivin numero** -kenttiin. Matkarivi viittaa jokaiseen edelliseen tietueeseen, joka luotiin matkaa, lähetyskonttia ja pakkausta varten. Tätä toimintoa tukee `ITMPurchaseLineEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Valuutta | ITMLine.CurrencyCode | Nvarchar(3) | En | En |
| Nettosumma | ITMLine.LineAmountMST | Numeric(32, 6) | En | En |
| Ostorivin numero | ITMLine.RefRecId | Numeric(32, 6) | **Kyllä** | En |
| Lähetyskontti | ITMLine.ShipContainerId | Int | En | En |
| Yritys | ITMLine.ShipDataArea | Nvarchar(20) | **Kyllä** | En |
| Ilmoitettu määrä | ITMLine.ShipDeclaredQty | Nvarchar(4) | En | En |
| Lasku | ITMLine.ShipFolioId | Numeric(32, 6) | En | En |
| Matka | ITMLine.ShipId | Nvarchar(20) | **Kyllä** | En |
| Nimiketunnus | ITMLine.ShipItemId | Nvarchar(20) | En | En |
| Mittaus | ITMLine.ShipMeasurement | Nvarchar(20) | En | En |
| Mittayksikkö | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | En | En |
| Laatikoiden määrä | ITMLine.ShipNoOfCartons | Int | En | En |
| Positio | ITMLine.ShipPosition | Numeric(32, 6) | En | En |
| Määrä | ITMLine.ShipQty | Int | En | En |
| Ostotilauksen numero | ITMLine.TransRefId | Numeric(32, 6) | **Kyllä** | En |
| Yksikkö | ITMLine.UnitId | Int | En | En |
| Äänenvoimakkuus | ITMLine.Volume | Nvarchar(10) | En | En |
| Paino | ITMLine.Weight | Numeric(32, 6) | En | En |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Siirtotilausten matkarivit (ITMTransferLineEntity)

Matkarivi edustaa yksittäistä siirtotilausriviä, joka sisältyy matkaan. Tämä suhde perustuu **Siirtotilauksen numero**- ja **Siirtorivin numero** -kenttiin. Matkarivi viittaa jokaiseen edelliseen tietueeseen, joka luotiin matkaa, lähetyskonttia ja pakkausta varten. Tätä toimintoa tukee `ITMTransferLineEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Valuutta | ITMLine.CurrencyCode | Nvarchar(3) | En | En |
| Nettosumma | ITMLine.LineAmountMST | Numeric(32, 6) | En | En |
| Lähetyskontti | ITMLine.ShipContainerId | Int | En | En |
| Yritys | ITMLine.ShipDataArea | Nvarchar(20) | **Kyllä** | En |
| Ilmoitettu määrä | ITMLine.ShipDeclaredQty | Nvarchar(4) | En | En |
| Lasku | ITMLine.ShipFolioId | Numeric(32, 6) | En | En |
| Matka | ITMLine.ShipId | Nvarchar(20) | **Kyllä** | En |
| Nimiketunnus | ITMLine.ShipItemId | Nvarchar(20) | En | En |
| Mittaus | ITMLine.ShipMeasurement | Nvarchar(20) | En | En |
| Mittayksikkö | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | En | En |
| Laatikoiden määrä | ITMLine.ShipNoOfCartons | Int | En | En |
| Positio | ITMLine.ShipPosition | Numeric(32, 6) | En | En |
| Määrä | ITMLine.ShipQty | Int | En | En |
| Siirtorivin numero | ITMLine.TransferLineNumber | Numeric(32, 6) | **Kyllä** | En |
| Siirtotilauksen numero | ITMLine.TransRefId | Numeric(32, 6) | **Kyllä** | En |
| Yksikkö | ITMLine.UnitId | Int | En | En |
| Äänenvoimakkuus | ITMLine.Volume | Nvarchar(10) | En | En |
| Paino | ITMLine.Weight | Numeric(32, 6) | En | En |

### <a name="reference-table"></a>Viitetaulu

Matkarivit luodaan liitoksen kautta avoimen saapuvan tilausrivin kanssa. Tämä rivi voi olla ostotilauksessa tai se voi olla vastaanottotapahtuma siirtotilauksessa. `RefTableId`-kenttä matkarivitaulukossa (`ITMLine`) viittaa taulukkonumeroon ja siten määrittää, mihin tilaustyyppiin rivi liittyy. Jos tiettyihin taulukkonumeroihin viitataan taulukossa, jossa tietoja luodaan, yksiköt jaetaan kyseisten arvojen perusteella.

Viitetaulukon (`RefTableId`) arvot ja tapahtuman tyyppi (`TransType`) ovat implisiittisiä joko aiheutuneiden kustannusten ostoriviyksikön tai aiheutuneiden kustannusten siirtoriviyksikön valinnassa.

### <a name="validation"></a>Tarkistus

Matkarivi viittaa suoraan matkatietueeseen, lähetyskonttitietueeseen tai pakkaustietueeseen. Jos ostoriviyksikköä (`ITMPurchaseLinesEntity`) tai siirtoriviyksikköä (`ITMPurchaseLinesEntity`) käytetään riippumattomasti yksiköistä, joita käytetään näiden viitetietueiden luontiin, **Matkan tunnus** (`ShipId`)-, **Lähetyskontti**- (`ShipContainerId`) ja **Pakkaus**- (`ShipFolioId`) arvojen on vastattava aiemmin luotua tietuetta vastaavissa taulukoissa. Muussa tapauksessa tuonti epäonnistuu.

Jos jompaakumpaa riviyksikköä käytetään saman tuonti-istunnon osana, kyseisten muiden yksikköjen on oltava matkarivin luonnin edellä. Muussa tapauksessa arvoja ei voi vahvistaa onnistuneesti. Jos matkan tai pakkauksen numerolle käytetään paikkamerkkiarvoa, liitos voidaan luoda vain, jos samaa paikkamerkkiä käytetään matkan tai pakkauksen numerolle matkariviyksikössä.

Jos ostotilaus- tai siirtotilausrivi on jo liitetty aiemmin luotuun riviin, uutta matkariviä ei luoda. Ennen kuin tilausrivi voidaan määrittää uudelle matkalle, se on poistettava nykyisestä matkastaan.

### <a name="order-line-identification"></a>Tilausrivin tunnus

Matkarivit viittaavat suoraan arvoihin **Tietueen tunnus** (`RefRecId`), **Varastodimension tunnus** (`InventDimId`) ja **Varastotapahtuman tunnus** (`InventTransId`). Näitä arvoja ei enää tarvitse sisällyttää, kun tietoyksikköä käytetään. Sen sijaan tilausrivin numero on nyt sisällytettävä. Yhdessä tilausrivin numero ja tilausnumero mahdollistavat kunkin viitearvon tunnistamisen.

### <a name="voyage-line-quantity"></a>Matkarivin määrä

Koska matkarivi on liitetty tilausriviin suoraan, yksikköä käyttämällä syötettävä **Määrä** (`ShipQty`)-arvo vaatii, että arvot vastaavat toisiaan. Vahvistus suoritetaan joko ostotilausrivin tai siirtorivin määrän mukaan. Jos vahvistus epäonnistuu, tietuetta ei käsitellä.

### <a name="calculated-fields"></a>Lasketut kentät

Lasketut kentät **Paino** ja **Tilavuus** hyväksyvät arvot, jotka vastaanotetaan tietoyksikön kautta. Jos arvoja ei ole annettu, järjestelmäarvoja käytetään näiden kenttien päivittämiseen, jos järjestelmäarvot ovat käytettävissä. Aiheutuneiden kustannusten osalta arvot lasketaan seuraavasti:

- *Paino* = *Määrä* × *Nimikkeen bruttopaino*
- *Tilavuus* = *Määrä* × (*Nimikkeen bruttosyvyys* × *Nimikkeen bruttokorkeus* × *Nimikkeen bruttoleveys*)

## <a name="sequencing"></a>Järjestys

Taulujen välisten riippuvuuksien vuoksi matkatietue on luotava ensin. Matkarivin voi luoda vasta sitten, kun matka, lähetyskontti ja pakkaukset on luotu.

Jos haluat luoda matkan ilman vahvistusvaroituksia, järjestelmän on käsiteltävä yksiköt seuraavassa järjestyksessä:

1. Matkat (`ITMTableEntity`)
1. Lähetyskontit (`ITMContainersEntity`)
1. Pakkaukset (`ITMFolioTableEntity`)
1. Matkarivit (`ITMPurchaseLinesEntity` tai `ITMTransferLinesEntity`)
