---
title: Luo pankin limiittisopimus takausasiakirjaa varten
description: Tässä tehtävässä luodaan pankin limiittisopimus takuuasiakirjan käsittelyä varten.
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2fe6bfebcc0cc302d623a34fd994a57cbea1c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177556"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="52f47-103">Luo pankin limiittisopimus takausasiakirjaa varten</span><span class="sxs-lookup"><span data-stu-id="52f47-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52f47-104">Tässä tehtävässä luodaan pankin limiittisopimus takuuasiakirjan käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="52f47-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="52f47-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="52f47-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="52f47-106">Pankin limiittisopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="52f47-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="52f47-107">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Pankin limiittisopimukset.</span><span class="sxs-lookup"><span data-stu-id="52f47-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="52f47-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="52f47-108">Click New.</span></span>
3. <span data-ttu-id="52f47-109">Anna Sopimusnumero-kenttään tapahtuman pankkisopimuksen numero.</span><span class="sxs-lookup"><span data-stu-id="52f47-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="52f47-110">Valitse Pankkitili-kenttään pankkitilin numero, jolle takausasiakirja on avattu.</span><span class="sxs-lookup"><span data-stu-id="52f47-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="52f47-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="52f47-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="52f47-112">Määritä päivämäärä ja kellonaika Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52f47-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="52f47-113">Määritä päivämäärä ja kellonaika Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52f47-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="52f47-114">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="52f47-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="52f47-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="52f47-115">Click Add line.</span></span>
10. <span data-ttu-id="52f47-116">Avaa haku valitsemalla Limiittityyppi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="52f47-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="52f47-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="52f47-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="52f47-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="52f47-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="52f47-119">Kirjoita Raja-kenttään pankin kanssa neuvoteltu summa.</span><span class="sxs-lookup"><span data-stu-id="52f47-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="52f47-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="52f47-120">Click Save.</span></span>
15. <span data-ttu-id="52f47-121">Ota Takausasiakirja-osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="52f47-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="52f47-122">Valitse vaihtoehto Laskentatapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="52f47-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="52f47-123">Anna tarvittaessa laskentatapa ja prosenttiosuudet seuraaville tiedoille: käteismarginaali, liikkeellelaskuprovisio, laajennusprovisio, arvonlisäysprovisio ja arvonvähennysprovisio.</span><span class="sxs-lookup"><span data-stu-id="52f47-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="52f47-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="52f47-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="52f47-125">Laajenna pankin limiittisopimus</span><span class="sxs-lookup"><span data-stu-id="52f47-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="52f47-126">Avaa valintaikkuna valitsemalla Laajenna.</span><span class="sxs-lookup"><span data-stu-id="52f47-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="52f47-127">Kirjoita Uusi sopimusnumero -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="52f47-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="52f47-128">Määritä päivämäärä ja kellonaika Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52f47-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="52f47-129">Valitse Laajenna.</span><span class="sxs-lookup"><span data-stu-id="52f47-129">Click Extend.</span></span>
5. <span data-ttu-id="52f47-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="52f47-130">Click Save.</span></span>
6. <span data-ttu-id="52f47-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="52f47-131">Close the page.</span></span>

