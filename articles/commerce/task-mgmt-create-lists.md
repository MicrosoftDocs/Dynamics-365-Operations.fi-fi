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
ms.openlocfilehash: 28bea16c3266115cf09aa80a364344789d60af7a
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477826"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="9706c-103">Tehtäväluetteloiden luominen ja tehtävien lisääminen</span><span class="sxs-lookup"><span data-stu-id="9706c-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9706c-104">Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot luodaan ja miten niihin lisätään tehtäviä Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="9706c-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9706c-105">*Tehtävä* määrittää tietyn työn tai toiminnon, joka on suoritettava tiettynä eräpäivänä tai ennen sitä.</span><span class="sxs-lookup"><span data-stu-id="9706c-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="9706c-106">Dynamics 365 Commerce -sovelluksessa tehtävä voi sisältää eriteltyjä ohjeita ja tietoja yhteyshenkilöstä.</span><span class="sxs-lookup"><span data-stu-id="9706c-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="9706c-107">Se voi sisältää myös linkkejä taustatoimintoihin, myyntipistetoimintoihin tai sivuston sivuihin. Tämä auttaa parantamaan tuottavuutta ja määrittämään kontekstin, jonka avulla tehtävän omistaja voi suorittaa tehtävän tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="9706c-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="9706c-108">*Tehtäväluettelo* on kokoelma tehtäviä, jotka on suoritettava liiketoimintaprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="9706c-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="9706c-109">Tehtäväluettelo voi olla esimerkiksi uudelle työntekijälle, jonka on suoritettava tehtävät perehdytyksen aikana, kassanhoitajalle, joka työskentelee iltavuoroissa tai tulevan lomakauden valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="9706c-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="9706c-110">Commercessa kaikki tehtäväluettelot, joilla on tavoitepäivämäärä, voidaan määrittää halutulle määrälle myymälöitä tai työntekijöitä. Ne voidaan määrittää myös toistuviksi.</span><span class="sxs-lookup"><span data-stu-id="9706c-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="9706c-111">Sekä päälliköt että työntekijät voivat luoda tehtäväluetteloita Commercen taustatoiminnoissa ja määrittää ne tämän jälkeen myymäläjoukoille.</span><span class="sxs-lookup"><span data-stu-id="9706c-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="9706c-112">Tehtäväluettelon luominen</span><span class="sxs-lookup"><span data-stu-id="9706c-112">Create a task list</span></span>

<span data-ttu-id="9706c-113">Voit luoda tehtäväluettelon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9706c-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="9706c-114">Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.</span><span class="sxs-lookup"><span data-stu-id="9706c-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="9706c-115">Valitse **Uusi** ja anna arvot **Nimi**-, **Kuvaus** -ja **Omistaja**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="9706c-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="9706c-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9706c-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="9706c-117">Tehtävien lisääminen tehtäväluetteloon</span><span class="sxs-lookup"><span data-stu-id="9706c-117">Add tasks to a task list</span></span>

<span data-ttu-id="9706c-118">Voit lisätä tehtäviä tehtäväluetteloon seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9706c-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="9706c-119">Lisää tehtävä valitsemalla olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9706c-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="9706c-120">Anna tehtävän nimi **Luo uusi tehtävä** -valintaikkunan **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9706c-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="9706c-121">Anna positiivinen tai negatiivinen kokonaisluku **Eräpäivän vastakirjaus tavoitepvm:stä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9706c-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="9706c-122">Anna esimerkiksi **-2**, jos tehtävä on suoritettava kaksi päivää ennen tehtäväluettelon eräpäivää.</span><span class="sxs-lookup"><span data-stu-id="9706c-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="9706c-123">Anna **Huomautukset**-kenttään yksityiskohtaiset ohjeet.</span><span class="sxs-lookup"><span data-stu-id="9706c-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="9706c-124">Anna **Yhteyshenkilö**-kenttään sen aihepiirin asiantuntijan nimi, johon tehtävän omistaja voi ottaa yhteyttä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="9706c-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="9706c-125">Anna **Tehtävän linkki** -kenttään linkki, joka perustuu tehtävän luonteeseen.</span><span class="sxs-lookup"><span data-stu-id="9706c-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="9706c-126">Vaikka voit käyttää **Määritetty henkilölle** -kenttää, jos haluat määrittää tehtäviä jollekin tehtäväluettelon luomisen yhteydessä, on suositeltavaa välttää tehtävien määrittämistä tehtäväluettelon luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="9706c-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="9706c-127">Sen sijaan tehtävät kannattaa määrittää sen jälkeen, kun luettelo on luotu yksittäisille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="9706c-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="9706c-128">Työntekijöiden tuottavuuden parantaminen tehtävälinkkien avulla</span><span class="sxs-lookup"><span data-stu-id="9706c-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="9706c-129">Commercen avulla tehtäviä voi linkittää tiettyihin myyntipistetoimintoihin, kuten myyntiraportin suorittaminen, online-koulutusvideon tarkasteleminen uuden työntekijän ohjauksen yhteydessä tai taustatoiminnon suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="9706c-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="9706c-130">Tämä ominaisuus auttaa tehtävän omistajia hankkimaan tiedot, joita he tarvitsevat tehtävän tehokasta suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="9706c-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="9706c-131">Voit lisätä linkkejä tehtävää luodessasi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9706c-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="9706c-132">Valitse olemassa olevan tehtäväluettelon **Tehtävät**-pikavälilehdessä **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="9706c-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="9706c-133">Valitse **Muokkaa tehtävää** -valintaikkunan **Tehtävän linkki** -kentässä vähintään yksi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="9706c-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="9706c-134">Valitse **Valikkovaihtoehto**, jos haluat määrittää taustatoiminnon, kuten Tuotteen myyntirakenteet.</span><span class="sxs-lookup"><span data-stu-id="9706c-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="9706c-135">Valitse **Myyntipistetoiminto**, jos haluat määrittää myyntipistetoiminnon. Se voi olla esimerkiksi myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="9706c-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="9706c-136">Valitse **URL-osoite**, jos haluat määrittää absoluuttisen URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="9706c-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="9706c-137">Seuraavassa kuvassa on tehtävän linkkien valikoima **Muokkaa tehtävää** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9706c-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Tehtävän linkkien valitseminen Muokkaa tehtävää -valintaikkunassa](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="9706c-139">Myyntipistetoiminnon määrittäminen niin, että se voidaan linkittää tehtävään</span><span class="sxs-lookup"><span data-stu-id="9706c-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="9706c-140">Jos haluat määrittää myyntipistetoiminnon niin, että se voidaan linkittää tehtävään, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="9706c-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="9706c-141">Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.</span><span class="sxs-lookup"><span data-stu-id="9706c-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="9706c-142">Valitse **Muokkaa**, etsi myyntipistetoiminto ja valitse sitten toiminnon **Ota tehtävienhallinta käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9706c-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9706c-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9706c-143">Additional resources</span></span>

[<span data-ttu-id="9706c-144">Tehtävien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9706c-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9706c-145">Tehtävien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9706c-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="9706c-146">Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille</span><span class="sxs-lookup"><span data-stu-id="9706c-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="9706c-147">Tehtävien hallinta myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="9706c-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
