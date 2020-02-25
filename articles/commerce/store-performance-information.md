---
title: Myymälän suorituskyvyn analysointi
description: Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Dynamics 365 Commercein tietojen perusteella.
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
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022400"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="d49a1-103">Myymälän tuoton analysointi</span><span class="sxs-lookup"><span data-stu-id="d49a1-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d49a1-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Dynamics 365 Commercein tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d49a1-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="d49a1-105">Osana Retailia käyttäjät voivat tarkastella myymälän suorituskykyä reaaliaikaisesti eri organisaatiohierarkian tasoilla valitun ajanjakson aikana avaamalla valmiin **Kanavayhteenveto**-raportin mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="d49a1-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="d49a1-106">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="d49a1-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d49a1-107">**Vähittäismyymälän myyntitiedot** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän myyntitiedot** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="d49a1-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d49a1-108">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Kanavan yhteenvetoraporttii**</span><span class="sxs-lookup"><span data-stu-id="d49a1-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="d49a1-109">Tämä raportti tarjoaa tilannevedoksen seuraaviin yhteenvetoihin osana myymälän suorituskykyä:</span><span class="sxs-lookup"><span data-stu-id="d49a1-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="d49a1-110">Bruttomyynnin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="d49a1-110">Gross sales summary</span></span>
- <span data-ttu-id="d49a1-111">Maksuvälinetyypin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="d49a1-111">Tender type summary</span></span>
- <span data-ttu-id="d49a1-112">Veron yhteenveto</span><span class="sxs-lookup"><span data-stu-id="d49a1-112">Tax summary</span></span>
- <span data-ttu-id="d49a1-113">Hinnan ohitusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="d49a1-113">Price overrides summary</span></span>
- <span data-ttu-id="d49a1-114">Alennusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="d49a1-114">Discounts summary</span></span>
