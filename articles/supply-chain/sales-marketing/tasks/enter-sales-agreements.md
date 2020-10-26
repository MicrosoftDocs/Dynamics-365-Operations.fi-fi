---
title: Myyntisopimusten syöttäminen
description: Tässä aiheessa kerrotaan, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d69f3eaacea641460b407c1456ee50600262fee
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982038"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="ce86e-103">Myyntisopimusten syöttäminen</span><span class="sxs-lookup"><span data-stu-id="ce86e-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce86e-104">Tässä aiheessa kerrotaan, miten luodaan myyntisopimus, jossa yksi asiakas sitoutuu ostamaan tuotteen sovitulla summalla tietyn ajan ja saa vastineeksi erikoisalennuksia.</span><span class="sxs-lookup"><span data-stu-id="ce86e-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="ce86e-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="ce86e-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="ce86e-106">Määritä myyntisopimuksen otsikko</span><span class="sxs-lookup"><span data-stu-id="ce86e-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="ce86e-107">Siirry siirtymisruudussa kohtaan **Moduulit > Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="ce86e-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-108">Select **New**.</span></span>
3. <span data-ttu-id="ce86e-109">Valitse **Asiakastili**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="ce86e-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="ce86e-110">Valitse **Myyntisopimuksen luokittelu**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="ce86e-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="ce86e-111">Laajenna **Yleiset**-osa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="ce86e-112">Valitse **Oletussitoumus**-kentässä **Tuotteen arvoon perustuva sitoumus**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="ce86e-113">Sitoumustyyppi on pakollinen ehto, joka on määritettävä sopimukseen määrittämään, miten sopimus toteutetaan.</span><span class="sxs-lookup"><span data-stu-id="ce86e-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="ce86e-114">Voit määrittää neljän esimääritetyn tyypin avulla määränä tai arvona ilmaistavan asiakkaan sitoumuksen tavoitteen.</span><span class="sxs-lookup"><span data-stu-id="ce86e-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="ce86e-115">Määräsitoumustyyppiä voidaan käyttää vain määritetyssä tuotteessa, mutta arvoperustaisia tyyppejä voi käyttää sekä määritettyjen että määrittämättömien tuotteiden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="ce86e-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="ce86e-116">Määritä **Vanhentumispäivä**-kentässä tuleva päivämäärä, jolloin haluat sopimuksen vanhentuvan.</span><span class="sxs-lookup"><span data-stu-id="ce86e-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="ce86e-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="ce86e-118">Määritä tuotteen arvon perustuvan sitoumuksen rivit</span><span class="sxs-lookup"><span data-stu-id="ce86e-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="ce86e-119">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-119">Select **Add line**.</span></span>
2. <span data-ttu-id="ce86e-120">Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="ce86e-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="ce86e-121">Sopimukseen valittu sitoumustyyppi vaikuttaa siihen, mitä tietoja sopimusriveillä annetaan.</span><span class="sxs-lookup"><span data-stu-id="ce86e-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="ce86e-122">Esimerkiksi arvoperustaisessa sopimuksessa on määritettävä kokonaisnettosumma (sovitussa valuutassa), jolla asiakas sitoutuu ostamaan sinulta tavaroita.</span><span class="sxs-lookup"><span data-stu-id="ce86e-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="ce86e-123">Tässä esimerkissä rivin **Määrä**- ja **Yksikkö**-kentät eivät ole käytettävissä, koska olet luomassa sopimuksen, jossa asiakas ostaa tuotetta tietyn arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="ce86e-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="ce86e-124">Anna **Nettosumma**-kenttään rahasumma, jolla asiakas on sitoutunut ostamaan.</span><span class="sxs-lookup"><span data-stu-id="ce86e-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="ce86e-125">Anna **Alennusprosentti**-kentässä prosenttiarvo, jota käytetään asiakkaan sopimukseen linkitetyillä myyntitilausriveillä.</span><span class="sxs-lookup"><span data-stu-id="ce86e-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="ce86e-126">Laajenna **Rivin erittely** -osa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="ce86e-127">Valitse **Maksimi pakotetaan** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="ce86e-128">**Maksimi pakotetaan** -asetuksen valinta tarkoittaa, että kaikkien sitoumuksen erikoishintoja, alennuksia ja/tai maksuehtoja käyttävien myyntitilausrivien yhteissumma ei saa ylittää sitoumuksessa määritettyä summaa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="ce86e-129">Vapautuksen vähimmäis- ja enimmäissummat määrittävät arvoalueen, joka on myytävä kussakin valittua sopimusta käyttävässä myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="ce86e-130">Laajenna **Myyntisopimuksen otsikko** -osa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="ce86e-131">Jos sopimuksen tilaksi ei ole valittu **Voimassa**, myyntitilauksia ei voi liittää sopimukseen eivätkä ne siten osallistu kyseisen sopimuksen täytäntöönpanoon.</span><span class="sxs-lookup"><span data-stu-id="ce86e-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="ce86e-132">Voit muuttaa tilan manuaalisesti tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="ce86e-133">Tila kuitenkin muutetaan tavallisesti silloin, kun vahvistat asiakkaan sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="ce86e-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="ce86e-134">Valitse toimintoruudussa **Myyntisopimus**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="ce86e-135">Valitse **Vahvistus**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-135">Select **Confirmation**.</span></span> <span data-ttu-id="ce86e-136">Varmista, että **Merkitse sopimus voimassa olevaksi** -asetukseksi on valittu **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="ce86e-137">Valitse **Tulosta raportti** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="ce86e-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce86e-138">Select **OK**.</span></span>
12. <span data-ttu-id="ce86e-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce86e-139">Close the page.</span></span> <span data-ttu-id="ce86e-140">Sopimus on nyt voimassa.</span><span class="sxs-lookup"><span data-stu-id="ce86e-140">The agreement is now effective.</span></span> <span data-ttu-id="ce86e-141">Voit aloittaa asiakkaan tilausten linkittämisen sopimukseen, jossa ne vastakirjataan sitoumustavoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="ce86e-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

