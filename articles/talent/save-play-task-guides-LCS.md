---
title: "Tehtäväoppaiden tallentaminen LCS-palveluun ja niiden toistaminen"
description: "Tässä ohjeaiheessa kerrotaan, miten tehtäväoppaat tallennetaan Microsoft Dynamics Lifecycle Servicesin (LCS) ja miten niitä toistetaan."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="a1ddd-103">Tehtäväoppaiden tallentaminen LCS-palveluun ja niiden toistaminen</span><span class="sxs-lookup"><span data-stu-id="a1ddd-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1ddd-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="a1ddd-104">**Environment details**</span></span> 

<span data-ttu-id="a1ddd-105">Microsoft Dynamics 365 for Talent, joka on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin kautta (LCS)</span><span class="sxs-lookup"><span data-stu-id="a1ddd-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="a1ddd-106">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="a1ddd-106">**Issue**</span></span>

<span data-ttu-id="a1ddd-107">Asiakas haluaa tallentaa uudet tehtävätallenteet LCS-projektiin ja sitten toistaa tallennettuja tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="a1ddd-108">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="a1ddd-108">**Resolution**</span></span>

<span data-ttu-id="a1ddd-109">Tallenna tehtävätallenne seuraavien ohjeiden mukaisesti LCS-palveluun.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="a1ddd-110">Kirjaudu LCS-palveluun ja valitse projekti.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="a1ddd-111">Valitse **Liiketoimintaprosessin mallintaja** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="a1ddd-112">Näytä sivu päivitetyssä BPM-käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="a1ddd-113">Valitse ensin kirjasto sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="a1ddd-114">Anna liiketoimintaprosessin mallintajalle (BPM) nimi.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="a1ddd-115">Kirjaudu Talentiin LCS-palvelusta.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="a1ddd-116">Kirjoita **Haku**-kenttään **ohje**.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="a1ddd-117">Lifecycle Servicesin ohje avautuu.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="a1ddd-118">Valitse Lifecycle Services -ohjemäärityksen **Päivitä**-painike.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="a1ddd-119">BPM-kirjaston pitäisi tulla näkyviin ja sen pitäisi olla aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="a1ddd-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-120">Close the page.</span></span>
10. <span data-ttu-id="a1ddd-121">Luo tehtävätallenne.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-121">Create a task recording.</span></span>
11. <span data-ttu-id="a1ddd-122">Kun olet valmis, valitse **Tallenna Lifecycle Servicesiin**.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Tallenna Lifecycle Servicesiin](media/task-guides.png)

12. <span data-ttu-id="a1ddd-124">Valitse BPM-kirjasto ja solmu, johon tehtävätallenne tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="a1ddd-125">Toista tehtäväopas LCS-palvelusta seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="a1ddd-126">Käynnistä tehtävän tallennustoiminto.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-126">Start Task recorder.</span></span>
2. <span data-ttu-id="a1ddd-127">Valitse **Avaa LCS-palvelusta**.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="a1ddd-128">Valitse kirjasto ja BPM-solmu, jossa tallennettu tehtäväopas on.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="a1ddd-129">Avaa tehtäväopas.</span><span class="sxs-lookup"><span data-stu-id="a1ddd-129">Open the task guide.</span></span>

