---
title: Haamunimikkeet
description: Tässä ohjeaiheessa kuvataan yksityiskohtaisesti, miten haamurivityyppiä voidaan käyttää tuoterakenteen riveillä ja Dynamics 365 Supply Chain Managementin kaavassa.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980739"
---
# <a name="phantom-items"></a><span data-ttu-id="a28f0-103">Haamunimikkeet</span><span class="sxs-lookup"><span data-stu-id="a28f0-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a28f0-104">Tässä ohjeaiheessa kuvataan yksityiskohtaisesti, miten haamurivityyppiä voidaan käyttää tuoterakenteen (BOM) riveillä ja lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="a28f0-105">Seuraavassa kuvassa (a) on tuotteen H sekä osien F ja G tuoterakenne ja (b) on tuotteen H ja osan F reititystaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Tuote H ja osa F](media/product-H-part-F.png)


<span data-ttu-id="a28f0-107">Tässä kuvassa näytetään esimerkki tuoterakenteesta kahdella tasolla.</span><span class="sxs-lookup"><span data-stu-id="a28f0-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="a28f0-108">Lopputuote H vastaa koneen kokoonpanon tuotetta.</span><span class="sxs-lookup"><span data-stu-id="a28f0-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="a28f0-109">Koneen kokoonpanossa on kaksi osaa: sähköinen yksikkö (F), jossa on kaksi materiaalia (A ja B), ja pakkausmateriaalien ryhmä (G), jossa on myös kaksi materiaalia (C ja D).</span><span class="sxs-lookup"><span data-stu-id="a28f0-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="a28f0-110">Toista materiaalia (E) käytetään koneen yleisen kokoonpanon aikana.</span><span class="sxs-lookup"><span data-stu-id="a28f0-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Tuote H ja osa F](media/product-H-part-B.png)

