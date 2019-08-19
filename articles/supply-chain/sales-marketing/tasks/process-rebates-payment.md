---
title: Käsittele ostohyvityksiä maksua varten
description: Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a05565d220c53d0f860a2c0569622b55c4021d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833869"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="6ab7d-103">Käsittele ostohyvityksiä maksua varten</span><span class="sxs-lookup"><span data-stu-id="6ab7d-103">Process rebates for payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ab7d-104">Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="6ab7d-105">Voit käyttää tätä opastusta USMF-demoyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="6ab7d-106">Opastuksen edellytyksenä on, että käytössä on vähintään yhden ostohyvitysvaatimuksen tila on Merkitse.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="6ab7d-107">Jos käytössä on USMF, suorita asiakkaiden ostohyvitysten luonti- ja käsittelyopastus ennen tämän opastuksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="6ab7d-108">Muunna ostohyvitysvaatimukset hyvityslaskuksi</span><span class="sxs-lookup"><span data-stu-id="6ab7d-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="6ab7d-109">Valitse Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-109">Go to All customers.</span></span>
2. <span data-ttu-id="6ab7d-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6ab7d-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6ab7d-112">Valitse toimintoruudussa Perintä.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="6ab7d-113">Valitse Selvitä tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="6ab7d-114">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-114">Click Functions.</span></span>
7. <span data-ttu-id="6ab7d-115">Valitse Ostohyvitysohjelma.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-115">Click Rebate program.</span></span>
    * <span data-ttu-id="6ab7d-116">Ostohyvitys-sivulla on luettelo ostohyvitysvaatimuksista, jotka olet käsitellyt asiakkaan ostohyvitystyötilassa ja joiden tila on Merkitse.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="6ab7d-117">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-117">Click Edit.</span></span>
    * <span data-ttu-id="6ab7d-118">Valitse hyvityslaskuun sisällytettävien vaatimusten Merkitse-valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="6ab7d-119">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-119">Click Functions.</span></span>
10. <span data-ttu-id="6ab7d-120">Valitse Luo hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-120">Click Create credit note.</span></span>
    * <span data-ttu-id="6ab7d-121">Avautuva sanoma ilmoittaa, että kirjauskansio on kirjattu. (Tämä on Myyntireskontran parametrit -sivulla määritetty myyntireskontran kulutuksen kirjauskansio.)</span><span class="sxs-lookup"><span data-stu-id="6ab7d-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="6ab7d-122">Tämän vuoksi todellinen velkasumma (hyvitys) siirretään asiakkaan saldoon.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="6ab7d-123">Asiakastiliä hyvitetään ja ostohyvitysohjelman jaksotusta on veloitettu.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="6ab7d-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-124">Close the page.</span></span>
12. <span data-ttu-id="6ab7d-125">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-125">Click Cancel.</span></span>
    * <span data-ttu-id="6ab7d-126">Sivu päivitetään näyttämään päivitykset.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="6ab7d-127">Valitse toimintoruudussa Perintä.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="6ab7d-128">Valitse Selvitä tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="6ab7d-129">Huomaa, että negatiivisen summan tapahtuma, joka ilmaisee ostohyvityksen kokonaismäärän ilman laskutusviitteen määrää, on lisätty asiakkaan saldoon.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="6ab7d-130">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="6ab7d-130">Click Cancel.</span></span>

