---
title: Resurssivikojen kustannusten hallinta
description: Tässä ohjeaiheessa kerrotaan resurssivikojen kustannushallinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918300"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="7ba90-103">Resurssivikojen kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="7ba90-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7ba90-104">Käyttöomaisuuden hallinnassa voit laskea käyttöomaisuuden vikamerkintöjen kustannukset, jolloin saat yleiskuvan todellisista kustannuksista verrattuna budjetin kustannuksiin vikojen osalta.</span><span class="sxs-lookup"><span data-stu-id="7ba90-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="7ba90-105">Todelliset kustannukset perustuvat kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="7ba90-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="7ba90-106">Päivämäärä on vikapäivämäärä, jolloin oire tallennettiin.</span><span class="sxs-lookup"><span data-stu-id="7ba90-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="7ba90-107">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen kustannusten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="7ba90-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="7ba90-108">Valitse **Resurssivikojen kustannusten hallinta** -valintaikkunassa laskennassa käytettävä taloushallinnon dimensioyhdistelmä, jos se on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="7ba90-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="7ba90-109">Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.</span><span class="sxs-lookup"><span data-stu-id="7ba90-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="7ba90-110">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="7ba90-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="7ba90-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin vikakustannusten valvontarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="7ba90-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="7ba90-112">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikojen kustannushallintarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="7ba90-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="7ba90-113">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät ja virheiden syyt **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7ba90-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="7ba90-114">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba90-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="7ba90-115">Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="7ba90-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7ba90-116">Valitut toimintoruudun painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="7ba90-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="7ba90-117">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="7ba90-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="7ba90-118">Alla olevassa kuvassa on esimerkki käyttöomaisuusvirheiden kustannustenhallinnan laskennasta.</span><span class="sxs-lookup"><span data-stu-id="7ba90-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![Kuva 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="7ba90-120">Lisätietoja vikojen määrittämisestä on [Vikojen hallinta](../setup-for-work-orders/fault-management.md) -osassa.</span><span class="sxs-lookup"><span data-stu-id="7ba90-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="7ba90-121">**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7ba90-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="7ba90-122">**Todelliset kustannukset** -kentässä näkyvät työtilausten kirjatut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7ba90-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="7ba90-123">**Sidottu kustannus** -kentässä näkyvät kokonaiskustannukset, joihin yritys on sitoutunut suhteessa työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="7ba90-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

