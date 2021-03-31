---
title: Lähtevien varaston työvaiheiden vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun lähteviä varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1344a1c16bf72b31f7aaf18aaeb6e08c7bc9d87e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223263"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="16de9-103">Lähtevien varaston työvaiheiden vianmääritys</span><span class="sxs-lookup"><span data-stu-id="16de9-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16de9-104">Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun lähteviä varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="16de9-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="16de9-105">Seuraava virhesanoma avautuu: Myyntitilausta ei voitu vapauttaa.</span><span class="sxs-lookup"><span data-stu-id="16de9-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="16de9-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="16de9-106">Issue description</span></span>

<span data-ttu-id="16de9-107">Tämä ongelman esiintymiseen voi olla useita syitä.</span><span class="sxs-lookup"><span data-stu-id="16de9-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="16de9-108">Tilaus on esimerkiksi luotonhallinnan pidossa eikä lähetyksiä voi luoda, ennen kuin kaikille myyntitilaukseen liitetyille myyntiriveille on annettu kelvollinen postiosoite.</span><span class="sxs-lookup"><span data-stu-id="16de9-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="16de9-109">Vaihtoehtoisesti kyse voi olla tilauksen pidosta, joka on käsiteltävä, ennen kuin tilaus voidaan vapauttaa varastoon.</span><span class="sxs-lookup"><span data-stu-id="16de9-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="16de9-110">Kyseinen pito voi olla tilauskohtainen ja se voi olla asiakastilissä.</span><span class="sxs-lookup"><span data-stu-id="16de9-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="16de9-111">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="16de9-111">Issue resolution</span></span>

<span data-ttu-id="16de9-112">Lisää tai päivitä myyntitilauksen tai myyntitilausten osoite ja vapauta tilaus sitten varastoon.</span><span class="sxs-lookup"><span data-stu-id="16de9-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="16de9-113">Tilaukset voidaan vapauttaa varastoon vain, jos niissä on kelvollinen toimitusosoite (**Organisaation hallinto** -moduulissa määritetyn osoitemuodon mukaisesti).</span><span class="sxs-lookup"><span data-stu-id="16de9-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="16de9-114">Selvitä tilauksen pito ja käsittele ongelmat.</span><span class="sxs-lookup"><span data-stu-id="16de9-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="16de9-115">Poista sitten pito tilauksesta tai asiakkaasta ja vapauta tilaus varastoon.</span><span class="sxs-lookup"><span data-stu-id="16de9-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="16de9-116">Seuraava sanoma avautuu: Kuorman 1% lähetys on vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="16de9-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="16de9-117">Mitään rivejä ei kuitenkaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="16de9-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="16de9-118">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="16de9-118">Issue description</span></span>

<span data-ttu-id="16de9-119">Kuorman lähetys on vahvistettu mutta lisäkirjauksia ei tehdä.</span><span class="sxs-lookup"><span data-stu-id="16de9-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="16de9-120">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="16de9-120">Issue resolution</span></span>

<span data-ttu-id="16de9-121">Lähetyksen vahvistus ei vaikuta kirjaukseen.</span><span class="sxs-lookup"><span data-stu-id="16de9-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="16de9-122">Se vain päivittää lähetyksen ja kuorman tilan.</span><span class="sxs-lookup"><span data-stu-id="16de9-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="16de9-123">Kirjaus on tehtävä erillisessä prosessissa.</span><span class="sxs-lookup"><span data-stu-id="16de9-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="16de9-124">Seuraava virhesanoma avautuu: Suoratoimitus ei voi käsitellä varastoa 1%, koska varastonhallinta on otettu siinä käyttöön.</span><span class="sxs-lookup"><span data-stu-id="16de9-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="16de9-125">Määritä toinen varasto, jossa varastonhallintaa ei ole otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="16de9-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="16de9-126">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="16de9-126">Issue description</span></span>

<span data-ttu-id="16de9-127">Nimike lisätään suoratoimituksen myyntiriville varastosta, jossa varastonhallinta on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="16de9-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="16de9-128">Tämä virhesanoma avautuu, kun myyntirivi on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="16de9-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="16de9-129">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="16de9-129">Issue resolution</span></span>

<span data-ttu-id="16de9-130">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="16de9-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="16de9-131">Varastonhallinta ei tue tällä hetkellä suoratoimitusta.</span><span class="sxs-lookup"><span data-stu-id="16de9-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="16de9-132">Suoratoimituksen käyttämistä varten on sen vuoksi valittava muu kuin varastonhallintanimike ja varasto.</span><span class="sxs-lookup"><span data-stu-id="16de9-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]