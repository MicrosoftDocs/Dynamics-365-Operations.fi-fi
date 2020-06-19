---
title: Projektiarvion poistaminen
description: Tässä ohjeaiheessa on tietoja projektiarvion poistamisesta sen jälkeen, kun se on valmis.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410214"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="35f70-103">Projektiarvion poistaminen</span><span class="sxs-lookup"><span data-stu-id="35f70-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35f70-104">Projektin arviot sisältävät projektin arvioidun ja ajoitetun työmäärän rahoitusnäkymän.</span><span class="sxs-lookup"><span data-stu-id="35f70-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="35f70-105">Voidaksesi työskennellä projektin arvioiden kanssa, projekti on liitettävä arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="35f70-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="35f70-106">Arviointiprojekti perustuu aina aiemmin luotuun projektiin, mutta kuitenkin useat projektit voivat viitata yksittäiseen arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="35f70-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="35f70-107">Vain kiinteähintaiset ja investointiprojektit voidaan liittää arviointiprojekteihin, ja näiden projektien on kuuluttava samaan projektiryhmään kuin arviointiprojekti.</span><span class="sxs-lookup"><span data-stu-id="35f70-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="35f70-108">Arviointiprojektin eliminointi edellyttää, että se on valmis.</span><span class="sxs-lookup"><span data-stu-id="35f70-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="35f70-109">Seuraavassa kerrotaan, kuinka arvio poistetaan.</span><span class="sxs-lookup"><span data-stu-id="35f70-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="35f70-110">Valitse **Projektinhallinta ja kirjanpito** > **Kaikki projektit** ja avaa projekti.</span><span class="sxs-lookup"><span data-stu-id="35f70-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="35f70-111">Valitse **Hallitse**-välilehdessä **Arviot** ja valitse **Arvio**-sivulla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="35f70-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="35f70-112">Määritä **Yleiset**-välilehden **Poista arvio** -sivulla seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="35f70-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="35f70-113">**Kausikoodi**: Valitse kausikoodi arviointiprojektien valintaa varten.</span><span class="sxs-lookup"><span data-stu-id="35f70-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="35f70-114">**Arviopäivämäärä**: Valitse eliminoinnin arviopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="35f70-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="35f70-115">**Eliminoi ja KET-varoitukset**: Ota tämä vaihtoehto käyttöön, kun keskeneräiseen työhön (KET) liittyvä arvio poistetaan.</span><span class="sxs-lookup"><span data-stu-id="35f70-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="35f70-116">Jos tämä vaihtoehto ei ole käytössä, eliminointi ei voi jatkua, jos ei-arvioituja tapahtumia on olemassa.</span><span class="sxs-lookup"><span data-stu-id="35f70-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="35f70-117">Tämä vaihtoehto on käytettävissä vain, kun eliminointi kohdistetaan arviointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="35f70-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="35f70-118">Se ei ole käytettävissä, jos käytät kausittaisia kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="35f70-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="35f70-119">Tämä asetus toimii **Projekti parametrit** -sivun **Arvio**-välilehden asetusten **Salli eliminointi, kun ei-arvioidut tapahtumat ovat olemassa** -kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="35f70-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="35f70-120">**Aseta vaihe valmiiksi**: Ota tämä asetus käyttöön, kun haluat määrittää, että arviointiprojektin vaihe on **Valmis** eliminoinnin suorittamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="35f70-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="35f70-121">**Tulosta arviointiluettelo**: Valitse tiedot, jotka otetaan mukaan arviointiluetteloa tulostettaessa.</span><span class="sxs-lookup"><span data-stu-id="35f70-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="35f70-122">**Näytä infoloki**: Ota tämä vaihtoehto käyttöön, kun haluat näyttää infolokin.</span><span class="sxs-lookup"><span data-stu-id="35f70-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="35f70-123">**Kirjauspvm**: Valitse arvion kirjanpidon kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="35f70-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="35f70-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="35f70-124">Select **OK**.</span></span>
5. <span data-ttu-id="35f70-125">Kun eliminointiprosessi on valmis, eliminoitu arviointiprojekti näytetään negatiivisena arvona.</span><span class="sxs-lookup"><span data-stu-id="35f70-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="35f70-126">Jos et aio poistaa arviota, voit valita eliminoidun arvion ja valita **Peruuta eliminointi**.</span><span class="sxs-lookup"><span data-stu-id="35f70-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
