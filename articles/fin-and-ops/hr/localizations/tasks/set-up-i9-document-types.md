--- 
title: "Määritä I-9-asiakirjatyypit"
description: "Tässä menettelyssä kerrotaan, miten I-9-vahvistuksessa käytettäviä asiakirjatyyppejä tarkastellaan ja määritetään."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="55e61-103">Määritä I-9-asiakirjatyypit</span><span class="sxs-lookup"><span data-stu-id="55e61-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="55e61-104">Tässä menettelyssä kerrotaan, miten I-9-vahvistuksessa käytettäviä asiakirjatyyppejä tarkastellaan ja määritetään.</span><span class="sxs-lookup"><span data-stu-id="55e61-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="55e61-105">Ennen I-9-asiakirjatyyppien määrittämistä on määritettävä myöntävät tahot ja tunnistetyypit.</span><span class="sxs-lookup"><span data-stu-id="55e61-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="55e61-106">Tämän menettelyn luomisessa käytetään esittelytietojen USMF-yritystä. Tiedot sisältävät esimerkkejä menettelyn suorittamisessa tarvittavista myöntävistä tahoista ja tunnistetyypeistä.</span><span class="sxs-lookup"><span data-stu-id="55e61-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="55e61-107">Siirry kohtaan Henkilöstöhallinto > Työntekijät > I-9 > I-9-asiakirjatyypit.</span><span class="sxs-lookup"><span data-stu-id="55e61-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="55e61-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55e61-108">Click New.</span></span>
3. <span data-ttu-id="55e61-109">Syötä arvo I-9-asiakirjatyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55e61-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="55e61-110">Esimerkki: Koulun tunnus</span><span class="sxs-lookup"><span data-stu-id="55e61-110">Example: School ID.</span></span>  
4. <span data-ttu-id="55e61-111">Valitse tunnistustyyppi.</span><span class="sxs-lookup"><span data-stu-id="55e61-111">Select the identification type.</span></span>  <span data-ttu-id="55e61-112">Esimerkki: Koulun tunnus</span><span class="sxs-lookup"><span data-stu-id="55e61-112">Example:  School ID</span></span>
    * <span data-ttu-id="55e61-113">Henkilöllisyyden voi osoittaa henkilötunnus, viisuminumero, passin tunnus tai ajokortti.</span><span class="sxs-lookup"><span data-stu-id="55e61-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="55e61-114">Valitse I-9 asiakirjaluettelo, jota käytetään asiakirjatyypissä.</span><span class="sxs-lookup"><span data-stu-id="55e61-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="55e61-115">Työntekijöiden on näytettävä I-9-prosessin osana dokumentaatio, josta työntekijälle selviää henkilöllisyys ja työskentelylupa.</span><span class="sxs-lookup"><span data-stu-id="55e61-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="55e61-116">Yhdysvaltojen kansalaisuus- ja maahanmuuttopalvelujen Internet-sivusto sisältää tietoja hyväksyttävistä asiakirjoista ja siitä, mihin luetteloon ne kuuluvat.</span><span class="sxs-lookup"><span data-stu-id="55e61-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="55e61-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="55e61-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="55e61-118">Syötä Lomake-kenttään asiakirjatyypin virallinen lomakenumero.</span><span class="sxs-lookup"><span data-stu-id="55e61-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="55e61-119">Esimerkki: Koulun tunnus</span><span class="sxs-lookup"><span data-stu-id="55e61-119">Example: School ID.</span></span>
    * <span data-ttu-id="55e61-120">Viralliset lomakenumerot löytyvät Yhdysvaltojen kansalaisuus- ja maahanmuuttopalvelujen Internet-sivustosta.</span><span class="sxs-lookup"><span data-stu-id="55e61-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="55e61-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="55e61-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="55e61-122">Valitse Aktiivinen-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="55e61-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="55e61-123">Lisää Vanhenee-kenttään päivämäärä 27.10.2019.</span><span class="sxs-lookup"><span data-stu-id="55e61-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="55e61-124">Erääntymispäivämäärä on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="55e61-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="55e61-125">Valitse asiakirjatyypin myöntänyt taho.</span><span class="sxs-lookup"><span data-stu-id="55e61-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="55e61-126">Esimerkki: provinssi/alue</span><span class="sxs-lookup"><span data-stu-id="55e61-126">Example: Province/territory</span></span>
10. <span data-ttu-id="55e61-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="55e61-127">Click Save.</span></span>


