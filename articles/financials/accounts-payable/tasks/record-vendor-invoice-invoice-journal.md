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
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837009"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="eb15c-103">Toimittajan laskun tallentaminen laskukirjauskansioon</span><span class="sxs-lookup"><span data-stu-id="eb15c-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb15c-104">Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="eb15c-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="eb15c-105">Tällaisia laskuja ovat esimerkiksi tarvikkeiden tai palveluiden kulut.</span><span class="sxs-lookup"><span data-stu-id="eb15c-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="eb15c-106">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="eb15c-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="eb15c-107">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Työtilat > Toimittajan laskun syöttö**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="eb15c-108">Napsauta **Toimintoruudussa** **Uusi laskukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="eb15c-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-109">Click **New**.</span></span>
4. <span data-ttu-id="eb15c-110">Avaa haku syöttämällä **Nimi**-kenttään kirjauskansion nimi tai valitsemalla avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="eb15c-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="eb15c-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="eb15c-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="eb15c-112">Valitse **toimintoruudussa** **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="eb15c-113">Syötä **Päivämäärä**-kenttään kirjauspäivämäärä, joka päivittää kirjanpidon.</span><span class="sxs-lookup"><span data-stu-id="eb15c-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="eb15c-114">Määritä **Tili**-kenttään **Toimittajan tili**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="eb15c-115">Syötä **Lasku**-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="eb15c-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="eb15c-116">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="eb15c-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="eb15c-117">Syötä **Kredit**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="eb15c-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="eb15c-118">Avaa haku syöttämällä **Vastatili**-kenttään tilinumero nimi tai valitsemalla avattavan valikon painike</span><span class="sxs-lookup"><span data-stu-id="eb15c-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="eb15c-119">**Arvonlisäveroryhmän** oletusarvo saadaan toimittajan tililtä.</span><span class="sxs-lookup"><span data-stu-id="eb15c-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="eb15c-120">**Nimikkeen arvonlisäveroryhmän** oletusarvo saadaan **Vastatili**-kentässä määritetyltä päätililtä.</span><span class="sxs-lookup"><span data-stu-id="eb15c-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="eb15c-121">**Eräpäivä** lasketaan maksuehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="eb15c-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="eb15c-122">**Käteisalennuksen** oletusarvo saadaan toimittajan tililtä.</span><span class="sxs-lookup"><span data-stu-id="eb15c-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="eb15c-123">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="eb15c-123">Click **Post**.</span></span>
13. <span data-ttu-id="eb15c-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="eb15c-124">Close the page.</span></span>

