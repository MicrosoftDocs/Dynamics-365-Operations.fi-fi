---
title: "Myymälän varaston hallinta"
description: "Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6245d37ace9f46ecce83a0cf80a014d5de898bbc
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="53d66-103">Myymälän varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="53d66-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="53d66-104">Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa.</span><span class="sxs-lookup"><span data-stu-id="53d66-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="53d66-105">Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.</span><span class="sxs-lookup"><span data-stu-id="53d66-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="53d66-106">Ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="53d66-106">Purchase orders</span></span>
<span data-ttu-id="53d66-107">Ostotilaukset luodaan pääkonttorilla.</span><span class="sxs-lookup"><span data-stu-id="53d66-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="53d66-108">Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään Microsoft Dynamics 365 for Retailin Modern POS- tai Cloud POS -sovelluksen Vähittäismyynti ja kauppa -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="53d66-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="53d66-109">Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="53d66-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="53d66-110">Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="53d66-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="53d66-111">Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa ostotilauksen **Ota vastaan nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="53d66-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="53d66-112">Siirtotilaukset</span><span class="sxs-lookup"><span data-stu-id="53d66-112">Transfer orders</span></span>
<span data-ttu-id="53d66-113">Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="53d66-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="53d66-114">Tässä tapauksessa siirtotilaus näkyy myymälässä poimintapyyntönä Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53d66-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="53d66-115">Kun pyydetyt määrät on kerätty, ne vahvistetaan ja lähetetään pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="53d66-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="53d66-116">Pääkonttorissa myymälässä kerätyt määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Lähetä nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="53d66-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="53d66-117">Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään.</span><span class="sxs-lookup"><span data-stu-id="53d66-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="53d66-118">Tässä tapauksessa siirtotilaus näkyy myymälässä vastaanottopyyntönä Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53d66-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="53d66-119">Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="53d66-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="53d66-120">Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="53d66-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="53d66-121">Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Ota vastaan nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="53d66-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="53d66-122">Varaston inventoinnit</span><span class="sxs-lookup"><span data-stu-id="53d66-122">Stock counts</span></span>
<span data-ttu-id="53d66-123">Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="53d66-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="53d66-124">Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi.</span><span class="sxs-lookup"><span data-stu-id="53d66-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="53d66-125">Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53d66-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="53d66-126">Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53d66-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="53d66-127">Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla.</span><span class="sxs-lookup"><span data-stu-id="53d66-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="53d66-128">Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille.</span><span class="sxs-lookup"><span data-stu-id="53d66-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="53d66-129">Pääkonttorissa inventointi tarkistetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="53d66-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="53d66-130">Varastohaku</span><span class="sxs-lookup"><span data-stu-id="53d66-130">Inventory lookup</span></span>
<span data-ttu-id="53d66-131">Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella varaston haku-sivulla.</span><span class="sxs-lookup"><span data-stu-id="53d66-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="53d66-132">Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä.</span><span class="sxs-lookup"><span data-stu-id="53d66-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="53d66-133">Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten **Näytä myymälän käytettävissä oleva määrä**.</span><span class="sxs-lookup"><span data-stu-id="53d66-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