<span data-ttu-id="a28f0-112">Edellinen kuva edustaa tuotteen H tuotannon tuoterakennetta. Tämä rakenne antaa hyvän yleiskatsauksen koko koneen kokoonpanon osista ja komponenteista.</span><span class="sxs-lookup"><span data-stu-id="a28f0-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="a28f0-113">Vaikka tuotesuunnittelijat haluavatkin ehkä mieluummin nähdä tuoterakenteen edustettuna tällä tavoin, rakenne ei välttämättä vastaa oikein sitä tapaa, jolla kone rakennetaan työnohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="a28f0-114">Esimerkiksi edellisen kuvan tuotannon tuoterakenne osoittaa, että sähköinen yksikkö F on koottu erillisenä osana erillisessä työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="a28f0-115">Työnohjauksessa voidaan kuitenkin arvioida, että on optimaalisempaa koota sähköinen yksikkö yleisen koneen kokoonpanon osana eikä erillisenä työtilauksena.</span><span class="sxs-lookup"><span data-stu-id="a28f0-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="a28f0-116">Tämä tuotannon tuotantorakenne osoittaa myös, että osa G on erillinen osa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="a28f0-117">Kuitenkin tässä rakenteessa osa G ei edusta fyysistä osaa vaan pakkausmateriaalien kokoelmaa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="a28f0-118">Sen vuoksi vaikka tuotannon tuoterakenne antaakin hyvän arvon tuotemallille ja sen ylläpitämiseen, se ei ehkä ole kaikkein loogisin keino tukea tuotteen tuotannonohjausprosessia.</span><span class="sxs-lookup"><span data-stu-id="a28f0-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="a28f0-119">Sitävastoin valmistuksen tuoterakenne edustaa parasta keinoa tuotteen kehittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="a28f0-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="a28f0-120">Seuraavassa kuvassa näytetään, miten edeltävä tuotannon tuoterakenne siirretään valmistuksen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="a28f0-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="a28f0-121">Tässä kuvassa (a) on tuotteen H tuoterakenne ja (b) on tuotteen H reititystaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="a28f0-122">Näet tästä rakenteesta, että siinä ei ole osia F ja G, ja että näiden osien rakennemateriaalit on siirretty seuraavalle tuoterakennetasolle.</span><span class="sxs-lookup"><span data-stu-id="a28f0-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="a28f0-123">Toisin kuin tuotannon tuoterakenne, jossa on kaksi työvaihetaulukkoa, valmistuksen tuoterakenteessa on vain yksi työvaihetaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="a28f0-124">Pakkausmateriaalin työvaihetta, joka on linkitetty osaan G, on myös laajennettu ja se kuuluu nyt tuotteen H työvaiheiden lomakkeeseen. Ensimmäinen työvaihe on sähköisen yksikön kokoonpano.</span><span class="sxs-lookup"><span data-stu-id="a28f0-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="a28f0-125">Tämä järjestys on hyvän järjen mukainen, koska yksikköä käytetään seuraavassa työvaiheessa eli koneen kokoonpanossa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="a28f0-126">Viimeinen työvaihe on pakkauksen työvaihe, jossa käytetään kahta pakkausmateriaalia (C ja D).</span><span class="sxs-lookup"><span data-stu-id="a28f0-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="a28f0-127">Siirtyminen tuotannon tuoterakenteen ja valmistuksen tuoterakenteen välillä on mahdollista käyttämällä tuoterakenteen haamurivityyppiä.</span><span class="sxs-lookup"><span data-stu-id="a28f0-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="a28f0-128">Kuten "haamu"-termi ilmaisee, osat F ja G ovat kadonneet kahden tuoterakennetyyppin välisen siirtymisen aikana.</span><span class="sxs-lookup"><span data-stu-id="a28f0-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="a28f0-129">Tässä esimerkissä haamurivityyppiä sovelletaan osien F ja G tuoterakenneriveille tuotannon tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="a28f0-130">Kun luodaan tuotanto- tai erätilaus, tuotannon tuoterakenne kopioidaan tuotantoon tai erätilaukseen.</span><span class="sxs-lookup"><span data-stu-id="a28f0-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="a28f0-131">Kun järjestys määritetty, tapahtuu siirtyminen tuotannon tuoterakenteesta valmistuksen tuoterakenteeseen edellisissä kuvissa näytetyn mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a28f0-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="a28f0-132">Toisen kuvan työvaihetaulukossa pakkausmateriaalit C ja D ovat työvaiheen syötteitä.</span><span class="sxs-lookup"><span data-stu-id="a28f0-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="a28f0-133">Monitasoiset haamutuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="a28f0-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="a28f0-134">Haamurivityyppiä voidaan käyttää monitasoisissa tuoterakenteissa seuraavassa kuvassa näytetyn mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a28f0-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="a28f0-135">Tässä kuvassa (a) on tuotteen H tuoterakenne ja (b) on osien E ja F sekä tuotteen G reititystaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Tuote G ja osa F reititystaulukoiden kanssa](media/product-G-route-sheet-G.png)


<span data-ttu-id="a28f0-137">Seuraavassa kuvassa näytetään tuloksena saatu valmistuksen tuoterakenne ja reititystaulukko, jos osien E ja F tuoterakennerivit määritetään siten, että rivityyppinä on haamu.</span><span class="sxs-lookup"><span data-stu-id="a28f0-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="a28f0-138">Tässä kuvassa (a) on tuotteen G tuoterakenne ja (b) on tuotteen G reititystaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Tuote G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="a28f0-140">Haamu ja reititysverkko</span><span class="sxs-lookup"><span data-stu-id="a28f0-140">Phantom and route network</span></span>
<span data-ttu-id="a28f0-141">Haamutuoterakenteita voidaan käyttää myös tuoterakenteelle, jossa on reititysverkko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="a28f0-142">Reititysverkossa yksi tai useampi toiminto suoritetaan samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a28f0-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="a28f0-143">Seuraavassa kuvassa näytetään esimerkki reititysverkosta, jota käytetään monitasoisessa tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="a28f0-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="a28f0-144">Tässä kuvassa (a) on tuotteen G ja osan F tuoterakenne ja (b) on tuotteen G ja osan F reititystaulukko, jossa on reititysverkko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Tuote G ja osa F](media/product-G-part-F.png)


<span data-ttu-id="a28f0-146">Seuraavassa kuvassa (a) on tuotteen G ja osan F tuoterakenne ja (b) on tuotteen G ja osan F reititystaulukko.</span><span class="sxs-lookup"><span data-stu-id="a28f0-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Tuote G ja osa F reititystaulukoiden kanssa](media/product-G-part-F-with-route-sheet.png)
