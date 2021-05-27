---
title: TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen
description: Tässä aiheessa kerrotaan, miten TDS-maksut tilitetään TDS-viranomaistoimittajille.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023215"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="3b89b-103">TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen</span><span class="sxs-lookup"><span data-stu-id="3b89b-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b89b-104">Tässä aiheessa kerrotaan, miten TDS-maksut tilitetään TDS-viranomaistoimittajille.</span><span class="sxs-lookup"><span data-stu-id="3b89b-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="3b89b-105">Valitse **Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="3b89b-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="3b89b-106">[![Toimittajan maksukirjauskansio -sivu](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="3b89b-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="3b89b-107">Valitse **Toimittajan maksukirjauskansio** -sivulla **Uusi** luodaksesi kirjauskansion rivin.</span><span class="sxs-lookup"><span data-stu-id="3b89b-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="3b89b-108">Valitse **Tili**-kentässä TDS-viranomaistoimittaja, jolle tilitetään TDS-maksut.</span><span class="sxs-lookup"><span data-stu-id="3b89b-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="3b89b-109">Valitse **Tilitystapahtumat** avataksesi **Tilitystapahtumat**-sivun, jolla voit tarkastella TDS-viranomaistoimittajan tilitettyjä TDS-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3b89b-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="3b89b-110">Tilityskauden tilitetyt TDS-tapahtumat näytetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="3b89b-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="3b89b-111">TDS-tapahtumat, joissa arvioinnin kohteen luokka on **Yritys**, näkyy yhtenä tapahtumarivinä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="3b89b-112">TDS-tapahtumat, joiden arvioitavan kohteen luonne on **HUF**, **Firma**, **Yksittäinen**, **AOP**, **BOI**, **Paikallinen viranomainen** tai **Muut**, näkyvät yhtenä tapahtumarivinä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="3b89b-113">**Summa**-kentässä näkyy TDS-kokonaissumma, joka on maksettava TDS-viranomaistoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="3b89b-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="3b89b-114">Valitsemalla **Ennakonpidätystapahtumat** voit tarkastella eri TDS-tapahtumia, jotka sisältyvät tilitystietueeseen.</span><span class="sxs-lookup"><span data-stu-id="3b89b-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="3b89b-115">Voit tarkastella kunkin TDS-tapahtuman jakoa, joka on sisällytetty tilityskauden tilitysprosessiin tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="3b89b-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="3b89b-116">Valitse **Yhteenveto**-välilehdestä **Merkitse**-valintaruutu TDS-tapahtumille, jotka tilitetään TDS-viranomaistoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="3b89b-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="3b89b-117">**Yhteenveto**-sivulla näkyvät seuraavat tiedot kutakin avointa TDS-tapahtumaa varten:</span><span class="sxs-lookup"><span data-stu-id="3b89b-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="3b89b-118">**Päivämäärä** – TDS-tapahtumapäivä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="3b89b-119">**Tosite** – Tositteen numero.</span><span class="sxs-lookup"><span data-stu-id="3b89b-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="3b89b-120">**Lähde** – Moduuli, josse TDS-tapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="3b89b-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="3b89b-121">**Toimittaja/asiakas** – Toimittajan tai asiakkaan tilinumero, josta TDS vähennetään.</span><span class="sxs-lookup"><span data-stu-id="3b89b-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="3b89b-122">**Vähennyksen saajan/osapuolen nimi** – Toimittajan tai asiakkaan nimi, joilta TDS vähennetään.</span><span class="sxs-lookup"><span data-stu-id="3b89b-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="3b89b-123">**Arvioitavan kohteen luonne** – Sen arvioitavan kohteen luokan luonne, johon vähennyksen saaja kuuluu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="3b89b-124">**Summa** – Laskun summa, jonka perusteella TDS laskettiin.</span><span class="sxs-lookup"><span data-stu-id="3b89b-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="3b89b-125">**Veron summa** – Tapahtumalle laskettu TDS-summa.</span><span class="sxs-lookup"><span data-stu-id="3b89b-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b89b-126">Poista niiden TDS-tapahtumien **Merkitse**-valintaruudun valinta, joita ei pitäisi selvittää TDS-viranomaistoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="3b89b-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="3b89b-127">**Yleinen**-välilehden **PAN**-kentässä näkyy vähennyksen saajan pysyvä tilinumero (PAN).</span><span class="sxs-lookup"><span data-stu-id="3b89b-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="3b89b-128">**Päivämäärä**-kentässä näkyy TDS-laskelman päivämäärä, ja **Arvo**-kentässä näkyy TDS-laskennassa käytetty kokonaisprosentti.</span><span class="sxs-lookup"><span data-stu-id="3b89b-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="3b89b-129">Valitsemalla **Tosite** voit tarkastella TDS-tapahtuman tositemerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="3b89b-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-130">Close the page.</span></span>
10. <span data-ttu-id="3b89b-131">Avaa **Ennakonpidätyksen komponentit** -sivu valitsemalla **Ennakonpidätyksen komponentit**. Sivulla voit tarkastella TDS-verokomponenttia kohti laskettua TDS:ää tietylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="3b89b-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="3b89b-132">**Yhteenveto**-välilehden **Verokomponentti**-kentässä näkyy tapahtumassa käytetty TDS-verokomponentti.</span><span class="sxs-lookup"><span data-stu-id="3b89b-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="3b89b-133">**Summa**-kentässä näkyy TDS-summa, joka on laskettu TDS-verokomponentille perusvaluuttana.</span><span class="sxs-lookup"><span data-stu-id="3b89b-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="3b89b-134">**Kertynyt summa** -kentässä näkyy TDS-kokonaissumma, joka on laskettu kaikkien tilitettyjen tapahtumien TDS-komponentille.</span><span class="sxs-lookup"><span data-stu-id="3b89b-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="3b89b-135">**Summa**-välilehden **Oletusvaluutta**-osassa näkyy TDS-verokomponentille laskettu TDS-veron summa oletusvaluuttana.</span><span class="sxs-lookup"><span data-stu-id="3b89b-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="3b89b-136">**Toissijainen valuutta** -osassa summa esitetään toissijaisena valuuttana.</span><span class="sxs-lookup"><span data-stu-id="3b89b-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="3b89b-137">Sulje **Ennakonpidätyksen komponentit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="3b89b-138">Huomaa **Avoimen tapahtuman muokkaus** -sivulla **Summa**-kentäss, että TDS-viranomaistoimittajalle tilitettävä kokonaissumma tilityskaudelta päivitetään.</span><span class="sxs-lookup"><span data-stu-id="3b89b-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="3b89b-139">Jos haluat selvittää eri TDS-tilityskausien TDS-tapahtumat TDS-viranomaistoimittajalle, valitse tapahtumien **Merkitse**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="3b89b-140">Sulje **Avoimen tapahtuman muokkaus** -sivu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b89b-141">Jos **Ennakonpidätystapahtumat**-sivulla on valittu tilitystä varten vain muutamia tapahtumia, valittujen tapahtumien TDS-kokonaissumma päivitetään **Korjaus**-kentässä **Avoimen tapahtuman muokkaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3b89b-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="3b89b-142">Korjaussumma päivitetään **Kirjaustosite**-sivun kirjauskansion rivillä, ja **Avoimen tapahtuman muokkaus** -sivu suljetaan.</span><span class="sxs-lookup"><span data-stu-id="3b89b-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="3b89b-143">**Kirjaustosite**-sivulla **Veloitus**-kentässä näkyy kokonaissumma, joka maksetaan TDS-viranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="3b89b-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="3b89b-144">Kirjoita vastatilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="3b89b-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b89b-145">Jos TDS-tapahtumilla on eri TAN-numerot, **Kirjaustosite**-sivulle luodaan kirjauskansion rivit TAN-numeroa kohden.</span><span class="sxs-lookup"><span data-stu-id="3b89b-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="3b89b-146">Valitse **Toimitusmaksu**-välilehden **Maksutunnus**-kentästä maksun tunnus, jonka maksutyyppi on **Korko** tai **Muut**, jos haluat veloittaa toimitusmaksun TDS-viranomaistoimittajalle suoritetuista viivästyneistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="3b89b-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="3b89b-147">**Verotiedot**-välilehden **Yritystiedot**-osassa **Nimi**-kentässä näkyy yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="3b89b-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="3b89b-148">**Ennakonpidätys**-osassa **Verotilin numero (TAN)** -kentässä näkyy tapahtumariviin liittyvä TAN.</span><span class="sxs-lookup"><span data-stu-id="3b89b-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="3b89b-149">Vahvista ja kirjaa kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="3b89b-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="3b89b-150">Valitse **Ennakonpidätys \> Challan-tiedot** syöttääksesi tapahtuman challan-tiedot.</span><span class="sxs-lookup"><span data-stu-id="3b89b-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="3b89b-151">**Tosite**-kentässä näkyy tapahtuman tositenumero.</span><span class="sxs-lookup"><span data-stu-id="3b89b-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="3b89b-152">Valitse **Kirjamerkinnän avulla talletettu TDS** -valintaruutu, jos TDS-summa talletetaan kirjamerkinnän avulla.</span><span class="sxs-lookup"><span data-stu-id="3b89b-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="3b89b-153">Kirjoita **Challan-numero**-kenttään challan-numero, jota käytetään maksun suorittamiseen TDS-viranomaistoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="3b89b-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="3b89b-154">Syötä **Päivämäärä**-kenttään challan-päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="3b89b-155">Valitse **Pankin nimi** -kentässä sen pankin nimi, jonne TDS-viranomaistoimittajalle maksettava TDS-summa talletetaan.</span><span class="sxs-lookup"><span data-stu-id="3b89b-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="3b89b-156">Tässä kentässä luetellaan kaikki pankkitilit, jotka on määritetty TDS-viranomaistoimittajalle kohdassa **Ostoreskontra \> Kaikki toimittajat \> Asetukset \> Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="3b89b-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="3b89b-157">Syötä **BSR-koodi**-kenttään pankin Basic Statistical Return (BSR) -koodi.</span><span class="sxs-lookup"><span data-stu-id="3b89b-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="3b89b-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3b89b-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="3b89b-159">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="3b89b-159">Example</span></span>

