---
title: Luo online-kanava ja määritä kanavamääritteet
description: Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "312367"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="e1e0b-103">Luo online-kanava ja määritä kanavamääritteet</span><span class="sxs-lookup"><span data-stu-id="e1e0b-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e1e0b-104">Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="e1e0b-105">Organisaatiohierarkia on luotava ennen uuden online-kanavan luomista.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="e1e0b-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="e1e0b-107">Uuden online-kanavan luominen</span><span class="sxs-lookup"><span data-stu-id="e1e0b-107">Create a new online channel</span></span>
1. <span data-ttu-id="e1e0b-108">Valitse Vähittäismyynti ja kauppa > Kanavat > Verkkokaupat.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="e1e0b-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-109">Click New.</span></span>
3. <span data-ttu-id="e1e0b-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e1e0b-111">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="e1e0b-112">Valitse vaihtoehto Varaston aikavyöhyke -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="e1e0b-113">Syötä tai valitse arvo Oletusasiakas-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="e1e0b-114">Syötä tai valitse arvo Asiakkaan osoitekirja -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="e1e0b-115">Syötä tai valitse arvo Maksuehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="e1e0b-116">Anna tai valitse arvo Maksutapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="e1e0b-117">Syötä tai valitse arvo Sähköposti-ilmoitusprofiili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="e1e0b-118">Laajenna Taloushallinnon dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="e1e0b-119">Syötä tai valitse arvo BusinessUnit-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="e1e0b-120">Määritä samalla tavalla kaikkien muiden oletusdimensioiden arvot.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="e1e0b-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="e1e0b-122">Verkkokaupan lisääminen organisaatiohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="e1e0b-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="e1e0b-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-123">Close the page.</span></span>
2. <span data-ttu-id="e1e0b-124">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="e1e0b-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e1e0b-126">Valitse Näytä.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-126">Click View.</span></span>
5. <span data-ttu-id="e1e0b-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-127">Click Edit.</span></span>
    * <span data-ttu-id="e1e0b-128">Voit valita minkä tahansa hierarkiasolmun, josta haluat lisätä uuden kanavan.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="e1e0b-129">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-129">Click Insert.</span></span>
7. <span data-ttu-id="e1e0b-130">Valitse Vähittäismyyntikanava.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-130">Click Retail channel.</span></span>
8. <span data-ttu-id="e1e0b-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-131">Click OK.</span></span>
9. <span data-ttu-id="e1e0b-132">Valitse Julkaise, jolloin valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="e1e0b-133">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="e1e0b-134">Valitse Julkaise.</span><span class="sxs-lookup"><span data-stu-id="e1e0b-134">Click Publish.</span></span>

