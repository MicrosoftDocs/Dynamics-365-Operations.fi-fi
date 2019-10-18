---
title: Myymälän suorituskyvyn analysointi
description: Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Dynamics 365 Retailin tietojen perusteella.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2ea6ad2e3d9589face06cd5f950973209c17d41
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017779"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="90419-103">Myymälän tuoton analysointi</span><span class="sxs-lookup"><span data-stu-id="90419-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90419-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Dynamics 365 Retailin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="90419-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="90419-105">Osana Retailia käyttäjät voivat tarkastella myymälän suorituskykyä reaaliaikaisesti eri organisaatiohierarkian tasoilla valitun ajanjakson aikana avaamalla valmiin **Kanavayhteenveto**-raportin mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="90419-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="90419-106">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="90419-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="90419-107">**Vähittäismyymälän myyntitiedot** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän myyntitiedot** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="90419-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="90419-108">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Kanavan yhteenvetoraporttii**</span><span class="sxs-lookup"><span data-stu-id="90419-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="90419-109">Tämä raportti tarjoaa tilannevedoksen seuraaviin yhteenvetoihin osana myymälän suorituskykyä:</span><span class="sxs-lookup"><span data-stu-id="90419-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="90419-110">Bruttomyynnin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="90419-110">Gross sales summary</span></span>
- <span data-ttu-id="90419-111">Maksuvälinetyypin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="90419-111">Tender type summary</span></span>
- <span data-ttu-id="90419-112">Veron yhteenveto</span><span class="sxs-lookup"><span data-stu-id="90419-112">Tax summary</span></span>
- <span data-ttu-id="90419-113">Hinnan ohitusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="90419-113">Price overrides summary</span></span>
- <span data-ttu-id="90419-114">Alennusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="90419-114">Discounts summary</span></span>
