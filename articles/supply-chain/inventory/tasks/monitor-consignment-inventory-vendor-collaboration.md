--- 
title: "Tavaralähetysvaraston valvonta toimittajayhteistyön avulla"
description: "Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 8186b553e8518f3153bfd88b89121d4b0567501b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="e4d79-103">Tavaralähetysvaraston valvonta toimittajayhteistyön avulla</span><span class="sxs-lookup"><span data-stu-id="e4d79-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4d79-104">Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun.</span><span class="sxs-lookup"><span data-stu-id="e4d79-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="e4d79-105">Voit seurata varaston kulutusta, kun varaston omistajuuden siirtyy asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e4d79-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="e4d79-106">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e4d79-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="e4d79-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="e4d79-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="e4d79-108">Näytä käytetty varasto</span><span class="sxs-lookup"><span data-stu-id="e4d79-108">View consumed inventory</span></span>
1. <span data-ttu-id="e4d79-109">Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Tavaralähetysvarastosta vastaanotetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e4d79-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="e4d79-110">Luettelossa on tuotteen vastaanottorivit, jotka luotiin kun tavaranlähetysvaraston omistajuus muutettiin toimittajalta asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e4d79-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="e4d79-111">Joudut ehkä vierittämään näyttöä oikealle nähdäksesi määrät ja muut tiedot.</span><span class="sxs-lookup"><span data-stu-id="e4d79-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="e4d79-112">Voit käyttää luettelon tietoja laskujen luonnissa asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e4d79-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="e4d79-113">Voit myös viedä tiedot Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="e4d79-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="e4d79-114">Valitse Näytä ostotilausrivit.</span><span class="sxs-lookup"><span data-stu-id="e4d79-114">Click View purchase order.</span></span>
3. <span data-ttu-id="e4d79-115">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="e4d79-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="e4d79-116">Rivi on merkitty tavaralähetykseksi ja otsikko-osa näyttä, että ostotilauksen tila on Vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="e4d79-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="e4d79-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e4d79-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="e4d79-118">Näytetään käytettävissä oleva varasto</span><span class="sxs-lookup"><span data-stu-id="e4d79-118">View on-hand inventory</span></span>
1. <span data-ttu-id="e4d79-119">Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Käytettävissä oleva tavaralähetysvarasto.</span><span class="sxs-lookup"><span data-stu-id="e4d79-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="e4d79-120">Käytettävissä oleva tavaralähetysvarasto -sivulla näytetään asiakkaan varastossa omistamasi varasto.</span><span class="sxs-lookup"><span data-stu-id="e4d79-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="e4d79-121">Voit näyttää muita dimensioita, kuten toimipaikan ja varaston, valitsemalla Näytä dimensiot -välilehden.</span><span class="sxs-lookup"><span data-stu-id="e4d79-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   


