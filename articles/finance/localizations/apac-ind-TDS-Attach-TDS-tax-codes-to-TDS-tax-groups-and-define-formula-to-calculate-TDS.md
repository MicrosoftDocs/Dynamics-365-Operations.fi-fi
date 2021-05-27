---
title: Liitä TDS-verokoodit TDS-veroryhmiin ja määritä TDS:n laskentakaava
description: Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -veroryhmät ja liitetään TDS-verokoodeja TDS-veroryhmiin. TDS-veroryhmän TDS:n laskemiseksi on määritettävä kaava siihen liitetyille TDS-verokoodeille.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023217"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="1c2c6-104">Liitä TDS-verokoodit TDS-veroryhmiin ja määritä TDS:n laskentakaava</span><span class="sxs-lookup"><span data-stu-id="1c2c6-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c2c6-105">Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -veroryhmät ja liitetään TDS-verokoodeja TDS-veroryhmiin.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="1c2c6-106">TDS-veroryhmän TDS:n laskemiseksi on määritettävä kaava siihen liitetyille TDS-verokoodeille.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="1c2c6-107">Seuraavia ohjeita noudattamalla voit määrittää TDS-veroryhmän, liittää siihen TDS-verokoodit ja määrittää TDS:n laskentakaavan.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="1c2c6-108">Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätysryhmät**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="1c2c6-109">[![Ennakonpidätysryhmät-sivu](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="1c2c6-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="1c2c6-110">Valitse toimintoruudusta **Uusi**, jos haluat luoda TDS:lle ennakonpidätysryhmän, ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="1c2c6-111">Valitse **Verotyyppi**-kentästä **TDS**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="1c2c6-112">Luo rivi valitsemalla **Asetukset**-pikavälilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="1c2c6-113">Valitse **Ennakonpidätyskoodi**-kentässä TDS-verokoodi TDS-veroryhmälle.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="1c2c6-114">**Ennakonpidätyksen nimi** -kentässä näkyy TDS-verokoodin nimi, ja **Arvo**-kenttä näyttää arvon.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="1c2c6-115">Jos haluat ohittaa TDS-tapahtumissa TDS-verokoodiin liitetylle TDS-verokomponentille määritetyn raja- ja poikkeusrajan, valitse **Ohita raja** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="1c2c6-116">Valitse **Veroton**-valintaruutu, jos haluat estää veroryhmän laskemisen tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="1c2c6-117">Avaa kaavan suunnittelutoiminto valitsemalla toimintoruudusta **Suunnittelutoiminto**, jotta voit määrittää kaavan TDS:n laskemiseksi TDS-veroryhmälle.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="1c2c6-118">**Suunnittelutoiminto**-sivulla **Verot**-välilehdessä näkyvät TDS-verokoodit, jotka on valittu TDS-veroryhmälle.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="1c2c6-119">[![Suunnittelutoiminto-sivu](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="1c2c6-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="1c2c6-120">Luo rivi valitsemalla **Laskelma**-välilehdessä **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="1c2c6-121">**Tunnus**-kentässä näkyy automaattisesti luotu TDS-laskennan prioriteettitunnus.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="1c2c6-122">Valitse **Verokoodi**-kentässä TDS-verokoodi, jolle kaava määritetään.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="1c2c6-123">Kaikki TDS-verokoodit, jotka on valittu TDS-veroryhmälle, ovat valittavissa tässä kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="1c2c6-124">Valitse **Veron peruste** -kentässä TDS-laskennan peruste:</span><span class="sxs-lookup"><span data-stu-id="1c2c6-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="1c2c6-125">**Bruttosumma** – Laske TDS-arvo tapahtuman bruttosumman perusteella (laskun summa) verokoodille määritetyn laskentalausekkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="1c2c6-126">**Ilman bruttosummaa** – Laske TDS verokoodille määritetyn laskentalausekkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c2c6-127">**Veron peruste** -kentän arvoksi ei voi määrittää **Ilman bruttosummaa** TDS-verokoodille, jonka prioriteettitunnus on **1**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="1c2c6-128">TDS-laskenta perustuu kaavaan, joka on määritetty **Laskelmalauseke**-kentässä jokaiselle TDS-veroryhmään liitetylle verokoodille.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="1c2c6-129">Valitse plusmerkki- (**+**), miinusmerkki- (**-**), kertomerkki- (**\**_) tai jakomerkki (_*/**) -painike syöttääksesi laskemalausekkeen valitulle TDS-verokoodille **Laskelmalauseke**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c2c6-130">TDS-verokoodille, jonka prioriteettitunnus on **1**, ei voida määrittää laskelmalauseketta.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="1c2c6-131">Voit määrittää TDS-verokoodin laskelmalausekkeen **Laskelmalauseke**-kentässä lisäämällä **Verot**-välilehdessä käytettävissä olevat TDS-verokoodit. Voit lisätä TDS-verokoodeja **Laskelmalauseke**-kentässä seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="1c2c6-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="1c2c6-132">Vedä tarvittava verokoodi **Verot**-välilehdestä **Laskelmalauseke**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="1c2c6-133">Kaksoisnapauta (tai kaksoisnapsauta) vaadittua verokoodia **Verot**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="1c2c6-134">Valitse ja pidä valittuna tarvittavaa verokoodia (tai paina hiiren kakkospainikkeella) **Verot**-välilehdessä ja valitse sitten **Lisää verokoodi**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c2c6-135">Lisää laskelmalauseke ennen jokaista TDS-verokoodia.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="1c2c6-136">Laskentakaavaan lisätyt TDS-verokoodit näkyvät hakasulkeissa (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="1c2c6-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="1c2c6-137">Voit poistaa verokoodille **Laskentalauseke**-kentässä määritetyn laskentalausekkeen valitsemalla **C**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="1c2c6-138">Jos haluat poistaa tietueen **Laskelma**-välilehdessä, valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="1c2c6-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c2c6-139">Close the page.</span></span>
