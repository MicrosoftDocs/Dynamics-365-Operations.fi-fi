---
title: Kirjanpidon oletuskuvaukset
description: Oletuskuvauksia voidaan käyttää tositteiden kirjausten Kuvaus-kentän päivittämiseksi kirjanpitoon.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500377"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="d87eb-103">Kirjanpidon oletuskuvaukset</span><span class="sxs-lookup"><span data-stu-id="d87eb-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d87eb-104">Oletuskuvauksia voidaan käyttää tositteiden kirjausten **Kuvaus**-kentän päivittämiseksi kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="d87eb-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="d87eb-105">Tätä ominaisuutta on parannettu toimimaan aiheutuneen kustannuksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="d87eb-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="d87eb-106">Voit määrittää oletuskuvauksia kirjanpidon kirjauksille valitsemalla **Organisaation hallinta \> Asetukset \> Oletuskuvaukset**.</span><span class="sxs-lookup"><span data-stu-id="d87eb-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="d87eb-107">Seuraavassa taulukossa luetellaan uudet arvot, jotka on lisätty **Oletuskuvaukset**-sivun **Kuvaus**-kentälle aiheutuneen kustannuksen tukemiseksi.</span><span class="sxs-lookup"><span data-stu-id="d87eb-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="d87eb-108">Kuvauksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="d87eb-108">Description type</span></span> | <span data-ttu-id="d87eb-109">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="d87eb-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="d87eb-110">Tuonnin kustannuslaskenta – Kustannusten jaksotus</span><span class="sxs-lookup"><span data-stu-id="d87eb-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="d87eb-111">Kun ostotilauslasku kirjataan, merikuljetuksen arvioiduille kustannuksille suoritetaan kustannusten jaksotus.</span><span class="sxs-lookup"><span data-stu-id="d87eb-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="d87eb-112">Voit määrittää oletuskuvauksia lisätäksesi merikuljetuksen numeron kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="d87eb-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="d87eb-113">Käytä lähetyksen numerona *%4*.</span><span class="sxs-lookup"><span data-stu-id="d87eb-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="d87eb-114">Tuonnin kustannuslaskenta – Matkalla olevien tavaroiden tilaus</span><span class="sxs-lookup"><span data-stu-id="d87eb-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="d87eb-115">Jos käytät kuljetettavien tuotteiden käsittelyä, ostotilauslasku kirjataan ja tavarat kirjataan kuljetustilin tavaroihin.</span><span class="sxs-lookup"><span data-stu-id="d87eb-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="d87eb-116">Voit määrittää oletuskuvauksia lisätäksesi kuljetettavien tuotteiden numeron kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="d87eb-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="d87eb-117">Käytä kuljetettavien tuotteiden tilausten numerona *%4*.</span><span class="sxs-lookup"><span data-stu-id="d87eb-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="d87eb-118">Varasto – Sulje – Oikaisu</span><span class="sxs-lookup"><span data-stu-id="d87eb-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="d87eb-119">Kun ostoreskontran lasku käsitellään merikuljetuksen kustannusta varten, merikuljetuksen kustannusten arvioimiseksi käsitellään varaston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="d87eb-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="d87eb-120">Voit määrittää oletuskuvauksia lisätäksesi merikuljetuksen numeron kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="d87eb-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="d87eb-121">Käytä lähetyksen numerona *%4*.</span><span class="sxs-lookup"><span data-stu-id="d87eb-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="d87eb-122">Lisätietoja **Oletuskuvaukset**-sivun käytöstä on kohdassa [Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="d87eb-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
