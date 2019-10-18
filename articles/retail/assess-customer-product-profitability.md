---
title: Asiakkaiden ja tuotteiden tuottavuuden arviointi
description: Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Retail -tiedoista.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5a9bebf948bd4602556f70a5a79690621a03261e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023587"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="fa74a-103">Asiakkaiden ja tuotteiden kannattavuuden arviointi</span><span class="sxs-lookup"><span data-stu-id="fa74a-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa74a-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Retail -tiedoista.</span><span class="sxs-lookup"><span data-stu-id="fa74a-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="fa74a-105">Käyttäjät voivat tutkia Retailin osana myös parhaiden asiakkaiden (10–100) tuottavuutta eri organisaatiohierarkian tasoilla jonkin seuraavan ehdon perusteella:</span><span class="sxs-lookup"><span data-stu-id="fa74a-105">As part of Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="fa74a-106">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="fa74a-106">Sales amount</span></span>
- <span data-ttu-id="fa74a-107">Määrä</span><span class="sxs-lookup"><span data-stu-id="fa74a-107">Quantity</span></span>
- <span data-ttu-id="fa74a-108">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="fa74a-108">Gross profit margin</span></span>
- <span data-ttu-id="fa74a-109">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="fa74a-109">Margin percentage</span></span>

<span data-ttu-id="fa74a-110">Voit käyttää tässä arvioinnissa valmista **Parhaat asiakkaat** -raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="fa74a-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="fa74a-111">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="fa74a-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="fa74a-112">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="fa74a-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="fa74a-113">Samalla tavoin, käyttäjät voivat tutkia parhaiden tuotteiden (10 - 100) tuottavuutta eri organisaatiohierarkian tasoilla perustuen yhteen seuraavista kriteereistä:</span><span class="sxs-lookup"><span data-stu-id="fa74a-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="fa74a-114">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="fa74a-114">Sales amount</span></span>
- <span data-ttu-id="fa74a-115">Määrä</span><span class="sxs-lookup"><span data-stu-id="fa74a-115">Quantity</span></span>
- <span data-ttu-id="fa74a-116">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="fa74a-116">Gross profit margin</span></span>
- <span data-ttu-id="fa74a-117">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="fa74a-117">Margin percentage</span></span>

<span data-ttu-id="fa74a-118">Voit käyttää tässä arvioinnissa valmista **Parhaat tuotteet**-raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="fa74a-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="fa74a-119">**Vähittäismyymälän hallinta** -työtila &gt; **Retail** &gt; **Kanavat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportit** &gt; **Parhaat tuotteet -raportti**</span><span class="sxs-lookup"><span data-stu-id="fa74a-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="fa74a-120">**Luokka- ja tuotehallinta** -työtila &gt; **Retail** &gt; **Tuotteet ja luokat** &gt; **Vähittäismyymälän hallinta** &gt; **Raportti** &gt; **Parhaat tuotteet -raportti**</span><span class="sxs-lookup"><span data-stu-id="fa74a-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="fa74a-121">**Kyselyt ja raportit** -osio &gt; **Retail** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Parhaat tuotteet -raportti**</span><span class="sxs-lookup"><span data-stu-id="fa74a-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
