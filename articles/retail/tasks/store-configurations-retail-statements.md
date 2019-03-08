---
title: Vähittäismyynnin laskelmien myymälän konfiguraatiot
description: Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "354710"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="1ba43-103">Vähittäismyynnin laskelmien myymälän konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="1ba43-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1ba43-104">Tässä menettelyssä esitellään vähittäismyymälän konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="1ba43-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="1ba43-105">Vähittäismyymälöiden taloushallinnon dimensioita käsitellään toisessa menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="1ba43-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="1ba43-106">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="1ba43-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1ba43-107">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="1ba43-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="1ba43-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1ba43-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ba43-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1ba43-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ba43-110">Laskelma/sulkeminen-osan asetukset vaikuttavat laskelman luomiseen, oikeellisuustarkistukseen ja kirjaamiseen myymälässä.</span><span class="sxs-lookup"><span data-stu-id="1ba43-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="1ba43-111">Avaa Laskelma/sulkeminen-osa.</span><span class="sxs-lookup"><span data-stu-id="1ba43-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="1ba43-112">Valitse laskelmarivien ryhmittelyssä käytettävä tapa.</span><span class="sxs-lookup"><span data-stu-id="1ba43-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="1ba43-113">Valitse Kyllä, jos päivää kohti luodaan vain yksi laskelma, kun laskelmia luodaan laskelman luonnin erätyön avulla.</span><span class="sxs-lookup"><span data-stu-id="1ba43-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="1ba43-114">Kassan laskeminen maksuvälineittäin -kentässä määritetään, lisätäänkö kassan laskemiset yhteen vai käytetäänkö viimeistä kassan laskemista.</span><span class="sxs-lookup"><span data-stu-id="1ba43-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="1ba43-115">Valitse kirjanpitotili, jolle pyöristyserot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1ba43-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="1ba43-116">Pyöristyseron enimmäissumma -kenttään voi syöttää pyöristyseron sallitun enimmäissumman.</span><span class="sxs-lookup"><span data-stu-id="1ba43-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="1ba43-117">Kirjaus-kenttään voi syöttää laskelman kirjauksen sallitun enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="1ba43-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="1ba43-118">Vuoro-kenttään voi syöttää laskelman enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="1ba43-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="1ba43-119">Tapahtuma-kenttään voi syöttää laskelmarivin enimmäiskokonaiseron.</span><span class="sxs-lookup"><span data-stu-id="1ba43-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="1ba43-120">Sulkemistapa-kenttään voi määrittää, ovatko laskelmaan sisällytettävät tapahtumat osa suljettua vuoroa vai voivatko ne olla mitä tahansa määritetyn päivämäärä-/aikavälin tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="1ba43-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="1ba43-121">Työpäivän päätös -kenttään voi syöttää ajan, jos keskiyön jälkeiset tapahtumat tulee kirjata edelliselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="1ba43-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="1ba43-122">Valitse Kyllä, jos keskiyön jälkeiset tapahtumat kirjataan edellisen päivän osaksi.</span><span class="sxs-lookup"><span data-stu-id="1ba43-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="1ba43-123">Valitse Kyllä, kun jokaiselle määritetylle laskelmatavalle luodut laskelmat haetaan.</span><span class="sxs-lookup"><span data-stu-id="1ba43-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="1ba43-124">Tämä voi olla hyödyllistä, jos kirjauksen suoritustasoa on parannettava myymälöissä, joiden tapahtumamäärät ovat suuria, ja halutaan useita pieniä rinnakkain käsiteltäviä laskelmia.</span><span class="sxs-lookup"><span data-stu-id="1ba43-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="1ba43-125">Valitse Oletusasiakas-kentässä myymälässä asioineiden asiakkaiden myynnissä käytettävä asiakastili.</span><span class="sxs-lookup"><span data-stu-id="1ba43-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  

