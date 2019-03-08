---
title: SEPA (Single Euro Payments Area) -suoraveloitusvaltakirjan asetukset
description: Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757f3f6e0c5443054d2d6bd21381d9f692e1b9a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "334815"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="075d0-103">SEPA (Single Euro Payments Area) -suoraveloitusvaltakirjan asetukset</span><span class="sxs-lookup"><span data-stu-id="075d0-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="075d0-104">Yhtenäisen euromaksualueen (SEPA) suoraveloituksen avulla velkoja voi hakea varoja asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen allekirjoitetun valtakirjan.</span><span class="sxs-lookup"><span data-stu-id="075d0-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="075d0-105">Asiakkaan allekirjoittama valtakirja antaa velkojalle valtuuden maksun hakemiseen ja ohjaa asiakkaan pankin maksamaan maksukehotuksen.</span><span class="sxs-lookup"><span data-stu-id="075d0-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="075d0-106">Tässä ohjeaiheessa kuvataan SEPA-suoraveloitusvaltakirjojen määrittämisprosessi.</span><span class="sxs-lookup"><span data-stu-id="075d0-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="075d0-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="075d0-107">Prerequisites</span></span>
<span data-ttu-id="075d0-108">Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="075d0-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="075d0-109">Luokka</span><span class="sxs-lookup"><span data-stu-id="075d0-109">Category</span></span>       | <span data-ttu-id="075d0-110">Edellytys</span><span class="sxs-lookup"><span data-stu-id="075d0-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075d0-111">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="075d0-111">Country/region</span></span> | <span data-ttu-id="075d0-112">Yrityksen ensisijaisen osoitteen on oltava seuraavissa maissa tai seuraavilla alueilla: Alankomaat, Belgia, Espanja, Italia, Itävalta, Ranska tai Saksa.</span><span class="sxs-lookup"><span data-stu-id="075d0-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="075d0-113">Määritä numerosarja suoraveloitusvaltakirjoille Jokaisella suoraveloitusvaltakirjalla on oltava yksilöllinen numero.</span><span class="sxs-lookup"><span data-stu-id="075d0-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="075d0-114">Luo **Numerosarjat**-sivulla suoraveloitusvaltakirjojen numerosarja.</span><span class="sxs-lookup"><span data-stu-id="075d0-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="075d0-115">Voit käyttää tätä tunnistetta suoraveloitusvaltakirjajärjestelmän numerosarjan määrittämiseen **Myyntireskontran parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="075d0-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="075d0-116">Määritä suoraveloitusvaltakirjojen myyntireskontran parametrit Määritä **Myyntireskontran parametrit** -sivulla suoraveloitusvaltakirjan parametrit.</span><span class="sxs-lookup"><span data-stu-id="075d0-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="075d0-117">Voit määrittää parametrit **Suoraveloitus**-välilehdellä muuttamalla oletusparametreja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="075d0-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="075d0-118">Päivitä sitten **Numerosarjat**-välilehden **Suoraveloitusvaltakirjan tunnus** -kenttään aiemmin määrittämäsi numerosarja.</span><span class="sxs-lookup"><span data-stu-id="075d0-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="075d0-119">Määritä maksutapa suoraveloitusvaltakirjoille Sinun on määritettävä maksutapa suoraveloitusvaltakirjoille.</span><span class="sxs-lookup"><span data-stu-id="075d0-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="075d0-120">Voit käyttää tätä maksutapaa laskukyselyille, joiden perusteella suoraveloitusmaksut luodaan.</span><span class="sxs-lookup"><span data-stu-id="075d0-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="075d0-121">Määritä maksutapa **Maksutavat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="075d0-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="075d0-122">Suoraveloitusvaltakirjan maksutapaa määritettäessä on suoritettava seuraavat maksutavan lisämääritykset:</span><span class="sxs-lookup"><span data-stu-id="075d0-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="075d0-123">Valitse **Maksutyyppi**-kentässä **Sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="075d0-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="075d0-124">Valinnainen: Jos haluat, että asiakkailla on oltava useita valtuutuksia, valitse **Kausi**-kentässä **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="075d0-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="075d0-125">Ohjelma luo kullekin laskulle erillisen maksun, ja jokainen maksu käyttää laskulle määritettyä valtakirjaa.</span><span class="sxs-lookup"><span data-stu-id="075d0-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="075d0-126">Voit luoda maksuja suoraveloitusvaltakirjojen avulla valitsemalla **Vaadi valtakirjaa**.</span><span class="sxs-lookup"><span data-stu-id="075d0-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="075d0-127">**Vaadi valtakirjaa** -vaihtoehto on käytettävissä vain, jos valitset **Sähköinen maksu** **Maksutyyppi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="075d0-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="075d0-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="075d0-128">Additional resources</span></span>

[<span data-ttu-id="075d0-129">Suoraveloituksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="075d0-129">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="075d0-130">Luo suoraveloitusvaltakirja asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="075d0-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

