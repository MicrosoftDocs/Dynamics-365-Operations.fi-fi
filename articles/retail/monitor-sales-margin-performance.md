---
title: Myynti- ja marginaalisuoritusten valvonta
description: Dynamics 365 Retailissa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018061"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="d2889-103">Myynnin ja katteen kehittymisen seuranta</span><span class="sxs-lookup"><span data-stu-id="d2889-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2889-104">Dynamics 365 Retailissa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="d2889-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="d2889-105">Retailissa käyttäjät voivat valvoa myynnin ja katetuoton kehittymistä reaaliaikaisesti organisaatiohierarkian eri tasoilla seuraavissa dimensioissa:</span><span class="sxs-lookup"><span data-stu-id="d2889-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="d2889-106">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="d2889-106">Products</span></span>
- <span data-ttu-id="d2889-107">Luokat</span><span class="sxs-lookup"><span data-stu-id="d2889-107">Categories</span></span>
- <span data-ttu-id="d2889-108">Alennukset</span><span class="sxs-lookup"><span data-stu-id="d2889-108">Discounts</span></span>
- <span data-ttu-id="d2889-109">Vuodet aikajaksona</span><span class="sxs-lookup"><span data-stu-id="d2889-109">Years as time period</span></span>
- <span data-ttu-id="d2889-110">Rekisterit/päätteet</span><span class="sxs-lookup"><span data-stu-id="d2889-110">Registers/terminals</span></span>
- <span data-ttu-id="d2889-111">Henkilökunta/työntekijät</span><span class="sxs-lookup"><span data-stu-id="d2889-111">Staff/employees</span></span>
- <span data-ttu-id="d2889-112">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="d2889-112">Customers</span></span>
- <span data-ttu-id="d2889-113">Käyttöyksiköt</span><span class="sxs-lookup"><span data-stu-id="d2889-113">Operating units</span></span>

<span data-ttu-id="d2889-114">Kahden hierarkkista ruudukkorakennetta hyödyntävän yksilöllisen raportin avulla käyttäjät voivat lisäksi valvoa myynnin ja katetuoton kehittymistä porautumalla päätason luokan solmusta luokan yksittäisiin lehtisolmuihin vähittäismyynnin oletusarvoisessa tuoteluokkahierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="d2889-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="d2889-115">Käyttäjät voivat myös porautua päätason toimintayksiköstä yksittäiseen kanavaan organisaatiohierarkiassa, joka on määritetty oletusorganisaatiohierarkiaksi vähittäismyynnin raportointihierarkiaa varten.</span><span class="sxs-lookup"><span data-stu-id="d2889-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="d2889-116">Raportit voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="d2889-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="d2889-117">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="d2889-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d2889-118">**Luokka- ja tuotehallinta** -työtila &gt; **Retail** &gt; **Tuotteet ja luokat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportti**</span><span class="sxs-lookup"><span data-stu-id="d2889-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d2889-119">**Hinnoittelun ja alennusten hallinta** -työtila &gt; **Retail** &gt; **Hinnoittelu ja alennukset** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="d2889-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d2889-120">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit**</span><span class="sxs-lookup"><span data-stu-id="d2889-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
