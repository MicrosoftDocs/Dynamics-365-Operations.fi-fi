---
title: Huoltosopimusten luominen
description: Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa.
author: ShylaThompson
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2343d60f5960702bc05705ee2dd0994c9e2d4fc1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817650"
---
# <a name="create-service-agreements"></a><span data-ttu-id="7d7fa-103">Huoltosopimusten luominen</span><span class="sxs-lookup"><span data-stu-id="7d7fa-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d7fa-104">Tässä aiheessa kuvataan, miten Huoltohallinta- ja Projektinhallinta ja kirjanpito -moduulien ominaisuuksia käytetään huoltosopimusten luonnissa.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="7d7fa-105">Huoltosopimuksen luominen Huoltohallinnassa</span><span class="sxs-lookup"><span data-stu-id="7d7fa-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="7d7fa-106">Siirry **huoltohallintaan**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="7d7fa-107">Valitse **Huoltosopimukset** luodaksesi uuden huoltosopimusrivin sivun yllätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-107">Select **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="7d7fa-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-108">Select **New**.</span></span> <span data-ttu-id="7d7fa-109">Anna kuvaus, valitse viittaus projektiin **Projektitunnus**-kentässä ja täytä huoltosopimuksen muut kentät ja rivit.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="7d7fa-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-110">Select **Save**.</span></span>
4. <span data-ttu-id="7d7fa-111">Luo huoltokohteen suhteet tai huoltotehtäväsuhteet huoltosopimusta varten valitsemalla **Suhteet**-välilehdessä **Huoltokohteet** tai **Huoltotehtävät**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="7d7fa-112">Huoltokohteet ja -tehtävät, joita varten olet luonut suhteet, voidaan liittää huoltosopimuksen riveihin.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="7d7fa-113">Luo sivun alaosaan huoltosopimusrivejä kopioimalla rivejä huoltomallista tai toisesta huoltosopimuksesta. Vaihtoehtoisesti voit luoda huoltosopimusrivit manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="7d7fa-114">Jos kopioit rivejä huoltosopimukseen toisesta huoltosopimuksesta, voit määrittää, haluatko kopioida myös huoltokohteen ja huoltotehtävän suhteet.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="7d7fa-115">Jos kopioit nämä suhteet, ne lisätään huoltosopimuksen aiemmin luotuihin suhteisiin.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="7d7fa-116">Jos kopioit huoltosopimusrivejä huoltomallista, huoltokohteen ja huoltotehtävän suhteet kopioidaan automaattisesti huoltokohteen ja huoltotehtävän suhteina uusiin huoltosopimusriveihin.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="7d7fa-117">Huoltosopimusrivien luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="7d7fa-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="7d7fa-118">Lisää huoltosopimusrivit riviruudukossa **Huoltosopimukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="7d7fa-119">Anna asiaankuuluvat tiedot huoltosopimusriville.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="7d7fa-120">Valitse **Tallenna** tallentaaksesi rivin ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-120">Select **Save** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="7d7fa-121">Huoltosopimuksen luominen projektista</span><span class="sxs-lookup"><span data-stu-id="7d7fa-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="7d7fa-122">Valitse **Projektinhallinta ja kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-122">Select **Project management and accounting**.</span></span>
2. <span data-ttu-id="7d7fa-123">Valitse **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-123">Select **All projects**.</span></span>
3. <span data-ttu-id="7d7fa-124">Valitse projekti luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-124">Select the project from the list.</span></span>
4. <span data-ttu-id="7d7fa-125">Valitse **Toimintoruutu**-osiosta **Hallinta**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-125">On the **Action Pane**, select **Manage**.</span></span> <span data-ttu-id="7d7fa-126">Valitse **Uusi**-toimintoryhmästä **Huolto** ja sitten **Huoltosopimus**.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-126">In the **New** Action group, select **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="7d7fa-127">Anna projektiviite noudattamalla osan **Huoltosopimuksen luominen** vaiheita, kuten on kuvattu aiemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="7d7fa-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="7d7fa-128">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="7d7fa-128">Related topics</span></span>

[<span data-ttu-id="7d7fa-129">Huoltosopimusten laatiminen ja luominen – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7d7fa-129">Develop and establish service agreements overview</span></span>](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]