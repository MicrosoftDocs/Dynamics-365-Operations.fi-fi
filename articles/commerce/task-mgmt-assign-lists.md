---
title: Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795258"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="bef74-103">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="bef74-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bef74-104">Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="bef74-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bef74-105">Dynamics 365 Commerce -sovelluksen tehtävienhallinnan avulla voit määrittää tehtäväluettelon useille myymälöille tai työntekijöille tai myymälöiden ja työntekijöiden yhdistelmille.</span><span class="sxs-lookup"><span data-stu-id="bef74-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="bef74-106">Esimerkiksi 20 myymälän aluepäällikkö voi haluta määrittää kaikille 20 myymälälle **Loma-ajan valmistelu** -tehtäväluettelon.</span><span class="sxs-lookup"><span data-stu-id="bef74-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="bef74-107">Tehtäväluettelon määritysprosessin käynnistäminen</span><span class="sxs-lookup"><span data-stu-id="bef74-107">Start the task list assignment process</span></span>

<span data-ttu-id="bef74-108">Voit aloittaa tehtäväluettelon määrittämisen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="bef74-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="bef74-109">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="bef74-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="bef74-110">Valitse määritettävä tehtäväluettelo.</span><span class="sxs-lookup"><span data-stu-id="bef74-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="bef74-111">Valitse **Käynnistä prosessi**.</span><span class="sxs-lookup"><span data-stu-id="bef74-111">Select **Start process**.</span></span>
1. <span data-ttu-id="bef74-112">Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi (esimerkiksi **Itäisen alueen myymälät**).</span><span class="sxs-lookup"><span data-stu-id="bef74-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="bef74-113">Määritä **Tavoitepvm**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bef74-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="bef74-114">Jos haluat määrittää myymälöille tehtäväluettelot, etsi ja valitse myymälät **Myymälät**-välilehden **Organisaatiohierarkia**-suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="bef74-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="bef74-115">Voit määrittää tehtäväluettelon työntekijöille etsimällä ja valitsemalla työntekijät **Työntekijät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bef74-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="bef74-116">Käynnistä prosessi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="bef74-116">Select **OK** to start the process.</span></span> <span data-ttu-id="bef74-117">Tehtäväluettelo määritetään valituille myymälöille tai työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="bef74-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="bef74-118">Seuraavassa kuvassa on esimerkki siitä, miten myymälät etsitään ja valitaan **Käynnistä prosessi** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="bef74-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Myymälöiden etsiminen ja valitseminen Käynnistä prosessi -valintaikkunassa](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="bef74-120">Tehtäväluetteloiden määrittäminen toistuviksi</span><span class="sxs-lookup"><span data-stu-id="bef74-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="bef74-121">Vähittäiskauppiailla on joskus toistuvia tehtäviä, kuten torstain sulkemisen tarkistuslista tai kuukauden ensimmäisen päivän tarkistuslista.</span><span class="sxs-lookup"><span data-stu-id="bef74-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="bef74-122">Tämän vuoksi he saattavat haluta määrittää tehtäväluettelon toistuvaksi.</span><span class="sxs-lookup"><span data-stu-id="bef74-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="bef74-123">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="bef74-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="bef74-124">Valitse määritettävä tehtäväluettelo.</span><span class="sxs-lookup"><span data-stu-id="bef74-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="bef74-125">Valitse **Käynnistä prosessi**.</span><span class="sxs-lookup"><span data-stu-id="bef74-125">Select **Start process**.</span></span>
1. <span data-ttu-id="bef74-126">Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="bef74-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="bef74-127">Määritä **Toistuvuus**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bef74-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="bef74-128">Anna **Toistuvuuden tavoitepvm:n vastakirjaus päivinä** -kenttään päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="bef74-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="bef74-129">Jos esimerkiksi annat arvoksi **4**, tavoitepäivämäärä on toistumispäivämäärä plus neljä päivää.</span><span class="sxs-lookup"><span data-stu-id="bef74-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="bef74-130">Valitse **Suorita taustalla** -välilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="bef74-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="bef74-131">Anna **Määritä toistuvuus** -valintaikkunaan taajuuden ehdot ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bef74-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="bef74-132">Seuraavassa kuvassa on esimerkki siitä, miten taajuuden ehdot annetaan **Määritä toistuminen** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="bef74-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Taajuuden ehtojen antaminen Määritä toistuvuus -valintaikkunassa](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="bef74-134">Tehtäväluettelon tilan seuraaminen</span><span class="sxs-lookup"><span data-stu-id="bef74-134">Track task list status</span></span>

<span data-ttu-id="bef74-135">Jos olet alue- tai myymäläpäällikkö, haluat ehkä seurata useille myymälöille tai työntekijöille määritettyjen tehtäväluetteloiden tilaa.</span><span class="sxs-lookup"><span data-stu-id="bef74-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="bef74-136">Tämän jälkeen voit seurata niitä myymälöitä tai työntekijöitä, jotka eivät ole suorittaneet heille määritettyjä tehtäviä ajoissa.</span><span class="sxs-lookup"><span data-stu-id="bef74-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="bef74-137">Commercen taustatoiminnon avulla voit tarkastella tehtäväluetteloiden tilaa, määrittää tehtäviä uudelleen ja muuttaa tehtävän tilaa.</span><span class="sxs-lookup"><span data-stu-id="bef74-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="bef74-138">Voit seurata kaikkien tehtävien tehtäväluettelon tilaa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="bef74-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="bef74-139">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.</span><span class="sxs-lookup"><span data-stu-id="bef74-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="bef74-140">Valitsemalla **Kaikki tehtäväluettelot** -välilehden voit tarkastella eri myymälöihin määritettyjen tehtäväluetteloiden tilaa.</span><span class="sxs-lookup"><span data-stu-id="bef74-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="bef74-141">Voit seurata kaikkien sinulle määritettyjen tehtävien tehtäväluettelon tilaa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="bef74-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="bef74-142">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.</span><span class="sxs-lookup"><span data-stu-id="bef74-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="bef74-143">Valitse **Omat tehtävät**- tai **Kaikki tehtävät** -välilehti, jos haluat tarkastella tai päivittää sinulle määritettyjen tehtävien tilaa.</span><span class="sxs-lookup"><span data-stu-id="bef74-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bef74-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bef74-144">Additional resources</span></span>

[<span data-ttu-id="bef74-145">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bef74-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="bef74-146">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bef74-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="bef74-147">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="bef74-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="bef74-148">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="bef74-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
