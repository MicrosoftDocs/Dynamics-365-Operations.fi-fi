---
title: Maksettaessa maksettavien toimittajan maksujen määrittäminen ja käyttäminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan maksa, kun maksettu (PWP)-ehtoja, jotta voit vapauttaa osittaiset toimittajamaksut asiakasmaksujen perusteella.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284110"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="bb85a-103">Maksettaessa maksettavien toimittajan maksujen määrittäminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="bb85a-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb85a-104">Kun hyväksyt toimittajan työskentelemään alihankkijaksi, haluat ehkä pidättää toimittajan maksun, kunnes asiakas on maksanut sinulle projektista.</span><span class="sxs-lookup"><span data-stu-id="bb85a-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="bb85a-105">Tämän skenaarion tukemiseksi voit pidättää maksun toimittajalle määrittämällä toimittajan ostotilaukseen (PO) Maksa, kun maksettu -ehdon.</span><span class="sxs-lookup"><span data-stu-id="bb85a-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="bb85a-106">Voit esimerkiksi vapauttaa joitakin tai kaikki toimittajan laskut maksettaviksi, kun asiakas maksaa projektilaskun summan.</span><span class="sxs-lookup"><span data-stu-id="bb85a-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="bb85a-107">Määritä Maksu, kun maksettu -ehdot määrittämään, että toimittajalle maksetaan sen jälkeen, kun vastaanotat asiakkaalta tietyn prosenttiosuuden liittyvästä maksusta.</span><span class="sxs-lookup"><span data-stu-id="bb85a-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="bb85a-108">Jos vastaanotat asiakkaalta osamaksun, voit vapauttaa manuaalisesti maksun osan liittyvistä toimittajan laskuista.</span><span class="sxs-lookup"><span data-stu-id="bb85a-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="bb85a-109">Seuraavassa esimerkissä kuvataan prosessi, jossa PWP-termejä käytetään.</span><span class="sxs-lookup"><span data-stu-id="bb85a-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="bb85a-110">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="bb85a-110">Example</span></span>

