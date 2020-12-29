---
title: Toimittajien hyväksyminen tiettyihin hankintaluokkiin
description: Tässä ohjeaiheessa selitetään, miten tiettyjen hankintaluokkien toimittajat hyväksytään Dynamics 365 Supply Chain Managementissa.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427018"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="c7559-103">Toimittajien hyväksyminen tiettyihin hankintaluokkiin</span><span class="sxs-lookup"><span data-stu-id="c7559-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7559-104">Tässä ohjeaiheessa selitetään, miten tiettyjen hankintaluokkien toimittajat hyväksytään Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="c7559-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c7559-105">Ostoehdotusta luotaessa saattaa olla tarpeen valita hyväksytty tai ensisijainen toimittaja sen mukaan, miten ostokäytännöt on määritetty.</span><span class="sxs-lookup"><span data-stu-id="c7559-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="c7559-106">Seuraavassa menettelyssä kuvataan, miten toimittaja määritetään hyväksytyksi tai ensisijaiseksi tietylle hankintaluokalle.</span><span class="sxs-lookup"><span data-stu-id="c7559-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="c7559-107">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="c7559-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="c7559-108">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="c7559-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="c7559-109">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="c7559-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c7559-110">Valitse toimittaja, jonka haluat määrittää hyväksytyksi tai ensisijaiseksi tietylle luokalle.</span><span class="sxs-lookup"><span data-stu-id="c7559-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="c7559-111">Valitse toimintoruudussa **Yleiset**.</span><span class="sxs-lookup"><span data-stu-id="c7559-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c7559-112">Valitse **Luokat**.</span><span class="sxs-lookup"><span data-stu-id="c7559-112">Select **Categories**.</span></span>
5. <span data-ttu-id="c7559-113">Valitse **Lisää luokka**.</span><span class="sxs-lookup"><span data-stu-id="c7559-113">Select **Add category**.</span></span>
6. <span data-ttu-id="c7559-114">Valitse **Luokka**-kenttään **TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET (TOIMISTON JA TYÖPÖYDÄN LISÄVARUSTEET)**.</span><span class="sxs-lookup"><span data-stu-id="c7559-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="c7559-115">Valitse **Toimittajaluokan tila** -kenttään **Ensisijainen**.</span><span class="sxs-lookup"><span data-stu-id="c7559-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="c7559-116">Luokalle on mahdollista määrittää useampi kuin yksi ensisijainen toimittaja.</span><span class="sxs-lookup"><span data-stu-id="c7559-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="c7559-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c7559-117">Select **Save**.</span></span>
9. <span data-ttu-id="c7559-118">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="c7559-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="c7559-119">Valitse puusta **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span><span class="sxs-lookup"><span data-stu-id="c7559-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="c7559-120">Laajenna **Toimittajat**-osa.</span><span class="sxs-lookup"><span data-stu-id="c7559-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="c7559-121">Tarkista, että valitsemasi toimittaja näkyy ensisijaisten toimittajien luettelossa Toimiston ja työpöydän lisävarusteet -luokassa.</span><span class="sxs-lookup"><span data-stu-id="c7559-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="c7559-122">Jos käytät tätä menettelyä tehtäväoppaana, saatat joutua napsauttamaan **Poista lukitus** -painiketta voidaksesi selata alas toimittajaluetteloon.</span><span class="sxs-lookup"><span data-stu-id="c7559-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="c7559-123">On myös mahdollista lisätä ensisijaisia ja hyväksyttyjä toimittajia tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="c7559-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="c7559-124">Laajenna puurakenteessa **OFFICE AND DESK ACCESSORIES** ja valitse **Scissors**.</span><span class="sxs-lookup"><span data-stu-id="c7559-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="c7559-125">Valitse **Ei** **Peri toimittajat ylemmän tason luokalta** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c7559-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="c7559-126">Valitse **Kyllä** **Peri toimittajat ylemmän tason luokalta** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c7559-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

