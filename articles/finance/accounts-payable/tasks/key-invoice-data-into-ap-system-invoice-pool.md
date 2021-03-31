---
title: Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla
description: Tässä aiheessa kuvataan, miten laskurekisteriä käytetään laskujen luomiseen.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227157"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="5c664-103">Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla</span><span class="sxs-lookup"><span data-stu-id="5c664-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c664-104">Tässä aiheessa kuvataan, miten laskurekisteriä käytetään laskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="5c664-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="5c664-105">Käytä sitten laskupoolia laskun ja ostotilauksen täsmäyttämisessä ja viimeistele kulu toimittajan laskun sivulla.</span><span class="sxs-lookup"><span data-stu-id="5c664-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5c664-106">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="5c664-106">Create a purchase order</span></span>
1. <span data-ttu-id="5c664-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5c664-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="5c664-108">Luo uusi ostotilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5c664-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="5c664-109">Avaa avattava luettelo **Toimittajan tili** -kentässä valitaksesi toimittajan.</span><span class="sxs-lookup"><span data-stu-id="5c664-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="5c664-110">Voit valita esimerkiksi toimittajan **1001**.</span><span class="sxs-lookup"><span data-stu-id="5c664-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="5c664-111">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c664-111">Select **OK**.</span></span>
5. <span data-ttu-id="5c664-112">Valitse **Nimiketunnus**-kentässä avattavasta valikosta palvelun nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="5c664-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="5c664-113">Voit valita esimerkiksi arvon **S0001**.</span><span class="sxs-lookup"><span data-stu-id="5c664-113">For example, select **S0001**.</span></span> <span data-ttu-id="5c664-114">Nettosumma on 75,00 euroa.</span><span class="sxs-lookup"><span data-stu-id="5c664-114">The net amount is 75.00.</span></span>  <span data-ttu-id="5c664-115">Tämä on laskuun odotettava summa.</span><span class="sxs-lookup"><span data-stu-id="5c664-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="5c664-116">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="5c664-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="5c664-117">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="5c664-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="5c664-118">Luominen, kirjaaminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="5c664-118">Create and post and invoice</span></span>
1. <span data-ttu-id="5c664-119">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskurekisteri**.</span><span class="sxs-lookup"><span data-stu-id="5c664-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="5c664-120">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5c664-120">Select **New**.</span></span>
3. <span data-ttu-id="5c664-121">Avaa haku, kun haluat valita käytettävän laskurekisterin nimen.</span><span class="sxs-lookup"><span data-stu-id="5c664-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="5c664-122">Valitse sen laskurekisterin nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="5c664-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="5c664-123">Valitse **Rivit**, kun haluat avata rekisterin ja syöttää kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="5c664-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="5c664-124">Valitse toimittaja haun avulla.</span><span class="sxs-lookup"><span data-stu-id="5c664-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="5c664-125">Voit valita esimerkiksi toimittajan **1001**.</span><span class="sxs-lookup"><span data-stu-id="5c664-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="5c664-126">Syötä **Lasku**-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="5c664-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="5c664-127">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5c664-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="5c664-128">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5c664-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="5c664-129">Avaa **Ostotilaus-** kentässä avattava luettelo, jossa voit valita aiemmin luomasi ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="5c664-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="5c664-130">Korosta **Hyväksynyt**- kentässä avattavassa luettelossa hyväksyjä ja valitse hyväksyjä valitsemalla **Valitse.**</span><span class="sxs-lookup"><span data-stu-id="5c664-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="5c664-131">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="5c664-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="5c664-132">Laskutusprosessin tekeminen valmiiksi avaamalla lasku poolista ja täsmäyttämällä se ostotilauksen kanssa</span><span class="sxs-lookup"><span data-stu-id="5c664-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="5c664-133">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskupooli**.</span><span class="sxs-lookup"><span data-stu-id="5c664-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="5c664-134">Luo toimittajan lasku poolissa olevasta laskusta valitsemalla **Ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="5c664-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="5c664-135">Valitse lasku, jota haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="5c664-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="5c664-136">Tee täsmäytys valmiiksi valitsemalla **Päivitä täsmäytyksen tila**.</span><span class="sxs-lookup"><span data-stu-id="5c664-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="5c664-137">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="5c664-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="5c664-138">Valitse **Vaihda näyttö**.</span><span class="sxs-lookup"><span data-stu-id="5c664-138">Select **Change view**.</span></span>
7. <span data-ttu-id="5c664-139">Valitse **Ruudukkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="5c664-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="5c664-140">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="5c664-140">Select **Post**.</span></span>
9. <span data-ttu-id="5c664-141">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="5c664-141">Close the form.</span></span>
10. <span data-ttu-id="5c664-142">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Toimittajat > Toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="5c664-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="5c664-143">Valitse ostotilauksessa mainittu toimittaja.</span><span class="sxs-lookup"><span data-stu-id="5c664-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="5c664-144">Voit valita esimerkiksi toimittajan **1001**.</span><span class="sxs-lookup"><span data-stu-id="5c664-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="5c664-145">Valitse toimintoruudussa **Toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="5c664-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="5c664-146">Valitse **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="5c664-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="5c664-147">Valitse luomasi lasku.</span><span class="sxs-lookup"><span data-stu-id="5c664-147">Select the invoice that you created.</span></span> <span data-ttu-id="5c664-148">Laskurekisterin jaksotus peruutettiin ja kirjattiin sopivalle kulutilille.</span><span class="sxs-lookup"><span data-stu-id="5c664-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]