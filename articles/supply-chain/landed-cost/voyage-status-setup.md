---
title: Matkan tilan määritys
description: Tässä aiheessa kuvataan, miten määritetään tila-arvot, joita käyttäjät voivat määrittää matkoille.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022105"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="d1a53-103">Matkan tilan määritys</span><span class="sxs-lookup"><span data-stu-id="d1a53-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1a53-104">**Matkan tilat** -sivulla voit määrittää niiden tila-arvojen joukon, jotka käyttäjät voivat määrittää matkoille.</span><span class="sxs-lookup"><span data-stu-id="d1a53-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="d1a53-105">Käyttäjät voivat määrittää matkan tila-arvoja kaikille matkan tasoille: matkat, kuljetuskontti, pakkaus, ostotilaus ja nimike (ostorivit ja siirtotilausrivit).</span><span class="sxs-lookup"><span data-stu-id="d1a53-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="d1a53-106">Niitä käytetään kahteen tarkoitukseen:</span><span class="sxs-lookup"><span data-stu-id="d1a53-106">They are used for two purposes:</span></span>

- <span data-ttu-id="d1a53-107">Matkan, kuljetuskontin, pakkauksen, ostotilauksen tai nimikkeen (ostorivit ja siirtotilausrivit) tilan ilmoittaminen käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="d1a53-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="d1a53-108">Voit rajoittaa kustannusalueen käyttöä estämällä muokkauksen tai poiston.</span><span class="sxs-lookup"><span data-stu-id="d1a53-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="d1a53-109">Voit määrittää matkojen tilat valitsemalla **Aiheutunut kustannus \> Määritys \> Matkojen tilat**.</span><span class="sxs-lookup"><span data-stu-id="d1a53-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="d1a53-110">Tällöin voit lisätä, poistaa ja muokata tiloja käyttämällä toimintoruudun painikkeita.</span><span class="sxs-lookup"><span data-stu-id="d1a53-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="d1a53-111">Kullakin kustannusalueella on oma matkatilojen joukkonsa ja hierarkiansa.</span><span class="sxs-lookup"><span data-stu-id="d1a53-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="d1a53-112">Siksi **Matkojen tilat** -sivun **Kustannusalue**-kentässä on ensin valittava se kustannusalue, jota halutaan tarkastella tai jolle halutaan luoda matkojen tiloja.</span><span class="sxs-lookup"><span data-stu-id="d1a53-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="d1a53-113">Määritä sitten kullekin matkan tilalle tarpeen mukaan seuraavassa taulukossa kuvatut kentät.</span><span class="sxs-lookup"><span data-stu-id="d1a53-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="d1a53-114">Huomaa, että myös järjestelmätapahtumat voivat muuttaa automaattisesti matkojen tiloja. Tällaisia tapahtumia ovat esimerkiksi säännöt, jotka on luotu jäljityksen hallintakeskuksella.</span><span class="sxs-lookup"><span data-stu-id="d1a53-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="d1a53-115">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d1a53-115">Field</span></span> | <span data-ttu-id="d1a53-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1a53-116">Description</span></span> |
|---|---|
| <span data-ttu-id="d1a53-117">Matkan tila</span><span class="sxs-lookup"><span data-stu-id="d1a53-117">Voyage status</span></span> | <span data-ttu-id="d1a53-118">Määritä matkan tilan nimi.</span><span class="sxs-lookup"><span data-stu-id="d1a53-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="d1a53-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1a53-119">Description</span></span> | <span data-ttu-id="d1a53-120">Anna matkan tilan kuvaus.</span><span class="sxs-lookup"><span data-stu-id="d1a53-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="d1a53-121">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="d1a53-121">Modify</span></span> | <span data-ttu-id="d1a53-122">Valitse tämä valintaruutu, jos käyttäjät saavat muokata matkoja, joilla on tämä tila.</span><span class="sxs-lookup"><span data-stu-id="d1a53-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="d1a53-123">Delete-näppäin</span><span class="sxs-lookup"><span data-stu-id="d1a53-123">Delete</span></span> | <span data-ttu-id="d1a53-124">Valitse tämä valintaruutu, jos käyttäjät saavat poistaa matkoja, joilla on tämä tila.</span><span class="sxs-lookup"><span data-stu-id="d1a53-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="d1a53-125">Pakollinen</span><span class="sxs-lookup"><span data-stu-id="d1a53-125">Mandatory</span></span> | <span data-ttu-id="d1a53-126">Valitse tämä valintaruutu, jos haluat tehdä matkan tilasta pakollisen siten, että sitä ei voi ohittaa.</span><span class="sxs-lookup"><span data-stu-id="d1a53-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="d1a53-127">Ylärakenne</span><span class="sxs-lookup"><span data-stu-id="d1a53-127">Parent</span></span> | <span data-ttu-id="d1a53-128">Tämän kentän avulla voit luoda hierarkian tila-arvoille.</span><span class="sxs-lookup"><span data-stu-id="d1a53-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="d1a53-129">Matkojen tiloja voidaan siirtää (joko manuaalisesti tai automaattisesti) vain alaspäin hierarkiasta eli päätilasta johonkin sen alitilaan.</span><span class="sxs-lookup"><span data-stu-id="d1a53-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="d1a53-130">Sinun tarvitsee määrittää vain ne tietyt matkojen tilat, joita organisaatiosi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d1a53-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="d1a53-131">Tyypillisiä matkojen tiloja ovat esimerkiksi *Vahvistettu*, *Tuotteet kuljetettavana*, *Vastaanotettu*, *Valmiina kustannuslaskentaan* ja *Kustannukset laskettu*.</span><span class="sxs-lookup"><span data-stu-id="d1a53-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="d1a53-132">Muitakin tiloja saattaa kuitenkin olla käytössä.</span><span class="sxs-lookup"><span data-stu-id="d1a53-132">However, other statuses might be present.</span></span>
