---
title: "Alusta Retail-ympäristössä alkutiedot"
description: "Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Microsoft Dynamics 365 for Retailin alustusprosessia."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d3c81aaa675352eb679c1e1540f947c1d1da804b
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="c988d-103">Alusta Retail-ympäristössä alkutiedot</span><span class="sxs-lookup"><span data-stu-id="c988d-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c988d-104">Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Microsoft Dynamics 365 for Retailin alustusprosessia.</span><span class="sxs-lookup"><span data-stu-id="c988d-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="c988d-105">Kun Retail-sovellus on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava vähittäismyyntikonfiguraatio luodaksesi peruskonfiguraation tiedot.</span><span class="sxs-lookup"><span data-stu-id="c988d-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="c988d-106">**Tärkeää:** Ennen kuin alustat vähittäismyyntikonfiguraation, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität vähittäismyyntiliikkeitä.</span><span class="sxs-lookup"><span data-stu-id="c988d-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="c988d-107">Tämä vaihe on suoritettava kullekin yritykselle, jota käytät vähittäismyyntiin.</span><span class="sxs-lookup"><span data-stu-id="c988d-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="c988d-108">Alusta vähittäismyyntikonfiguraatio noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="c988d-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="c988d-109">Käynnistä Dynamics 365 for Retail -asiakasohjelma</span><span class="sxs-lookup"><span data-stu-id="c988d-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="c988d-110">Valitse **Vähittäismyynti** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Vähittäismyyntiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="c988d-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="c988d-111">Napsauta **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="c988d-111">Click **Initialize**.</span></span>

<span data-ttu-id="c988d-112">Alustaminen luo seuraavat oletusmääritystiedot:</span><span class="sxs-lookup"><span data-stu-id="c988d-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="c988d-113">Retail-ajastuksen työt ja alityöt</span><span class="sxs-lookup"><span data-stu-id="c988d-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="c988d-114">Vähittäismyyntikanavan skeema</span><span class="sxs-lookup"><span data-stu-id="c988d-114">Retail channel schema</span></span>
-   <span data-ttu-id="c988d-115">Vähittäismyyntijakelun aikataulut</span><span class="sxs-lookup"><span data-stu-id="c988d-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="c988d-116">Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat</span><span class="sxs-lookup"><span data-stu-id="c988d-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="c988d-117">Aikavyöhyketiedot</span><span class="sxs-lookup"><span data-stu-id="c988d-117">Time zone information</span></span>
-   <span data-ttu-id="c988d-118">Myyntipisteen (POS) toiminnot:</span><span class="sxs-lookup"><span data-stu-id="c988d-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="c988d-119">Myyntipisteen käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="c988d-119">POS permissions</span></span>
-   <span data-ttu-id="c988d-120">Kanavaraportit</span><span class="sxs-lookup"><span data-stu-id="c988d-120">Channel reports</span></span>
-   <span data-ttu-id="c988d-121">Määritteen metatiedot</span><span class="sxs-lookup"><span data-stu-id="c988d-121">Attribute metadata</span></span>
-   <span data-ttu-id="c988d-122">Yksikön tarkistusmallit</span><span class="sxs-lookup"><span data-stu-id="c988d-122">Entity validation templates</span></span>
-   <span data-ttu-id="c988d-123">Komentojonotyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen</span><span class="sxs-lookup"><span data-stu-id="c988d-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="c988d-124">Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Dynamics 365 for Retailin tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="c988d-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="c988d-125">**Huomautus:** Retail-ajastus voidaan määrittää erikseen.</span><span class="sxs-lookup"><span data-stu-id="c988d-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="c988d-126">Tämä vaihtoehto mahdollistaa Retail-ajastuksen määrityksen sen oletusasetuksille.</span><span class="sxs-lookup"><span data-stu-id="c988d-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="c988d-127">Kun alustus on valmis, sinun määritettävä vähittäismyynnin lisätiedot.</span><span class="sxs-lookup"><span data-stu-id="c988d-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="c988d-128">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="c988d-128">Here are some examples:</span></span>

-   <span data-ttu-id="c988d-129">Vähittäismyynnin parametrit</span><span class="sxs-lookup"><span data-stu-id="c988d-129">Retail parameters</span></span>
-   <span data-ttu-id="c988d-130">Retail-ajastuksen parametrit</span><span class="sxs-lookup"><span data-stu-id="c988d-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="c988d-131">Vähittäismyyntikanavat</span><span class="sxs-lookup"><span data-stu-id="c988d-131">Retail channels</span></span>
-   <span data-ttu-id="c988d-132">Kassakoneet ja laitteet</span><span class="sxs-lookup"><span data-stu-id="c988d-132">Registers and devices</span></span>
-   <span data-ttu-id="c988d-133">Valikoimat</span><span class="sxs-lookup"><span data-stu-id="c988d-133">Assortments</span></span>





