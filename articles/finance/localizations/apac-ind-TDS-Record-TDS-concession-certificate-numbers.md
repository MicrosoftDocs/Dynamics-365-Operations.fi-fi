---
title: Tallenna TDS-huojennustodistuksen numerot
description: Tässä aiheessa kuvataan, miten toimittajille myönnetyt Vero vähennettynä lähteissä (TDS) -huojennustodistuksen numerot tallennetaan.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023196"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="b37db-103">Tallenna TDS-huojennustodistuksen numerot</span><span class="sxs-lookup"><span data-stu-id="b37db-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b37db-104">Tässä aiheessa kuvataan, miten toimittajille myönnetyt Vero vähennettynä lähteissä (TDS) -huojennustodistuksen numerot tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="b37db-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="b37db-105">Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyksen huojennukset**.</span><span class="sxs-lookup"><span data-stu-id="b37db-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="b37db-106">Valitse **Verotyyppi**-kentässä **TDS**, jos haluat tallentaa huojennustodistukset TDS-verotyypille.</span><span class="sxs-lookup"><span data-stu-id="b37db-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="b37db-107">Luo rivi valitsemalla **Yhteenveto**-välilehdessä **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="b37db-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="b37db-108">[![Uuden rivin otsikko](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="b37db-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="b37db-109">Valitse **Ennakonpidätyskoodi**-kentässä TDS-verokoodi, jota varten toimittajan huojennustodistukset on myönnetty.</span><span class="sxs-lookup"><span data-stu-id="b37db-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="b37db-110">**Ennakonpidätyskoodin nimi** -kentässä näkyy TDS-verokoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="b37db-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="b37db-111">Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin sen huojennustodistuksen voimassaolokausi, joka laskee toimittajan TDS:n huojennuksen perusteella TDS-verokoodin avulla.</span><span class="sxs-lookup"><span data-stu-id="b37db-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="b37db-112">Kirjoita **Huomautukset**-kenttään mahdolliset huomautukset.</span><span class="sxs-lookup"><span data-stu-id="b37db-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="b37db-113">Kirjoita **Osio**-kenttään lakisääteinen osakoodi, jonka alaisena TDS-toimiluvan sertifikaattia käytetään.</span><span class="sxs-lookup"><span data-stu-id="b37db-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="b37db-114">Jos osakoodi on 197, arvo "A" näkyy sekä lomakkeen 26Q sarakkeessa "Ei-vähennyksen syy / pienempi vähennys" sekä lomakkeen 27Q sarakkeessa "Ei-vähennyksen syy / pienempi vähennys / brutto ylös" (jos sellainen on).</span><span class="sxs-lookup"><span data-stu-id="b37db-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="b37db-115">Jos osion koodi on 197A, arvo "B" näkyy molemmissa paikoissa.</span><span class="sxs-lookup"><span data-stu-id="b37db-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="b37db-116">Valitse **Sertifikaatti**-pikavälilehti, kun haluat kirjata toimittajien TDS-huojennustodistusten numerot.</span><span class="sxs-lookup"><span data-stu-id="b37db-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="b37db-117">Valitse **Toimittajatili**-kentässä toimittajatili, jota varten TDS-huojennustodistus on myönnetty.</span><span class="sxs-lookup"><span data-stu-id="b37db-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="b37db-118">Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin TDS-huojennustodistuksen voimassaolokausi.</span><span class="sxs-lookup"><span data-stu-id="b37db-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="b37db-119">TDS:n laskeminen huojennuksen perusteella perustuu kauteen, jolloin toimittajalle luodaan todistus.</span><span class="sxs-lookup"><span data-stu-id="b37db-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="b37db-120">Kirjoita **Todistus**-kenttään TDS-huojennustodistuksen numero.</span><span class="sxs-lookup"><span data-stu-id="b37db-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="b37db-121">[![Sertifikaatti-pikavälilehti](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="b37db-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="b37db-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b37db-122">Close the page.</span></span>
