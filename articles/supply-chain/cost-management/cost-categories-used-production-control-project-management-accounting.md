---
title: "Tuotannonhallinnassa ja projektinhallinnan kirjanpidossa käytettävät kustannusluokat"
description: "Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa. Tässä artikkelissa on tietoja kustannusluokista, jotka on määritettävä tämäntyyppiselle tuotantotyölle tuotanto- ja projektitarkoituksiin."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1fcc7914f2bb283a746b5e10993f91f949818473
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="d2030-104">Tuotannonhallinnassa ja projektinhallinnan kirjanpidossa käytettävät kustannusluokat</span><span class="sxs-lookup"><span data-stu-id="d2030-104">Cost categories used in Production control and Project management accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2030-105">Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="d2030-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="d2030-106">Tässä artikkelissa on tietoja kustannusluokista, jotka on määritettävä tämäntyyppiselle tuotantotyölle tuotanto- ja projektitarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="d2030-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="d2030-107">Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="d2030-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="d2030-108">Tässä tapauksessa kustannusluokka tarvitaan tuotantoa ja projektia varten.</span><span class="sxs-lookup"><span data-stu-id="d2030-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="d2030-109">Kun kustannusluokka on merkitty käytettäväksi tuotannossa tai projekteissa, sille on määritettävä projektiin liittyviä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="d2030-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="d2030-110">Esimerkiksi projekteihin liittyvät tuntikustannukset saattavat poiketa tuotantoon liittyvistä tuntikustannuksista.</span><span class="sxs-lookup"><span data-stu-id="d2030-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="d2030-111">**Kustannusluokat**-sivun avulla voit määrittää kustannusluokan, jota käytetään tuotannonhallinnassa ja projektinhallinnan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="d2030-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> <span data-ttu-id="d2030-112">**Huomautus:** Kustannuslaskennalla on **Projektiluokat**-sivu, mutta tämä sivu ei liity tässä ohjeaiheessa kuvattuun toimintoon.</span><span class="sxs-lookup"><span data-stu-id="d2030-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="d2030-113">Kun käytät projektissa kustannusluokkaa, **Kustannusluokat**-sivulla on lisävälilehtiä, jotka sisältävät projektiin liittyviä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="d2030-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="d2030-114">Näihin tietoihin kuuluvat muun muassa luokkaryhmä, rivin ominaisuus ja kustannusluokkaan kohdistetut kirjanpitotilit.</span><span class="sxs-lookup"><span data-stu-id="d2030-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="d2030-115">Kustannusluokka on kohdistettava kustannusryhmään, joka tukee **Tunnit**-tapahtumatyyppiä.</span><span class="sxs-lookup"><span data-stu-id="d2030-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="d2030-116">Rivin ominaisuus ilmaisee oletustiedot siitä, kuinka raportoitu aika voidaan veloittaa projektissa.</span><span class="sxs-lookup"><span data-stu-id="d2030-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="d2030-117">Kustannuksiin ja myyntiin liittyvät kirjanpitotilit määräytyvät tavallisesti kustannusluokkaan kohdistetun luokkaryhmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2030-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="d2030-118">Yksittäiselle kustannusluokalle voidaan kuitenkin määrittää tiettyjä tilejä.</span><span class="sxs-lookup"><span data-stu-id="d2030-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="d2030-119">**Kustannusluokat**-sivun lisäpainikkeiden avulla voit tarkastella valittuun kustannusluokkaan liittyviä projektitietoja.</span><span class="sxs-lookup"><span data-stu-id="d2030-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="d2030-120">Voit esimerkiksi tarkastella projektiin liittyviä tapahtumia, määrittää työntekijöitä tai projekteja, määrittää tuntikustannuksia myyntihintoja sekä tarkastella raportteja.</span><span class="sxs-lookup"><span data-stu-id="d2030-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




