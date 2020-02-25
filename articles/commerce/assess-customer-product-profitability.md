---
title: Asiakkaiden ja tuotteiden tuottavuuden arviointi
description: Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Commerce -tiedoista.
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022342"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="bd784-103">Asiakkaiden ja tuotteiden kannattavuuden arviointi</span><span class="sxs-lookup"><span data-stu-id="bd784-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd784-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Commerce -tiedoista.</span><span class="sxs-lookup"><span data-stu-id="bd784-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="bd784-105">Käyttäjät voivat tutkia Commercen osana myös parhaiden asiakkaiden (10–100) tuottavuutta eri organisaatiohierarkian tasoilla jonkin seuraavan ehdon perusteella:</span><span class="sxs-lookup"><span data-stu-id="bd784-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="bd784-106">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="bd784-106">Sales amount</span></span>
- <span data-ttu-id="bd784-107">Määrä</span><span class="sxs-lookup"><span data-stu-id="bd784-107">Quantity</span></span>
- <span data-ttu-id="bd784-108">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="bd784-108">Gross profit margin</span></span>
- <span data-ttu-id="bd784-109">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="bd784-109">Margin percentage</span></span>

<span data-ttu-id="bd784-110">Voit käyttää tässä arvioinnissa valmista **Parhaat asiakkaat** -raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="bd784-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="bd784-111">**Myymälän hallinta** -työtila &gt; **Retail ja Commerce** &gt; **Kanavat** &gt; **Myymälän hallinta** &gt; **Raportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="bd784-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="bd784-112">**Kyselyt ja raportit** -osio &gt; **Retail ja Commerce** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="bd784-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="bd784-113">Samalla tavoin, käyttäjät voivat tutkia parhaiden tuotteiden (10 - 100) tuottavuutta eri organisaatiohierarkian tasoilla perustuen yhteen seuraavista kriteereistä:</span><span class="sxs-lookup"><span data-stu-id="bd784-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="bd784-114">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="bd784-114">Sales amount</span></span>
- <span data-ttu-id="bd784-115">Määrä</span><span class="sxs-lookup"><span data-stu-id="bd784-115">Quantity</span></span>
- <span data-ttu-id="bd784-116">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="bd784-116">Gross profit margin</span></span>
- <span data-ttu-id="bd784-117">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="bd784-117">Margin percentage</span></span>

<span data-ttu-id="bd784-118">Voit käyttää tässä arvioinnissa valmista **Parhaat tuotteet**-raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="bd784-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="bd784-119">**Myymälän hallinta** -työtila &gt; **Retail ja Commerce** &gt; **Kanavat** &gt; **Myymälän hallinta** &gt; **Raportit** &gt; **Suurimpien tuotteiden raportti**</span><span class="sxs-lookup"><span data-stu-id="bd784-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="bd784-120">**Luokka- ja tuotehallinta** -työtila &gt; **Retail ja Commerce** &gt; **Tuotteet ja luokat** &gt; **Myymälän hallinta** &gt; **Raportti** &gt; **Parhaat tuotteet -raportti**</span><span class="sxs-lookup"><span data-stu-id="bd784-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="bd784-121">**Kyselyt ja raportit** -osio &gt; **Retail ja Commerce** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Suurimpien tuotteiden raportti**</span><span class="sxs-lookup"><span data-stu-id="bd784-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
