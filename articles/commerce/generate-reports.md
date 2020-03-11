---
title: Verkkokanavaraporttien luominen
description: Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7b73c7a51ffa606876072d607fc219f5f6a2ba
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057587"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="936fc-103">Verkkokanavaraporttien luominen</span><span class="sxs-lookup"><span data-stu-id="936fc-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="936fc-104">Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.</span><span class="sxs-lookup"><span data-stu-id="936fc-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="936fc-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="936fc-105">Overview</span></span>

<span data-ttu-id="936fc-106">Voit luoda ja tarkastella useita Commerce-raportteja. Ne osoittavat, miten verkkokanava toimii.</span><span class="sxs-lookup"><span data-stu-id="936fc-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="936fc-107">Kanavan yhteenvetoraportti</span><span class="sxs-lookup"><span data-stu-id="936fc-107">Channel summary report</span></span>

<span data-ttu-id="936fc-108">**Kanavan yhteenveto** -raportissa näkyy yhteenveto valitun kanavan seuraavista tapahtumista:</span><span class="sxs-lookup"><span data-stu-id="936fc-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="936fc-109">Myyntitapahtumat</span><span class="sxs-lookup"><span data-stu-id="936fc-109">Sales transactions</span></span>
- <span data-ttu-id="936fc-110">Maksutapahtumat</span><span class="sxs-lookup"><span data-stu-id="936fc-110">Payment transactions</span></span>
- <span data-ttu-id="936fc-111">Verotapahtumat</span><span class="sxs-lookup"><span data-stu-id="936fc-111">Tax transactions</span></span>
- <span data-ttu-id="936fc-112">Alennustapahtumat</span><span class="sxs-lookup"><span data-stu-id="936fc-112">Discounted transactions</span></span>

<span data-ttu-id="936fc-113">Voit luoda **Kanavan yhteenveto** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-114">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan yhteenveto -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="936fc-115">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-116">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-117">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="936fc-119">Vuosikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="936fc-119">Channel sales by year report</span></span> 

<span data-ttu-id="936fc-120">**Kanavan myynti vuoden mukaan** -raportissa näkyy tietyn myymälän vuosittaisen myynnin vertailu.</span><span class="sxs-lookup"><span data-stu-id="936fc-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="936fc-121">Valitse vuosi, jonka myyntiä verrataan. Raportti vertaa valitun vuoden myyntiä edellisen vuoden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="936fc-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="936fc-122">Voit luoda **Kanavan myynti vuoden mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-123">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan vuosikohtainen myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="936fc-124">Anna vuosi **Kalenterivuodesta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="936fc-125">Anna vuosi **Kalenterivuoteen**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="936fc-126">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="936fc-128">Tuntikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="936fc-128">Channel sales by hour report</span></span>

<span data-ttu-id="936fc-129">**Kanavan myynti tunnin mukaan** -raportti näyttää valitun kanavan tai toimintoyksikön myyntimittarin tunnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="936fc-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="936fc-130">Voit luoda **Kanavan myynti tunnin mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-131">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan tuntikohtainen myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="936fc-132">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-133">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-134">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="936fc-136">Suurimpien asiakkaiden raportti</span><span class="sxs-lookup"><span data-stu-id="936fc-136">Top customers report</span></span>

<span data-ttu-id="936fc-137">**Parhaat asiakkaat** -raportissa on myyntimittarit parhaille *N* asiakkaille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="936fc-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="936fc-138">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="936fc-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="936fc-139">Voit luoda **Parhaat asiakkaat** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-140">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat asiakkaat -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="936fc-141">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-142">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-143">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="936fc-145">Parhaat alennukset -raportti</span><span class="sxs-lookup"><span data-stu-id="936fc-145">Top discounts report</span></span>

<span data-ttu-id="936fc-146">**Parhaat alennukset** -raportissa on myyntimittarit parhaille *N* alennuksille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="936fc-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="936fc-147">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="936fc-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="936fc-148">Voit luoda **Parhaat alennukset** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-149">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat alennukset -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="936fc-150">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-151">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-152">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="936fc-154">Parhaat tuotteet -raportti</span><span class="sxs-lookup"><span data-stu-id="936fc-154">Top products report</span></span>

<span data-ttu-id="936fc-155">**Parhaat tuotteet** -raportissa on myyntimittarit parhaille *N* tuotteille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="936fc-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="936fc-156">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="936fc-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="936fc-157">Voit luoda **Parhaat tuotteet** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-158">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat tuotteet -raportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="936fc-159">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-160">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-161">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-162">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="936fc-163">Luokan myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="936fc-163">Category sales report</span></span>

<span data-ttu-id="936fc-164">**Luokan myynti** -raportissa näkyvät myyntimittarit valittuna kautena jokaiselle luokkahierarkian solmulle valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="936fc-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="936fc-165">Voit luoda **Luokan myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-166">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Luokan myyntiraportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="936fc-167">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-168">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-169">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="936fc-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="936fc-170">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="936fc-171">Organisaation myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="936fc-171">Organization sales report</span></span>

<span data-ttu-id="936fc-172">**Organisaation myynti** -raportti näyttää myymälöiden suorituskyvyn organisaatioyksiköiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="936fc-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="936fc-173">Tämä raportti sisältää myynnin määrän ja summan myymälän mukaan sekä kunkin myymälän katetuoton.</span><span class="sxs-lookup"><span data-stu-id="936fc-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="936fc-174">Organisaatioyksikkö perustuu oletusraportointihierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="936fc-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="936fc-175">Voit luoda **Organisaation myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="936fc-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="936fc-176">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Organisaation myyntiraportti**.</span><span class="sxs-lookup"><span data-stu-id="936fc-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="936fc-177">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-178">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="936fc-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="936fc-179">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="936fc-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="936fc-180">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="936fc-180">Additional resources</span></span>

- [<span data-ttu-id="936fc-181">Kaupan aloitussivu</span><span class="sxs-lookup"><span data-stu-id="936fc-181">Commerce home page</span></span>](../retail/index.md)
