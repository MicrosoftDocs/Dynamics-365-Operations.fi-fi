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
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744462"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="94e60-103">Toimittajan mallien välillä siirtyminen</span><span class="sxs-lookup"><span data-stu-id="94e60-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="94e60-104">Toimittajatietojen virta</span><span class="sxs-lookup"><span data-stu-id="94e60-104">Vendor data flow</span></span> 

<span data-ttu-id="94e60-105">Jos päätät käyttää **Tili**-taulua, kun haluat tallentaa **Organisaatio**-tyypin ja **Yhteyshenkilö**-taulun **Henkilö**-tyypin myymälätoimittajia, määritä seuraavat työnkulut.</span><span class="sxs-lookup"><span data-stu-id="94e60-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="94e60-106">Muussa tapauksessa tätä kokoonpanoa ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="94e60-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="94e60-107">Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="94e60-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="94e60-108">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="94e60-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="94e60-109">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="94e60-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="94e60-110">Toimittajien luonti Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="94e60-111">Toimittajien luonti Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="94e60-112">Toimittajien päivitys Tilit-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="94e60-113">Toimittajien päivitys Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="94e60-114">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="94e60-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="94e60-115">Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Luo toimittajia Tilit-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="94e60-116">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e60-116">Then select **OK**.</span></span> <span data-ttu-id="94e60-117">Tämä työnkulku käsittelee **Tilli**-taulun toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="94e60-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Toimittajien luonti Tilit-taulun työnkulkuprosessissa](media/create_process.png)

2. <span data-ttu-id="94e60-119">Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Päivitä toimittajia Tilit-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="94e60-120">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e60-120">Then select **OK**.</span></span> <span data-ttu-id="94e60-121">Tämä työnkulku käsittelee **Tili**-taulun toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="94e60-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="94e60-122">Luo uusi työnkulkuprosessi **Tili**-taululle ja valitse **Luo toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="94e60-123">Luo uusi työnkulkuprosessi **Tili**-taululle ja valitse **Päivitä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="94e60-124">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="94e60-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="94e60-125">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="94e60-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. <span data-ttu-id="94e60-127">Aktivoi **Tili**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Tili**-taulua **Organisaatio**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="94e60-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="94e60-128">Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille</span><span class="sxs-lookup"><span data-stu-id="94e60-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="94e60-129">**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit.</span><span class="sxs-lookup"><span data-stu-id="94e60-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="94e60-130">Kullekin mallille luodaan työnkulku.</span><span class="sxs-lookup"><span data-stu-id="94e60-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="94e60-131">Luo henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="94e60-132">Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="94e60-133">Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="94e60-134">Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa</span><span class="sxs-lookup"><span data-stu-id="94e60-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="94e60-135">Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:</span><span class="sxs-lookup"><span data-stu-id="94e60-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="94e60-136">Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="94e60-137">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e60-137">Then select **OK**.</span></span> <span data-ttu-id="94e60-138">Tämä työnkulku käsittelee **Yhteyshenkilö**-taulun toimittajan luontiskenaarion.</span><span class="sxs-lookup"><span data-stu-id="94e60-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="94e60-139">Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="94e60-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="94e60-140">Then select **OK**.</span></span> <span data-ttu-id="94e60-141">Tämä työnkulku käsittelee **Yhteyshenkilö**-taulun toimittajan päivitysskenaarion.</span><span class="sxs-lookup"><span data-stu-id="94e60-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="94e60-142">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-taululle ja valitse **Luo henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="94e60-143">Luo uusi työnkulkuprosessi **Yhteyshenkilö**-taululle ja valitse **Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.</span><span class="sxs-lookup"><span data-stu-id="94e60-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="94e60-144">Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi.</span><span class="sxs-lookup"><span data-stu-id="94e60-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="94e60-145">Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.</span><span class="sxs-lookup"><span data-stu-id="94e60-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="94e60-146">Aktivoi **Yhteyshenkilö**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö**-taulua **Henkilö**-tyyppisten toimittajien tietojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="94e60-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
