---
title: Luo myyntipisteen (POS) visuaaliset profiilit
description: Tässä menetelmässä kerrotaan, miten uuden myyntipisteen visuaalinen profiili luodaan.
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b265a94c6d8f9e2534e1509e4f33c6f8a05eded0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140932"
---
# <a name="create-point-of-sale-pos-visual-profiles"></a><span data-ttu-id="8c8a1-103">Luo myyntipisteen (POS) visuaaliset profiilit</span><span class="sxs-lookup"><span data-stu-id="8c8a1-103">Create point of sale (POS) visual profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c8a1-104">Tässä menetelmässä kerrotaan, miten uuden myyntipisteen visuaalinen profiili luodaan.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="8c8a1-105">Visuaalinen profiili sisältää perustiedot, jotka määrittävät kassakoneiden ulkoasun.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="8c8a1-106">Voit luoda useita visuaalisia profiileja sekä liittää tietyissä kassakoneissa käytettävät yksilölliset profiilit.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="8c8a1-107">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="8c8a1-108">Siirry kohtaan Retail ja Commerce > Kanavan asetukset > Myyntipisteen asetukset > Myyntipisteen profiilit > Visuaaliset profiilit.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-108">Go to Retail and Commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="8c8a1-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-109">Click New.</span></span>
3. <span data-ttu-id="8c8a1-110">Kirjoita arvo Profiilinumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="8c8a1-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8c8a1-112">Avaa haku valitsemalla Sovellustyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8c8a1-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8c8a1-114">Avaa haku valitsemalla Teema-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8c8a1-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8c8a1-116">Avaa haku valitsemalla Korostuksen väri -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-116">In the Accent color field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8c8a1-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8c8a1-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8c8a1-119">Ota käyttöön Kirjautumisen tausta -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="8c8a1-120">Valitse tai syötä Vaakatulostuskuvan tunnus -kenttään kuvan tunnus.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="8c8a1-121">Valitse tai syötä Pystykuvan tunnus -kenttään kuvan tunnus.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-121">In the Portrait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="8c8a1-122">Ota käyttöön Tausta-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="8c8a1-123">RequestPopup - kuvan tunnus.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="8c8a1-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8c8a1-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-125">Click Save.</span></span>

