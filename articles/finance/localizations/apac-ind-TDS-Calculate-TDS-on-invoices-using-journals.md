---
title: Laskujen TDS:n laskeminen kirjauskansioiden avulla
description: Tässä aiheessa luetellaan kirjauskansioiden vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023222"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="48936-103">Laskujen TDS:n laskeminen kirjauskansioiden avulla</span><span class="sxs-lookup"><span data-stu-id="48936-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48936-104">Tässä aiheessa luetellaan kirjauskansioiden vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="48936-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="48936-105">Aloita avaamalla **Yleiset kirjauskansiot** -sivu (**Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot**).</span><span class="sxs-lookup"><span data-stu-id="48936-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="48936-106">[![Yleiset kirjauskansiot](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="48936-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="48936-107">Luo kirjauskansiorivejä taulussa lueteltujen kirjauskansiolomakkeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="48936-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="48936-108">Valitse tilityyppi ja vastatilin tyyppi ja kirjoita tapahtuman summa.</span><span class="sxs-lookup"><span data-stu-id="48936-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="48936-109">Valitse **Hyväksyttyjen laskujen kirjauskansio** -sivulla **Etsi tositteet** ja valitse, joissa TDS lasketaan.</span><span class="sxs-lookup"><span data-stu-id="48936-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="48936-110">Tarkastele **Laskurekisteri**-sivulla tai **Etsi tositteet** -sivulla luotuja laskuja.</span><span class="sxs-lookup"><span data-stu-id="48936-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="48936-111">**Yleiset**-välilehdessä **Kirjaustosite**-sivulla tarkastele tai muokkaa toimittajalle tai asiakkaalle määritettyä oletusarvoista TDS-ryhmää **TDS-ryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="48936-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="48936-112">Kirjauskansion riveille laskettu TDS-summa perustuu **TDS-ryhmä**-kentässä luetelluille TDS-verokoodeille määritettyyn kaavaan.</span><span class="sxs-lookup"><span data-stu-id="48936-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="48936-113">**Ennakonpidätysryhmä**-kenttä ja **TCS-ryhmä**-kenttä eivät ole käytettävissä, kun valitset TDS-ryhmän **TDS-ryhmä**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="48936-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="48936-114">**Ennakonpidätysryhmä**-kenttä on käytettävissä vain **Kirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="48936-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="48936-115">TDS lasketaan vain, jos **Laske ennakonpidätys** -valintaruutu on valittuna toimittajalle tai asiakkaalle **Kaikki toimittajat**- tai **Kaikki asiakkaat** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="48936-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="48936-116">Valitse **Verotiedot**-välilehti ja valitse yrityksen vaihtoehtoinen osoite, joka on määritetty tässä kentässä näkyvää yritystä varten, tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="48936-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="48936-117">Yrityksen nimi näkyy **Nimi**-kentässä, joka on **Yritystiedot**-kenttäryhmän alla.</span><span class="sxs-lookup"><span data-stu-id="48936-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="48936-118">Voit tarkastella toimittajan tai asiakkaan arvioitavan kohteen luonnetta **Arvioitavan kohteen luonne** -kentässä, joka kuuluu **Ennakonpidätys**-kenttäryhmään.</span><span class="sxs-lookup"><span data-stu-id="48936-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="48936-119">**Verotilin numero** (**TAN**) -kentässä tarkastele valitun yrityksen näkyvissä olevaa TAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="48936-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="48936-120">Valitse **Ennakonpidätys** **Ennakonpidätys**-valikossa avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun.</span><span class="sxs-lookup"><span data-stu-id="48936-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="48936-121">Seuraavat kentät tulevat näkyviin tilapäisten **Väliaikaiset ennakonpidätystapahtumat** -sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="48936-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="48936-122">**Ennakonpidätyksen summa yhteensä** - TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="48936-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="48936-123">**Arvo** - Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti.</span><span class="sxs-lookup"><span data-stu-id="48936-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="48936-124">Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-ryhmään liitetyille TDS-verokoodeille.</span><span class="sxs-lookup"><span data-stu-id="48936-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="48936-125">**Oikaistu ennakonpidätyksen summa yhteensä** - Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="48936-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="48936-126">**TDS** - Jos tämä on valittuna, tapahtumaan liittyy TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="48936-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="48936-127">**Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehtien kentissä **Väliaikaiset ennakonpidätystapahtumat** -sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="48936-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="48936-128">Valitse **Raja** avataksesi **Raja**-sivun.</span><span class="sxs-lookup"><span data-stu-id="48936-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="48936-129">Näytä tiettyyn TDS-verokoodiin tällä sivulla liitetylle TDS-verokomponentille määritetty raja-arvo ja poikkeusraja.</span><span class="sxs-lookup"><span data-stu-id="48936-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="48936-130">Avaa **Kaavojen suunnittelutoiminto** avataksesi **Kaavojen suunnittelutoiminto** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="48936-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="48936-131">Tarkastele kaavaa, joka on määritetty tietylle TDS-verokoodille tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="48936-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="48936-132">Sulje **Kaavan suunnittelutoiminto**- ja **Väliaikaiset ennakonpidätystapahtumat** -sivu palataksesi **Kirjaustosite**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="48936-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="48936-133">Lisää muut pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="48936-133">Enter the other required details.</span></span> <span data-ttu-id="48936-134">Vahvista ja kirjaa kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="48936-134">Validate and post the journal.</span></span> <span data-ttu-id="48936-135">Ostolaskuissa laskettu TDS-summa kirjataan ostoreskontratilille.</span><span class="sxs-lookup"><span data-stu-id="48936-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="48936-136">Myyntilaskuissa laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-verokoodille TDS-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="48936-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="48936-137">TDS-verokoodien ostoreskontran tai myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="48936-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="48936-138">Valitse **Kirjattu ennakonpidätys** avataksesi **Ennakonpidätystapahtumat**-sivun.</span><span class="sxs-lookup"><span data-stu-id="48936-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="48936-139">Tapahtuman TDS:n laskemiseen käytetty kokonaisprosentti on näkyvissä **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="48936-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="48936-140">**Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä Ennakonpidätystapahtumat-sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="48936-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
