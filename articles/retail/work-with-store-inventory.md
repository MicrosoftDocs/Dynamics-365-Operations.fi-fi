---
title: "Myymälän varastonhallinta"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="store-inventory-management"></a><span data-ttu-id="99a23-103">Myymälän varastonhallinta</span><span class="sxs-lookup"><span data-stu-id="99a23-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99a23-104">Tässä artikkelissa asiakirjatyypit, joiden avulla hallitaan varastoa.</span><span class="sxs-lookup"><span data-stu-id="99a23-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="99a23-105">Organisaation varastoa voi hallita seuraavien asiakirjatyyppien avulla.</span><span class="sxs-lookup"><span data-stu-id="99a23-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="99a23-106">Ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="99a23-106">Purchase orders</span></span>
<span data-ttu-id="99a23-107">Ostotilaukset luodaan pääkonttorilla.</span><span class="sxs-lookup"><span data-stu-id="99a23-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="99a23-108">Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään Microsoft Dynamics 365 for Retailin Modern POS- tai Cloud POS -sovelluksen Vähittäismyynti ja kauppa -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="99a23-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="99a23-109">Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="99a23-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="99a23-110">Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="99a23-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="99a23-111">Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa ostotilauksen **Ota vastaan nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99a23-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="99a23-112">Siirtotilaukset</span><span class="sxs-lookup"><span data-stu-id="99a23-112">Transfer orders</span></span>
<span data-ttu-id="99a23-113">Siirtotilaus voi määrittää, että nimikkeet lähetetään tietystä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="99a23-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="99a23-114">Tässä tapauksessa siirtotilaus näkyy myymälässä poimintapyyntönä Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="99a23-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="99a23-115">Kun pyydetyt määrät on kerätty, ne vahvistetaan ja lähetetään pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="99a23-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="99a23-116">Pääkonttorissa myymälässä kerätyt määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Lähetä nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99a23-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="99a23-117">Siirtotilaus voi määrittää, että nimikkeet lähetetään tiettyyn myymälään.</span><span class="sxs-lookup"><span data-stu-id="99a23-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="99a23-118">Tässä tapauksessa siirtotilaus näkyy myymälässä vastaanottopyyntönä Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="99a23-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="99a23-119">Kun myymälään vastaanotetut määrät on syötetty, ne voidaan tallentaa paikallisesti muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="99a23-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="99a23-120">Vaihtoehtoisesti määrät voidaan vahvistaa ja lähettää pääkonttoriin.</span><span class="sxs-lookup"><span data-stu-id="99a23-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="99a23-121">Pääkonttorissa myymälään vastaanotetut määrät näytetään Microsoft Dynamics 365 for Retailissa siirtotilauksen **Ota vastaan nyt** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99a23-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="99a23-122">Varaston inventoinnit</span><span class="sxs-lookup"><span data-stu-id="99a23-122">Stock counts</span></span>
<span data-ttu-id="99a23-123">Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="99a23-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="99a23-124">Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi.</span><span class="sxs-lookup"><span data-stu-id="99a23-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="99a23-125">Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="99a23-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="99a23-126">Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="99a23-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="99a23-127">Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla.</span><span class="sxs-lookup"><span data-stu-id="99a23-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="99a23-128">Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille.</span><span class="sxs-lookup"><span data-stu-id="99a23-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="99a23-129">Pääkonttorissa inventointi tarkistetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="99a23-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="99a23-130">Varastohaku</span><span class="sxs-lookup"><span data-stu-id="99a23-130">Inventory lookup</span></span>
<span data-ttu-id="99a23-131">Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella varaston haku-sivulla.</span><span class="sxs-lookup"><span data-stu-id="99a23-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="99a23-132">Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä.</span><span class="sxs-lookup"><span data-stu-id="99a23-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="99a23-133">Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten **Näytä myymälän käytettävissä oleva määrä**.</span><span class="sxs-lookup"><span data-stu-id="99a23-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





