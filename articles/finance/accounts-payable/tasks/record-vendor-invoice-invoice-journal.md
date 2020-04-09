---
title: Toimittajan laskun tallentaminen laskukirjauskansioon
description: Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140372"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="f8f14-103">Toimittajan laskun tallentaminen laskukirjauskansioon</span><span class="sxs-lookup"><span data-stu-id="f8f14-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8f14-104">Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="f8f14-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="f8f14-105">Tällaisia laskuja ovat esimerkiksi tarvikkeiden tai palveluiden kulut.</span><span class="sxs-lookup"><span data-stu-id="f8f14-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="f8f14-106">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f8f14-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="f8f14-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Työtilat > Toimittajan laskun syöttö**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="f8f14-108">Napsauta **Toimintoruudussa** **Uusi laskukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="f8f14-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-109">Click **New**.</span></span>
4. <span data-ttu-id="f8f14-110">Avaa haku syöttämällä **Nimi**-kenttään kirjauskansion nimi tai valitsemalla avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f8f14-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="f8f14-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f8f14-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f8f14-112">Valitse **toimintoruudussa** **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="f8f14-113">Syötä **Päivämäärä**-kenttään kirjauspäivämäärä, joka päivittää kirjanpidon.</span><span class="sxs-lookup"><span data-stu-id="f8f14-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="f8f14-114">Määritä **Tili**-kenttään **Toimittajan tili**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="f8f14-115">Syötä **Lasku**-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="f8f14-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="f8f14-116">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f8f14-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="f8f14-117">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f8f14-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="f8f14-118">Avaa haku syöttämällä **Vastatili**-kenttään tilinumero nimi tai valitsemalla avattavan valikon painike</span><span class="sxs-lookup"><span data-stu-id="f8f14-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="f8f14-119">**Arvonlisäveroryhmän** oletusarvo saadaan toimittajan tililtä.</span><span class="sxs-lookup"><span data-stu-id="f8f14-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="f8f14-120">**Nimikkeen arvonlisäveroryhmän** oletusarvo saadaan **Vastatili**-kentässä määritetyltä päätililtä.</span><span class="sxs-lookup"><span data-stu-id="f8f14-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="f8f14-121">**Eräpäivä** lasketaan maksuehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f8f14-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="f8f14-122">**Käteisalennuksen** oletusarvo saadaan toimittajan tililtä.</span><span class="sxs-lookup"><span data-stu-id="f8f14-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="f8f14-123">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="f8f14-123">Click **Post**.</span></span>
13. <span data-ttu-id="f8f14-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8f14-124">Close the page.</span></span>

