---
title: Käsittele kirjanpidon kohdistuskirjauskansio
description: Tässä ohjeaiheessa kerrotaan, miten kohdistuspyyntö käsitellään Dynamics 365 Finance -ohjelmassa.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7e8c3ef6fa85daec2a191b433b1ec4ece441ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968476"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="3ca16-103">Käsittele kirjanpidon kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="3ca16-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ca16-104">Tässä ohjeaiheessa kerrotaan, miten kohdistuspyyntö käsitellään.</span><span class="sxs-lookup"><span data-stu-id="3ca16-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="3ca16-105">Voit luoda Käsittele kohdistuspyyntö -sivulla kohdistuskirjauskansion, joka voidaan tarkistaa ja hyväksyä ennen kirjanpitoon kirjaamista tai kirjata kirjanpitoon suoraan.</span><span class="sxs-lookup"><span data-stu-id="3ca16-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="3ca16-106">Ennen kohdistuskirjauskansion luomista käytössä on oltava vähintään yksi aktiivinen kirjanpidon kohdistussääntö.</span><span class="sxs-lookup"><span data-stu-id="3ca16-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="3ca16-107">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="3ca16-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3ca16-108">Siirry siirtymisruudussa kohtaan **Moduulit > Kirjanpito > Kohdistukset > Käsittele kohdistuspyyntö**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="3ca16-109">Valitse **Sääntö**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="3ca16-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="3ca16-110">Lisää **Alkupäivämäärä** -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3ca16-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="3ca16-111">**Alkupäivämäärä** on erittäin tärkeä, kun kirjanpito on säännön tietolähde.</span><span class="sxs-lookup"><span data-stu-id="3ca16-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="3ca16-112">Tämä päivämäärä määrittää, mitkä kirjanpidon saldot sisällytetään kohdistukseen.</span><span class="sxs-lookup"><span data-stu-id="3ca16-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="3ca16-113">Valitse **Lähdearvo nolla** -kentässä **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="3ca16-114">Kohdistusprosessi pysäytetään ja näyttöön avautuu sanoma, jonka mukaan lähdesumma on nolla.</span><span class="sxs-lookup"><span data-stu-id="3ca16-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="3ca16-115">Valitse **Ehdotuksen asetukset** -kentässä **Vain ehdotus**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="3ca16-116">Valitsemalla **Vain ehdotus** voit tarkastella ja halutessasi hyväksyä tuloksen kohdistuskirjauskansioissa ennen kohdistuksen kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="3ca16-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="3ca16-117">Lisää päivämäärä Kirjanpidon kirjauspäivä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3ca16-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="3ca16-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-118">Select **OK**.</span></span>
7. <span data-ttu-id="3ca16-119">Siirry siirtymisruudussa kohtaan **Moduulit > Kirjanpito > Kohdistukset > Kohdistuskirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="3ca16-120">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-120">Select **Lines**.</span></span>
9. <span data-ttu-id="3ca16-121">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-121">Select **Post**.</span></span>
10. <span data-ttu-id="3ca16-122">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="3ca16-122">Select **Post**.</span></span>

