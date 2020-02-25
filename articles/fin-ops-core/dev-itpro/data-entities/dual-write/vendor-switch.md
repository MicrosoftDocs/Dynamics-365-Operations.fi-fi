---
title: Toimittajan mallien välillä siirtyminen
description: Tässä aiheessa käsitellään kuinka vaihtaa toimittajan tietojen integrointia Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019753"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="0c0fd-103">Toimittajan mallien välillä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="0c0fd-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="0c0fd-104">Toimittajatietojen virta</span><span class="sxs-lookup"><span data-stu-id="0c0fd-104">Vendor data flow</span></span> 

<span data-ttu-id="0c0fd-105">Jos käytät muita Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja haluat eristää toimittajan tiedot asiakastiedoista, käytä tätä perustoimittajarakennetta.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Toimittajan perustyönkulku](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="0c0fd-107">Jos käytät Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja jatkat toimittajan tietojen tallentamista **Tili**-yksikköön, käytä tätä uutta laajennettua toimittajarakennetta.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="0c0fd-108">Tässä rakenteessa laajennetut toimittajatiedot, kuten toimittajan pidossaolotila ja toimittajan profiili, tallennetaan **toimittajat**-yksikköön Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Laajennettu toimittajatyönkulku](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="0c0fd-110">Käytä laajennettua toimittajarakennetta seuraavien ohjeiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="0c0fd-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="0c0fd-111">**SupplyChainCommon**-ratkaisupaketti sisältää työnkulun prosessimallit, jotka näkyvät seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="0c0fd-112">![Työnkulun prosessimallit](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="0c0fd-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="0c0fd-113">Uusien työnkulkuprosessien luominen työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="0c0fd-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="0c0fd-114">Luo **Toimittaja**-yksikön uusi työnkulkuprosessi käyttämällä työnkulun **Luo toimittajia tiliyksikössä** -prosessimallia ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="0c0fd-115">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="0c0fd-116">![Toimittajien luonti Tili-yksikössä](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="0c0fd-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="0c0fd-117">Luo **Toimittaja**-yksikön uusi työnkulkuprosessi käyttämällä työnkulun **Päivitä tiliyksikkö** -prosessimallia ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="0c0fd-118">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="0c0fd-119">![Tiliyksikön päivittäminen](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="0c0fd-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="0c0fd-120">Luo uusia työnkulkuprosesseja **Tilit**-yksikössä luoduista malleista.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="0c0fd-121">![Toimittajien luonti toimittajat-yksikössä](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="0c0fd-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="0c0fd-122">![Toimittajat-yksikön päivittäminen](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="0c0fd-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="0c0fd-123">Voit määrittää työnkulut tarpeen mukaan reaaliaikaisiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="0c0fd-124">![Taustatyönkuluksi muuntaminen](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="0c0fd-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="0c0fd-125">Aktivoi **Tili**- ja **Toimittaja**-yksiköissä luodut työnkulut ja aloita **Tili**-yksikön käyttäminen toimittajatietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="0c0fd-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
