---
title: Huoltosopimusten luominen
description: "Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5447787ea0f6b0c83e43fa5f0a4e18db9361f04c
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="90510-103">Huoltosopimusten luominen</span><span class="sxs-lookup"><span data-stu-id="90510-103">Create service agreements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="90510-104">Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa.</span><span class="sxs-lookup"><span data-stu-id="90510-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="90510-105">Huoltosopimuksen luominen Huoltohallinnassa</span><span class="sxs-lookup"><span data-stu-id="90510-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="90510-106">Siirry **huoltohallintaan**.</span><span class="sxs-lookup"><span data-stu-id="90510-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="90510-107">Luo uusi huoltosopimus sivun otsikossa valitsemalla **Huoltosopimukset**.</span><span class="sxs-lookup"><span data-stu-id="90510-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="90510-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="90510-108">Click **New**.</span></span> <span data-ttu-id="90510-109">Anna kuvaus, valitse viittaus projektiin **Projektitunnus**-kentässä ja täytä huoltosopimuksen muut kentät ja rivit.</span><span class="sxs-lookup"><span data-stu-id="90510-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="90510-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="90510-110">Click **Save**.</span></span>
4. <span data-ttu-id="90510-111">Luo huoltokohteen suhteet tai huoltotehtäväsuhteet huoltosopimusta varten valitsemalla **Suhteet**-välilehdessä **Huoltokohteet** tai **Huoltotehtävät**.</span><span class="sxs-lookup"><span data-stu-id="90510-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="90510-112">Huoltokohteet ja -tehtävät, joita varten olet luonut suhteet, voidaan liittää huoltosopimuksen riveihin.</span><span class="sxs-lookup"><span data-stu-id="90510-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="90510-113">Luo sivun alaosaan huoltosopimusrivejä kopioimalla rivejä huoltomallista tai toisesta huoltosopimuksesta. Vaihtoehtoisesti voit luoda huoltosopimusrivit manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="90510-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="90510-114">Jos kopioit rivejä huoltosopimukseen toisesta huoltosopimuksesta, voit määrittää, haluatko kopioida myös huoltokohteen ja huoltotehtävän suhteet.</span><span class="sxs-lookup"><span data-stu-id="90510-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="90510-115">Jos kopioit nämä suhteet, ne lisätään huoltosopimuksen aiemmin luotuihin suhteisiin.</span><span class="sxs-lookup"><span data-stu-id="90510-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="90510-116">Jos kopioit huoltosopimusrivejä huoltomallista, huoltokohteen ja huoltotehtävän suhteet kopioidaan automaattisesti huoltokohteen ja huoltotehtävän suhteina uusiin huoltosopimusriveihin.</span><span class="sxs-lookup"><span data-stu-id="90510-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="90510-117">Huoltosopimusrivien luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="90510-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="90510-118">Lisää huoltosopimusrivit riviruudukossa **Huoltosopimukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="90510-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="90510-119">Anna asiaankuuluvat tiedot huoltosopimusriville.</span><span class="sxs-lookup"><span data-stu-id="90510-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="90510-120">Tallenna rivi painamalla näppäinyhdistelmää **CTRL+S** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="90510-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="90510-121">Huoltosopimuksen luominen projektista</span><span class="sxs-lookup"><span data-stu-id="90510-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="90510-122">Valitse **Projektinhallinta ja kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="90510-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="90510-123">Valitse **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="90510-123">Click **All projects**.</span></span>
3. <span data-ttu-id="90510-124">Valitse projekti luettelosta.</span><span class="sxs-lookup"><span data-stu-id="90510-124">Select the project from the list.</span></span>
4. <span data-ttu-id="90510-125">Valitse **toimintoruudussa** **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="90510-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="90510-126">Valitse **Uusi**-toimintoryhmässä ensin **Huolto** ja sitten **Huoltosopimus**.</span><span class="sxs-lookup"><span data-stu-id="90510-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="90510-127">Anna projektiviite noudattamalla osan **Huoltosopimuksen luominen** vaiheita, kuten on kuvattu aiemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="90510-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="90510-128">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="90510-128">Related topics</span></span>

[<span data-ttu-id="90510-129">Huoltosopimukset</span><span class="sxs-lookup"><span data-stu-id="90510-129">Service agreements</span></span>](service-agreements.md)


