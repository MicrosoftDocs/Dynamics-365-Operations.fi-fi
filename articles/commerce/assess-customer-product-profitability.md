---
title: Asiakkaiden ja tuotteiden tuottavuuden arviointi
description: Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Commerce -tiedoista.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797326"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="ce0bf-103">Asiakkaiden ja tuotteiden kannattavuuden arviointi</span><span class="sxs-lookup"><span data-stu-id="ce0bf-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce0bf-104">Tässä artikkelissa kerrotaan, miten voit muistiin sisältyvän ja reaaliaikaisen analytiikan avulla käsitellä ja kerätä asiakkaisiin sekä tuotteiden kannattavuuteen liittyviä tietoja Dynamics 365 Commerce -tiedoista.</span><span class="sxs-lookup"><span data-stu-id="ce0bf-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="ce0bf-105">Käyttäjät voivat tutkia Commercen osana myös parhaiden asiakkaiden (10–100) tuottavuutta eri organisaatiohierarkian tasoilla jonkin seuraavan ehdon perusteella:</span><span class="sxs-lookup"><span data-stu-id="ce0bf-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="ce0bf-106">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="ce0bf-106">Sales amount</span></span>
- <span data-ttu-id="ce0bf-107">Määrä</span><span class="sxs-lookup"><span data-stu-id="ce0bf-107">Quantity</span></span>
- <span data-ttu-id="ce0bf-108">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="ce0bf-108">Gross profit margin</span></span>
- <span data-ttu-id="ce0bf-109">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="ce0bf-109">Margin percentage</span></span>

<span data-ttu-id="ce0bf-110">Voit käyttää tässä arvioinnissa valmista **Parhaat asiakkaat** -raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="ce0bf-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="ce0bf-111">**Myymälän hallinta** -työtila &gt; **Retail ja Commerce** &gt; **Kanavat** &gt; **Myymälän hallinta** &gt; **Raportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="ce0bf-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="ce0bf-112">**Kyselyt ja raportit** -osio &gt; **Retail ja Commerce** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Suurimpien asiakkaiden raportti**</span><span class="sxs-lookup"><span data-stu-id="ce0bf-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="ce0bf-113">Samalla tavoin, käyttäjät voivat tutkia parhaiden tuotteiden (10 - 100) tuottavuutta eri organisaatiohierarkian tasoilla perustuen yhteen seuraavista kriteereistä:</span><span class="sxs-lookup"><span data-stu-id="ce0bf-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="ce0bf-114">Myyntisumma</span><span class="sxs-lookup"><span data-stu-id="ce0bf-114">Sales amount</span></span>
- <span data-ttu-id="ce0bf-115">Määrä</span><span class="sxs-lookup"><span data-stu-id="ce0bf-115">Quantity</span></span>
- <span data-ttu-id="ce0bf-116">Bruttovoittokate</span><span class="sxs-lookup"><span data-stu-id="ce0bf-116">Gross profit margin</span></span>
- <span data-ttu-id="ce0bf-117">Marginaalin prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="ce0bf-117">Margin percentage</span></span>

<span data-ttu-id="ce0bf-118">Voit käyttää tässä arvioinnissa valmista **Parhaat tuotteet**-raporttia, jonka voit avata mistä tahansa seuraavista sijainneista:</span><span class="sxs-lookup"><span data-stu-id="ce0bf-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="ce0bf-119">**Myymälän hallinta** -työtila &gt; **Retail ja Commerce** &gt; **Kanavat** &gt; **Myymälän hallinta** &gt; **Raportit** &gt; **Suurimpien tuotteiden raportti**</span><span class="sxs-lookup"><span data-stu-id="ce0bf-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="ce0bf-120">**Luokka- ja tuotehallinta** -työtila &gt; **Retail ja Commerce** &gt; **Tuotteet ja luokat** &gt; **Myymälän hallinta** &gt; **Raportti** &gt; **Parhaat tuotteet -raportti**</span><span class="sxs-lookup"><span data-stu-id="ce0bf-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="ce0bf-121">**Kyselyt ja raportit** -osio &gt; **Retail ja Commerce** &gt; **Kyselyt ja raportit** &gt; **Myyntiraportit** &gt; **Suurimpien tuotteiden raportti**</span><span class="sxs-lookup"><span data-stu-id="ce0bf-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]