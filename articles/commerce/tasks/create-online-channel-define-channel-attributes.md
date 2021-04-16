---
title: Luo online-kanava ja määritä kanavamääritteet
description: Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798510"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="cf1d9-103">Luo online-kanava ja määritä kanavamääritteet</span><span class="sxs-lookup"><span data-stu-id="cf1d9-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf1d9-104">Tässä menettelyssä kerrotaan, miten uusi online-kanava luodaan ja lisätään organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="cf1d9-105">Organisaatiohierarkia on luotava ennen uuden online-kanavan luomista.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="cf1d9-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="cf1d9-107">Uuden online-kanavan luominen</span><span class="sxs-lookup"><span data-stu-id="cf1d9-107">Create a new online channel</span></span>
1. <span data-ttu-id="cf1d9-108">Valitse Retail ja Commerce > Kanavat > Verkkokaupat.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="cf1d9-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-109">Click New.</span></span>
3. <span data-ttu-id="cf1d9-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cf1d9-111">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="cf1d9-112">Valitse vaihtoehto Varaston aikavyöhyke -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="cf1d9-113">Syötä tai valitse arvo Oletusasiakas-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="cf1d9-114">Syötä tai valitse arvo Asiakkaan osoitekirja -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="cf1d9-115">Syötä tai valitse arvo Maksuehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="cf1d9-116">Anna tai valitse arvo Maksutapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="cf1d9-117">Syötä tai valitse arvo Sähköposti-ilmoitusprofiili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="cf1d9-118">Laajenna Taloushallinnon dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="cf1d9-119">Syötä tai valitse arvo BusinessUnit-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="cf1d9-120">Määritä samalla tavalla kaikkien muiden oletusdimensioiden arvot.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="cf1d9-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="cf1d9-122">Verkkokaupan lisääminen organisaatiohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="cf1d9-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="cf1d9-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-123">Close the page.</span></span>
2. <span data-ttu-id="cf1d9-124">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="cf1d9-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cf1d9-126">Valitse Näytä.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-126">Click View.</span></span>
5. <span data-ttu-id="cf1d9-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-127">Click Edit.</span></span>
    * <span data-ttu-id="cf1d9-128">Voit valita minkä tahansa hierarkiasolmun, josta haluat lisätä uuden kanavan.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="cf1d9-129">Valitse Lisää.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-129">Click Insert.</span></span>
7. <span data-ttu-id="cf1d9-130">Valitse Commerce-kanava.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="cf1d9-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-131">Click OK.</span></span>
9. <span data-ttu-id="cf1d9-132">Valitse Julkaise, jolloin valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="cf1d9-133">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="cf1d9-134">Valitse Julkaise.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="cf1d9-135">Tilausten määrittäminen lähes reaaliaikaista ilmoitusta varten</span><span class="sxs-lookup"><span data-stu-id="cf1d9-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="cf1d9-136">Valitse Retail ja Commerce > Pääkonttorin asetukset > Parametrit > Commerce-parametrit.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="cf1d9-137">Määritä Käytä reaaliaikaista palvelua verkkokauppatilausten luontiin asetukseksi "kyllä".</span><span class="sxs-lookup"><span data-stu-id="cf1d9-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="cf1d9-138">Suorita 1070-jakeluaikataulu, kun synkronoit muutokset kanavatietokannan kanssa.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]