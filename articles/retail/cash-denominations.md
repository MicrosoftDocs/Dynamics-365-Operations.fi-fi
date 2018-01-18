---
title: "Myyntipisteen käteisvarojen arvojen määrittäminen"
description: "Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 523ceb85d7f6a297c1e6d1bfb70761ddd888abe1
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="777b4-103">Myyntipisteen käteisvarojen arvojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="777b4-103">Configure cash denominations for POS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="777b4-104">Seteleiden ja kolikoiden arvot voidaan määrittää taustajärjestelmässä kassojen, myyjien ja esimiesten käyttöön myymälän myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="777b4-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="777b4-105">Näitä arvoja voidaan käyttää helpottamaan käteisvarojen laskemista, kun kassa lasketaan päivän lopussa maksuvälineittäin tai myynnin nopeassa maksuvälinetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="777b4-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="777b4-106">Arvojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="777b4-106">Define denominations</span></span>
<span data-ttu-id="777b4-107">Myymäläkohtaiset arvot määritetään **Asetukset** > **Myymäläominaisuuden kassatilitysasetus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="777b4-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![käteisvarojen arvot](./media/image1-denomination.png)

<span data-ttu-id="777b4-109">Arvon määrittäminen:</span><span class="sxs-lookup"><span data-stu-id="777b4-109">To define a denomination:</span></span>
1. <span data-ttu-id="777b4-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="777b4-110">Click **New**.</span></span>
1. <span data-ttu-id="777b4-111">Määritä tyyppi (kolikko tai seteli).</span><span class="sxs-lookup"><span data-stu-id="777b4-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="777b4-112">Määritä summa (arvo).</span><span class="sxs-lookup"><span data-stu-id="777b4-112">Specify the amount (value).</span></span>

![käteisvarojen arvot](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="777b4-114">Toimintoprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="777b4-114">Configure the functionality profile</span></span>
<span data-ttu-id="777b4-115">Kun myyntipisteessä maksetaan käteisellä, käyttäjä voi antaa asiakkaan maksaman summan nopeasti käyttämällä setelin arvoja.</span><span class="sxs-lookup"><span data-stu-id="777b4-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="777b4-116">Voit määrittää toimintoprofiilissa kaksi asetusta, jolla arvo näytetään myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="777b4-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="777b4-117">**Suurempi tai yhtä suuri summa erääntyy**: Myyntipiste näyttää oletusarvoisesti vain arvot, jotka ovat suurempia kuin erääntyvä summa, mikä mahdollistaa yhden kosketuksen maksuvälinetapahtuman.</span><span class="sxs-lookup"><span data-stu-id="777b4-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="777b4-118">Jos erääntyvä summa on esimerkiksi 7,50 $, myyntipiste näyttää seuraavat arvot: 10 $, 20 $, 50 $ ja 100 $.</span><span class="sxs-lookup"><span data-stu-id="777b4-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="777b4-119">Jonkin edellä mainitun summan koskettaminen käsittelee automaattisesti kyseisen summan myynnin.</span><span class="sxs-lookup"><span data-stu-id="777b4-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="777b4-120">1 ja 5 dollarin arvoja ei näytetä, koska nämä summat ovat pienempiä kuin erääntyvä summa.</span><span class="sxs-lookup"><span data-stu-id="777b4-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="777b4-121">**Kaikki arvot**: Kun tämä asetus valitaan, kaikki setelin arvot näytetään aina myyntipisteessä erääntyvästä summasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="777b4-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="777b4-122">Käyttäjä voikin määrittää erääntyvän summan käyttämällä seteliyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="777b4-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="777b4-123">Jos erääntyvä summa on esimerkiksi 25,00 $, käyttäjä voi viimeistellä myynnin valitsemalla 20 $ ja 5 $.</span><span class="sxs-lookup"><span data-stu-id="777b4-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

