---
title: Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412037"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="26be5-103">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="26be5-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26be5-104">Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="26be5-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26be5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="26be5-105">Overview</span></span>

<span data-ttu-id="26be5-106">Dynamics 365 Commerce -sovelluksen tehtävienhallinnan avulla voit määrittää tehtäväluettelon useille myymälöille tai työntekijöille tai myymälöiden ja työntekijöiden yhdistelmille.</span><span class="sxs-lookup"><span data-stu-id="26be5-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="26be5-107">Esimerkiksi 20 myymälän aluepäällikkö voi haluta määrittää kaikille 20 myymälälle **Loma-ajan valmistelu** -tehtäväluettelon.</span><span class="sxs-lookup"><span data-stu-id="26be5-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="26be5-108">Tehtäväluettelon määritysprosessin käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="26be5-108">Start the task list assignment process</span></span>

<span data-ttu-id="26be5-109">Voit aloittaa tehtäväluettelon määrittämisen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="26be5-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="26be5-110">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="26be5-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="26be5-111">Valitse määritettävä tehtäväluettelo.</span><span class="sxs-lookup"><span data-stu-id="26be5-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="26be5-112">Valitse **Käynnistä prosessi**.</span><span class="sxs-lookup"><span data-stu-id="26be5-112">Select **Start process**.</span></span>
1. <span data-ttu-id="26be5-113">Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi (esimerkiksi **Itäisen alueen myymälät**).</span><span class="sxs-lookup"><span data-stu-id="26be5-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="26be5-114">Määritä **Tavoitepvm**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="26be5-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="26be5-115">Jos haluat määrittää myymälöille tehtäväluettelot, etsi ja valitse myymälät **Myymälät**-välilehden **Organisaatiohierarkia**-suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="26be5-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="26be5-116">Voit määrittää tehtäväluettelon työntekijöille etsimällä ja valitsemalla työntekijät **Työntekijät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="26be5-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="26be5-117">Käynnistä prosessi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="26be5-117">Select **OK** to start the process.</span></span> <span data-ttu-id="26be5-118">Tehtäväluettelo määritetään valituille myymälöille tai työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="26be5-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="26be5-119">Seuraavassa kuvassa on esimerkki siitä, miten myymälät etsitään ja valitaan **Käynnistä prosessi** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="26be5-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Myymälöiden etsiminen ja valitseminen Käynnistä prosessi -valintaikkunassa](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="26be5-121">Tehtäväluetteloiden määrittäminen toistuviksi</span><span class="sxs-lookup"><span data-stu-id="26be5-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="26be5-122">Vähittäiskauppiailla on joskus toistuvia tehtäviä, kuten torstain sulkemisen tarkistuslista tai kuukauden ensimmäisen päivän tarkistuslista.</span><span class="sxs-lookup"><span data-stu-id="26be5-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="26be5-123">Tämän vuoksi he saattavat haluta määrittää tehtäväluettelon toistuvaksi.</span><span class="sxs-lookup"><span data-stu-id="26be5-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="26be5-124">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="26be5-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="26be5-125">Valitse määritettävä tehtäväluettelo.</span><span class="sxs-lookup"><span data-stu-id="26be5-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="26be5-126">Valitse **Käynnistä prosessi**.</span><span class="sxs-lookup"><span data-stu-id="26be5-126">Select **Start process**.</span></span>
1. <span data-ttu-id="26be5-127">Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="26be5-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="26be5-128">Määritä **Toistuvuus**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="26be5-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="26be5-129">Anna **Toistuvuuden tavoitepvm:n vastakirjaus päivinä** -kenttään päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="26be5-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="26be5-130">Jos esimerkiksi annat arvoksi **4**, tavoitepäivämäärä on toistumispäivämäärä plus neljä päivää.</span><span class="sxs-lookup"><span data-stu-id="26be5-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="26be5-131">Valitse **Suorita taustalla** -välilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="26be5-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="26be5-132">Anna **Määritä toistuvuus** -valintaikkunaan taajuuden ehdot ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="26be5-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="26be5-133">Seuraavassa kuvassa on esimerkki siitä, miten taajuuden ehdot annetaan **Määritä toistuminen** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="26be5-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Taajuuden ehtojen antaminen Määritä toistuvuus -valintaikkunassa](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="26be5-135">Tehtäväluettelon tilan seuraaminen</span><span class="sxs-lookup"><span data-stu-id="26be5-135">Track task list status</span></span>

<span data-ttu-id="26be5-136">Jos olet alue- tai myymäläpäällikkö, haluat ehkä seurata useille myymälöille tai työntekijöille määritettyjen tehtäväluetteloiden tilaa.</span><span class="sxs-lookup"><span data-stu-id="26be5-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="26be5-137">Tämän jälkeen voit seurata niitä myymälöitä tai työntekijöitä, jotka eivät ole suorittaneet heille määritettyjä tehtäviä ajoissa.</span><span class="sxs-lookup"><span data-stu-id="26be5-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="26be5-138">Commercen taustatoiminnon avulla voit tarkastella tehtäväluetteloiden tilaa, määrittää tehtäviä uudelleen ja muuttaa tehtävän tilaa.</span><span class="sxs-lookup"><span data-stu-id="26be5-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="26be5-139">Voit seurata kaikkien tehtävien tehtäväluettelon tilaa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="26be5-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="26be5-140">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.</span><span class="sxs-lookup"><span data-stu-id="26be5-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="26be5-141">Valitsemalla **Kaikki tehtäväluettelot** -välilehden voit tarkastella eri myymälöihin määritettyjen tehtäväluetteloiden tilaa.</span><span class="sxs-lookup"><span data-stu-id="26be5-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="26be5-142">Voit seurata kaikkien sinulle määritettyjen tehtävien tehtäväluettelon tilaa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="26be5-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="26be5-143">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.</span><span class="sxs-lookup"><span data-stu-id="26be5-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="26be5-144">Valitse **Omat tehtävät**- tai **Kaikki tehtävät** -välilehti, jos haluat tarkastella tai päivittää sinulle määritettyjen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="26be5-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26be5-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="26be5-145">Additional resources</span></span>

[<span data-ttu-id="26be5-146">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="26be5-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="26be5-147">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26be5-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="26be5-148">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="26be5-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="26be5-149">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="26be5-149">Task management in POS</span></span>](task-mgmt-POS.md)
