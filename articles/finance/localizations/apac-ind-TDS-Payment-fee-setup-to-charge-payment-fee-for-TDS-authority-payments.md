---
title: Määritä TDS-viranomaisen maksujen toimitusmaksut
description: Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -viranomaisen maksujen toimitusmaksut.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023223"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="124ac-103">Määritä TDS-viranomaisen maksujen toimitusmaksut</span><span class="sxs-lookup"><span data-stu-id="124ac-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="124ac-104">Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -viranomaisen maksujen toimitusmaksut.</span><span class="sxs-lookup"><span data-stu-id="124ac-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="124ac-105">Siirry kohtaan **Ostoreskontra \> Maksun asetukset \> Toimitusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="124ac-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="124ac-106">[![Toimitusmaksu-sivu](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="124ac-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="124ac-107">Luo toimitusmaksu valitsemalla **Uusi** ja kirjoita tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="124ac-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="124ac-108">Valitse toimitusmaksun tyyppi **Maksun tyyppi** -kentästä:</span><span class="sxs-lookup"><span data-stu-id="124ac-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="124ac-109">**None**</span><span class="sxs-lookup"><span data-stu-id="124ac-109">**None**</span></span>
    - <span data-ttu-id="124ac-110">**Korko** – Korko veloitetaan TDS-viranomaistoimittajalle suoritetuista myöhästyneistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="124ac-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="124ac-111">**Muut** – Muut maksut veloitetaan TDS-viranomaistoimittajalle suoritetuista myöhästyneistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="124ac-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="124ac-112">Jos valitset **Korko** tai **Muut**, **Maksu**-kentän arvoksi tulee automaattisesti **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="124ac-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="124ac-113">Jos valitset **Korko** tai **Muut** **Kenttätyyppi**-kentässä **Päätili**-kentässä valitse kirjanpitotili, jolle korko tai muut kulut kirjataan.</span><span class="sxs-lookup"><span data-stu-id="124ac-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="124ac-114">Lisää muut pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="124ac-114">Enter the other required details.</span></span>
6. <span data-ttu-id="124ac-115">Avaa **Toimitusmaksujen asetukset** -sivu valitsemalla **Toimitusmaksujen asetukset** toimintoruudussa. Sivulla voit määrittää toimitusmaksut erilaisille pankkien, maksutapojen, maksuerittelyjen, valuuttojen ja päivämäärävälien yhdistelmille.</span><span class="sxs-lookup"><span data-stu-id="124ac-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="124ac-116">[![Toimitusmaksujen asetukset -sivu](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="124ac-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="124ac-117">Määritä **Yhteenveto**-välilehden **Ryhmittelyt**-kentässä pankit, joille olet määrittänyt toimitusmaksun:</span><span class="sxs-lookup"><span data-stu-id="124ac-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="124ac-118">**Taulukko** – Maksu on voimassa tietylle pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="124ac-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="124ac-119">**Ryhmä** – Maksu on voimassa tietylle pankkiryhmälle.</span><span class="sxs-lookup"><span data-stu-id="124ac-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="124ac-120">**Kaikki** – maksu on voimassa kaikille pankkitileille.</span><span class="sxs-lookup"><span data-stu-id="124ac-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="124ac-121">Jos valitsit **Ryhmittelyt**-kentästä **Taulukko** tai **Ryhmä**, valitse **Pankkisuhde**-kentästä tietty pankkitili tai pankkiryhmä, jolle olet määrität toimitusmaksun.</span><span class="sxs-lookup"><span data-stu-id="124ac-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="124ac-122">Valitse **Maksutapa**-kentässä maksutapa, jota maksujen maksamiseen käytetään.</span><span class="sxs-lookup"><span data-stu-id="124ac-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="124ac-123">Valitse tai lisää **Maksumäärittely**-kentässä **Maksumäärittely**-sivulla luotu maksumäärittelykoodi.</span><span class="sxs-lookup"><span data-stu-id="124ac-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="124ac-124">Maksumäärittelyä käytetään sähköisen rahansiirron maksutavoissa.</span><span class="sxs-lookup"><span data-stu-id="124ac-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="124ac-125">Valitse **Maksun valuutta** -kentässä maksun aktivoiva valuutta.</span><span class="sxs-lookup"><span data-stu-id="124ac-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="124ac-126">Vain valittua valuuttaa käyttävät tapahtumat voivat aktivoida maksun.</span><span class="sxs-lookup"><span data-stu-id="124ac-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="124ac-127">Jos jätät tämän kentän tyhjäksi, kaikki valuutat aktivoivat maksun.</span><span class="sxs-lookup"><span data-stu-id="124ac-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="124ac-128">Valitse laskentatapa **Prosentti/Summa**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="124ac-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="124ac-129">Vaihtoehdot ovat **Summa**, **Prosentti** ja **Väli**.</span><span class="sxs-lookup"><span data-stu-id="124ac-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="124ac-130">Määritä **Maksun summa** -kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.</span><span class="sxs-lookup"><span data-stu-id="124ac-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="124ac-131">Valitse **Maksun valuutta** -kentässä maksun valuuttakoodi.</span><span class="sxs-lookup"><span data-stu-id="124ac-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="124ac-132">Valitse **Yleinen**-välilehti, jos haluat tarkastella tai muokata valitun pankkitilin tietoja.</span><span class="sxs-lookup"><span data-stu-id="124ac-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="124ac-133">[![Yleinen-välilehti](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="124ac-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="124ac-134">Kirjoita **Vähintään**-kenttään tapahtuman vähimmäissumma, joka aktivoi maksun.</span><span class="sxs-lookup"><span data-stu-id="124ac-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="124ac-135">Kirjoita **Enintään**-kenttään tapahtuman enimmäissumma, joka aktivoi maksun.</span><span class="sxs-lookup"><span data-stu-id="124ac-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="124ac-136">Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin maksujen laskennan päivämääräväli.</span><span class="sxs-lookup"><span data-stu-id="124ac-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="124ac-137">Määritä **Vähimmäissumma**-kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.</span><span class="sxs-lookup"><span data-stu-id="124ac-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="124ac-138">Valitse **Arvonlisäveroryhmä**-kentässä arvonlisäveroryhmä, jonka avulla maksun summan arvonlisävero lasketaan.</span><span class="sxs-lookup"><span data-stu-id="124ac-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="124ac-139">Valitse **Nimikkeen arvonlisäveroryhmä**-kentässä nimikkeen arvonlisäveroryhmä, jonka avulla maksun summan nimikkeen arvonlisävero lasketaan.</span><span class="sxs-lookup"><span data-stu-id="124ac-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="124ac-140">Valitse **Väli**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="124ac-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="124ac-141">[![Väli-välilehti](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="124ac-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="124ac-142">Kirjoita maksun kirjauspäivämäärän (alennuksen päivämäärän) ja velkakirjan eräpäivän välinen aika päivinä **Päivää**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="124ac-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="124ac-143">Valitse **Prosentti/summa**-kentässä, onko määritys prosentti vai määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="124ac-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="124ac-144">Määritä **Maksun summa**-kenttään maksun summa joko maksun prosenttiosuutena tai yhden maksun summana.</span><span class="sxs-lookup"><span data-stu-id="124ac-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="124ac-145">Sulje **Toimitusmaksujen asetukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="124ac-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="124ac-146">Sulje **Toimitusmaksu**-sivu.</span><span class="sxs-lookup"><span data-stu-id="124ac-146">Close the **Payment fee** page.</span></span>
