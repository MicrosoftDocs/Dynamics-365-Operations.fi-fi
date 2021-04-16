---
title: Organisaation mallinnushierarkioiden luominen B2B-organisaatioille
description: Tässä aiheessa kuvataan, miten luodaan organisaation mallinnushierarkioita B2B-organisaatioille.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799826"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="3431a-103">Organisaation mallinnushierarkioiden luominen B2B-organisaatioille</span><span class="sxs-lookup"><span data-stu-id="3431a-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3431a-104">Tässä aiheessa kuvataan, miten luodaan organisaation mallinnushierarkioita B2B-organisaatioille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="3431a-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3431a-105">Commerce headquarters -sovelluksessa liikekumppaniorganisaatioita edustavat asiakas- ja asiakashierarkiayksiköt.</span><span class="sxs-lookup"><span data-stu-id="3431a-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="3431a-106">Liikekumppaniorganisaatio ja sen käyttäjät esitetään asiakkaina, ja asiakashierarkioiden avulla nämä asiakkaat liitetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="3431a-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="3431a-107">Kun liikekumppanin pyyntö liittyä B2B-verkkokauppasivustoon hyväksytään, suoritetaan seuraavat toimenpiteet:</span><span class="sxs-lookup"><span data-stu-id="3431a-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="3431a-108">Järjestelmään luodaan kaksi uutta asiakastietuetta: liikekumppaniorganisaation **Tyyppi – organisaatio** -asiakastietue ja pyytäjän (eli liikekumppanin käyttäjä, joka lähetti pyynnön) **Tyyppi – henkilö** -asiakastietue.</span><span class="sxs-lookup"><span data-stu-id="3431a-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="3431a-109">Luodaan uusi asiakashierarkiatietue kohdassa **Asiakas \> Asiakashierarkia**.</span><span class="sxs-lookup"><span data-stu-id="3431a-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="3431a-110">Tietueella on seuraavat otsikko-ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="3431a-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="3431a-111">**Asiakashierarkian tunnus** – Asiakashierarkian yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="3431a-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="3431a-112">Tämä tunnus käyttää Commerce headquarters -parametrien Commercen jaetuissa parametreissa määritettyä numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="3431a-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="3431a-113">**Nimi** – Liikekumppanin organisaationimi, joka on määritetty rekisteröintipyynnössä.</span><span class="sxs-lookup"><span data-stu-id="3431a-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="3431a-114">**Tarkoitus** – Tämä ominaisuus on määritetty ennalta määritetylle arvolle **B2B-organisaatio**.</span><span class="sxs-lookup"><span data-stu-id="3431a-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="3431a-115">**Organisaatio** – Liikekumppanin asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="3431a-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="3431a-116">Seuraavassa on asiakashierarkiatietueen tiedot:</span><span class="sxs-lookup"><span data-stu-id="3431a-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="3431a-117">Pyytäjän asiakastietue on liitetty asiakashierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="3431a-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="3431a-118">Järjestelmänvalvojan rooli on liitetty pyytäjään.</span><span class="sxs-lookup"><span data-stu-id="3431a-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="3431a-119">Kun järjestelmänvalvoja lisää käyttäjiä B2B-sivuston liikekumppaniorganisaatioon, kullekin käyttäjälle luodaan uusi asiakastietue Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3431a-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="3431a-120">Tämä asiakastietue lisätään myös liikekumppanin asiakashierarkiatietueeseen, ja sen rooli on "käyttäjä".</span><span class="sxs-lookup"><span data-stu-id="3431a-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="3431a-121">Useimmissa tapauksissa hierarkian kaikkien asiakastietueiden vastaavat ominaisuuksien arvot pitäisi vastata toisiaan.</span><span class="sxs-lookup"><span data-stu-id="3431a-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="3431a-122">Esimerkiksi koska kaikkien liikekumppanien käyttäjien tulisi saada samanlaisia hintoja tuotteille, hintaryhmän ja siihen liittyvien konfiguraatioiden tulisi täsmätä.</span><span class="sxs-lookup"><span data-stu-id="3431a-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="3431a-123">Järjestelmä ei kuitenkaan pakota tämän yhdenmukaisuuden noudattamista.</span><span class="sxs-lookup"><span data-stu-id="3431a-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="3431a-124">Siksi relevantit Commerce headquarters -käyttäjät ovat vastuussa siitä, että ominaisuusarvot ja konfiguroinnit vastaavat toisiaan annetun hierarkian kaikille asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="3431a-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="3431a-125">Commerce headquarters -käyttäjät voivat tarkastella hierarkian kaikkien asiakastietueiden ominaisuusarvoja vierekkäisessä näkymässä.</span><span class="sxs-lookup"><span data-stu-id="3431a-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="3431a-126">Valitse asianmukaisen asiakastietueen ominaisuudet valitsemalla välilehtien nimet avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="3431a-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="3431a-127">Käyttäjät voivat tarkastella ja muokata ominaisuusarvoja suoraan tässä näkymässä.</span><span class="sxs-lookup"><span data-stu-id="3431a-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="3431a-128">Vaihtoehtoisesti voit ottaa järjestelmänvalvojan asiakastietueen kaikki arvot käyttöön kaikissa käyttäjäasiakastietueissa valitsemalla **Ohita**-vaihtoehdon asiakashierarkian tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="3431a-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3431a-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3431a-129">Additional resources</span></span>

[<span data-ttu-id="3431a-130">B2B-verkkokauppasivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3431a-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="3431a-131">Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa</span><span class="sxs-lookup"><span data-stu-id="3431a-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="3431a-132">Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="3431a-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="3431a-133">Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille</span><span class="sxs-lookup"><span data-stu-id="3431a-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]