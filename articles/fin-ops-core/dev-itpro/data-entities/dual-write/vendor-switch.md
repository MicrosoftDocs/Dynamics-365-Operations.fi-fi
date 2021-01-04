---
title: Toimittajan mallien välillä siirtyminen
description: Tässä aiheessa käsitellään kuinka vaihtaa toimittajan tietojen integrointia Finance and Operations -sovellusten ja Dataversen välillä.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685506"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="ec930-103">Toimittajan mallien välillä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="ec930-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="ec930-104">Toimittajatietojen virta</span><span class="sxs-lookup"><span data-stu-id="ec930-104">Vendor data flow</span></span> 

<span data-ttu-id="ec930-105">Jos päätät käyttää **Tili**-yksikköä, kun haluat tallentaa **Organisaatio**-tyypin ja **Yhteyshenkilö**-yksikön **Henkilö**-tyypin myymälätoimittajia, määritä seuraavat työnkulut.</span><span class="sxs-lookup"><span data-stu-id="ec930-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="ec930-106">Muussa tapauksessa tätä kokoonpanoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="ec930-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="ec930-107">Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="ec930-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="ec930-108">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="ec930-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="ec930-109">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="ec930-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="ec930-110">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="ec930-111">Toimittajien luonti Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="ec930-112">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="ec930-113">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="ec930-114">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="ec930-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="ec930-115">Luo uusi työnkulkuprosessi **Toimittaja**-entiteetille ja valitse **Luo toimittajia Tilit-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="ec930-116">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec930-116">Then select **OK**.</span></span> <span data-ttu-id="ec930-117">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="ec930-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Toimittajien luonti Tilit-taulun työnkulkuprosessissa](media/create_process.png)

2. <span data-ttu-id="ec930-119">Luo uusi työnkulkuprosessi **Toimittaja**-entiteetille ja valitse **Päivitä toimittajia Tilit-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="ec930-120">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec930-120">Then select **OK**.</span></span> <span data-ttu-id="ec930-121">Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="ec930-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="ec930-122">Luo uusi työnkulkuprosessi **Tili**-entiteetille ja valitse **Luo toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="ec930-123">Luo uusi työnkulkuprosessi **Tili**-entiteetille ja valitse **Päivitä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="ec930-124">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="ec930-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="ec930-125">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="ec930-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. <span data-ttu-id="ec930-127">Aktivoi **Tili**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Tili**-entiteettiä **Organisaatio**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="ec930-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="ec930-128">Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="ec930-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="ec930-129">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="ec930-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="ec930-130">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="ec930-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="ec930-131">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="ec930-132">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="ec930-133">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="ec930-134">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="ec930-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="ec930-135">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="ec930-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="ec930-136">Luo uusi työnkulkuprosessi **Toimittaja**-entiteetille ja valitse **Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="ec930-137">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec930-137">Then select **OK**.</span></span> <span data-ttu-id="ec930-138">Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="ec930-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="ec930-139">Luo uusi työnkulkuprosessi **Toimittaja**-entiteetille ja valitse **Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="ec930-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec930-140">Then select **OK**.</span></span> <span data-ttu-id="ec930-141">Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="ec930-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="ec930-142">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Luo henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="ec930-143">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="ec930-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="ec930-144">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="ec930-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="ec930-145">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="ec930-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="ec930-146">Aktivoi **Yhteyshenkilö**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö**-entiteettiä **Henkilö**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="ec930-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
