---
title: Määritä asiakkaan maksutapa
description: Tässä ohjeaiheessa käsitellään, kuinka maksutapa luodaan asiakasmaksuille.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b9960c3fdf0d65be19e28dbb41913a310ae7530
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442761"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="a3413-103">Määritä asiakkaan maksutapa</span><span class="sxs-lookup"><span data-stu-id="a3413-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3413-104">Tässä ohjeaiheessa käsitellään, kuinka maksutapa luodaan asiakasmaksuille.</span><span class="sxs-lookup"><span data-stu-id="a3413-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="a3413-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="a3413-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a3413-106">Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra >Maksujen asetukset > Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="a3413-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a3413-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a3413-107">Select **New**.</span></span>
3. <span data-ttu-id="a3413-108">Syötä **Maksutapa**-kenttään maksutavan tunnus.</span><span class="sxs-lookup"><span data-stu-id="a3413-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="a3413-109">Laskuissa ja maksuissa näkyy maksutavan tunnus. Tee siitä riittävän kuvaava, jolloin siitä selviää tallennettavan maksun tyyppi ja pankkitili.</span><span class="sxs-lookup"><span data-stu-id="a3413-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="a3413-110">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a3413-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a3413-111">Määritä, minkä maksun tilan maksujen kirjaaminen vaatii.</span><span class="sxs-lookup"><span data-stu-id="a3413-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="a3413-112">Asiakkaan maksu voidaan kirjata luonnin yhteydessä vain silloin, kun maksun tila on sama kuin tässä määrittämäsi maksun tila.</span><span class="sxs-lookup"><span data-stu-id="a3413-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="a3413-113">Määritä, miten asiakkaan maksut luodaan laskuille.</span><span class="sxs-lookup"><span data-stu-id="a3413-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="a3413-114">Tätä asetusta käytetään vain maksuehdotuksen suorituksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a3413-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="a3413-115">Maksuehdotusta voidaan käyttää asiakkaan maksuissa suoraveloituksissa ja haettaessa varoja asiakkaiden pankkitileiltä.</span><span class="sxs-lookup"><span data-stu-id="a3413-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="a3413-116">Valitse maksutapa.</span><span class="sxs-lookup"><span data-stu-id="a3413-116">Select the type of payment.</span></span> <span data-ttu-id="a3413-117">Maksutyypin avulla määritetään, vaatiiko maksu tarkistuksen.</span><span class="sxs-lookup"><span data-stu-id="a3413-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="a3413-118">Määritä tilityyppi, jolle maksut kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a3413-118">Select what account type payments will post to.</span></span> <span data-ttu-id="a3413-119">Yleensä arvoksi valitaan Pankki.</span><span class="sxs-lookup"><span data-stu-id="a3413-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="a3413-120">Valitse pankkitili, jolle tämä maksu kirjataan.</span><span class="sxs-lookup"><span data-stu-id="a3413-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="a3413-121">Syötä pankkitapahtuman tyyppi, jonka avulla pankin käyttämä maksutyyppi tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="a3413-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="a3413-122">Pankkitapahtumalajia käytetään pankkitilin täsmäytysprosessin aikana. Sen avulla täsmäytys on helpompi tehdä.</span><span class="sxs-lookup"><span data-stu-id="a3413-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="a3413-123">Määritä, kirjataanko tämä maksu väliaikaisesti välitilille.</span><span class="sxs-lookup"><span data-stu-id="a3413-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="a3413-124">Jos haluat kokeilla maksulle kellutusaikaa pankin selvityksessä, käytä välitiliöintitoimintoa.</span><span class="sxs-lookup"><span data-stu-id="a3413-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="a3413-125">Maksu kirjataan väliaikaisesti kirjanpitotilille, kunnes selvitys on tehty. Tällöin maksu siirretään tässä määrittämällesi pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="a3413-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="a3413-126">Syötä päätili välitiöintiä varten.</span><span class="sxs-lookup"><span data-stu-id="a3413-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="a3413-127">Tämä on päätili, jolle maksu kirjataan väliaikaisesti välitiliöinnin avulla.</span><span class="sxs-lookup"><span data-stu-id="a3413-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="a3413-128">Määritä sähköisten maksujen asetukset **Tiedostomuoto**-välilehden avulla.</span><span class="sxs-lookup"><span data-stu-id="a3413-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="a3413-129">Määritä pakolliset kentät **Maksunvalvonta**-välilehden avulla.</span><span class="sxs-lookup"><span data-stu-id="a3413-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="a3413-130">Jos esimerkiksi haluat käyttää kaikkien maksujen tallentamisessa tätä tapaa, voit valita tämän välilehden kyseisen asetuksen.</span><span class="sxs-lookup"><span data-stu-id="a3413-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="a3413-131">Määritä **Maksun määritteet** -välilehden avulla, mitä maksumääritteitä haluat käyttää tässä maksutavassa.</span><span class="sxs-lookup"><span data-stu-id="a3413-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="a3413-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a3413-132">Select **Save**.</span></span>

