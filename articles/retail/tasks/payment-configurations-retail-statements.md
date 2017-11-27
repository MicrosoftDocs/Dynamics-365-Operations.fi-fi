--- 
title: "Vähittäismyynnin laskelmien maksun konfiguraatiot"
description: "Tässä menettelyssä esitellään vähittäismyymälän maksutavat, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 19f9c0b1c3a93ed9c84d66041814fd64951744b0
ms.contentlocale: fi-fi
ms.lasthandoff: 11/14/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="c01f0-103">Vähittäismyynnin laskelmien maksun konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="c01f0-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c01f0-104">Tässä menettelyssä esitellään vähittäismyymälän maksutavat, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="c01f0-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="c01f0-105">Tässä tallenteessa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="c01f0-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="c01f0-106">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="c01f0-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="c01f0-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c01f0-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c01f0-108">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c01f0-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c01f0-109">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="c01f0-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="c01f0-110">Valitse Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="c01f0-110">Click Payment methods.</span></span>
6. <span data-ttu-id="c01f0-111">Laajenna tai tiivistä Kirjaus-osa.</span><span class="sxs-lookup"><span data-stu-id="c01f0-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="c01f0-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c01f0-112">Click Edit.</span></span>
    * <span data-ttu-id="c01f0-113">Määritä, kirjataanko tälle maksulle vastaanotettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="c01f0-114">Valitse tili, jolle tämän maksutavan vastaanotetut summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c01f0-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="c01f0-115">Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja tälle maksutavalle lasketun summan mahdolliset erot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c01f0-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="c01f0-116">Tähän kenttään voi syöttää summan, joka määrittää, milloin erosumma tulee kirjata toiselle erotilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="c01f0-117">Tätä voi käyttää suurien erojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="c01f0-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="c01f0-118">Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja lasketun summan väliset erot kirjataan, kun ero ylittää Eron enimmäissumma -kentässä määritetyn arvo.</span><span class="sxs-lookup"><span data-stu-id="c01f0-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="c01f0-119">Valitse Kyllä, kun pankkiin toimitettavat summat kirjataan erilliselle tilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="c01f0-120">Tässä kentässä voit määrittää, kirjataanko pankkiin toimitettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="c01f0-121">Valitse tili, jolle pankkiin toimitettavat summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c01f0-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="c01f0-122">Valitse pankkitapahtuman tyyppi, jota käytetään, kun pankkiin toimitettavat summat kirjataan pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="c01f0-123">Valitse Kyllä, kun kassakaappiin toimitettavat summat kirjataan erilliselle tilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="c01f0-124">Määritä, kirjataanko kassakaappiin toimitettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="c01f0-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="c01f0-125">Valitse tili, jolle kassakaappiin toimitettavat summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c01f0-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="c01f0-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c01f0-126">Click Save.</span></span>


