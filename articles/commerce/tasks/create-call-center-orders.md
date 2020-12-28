---
title: Luo puhelinkeskustilauksia
description: Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594233"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="6c233-103">Luo puhelinkeskustilauksia</span><span class="sxs-lookup"><span data-stu-id="6c233-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c233-104">Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="6c233-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="6c233-105">Tässä menettelyssä käytetään esittely-yritystä USRT. Tämä on tarkoitettu myyntitilauksia käsittelevälle assistentille.</span><span class="sxs-lookup"><span data-stu-id="6c233-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="6c233-106">Edellytykset: Menettelyn suorittava käyttäjä on määritetty puhelinkeskuksen käyttäjiksi. Julkaistussa Fabrikamin puolivuosittaisessa luettelossa on vähintään yksi lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="6c233-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="6c233-107">Valitse **Retail ja Commerce \> Asiakkaat \> Asiakaspalvelu**.</span><span class="sxs-lookup"><span data-stu-id="6c233-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="6c233-108">Anna **SearchText**-kenttään hakuehdot, joilla etsit asiakasta.</span><span class="sxs-lookup"><span data-stu-id="6c233-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="6c233-109">Valitse tässä esimerkissä menettelytyypiksi Nieminen ja valitse **sarkainnäppäin**.</span><span class="sxs-lookup"><span data-stu-id="6c233-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="6c233-110">Valitse Haku.</span><span class="sxs-lookup"><span data-stu-id="6c233-110">Select Search.</span></span>
    * <span data-ttu-id="6c233-111">Koska esittelytiedoissa on vain yksi asiakas nimeltä Nieminen, hänet valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6c233-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="6c233-112">Valitse **Uusi myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="6c233-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="6c233-113">Laajenna tai tiivistä **myyntitilauksen** otsikko-osa.</span><span class="sxs-lookup"><span data-stu-id="6c233-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="6c233-114">Valitse luettelon lähdekoodi.</span><span class="sxs-lookup"><span data-stu-id="6c233-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="6c233-115">Jos aktiivisia lähdekoodeja ei ole, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="6c233-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="6c233-116">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="6c233-116">Select **Add line**.</span></span>
8. <span data-ttu-id="6c233-117">Anna **Nimiketunnus**-kenttään nimikkeen hakuehto.</span><span class="sxs-lookup"><span data-stu-id="6c233-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="6c233-118">Anna tässä mallimenettelyssä osittainen nimikenumero 8111 ja paina sarkainnäppäintä. Toiminto avaa nimikkeen hakuikkunan.</span><span class="sxs-lookup"><span data-stu-id="6c233-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="6c233-119">Valitse myyntitilaukseen lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="6c233-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="6c233-120">Syötä myyntimäärä.</span><span class="sxs-lookup"><span data-stu-id="6c233-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="6c233-121">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="6c233-121">Select **Create**.</span></span>
12. <span data-ttu-id="6c233-122">Valitse **Valmis**, kun haluat tarkistaa asiakkaan maksun.</span><span class="sxs-lookup"><span data-stu-id="6c233-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="6c233-123">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6c233-123">Select **Add**.</span></span>
    * <span data-ttu-id="6c233-124">Lisää-linkki löytyy Maksut-välilehdestä. Laajenna Maksut-välilehti, jos se on tiivistetty.</span><span class="sxs-lookup"><span data-stu-id="6c233-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="6c233-125">Valitse maksutapa.</span><span class="sxs-lookup"><span data-stu-id="6c233-125">Select the payment method.</span></span>
    * <span data-ttu-id="6c233-126">Valitse tässä menettelyssä käteismaksutapa.</span><span class="sxs-lookup"><span data-stu-id="6c233-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="6c233-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6c233-127">Close the page.</span></span>
16. <span data-ttu-id="6c233-128">Anna määrä.</span><span class="sxs-lookup"><span data-stu-id="6c233-128">Enter the amount.</span></span>
    * <span data-ttu-id="6c233-129">Anna tässä menettelyssä tilaussummaksi summa, joka löytyy Myyntitilauksen yhteenveto -sivun summakentän vasemmalta puolelta.</span><span class="sxs-lookup"><span data-stu-id="6c233-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="6c233-130">Tällä toiminnolla voi määrittää tilauksen kokonaan maksetuksi.</span><span class="sxs-lookup"><span data-stu-id="6c233-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="6c233-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c233-131">Select **OK**.</span></span>
18. <span data-ttu-id="6c233-132">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="6c233-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c233-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6c233-133">Additional resources</span></span>

[<span data-ttu-id="6c233-134">Tapahtumasähköpostien mukauttaminen toimitustilan mukaan</span><span class="sxs-lookup"><span data-stu-id="6c233-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="6c233-135">Toimitustavan muuttaminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="6c233-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)

