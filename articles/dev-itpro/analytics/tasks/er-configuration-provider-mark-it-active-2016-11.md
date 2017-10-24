--- 
title: "Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="5a53a-103">Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="5a53a-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a53a-104">Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi luoda konfigurointilähteen sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="5a53a-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="5a53a-105">Kunkin ER-konfiguraation tekijänä pidetään lähdettä.</span><span class="sxs-lookup"><span data-stu-id="5a53a-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="5a53a-106">Tässä esimerkissä luodaan konfiguraation lähde malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="5a53a-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="5a53a-107">Luo lähde</span><span class="sxs-lookup"><span data-stu-id="5a53a-107">Create a provider</span></span>
1. <span data-ttu-id="5a53a-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="5a53a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5a53a-109">Valitse Konfiguraation lähteet.</span><span class="sxs-lookup"><span data-stu-id="5a53a-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="5a53a-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5a53a-110">Click New.</span></span>
    * <span data-ttu-id="5a53a-111">Lähdetietueella on yksilöivä nimi ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="5a53a-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="5a53a-112">Tarkista tämän sivun sisältö ja ohita tämä menettely, jos Litware, Inc.:n (http://www.litware.com) tietue on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="5a53a-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="5a53a-113">Syötä Nimi-kenttään Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5a53a-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="5a53a-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5a53a-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="5a53a-115">Syötä Internet-osoite-kenttään http://www.litware.com.</span><span class="sxs-lookup"><span data-stu-id="5a53a-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="5a53a-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="5a53a-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="5a53a-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5a53a-117">Click Save.</span></span>
7. <span data-ttu-id="5a53a-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5a53a-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="5a53a-119">Valitse aktiiviseksi lähteeksi</span><span class="sxs-lookup"><span data-stu-id="5a53a-119">Select as an active provider</span></span>
1. <span data-ttu-id="5a53a-120">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5a53a-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="5a53a-121">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="5a53a-121">Click Set active.</span></span>