<span data-ttu-id="3b89b-160">Kausi 1.4.2009 selvitetään **Vuokra**-TDS-komponenttiryhmälle käyttämällä kausittaista TDS-selvitysprosessia.</span><span class="sxs-lookup"><span data-stu-id="3b89b-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="3b89b-161">TDS-kokonaissumma 141 625,00 kirjataan TDS-toimittajaviranomaisen tilille TDS-tilityskaudelta.</span><span class="sxs-lookup"><span data-stu-id="3b89b-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="3b89b-162">Voit tarkastella tätä summaa TDS-viranomaistoimittajan **Avoimen tapahtuman muokkaus** -sivun **Summa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="3b89b-163">Jos valitset **Ennakonpidätystapahtumat** tarkastellaksesi kauden tilitettyjä TDS-tapahtumia, seuraavat tiedot ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="3b89b-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="3b89b-164">TDS-summa</span><span class="sxs-lookup"><span data-stu-id="3b89b-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="3b89b-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-165">16,995.00</span></span>  |
| <span data-ttu-id="3b89b-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-166">22,660.00</span></span>  |
| <span data-ttu-id="3b89b-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-167">28,325.00</span></span>  |
| <span data-ttu-id="3b89b-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-168">16,995.00</span></span>  |
| <span data-ttu-id="3b89b-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-169">28,325.00</span></span>  |
| <span data-ttu-id="3b89b-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-170">16,995.00</span></span>  |
| <span data-ttu-id="3b89b-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-171">11,330.00</span></span>  |

