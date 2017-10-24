---
title: "Nimikkeen tai raaka-aineen jäljittäminen"
description: "Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="1d798-103">Nimikkeen tai raaka-aineen jäljittäminen</span><span class="sxs-lookup"><span data-stu-id="1d798-103">Trace an item or raw material</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d798-104">Tässä menettelyssä käsitellään, miten nimikkeen seurannalla voidaan selvittää, miten nimikkeitä tai raaka-aineita on käytetty tai ollaan käyttämässä.</span><span class="sxs-lookup"><span data-stu-id="1d798-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="1d798-105">Tämän menettelyn avulla voit tunnistaa nimikkeen sekä seurata sitä takaisin lähteeseen ja sitten tuotannon ja myynnin kautta lopulliseen tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="1d798-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="1d798-106">Prosessilla voit selvittää esimerkiksi, mitä asiakkaita tai myyntitilauksia se koski.</span><span class="sxs-lookup"><span data-stu-id="1d798-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="1d798-107">Menettely käyttää USP2-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="1d798-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="1d798-108">Jäljitä nimike taaksepäin tiedossa olevaan eränumeroon</span><span class="sxs-lookup"><span data-stu-id="1d798-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="1d798-109">Valitse Inventoinnin- ja varastonhallinta > Kyselyt ja raportit > Seurantadimensiot > Nimikkeen seuranta.</span><span class="sxs-lookup"><span data-stu-id="1d798-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="1d798-110">Valitse Nimiketunnus-kenttään P9100.</span><span class="sxs-lookup"><span data-stu-id="1d798-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="1d798-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1d798-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1d798-112">Valitse Eteen- tai taaksepäin -kentässä Taaksepäin.</span><span class="sxs-lookup"><span data-stu-id="1d798-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="1d798-113">Valitse Eränumero-kentässä as 12-344-01.</span><span class="sxs-lookup"><span data-stu-id="1d798-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="1d798-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1d798-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="1d798-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1d798-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="1d798-116">Tunnista nimike, seuraa sitä eteenpäin ja analysoi</span><span class="sxs-lookup"><span data-stu-id="1d798-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="1d798-117">Puun ylin solmu vastaa valitun nimikkeen ja erän käytettävissä olevaa määrää.</span><span class="sxs-lookup"><span data-stu-id="1d798-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="1d798-118">Laajenna puun nimike, jotta voit paikantaa nimikkeen, jolle seuranta tulisi suorittaa.</span><span class="sxs-lookup"><span data-stu-id="1d798-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="1d798-119">Laajenna puussa "alla kuvatut solmut ja valitse sitten viimeinen solmu".</span><span class="sxs-lookup"><span data-stu-id="1d798-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="1d798-120">Laajenna: P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101 ja valitse sitten kyseinen solmu.</span><span class="sxs-lookup"><span data-stu-id="1d798-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="1d798-121">Laajenna puussa "alla kuvattu solmu ja valitse sitten kyseinen solmu".</span><span class="sxs-lookup"><span data-stu-id="1d798-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="1d798-122">Laajenna valitusta solmusta lähtien "M9103 ● Tuotantorivi B-000050 ● 12/9/2015 ●-160.00 lb ● Koko=70,Väri=OK, Toimipaikka=1, Varasto=10, Eränumero=App01" ja valitse sitten kyseinen solmu.</span><span class="sxs-lookup"><span data-stu-id="1d798-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="1d798-123">Valitse Seuraa solmusta.</span><span class="sxs-lookup"><span data-stu-id="1d798-123">Click Trace from node.</span></span>
4. <span data-ttu-id="1d798-124">Valitse Eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="1d798-124">Click Forward.</span></span>
5. <span data-ttu-id="1d798-125">Valitse toimintoruudussa Jäljitys.</span><span class="sxs-lookup"><span data-stu-id="1d798-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="1d798-126">Seurantavaihtoehtoja on useita; ne tarjoavat tietoja asiakkaista, joihin seurattava nimike vaikuttaa sekä myyntitilauksista, jotka liittyvät nimikkeeseen, oli niitä lähetetty tai ei.</span><span class="sxs-lookup"><span data-stu-id="1d798-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="1d798-127">Valitse Asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="1d798-127">Click Customers.</span></span>
7. <span data-ttu-id="1d798-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1d798-128">Close the page.</span></span>
8. <span data-ttu-id="1d798-129">Valitse toimintoruudussa Jäljitys.</span><span class="sxs-lookup"><span data-stu-id="1d798-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="1d798-130">Valitse Lähetetyt myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1d798-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="1d798-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1d798-131">Close the page.</span></span>

