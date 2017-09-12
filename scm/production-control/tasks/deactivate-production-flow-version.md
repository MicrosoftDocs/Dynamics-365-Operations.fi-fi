--- 
title: Poista tuotantovirran version aktivointi
description: "Kun aktiivista tuotantovirran versiota ei enää tarvita, se voidaan poistaa käytöstä."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db4b2857e9a7c99ee6fa4ef397f7ed99335faba
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="920e5-103">Poista tuotantovirran version aktivointi</span><span class="sxs-lookup"><span data-stu-id="920e5-103">Deactivate a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="920e5-104">Kun aktiivista tuotantovirran versiota ei enää tarvita, se voidaan poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="920e5-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="920e5-105">Käytä tätä vaihtoehtoa vain, jos kaikki kanban-säännöt ja aktiviteetit ovat päättyneet, eikä niitä aktivoida uudelleen.</span><span class="sxs-lookup"><span data-stu-id="920e5-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="920e5-106">Huomaa, että kaikkien tämän tuotantovirran versioon liittyvien kanban-sääntöjen päättymispäivämääräksi asetetaan nykyinen päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="920e5-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="920e5-107">Jos haluat muokata aktiivisen tuotantovirran versiota, harkitse vanhentumispäivämäärän asettamista on aktiiviselle versiolle, jonka jälkeen voit luoda uuden version.</span><span class="sxs-lookup"><span data-stu-id="920e5-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="920e5-108">Näin voit jatkaa antaa tuotantosi jatkua samalla, kun valmistelet uutta versiota ja siihen liittyviä kanban-sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="920e5-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="920e5-109">Jotta aktiivisen tuotantovirran versio voisi poistaa käytöstä, sille on määritettävä vanhentumispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="920e5-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="920e5-110">Tavallaan siis käytöstä poistaminen on enemmänkin poikkeus kuin sääntö.</span><span class="sxs-lookup"><span data-stu-id="920e5-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="920e5-111">Tätä menettelyä varten tarvitset tuotantovirran, jolla on käytöstä poistettava versio.</span><span class="sxs-lookup"><span data-stu-id="920e5-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="920e5-112">Älä tee tätä tuotantoympäristössä, jos et ole täysin varma, että versio on täysin tarpeeton.</span><span class="sxs-lookup"><span data-stu-id="920e5-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="920e5-113">Poista tuotantovirran version aktivointi</span><span class="sxs-lookup"><span data-stu-id="920e5-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="920e5-114">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="920e5-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="920e5-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="920e5-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="920e5-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="920e5-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="920e5-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="920e5-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="920e5-118">Valitse Poista käytöstä.</span><span class="sxs-lookup"><span data-stu-id="920e5-118">Click Deactivate.</span></span>
    * <span data-ttu-id="920e5-119">Älä jatka, jos et ole täysin varma, että tämän tuotantovirran versio on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="920e5-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="920e5-120">Valitsemalla Ok asetat kaikki aktiiviset kanban-säännöt vanhentuneeksi; kaikki tämän tuotantovirran version tuotanto- ja täydennysaktiviteetit pysäytetään välittömästi.</span><span class="sxs-lookup"><span data-stu-id="920e5-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="920e5-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="920e5-121">Click OK.</span></span>


