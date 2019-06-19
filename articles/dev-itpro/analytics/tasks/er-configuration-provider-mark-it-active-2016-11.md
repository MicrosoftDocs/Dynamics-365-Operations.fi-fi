---
title: Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi
description: Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595392"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="fae9e-103">Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="fae9e-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fae9e-104">Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="fae9e-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="fae9e-105">Kunkin ER-konfiguraation tekijänä pidetään lähdettä.</span><span class="sxs-lookup"><span data-stu-id="fae9e-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="fae9e-106">Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="fae9e-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="fae9e-107">Luo lähde</span><span class="sxs-lookup"><span data-stu-id="fae9e-107">Create a provider</span></span>
1. <span data-ttu-id="fae9e-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="fae9e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="fae9e-109">Valitse Konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="fae9e-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="fae9e-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fae9e-110">Click New.</span></span>
    * <span data-ttu-id="fae9e-111">Lähdetietueella on yksilöivä nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fae9e-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="fae9e-112">Tarkista tämän sivun sisältö ja ohita tämä menettely, jos Litware, Inc. (https://www.litware.com) on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="fae9e-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="fae9e-113">Syötä Nimi-kenttään Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fae9e-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="fae9e-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fae9e-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="fae9e-115">Kirjoita Internet-osoite-kenttään https://www.litware.com.</span><span class="sxs-lookup"><span data-stu-id="fae9e-115">In the Internet address field, type 'https://www.litware.com'.</span></span>
    * https://www.litware.com  
6. <span data-ttu-id="fae9e-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fae9e-116">Click Save.</span></span>
7. <span data-ttu-id="fae9e-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fae9e-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="fae9e-118">Valitse aktiiviseksi lähteeksi</span><span class="sxs-lookup"><span data-stu-id="fae9e-118">Select as an active provider</span></span>
1. <span data-ttu-id="fae9e-119">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fae9e-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="fae9e-120">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="fae9e-120">Click Set active.</span></span>

