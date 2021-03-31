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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2439d1912b3ca013f4a524f3354923d2a3f76ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221278"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="7fd8c-103">Myyntipisteen käyttöoikeusryhmien luominen</span><span class="sxs-lookup"><span data-stu-id="7fd8c-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fd8c-104">Tässä ohjeaiheessa kerrotaan, miten voit luoda myyntipisteen käyttöoikeusryhmän.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="7fd8c-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="7fd8c-106">Tämä tehtävä on tarkoitettu Commerce-toiminnoista vastaavan johtajan roolille.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="7fd8c-107">Siirry siirtymisruudussa kohtaan **Moduulit > Retail ja Commerce > Työntekijät > käyttöoikeusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="7fd8c-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-108">Select **New**.</span></span>
3. <span data-ttu-id="7fd8c-109">Syötä **Myyntipisteen käyttöoikeusryhmän tunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="7fd8c-110">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7fd8c-111">Valitse **Näytä aikamerkinnät** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="7fd8c-112">Voit ottaa käyttöön myyntipisteen käyttöoikeusryhmän käyttöoikeuksia tai poistaa niitä käytöstä.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="7fd8c-113">Joillekin käyttöoikeuksille voi määrittää arvon, jonka avulla arvioidaan, voiko myyntipisteen käyttäjä suorittaa toiminnon.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="7fd8c-114">Tässä tehtävän ohjauksessa otetaan käyttöön joitakin käyttöoikeuksia, jotka voidaan antaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="7fd8c-115">Valitse **Salli tilauksen luominen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="7fd8c-116">Valitse **Salli tilauksen muokkaaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="7fd8c-117">Valitse **Salli tilauksen noutaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="7fd8c-118">Valitse **Salli salasanan vaihtaminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="7fd8c-119">Valitse **Salli piilottava sulkeminen** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="7fd8c-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-120">Select **Save**.</span></span> <span data-ttu-id="7fd8c-121">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kaupankäyntikanaville.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="7fd8c-122">Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työt > Työt**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="7fd8c-123">Seuraavaksi liitetään myyntipisteen käyttöoikeusryhmä työhön.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="7fd8c-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7fd8c-125">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-125">Select **Edit**.</span></span>
15. <span data-ttu-id="7fd8c-126">Laajenna **Työn luokittelu** -osa.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="7fd8c-127">Syötä tai valitse arvo Myyntipisteen käyttöoikeusryhmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="7fd8c-128">Kaikki tämän työn toimissa olevat työntekijät käyttävät näitä myyntipisteen käyttöoikeusryhmän asetuksia, ellei työntekijöiden myyntipisteen käyttöoikeuksia ole ohitettu toimen tasolla.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="7fd8c-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-129">Select **Save**.</span></span> <span data-ttu-id="7fd8c-130">Kun muutokset on tallennettu, suorita henkilökunnan jakeluaikataulu ja siirrä muutokset kanaville.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]