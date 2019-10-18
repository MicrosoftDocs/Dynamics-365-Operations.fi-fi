---
title: Kirjaa kirjatut kirjauskansioviennit
description: Tässä menettelyssä käsitellään kirjattujen kirjauskansiovientien kirjaaminen.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175403"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="25fbd-103">Kirjaa kirjatut kirjauskansioviennit</span><span class="sxs-lookup"><span data-stu-id="25fbd-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25fbd-104">Tässä menettelyssä käsitellään kirjattujen kirjauskansiovientien kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="25fbd-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="25fbd-105">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="25fbd-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="25fbd-106">Valitse **siirtymisruudussa** **Moduulit > Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="25fbd-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="25fbd-107">**Laajennettu kirjanpidon kirjauskansio** -kentän arvoksi voi määrittää Kyllä tai Ei.</span><span class="sxs-lookup"><span data-stu-id="25fbd-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="25fbd-108">Jos asetus on Kyllä, raportin tiedot ovat erilaisia.</span><span class="sxs-lookup"><span data-stu-id="25fbd-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="25fbd-109">Valitse, voiko kauden sulkea, jos kirjaamisprosessia ei ole suoritettu.</span><span class="sxs-lookup"><span data-stu-id="25fbd-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="25fbd-110">Jos asetukseksi on määritetty Kyllä, aikajaksoa ei voi sulkea, ennen kuin jakson kirjaamisprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="25fbd-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="25fbd-111">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="25fbd-111">Close the page.</span></span>
5. <span data-ttu-id="25fbd-112">Valitse **siirtymisruudussa** **Moduulit > Kirjanpito > Kausittaiset tehtävät > Kirjauskansion kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="25fbd-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="25fbd-113">Valitse **Suodatin**.</span><span class="sxs-lookup"><span data-stu-id="25fbd-113">Click **Filter**.</span></span>
7. <span data-ttu-id="25fbd-114">Korosta rivi, jolle haluat määrittää suodatusehdot.</span><span class="sxs-lookup"><span data-stu-id="25fbd-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="25fbd-115">Syötä tai valitse suodatusehdot **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="25fbd-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="25fbd-116">Sulje suodatussivu valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="25fbd-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="25fbd-117">Aloita kirjausprosessi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="25fbd-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="25fbd-118">Raportti luodaan, kun prosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="25fbd-118">A report will be generated after the process is complete.</span></span>  

