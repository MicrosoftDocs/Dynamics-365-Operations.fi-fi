---
title: Myyntipisteen käyttöoikeusryhmien luominen
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022387"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="c9e2e-103">Myyntipisteen käyttöoikeusryhmien luominen</span><span class="sxs-lookup"><span data-stu-id="c9e2e-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c9e2e-104">Tässä ohjeaiheessa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="c9e2e-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="c9e2e-106">Tämä tehtävä on tarkoitettu Commerce-toiminnoista vastaavan johtajan roolille.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="c9e2e-107">Siirry siirtymisruudussa kohtaan **Moduulit > Retail ja Commerce > Työntekijät > käyttöoikeusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="c9e2e-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-108">Select **New**.</span></span>
3. <span data-ttu-id="c9e2e-109">Syötä **Myyntipisteen käyttöoikeusryhmän tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="c9e2e-110">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c9e2e-111">Valitse **Näytä aikamerkinnät** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="c9e2e-112">Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="c9e2e-113">Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="c9e2e-114">Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="c9e2e-115">Valitse **Salli tilauksen luominen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="c9e2e-116">Valitse **Salli tilauksen muokkaaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="c9e2e-117">Valitse **Salli tilauksen noutaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="c9e2e-118">Valitse **Salli salasanan vaihtaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="c9e2e-119">Valitse **Salli piilottava sulkeminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="c9e2e-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-120">Select **Save**.</span></span> <span data-ttu-id="c9e2e-121">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kaupankäyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="c9e2e-122">Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työt > Työt**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="c9e2e-123">Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="c9e2e-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c9e2e-125">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-125">Select **Edit**.</span></span>
15. <span data-ttu-id="c9e2e-126">Laajenna **Työn luokittelu** -osa.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="c9e2e-127">Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="c9e2e-128">Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="c9e2e-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-129">Select **Save**.</span></span> <span data-ttu-id="c9e2e-130">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kanaville.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  
