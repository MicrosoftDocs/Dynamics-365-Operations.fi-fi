---
title: Työtilaustyypit
description: Tässä ohjeaiheessa selitetään työtilaustyypit käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6bdc9d226d8e1aa6960cac38b95b0245e46ee1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825587"
---
# <a name="work-order-types"></a><span data-ttu-id="2b600-103">Työtilaustyypit</span><span class="sxs-lookup"><span data-stu-id="2b600-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2b600-104">Työtilaustyyppejä käytetään työtilausten luokituksessa.</span><span class="sxs-lookup"><span data-stu-id="2b600-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="2b600-105">Sinulla voi esimerkiksi olla työtilauksia, jotka liittyvät ennakoivaan tai korjaavaan ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="2b600-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="2b600-106">Työtilaustyyppi määrittää liitoksen työtilauksen elinkaarimalliin.</span><span class="sxs-lookup"><span data-stu-id="2b600-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="2b600-107">Työtilauksen elinkaarimalli määrittää työtilauksen elinkaaritilat, jotka voidaan määrittää työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="2b600-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="2b600-108">(Esimerkkejä työtilausten elinkaaritiloista ovat **Luotu**, **Käynnissä** ja **Valmis**.)</span><span class="sxs-lookup"><span data-stu-id="2b600-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="2b600-109">Lisätietoja työtilausten elinkaaritiloista ja projektin vaiheista on kohdassa [Työtilauksen elinkaaren tilat](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="2b600-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="2b600-110">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Työtilaustyypit**.</span><span class="sxs-lookup"><span data-stu-id="2b600-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="2b600-111">Luo uusi työtilaustyyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2b600-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="2b600-112">Kirjoita **Työtilaustyyppi** -kenttään työtilaustyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="2b600-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="2b600-113">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2b600-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="2b600-114">Valitse elinkaarimalli **Työtilauksen elinkaarimalli** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2b600-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="2b600-115">Määritä **Yksi ylläpitotyöntekijä** -asetukseksi **Kyllä**, jos kaikki tämän tyypin työtilaukseen liittyvät työtilaustyöt ajoitetaan samalle kunnossapitotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="2b600-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="2b600-116">Valitse **Kustannustyyppi**-kentässä tarvittaessa **korjaava**, **ennaltaehkäisevä** tai **investointi**.</span><span class="sxs-lookup"><span data-stu-id="2b600-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="2b600-117">Kaikilla työtilauksen työtilaustöillä on oltava sama kustannustyyppi.</span><span class="sxs-lookup"><span data-stu-id="2b600-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="2b600-118">Määritä **Pakollinen**-osassa asetuksiksi **Kyllä**, jos haluat määrittää, mitkä vikaan liittyvät tai kunnossapitoon liittyvät tiedot lisätään tämäntyyppiseen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="2b600-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b600-119">**Pakollinen**-osan vaihtoehdot liittyvät **Työtilauksen elinkaaren tilat** -sivun **Vahvista**-pikavälilehteen(**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaaren tilat**).</span><span class="sxs-lookup"><span data-stu-id="2b600-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="2b600-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2b600-120">Select **Save**.</span></span>

![Työtilaustyypit](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]