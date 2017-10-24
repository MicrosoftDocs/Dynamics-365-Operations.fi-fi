--- 
title: "Vähittäismyynnin laskelmien myymälän konfiguraatiot"
description: "Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cac676c9c6ebb6769fe7e30ac08a2c8334befc24
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="138f4-103">Vähittäismyynnin laskelmien myymälän konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="138f4-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="138f4-104">Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="138f4-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="138f4-105">Vähittäismyymälöiden taloushallinnon dimensioita käsitellään toisessa menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="138f4-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="138f4-106">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="138f4-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="138f4-107">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="138f4-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="138f4-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="138f4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="138f4-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="138f4-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="138f4-110">Laskelma/sulkeminen-osan asetukset vaikuttavat laskelman luomiseen, oikeellisuustarkistukseen ja kirjaamiseen myymälässä.</span><span class="sxs-lookup"><span data-stu-id="138f4-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="138f4-111">Avaa Laskelma/sulkeminen-osa.</span><span class="sxs-lookup"><span data-stu-id="138f4-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="138f4-112">Valitse laskelmarivien ryhmittelyssä käytettävä tapa.</span><span class="sxs-lookup"><span data-stu-id="138f4-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="138f4-113">Valitse Kyllä, jos päivää kohti luodaan vain yksi laskelma, kun laskelmia luodaan laskelman luonnin erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="138f4-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="138f4-114">Kassan laskeminen maksuvälineittäin -kentässä määritetään, lisätäänkö kassan laskemiset yhteen vai käytetäänkö viimeistä kassan laskemista.</span><span class="sxs-lookup"><span data-stu-id="138f4-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="138f4-115">Valitse kirjanpitotili, jolle pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="138f4-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="138f4-116">Pyöristyseron enimmäissumma -kenttään voi syöttää pyöristyseron sallitun enimmäissumman.</span><span class="sxs-lookup"><span data-stu-id="138f4-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="138f4-117">Kirjaus-kenttään voi syöttää laskelman kirjauksen sallitun enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="138f4-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="138f4-118">Vuoro-kenttään voi syöttää laskelman enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="138f4-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="138f4-119">Tapahtuma-kenttään voi syöttää laskelmarivin enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="138f4-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="138f4-120">Sulkemistapa-kenttään voi määrittää, ovatko laskelmaan sisällytettävät tapahtumat osa suljettua vuoroa vai voivatko ne olla mitä tahansa määritetyn päivämäärä-/aikavälin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="138f4-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="138f4-121">Työpäivän päätös -kenttään voi syöttää ajan, jos keskiyön jälkeiset tapahtumat tulee kirjata edelliselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="138f4-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="138f4-122">Valitse Kyllä, jos keskiyön jälkeiset tapahtumat kirjataan edellisen päivän osaksi.</span><span class="sxs-lookup"><span data-stu-id="138f4-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="138f4-123">Valitse Kyllä, kun jokaiselle määritetylle laskelmatavalle luodut laskelmat haetaan.</span><span class="sxs-lookup"><span data-stu-id="138f4-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="138f4-124">Tämä voi olla hyödyllistä, jos kirjauksen suoritustasoa on parannettava myymälöissä, joiden tapahtumamäärät ovat suuria, ja halutaan useita pieniä rinnakkain käsiteltäviä laskelmia.</span><span class="sxs-lookup"><span data-stu-id="138f4-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="138f4-125">Valitse Oletusasiakas-kentässä myymälässä asioineiden asiakkaiden myynnissä käytettävä asiakastili.</span><span class="sxs-lookup"><span data-stu-id="138f4-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


