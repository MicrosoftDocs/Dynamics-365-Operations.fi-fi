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
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173036"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="2b2ea-103">Toimittajan mallien välillä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="2b2ea-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="2b2ea-104">Toimittajatietojen virta</span><span class="sxs-lookup"><span data-stu-id="2b2ea-104">Vendor data flow</span></span> 

<span data-ttu-id="2b2ea-105">Jos päätät käyttää **Tili**-yksikköä, kun haluat tallentaa **Organisaatio**-tyypin ja **Yhteyshenkilö**-yksikön **Henkilö**-tyypin myymälätoimittajia, määritä seuraavat työnkulut.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="2b2ea-106">Muussa tapauksessa tätä kokoonpanoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="2b2ea-107">Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="2b2ea-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="2b2ea-108">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2b2ea-109">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2b2ea-110">Toimittajien luonti Tilit-yksikössä</span><span class="sxs-lookup"><span data-stu-id="2b2ea-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2b2ea-111">Toimittajien luonti toimittajat-yksikössä</span><span class="sxs-lookup"><span data-stu-id="2b2ea-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="2b2ea-112">Toimittajien päivittäminen Tilit-yksikössä</span><span class="sxs-lookup"><span data-stu-id="2b2ea-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2b2ea-113">Toimittajien päivittäminen toimittajat-yksikössä</span><span class="sxs-lookup"><span data-stu-id="2b2ea-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="2b2ea-114">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="2b2ea-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2b2ea-115">Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Luo toimittajia tiliyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2b2ea-116">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-116">Then select **OK**.</span></span> <span data-ttu-id="2b2ea-117">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Toimittajien luonti Tilit-yksikön työnkulkuprosessissa](media/create_process.png)

2. <span data-ttu-id="2b2ea-119">Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Päivitä toimittajia tiliyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2b2ea-120">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-120">Then select **OK**.</span></span> <span data-ttu-id="2b2ea-121">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="2b2ea-122">Luo uusi työnkulkuprosessi **Tili**-yksikölle ja valitse **Luo toimittajia toimittajayksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="2b2ea-123">Luo uusi työnkulkuprosessi **Tili**-yksikölle ja valitse **Päivitä toimittajia toimittajayksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="2b2ea-124">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2b2ea-125">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. <span data-ttu-id="2b2ea-127">Aktivoi **Tili**- ja **Toimittaja**-yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Tili**-yksikköä **Organisaatio**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="2b2ea-128">Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="2b2ea-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="2b2ea-129">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2b2ea-130">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2b2ea-131">Luo henkilötyyppisiä toimittajia toimittajayksikköön</span><span class="sxs-lookup"><span data-stu-id="2b2ea-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="2b2ea-132">Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikköön</span><span class="sxs-lookup"><span data-stu-id="2b2ea-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2b2ea-133">Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikköön</span><span class="sxs-lookup"><span data-stu-id="2b2ea-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2b2ea-134">Päivitä henkilötyyppisiä toimittajia toimittajayksikköön</span><span class="sxs-lookup"><span data-stu-id="2b2ea-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="2b2ea-135">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="2b2ea-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2b2ea-136">Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2b2ea-137">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-137">Then select **OK**.</span></span> <span data-ttu-id="2b2ea-138">Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="2b2ea-139">Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2b2ea-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-140">Then select **OK**.</span></span> <span data-ttu-id="2b2ea-141">Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="2b2ea-142">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="2b2ea-143">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="2b2ea-144">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2b2ea-145">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="2b2ea-146">Aktivoi **Yhteyshenkilö**- ja **Toimittaja**-yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö**-yksikköä **Henkilö**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="2b2ea-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
