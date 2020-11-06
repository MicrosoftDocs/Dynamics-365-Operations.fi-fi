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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997549"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="4a53c-103">Toimittajan mallien välillä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="4a53c-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="4a53c-104">Toimittajatietojen virta</span><span class="sxs-lookup"><span data-stu-id="4a53c-104">Vendor data flow</span></span> 

<span data-ttu-id="4a53c-105">Jos päätät käyttää **Tili** -yksikköä, kun haluat tallentaa **Organisaatio** -tyypin ja **Yhteyshenkilö** -yksikön **Henkilö** -tyypin myymälätoimittajia, määritä seuraavat työnkulut.</span><span class="sxs-lookup"><span data-stu-id="4a53c-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="4a53c-106">Muussa tapauksessa tätä kokoonpanoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="4a53c-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="4a53c-107">Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="4a53c-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="4a53c-108">**Dynamics365FinanceExtended** -ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="4a53c-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4a53c-109">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="4a53c-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4a53c-110">Toimittajien luonti Tilit-yksikössä</span><span class="sxs-lookup"><span data-stu-id="4a53c-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="4a53c-111">Toimittajien luonti toimittajat-yksikössä</span><span class="sxs-lookup"><span data-stu-id="4a53c-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="4a53c-112">Toimittajien päivittäminen Tilit-yksikössä</span><span class="sxs-lookup"><span data-stu-id="4a53c-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="4a53c-113">Toimittajien päivittäminen toimittajat-yksikössä</span><span class="sxs-lookup"><span data-stu-id="4a53c-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="4a53c-114">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="4a53c-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4a53c-115">Luo uusi työnkulkuprosessi **Toimittaja** -yksikölle ja valitse **Luo toimittajia tiliyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="4a53c-116">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-116">Then select **OK**.</span></span> <span data-ttu-id="4a53c-117">Tämä työnkulku käsittelee **Tilli** -yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="4a53c-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Toimittajien luonti Tilit-yksikön työnkulkuprosessissa](media/create_process.png)

2. <span data-ttu-id="4a53c-119">Luo uusi työnkulkuprosessi **Toimittaja** -yksikölle ja valitse **Päivitä toimittajia tiliyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="4a53c-120">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-120">Then select **OK**.</span></span> <span data-ttu-id="4a53c-121">Tämä työnkulku käsittelee **Tilli** -yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="4a53c-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="4a53c-122">Luo uusi työnkulkuprosessi **Tili** -yksikölle ja valitse **Luo toimittajia toimittajayksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="4a53c-123">Luo uusi työnkulkuprosessi **Tili** -yksikölle ja valitse **Päivitä toimittajia toimittajayksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="4a53c-124">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="4a53c-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4a53c-125">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. <span data-ttu-id="4a53c-127">Aktivoi **Tili** - ja **Toimittaja** -yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Tili** -yksikköä **Organisaatio** -tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="4a53c-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="4a53c-128">Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="4a53c-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="4a53c-129">**Dynamics365FinanceExtended** -ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="4a53c-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4a53c-130">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="4a53c-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4a53c-131">Luo henkilötyyppisiä toimittajia toimittajayksikköön</span><span class="sxs-lookup"><span data-stu-id="4a53c-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="4a53c-132">Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikköön</span><span class="sxs-lookup"><span data-stu-id="4a53c-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="4a53c-133">Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikköön</span><span class="sxs-lookup"><span data-stu-id="4a53c-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="4a53c-134">Päivitä henkilötyyppisiä toimittajia toimittajayksikköön</span><span class="sxs-lookup"><span data-stu-id="4a53c-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="4a53c-135">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="4a53c-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4a53c-136">Luo uusi työnkulkuprosessi **Toimittaja** -yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="4a53c-137">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-137">Then select **OK**.</span></span> <span data-ttu-id="4a53c-138">Tämä työnkulku käsittelee **Yhteyshenkilö** -yksikön toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="4a53c-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="4a53c-139">Luo uusi työnkulkuprosessi **Toimittaja** -yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="4a53c-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-140">Then select **OK**.</span></span> <span data-ttu-id="4a53c-141">Tämä työnkulku käsittelee **Yhteyshenkilö** -yksikön toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="4a53c-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="4a53c-142">Luo uusi työnkulkuprosessi **Yhteyshenkilö** -yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="4a53c-143">Luo uusi työnkulkuprosessi **Yhteyshenkilö** -yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="4a53c-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="4a53c-144">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="4a53c-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4a53c-145">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="4a53c-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="4a53c-146">Aktivoi **Yhteyshenkilö** - ja **Toimittaja** -yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö** -yksikköä **Henkilö** -tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="4a53c-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
