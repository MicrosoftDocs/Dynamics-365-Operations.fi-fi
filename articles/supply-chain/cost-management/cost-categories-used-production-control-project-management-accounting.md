---
title: Tuotannonhallinnassa ja projektinhallinnan kirjanpidossa käytettävät kustannusluokat
description: Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa. Tässä artikkelissa on tietoja kustannusluokista, jotka on määritettävä tämäntyyppiselle tuotantotyölle tuotanto- ja projektitarkoituksiin.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26f4ce073528bf102a951d6fa002aeb0da9e380c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426960"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="ddffe-104">Tuotannonhallinnassa ja projektinhallinnan kirjanpidossa käytettävät kustannusluokat</span><span class="sxs-lookup"><span data-stu-id="ddffe-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddffe-105">Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="ddffe-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="ddffe-106">Tässä artikkelissa on tietoja kustannusluokista, jotka on määritettävä tämäntyyppiselle tuotantotyölle tuotanto- ja projektitarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="ddffe-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="ddffe-107">Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="ddffe-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="ddffe-108">Tässä tapauksessa kustannusluokka tarvitaan tuotantoa ja projektia varten.</span><span class="sxs-lookup"><span data-stu-id="ddffe-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="ddffe-109">Kun kustannusluokka on merkitty käytettäväksi tuotannossa tai projekteissa, sille on määritettävä projektiin liittyviä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="ddffe-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="ddffe-110">Esimerkiksi projekteihin liittyvät tuntikustannukset saattavat poiketa tuotantoon liittyvistä tuntikustannuksista.</span><span class="sxs-lookup"><span data-stu-id="ddffe-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="ddffe-111">**Kustannusluokat**-sivun avulla voit määrittää kustannusluokan, jota käytetään tuotannonhallinnassa ja projektinhallinnan kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="ddffe-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="ddffe-112">**Huomautus:** Kustannuslaskennalla on **Projektiluokat**-sivu, mutta tämä sivu ei liity tässä ohjeaiheessa kuvattuun toimintoon.</span><span class="sxs-lookup"><span data-stu-id="ddffe-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="ddffe-113">Kun käytät projektissa kustannusluokkaa, **Kustannusluokat**-sivulla on lisävälilehtiä, jotka sisältävät projektiin liittyviä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="ddffe-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="ddffe-114">Näihin tietoihin kuuluvat muun muassa luokkaryhmä, rivin ominaisuus ja kustannusluokkaan kohdistetut kirjanpitotilit.</span><span class="sxs-lookup"><span data-stu-id="ddffe-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="ddffe-115">Kustannusluokka on kohdistettava kustannusryhmään, joka tukee **Tunnit**-tapahtumatyyppiä.</span><span class="sxs-lookup"><span data-stu-id="ddffe-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="ddffe-116">Rivin ominaisuus ilmaisee oletustiedot siitä, kuinka raportoitu aika voidaan veloittaa projektissa.</span><span class="sxs-lookup"><span data-stu-id="ddffe-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="ddffe-117">Kustannuksiin ja myyntiin liittyvät kirjanpitotilit määräytyvät tavallisesti kustannusluokkaan kohdistetun luokkaryhmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="ddffe-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="ddffe-118">Yksittäiselle kustannusluokalle voidaan kuitenkin määrittää tiettyjä tilejä.</span><span class="sxs-lookup"><span data-stu-id="ddffe-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="ddffe-119">**Kustannusluokat**-sivun lisäpainikkeiden avulla voit tarkastella valittuun kustannusluokkaan liittyviä projektitietoja.</span><span class="sxs-lookup"><span data-stu-id="ddffe-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="ddffe-120">Voit esimerkiksi tarkastella projektiin liittyviä tapahtumia, määrittää työntekijöitä tai projekteja, määrittää tuntikustannuksia myyntihintoja sekä tarkastella raportteja.</span><span class="sxs-lookup"><span data-stu-id="ddffe-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



