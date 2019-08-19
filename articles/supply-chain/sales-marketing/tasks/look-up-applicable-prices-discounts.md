---
title: Etsi sovellettavat hinnat ja alennukset
description: Menettelyssä selvitetään, miten voidaan etsiä tietyllä asiakkaalla voimassaoleva tuotehinta ja/tai -alennus myyntitilausta luomatta.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9caaa7f425133eda7a5f225b39ca52e11e0716
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835576"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="6d19a-103">Etsi sovellettavat hinnat ja alennukset</span><span class="sxs-lookup"><span data-stu-id="6d19a-103">Look up applicable prices and discounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d19a-104">Menettelyssä selvitetään, miten voidaan etsiä tietyllä asiakkaalla voimassaoleva tuotehinta ja/tai -alennus myyntitilausta luomatta.</span><span class="sxs-lookup"><span data-stu-id="6d19a-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="6d19a-105">Menettelyssä käsitellään yksi esimerkki yksityiskohtaisesti ja, jotta voisit seurata esimerkkiä ja valita tarvittavat arvon, sinun on käytettävä USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="6d19a-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="6d19a-106">Etsi sovellettava hinta</span><span class="sxs-lookup"><span data-stu-id="6d19a-106">Find the applicable price</span></span>
1. <span data-ttu-id="6d19a-107">Valitse Myynti ja markkinointi > Hinnat ja alennukset > Etsi hinnat.</span><span class="sxs-lookup"><span data-stu-id="6d19a-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="6d19a-108">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6d19a-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6d19a-109">Etsi luettelosta asiakas US-001 ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6d19a-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="6d19a-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6d19a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6d19a-111">Kirjoita Nimiketunnus-kenttään T0004.</span><span class="sxs-lookup"><span data-stu-id="6d19a-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="6d19a-112">Määrä-kentän oletusarvo on 1.</span><span class="sxs-lookup"><span data-stu-id="6d19a-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="6d19a-113">Jos kuitenkin tiedät, kuinka paljon kukin asiakas aikoo kyseistä tuotetta tilata, anna sen sijaan kyseinen arvo.</span><span class="sxs-lookup"><span data-stu-id="6d19a-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="6d19a-114">Näillä tiedoilla on merkitystä, jos asiakkaan kanssa solmitussa sopimuksessa on määrärajoja eli tuotteen hinta määräytyy ostetun vähimmäismäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="6d19a-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="6d19a-115">Anna Päivämäärä-kenttää päivämäärä, jolloin asiakas odottaa tekevänsä tilauksen.</span><span class="sxs-lookup"><span data-stu-id="6d19a-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="6d19a-116">Päivämäärä voi kuluva päivä tai mikä tahansa tuleva päivä.</span><span class="sxs-lookup"><span data-stu-id="6d19a-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="6d19a-117">Järjestelmä palauttaa nyt hinnan, joka koskee valittua tuotetta, jota valittu asiakas on ostanut tietyn määrän valittuna päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="6d19a-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="6d19a-118">Jos asiakas US-001 on tässä esimerkissä ostanut tänään 1 yksikön tuotetta T0004, asiakkaalta veloitettaisiin yksikköä kohden 350 Kanadan dollaria.</span><span class="sxs-lookup"><span data-stu-id="6d19a-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="6d19a-119">Tämä hinta perustuu asiakkaan kanssa aiemmin solmittuun, aktiiviseen kauppasopimukseen.</span><span class="sxs-lookup"><span data-stu-id="6d19a-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="6d19a-120">Sivun muissa kentissä on lisätietoja tuotehinnasta ja tuotteen kustannuksista (jos ne on määritetty päätuotteessa) sekä laskettu kannattavuus.</span><span class="sxs-lookup"><span data-stu-id="6d19a-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="6d19a-121">Jos Näytä liittyvät tuotevariantit -vaihtoehto on valittu, tuotevarianteille on muita kauppasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="6d19a-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="6d19a-122">Valitse Näytä liittyvät tuotevariantit -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6d19a-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="6d19a-123">Näkyvissä on tuotevarianttiluettelo, jossa on tietoja niiden dimensioista.</span><span class="sxs-lookup"><span data-stu-id="6d19a-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="6d19a-124">Merkitse luettelossa väriä Valkoinen vastaava rivi.</span><span class="sxs-lookup"><span data-stu-id="6d19a-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="6d19a-125">Huomaa, että tuotehinta poikkeaa nyt hinnasta, joka näytettiin, kun sitä ei oltu määritetty dimensiokohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="6d19a-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="6d19a-126">Valitse Näytä myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="6d19a-126">Click View sales prices.</span></span>
    * <span data-ttu-id="6d19a-127">Hinta (myynti) -sivulla on nähtävissä kaikki tuotteeseen ja sen variantteihin sovellettavat kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="6d19a-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="6d19a-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d19a-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="6d19a-129">Etsi sovellettava alennus</span><span class="sxs-lookup"><span data-stu-id="6d19a-129">Find the applicable discount</span></span>
    * <span data-ttu-id="6d19a-130">Varmista, Asiakastili-kentässä on asiakasnumero US-001 </span><span class="sxs-lookup"><span data-stu-id="6d19a-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="6d19a-131">Kirjoita Nimiketunnus-kenttään T0012.</span><span class="sxs-lookup"><span data-stu-id="6d19a-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="6d19a-132">Varmista, että Määrä-kentän arvo on 1.</span><span class="sxs-lookup"><span data-stu-id="6d19a-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="6d19a-133">Seuraavat tuotteelle T0012 näytetyt hinnoittelutiedot perustuvat vähintään yhteen kauppasopimukseen: yksikköhinta on 1 000 Kanadan dollaria ja alennusprosentti 5.</span><span class="sxs-lookup"><span data-stu-id="6d19a-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="6d19a-134">Valitse määräksi 20.</span><span class="sxs-lookup"><span data-stu-id="6d19a-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="6d19a-135">Tilausmäärän kasvun vuoksi asiakkaalle annettava rivialennus muuttuu 5 prosentista 7 prosenttiin.</span><span class="sxs-lookup"><span data-stu-id="6d19a-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="6d19a-136">Nettosumma lasketaan yksikköhinnan, alennuksen ja kokonaismäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="6d19a-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="6d19a-137">Valitse Näytä rivialennus.</span><span class="sxs-lookup"><span data-stu-id="6d19a-137">Click View line discount.</span></span>
    * <span data-ttu-id="6d19a-138">Tuotteella T0012 on kaksi rivialennussopimusta, joista toinen antaa 5 prosentin alennuksen, kun tilausmäärä on 1–10 ja toinen 7 prosentin alennuksen, kun määrä on yli 10.</span><span class="sxs-lookup"><span data-stu-id="6d19a-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="6d19a-139">Huomaa, että alennuksia käytetään tuoteryhmissä, tässä esimerkissä ryhmäkoodi 01, johon tuote T0012 kuuluu.</span><span class="sxs-lookup"><span data-stu-id="6d19a-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="6d19a-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d19a-140">Close the page.</span></span>

