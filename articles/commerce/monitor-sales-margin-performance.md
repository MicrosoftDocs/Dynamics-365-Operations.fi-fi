---
title: Myynti- ja marginaalisuoritusten valvonta
description: Dynamics 365 Commercessa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7ea2bd9388e2fcfc6ae5f17d61054092cbac58c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796943"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="66231-103">Myynnin ja katteen kehittymisen seuranta</span><span class="sxs-lookup"><span data-stu-id="66231-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66231-104">Dynamics 365 Commercessa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="66231-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="66231-105">Kaupassa käyttäjät voivat valvoa myynnin ja katetuoton kehittymistä reaaliaikaisesti organisaatiohierarkian eri tasoilla seuraavissa dimensioissa:</span><span class="sxs-lookup"><span data-stu-id="66231-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="66231-106">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="66231-106">Products</span></span>
- <span data-ttu-id="66231-107">Luokat</span><span class="sxs-lookup"><span data-stu-id="66231-107">Categories</span></span>
- <span data-ttu-id="66231-108">Alennukset</span><span class="sxs-lookup"><span data-stu-id="66231-108">Discounts</span></span>
- <span data-ttu-id="66231-109">Vuodet aikajaksona</span><span class="sxs-lookup"><span data-stu-id="66231-109">Years as time period</span></span>
- <span data-ttu-id="66231-110">Rekisterit/päätteet</span><span class="sxs-lookup"><span data-stu-id="66231-110">Registers/terminals</span></span>
- <span data-ttu-id="66231-111">Henkilökunta/työntekijät</span><span class="sxs-lookup"><span data-stu-id="66231-111">Staff/employees</span></span>
- <span data-ttu-id="66231-112">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="66231-112">Customers</span></span>
- <span data-ttu-id="66231-113">Käyttöyksiköt</span><span class="sxs-lookup"><span data-stu-id="66231-113">Operating units</span></span>

<span data-ttu-id="66231-114">Kahden hierarkkista ruudukkorakennetta hyödyntävän yksilöllisen raportin avulla käyttäjät voivat lisäksi valvoa myynnin ja katetuoton kehittymistä porautumalla päätason luokan solmusta luokan yksittäisiin lehtisolmuihin oletusarvoisessa tuoteluokkahierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="66231-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="66231-115">Käyttäjät voivat myös porautua päätason toimintayksiköstä yksittäiseen kanavaan organisaatiohierarkiassa, joka on määritetty oletusorganisaatiohierarkiaksi raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="66231-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="66231-116">Raportit voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="66231-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="66231-117">**Myymälän hallinta** -työtila &gt; **Vähittäismyynti ja kauppa** &gt; **Kanavat** &gt; **Myymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="66231-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66231-118">**Luokka- ja tuotehallinta** -työtila &gt; **Vähittäismyynti ja kauppa** &gt; **Tuotteet ja luokat** &gt; **Myymälän hallinta** &gt; **Raportti**</span><span class="sxs-lookup"><span data-stu-id="66231-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66231-119">**Hinnoittelun ja alennusten hallinta** -työtila &gt; **Vähittäismyynti ja kauppa** &gt; **Hinnoittelu ja alennukset** &gt; **Myymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="66231-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="66231-120">**Kyselyt ja raportit** -osio &gt; **Vähittäismyynti ja kauppa** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit**</span><span class="sxs-lookup"><span data-stu-id="66231-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]