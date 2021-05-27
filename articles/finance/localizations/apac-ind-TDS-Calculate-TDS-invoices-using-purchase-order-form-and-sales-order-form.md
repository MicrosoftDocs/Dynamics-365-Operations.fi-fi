---
title: TDS-laskujen laskeminen ostotilauslomakkeen ja myyntitilauslomakkeen avulla
description: Tässä aiheessa luetellaan erityyppisten laskujen vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023198"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="8914f-103">TDS-laskujen laskeminen ostotilauslomakkeen ja myyntitilauslomakkeen avulla</span><span class="sxs-lookup"><span data-stu-id="8914f-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8914f-104">Tässä aiheessa luetellaan vaiheet, joilla lasketaan Vero vähennettynä lähteissä (TDS) erilaisissa laskuissa **Ostotilaus**-, **Ostokirjauskansio**-, **Yleistilaus**- ja **Myyntitilaus**-sivuilla.</span><span class="sxs-lookup"><span data-stu-id="8914f-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="8914f-105">Luo ostotilaus, ostokirjauskansio, oston yleistilaus tai myyntitilaus käyttämällä luettelosivua.</span><span class="sxs-lookup"><span data-stu-id="8914f-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="8914f-106">Kirjoita tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="8914f-106">Enter the required details.</span></span>

2. <span data-ttu-id="8914f-107">Valitse **Asetukset**-välilehti, jos haluat tarkastella toimittajan tai asiakkaan arvioitavan kohteen luonnetta.</span><span class="sxs-lookup"><span data-stu-id="8914f-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="8914f-108">Nämä tiedot on lueteltu **Arvioitavan kohteen luonne** -kentässä **Ennakonpidätysryhmä**-kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="8914f-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="8914f-109">**TDS-ryhmä**-kentässä tarkastele tai muokkaa TDS-ryhmän oletusryhmää, joka on määritetty toimittajalle tai asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="8914f-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8914f-110">**TCS-ryhmä**-kenttä ei ole käytettävissä, kun valitset TDS-ryhmän **TDS-ryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8914f-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="8914f-111">TDS lasketaan vain, jos **Laske ennakonpidätys** -valintaruutu on valittuna toimittajalle tai asiakkaalle **Kaikki toimittajat**- tai **Kaikki asiakkaat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8914f-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="8914f-112">Luo nimikerivit **Rivit**-välilehdessä ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="8914f-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="8914f-113">Valitse **Asetukset**-välilehti (rivitaso), jos haluat tarkastella tai muuttaa otsikon tasolla määritettyä TDS-ryhmää.</span><span class="sxs-lookup"><span data-stu-id="8914f-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="8914f-114">TDS-ryhmä näkyy **TDS-ryhmä**-kentässä, joka on **Ennakonpidätysryhmä**-kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="8914f-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="8914f-115">Valitse **Verotiedot**-välilehti ja valitse vaihtoehtoiset osoitteet, jotka on määritetty tässä kentässä näkyvää yrityksen nimeä varten.</span><span class="sxs-lookup"><span data-stu-id="8914f-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="8914f-116">Yrityksen nimi näkyy **Nimi**-kentässä, joka on **Yritystiedot**-kenttäryhmän alla.</span><span class="sxs-lookup"><span data-stu-id="8914f-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="8914f-117">Valitun yrityksen verotilin numero (TAN) näkyy **Verotilin numero** (**TAN**) -kentässä **Ennakonpidätys**-kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="8914f-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="8914f-118">Valitse **Ennakonpidätys** avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun.</span><span class="sxs-lookup"><span data-stu-id="8914f-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="8914f-119">Tarkastele seuraavia kenttiä tilapäisten **Väliaikaiset ennakonpidätystapahtumat** -sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="8914f-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="8914f-120">**Ennakonpidätyksen** **summa** **yhteensä** - TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="8914f-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="8914f-121">**Arvo** - Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti.</span><span class="sxs-lookup"><span data-stu-id="8914f-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="8914f-122">Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-ryhmään liitetyille TDS-verokoodeille.</span><span class="sxs-lookup"><span data-stu-id="8914f-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="8914f-123">**Oikaistu ennakonpidätyksen summa yhteensä** - Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="8914f-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="8914f-124">**TDS** - Jos tämä on valittuna, tapahtumaan liittyy TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="8914f-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="8914f-125">**Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehtien kentissä **Väliaikaiset ennakonpidätystapahtumat** -sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="8914f-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="8914f-126">Valitse **Raja** avataksesi **Raja**-sivun.</span><span class="sxs-lookup"><span data-stu-id="8914f-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="8914f-127">Näytä tiettyyn TDS-verokoodiin tällä sivulla liitetylle TDS-verokomponentille määritetty raja-arvo.</span><span class="sxs-lookup"><span data-stu-id="8914f-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="8914f-128">Avaa **Kaavojen suunnittelutoiminto** avataksesi **Kaavojen suunnittelutoiminto** -sivun.</span><span class="sxs-lookup"><span data-stu-id="8914f-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="8914f-129">Tarkastele kaavaa, joka on määritetty tietylle TDS-verokoodille tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="8914f-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="8914f-130">Kirjaa lasku.</span><span class="sxs-lookup"><span data-stu-id="8914f-130">Post the invoice.</span></span> <span data-ttu-id="8914f-131">Ostolaskuissa laskettu TDS- summa kirjataan ostoreskontratilille ja myyntilaskuissa laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-ryhmän TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="8914f-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="8914f-132">TDS-verokoodien ostoreskontran tai myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8914f-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="8914f-133">Valitse **Kysely**-painike **> Lasku > Kirjattu ennakonpidätys** -painike avataksesi **Ennakonpidätystapahtumat**-sivun.</span><span class="sxs-lookup"><span data-stu-id="8914f-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="8914f-134">Voit tarkastella tapahtuman TDS:n laskemiseen käytettyä kokonaisprosenttia **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8914f-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="8914f-135">**Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä **Ennakonpidätystapahtumat**-sivulla näkyvät tapahtumalle lasketun TDS:n tiedot.</span><span class="sxs-lookup"><span data-stu-id="8914f-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="8914f-136">Näytä kunkin TDS-ryhmään liitetyn TDS-verokoodin TDS-laskentatiedot.</span><span class="sxs-lookup"><span data-stu-id="8914f-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
