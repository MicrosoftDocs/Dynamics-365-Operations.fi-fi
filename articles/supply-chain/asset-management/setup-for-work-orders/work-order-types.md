---
title: Työtilaustyypit
description: Tässä ohjeaiheessa selitetään työtilaustyypit käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888782"
---
# <a name="work-order-types"></a><span data-ttu-id="4bd84-103">Työtilaustyypit</span><span class="sxs-lookup"><span data-stu-id="4bd84-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4bd84-104">Työtilaustyyppejä käytetään työtilausten luokituksessa.</span><span class="sxs-lookup"><span data-stu-id="4bd84-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="4bd84-105">Sinulla voi esimerkiksi olla työtilauksia, jotka liittyvät ennakoivaan tai korjaavaan ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="4bd84-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="4bd84-106">Työtilaustyyppi määrittää liitoksen työtilauksen elinkaarimalliin.</span><span class="sxs-lookup"><span data-stu-id="4bd84-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="4bd84-107">Työtilauksen elinkaarimalli määrittää työtilauksen elinkaaritilat, jotka voidaan määrittää työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="4bd84-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="4bd84-108">(Esimerkkejä työtilausten elinkaaritiloista ovat **Luotu**, **Käynnissä**ja **Valmis**.)</span><span class="sxs-lookup"><span data-stu-id="4bd84-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="4bd84-109">Lisätietoja työtilausten elinkaaritiloista ja projektin vaiheista on kohdassa [Työtilauksen elinkaaren tilat](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="4bd84-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="4bd84-110">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Työtilaustyypit**.</span><span class="sxs-lookup"><span data-stu-id="4bd84-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="4bd84-111">Luo uusi työtilaustyyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4bd84-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="4bd84-112">Kirjoita **Työtilaustyyppi** -kenttään työtilaustyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="4bd84-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="4bd84-113">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4bd84-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="4bd84-114">Valitse elinkaarimalli **Työtilauksen elinkaarimalli** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4bd84-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="4bd84-115">Määritä **Yksi ylläpitotyöntekijä** -asetukseksi **Kyllä**, jos kaikki tämän tyypin työtilaukseen liittyvät työtilaustyöt ajoitetaan samalle kunnossapitotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="4bd84-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="4bd84-116">Valitse**Kustannustyyppi**-kentässä tarvittaessa **korjaava**, **ennaltaehkäisevä** tai **investointi**.</span><span class="sxs-lookup"><span data-stu-id="4bd84-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="4bd84-117">Kaikilla työtilauksen työtilaustöillä on oltava sama kustannustyyppi.</span><span class="sxs-lookup"><span data-stu-id="4bd84-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="4bd84-118">Määritä **Pakollinen**-osassa asetuksiksi **Kyllä**, jos haluat määrittää, mitkä vikaan liittyvät tai kunnossapitoon liittyvät tiedot lisätään tämäntyyppiseen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="4bd84-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bd84-119">**Pakollinen**-osan vaihtoehdot liittyvät **Työtilauksen elinkaaren tilat** -sivun **Vahvista**-pikavälilehteen(**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaaren tilat**).</span><span class="sxs-lookup"><span data-stu-id="4bd84-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="4bd84-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4bd84-120">Select **Save**.</span></span>

![Työtilaustyypit](media/16-setup-for-work-orders.png)
