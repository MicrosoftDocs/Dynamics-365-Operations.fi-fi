---
title: Resurssivikojen kustannusten hallinta
description: Tässä ohjeaiheessa kerrotaan resurssivikojen kustannushallinnasta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 597e30db346e882a7002709be52ad1c2d0576099
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019943"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="97225-103">Resurssivikojen kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="97225-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="97225-104">Käyttöomaisuuden hallinnassa voit laskea käyttöomaisuuden vikamerkintöjen kustannukset, jolloin saat yleiskuvan todellisista kustannuksista verrattuna budjetin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="97225-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="97225-105">Todelliset kustannukset perustuvat kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="97225-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="97225-106">Päivämäärä on vikapäivämäärä, jolloin oire tallennettiin.</span><span class="sxs-lookup"><span data-stu-id="97225-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="97225-107">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen kustannusten hallinta**.</span><span class="sxs-lookup"><span data-stu-id="97225-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="97225-108">Valitse **Resurssivikojen kustannusten hallinta** -valintaikkunassa laskennassa käytettävä taloushallinnon dimensioyhdistelmä, jos se on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="97225-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="97225-109">Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.</span><span class="sxs-lookup"><span data-stu-id="97225-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="97225-110">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="97225-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="97225-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin vikakustannusten valvontarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="97225-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="97225-112">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikojen kustannushallintarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="97225-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="97225-113">Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät ja virheiden syyt **Sisällytettävät tietueet** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="97225-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="97225-114">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="97225-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="97225-115">Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="97225-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="97225-116">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="97225-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="97225-117">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="97225-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="97225-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="97225-118">Example</span></span>

<span data-ttu-id="97225-119">Tässä esimerkissä esitetään resurssivikojen kustannushallinnan laskutoimituksista.</span><span class="sxs-lookup"><span data-stu-id="97225-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="97225-120">**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="97225-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="97225-121">**Todelliset kustannukset** -kentässä näkyvät työtilausten kirjatut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="97225-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="97225-122">**Sidottu kustannus** -kentässä näkyvät kokonaiskustannukset, joihin yritys on sitoutunut suhteessa työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="97225-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Kuva 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="97225-124">Lisätietoja vikojen määrittämisestä esitetään aiheessa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="97225-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
