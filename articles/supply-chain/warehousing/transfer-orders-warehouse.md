---
title: Siirtotilausten varastojen määrittäminen
description: Tässä ohjeaiheessa käsitellään siirtotilausten varastojen määrittämistä.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8111601cb2948c66097b0f5b2f261b7462b279f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "337460"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="53c97-103">Siirtotilausten varastojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="53c97-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53c97-104">Varastotasoja käyttämällä voidaan luoda hierarkia, joka tukee varastojen välisiä siirtotilauksia.</span><span class="sxs-lookup"><span data-stu-id="53c97-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="53c97-105">Tämän määrityksen mukaan pääajoitus laskee nimikkeiden tarpeen kullakin varastotasolla ja täyttää tarpeet luomalla suunnitellut siirtotilaukset, joiden mukaan siirtäminen tapahtuu varastojen välillä.</span><span class="sxs-lookup"><span data-stu-id="53c97-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="53c97-106">Valitse **Varastonhallinta > Asetukset > Inventaarioanalyysi > Varastot**.</span><span class="sxs-lookup"><span data-stu-id="53c97-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="53c97-107">Valitse varasto, jota haluat täydentää.</span><span class="sxs-lookup"><span data-stu-id="53c97-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="53c97-108">Valitse **Pääsuunnittelu**-pikavälilehdessä **Uudelleentäyttö**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="53c97-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="53c97-109">Valitse **Päävarasto**-kentässä varasto, jota haluat käyttää täydennysvarastona.</span><span class="sxs-lookup"><span data-stu-id="53c97-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="53c97-110">Pääajoitus laskee valittua varastoa koskevan siirtovaatimuksen ja luo suunnitellun siirtotilauksen, jonka mukaan siirto tapahtuu määritetystä **päävarastosta**.</span><span class="sxs-lookup"><span data-stu-id="53c97-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="53c97-111">Jos tyhjennät <STRONG>Uudelleentäyttö</STRONG>-valintaruudun, valitulle varastolle määritetään <STRONG>päävarastoa</STRONG> koskeva varastotaso, mutta <STRONG>päävarastoa</STRONG> ei määritetä täydennysvarastoksi.</span><span class="sxs-lookup"><span data-stu-id="53c97-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="53c97-112">Valitse sivu, joilla uusia asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="53c97-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="53c97-113">Jos haluat määrittää varaston täydennystä varten, määritä varasto ensin varastodimensioksi <STRONG>Varastodimensioryhmät</STRONG>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="53c97-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="53c97-114">Valitse tällä sivulla <STRONG>Aktiivinen</STRONG>-kenttä ja varaston <STRONG>Kattavuussuunnitelma dimension mukaan</STRONG> -kenttä.</span><span class="sxs-lookup"><span data-stu-id="53c97-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="53c97-115">Kuljetusajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="53c97-115">Set up transport lead time</span></span>

<span data-ttu-id="53c97-116">Määritä myös varastojen välinen kuljetusaika **Kuljetusvuorokaudet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="53c97-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="53c97-117">Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Toimitus > Kuljetusvuorokaudet**.</span><span class="sxs-lookup"><span data-stu-id="53c97-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="53c97-118">Valitse **Vastaanottopiste**-kentässä **varasto**.</span><span class="sxs-lookup"><span data-stu-id="53c97-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="53c97-119">Valitse **Lähetysvarasto**, **Vastaanottovarasto** ja **Kuljetusvuorokaudet**.</span><span class="sxs-lookup"><span data-stu-id="53c97-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="53c97-120">(Valinnainen) Voit määrittää myös kuljetusajan toimitustavan mukaan **Kuljetuspäivät toimitustavan mukaan** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="53c97-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>