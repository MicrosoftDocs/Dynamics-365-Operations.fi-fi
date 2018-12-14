---
title: Prosessimallin luominen Attractissa
description: "Tässä ohjeaiheessa on tietoja prosessimallin luomisesta Attractissa."
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: 2b9cac68093be65584192757229c20b1a1546342
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="57f9a-103">Prosessimallin luominen Attractissa</span><span class="sxs-lookup"><span data-stu-id="57f9a-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57f9a-104">*Työhönoton prosessimalli* sisältää kaikki tehtävät, joiden on sisällyttävä työn työhönottoprosessiin.</span><span class="sxs-lookup"><span data-stu-id="57f9a-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="57f9a-105">Tässä ohjeaiheessa käsitellään prosessimallin elementtejä Microsoft Dynamics 365 for Talent: Attractissa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="57f9a-106">Siinä käsitellään myös mallin luomista.</span><span class="sxs-lookup"><span data-stu-id="57f9a-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="57f9a-107">Mallin luonti sisältyy Attractin kattavaan työhönottolaajennukseen.</span><span class="sxs-lookup"><span data-stu-id="57f9a-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="57f9a-108">Mallien hallinta</span><span class="sxs-lookup"><span data-stu-id="57f9a-108">Template management</span></span>

<span data-ttu-id="57f9a-109">Organisaatiot voit päättää, voivatko ryhmän jäsenet tai vain järjestelmänvalvojat luoda prosessimalleja Attractissa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="57f9a-110">Voit määrittää mallien hallinnan valitsemalla **Hallintakeskus** \> **Mallien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="57f9a-111">Jos haluat, että ryhmän jäsenet luomat oman mallinsa, ota mallien hallinta käyttöön.</span><span class="sxs-lookup"><span data-stu-id="57f9a-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="57f9a-112">Jos et ota mallien hallintaa käyttöön, vain järjestelmänvalvojat voivat luoda malleja.</span><span class="sxs-lookup"><span data-stu-id="57f9a-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="57f9a-113">Oletusmalli</span><span class="sxs-lookup"><span data-stu-id="57f9a-113">Default template</span></span>

<span data-ttu-id="57f9a-114">Vain järjestelmänvalvojat voivat määrittää oletusmallin.</span><span class="sxs-lookup"><span data-stu-id="57f9a-114">Only admins can set the default template.</span></span> <span data-ttu-id="57f9a-115">Oletusmallia käytetään, jos mallia ei ole valittu työtä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="57f9a-116">Määritä oletusmalli valitsemalla **Hallintakeskus** \> **Mallien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="57f9a-117">Valitse oletusmalliksi valittavan mallin kortissa ensin ellipsipainike (**...**) ja sitten **Aseta oletukseksi**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="57f9a-118">Prosessimallin luominen</span><span class="sxs-lookup"><span data-stu-id="57f9a-118">Create a process template</span></span>

<span data-ttu-id="57f9a-119">Järjestelmänvalvojat, työhönottajat ja työhönottopäälliköt voivat luoda prosessimalleja.</span><span class="sxs-lookup"><span data-stu-id="57f9a-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="57f9a-120">Prosessimalli koostuu *vaiheista* ja *tehtävistä*.</span><span class="sxs-lookup"><span data-stu-id="57f9a-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="57f9a-121">Vaiheet ryhmittävät tehtävät yhteen.</span><span class="sxs-lookup"><span data-stu-id="57f9a-121">Stages group together one or more activities.</span></span> <span data-ttu-id="57f9a-122">Oletusarvoisesti jokaisessa prosessimallissa on seuraavat tehtävät: potentiaalinen ehdokas, hakemus ja tarjous.</span><span class="sxs-lookup"><span data-stu-id="57f9a-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="57f9a-123">Nämä tehtävät sisältävät vaiheet voidaan nimetä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="57f9a-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="57f9a-124">Voit lisätä muita vaiheita valitsemalla **+ Uusi vaihe**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="57f9a-125">Voit lisätä tehtäviä vaiheeseen joko vetämällä ne sopivaan vaiheeseen tai kaksoisnapsauttamalla tehtävää tehtäväluettelossa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="57f9a-126">Ehdokkaat näkevät vaiheen nimet **Hakemuksen tila** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="57f9a-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="57f9a-127">Ota tämä huomioon, kun valitset vaiheiden nimiä.</span><span class="sxs-lookup"><span data-stu-id="57f9a-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="57f9a-128">Lisätietoja tehtävistä on kohdassa [Työhönottoprosessin tehtävät Attractissa](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="57f9a-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="57f9a-129">Luo työhönoton prosessimalli noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="57f9a-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="57f9a-130">Valitse **Mallit**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="57f9a-131">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-131">Select **New**.</span></span>
3. <span data-ttu-id="57f9a-132">Kirjoita **Mallin nimi** -kenttään mallin nimi ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="57f9a-133">Valitse **Valitse hyväksyntäprosessi** -luettelossa **Oletus**, jos haluat, että työ on aina hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="57f9a-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="57f9a-134">Valitse, otetaanko potentiaaliset ehdokkaat käyttöön vai poistetaanko ne käytöstä.</span><span class="sxs-lookup"><span data-stu-id="57f9a-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="57f9a-135">Valinnainen: lisää tai poista vaiheita.</span><span class="sxs-lookup"><span data-stu-id="57f9a-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="57f9a-136">Lisää vaihe valitsemalla **+ Uusi vaihe**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="57f9a-137">Poista vaihe pitämällä osoitinta vaiheen päällä ja valitsemalla esiin tuleva roskakoripainike.</span><span class="sxs-lookup"><span data-stu-id="57f9a-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="57f9a-138">Potentiaalinen vaihe-, Hakemus- ja Tarjous-vaiheita ei voi poistaa, mutta niiden nimi voidaan vaihtaa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="57f9a-139">Valinnainen: lisää tai poista tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="57f9a-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="57f9a-140">Voit lisätä tehtävän vetämällä sen oikeaan vaiheeseen oikealla olevassa tehtäväluettelossa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="57f9a-141">Vaihtoehtoisesti voit kaksoisnapsauttaa tehtävää ja valita sitten vaiheen, johon se lisätään.</span><span class="sxs-lookup"><span data-stu-id="57f9a-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="57f9a-142">Poista tehtävä laajentamalla se ja valitsemalla sitten roskakorikuvake tehtävän ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="57f9a-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="57f9a-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="57f9a-143">Select **Save**.</span></span>