<span data-ttu-id="bb85a-111">Organisaatiosi sitoutuu tarjoamaan asiakkaalle 100 tietokonetta, joissa on asennettuna ohjelmisto, jonka hinta on 150,00 Yhdysvaltain dollaria (USD) tietokonetta kohden.</span><span class="sxs-lookup"><span data-stu-id="bb85a-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="bb85a-112">Tämän jälkeen voit palkata toimittajan tarjoamaan tietokoneita, joihin on asennettu ohjelmisto.</span><span class="sxs-lookup"><span data-stu-id="bb85a-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="bb85a-113">Sopimuksen mukaan asiakkaan on hyväksyttävä tietokoneiden laatu, ennen kuin se maksaa organisaatiollesi.</span><span class="sxs-lookup"><span data-stu-id="bb85a-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="bb85a-114">Organisaatiosi käytäntö on evätä toimittajalle maksu, kunnes asiakas on maksanut sinulle.</span><span class="sxs-lookup"><span data-stu-id="bb85a-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="bb85a-115">Tämän vuoksi voit määrittää projektin niin, että sen PWP-prosenttiosuus on 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="bb85a-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="bb85a-116">Toimittaja lähettää 100 tietokonetta, joihin on asennettu ohjelmisto, sekä 10 000,00 USD:n laskun.</span><span class="sxs-lookup"><span data-stu-id="bb85a-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="bb85a-117">Koska PWP-ehdot on määritetty projektiasi varten, et maksa toimittajalle tietokoneiden vastaanottamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bb85a-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="bb85a-118">Sen sijaan lähetät tietokoneet asiakkaalle sekä laskun, jonka summa on 15 000,00.</span><span class="sxs-lookup"><span data-stu-id="bb85a-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="bb85a-119">Asiakas tarkastaa tietokoneet ja hyväksyy projektilaskun täyden määrän.</span><span class="sxs-lookup"><span data-stu-id="bb85a-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="bb85a-120">Kun koko maksu on vastaanotettu asiakkaalta, maksat toimittajalle, 10 000,00, koko toimittajan laskun summan.</span><span class="sxs-lookup"><span data-stu-id="bb85a-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="bb85a-121">Määritä projektin PWP-ehdot</span><span class="sxs-lookup"><span data-stu-id="bb85a-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="bb85a-122">Kun määrität projektin PWP-ehdot, sinun on määritettävä prosenttiosuutena vähimmäissumma, joka asiakkaan on maksettava projektista, ennen kuin maksat toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="bb85a-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="bb85a-123">Summan raja-arvo lasketaan automaattisesti projektin myyntilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="bb85a-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="bb85a-124">Seuraa näitä ohjeita määrittääksesi kynnysprosentin PWP-ehdoille.</span><span class="sxs-lookup"><span data-stu-id="bb85a-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="bb85a-125">Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="bb85a-126">Etsi ja avaa projekti, jolle haluat määrittää PWP-ehdot.</span><span class="sxs-lookup"><span data-stu-id="bb85a-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="bb85a-127">Valitse **Toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="bb85a-128">Valitse **Tilikoodi** -kentästä jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="bb85a-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="bb85a-129">**Taulu** – PWP-ehtoja sovelletaan yksittäiseen toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="bb85a-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="bb85a-130">**Ryhmä** – PWP-ehtoja sovelletaan kaikkiin toimittajaryhmän toimittajiin.</span><span class="sxs-lookup"><span data-stu-id="bb85a-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="bb85a-131">**Kaikki** – PWP-ehtoja sovelletaan kaikkiin toimittajiin.</span><span class="sxs-lookup"><span data-stu-id="bb85a-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="bb85a-132">Jos valitsit edellisessä vaiheessa **Taulu** tai **Ryhmä**, valitse **toimittaja/toimittajaryhmä**-kentästä toimittaja tai toimittajaryhmä, joita PWP-ehdot koskevat.</span><span class="sxs-lookup"><span data-stu-id="bb85a-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="bb85a-133">Jos valitsit edellisessä vaiheessa **Kaikki**, **Toimittaja/toimittajaryhmä**-kenttää ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="bb85a-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="bb85a-134">Jos toimittajan pidätysehdot on määritetty myyjälle projektissa **Toimittajan pidätysehdot** -kentässä, valitse säännön tunnus pidätysehdoille.</span><span class="sxs-lookup"><span data-stu-id="bb85a-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="bb85a-135">Syötä **PWP-kynnysprosentti**-kentässä projektin kynnysprosenttiarvo.</span><span class="sxs-lookup"><span data-stu-id="bb85a-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="bb85a-136">Syöttämäsi prosentti määrittää projektin vähimmäissumman, joka asiakkaan on maksettava sinulle, ennen kuin maksat toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="bb85a-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="bb85a-137">Luo ostotilaus, jossa on PWP-termejä</span><span class="sxs-lookup"><span data-stu-id="bb85a-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="bb85a-138">Kun kirjaat toimittajan laskun ja toimittajaan pätevät PWP-ehdot, PWP-ehdot näkyvät PO:n riveillä.</span><span class="sxs-lookup"><span data-stu-id="bb85a-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="bb85a-139">Jos haluat luoda ostotilauksen, jossa on PWP-ehtoja, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="bb85a-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="bb85a-140">Siirry kohtaan **Hankinta ja alihankinta** \> **Ostotilaukset** \> **Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="bb85a-141">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="bb85a-142">Kirjoita sitten **Luo ostotilaus** -valintaikkunaan tarvittavat tiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="bb85a-143">Vaihtoehtoisesti voit avata olemassa olevan ostotilauksen **Kaikki ostotilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="bb85a-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="bb85a-144">Tarkasta **Ostotilaus**-lomakkeen **Ostotilausrivit**-pikavälilehdessä toimittajan PO:n tiedot.</span><span class="sxs-lookup"><span data-stu-id="bb85a-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="bb85a-145">**Maksu, kun maksettu** -vaihtoehto valitaan automaattisesti, ja **PWP-kynnysprosentti**-kentän arvo kopioidaan automaattisesti **PWP-kynnysprosentti** -kentästä **Projektit**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="bb85a-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="bb85a-146">Jos et halua käyttää PWP-ehtoja ostotilausrivin toimittajalle, poista **Maksu, kun maksettu** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="bb85a-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="bb85a-147">Tässä tapauksessa ostotilausrivin **PWP-kynnysprosentti** -kentän arvoksi palautetaan 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="bb85a-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="bb85a-148">Päivitä asiakkaan maksut ja maksa toimittajalle</span><span class="sxs-lookup"><span data-stu-id="bb85a-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="bb85a-149">Kun toimittajan työ tässä projektissa on valmis, ja hän lähettää laskun, tarkasta projektin tila ja asiakkaan laskut määrittääksesi, ovatko projektin PWP-ehdot täyttyneet.</span><span class="sxs-lookup"><span data-stu-id="bb85a-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="bb85a-150">Jos toimittajan PWP-ehdot on täytetty, voit määrittää mitkä rivit toimittajan laskusta maksetaan projektin asiakasmaksujen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb85a-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="bb85a-151">Jos päätät maksaa toimittajalle, vaikka PWP-ehtoja ei olisi täytetty, voit ohittaa PWP-ehdot **Toimittajalasku maksa, kun maksettu -ehto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bb85a-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="bb85a-152">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kyselyt ja raportit** \> **Pidätyskysely** \> **Toimittajalasku maksa, kun maksettu -ehto**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="bb85a-153">Syötä tarkastettavien toimittajien laskujen haku-kenttään arvot, joissa on **Toimittajalasku maksa, kun maksettu -ehto** -sivu, ja valitse sitten **Hae**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="bb85a-154">Valitse muutettavien rivien **Toimittajalaskun rivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bb85a-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="bb85a-155">Jos laskurivin **Maksu, kun maksettu** -ehdot täyttyvät, valitse **Vapauta toimittajan maksu**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="bb85a-156">**Maksu, kun maksettu** -vaihtoehto tyhjennetään, ja **Valmis maksettavaksi** -kentän arvoksi vaihdetaan **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bb85a-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>