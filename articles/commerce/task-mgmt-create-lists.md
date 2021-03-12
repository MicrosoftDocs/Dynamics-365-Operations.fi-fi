---
title: Tehtäväluetteloiden luominen ja tehtävien lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot luodaan ja miten niihin lisätään tehtäviä Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006207"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="dee5a-103">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="dee5a-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dee5a-104">Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot luodaan ja miten niihin lisätään tehtäviä Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="dee5a-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dee5a-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dee5a-105">Overview</span></span>

<span data-ttu-id="dee5a-106">*Tehtävä* määrittää tietyn työn tai toiminnon, joka on suoritettava tiettynä eräpäivänä tai ennen sitä.</span><span class="sxs-lookup"><span data-stu-id="dee5a-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="dee5a-107">Dynamics 365 Commerce -sovelluksessa tehtävä voi sisältää eriteltyjä ohjeita ja tietoja yhteyshenkilöstä.</span><span class="sxs-lookup"><span data-stu-id="dee5a-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="dee5a-108">Se voi sisältää myös linkkejä taustatoimintoihin, myyntipistetoimintoihin tai sivuston sivuihin. Tämä auttaa parantamaan tuottavuutta ja määrittämään kontekstin, jonka avulla tehtävän omistaja voi suorittaa tehtävän tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="dee5a-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="dee5a-109">*Tehtäväluettelo* on kokoelma tehtäviä, jotka on suoritettava liiketoimintaprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="dee5a-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="dee5a-110">Tehtäväluettelo voi olla esimerkiksi uudelle työntekijälle, jonka on suoritettava tehtävät perehdytyksen aikana, kassanhoitajalle, joka työskentelee iltavuoroissa tai tulevan lomakauden valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="dee5a-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="dee5a-111">Commercessa kaikki tehtäväluettelot, joilla on tavoitepäivämäärä, voidaan määrittää halutulle määrälle myymälöitä tai työntekijöitä. Ne voidaan määrittää myös toistuviksi.</span><span class="sxs-lookup"><span data-stu-id="dee5a-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="dee5a-112">Sekä päälliköt että työntekijät voivat luoda tehtäväluetteloita Commercen taustatoiminnoissa ja määrittää ne tämän jälkeen myymäläjoukoille.</span><span class="sxs-lookup"><span data-stu-id="dee5a-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="dee5a-113">Tehtäväluettelon luominen</span><span class="sxs-lookup"><span data-stu-id="dee5a-113">Create a task list</span></span>

<span data-ttu-id="dee5a-114">Voit luoda tehtäväluettelon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="dee5a-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="dee5a-115">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="dee5a-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="dee5a-116">Valitse **Uusi** ja anna arvot **Nimi**-, **Kuvaus** -ja **Omistaja**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="dee5a-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="dee5a-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dee5a-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="dee5a-118">Tehtävien lisääminen tehtäväluetteloon</span><span class="sxs-lookup"><span data-stu-id="dee5a-118">Add tasks to a task list</span></span>

<span data-ttu-id="dee5a-119">Voit lisätä tehtäviä tehtäväluetteloon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="dee5a-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="dee5a-120">Lisää tehtävä valitsemalla olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dee5a-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="dee5a-121">Anna tehtävän nimi **Luo uusi tehtävä** -valintaikkunan **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dee5a-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="dee5a-122">Anna positiivinen tai negatiivinen kokonaisluku **Eräpäivän vastakirjaus tavoitepvm:stä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dee5a-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="dee5a-123">Anna esimerkiksi **-2**, jos tehtävä on suoritettava kaksi päivää ennen tehtäväluettelon eräpäivää.</span><span class="sxs-lookup"><span data-stu-id="dee5a-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="dee5a-124">Anna **Huomautukset**-kenttään yksityiskohtaiset ohjeet.</span><span class="sxs-lookup"><span data-stu-id="dee5a-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="dee5a-125">Anna **Yhteyshenkilö**-kenttään sen aihepiirin asiantuntijan nimi, johon tehtävän omistaja voi ottaa yhteyttä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="dee5a-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="dee5a-126">Anna **Tehtävän linkki** -kenttään linkki, joka perustuu tehtävän luonteeseen.</span><span class="sxs-lookup"><span data-stu-id="dee5a-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="dee5a-127">Vaikka voit käyttää **Määritetty henkilölle** -kenttää, jos haluat määrittää tehtäviä jollekin tehtäväluettelon luomisen yhteydessä, on suositeltavaa välttää tehtävien määrittämistä tehtäväluettelon luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="dee5a-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="dee5a-128">Sen sijaan tehtävät kannattaa määrittää sen jälkeen, kun luettelo on luotu yksittäisille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="dee5a-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="dee5a-129">Työntekijöiden tuottavuuden parantaminen tehtävälinkkien avulla</span><span class="sxs-lookup"><span data-stu-id="dee5a-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="dee5a-130">Commercen avulla tehtäviä voi linkittää tiettyihin myyntipistetoimintoihin, kuten myyntiraportin suorittaminen, online-koulutusvideon tarkasteleminen uuden työntekijän ohjauksen yhteydessä tai taustatoiminnon suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="dee5a-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="dee5a-131">Tämä ominaisuus auttaa tehtävän omistajia hankkimaan tiedot, joita he tarvitsevat tehtävän tehokasta suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="dee5a-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="dee5a-132">Voit lisätä linkkejä tehtävää luodessasi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="dee5a-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="dee5a-133">Valitse olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="dee5a-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="dee5a-134">Valitse **Muokkaa tehtävää** -valintaikkunan **Tehtävän linkki** -kentässä vähintään yksi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="dee5a-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="dee5a-135">Valitse **Valikkovaihtoehto**, jos haluat määrittää taustatoiminnon, kuten Tuotteen myyntirakenteet.</span><span class="sxs-lookup"><span data-stu-id="dee5a-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="dee5a-136">Valitse **Myyntipistetoiminto**, jos haluat määrittää myyntipistetoiminnon. Se voi olla esimerkiksi myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="dee5a-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="dee5a-137">Valitse **URL-osoite**, jos haluat määrittää absoluuttisen URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="dee5a-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="dee5a-138">Seuraavassa kuvassa on tehtävän linkkien valikoima **Muokkaa tehtävää** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="dee5a-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Tehtävän linkkien valitseminen Muokkaa tehtävää -valintaikkunassa](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="dee5a-140">Myyntipistetoiminnon määrittäminen niin, että se voidaan linkittää tehtävään</span><span class="sxs-lookup"><span data-stu-id="dee5a-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="dee5a-141">Jos haluat määrittää myyntipistetoiminnon niin, että se voidaan linkittää tehtävään, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="dee5a-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="dee5a-142">Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.</span><span class="sxs-lookup"><span data-stu-id="dee5a-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="dee5a-143">Valitse **Muokkaa**, etsi myyntipistetoiminto ja valitse sitten toiminnon **Ota tehtävienhallinta käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="dee5a-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dee5a-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dee5a-144">Additional resources</span></span>

[<span data-ttu-id="dee5a-145">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dee5a-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="dee5a-146">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dee5a-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="dee5a-147">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="dee5a-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="dee5a-148">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="dee5a-148">Task management in POS</span></span>](task-mgmt-POS.md)
