--- 
title: Anna myyntisopimukset
description: "Tässä menettelyssä näytetään, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 943ae430b148670d248716c9ece21850bf7d2dfd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="033d5-103">Anna myyntisopimukset</span><span class="sxs-lookup"><span data-stu-id="033d5-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="033d5-104">Tässä menettelyssä näytetään, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla</span><span class="sxs-lookup"><span data-stu-id="033d5-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="033d5-105">tietyn ajan ja saa vastineeksi erikoisalennuksia.</span><span class="sxs-lookup"><span data-stu-id="033d5-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="033d5-106">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="033d5-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="033d5-107">Määritä myyntisopimuksen otsikko</span><span class="sxs-lookup"><span data-stu-id="033d5-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="033d5-108">Valitse Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset.</span><span class="sxs-lookup"><span data-stu-id="033d5-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="033d5-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="033d5-109">Click New.</span></span>
3. <span data-ttu-id="033d5-110">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="033d5-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="033d5-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="033d5-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="033d5-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="033d5-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="033d5-113">Avaa haku napsauttamalla Myyntisopimuksen luokitus -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="033d5-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="033d5-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="033d5-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="033d5-115">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="033d5-115">Expand the General section.</span></span>
9. <span data-ttu-id="033d5-116">Valitse Oletussitoumus-kentässä Tuotteen arvoon perustuva sitoumus.</span><span class="sxs-lookup"><span data-stu-id="033d5-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="033d5-117">Sitoumustyyppi on pakollinen ehto, joka on määritettävä sopimukseen määrittämään, miten sopimus toteutetaan.</span><span class="sxs-lookup"><span data-stu-id="033d5-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="033d5-118">Voit määrittää neljän esimääritetyn tyypin avulla määränä tai arvona ilmaistavan asiakkaan sitoumuksen tavoitteen.</span><span class="sxs-lookup"><span data-stu-id="033d5-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="033d5-119">Määräsitoumustyyppiä voidaan käyttää vain määritetyssä tuotteessa, mutta arvoperustaisia tyyppejä voi käyttää sekä määritettyjen että määrittämättömien tuotteiden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="033d5-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="033d5-120">Määritä Vanhentumispäivä-kentässä tuleva päivämäärä, jolloin haluat sopimuksen vanhentuvan.</span><span class="sxs-lookup"><span data-stu-id="033d5-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="033d5-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="033d5-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="033d5-122">Määritä tuotteen arvon perustuvan sitoumuksen rivit</span><span class="sxs-lookup"><span data-stu-id="033d5-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="033d5-123">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="033d5-123">Click Add line.</span></span>
2. <span data-ttu-id="033d5-124">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="033d5-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="033d5-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="033d5-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="033d5-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="033d5-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="033d5-127">Sopimukseen valittu sitoumustyyppi vaikuttaa siihen, mitä tietoja sopimusriveillä annetaan.</span><span class="sxs-lookup"><span data-stu-id="033d5-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="033d5-128">Esimerkiksi arvoperustaisessa sopimuksessa on määritettävä kokonaisnettosumma (sovitussa valuutassa), jolla asiakas sitoutuu ostamaan sinulta tavaroita.</span><span class="sxs-lookup"><span data-stu-id="033d5-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="033d5-129">Tässä esimerkissä rivin Määrä- ja Yksikkö-kentät eivät ole käytettävissä, koska olet luomassa sopimuksen, jossa asiakas ostaa tuotetta tietyn arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="033d5-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="033d5-130">Anna Nettosumma-kenttään rahasumma, jolla asiakas on sitoutunut ostamaan.</span><span class="sxs-lookup"><span data-stu-id="033d5-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="033d5-131">Anna Alennusprosentti-kentässä prosenttiarvo, jota käytetään asiakkaan sopimukseen linkitetyillä myyntitilausriveillä.</span><span class="sxs-lookup"><span data-stu-id="033d5-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="033d5-132">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="033d5-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="033d5-133">Valitse Maksimi pakotetaan -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="033d5-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="033d5-134">Maksimi pakotetaan -asetuksen valinta tarkoittaa, että kaikkien sitoumuksen erikoishintoja, alennuksia ja/tai maksuehtoja käyttävien myyntitilausrivien yhteissumma ei saa ylittää sitoumuksessa määritettyä summaa.</span><span class="sxs-lookup"><span data-stu-id="033d5-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="033d5-135">Vapautuksen vähimmäis- ja enimmäissummat määrittävät arvoalueen, joka on myytävä kussakin valittua sopimusta käyttävässä myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="033d5-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="033d5-136">Laajenna Myyntisopimuksen otsikko -osa.</span><span class="sxs-lookup"><span data-stu-id="033d5-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="033d5-137">Jos sopimuksen tilaksi ei ole valittu Voimassa, myyntitilauksia ei voi liittää sopimukseen eivätkä ne siten osallistu kyseisen sopimuksen täytäntöönpanoon.</span><span class="sxs-lookup"><span data-stu-id="033d5-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="033d5-138">Voit muuttaa tilan manuaalisesti tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="033d5-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="033d5-139">Tila kuitenkin muutetaan tavallisesti silloin, kun vahvistat asiakkaan sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="033d5-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="033d5-140">Valitse toimintoruudussa Myyntisopimus.</span><span class="sxs-lookup"><span data-stu-id="033d5-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="033d5-141">Valitse Vahvistus.</span><span class="sxs-lookup"><span data-stu-id="033d5-141">Click Confirmation.</span></span>
    * <span data-ttu-id="033d5-142">Varmista, Merkitse sopimus voimassa olevaksi -asetukseksi on valittu Kyllä.</span><span class="sxs-lookup"><span data-stu-id="033d5-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="033d5-143">Valitse Tulosta raportti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="033d5-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="033d5-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="033d5-144">Click OK.</span></span>
14. <span data-ttu-id="033d5-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="033d5-145">Close the page.</span></span>
    * <span data-ttu-id="033d5-146">Sopimus on nyt voimassa oleva ja voit aloittaa asiakkaan tilausten linkittämisen sopimukseen, jossa ne vastakirjataan sitoumustavoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="033d5-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


