---
title: Luo tuotantotilauksia
description: Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "324626"
---
# <a name="create-production-orders"></a><span data-ttu-id="5c4f6-105">Luo tuotantotilauksia</span><span class="sxs-lookup"><span data-stu-id="5c4f6-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c4f6-106">Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="5c4f6-107">Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="5c4f6-108">Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="5c4f6-109">Tuotantotilaus etenee tuotannon elinkaaren vaiheesta toiseen.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="5c4f6-110">Kun tilaus luodaan, sen tilaksi määritetään **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="5c4f6-111">Kun tilaus on valmis, sen tilaksi määritetään **Päättynyt**.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="5c4f6-112">Käyttäjä voi määrittää kunkin vaiheen kyseisen vaiheen parametriasetuksella.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="5c4f6-113">Asetus voidaan määrittää yhdelle käyttäjälle tai kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="5c4f6-114">Tuotannon tuoterakenne ja tuotantoreititys ovat tuotantotilauksen tärkeimmät yksiköt.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="5c4f6-115">Ne kopioidaan tuotantotilaukseen tuotettavaksi valitun nimikkeen ja määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="5c4f6-116">Tuotannon tuoterakennetta ja reititystä voidaan muokata ennen tuotantotilauksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="5c4f6-117">Tuotantotilaus voidaan luoda seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="5c4f6-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="5c4f6-118">Luotu toteuttamalla materiaaliin kysyntään perustuva pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="5c4f6-119">Luotu suoraan myyntitilausriviltä tai luotaessa ja arvioitaessa ylemmän tason tuotantotilaus (tarvekohdistus).</span><span class="sxs-lookup"><span data-stu-id="5c4f6-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="5c4f6-120">Luo manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5c4f6-120">Created manually.</span></span>




