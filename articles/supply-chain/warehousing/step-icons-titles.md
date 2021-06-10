---
title: Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen
description: Tässä aiheessa kuvataan, miten määritetään Warehouse Managementin mobiilisovelluksen uusien tai mukautettujen tehtävävirtojen vaihekuvakkeet ja otsikot.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049361"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten määritetään Warehouse Managementin mobiilisovelluksen uusien tai mukautettujen tehtävävirtojen vaihekuvakkeet ja vaiheiden otsikot.

Seuraavissa kuvissa näytetään, miten vaihekuvakkeet ja otsikot näkyvät Warehouse Management -mobiilisovelluksessa.

![Esimerkki vaihekuvakkeesta ja vaiheen otsikosta Warehouse Management -mobiilisovelluksessa](media/step-icon-example.png "Esimerkki vaihekuvakkeesta ja vaiheen otsikosta Warehouse Management -mobiilisovelluksessa")

## <a name="turn-on-this-feature-in-your-system"></a>Tämän toiminnon ottaminen käyttöön järjestelmässä

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat tarkistaa toiminnon tilan ja ottaa sen käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetusten avulla. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Uuden varastointisovelluksen käyttäjäasetukset, kuvakkeet ja vaiheiden otsikot*

## <a name="standard-step-ids-classes-and-icons"></a>Vakiovaihetunnukset, -luokat ja -kuvakkeet

Jokainen tehtävätyönkulun vaihe on määritetty vaiheen tunnuksen perusteella, ja kullakin vaiheen tunnuksella on vastaava vaiheluokka. Vaihekuvake ja otsikko määritetään jokaisessa vaiheen luokassa.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Vaihetunnukset ja vaiheluokat

Seuraavassa taulukossa luetellaan kaikki käytettävissä olevat vaihetunnukset, ja vaiheluokka on sitä vastaava. Ensisijaisen syöttökentän ohjausobjektin nimeä käytetään vaiheen tunnuksena.

