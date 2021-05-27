---
title: Verokomponenttien määrittäminen TDS-verotyypille
description: Tässä aiheessa kuvataan, miten ennakonpidätyksen komponentit määritetään Vero vähennettynä lähteissä (TDS) -verotyypille. Se myös kertoo, miten määritetään kunkin TDS-komponentin TDS:n laskemiseen käytettävä raja.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023203"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="ce021-104">Verokomponenttien määrittäminen TDS-verotyypille</span><span class="sxs-lookup"><span data-stu-id="ce021-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce021-105">Tässä aiheessa kuvataan, miten ennakonpidätyksen komponentit määritetään Vero vähennettynä lähteissä (TDS) -verotyypille.</span><span class="sxs-lookup"><span data-stu-id="ce021-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="ce021-106">TDS-komponentit ovat TDS, lisämaksu, PE-Cess ja SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="ce021-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="ce021-107">Aiheessa kerrotaan myös, miten määritetään kunkin TDS-komponentin TDS:n laskemiseen käytettävä raja.</span><span class="sxs-lookup"><span data-stu-id="ce021-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="ce021-108">Voit myös määrittää poikkeusraja-arvon, jota käytetään kunkin TDS-komponentin TDS-laskennassa.</span><span class="sxs-lookup"><span data-stu-id="ce021-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="ce021-109">Määritä TDS-komponentit seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ce021-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="ce021-110">Siirry kohtaan **Vero \> Asetukset \> Ennakonpidätys \> Ennakonpidätyksen komponentit**.</span><span class="sxs-lookup"><span data-stu-id="ce021-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="ce021-111">[![Ennakonpidätyksen komponentit -sivu](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="ce021-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="ce021-112">Valitse **Verotyyppi**-kentässä **TDS**, haluat määrittää ennakonpidätyksen komponentit TDS-verotyypille.</span><span class="sxs-lookup"><span data-stu-id="ce021-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="ce021-113">Valitse toimintoruudussa **Uusi** ja luo rivi.</span><span class="sxs-lookup"><span data-stu-id="ce021-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="ce021-114">Kirjoita **Ennakonpidätyksen komponentti** -kenttään TDS-komponentin nimi.</span><span class="sxs-lookup"><span data-stu-id="ce021-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="ce021-115">Valitse **Ennakonpidätyksen komponenttiryhmä** -kentässä TDS-ennakonpidätyksen komponenttiryhmä, jonne TDS-komponentti liitetään.</span><span class="sxs-lookup"><span data-stu-id="ce021-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="ce021-116">Kirjoita **Yleiset**-pikavälilehden **Kuvaus**-kenttään TDS-komponentin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ce021-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="ce021-117">Valitse toimintoruudusta **Raja** avataksesi **Raja**-sivun, jotta voit määrittää raja-arvon, jota käytetään TDS-komponentin TDS:n laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ce021-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="ce021-118">Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttien avulla kausi, jota raja koskee.</span><span class="sxs-lookup"><span data-stu-id="ce021-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="ce021-119">Määritä **Yleinen**-pikavälilehden **Raja**-kenttään rajasumma, jota käytetään TDS-komponentin TDS:n laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ce021-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="ce021-120">Vero vähennetään lähteestä vain, kun kumulatiivinen laskun summa ylittää rajan.</span><span class="sxs-lookup"><span data-stu-id="ce021-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="ce021-121">Jos rajasumma on esimerkiksi 10 000, TDS lasketaan kun kumulatiivinen laskun summa ylittää 10 000 (eli kun se on 10 001 tai suurempi).</span><span class="sxs-lookup"><span data-stu-id="ce021-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="ce021-122">Määritä **Poikkeusraja-arvo**-kenttään poikkeusraja-arvon summa, jota käytetään TDS-komponentin TDS:n laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="ce021-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="ce021-123">Laskurivillä oleva vero vähennetään lähteestä vain, kun summa ylittää poikkeusraja-arvon.</span><span class="sxs-lookup"><span data-stu-id="ce021-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="ce021-124">Jos poikkeusrajan summa on esimerkiksi 5 000, TDS lasketaan tietylle laskuriville, jos laskurivin summa ylittää 5 000 (toisin sanoen on 5 001 tai suurempi).</span><span class="sxs-lookup"><span data-stu-id="ce021-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="ce021-125">[![Raja-arvo-sivu](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="ce021-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce021-126">Poikkeusraja-arvon summan on oltava pienempi tai yhtä suuri kuin raja-arvon summa.</span><span class="sxs-lookup"><span data-stu-id="ce021-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="ce021-127">Tapahtumalle vähennetään vero, jos tapahtuman summa ylittää poikkeusraja-arvon, vaikka kumulatiivinen laskun summa ei ylittää **Raja**-kentässä määritettyä rajaa.</span><span class="sxs-lookup"><span data-stu-id="ce021-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="ce021-128">Sulje **Raja**-sivu palataksesi **Ennakonpidätyksen komponentit** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="ce021-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="ce021-129">Valitse toimintoruudussa **Kopioi** avataksesi **Kopioi ennakonpidätyksen komponentit** -valintaikkunan, jotta voit kopioida TDS-komponentit, jotka on määritetty yhdelle TDS-komponenttiryhmälle, toiseen TDS-komponenttiryhmään.</span><span class="sxs-lookup"><span data-stu-id="ce021-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="ce021-130">Valitse **Alkaen**-kentästä TDS-komponenttiryhmä, josta TDS-komponentit kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="ce021-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="ce021-131">Valitse **Asti**-kentässä ennakonpidätyksen komponenttiryhmä, jonne TDS-komponentit kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="ce021-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce021-132">Yleisiä TDS-komponentteja, jotka on liitetty molempiin TDS-komponenttiryhmiin, ei kopioida.</span><span class="sxs-lookup"><span data-stu-id="ce021-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="ce021-133">Valitse **OK**, kun haluat kopioida ja luoda TDS-komponentit toiselle TDS-komponenttiryhmälle **Ennakonpidätyksen komponentit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ce021-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="ce021-134">[![Ennakonpidätyksen komponenttien kopioiminen -valintaikkuna](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="ce021-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="ce021-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ce021-135">Close the page.</span></span>
