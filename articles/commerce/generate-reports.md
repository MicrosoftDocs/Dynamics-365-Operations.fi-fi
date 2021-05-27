---
title: Verkkokanavaraporttien luominen
description: Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 80d62b29fcc95a3153c604512e1ee6b3e55ba840
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019784"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="6b2a9-103">Verkkokanavaraporttien luominen</span><span class="sxs-lookup"><span data-stu-id="6b2a9-103">Generate online channel reports</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b2a9-104">Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Commercessa luodaan raportteja verkkokanavassa.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b2a9-105">Voit luoda ja tarkastella useita Commerce-raportteja. Ne osoittavat, miten verkkokanava toimii.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-105">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="6b2a9-106">Kanavan yhteenvetoraportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-106">Channel summary report</span></span>

<span data-ttu-id="6b2a9-107">**Kanavan yhteenveto** -raportissa näkyy yhteenveto valitun kanavan seuraavista tapahtumista:</span><span class="sxs-lookup"><span data-stu-id="6b2a9-107">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="6b2a9-108">Myyntitapahtumat</span><span class="sxs-lookup"><span data-stu-id="6b2a9-108">Sales transactions</span></span>
- <span data-ttu-id="6b2a9-109">Maksutapahtumat</span><span class="sxs-lookup"><span data-stu-id="6b2a9-109">Payment transactions</span></span>
- <span data-ttu-id="6b2a9-110">Verotapahtumat</span><span class="sxs-lookup"><span data-stu-id="6b2a9-110">Tax transactions</span></span>
- <span data-ttu-id="6b2a9-111">Alennustapahtumat</span><span class="sxs-lookup"><span data-stu-id="6b2a9-111">Discounted transactions</span></span>

<span data-ttu-id="6b2a9-112">Voit luoda **Kanavan yhteenveto** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-112">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-113">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan yhteenveto -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-113">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="6b2a9-114">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-114">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-115">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-115">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-116">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-116">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-117">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="6b2a9-118">Vuosikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-118">Channel sales by year report</span></span> 

<span data-ttu-id="6b2a9-119">**Kanavan myynti vuoden mukaan** -raportissa näkyy tietyn myymälän vuosittaisen myynnin vertailu.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-119">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="6b2a9-120">Valitse vuosi, jonka myyntiä verrataan. Raportti vertaa valitun vuoden myyntiä edellisen vuoden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-120">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="6b2a9-121">Voit luoda **Kanavan myynti vuoden mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-121">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-122">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan vuosikohtainen myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-122">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="6b2a9-123">Anna vuosi **Kalenterivuodesta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-123">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="6b2a9-124">Anna vuosi **Kalenterivuoteen**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-124">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="6b2a9-125">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-125">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-126">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="6b2a9-127">Tuntikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-127">Channel sales by hour report</span></span>

<span data-ttu-id="6b2a9-128">**Kanavan myynti tunnin mukaan** -raportti näyttää valitun kanavan tai toimintoyksikön myyntimittarin tunnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-128">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="6b2a9-129">Voit luoda **Kanavan myynti tunnin mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-129">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-130">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan tuntikohtainen myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-130">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="6b2a9-131">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-131">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-132">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-132">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-133">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-133">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-134">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="6b2a9-135">Suurimpien asiakkaiden raportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-135">Top customers report</span></span>

<span data-ttu-id="6b2a9-136">**Parhaat asiakkaat** -raportissa on myyntimittarit parhaille *N* asiakkaille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-136">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="6b2a9-137">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-137">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="6b2a9-138">Voit luoda **Parhaat asiakkaat** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-138">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-139">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat asiakkaat -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-139">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="6b2a9-140">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-140">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-141">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-141">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-142">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-142">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-143">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-143">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="6b2a9-144">Parhaat alennukset -raportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-144">Top discounts report</span></span>

<span data-ttu-id="6b2a9-145">**Parhaat alennukset** -raportissa on myyntimittarit parhaille *N* alennuksille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-145">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="6b2a9-146">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-146">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="6b2a9-147">Voit luoda **Parhaat alennukset** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-147">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-148">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat alennukset -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-148">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="6b2a9-149">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-149">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-150">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-150">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-151">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-151">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-152">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-152">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="6b2a9-153">Parhaat tuotteet -raportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-153">Top products report</span></span>

<span data-ttu-id="6b2a9-154">**Parhaat tuotteet** -raportissa on myyntimittarit parhaille *N* tuotteille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-154">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="6b2a9-155">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-155">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="6b2a9-156">Voit luoda **Parhaat tuotteet** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-156">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-157">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat tuotteet -raportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-157">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="6b2a9-158">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-158">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-159">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-159">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-160">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-160">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-161">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-161">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="6b2a9-162">Luokan myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-162">Category sales report</span></span>

<span data-ttu-id="6b2a9-163">**Luokan myynti** -raportissa näkyvät myyntimittarit valittuna kautena jokaiselle luokkahierarkian solmulle valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-163">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="6b2a9-164">Voit luoda **Luokan myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-164">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-165">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Luokan myyntiraportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-165">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="6b2a9-166">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-166">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-167">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-167">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-168">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-168">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="6b2a9-169">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-169">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="6b2a9-170">Organisaation myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="6b2a9-170">Organization sales report</span></span>

<span data-ttu-id="6b2a9-171">**Organisaation myynti** -raportti näyttää myymälöiden suorituskyvyn organisaatioyksiköiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-171">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="6b2a9-172">Tämä raportti sisältää myynnin määrän ja summan myymälän mukaan sekä kunkin myymälän katetuoton.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-172">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="6b2a9-173">Organisaatioyksikkö perustuu oletusraportointihierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-173">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="6b2a9-174">Voit luoda **Organisaation myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-174">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="6b2a9-175">Siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Myyntiraportit \> Organisaation myyntiraportti**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-175">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="6b2a9-176">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-176">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-177">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-177">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="6b2a9-178">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b2a9-178">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b2a9-179">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6b2a9-179">Additional resources</span></span>

- [<span data-ttu-id="6b2a9-180">Kaupan aloitussivu</span><span class="sxs-lookup"><span data-stu-id="6b2a9-180">Commerce home page</span></span>](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]