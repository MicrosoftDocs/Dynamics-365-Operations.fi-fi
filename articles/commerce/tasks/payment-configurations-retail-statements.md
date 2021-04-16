---
title: Vähittäismyynnin laskelmien maksun konfiguraatiot
description: Tässä menettelyssä esitellään Commercen maksutavat, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edd4a73523934e1fd70995c9275c564a50809957
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796703"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="9c896-103">Vähittäismyynnin laskelmien maksun konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="9c896-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c896-104">Tässä menettelyssä esitellään Commercen maksutavat, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="9c896-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="9c896-105">Tässä tallenteessa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="9c896-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="9c896-106">Valitse Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät.</span><span class="sxs-lookup"><span data-stu-id="9c896-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="9c896-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c896-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9c896-108">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9c896-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9c896-109">Valitse toimintoruudussa Määritä.</span><span class="sxs-lookup"><span data-stu-id="9c896-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="9c896-110">Valitse Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="9c896-110">Click Payment methods.</span></span>
6. <span data-ttu-id="9c896-111">Laajenna tai tiivistä Kirjaus-osa.</span><span class="sxs-lookup"><span data-stu-id="9c896-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="9c896-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9c896-112">Click Edit.</span></span>
    * <span data-ttu-id="9c896-113">Määritä, kirjataanko tälle maksulle vastaanotettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="9c896-114">Valitse tili, jolle tämän maksutavan vastaanotetut summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9c896-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="9c896-115">Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja tälle maksutavalle lasketun summan mahdolliset erot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9c896-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="9c896-116">Tähän kenttään voi syöttää summan, joka määrittää, milloin erosumma tulee kirjata toiselle erotilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="9c896-117">Tätä voi käyttää suurien erojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="9c896-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="9c896-118">Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja lasketun summan väliset erot kirjataan, kun ero ylittää Eron enimmäissumma -kentässä määritetyn arvo.</span><span class="sxs-lookup"><span data-stu-id="9c896-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="9c896-119">Valitse Kyllä, kun pankkiin toimitettavat summat kirjataan erilliselle tilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="9c896-120">Tässä kentässä voit määrittää, kirjataanko pankkiin toimitettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="9c896-121">Valitse tili, jolle pankkiin toimitettavat summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9c896-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="9c896-122">Valitse pankkitapahtuman tyyppi, jota käytetään, kun pankkiin toimitettavat summat kirjataan pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="9c896-123">Valitse Kyllä, kun kassakaappiin toimitettavat summat kirjataan erilliselle tilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="9c896-124">Määritä, kirjataanko kassakaappiin toimitettavat summat kirjanpitotilille vai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="9c896-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="9c896-125">Valitse tili, jolle kassakaappiin toimitettavat summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9c896-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="9c896-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9c896-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]