<span data-ttu-id="3b89b-172">Tietyn TDS-summan kohdalla voit valita **Ennakonpidätyksen komponentit** tarkastellaksesi TDS-verokomponenttia kohti laskettua TDS:ää tietylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="3b89b-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="3b89b-173">Tässä esimerkissä valitaan **Ennakonpidätyksen komponentit** TDS-summalle 16 995,00.</span><span class="sxs-lookup"><span data-stu-id="3b89b-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="3b89b-174">Tapahtumalle komponenttikohtaisesti laskettu veron summa näytetään.</span><span class="sxs-lookup"><span data-stu-id="3b89b-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="3b89b-175">Verokomponentti</span><span class="sxs-lookup"><span data-stu-id="3b89b-175">Tax component</span></span> | <span data-ttu-id="3b89b-176">Määrä</span><span class="sxs-lookup"><span data-stu-id="3b89b-176">Amount</span></span>    | <span data-ttu-id="3b89b-177">Kumulatiivinen summa</span><span class="sxs-lookup"><span data-stu-id="3b89b-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="3b89b-178">TDS</span><span class="sxs-lookup"><span data-stu-id="3b89b-178">TDS</span></span>           | <span data-ttu-id="3b89b-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-179">1,5000.00</span></span> | <span data-ttu-id="3b89b-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-180">125,000.00</span></span>         |
| <span data-ttu-id="3b89b-181">Lisämaksu</span><span class="sxs-lookup"><span data-stu-id="3b89b-181">Surcharge</span></span>     | <span data-ttu-id="3b89b-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-182">1,500.00</span></span>  | <span data-ttu-id="3b89b-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-183">12,500.00</span></span>          |
| <span data-ttu-id="3b89b-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="3b89b-184">PE-Cess</span></span>       | <span data-ttu-id="3b89b-185">330.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-185">330.00</span></span>    | <span data-ttu-id="3b89b-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-186">2,750.00</span></span>           |
| <span data-ttu-id="3b89b-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="3b89b-187">SHE Cess</span></span>      | <span data-ttu-id="3b89b-188">165.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-188">165.00</span></span>    | <span data-ttu-id="3b89b-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="3b89b-189">1,375.00</span></span>           |

