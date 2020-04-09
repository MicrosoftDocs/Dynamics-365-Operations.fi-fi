---
title: Määritä tuotantovirran versiolle viimeinen myyntipäivä
description: Tuotantovirran version voimassaolon ja käsittelyn voi päättää tiettynä päivänä asettamalla versiolle vanhentumispäivän. Sama pätee aktiivisen version korvaamiseen uudella versiolla.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8df396abc3ac4a2c3920e6bf2b21d8a4463df2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146856"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="6f46b-103">Määritä tuotantovirran versiolle viimeinen myyntipäivä</span><span class="sxs-lookup"><span data-stu-id="6f46b-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f46b-104">Tuotantovirran version voimassaolon ja käsittelyn voi päättää tiettynä päivänä asettamalla versiolle vanhentumispäivän. Sama pätee aktiivisen version korvaamiseen uudella versiolla.</span><span class="sxs-lookup"><span data-stu-id="6f46b-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="6f46b-105">Versiota ei ole tarpeen poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6f46b-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="6f46b-106">Vanhentumispäivän määrittäminen tuotantovirran version päättämiseksi</span><span class="sxs-lookup"><span data-stu-id="6f46b-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="6f46b-107">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="6f46b-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6f46b-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6f46b-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f46b-109">Valitse tuotantovirta, jolla on jo määritelty versio.</span><span class="sxs-lookup"><span data-stu-id="6f46b-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="6f46b-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6f46b-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6f46b-111">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="6f46b-111">Click Edit.</span></span>
5. <span data-ttu-id="6f46b-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6f46b-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6f46b-113">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f46b-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="6f46b-114">Vanhentumispäivästä alkaen uusi versio ei käynnisty tai aktivoidu.</span><span class="sxs-lookup"><span data-stu-id="6f46b-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="6f46b-115">Töiden käynnistäminen tai luonti tähän tuotantovirtaan ei ole myöskään enää mahdollista.</span><span class="sxs-lookup"><span data-stu-id="6f46b-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="6f46b-116">Käynnistetyt työt voi saattaa valmiiksi vanhentumispäivän jälkeenkin.</span><span class="sxs-lookup"><span data-stu-id="6f46b-116">You can still complete started jobs after the expiration date.</span></span>  