Katso esimerkki `WHSMobileAppStepInfoBuilder.stepId()` -menetelmän toteutuksesta, joka osoittaa, kuinka näitä vaihetunnuksia ja luokkia käytetään on kohdassa [Esimerkki: Vaihekuvakkeiden ja otsikoiden määrittäminen muokatulle työnkululle](#example) jäljempänä tässä ohjeaiheessa.

| Vaihetunnus | Vaiheluokka |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Rahdinkuljettaja | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Vahvistus | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Käsittely | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Tilausnumero | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Vaikuttavuus | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Määritä | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Määrä | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Paino | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Käytettävissä olevat vaiheen kuvakkeet

Järjestelmä sisältää kokoelman vakiovaihekuvakkeita, joita voit käyttää myös mukautetuissa vaiheissasi. Et voi ladata mukautettuja vaihekuvakkeita palvelimeen. Siksi sinun on aina valittava jokin vakiovaihekuvakkeista.

Seuraavassa taulukossa näkyvät kaikki käytettävissä olevat vakiovaihekuvakkeet ja niiden nimet.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Tietoja vaihekuvakkeesta"><br>Tietoja</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Käyttöoikeussopimuksen tai nimikevaihekuvakkeen lisääminen"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Erän käsittelyvaihe -kuvake"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Rahdinkuljettajan vaiheen kuvake"><br>Rahdinkuljettaja</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Todellisen painon tunnisteen vaiheen kuvake"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Todellisen painon tunnisteen painovaiheen kuvake"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Tarkistusnumerovaihe-kuvake"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Sisään- tai uloskäyntitunnuksen vaiheen kuvake"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alikäyttöoikeusvaihekuvake"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klusterin tunnus -vaiheen kuvake"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klusterin sijainti -vaiheen kuvake"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Määritteen tunnus -vaiheen kuvake"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Määritetty kentän vaiheen kuvake"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con- tai LP-vaihekuvake"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidoi lisenssikäyttöoikeuksien tunnuksen vaiheen kuvake"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidoi lisenssikäyttöoikeustunnuksen vaihekuvakkeeseen"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konttityypin vaiheen kuvake"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Inventointivaihe-kuvake"><br>Inventointi</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventoinnin syykoodin vaiheen kuvake"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Alkuperämaakoodin vaiheen kuvake"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Käsittelyvaihe-kuvake"><br>Käsittely</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Valmis vaihe -kuvake"><br>Valmis</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Ohjaimen vahvistusvaihe -kuvake"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Kuljettajan sisäänkäyntitunnuksen vaiheen kuvake"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Kuljettajan uloskäyntitunnuksen vaiheen kuvake"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Vanhenemispäivän vaiheen kuvake"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Kentän vaiheen kuvake"><br>Kenttä</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Erästä käsittelyvaiheen kuvake"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Varastosta tilan vaiheen kuvake"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Määritystunnus -vaiheen kuvake"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Varastoerän tunnuksen vaiheen kuvake"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Varastovärin tunnuksen vaiheen kuvake"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Varastosijainnin tunnuksen vaiheen kuvake"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Varastosarjan tunnuksen vaiheen kuvake"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Varastokoon tunnuksen vaiheen kuvake"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Varastotilan tunnuksen vaiheen kuvake"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Varastotyylin tunnuksen vaiheen kuvake"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Varastoversion tunnuksen vaiheen kuvake"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Nimikkeen tunnus -vaiheen kuvake"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM-konttitunnuksen vaiheen kuvake"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM-lähetystunnuksen vaiheen kuvake"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-kortin tunnus -vaiheen kuvake"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban- tai kortin tunnus -vaiheen kuvake"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Käyttöoikeustunnuksen vaiheen kuvake"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Lataa tunnus -vaiheen kuvake"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Toimipaikan rekisterikilpien paikan vaiheen kuvake"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Sijainti- tai käyttöoikeussopimuksen vaiheen kuvakkeen lisääminen"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Sijainti- tai käyttöoikeussopimuksen tarkistusvaiheen kuvake"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Sijainti- tai käyttöoikeussopimuksen lomakevaiheesta kuvake"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Sijainti- tai käyttöoikeussopimuksen vaiheeseen kuvakkeen lisääminen"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Pitkä prosessi valmis -vaiheen kuvake"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-tauon pää-LP-vaiheen kuvake"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Yhdistä konttitunnuksen vaiheen kuvake"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Sekalaisen käyttöoikeusnumerorivin vaiheen kuvake"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Lähtevän painon vaiheen kuvake"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Omistajavaihe-kuvake"><br>Omistaja</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pääkäyttöoikeusvaihekuvake"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Vahvista vaiheen kuvake"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ostotilausrivin numeron vaiheen kuvake"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ostotilauksen numeron vaiheen kuvake"><br>Tilausnumero</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Sijainti täynnä -vaiheen kuvake"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Vaikuttavuusvaihe-kuvake"><br>Vaikuttavuus</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Tulostimen nimen vaiheen kuvake"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Tuotteen tunnus -vaiheen kuvake"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Tuotevahvistusvaihe-kuvake"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Pitovaiheen kuvake"><br>Määritä</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Pois laitettavan klusterin tunnus -vaiheen kuvake"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Määrävaihekuvake"><br>Määrä</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Määrän oikaisemisvaiheen kuvake"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Määrä vähissä -vaiheen kuvake"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Kulutettavan määrän vaiheen kuvake"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Pidettävän määrän vaiheen kuvake"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Hävikkimäärän vaiheen kuvake"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Määrän vahvistuksen vaihe -kuvake"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ilmoita valmiiksi -työn vaiheen kuvake"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Vastaanottosijainnin tunnus -vaiheen kuvake"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Poista konttitunnuksen vaiheen kuvake"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA-numeron vaiheen kuvake"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Valitse tilaus -vaiheen kuvake"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Lyhyen poiminnan syyvaihe -kuvake"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Sijaintitunnuksen vaiheen lajittelukuvake"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Kohdekäyttöoikeustunnuksen vaiheen kuvake"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Rivinumeroon -vaiheen kuvake"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Sijaintiin -vaiheen kuvake"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numeroon -vaiheen kuvake"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Varastoon -vaiheen kuvake"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Välitä kuormatunnus -vaiheen kuvake"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Toimittajaerän tunnuksen vaiheen kuvake"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Aallon nimiketunnuksen vaiheen kuvake"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Aallon nimikemäärän vaiheen kuvake"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Painon vaiheen kuvake"><br>Paino</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Kulutettavan painon vaiheen kuvake"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS-oikaisutyypin vaiheen kuvake"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS-vastaanottopoikkeusvaiheen kuvake"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS-sijainnin tunnus -vaiheen kuvake"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Työn tunnus -vaiheen kuvake"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Työtunnus, kun haluat peruuttaa vaiheen kuvakkeen"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Työn käyttöoikeustunnuksen vaiheen kuvake"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Työn käyttöoikeustunnuksen säilytettävän klusterin vaiheen kuvake"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Työpoolin tunnus -vaiheen kuvake"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Vyöhyketunnus -vaiheen kuvake"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Esimerkki: Mukautetun työnkulun vaihekuvakkeiden ja otsikoiden liittäminen

Tässä esimerkissä kerrotaan, miten mukautetun tehtävän työnkulun vaihekuvakkeet ja otsikot määritetään. Skenaario perustuu esimerkkiin mukautetusta tehtävätyönkulusta, joka esitellään ja johon voi tutustua tarkemmin seuraavassa kirjauksen esimerkissä: [Warehouse Mobile App -sovelluksen mukauttaminen](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Tehtävätyönkulku toimii seuraavasti:

1. Sovellus näyttää sivun, joka kehottaa työntekijää antamaan säilötunnuksen (esimerkiksi skannaamalla viivakoodi).
1. Jos säilön tunnus on kelvollinen, sovellus avaa uuden sivun, joka kysyy työntekijältä painoa. (Jos säilön tunnus ei kelpaa, työntekijä palautetaan ensimmäiselle sivulle.)
1. Kun työntekijä määrittää kelvollisen painon, järjestelmä tallentaa painon ja palauttaa työntekijän ensimmäiselle sivulle.

Seuraavassa kuvassa näkyy tämä tehtävätyönkulku.

![Tehtävän työnkulkukaavio](media/step-icons-example-task-flow.png "Tehtävän työnkulkukaavio")

### <a name="create-a-step-class-for-the-container-input-page"></a>Vaiheluokan luominen säilön syöttösivulle

Säilön syöttösivun avulla työntekijä voi skannata tai määrittää säilön tunnuksen.

![Säilön syöttösivu](media/step-icons-example-container-input.png "Säilön syöttösivu")

Säilön syöttö -sivulla syöttökentän ohjausobjektinimi on `ContainerId`. Koska tätä ohjausobjektin nimeä ei ole [vaihetunnusten luettelossa](#step-ids-classes), siihen perustuvaa vaihetta ei etsitä. Siksi sinun on luotava vaiheluokka, joka edustaa vaihetta. Esimerkki:

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Vaiheen kuvakkeen tunnus tallennetaan `defaultStepIcon`-luokan jäseneksi ja vaiheen otsikko tallennetaan `defaultStepTitle`-luokan jäseneksi.

Jos haluat määrittää vaihekuvakkeen, aseta `defaultStepIcon` jollekin kuvaketunnukselle, joita on lueteltu aiemmin tässä ohjeaiheessa olevassa [Käytettävissä olevan vaiheen kuvakkeet](#step-icons) -osassa.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Painosyötön vakiokuvakkeen tai mukautetun vaiheen kuvakkeen ja otsikon käyttö

Painon syöttö -sivulla työntekijä voi määrittää painon.

![Painon syöttösivu](media/step-icons-example-weight-input.png "Painon syöttösivu")

Painon syöttösivulla syöttökentän ohjausobjektinimi on `Weight`, joka on [vaihetunnusten luettelossa](#step-ids-classes). Jos voit hyväksyä `WHSMobileAppStepWeight`-luokassa määritetyn vaihekuvakkeen ja otsikon, sinun ei tarvitse muuttaa mitään tätä vaihetta varten.

Jos kuitenkin haluat käyttää tässä vaiheessa toista kuvaketta tai otsikkoa, voit ohittaa joko builder-luokan `stepId()`-menetelmän tai `stepInfo()`-menetelmän. Jokaisella tehtävätyönkululla on oma vaiheen tiedon muodostin.

#### <a name="override-the-stepid-method"></a>StepId()-menetelmän ohittaminen

Seuraavassa esimerkissä näkyy yksi tapa, jolla voit muokata muodostinluokkaa ohitamalla `stepId()`-menetelmän.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Sen jälkeen luot vaiheluokan `NewWeight`-vaiheelle. Koodin pitäisi muistuttaa aiemmin tässä ohjeaiheessa näkyvää `ContainerId`-esimerkkiä.

#### <a name="override-the-stepinfo-method"></a>StepInfo()-menetelmän ohittaminen

Seuraavassa esimerkissä näkyy yksi tapa, jolla voit muokata muodostinluokkaa ohitamalla `stepInfo()`-menetelmän.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Sen jälkeen voit luoda `WHSMobileAppStepInfo`-objektin ja määrittää kuvakkeen ja/tai otsikon suoraan.

## <a name="additional-resources"></a>Lisäresurssit

- [Varastonhallinnan mobiilisovelluksen asentaminen ja yhteyden muodostaminen](install-configure-warehouse-management-app.md)
- [Mobiililaitteen käyttäjäasetukset](mobile-device-user-settings.md)
