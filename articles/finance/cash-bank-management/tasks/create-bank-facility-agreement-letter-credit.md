---
title: Luo pankin limiittisopimus remburssia varten
description: Tämä tehtävä näyttää, miten pankin limiittisopimus luodaan remburssin käsittelemistä varten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bffb5c802e8fa261e52197d1293ffb15c35981f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989151"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="2f64d-103">Luo pankin limiittisopimus remburssia varten</span><span class="sxs-lookup"><span data-stu-id="2f64d-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f64d-104">Tämä tehtävä näyttää, miten pankin limiittisopimus luodaan remburssin käsittelemistä varten.</span><span class="sxs-lookup"><span data-stu-id="2f64d-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="2f64d-105">Määritä pankin limiitit ja kirjausprofiilit ennen tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="2f64d-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="2f64d-106">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="2f64d-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="2f64d-107">Pankin limiittisopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="2f64d-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="2f64d-108">Siirry kohtaan Maksuliikenteen hallinta > Remburssit > Pankin limiittisopimukset.</span><span class="sxs-lookup"><span data-stu-id="2f64d-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="2f64d-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2f64d-109">Click New.</span></span>
3. <span data-ttu-id="2f64d-110">Syötä Sopimusnumero-kenttään sopimusnumero pankin kanssa tehdyn sopimuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2f64d-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="2f64d-111">Syötä Pankkitili-kenttään liikkeelle laskevan pankin tilinumero.</span><span class="sxs-lookup"><span data-stu-id="2f64d-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="2f64d-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2f64d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2f64d-113">Määritä päivämäärä ja kellonaika Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f64d-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="2f64d-114">Määritä päivämäärä ja kellonaika Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f64d-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="2f64d-115">Laajenna tai tiivistä Yleiset-osa.</span><span class="sxs-lookup"><span data-stu-id="2f64d-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="2f64d-116">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="2f64d-116">Click Add line.</span></span>
10. <span data-ttu-id="2f64d-117">Avaa haku valitsemalla Limiittityyppi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2f64d-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2f64d-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2f64d-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2f64d-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2f64d-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2f64d-120">Syötä Raja-kenttään pankin kanssa neuvoteltu limiittisumma.</span><span class="sxs-lookup"><span data-stu-id="2f64d-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="2f64d-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2f64d-121">Click Save.</span></span>
15. <span data-ttu-id="2f64d-122">Avaa valintaikkuna valitsemalla Laajenna.</span><span class="sxs-lookup"><span data-stu-id="2f64d-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="2f64d-123">Kirjoita Uusi sopimusnumero -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2f64d-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="2f64d-124">Määritä päivämäärä ja kellonaika Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f64d-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="2f64d-125">Valitse Laajenna.</span><span class="sxs-lookup"><span data-stu-id="2f64d-125">Click Extend.</span></span>
19. <span data-ttu-id="2f64d-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2f64d-126">Close the page.</span></span>