<span data-ttu-id="3b89b-190">Jos valitse vain TDS-summat 16 995,00, 22 660,00 ja 2 8325,00 tilitykselle **Ennakonpidätystapahtumat**-sivulla, tilityksen kokonaissumma näkyy muodossa **67 980,00** **Korjaus**-kentässä **Avoimen tapahtuman muokkaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3b89b-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="3b89b-191">Jos tämä tapahtuma on merkitty tilitystä varten ja **Avoimen tapahtuman muokkaus** -sivu on suljettu, summa **67 980,00** näkyy **Veloitus**-kentässä **Kirjaustosite**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3b89b-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="3b89b-192">Voit nyt kirjata kirjauskansion ja luoda TDS-challan-numeron.</span><span class="sxs-lookup"><span data-stu-id="3b89b-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="3b89b-193">TDS-viranomaistoimittajille tehtyjen ennakkomaksujen oikaisu</span><span class="sxs-lookup"><span data-stu-id="3b89b-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="3b89b-194">Voit oikaista TDS-viranomaistoimittajalle maksetun ennakkomaksun todelliseksi maksuksi valitsemalla **Ostoreskontra \> Toimittajat \> Kaikki toimittajat \> Tapahtumien muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="3b89b-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="3b89b-195">Jos todellinen tehty maksu ylittää ennakkomaksun, tapahtumalle luodaan kaksi challan-numeroa.</span><span class="sxs-lookup"><span data-stu-id="3b89b-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="3b89b-196">TDS-kyselyssä näkyy kuitenkin vain ensimmäinen challan-numero.</span><span class="sxs-lookup"><span data-stu-id="3b89b-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
