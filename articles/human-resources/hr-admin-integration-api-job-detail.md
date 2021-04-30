---
title: Työn tietojen ohjelmointirajapinta
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Työn tiedot -yksikölle Dynamics 365 Human Resourcesissa.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f15282bf72340cb1a832ff3264361472d0a6c70
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881973"
---
# <a name="job-detail-api"></a><span data-ttu-id="e59cc-103">Työn tietojen ohjelmointirajapinta</span><span class="sxs-lookup"><span data-stu-id="e59cc-103">Job detail API</span></span>

<span data-ttu-id="e59cc-104">Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn Työn tiedot -yksikölle Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="e59cc-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e59cc-105">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e59cc-105">Properties</span></span>

| <span data-ttu-id="e59cc-106">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="e59cc-106">Property</span></span><br><span data-ttu-id="e59cc-107">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="e59cc-107">**Physical name**</span></span><br><span data-ttu-id="e59cc-108">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="e59cc-108">**_Type_**</span></span> | <span data-ttu-id="e59cc-109">Käytä</span><span class="sxs-lookup"><span data-stu-id="e59cc-109">Use</span></span> | <span data-ttu-id="e59cc-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e59cc-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e59cc-111">**Työn tunnus**</span><span class="sxs-lookup"><span data-stu-id="e59cc-111">**Job ID**</span></span><br><span data-ttu-id="e59cc-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="e59cc-112">mshr_jobid</span></span><br><span data-ttu-id="e59cc-113">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e59cc-113">*String*</span></span> | <span data-ttu-id="e59cc-114">Vain luku</span><span class="sxs-lookup"><span data-stu-id="e59cc-114">Read-only</span></span><br><span data-ttu-id="e59cc-115">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="e59cc-115">Required</span></span> | <span data-ttu-id="e59cc-116">Työn yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="e59cc-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="e59cc-117">**Markkinahinnan alaraja**</span><span class="sxs-lookup"><span data-stu-id="e59cc-117">**Market price low threshold**</span></span><br><span data-ttu-id="e59cc-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="e59cc-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="e59cc-119">*Desimaali*</span><span class="sxs-lookup"><span data-stu-id="e59cc-119">*Decimal*</span></span> | | <span data-ttu-id="e59cc-120">Järjestelmän luoma GUID-arvo, jonka avulla toimi voidaan yksilöivästi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="e59cc-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
