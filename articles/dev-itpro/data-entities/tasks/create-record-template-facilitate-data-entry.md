---
title: Tietuemallin luonti helpottamaan tietojen kirjaamista
description: Tämä menettely näyttää, miten voit luoda tietuemallin, jolloin usein käytettyjen kenttien arvoja ei tarvitse lisätä erikseen kussakin uudessa tietueessa.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b2ba56b6146f2495fb6a53c3cef9f549b1ad837
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848204"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="e4d13-103">Tietuemallin luonti helpottamaan tietojen kirjaamista</span><span class="sxs-lookup"><span data-stu-id="e4d13-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4d13-104">Tämä menettely näyttää, miten voit luoda tietuemallin, jolloin usein käytettyjen kenttien arvoja ei tarvitse lisätä erikseen kussakin uudessa tietueessa.</span><span class="sxs-lookup"><span data-stu-id="e4d13-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="e4d13-105">Tässä menettelyssä luodaan uusi tietue uusille käyttöomaisuuteen lisättäville kannettaville.</span><span class="sxs-lookup"><span data-stu-id="e4d13-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="e4d13-106">Tässä menettelyssä käytetään USMF-malliyritystä.</span><span class="sxs-lookup"><span data-stu-id="e4d13-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="e4d13-107">Siirry kohtaan Käyttöomaisuudet > Käyttöomaisuudet > Käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="e4d13-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="e4d13-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e4d13-108">Click New.</span></span>
3. <span data-ttu-id="e4d13-109">Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e4d13-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="e4d13-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4d13-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e4d13-111">Kirjoita esimerkiksi Yritysliidi, kannettava.</span><span class="sxs-lookup"><span data-stu-id="e4d13-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="e4d13-112">Kirjoita arvo Hakunimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4d13-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="e4d13-113">Kirjoita esimerkiksi "kannettava".</span><span class="sxs-lookup"><span data-stu-id="e4d13-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="e4d13-114">Laajenna Teknistä tietoa -osa.</span><span class="sxs-lookup"><span data-stu-id="e4d13-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="e4d13-115">Kirjoita arvo Valmistaja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4d13-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="e4d13-116">Kirjoita Malli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e4d13-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="e4d13-117">Kirjoita Mallin vuosi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e4d13-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="e4d13-118">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="e4d13-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="e4d13-119">Valitse Tietueen tiedot.</span><span class="sxs-lookup"><span data-stu-id="e4d13-119">Click Record info.</span></span>
12. <span data-ttu-id="e4d13-120">Valitse Käyttäjämalli.</span><span class="sxs-lookup"><span data-stu-id="e4d13-120">Click User template.</span></span>
13. <span data-ttu-id="e4d13-121">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4d13-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e4d13-122">Kirjoita esimerkiksi Yrityskannettava.</span><span class="sxs-lookup"><span data-stu-id="e4d13-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="e4d13-123">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4d13-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e4d13-124">Kirjoita esimerkiksi Yrityskannettava.</span><span class="sxs-lookup"><span data-stu-id="e4d13-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="e4d13-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e4d13-125">Click OK.</span></span>
16. <span data-ttu-id="e4d13-126">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="e4d13-126">Click Close.</span></span>

