--- 
title: "Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi"
description: "Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="8ee27-103">Konfiguraation lähteiden luominen ja niiden merkitseminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="8ee27-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ee27-104">Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="8ee27-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="8ee27-105">Kunkin ER-konfiguraation tekijänä pidetään lähdettä.</span><span class="sxs-lookup"><span data-stu-id="8ee27-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="8ee27-106">Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="8ee27-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="8ee27-107">Luo lähde</span><span class="sxs-lookup"><span data-stu-id="8ee27-107">Create a provider</span></span>
1. <span data-ttu-id="8ee27-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="8ee27-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8ee27-109">Valitse Konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="8ee27-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="8ee27-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8ee27-110">Click New.</span></span>
    * <span data-ttu-id="8ee27-111">Lähdetietueella on yksilöivä nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="8ee27-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="8ee27-112">Tarkista tämän sivun sisältö ja ohita tämä menettely, jos Litware, Inc. (http://www.litware.com) on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="8ee27-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="8ee27-113">Syötä Nimi-kenttään Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8ee27-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="8ee27-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8ee27-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="8ee27-115">Kirjoita Internet-osoite-kenttään http://www.litware.com.</span><span class="sxs-lookup"><span data-stu-id="8ee27-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="8ee27-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8ee27-116">Click Save.</span></span>
7. <span data-ttu-id="8ee27-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8ee27-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="8ee27-118">Valitse aktiiviseksi lähteeksi</span><span class="sxs-lookup"><span data-stu-id="8ee27-118">Select as an active provider</span></span>
1. <span data-ttu-id="8ee27-119">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8ee27-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="8ee27-120">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="8ee27-120">Click Set active.</span></span>


