---
title: Myyntitrendien ja -mallien analysointi
description: Dynamics 365 Retailissa voi tarkastella myyntitrendejä ja -malleja reaaliaikaisesti.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c54e707d312d7ac3bbcad71a914e528859038a13
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025814"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="184c3-103">Myyntitrendien ja -mallien analysointi</span><span class="sxs-lookup"><span data-stu-id="184c3-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="184c3-104">Dynamics 365 Retailissa voi tarkastella myyntitrendejä ja -malleja reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="184c3-104">You can study sales trends and patterns in real time in Dynamics 365 Retail.</span></span>

<span data-ttu-id="184c3-105">Retailissa käyttäjät voivat tarkastella myyntitrendejä ja -malleja reaaliaikaisesti organisaatiohierarkian eri tasoilla valitun ajanjakson aikana avaamalla valmiin **Vuosikohtaisen kanavamyynnin** -raportin.</span><span class="sxs-lookup"><span data-stu-id="184c3-105">As part of Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="184c3-106">Tämän raportin voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="184c3-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="184c3-107">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Vuosikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="184c3-108">**Vähittäismyymälän myyntitiedot** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän myyntitiedot** &gt; **Raportit** &gt; **Vuosikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="184c3-109">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Vuosikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="184c3-110">Käyttäjät voivat tarkastella myyntitrendejä ja -malleja myös tuntiperusteisesti organisaatiohierarkian eri tasoilla valitun ajanjakson aikana avaamalla valmiin **tuntikohtaisen kanavamyynnin raportin**.</span><span class="sxs-lookup"><span data-stu-id="184c3-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="184c3-111">Tämän raportin voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="184c3-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="184c3-112">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Tuntikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="184c3-113">**Vähittäismyymälän myyntitiedot** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän myyntitiedot** &gt; **Raportit** &gt; **Tuntikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="184c3-114">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Tuntikohtaisen kanavamyynnin raportti**</span><span class="sxs-lookup"><span data-stu-id="184c3-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
