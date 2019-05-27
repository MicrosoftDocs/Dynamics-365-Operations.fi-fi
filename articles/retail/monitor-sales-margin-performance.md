---
title: Myynti- ja marginaalisuoritusten valvonta
description: Microsoft Dynamics 365 for Retailissa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.
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
ms.openlocfilehash: e2b3591f6403542c79457d12ae850ad40d9253a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555647"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="8f8c2-103">Myynnin ja katteen kehittymisen seuranta</span><span class="sxs-lookup"><span data-stu-id="8f8c2-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f8c2-104">Microsoft Dynamics 365 for Retailissa voi valvoa myynnin ja katetuoton kehitystä reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="8f8c2-104">You can monitor sales and margin performance in real time using Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="8f8c2-105">Dynamics 365 for Retailissa käyttäjät voivat valvoa myynnin ja katetuoton kehittymistä reaaliaikaisesti organisaatiohierarkian eri tasoilla seuraavissa dimensioissa:</span><span class="sxs-lookup"><span data-stu-id="8f8c2-105">As part of Dynamics 365 for Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="8f8c2-106">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="8f8c2-106">Products</span></span>
- <span data-ttu-id="8f8c2-107">Luokat</span><span class="sxs-lookup"><span data-stu-id="8f8c2-107">Categories</span></span>
- <span data-ttu-id="8f8c2-108">Alennukset</span><span class="sxs-lookup"><span data-stu-id="8f8c2-108">Discounts</span></span>
- <span data-ttu-id="8f8c2-109">Vuodet aikajaksona</span><span class="sxs-lookup"><span data-stu-id="8f8c2-109">Years as time period</span></span>
- <span data-ttu-id="8f8c2-110">Rekisterit/päätteet</span><span class="sxs-lookup"><span data-stu-id="8f8c2-110">Registers/terminals</span></span>
- <span data-ttu-id="8f8c2-111">Henkilökunta/työntekijät</span><span class="sxs-lookup"><span data-stu-id="8f8c2-111">Staff/employees</span></span>
- <span data-ttu-id="8f8c2-112">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="8f8c2-112">Customers</span></span>
- <span data-ttu-id="8f8c2-113">Käyttöyksiköt</span><span class="sxs-lookup"><span data-stu-id="8f8c2-113">Operating units</span></span>

<span data-ttu-id="8f8c2-114">Kahden hierarkkista ruudukkorakennetta hyödyntävän yksilöllisen raportin avulla käyttäjät voivat lisäksi valvoa myynnin ja katetuoton kehittymistä porautumalla päätason luokan solmusta luokan yksittäisiin lehtisolmuihin vähittäismyynnin oletusarvoisessa tuoteluokkahierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="8f8c2-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="8f8c2-115">Käyttäjät voivat myös porautua päätason toimintayksiköstä yksittäiseen kanavaan organisaatiohierarkiassa, joka on määritetty oletusorganisaatiohierarkiaksi vähittäismyynnin raportointihierarkiaa varten.</span><span class="sxs-lookup"><span data-stu-id="8f8c2-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="8f8c2-116">Raportit voi avata seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="8f8c2-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="8f8c2-117">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="8f8c2-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8f8c2-118">**Luokka- ja tuotehallinta** -työtila &gt; **Retail** &gt; **Tuotteet ja luokat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportti**</span><span class="sxs-lookup"><span data-stu-id="8f8c2-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8f8c2-119">**Hinnoittelun ja alennusten hallinta** -työtila &gt; **Retail** &gt; **Hinnoittelu ja alennukset** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit**</span><span class="sxs-lookup"><span data-stu-id="8f8c2-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8f8c2-120">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit**</span><span class="sxs-lookup"><span data-stu-id="8f8c2-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
