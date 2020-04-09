---
title: Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi
description: Tässä ohjeaiheessa käsitellään tapaa, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5f238a492dbc3f9318b1bd1d3ea5657e92b33fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142106"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="89f8e-103">Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi</span><span class="sxs-lookup"><span data-stu-id="89f8e-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89f8e-104">Tässä ohjeaiheessa käsitellään tapaa, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="89f8e-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="89f8e-105">Kunkin ER-konfiguraation tekijänä pidetään lähdettä.</span><span class="sxs-lookup"><span data-stu-id="89f8e-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="89f8e-106">Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="89f8e-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="89f8e-107">Luo lähde</span><span class="sxs-lookup"><span data-stu-id="89f8e-107">Create a provider</span></span>
1. <span data-ttu-id="89f8e-108">Valitse **siirtymisruutu** vasemmassa yläkulmassa ja valitsemalla **Organisaation hallinto**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="89f8e-109">Valitse **Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="89f8e-110">Valitse **Liittyvät linkit > Konfiguraation lähteet**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="89f8e-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-111">Select **New**.</span></span>
    - <span data-ttu-id="89f8e-112">Lähdetietueella on yksilöivä nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="89f8e-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="89f8e-113">Tarkista tämän sivun sisältö ja ohita tämä menettely, jos Litware, Inc. (https://www.litware.com) on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="89f8e-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="89f8e-114">Syötä Nimi-kenttään `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="89f8e-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="89f8e-115">Kirjoita Internet-osoite-kenttään `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="89f8e-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="89f8e-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-116">Select **Save**.</span></span>
8. <span data-ttu-id="89f8e-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="89f8e-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="89f8e-118">Valitse aktiiviseksi lähteeksi</span><span class="sxs-lookup"><span data-stu-id="89f8e-118">Select as an active provider</span></span>
1. <span data-ttu-id="89f8e-119">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="89f8e-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="89f8e-120">Valitse **Määritä aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="89f8e-120">Select **Set active**.</span></span>

![Sähköisen raportoinnin työtilan sivu](../media/GER-Task-ActiveProvider-1.png)
