---
title: Määritä arvonlisäveron tilityskaudet
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäveron täsmäytyskaudet Dynamics 365 Financeissa.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658926"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="38a7c-103">Määritä arvonlisäveron tilityskaudet</span><span class="sxs-lookup"><span data-stu-id="38a7c-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38a7c-104">Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäveron täsmäytyskaudet.</span><span class="sxs-lookup"><span data-stu-id="38a7c-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="38a7c-105">Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava.</span><span class="sxs-lookup"><span data-stu-id="38a7c-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="38a7c-106">Tilitysprosessi voidaan suorittaa tietyn päivämäärävälin tilityskaudelle.</span><span class="sxs-lookup"><span data-stu-id="38a7c-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="38a7c-107">Kaikki tilityskauteen liittyvät verokoodit on tilitettävä.</span><span class="sxs-lookup"><span data-stu-id="38a7c-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="38a7c-108">Liittyvän arvonlisäveroviranomaisen määrityksestä riippuen verovelka kirjataan joko toimittajan tilille tai kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="38a7c-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="38a7c-109">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="38a7c-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="38a7c-110">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Arvonlisävero > Arvonlisäveron tilityskaudet**.</span><span class="sxs-lookup"><span data-stu-id="38a7c-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="38a7c-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="38a7c-111">Select **New**.</span></span>
3. <span data-ttu-id="38a7c-112">Kirjoita arvo **Tilityskausi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38a7c-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="38a7c-113">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="38a7c-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="38a7c-114">Valitse **Viranomainen**-kentästä arvonlisäveroviranomainen, joka vastaanottaa tilityskaudelle luodut raportit ja maksut.</span><span class="sxs-lookup"><span data-stu-id="38a7c-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="38a7c-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="38a7c-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="38a7c-116">Valitse **Maksuehdot**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="38a7c-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="38a7c-117">Liittyvä arvonlisäveroviranomainen voidaan määrittää toimittajaksi. Arvonlisäveron tilitys luo avoimen toimittajan laskun.</span><span class="sxs-lookup"><span data-stu-id="38a7c-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="38a7c-118">Maksuehdot määrittävät avoimen toimittajan laskun eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="38a7c-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="38a7c-119">Valitse tilityskauden välien tyyppi.</span><span class="sxs-lookup"><span data-stu-id="38a7c-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="38a7c-120">Syötä kausivälien yksiköiden määrä kautta kohti.</span><span class="sxs-lookup"><span data-stu-id="38a7c-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="38a7c-121">Esimerkiksi neljännesvuosi sisältää 3 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="38a7c-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="38a7c-122">Valitse **Käytä arvonlisäveron tilitykseen eräprosessia** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="38a7c-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="38a7c-123">Tilityskauden tilitysprosessi voidaan käsitellä taustalla erätyönä.</span><span class="sxs-lookup"><span data-stu-id="38a7c-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="38a7c-124">Tätä suositellaan, jos kausiväli sisältää paljon verotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="38a7c-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="38a7c-125">Tällä hetkellä tätä ei tueta Espanjassa, Japanissa tai Alankomaissa.</span><span class="sxs-lookup"><span data-stu-id="38a7c-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="38a7c-126">Valitse **Estä verotapahtumien vastakirjauksien luonti** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="38a7c-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="38a7c-127">Järjestelmä luo oletusarvoisesti verotapahtumien vastakirjauksia selvitysprosessin aikana, mikä voi heikentää suorituskykyä, jos kausiväliin sisältyy suuri määrä verotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="38a7c-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="38a7c-128">Estä verotapahtumien vastakirjauksien luonti valitsemalla tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="38a7c-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="38a7c-129">Laajenna **Kausivälit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="38a7c-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="38a7c-130">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="38a7c-130">Select **Add**.</span></span>
14. <span data-ttu-id="38a7c-131">Kirjoita päivämäärä uuden rivin **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38a7c-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="38a7c-132">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38a7c-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="38a7c-133">Valitse **Uusi kausiväli**.</span><span class="sxs-lookup"><span data-stu-id="38a7c-133">Select **New period interval**.</span></span> <span data-ttu-id="38a7c-134">Kun ensimmäinen kausiväli on syötetty, uudet kaudet voidaan luoda automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="38a7c-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="38a7c-135">Voit siirtyä takaisin ja lisätä tarvittaessa uusia kausivälejä.</span><span class="sxs-lookup"><span data-stu-id="38a7c-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="38a7c-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38a7c-136">Close the page.</span></span>

