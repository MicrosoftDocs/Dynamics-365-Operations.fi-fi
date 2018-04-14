--- 
title: "Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9ed6f62318cd6806de1b4c9d6aa314c5f0a25500
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="65f57-103">Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="65f57-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65f57-104">Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="65f57-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="65f57-105">Kunkin ER-konfiguraation tekijänä pidetään lähdettä.</span><span class="sxs-lookup"><span data-stu-id="65f57-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="65f57-106">Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="65f57-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="65f57-107">Luo lähde</span><span class="sxs-lookup"><span data-stu-id="65f57-107">Create a provider</span></span>
1. <span data-ttu-id="65f57-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="65f57-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="65f57-109">Valitse Konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="65f57-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="65f57-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="65f57-110">Click New.</span></span>
    * <span data-ttu-id="65f57-111">Lähdetietueella on yksilöivä nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="65f57-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="65f57-112">Seuraa tämän sivun sisältöä ja ohita tämä menettely, jos Litware, Inc. (`http://www.litware.com`) on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="65f57-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="65f57-113">Syötä Nimi-kenttään Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="65f57-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="65f57-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="65f57-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="65f57-115">Kirjoita Internet-osoite-kenttään `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="65f57-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="65f57-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="65f57-116">Click Save.</span></span>
7. <span data-ttu-id="65f57-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="65f57-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="65f57-118">Valitse aktiiviseksi lähteeksi</span><span class="sxs-lookup"><span data-stu-id="65f57-118">Select as an active provider</span></span>
1. <span data-ttu-id="65f57-119">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="65f57-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="65f57-120">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="65f57-120">Click Set active.</span></span>


