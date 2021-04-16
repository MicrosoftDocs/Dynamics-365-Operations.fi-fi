---
title: Puhelinkeskusten jatkuvuusohjelmien määrittäminen
description: Tässä artikkelissa kuvataan, miten voit määrittää jatkuvuusohjelman puhelinkeskukselle.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7f90e919133fd7443083261a325b285b3abb75b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791027"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="377bd-103">Puhelinkeskusten jatkuvuusohjelmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="377bd-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="377bd-104">Tässä artikkelissa kuvataan, miten voit määrittää jatkuvuusohjelman puhelinkeskukselle.</span><span class="sxs-lookup"><span data-stu-id="377bd-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="377bd-105">Jatkuvuusohjelmassa, joka tunnetaan myös toistuvan tilauksen ohjelmana, asiakkaat saavat tavalliset tuotelähetykset ennalta määritetyn maksusuunnitelman mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="377bd-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="377bd-106">Jokainen lähetys voi sisältää eri tuotteen, kuten kuukauden kirja -klubissa tai sama tuote voidaan lähettää toistuvasti.</span><span class="sxs-lookup"><span data-stu-id="377bd-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="377bd-107">Kun perustat jatkuvuusohjelman, tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="377bd-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="377bd-108">Määritä jatkuvuuden parametrit **Puhelinpalvelukeskuksen parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="377bd-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="377bd-109">Luo jatkuvuusohjelma, joka määrittää tiedot, kuten maksusuunnitelman, lähetysten ajoituksen ja sen tapahtuuko laskutus etukäteen.</span><span class="sxs-lookup"><span data-stu-id="377bd-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="377bd-110">Sinun on myös lisättävä luettelo tuotteista, jotka on sisällytetty jatkuvuusohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="377bd-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="377bd-111">Jokainen tuote saa tapahtuman tunnusnumeron, joka määritetään järjestyksessä numerosta 1 alkaen.</span><span class="sxs-lookup"><span data-stu-id="377bd-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="377bd-112">Tapahtumatunnus määrittää järjestyksen, jossa tuotteet lähetetään.</span><span class="sxs-lookup"><span data-stu-id="377bd-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="377bd-113">Jos asiakkaat vastaanottavat eri tuotteen kussakin lähetyksessä, tuotteet lähetetään numerojärjestyksessä niiden tapahtumatunnusten mukaan ja alkaen nykyisestä tapahtumasta.</span><span class="sxs-lookup"><span data-stu-id="377bd-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="377bd-114">Jos asiakkaat vastaanottavat saman tuotteen kussakin lähetyksessä, luettelo sisältää vain yhden tuotteen, jolla on yksi tapahtumatunnus.</span><span class="sxs-lookup"><span data-stu-id="377bd-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="377bd-115">Sama tapahtuma toteutuu toistuvasti.</span><span class="sxs-lookup"><span data-stu-id="377bd-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="377bd-116">Voit määrittää, kuinka monta kertaa jokainen tapahtuma toistetaan.</span><span class="sxs-lookup"><span data-stu-id="377bd-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="377bd-117">Luo ylätason tuote, joka edustaa tehtävässä 2 luomaasi jatkuvuusohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="377bd-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="377bd-118">Jos lisäät tämän tuotteen myyntitilaukseen, **Jatkuvuus**-sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="377bd-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="377bd-119">Tämän jälkeen voit käyttää tätä sivua luodaksesi varsinaisen jatkuvuustilauksen.</span><span class="sxs-lookup"><span data-stu-id="377bd-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="377bd-120">Ylätason tuote ei määritä yksittäisiä tuotteita, jotka asiakas vastaanottaa jokaisessa toimituksessa.</span><span class="sxs-lookup"><span data-stu-id="377bd-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="377bd-121">Sen jälkeen kun olet määrittänyt jatkuvuusohjelman yllä kuvatulla tavalla, voit luoda jatkuvuustilauksen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="377bd-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="377bd-122">Saatat ehkä joutua suorittamaan myös seuraavat ylläpitotehtävät:</span><span class="sxs-lookup"><span data-stu-id="377bd-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="377bd-123">**Päivitä nykyinen jatkuvuustapahtuman kausi**– Määritä komentojonotyö, joka kertoo järjestelmälle, mikä nykyisen tapahtuman kausi on.</span><span class="sxs-lookup"><span data-stu-id="377bd-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="377bd-124">**Luo jatkuvuuden alitilauksia** – Luo alitilauksia ylätason jatkuvuustilauksesta.</span><span class="sxs-lookup"><span data-stu-id="377bd-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="377bd-125">**Käsittele jatkuvuuden maksut** – Käsittele laskutus ja maksuhuomautukset, jotka liittyvät jatkuvuuden myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="377bd-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="377bd-126">**Laajenna jatkuvuusrivejä tarvittaessa** (jos tarpeellista) – Lisää jatkuvuustapahtuman toistokertojen määrää.</span><span class="sxs-lookup"><span data-stu-id="377bd-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="377bd-127">Lähetysten toisto voi jatkua asetettujen rajojen yli, jotka määritettiin **Jatkuvuuden toistuva kynnys** -kentässä puhelinkeskuksen parametreissä.</span><span class="sxs-lookup"><span data-stu-id="377bd-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="377bd-128">**Suorita jatkuvuuspäivitys** (tarvittaessa) – Synkronoi muutokset jatkuvuusohjelman ja jatkuvuuspäämyyntitilausten välillä.</span><span class="sxs-lookup"><span data-stu-id="377bd-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="377bd-129">**Sulje jatkuvuuden päärivit ja tilaukset** - Sulje jatkuvuustilaukset.</span><span class="sxs-lookup"><span data-stu-id="377bd-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]