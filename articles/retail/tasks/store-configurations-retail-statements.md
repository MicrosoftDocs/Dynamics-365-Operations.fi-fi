---
title: Vähittäismyynnin laskelmien myymälän konfiguraatiot
description: Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916527"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="69838-103">Vähittäismyynnin laskelmien myymälän konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="69838-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="69838-104">Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="69838-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="69838-105">Vähittäismyymälöiden taloushallinnon dimensioita käsitellään toisessa menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="69838-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="69838-106">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="69838-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="69838-107">Siirry **siirtymisruudussa** kohtaan **Moduulit > Vähittäismyynti-ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät**.</span><span class="sxs-lookup"><span data-stu-id="69838-107">In the **Navgiation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
2. <span data-ttu-id="69838-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="69838-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="69838-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="69838-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="69838-110">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="69838-110">Click **Edit**.</span></span>
5. <span data-ttu-id="69838-111">**Laskelma/sulkeminen**-pikavälilehden asetukset vaikuttavat laskelman luomiseen, oikeellisuustarkistukseen ja kirjaamiseen myymälässä.</span><span class="sxs-lookup"><span data-stu-id="69838-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="69838-112">Laajenna **Laskelma/sulkeminen**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="69838-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="69838-113">Valitse **Laskelmatapa**-kentässä laskelmarivien ryhmittelyssä käytettävä tapa.</span><span class="sxs-lookup"><span data-stu-id="69838-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="69838-114">Valitse **Yksi laskelma päivässä** -kohdassa Kyllä, jos päivää kohti luodaan vain yksi laskelma, kun laskelmia luodaan laskelman luonnin erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="69838-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="69838-115">**Kassan laskeminen maksuvälineittäin** -kentässä määritetään, lisätäänkö kassan laskemiset yhteen vai käytetäänkö viimeistä kassan laskemista.</span><span class="sxs-lookup"><span data-stu-id="69838-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="69838-116">Valitse **Pyöristys**-kentässä kirjanpitotili, jolle pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="69838-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="69838-117">**Pyöristyseron enimmäissumma** -kenttään voi syöttää pyöristyseron sallitun enimmäissumman.</span><span class="sxs-lookup"><span data-stu-id="69838-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="69838-118">**Kirjaus**-kenttään voi syöttää laskelman kirjauksen sallitun enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="69838-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="69838-119">**Vuoro**-kenttään voi syöttää laskelman enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="69838-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="69838-120">**Tapahtuma**-kenttään voi syöttää laskelmarivin enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="69838-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="69838-121">**Sulkemistapa**-kenttään voi määrittää, ovatko laskelmaan sisällytettävät tapahtumat osa suljettua vuoroa vai voivatko ne olla mitä tahansa määritetyn päivämäärä-/aikavälin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="69838-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="69838-122">**Työpäivän päätös** -kenttään voi syöttää ajan, jos keskiyön jälkeiset tapahtumat tulee kirjata edelliselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="69838-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="69838-123">Valitse **Kirjaa työpäivänä** -kohdassa Kyllä, jos keskiyön jälkeiset tapahtumat kirjataan edellisen päivän osaksi.</span><span class="sxs-lookup"><span data-stu-id="69838-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="69838-124">Valitse **Jakoperusteena laskelmatapa** -kohdassa Kyllä, kun jokaiselle määritetylle laskelmatavalle luodut laskelmat haetaan.</span><span class="sxs-lookup"><span data-stu-id="69838-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="69838-125">Tämä voi olla hyödyllistä, jos kirjauksen suoritustasoa on parannettava myymälöissä, joiden tapahtumamäärät ovat suuria, ja halutaan useita pieniä rinnakkain käsiteltäviä laskelmia.</span><span class="sxs-lookup"><span data-stu-id="69838-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="69838-126">Valitse **Yleiset**-pikavälilehdessä **Oletusasiakas**-kentässä myymälässä asioineiden asiakkaiden myynnissä käytettävä asiakastili.</span><span class="sxs-lookup"><span data-stu-id="69838-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

