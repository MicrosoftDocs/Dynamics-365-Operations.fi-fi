---
title: "Myymälän suorituskyvyn analysointi"
description: "Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Microsoft Dynamics 365 for Retail -tietojen perusteella."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.contentlocale: fi-fi
ms.lasthandoff: 01/04/2019

---

# <a name="analyze-store-performance"></a><span data-ttu-id="82bdc-103">Myymälän suorituksen analysointi</span><span class="sxs-lookup"><span data-stu-id="82bdc-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82bdc-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä myymälän suorituskykyyn liittyviä tietoja Microsoft Dynamics 365 for Retail -tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="82bdc-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="82bdc-105">Osana Microsoft Dynamics 365 for Retailia käyttäjät voivat tarkastella myymälän suorituskykyä reaaliaikaisesti eri organisaatiohierarkian tasoilla valitun ajanjakson aikana avaamalla valmiin **Kanavayhteenveto**-raportin mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="82bdc-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="82bdc-106">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="82bdc-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="82bdc-107">**Vähittäismyymälän myyntitiedot** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän myyntitiedot** &gt; **Raportit** &gt; **Kanavan yhteenvetoraportti**</span><span class="sxs-lookup"><span data-stu-id="82bdc-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="82bdc-108">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Kanavan yhteenvetoraporttii**</span><span class="sxs-lookup"><span data-stu-id="82bdc-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="82bdc-109">Tämä raportti tarjoaa tilannevedoksen seuraaviin yhteenvetoihin osana myymälän suorituskykyä:</span><span class="sxs-lookup"><span data-stu-id="82bdc-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="82bdc-110">Bruttomyynnin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="82bdc-110">Gross sales summary</span></span>
- <span data-ttu-id="82bdc-111">Maksuvälinetyypin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="82bdc-111">Tender type summary</span></span>
- <span data-ttu-id="82bdc-112">Veron yhteenveto</span><span class="sxs-lookup"><span data-stu-id="82bdc-112">Tax summary</span></span>
- <span data-ttu-id="82bdc-113">Hinnan ohitusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="82bdc-113">Price overrides summary</span></span>
- <span data-ttu-id="82bdc-114">Alennusten yhteenveto</span><span class="sxs-lookup"><span data-stu-id="82bdc-114">Discounts summary</span></span>

