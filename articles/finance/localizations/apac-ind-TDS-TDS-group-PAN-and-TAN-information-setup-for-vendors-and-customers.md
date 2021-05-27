---
title: Asiakkaiden ja toimittajien TDS-ryhmä-, PAN- ja TAN-tietojen määrittäminen
description: Tässä aiheessa kerrotaan, miten määritetään toimittajien ja asiakkaiden Vero vähennettynä lähteissä (TDS) -ryhmän tiedot, pysyvä tilinumero (PAN) ja verotilin numero (TAN).
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023209"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="7287c-103">Asiakkaiden ja toimittajien TDS-ryhmä-, PAN- ja TAN-tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7287c-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7287c-104">Tässä aiheessa kerrotaan, miten määritetään toimittajien ja asiakkaiden Vero vähennettynä lähteissä (TDS) -ryhmän tiedot, pysyvä tilinumero (PAN) ja verotilin numero (TAN).</span><span class="sxs-lookup"><span data-stu-id="7287c-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="7287c-105">Valitse **Ostoreskontra \> Toimittajat \> Kaikki toimittajat** tai **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="7287c-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="7287c-106">[![Kaikki toimittajat -sivu](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="7287c-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="7287c-107">Valitse toimintoruudusta **Uusi**, jos haluat luoda toimittajan tai asiakkaan, ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="7287c-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="7287c-108">Vaihtoehtoisesti voit valita aiemmin luodun toimittajan tai asiakkaan.</span><span class="sxs-lookup"><span data-stu-id="7287c-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="7287c-109">Määritä **Lasku ja toimitus** -pikavälilehden **Ennakonpidätys**-osassa **Laske ennakonpidätys** -asetuksen arvoksi **Kyllä**, kun haluat laskea toimittajan tai asiakkaan ennakonpidätyksen, TDS:n tai Lähteessä kerätyn veron (TCS).</span><span class="sxs-lookup"><span data-stu-id="7287c-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="7287c-110">Ostolaskun TDS-tiedot lasketaan toimittajalle tai asiakkaalle määritetyn TDS-oletusryhmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="7287c-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="7287c-111">Valitse **TDS-ryhmä**-kentässä oletusarvoinen TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="7287c-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7287c-112">Kun valitset TDS-ryhmän **TDS-ryhmä**-kentässä, **Ennakonpidätysryhmä**- ja **TCS-ryhmä**-kentät eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7287c-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="7287c-113">Valitse **Verotiedot**-pikavälilehden **PAN-tiedot**-osassa **Tila**-kentästä toimittajan tai asiakkaan pysyvä tilinumeron tila:</span><span class="sxs-lookup"><span data-stu-id="7287c-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="7287c-114">**Ei käytettävissä** – Toimittajalla tai asiakkaalla ei ole PAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="7287c-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="7287c-115">**Vastaanotettu** – Toimittajalla tai asiakkaalla on PAN-numero.</span><span class="sxs-lookup"><span data-stu-id="7287c-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="7287c-116">**Haettu** – Toimittaja tai asiakas on hakenut PAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="7287c-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="7287c-117">**Virheellinen** – Toimittajalla tai asiakkaalla on PAN-koodi, mutta se ei kelpaa.</span><span class="sxs-lookup"><span data-stu-id="7287c-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="7287c-118">Jos valitsit **Tila**-kentästä **Vastaanotettu**-kentässä ilmaistaksesi, että toimittajalla tai asiakkaalla on PAN-numero, kirjoita PAN **Numero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7287c-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="7287c-119">PAN-numerossa on oltava viisi aakkosmerkkiä, sitten neljä numeromerkkiä ja yksi aakkosmerkki.</span><span class="sxs-lookup"><span data-stu-id="7287c-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="7287c-120">Tässä on esimerkki: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="7287c-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="7287c-121">Jos valitsit **Tila**-kentästä **Haettu**-kentässä ilmaistaksesi, että toimittaja tai asiakas on hakenut PAN-numeroa, kirjoita viitenumero **Viitenumero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7287c-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="7287c-122">Valitse **Arvioitavan kohteen luonne** -kentässä arvioitavan kohteen luonteen luokka, johon toimittaja tai asiakas kuuluu:</span><span class="sxs-lookup"><span data-stu-id="7287c-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="7287c-123">Yhtiö</span><span class="sxs-lookup"><span data-stu-id="7287c-123">Company</span></span>
    - <span data-ttu-id="7287c-124">HUF</span><span class="sxs-lookup"><span data-stu-id="7287c-124">HUF</span></span>
    - <span data-ttu-id="7287c-125">Vahvista</span><span class="sxs-lookup"><span data-stu-id="7287c-125">Firm</span></span>
    - <span data-ttu-id="7287c-126">Henkilö</span><span class="sxs-lookup"><span data-stu-id="7287c-126">Individual</span></span>
    - <span data-ttu-id="7287c-127">AOP</span><span class="sxs-lookup"><span data-stu-id="7287c-127">AOP</span></span>
    - <span data-ttu-id="7287c-128">BOI</span><span class="sxs-lookup"><span data-stu-id="7287c-128">BOI</span></span>
    - <span data-ttu-id="7287c-129">Paikallinen viranomainen</span><span class="sxs-lookup"><span data-stu-id="7287c-129">Local authority</span></span>
    - <span data-ttu-id="7287c-130">Muut</span><span class="sxs-lookup"><span data-stu-id="7287c-130">Others</span></span>

    <span data-ttu-id="7287c-131">[![Verotiedot-pikavälilehti](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="7287c-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="7287c-132">Toimintoruudun **Toimittaja**-välilehdessä **Rekisteröinti**-ryhmässä valitse **Rekisteröintitunnukset** avataksesi **Osoitteiden hallinta** -sivun.</span><span class="sxs-lookup"><span data-stu-id="7287c-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="7287c-133">Valitse **Osoitteiden hallinta** -sivulla **Verotiedot**-pikavälilehdellä **Lisää** tai **Muokkaa** avataksesi **Verotietojen hallinta** -sivun, jossa voit ylläpitää verorekisteröintimerkintää.</span><span class="sxs-lookup"><span data-stu-id="7287c-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="7287c-134">**Verotietojen hallinta** -sivulla **Ennakonpidätys**-pikavälilehdessä **Verotilin numero (TAN)** -kentässä syötä TAN.</span><span class="sxs-lookup"><span data-stu-id="7287c-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="7287c-135">TAN-numerossa on oltava neljä aakkosmerkkiä, sitten viisi numeromerkkiä ja yksi aakkosmerkki.</span><span class="sxs-lookup"><span data-stu-id="7287c-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="7287c-136">Tässä on esimerkki: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="7287c-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="7287c-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7287c-137">Close the page.</span></span>
