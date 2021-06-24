---
title: Toimittajayhteistyön laskutustyötila
description: Tässä aiheessa kerrotaan, miten toimittajien laskuja voidaan tarkastella ja lähettää laskuja toimittajayhteistyön laskutustyötilasta.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3f4729a8a788f4f5b2b2e9923f515b86590b946
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188805"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="2d20e-103">Toimittajayhteistyön laskutustyötila</span><span class="sxs-lookup"><span data-stu-id="2d20e-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d20e-104">Tässä aiheessa kerrotaan, miten toimittajien laskuja voidaan tarkastella ja lähettää laskuja toimittajayhteistyön laskutustyötilasta.</span><span class="sxs-lookup"><span data-stu-id="2d20e-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="2d20e-105">**Toimittajayhteistyön laskutus** -työtilan avulla voit tarkastella toimittajien laskujen tietoja ja lähettää laskuja järjestelmään työnkulkutoimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="2d20e-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


## <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="2d20e-106">Toimittajayhteistyön laskutustyötila</span><span class="sxs-lookup"><span data-stu-id="2d20e-106">Vendor collaboration invoicing workspace</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="2d20e-107">Yhteenvetoruudut</span><span class="sxs-lookup"><span data-stu-id="2d20e-107">Summary tiles</span></span>

<span data-ttu-id="2d20e-108">**Yhteenveto**-ruuduissa näkyy yhteenveto valitun toimittajan laskuista.</span><span class="sxs-lookup"><span data-stu-id="2d20e-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="2d20e-109">Voit tarkastella laskuja tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="2d20e-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="2d20e-110">Luonnoslaskuja ei ole lähetetty työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="2d20e-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="2d20e-111">Lähetetty, ei hyväksytty -tilassa olevat laskut ovat laskuja, jotka on lähetetty toimittajalle, mutta niitä ei ole kirjattu sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="2d20e-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="2d20e-112">Hyväksytty, ei maksettu -tilassa olevat laskut ovat laskuja, jotka on kirjattu, mutta joita ei ole maksettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="2d20e-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="2d20e-113">Maksetut laskut on maksettu kokonaan sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2d20e-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="2d20e-114">Ruutua napsauttamalla avautuu suodatettu näkymä **laskujen luettelo** sivulle.</span><span class="sxs-lookup"><span data-stu-id="2d20e-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="2d20e-115">Taulukkoluettelot</span><span class="sxs-lookup"><span data-stu-id="2d20e-115">Tabular lists</span></span>

<span data-ttu-id="2d20e-116">**Taulukkoluettelot** kohdassa laskutuksen tila on eritelty samalla tavalla kuin yhteenvetoruuduissa: Luonnos- ja Lähetetty, ei hyväksytty -luetteloissa.</span><span class="sxs-lookup"><span data-stu-id="2d20e-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="2d20e-117">Luonnos-tilassa lasku voidaan lähettää työnkulkuun tai poistaa.</span><span class="sxs-lookup"><span data-stu-id="2d20e-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="2d20e-118">Viimeisessä taulukkoluettelossa voit etsiä laskut.</span><span class="sxs-lookup"><span data-stu-id="2d20e-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="2d20e-119">Suodattamalla saat nopeampia hakuja.</span><span class="sxs-lookup"><span data-stu-id="2d20e-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="2d20e-120">Kaikki toimittajan laskut -luettelosivu</span><span class="sxs-lookup"><span data-stu-id="2d20e-120">All vendor invoices list page</span></span>

<span data-ttu-id="2d20e-121">Voit tarkastella kaikkia kirjattuja ja kirjaamattomia toimittajalaskuja **Toimittajayhteistyön laskut** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="2d20e-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="2d20e-122">Voit tarkastella luettelosivulta laskujen maksun tilaa.</span><span class="sxs-lookup"><span data-stu-id="2d20e-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="2d20e-123">Maksun tilat ovat: kirjaamattomat, maksamatta, maksettu osittain, täysin maksettu.</span><span class="sxs-lookup"><span data-stu-id="2d20e-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="2d20e-124">Luo toimittajan lasku ostotilauksesta</span><span class="sxs-lookup"><span data-stu-id="2d20e-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="2d20e-125">Voit luoda uuden toimittajalaskun valitsemalla **uusi** toimenpiteen **Toimittajayhteistyön laskutus**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="2d20e-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="2d20e-126">Toimittajan on annettava ostotilauksen numero ja laskunumero.</span><span class="sxs-lookup"><span data-stu-id="2d20e-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="2d20e-127">Oletusarvon mukaan toimittajan ostotilauksen kaikkien rivien kirjauspäivä ilmestyy uuteen laskuun.</span><span class="sxs-lookup"><span data-stu-id="2d20e-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="2d20e-128">Määrä-ja kustannustietoja voidaan muokata ennen toimittajalaskun työnkulkuun lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="2d20e-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="2d20e-129">Voit liittää huomautuksia, tiedostoja, kuvia ja URL-osoitteet laskuun ennen sen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="2d20e-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="2d20e-130">Lisätietoja on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="2d20e-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]