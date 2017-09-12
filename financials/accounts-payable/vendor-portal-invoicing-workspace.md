---
title: "Toimittajayhteistyön laskutustyötila"
description: "Tässä aiheessa kerrotaan, miten toimittajien laskuja voidaan tarkastella ja lähettää laskuja toimittajayhteistyön laskutustyötilasta."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f9b8cc1ee7f8c8bed79bac3ca6a6856d9101aad
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="044ef-103">Toimittajayhteistyön laskutustyötila</span><span class="sxs-lookup"><span data-stu-id="044ef-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="044ef-104">Tässä aiheessa kerrotaan, miten toimittajien laskuja voidaan tarkastella ja lähettää laskuja toimittajayhteistyön laskutustyötilasta.</span><span class="sxs-lookup"><span data-stu-id="044ef-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="044ef-105">**Toimittajayhteistyön laskutus**-työtilan avulla voit tarkastella toimittajan laskun tietoja ja lähettää laskuja Microsoft Dynamics 365 for Finance and Operations Enterprise edition -järjestelmään ominaisuuksia työnkulkutoimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="044ef-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="044ef-106">Toimittajayhteistyön laskutustyötila</span><span class="sxs-lookup"><span data-stu-id="044ef-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="044ef-107">Yhteenvetoruudut</span><span class="sxs-lookup"><span data-stu-id="044ef-107">Summary tiles</span></span>

<span data-ttu-id="044ef-108">**Yhteenveto**-ruuduissa näkyy yhteenveto valitun toimittajan laskuista.</span><span class="sxs-lookup"><span data-stu-id="044ef-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="044ef-109">Voit tarkastella laskuja tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="044ef-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="044ef-110">Luonnoslaskuja ei ole lähetetty työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="044ef-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="044ef-111">Lähetetty, ei hyväksytty -tilassa olevat laskut ovat laskuja, jotka on lähetetty toimittajalle, mutta niitä ei ole kirjattu Dynamics 365 for Finance and Operations -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="044ef-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="044ef-112">Hyväksytty, ei maksettu -tilassa olevat laskut ovat laskuja, jotka on kirjattu Finance and Operations -järjestelmään mutta niitä ei ole maksettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="044ef-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="044ef-113">Maksetut laskut on maksettu kokonaan Finance and Operations -järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="044ef-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="044ef-114">Ruutua napsauttamalla avautuu suodatettu näkymä **laskujen luettelo** sivulle.</span><span class="sxs-lookup"><span data-stu-id="044ef-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="044ef-115">Taulukkoluettelot</span><span class="sxs-lookup"><span data-stu-id="044ef-115">Tabular lists</span></span>

<span data-ttu-id="044ef-116">**Taulukkoluettelot** kohdassa laskutuksen tila on eritelty samalla tavalla kuin yhteenvetoruuduissa: Luonnos- ja Lähetetty, ei hyväksytty -luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="044ef-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="044ef-117">Luonnos-tilassa lasku voidaan lähettää työnkulkuun tai poistaa.</span><span class="sxs-lookup"><span data-stu-id="044ef-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="044ef-118">Viimeisessä taulukkoluettelossa voit etsiä laskut.</span><span class="sxs-lookup"><span data-stu-id="044ef-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="044ef-119">Suodattamalla saat nopeampia hakuja.</span><span class="sxs-lookup"><span data-stu-id="044ef-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="044ef-120">Kaikki toimittajan laskut -luettelosivu</span><span class="sxs-lookup"><span data-stu-id="044ef-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="044ef-121">Voit tarkastella kaikkia kirjattuja ja kirjaamattomia toimittajalaskuja **Toimittajayhteistyön laskut** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="044ef-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="044ef-122">Voit tarkastella luettelosivulta laskujen maksun tilaa.</span><span class="sxs-lookup"><span data-stu-id="044ef-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="044ef-123">Maksun tilat ovat: kirjaamattomat, maksamatta, maksettu osittain, täysin maksettu.</span><span class="sxs-lookup"><span data-stu-id="044ef-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="044ef-124">Luo toimittajan lasku ostotilauksesta</span><span class="sxs-lookup"><span data-stu-id="044ef-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="044ef-125">Voit luoda uuden toimittajalaskun valitsemalla **uusi** toimenpiteen **Toimittajayhteistyön laskutus**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="044ef-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="044ef-126">Toimittajan on annettava ostotilauksen numero ja laskunumero.</span><span class="sxs-lookup"><span data-stu-id="044ef-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="044ef-127">Oletusarvon mukaan toimittajan ostotilauksen kaikkien rivien kirjauspäivä ilmestyy uuteen laskuun.</span><span class="sxs-lookup"><span data-stu-id="044ef-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="044ef-128">Määrä-ja kustannustietoja voidaan muokata ennen toimittajalaskun työnkulkuun lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="044ef-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="044ef-129">Voit liittää huomautuksia, tiedostoja, kuvia ja URL-osoitteet laskuun ennen sen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="044ef-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="044ef-130">Lisätietoja on ohjeaiheessa [Yhteistyö toimittajien kanssa Toimittajaportaalissa](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span><span class="sxs-lookup"><span data-stu-id="044ef-130">For more information, see [Collaborating with vendors by using the Vendor portal](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span></span>




