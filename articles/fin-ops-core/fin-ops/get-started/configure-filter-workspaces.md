---
title: Määritä työtiloja ja suodata niitä
description: Tämä artikkeli sisältää työtilojen määrittämisen ja suodattamisen yleiskuvauksen.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace, HcmBenefitWorkspace, BudgetPlanningWorkspace, BusinessProcessGenericWorkspace, RetailCatalogManagementWorkspace, RetailCategoryAndProductWorkspace, RetailChannelManagementWorkspace, HcmCompensationWorkspace, CAMCostAccountingLedgerAdminWorkspace, CostAdminWorkspace, CostAnalysisWorkspace, CAMCostControlWorkspace, CustomerCollectionManagerWorkspace, CustomerInvoiceWorkspace, CustPaymentWorkspace, DataManagementWorkspace, DataValidationWorkspace, ERWorkspace, LedgerPeriodCloseProjectWorkspace, AssetWorkspace, GeneralJournalEntryWorkspace, VendVendorPortalInvoiceWorkspace, BudgetTrackingWorkspace, ReqCreatePlanWorkspace, BusinessProcessGenericOwnerWorkspace, SelfHealingWorkspace, WHSOutboundWorkMonitoringWorkspace, WHSWavePlanningWorkspace, PayrollWorkspace, HcmWorkforceWorkspace, RetailDiscountPricingWorkspace, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, EcoResProductVariantMaintainWorkspace, JmgShopSupervisorWorkspace, ProjProjectManagementWorkspace, VendVendorPortalWorkspace, PurchOrderMaintainWorkspace, PurchOrderProcessReceiptsWorkspace, HcmRecruitmentWorkspace, EcoResProductMaintainWorkspace, FMClerkWorkspace, OpResLifecycleManagementWorkspace, RetailITWorkspace, RetailChannelOperationsWorkspace, RetailStoreManagementWorkspace, SalesOrderProcessingWorkspace, SalesReturnWorkspace, SystemAdministrationWorkspaceForm, VendVendorRequestForQuotationsWorkspace, VendVendorProfileManagementWorkspace, VendInvoiceWorkspace, VendPaymentWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 974980e1633e3f909b7c73964e811c351a042a7b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191198"
---
# <a name="configure-and-filter-workspaces"></a>Määritä työtiloja ja suodata niitä

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää työtilojen määrittämisen ja suodattamisen yleiskuvauksen.

## <a name="configuring-a-workspace"></a>Työtilan määrittäminen

Voit muuttaa joidenkin työtilojen ulkoasua ja toimintaa päivittämällä koko työtilaa koskevat asetukset. Kun työtilaa voi määrittää, toimintoruudussa on painike, jonka avulla määrityksiä voi muuttaa. Esimerkiksi seuraavassa kuvassa painikkeen nimeksi on annettu **Määritä oma työtila**.

[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)

Kun napsautat painiketta, voit muokata avautuvassa valintaikkunassa työtilan ennalta määritettyjä asetuksia. Valintaikkunassa olevat erikoisasetukset vaihtelevat työtilan mukaan. Ne riippuvat työtilan erityisistä ohjausobjekteista ja liiketoimintatiedoista.

[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)

## <a name="filtering-a-workspace"></a>Työtilan suodattaminen

Useiden työtilojen sisältöä voi suodattaa. Käytettävissä olevien ohjausobjektien avulla voi suodattaa kaiken sisällön tai vain tietyn osan sisällön työtilassa. Työtilojen suodattimet voivat olla valintoja, yhdistelmäruutuja, vapaatekstikenttiä tai muita ohjausobjekteja. Jokaisella suodattimella on kuitenkin samat vaikutukset seuraavissa osissa esitetyllä tavalla.

### <a name="workspace-wide-filters"></a>Työtilakohtaiset suodattimet

Voit suodattaa koko työtilan työtilakohtaisen suodattimen avulla. Työtilakohtainen suodatin löytyy työtilan vasemmasta yläkulmasta. Kun avattavasta luettelosta valitaan arvo, työtilan sisältö suodatetaan valinnan mukaan.

[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)

Kun avaat suodattimen, esiin tulee useita vaihtoehtoja.

[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)

Valitse asetus, jonka perusteella työtila suodatetaan.

### <a name="workspace-section-filters"></a>Työtilan osan suodattimet

Jos työtilan yksittäisillä osilla on suodattimia, voit suodattaa kunkin osan erikseen. Seuraavassa kuvassa suodatin (kenttä, jossa lukee Suodatin) on esimerkki vapaatekstikentän suodattimesta.

[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)

Suodata osan sisältö valitsemalla tai antamalla arvo samalla tavalla kuin työtilakohtaisessa suodattimessa.
