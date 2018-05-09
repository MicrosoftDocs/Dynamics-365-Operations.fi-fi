--- 
title: Kirjaa kirjatut kirjauskansioviennit
description: "Tässä menettelyssä käsitellään kirjattujen kirjauskansiovientien kirjaaminen."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7211e56f80b085f6a245010e780512e92a52bc57
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="cedda-103">Kirjaa kirjatut kirjauskansioviennit</span><span class="sxs-lookup"><span data-stu-id="cedda-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cedda-104">Tässä menettelyssä käsitellään kirjattujen kirjauskansiovientien kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="cedda-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="cedda-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="cedda-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="cedda-106">Vahvista kirjausasetukset valitsemalla Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit.</span><span class="sxs-lookup"><span data-stu-id="cedda-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="cedda-107">Laajennettu kirjanpidon kirjauskansio -kentän arvoksi voi määrittää Kyllä tai Ei.</span><span class="sxs-lookup"><span data-stu-id="cedda-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="cedda-108">Jos asetus on Kyllä, raportin tiedot ovat erilaisia.</span><span class="sxs-lookup"><span data-stu-id="cedda-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="cedda-109">Valitse, voiko kauden sulkea, jos kirjaamisprosessia ei ole suoritettu.</span><span class="sxs-lookup"><span data-stu-id="cedda-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="cedda-110">Jos asetukseksi on määritetty Kyllä, aikajaksoa ei voi sulkea, ennen kuin jakson kirjaamisprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="cedda-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="cedda-111">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cedda-111">Close the page.</span></span>
5. <span data-ttu-id="cedda-112">Valitse Kirjanpito > Kausittaiset tehtävät > Kirjauskansion kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="cedda-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="cedda-113">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="cedda-113">Click Filter.</span></span>
7. <span data-ttu-id="cedda-114">Korosta rivi, jolle haluat määrittää suodatusehdot.</span><span class="sxs-lookup"><span data-stu-id="cedda-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="cedda-115">Syötä tai valitse suodatusehdot Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cedda-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="cedda-116">Sulje suodatussivu valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="cedda-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="cedda-117">Aloita kirjausprosessi valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="cedda-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="cedda-118">Raportti luodaan, kun prosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="cedda-118">A report will be generated after the process is complete.</span></span>  


