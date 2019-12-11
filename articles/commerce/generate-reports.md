---
title: Verkkokanavaraporttien luominen
description: Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Retailissa luodaan raportteja verkkokanavassa.
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
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698047"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="19206-103">Verkkokanavaraporttien luominen</span><span class="sxs-lookup"><span data-stu-id="19206-103">Generate online channel reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="19206-104">Tässä aiheessa kuvataan, miten Microsoft Dynamics 365 Retailissa luodaan raportteja verkkokanavassa.</span><span class="sxs-lookup"><span data-stu-id="19206-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="19206-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="19206-105">Overview</span></span>

<span data-ttu-id="19206-106">Voit luoda ja tarkastella useita Retail-raportteja. Ne osoittavat, miten verkkokanava toimii.</span><span class="sxs-lookup"><span data-stu-id="19206-106">You can generate and view several reports in Retail to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="19206-107">Kanavan yhteenvetoraportti</span><span class="sxs-lookup"><span data-stu-id="19206-107">Channel summary report</span></span>

<span data-ttu-id="19206-108">**Kanavan yhteenveto** -raportissa näkyy yhteenveto valitun kanavan seuraavista tapahtumista:</span><span class="sxs-lookup"><span data-stu-id="19206-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="19206-109">Myyntitapahtumat</span><span class="sxs-lookup"><span data-stu-id="19206-109">Sales transactions</span></span>
- <span data-ttu-id="19206-110">Maksutapahtumat</span><span class="sxs-lookup"><span data-stu-id="19206-110">Payment transactions</span></span>
- <span data-ttu-id="19206-111">Verotapahtumat</span><span class="sxs-lookup"><span data-stu-id="19206-111">Tax transactions</span></span>
- <span data-ttu-id="19206-112">Alennustapahtumat</span><span class="sxs-lookup"><span data-stu-id="19206-112">Discounted transactions</span></span>

<span data-ttu-id="19206-113">Voit luoda **Kanavan yhteenveto** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-114">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan yhteenveto -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-114">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="19206-115">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-116">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-117">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="19206-119">Vuosikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="19206-119">Channel sales by year report</span></span> 

<span data-ttu-id="19206-120">**Kanavan myynti vuoden mukaan** -raportissa näkyy tietyn myymälän vuosittaisen myynnin vertailu.</span><span class="sxs-lookup"><span data-stu-id="19206-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="19206-121">Valitse vuosi, jonka myyntiä verrataan. Raportti vertaa valitun vuoden myyntiä edellisen vuoden myyntiin.</span><span class="sxs-lookup"><span data-stu-id="19206-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="19206-122">Voit luoda **Kanavan myynti vuoden mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-123">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan myynti vuoden mukaan -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-123">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="19206-124">Anna vuosi **Kalenterivuodesta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="19206-125">Anna vuosi **Kalenterivuoteen**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="19206-126">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="19206-128">Tuntikohtaisen kanavamyynnin raportti</span><span class="sxs-lookup"><span data-stu-id="19206-128">Channel sales by hour report</span></span>

<span data-ttu-id="19206-129">**Kanavan myynti tunnin mukaan** -raportti näyttää valitun kanavan tai toimintoyksikön myyntimittarin tunnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="19206-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="19206-130">Voit luoda **Kanavan myynti tunnin mukaan** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-131">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Kanavan myynti tunnin mukaan -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-131">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="19206-132">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-133">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-134">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="19206-136">Suurimpien asiakkaiden raportti</span><span class="sxs-lookup"><span data-stu-id="19206-136">Top customers report</span></span>

<span data-ttu-id="19206-137">**Parhaat asiakkaat** -raportissa on myyntimittarit parhaille *N* asiakkaille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="19206-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="19206-138">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="19206-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="19206-139">Voit luoda **Parhaat asiakkaat** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-140">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat asiakkaat -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-140">Go to **Retail \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="19206-141">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-142">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-143">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="19206-145">Parhaat alennukset -raportti</span><span class="sxs-lookup"><span data-stu-id="19206-145">Top discounts report</span></span>

<span data-ttu-id="19206-146">**Parhaat alennukset** -raportissa on myyntimittarit parhaille *N* alennuksille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="19206-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="19206-147">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="19206-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="19206-148">Voit luoda **Parhaat alennukset** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-149">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat alennukset -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-149">Go to **Retail \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="19206-150">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-151">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-152">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="19206-154">Parhaat tuotteet -raportti</span><span class="sxs-lookup"><span data-stu-id="19206-154">Top products report</span></span>

<span data-ttu-id="19206-155">**Parhaat tuotteet** -raportissa on myyntimittarit parhaille *N* tuotteille valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="19206-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="19206-156">Arvo *N* on luku väliltä 10–100. Se perustuu käyttäjän valitsemaan koostemittariin.</span><span class="sxs-lookup"><span data-stu-id="19206-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="19206-157">Voit luoda **Parhaat tuotteet** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-158">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Parhaat tuotteet -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-158">Go to **Retail \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="19206-159">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-160">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-161">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-162">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="19206-163">Luokan myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="19206-163">Category sales report</span></span>

<span data-ttu-id="19206-164">**Luokan myynti** -raportissa näkyvät myyntimittarit valittuna kautena jokaiselle luokkahierarkian solmulle valitussa kanavassa tai toimintoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="19206-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="19206-165">Voit luoda **Luokan myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-166">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Luokan myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-166">Go to **Retail \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="19206-167">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-168">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-169">Valitse **Kanava**-kentässä verkkokanava.</span><span class="sxs-lookup"><span data-stu-id="19206-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="19206-170">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="19206-171">Organisaation myyntiraportti</span><span class="sxs-lookup"><span data-stu-id="19206-171">Organization sales report</span></span>

<span data-ttu-id="19206-172">**Organisaation myynti** -raportti näyttää vähittäismyymälöiden suorituskyvyn organisaatioyksiköiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="19206-172">The **Organization sales** report shows the performance of your retail stores by organization unit.</span></span> <span data-ttu-id="19206-173">Tämä raportti sisältää myynnin määrän ja summan myymälän mukaan sekä kunkin myymälän katetuoton.</span><span class="sxs-lookup"><span data-stu-id="19206-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="19206-174">Organisaatioyksikkö perustuu oletusraportointihierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="19206-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="19206-175">Voit luoda **Organisaation myynti** -raportin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="19206-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="19206-176">Siirry kohtaan **Vähittäismyynti \> Kyselyt ja raportit \> Myyntiraportit \> Organisaation myynti -raportti**.</span><span class="sxs-lookup"><span data-stu-id="19206-176">Go to **Retail \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="19206-177">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-178">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="19206-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="19206-179">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="19206-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19206-180">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="19206-180">Additional resources</span></span>

- [<span data-ttu-id="19206-181">Dynamics 365 Retailin ohjeresurssit</span><span class="sxs-lookup"><span data-stu-id="19206-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
