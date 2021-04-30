---
title: Kulutyyppien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka kulutyypit määritetään resurssien vuokrauksessa.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880981"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="52330-103">Kulutyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52330-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52330-104">Tässä ohjeaiheessa kerrotaan, kuinka kulutyypit määritetään resurssien vuokrauksessa.</span><span class="sxs-lookup"><span data-stu-id="52330-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="52330-105">Kustannukset, joita ,maksuaikataulu ei sisällä, kutsutaan *kulukustannuksiksi*.</span><span class="sxs-lookup"><span data-stu-id="52330-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="52330-106">Esimerkkejä näistä kustannuksista ovat kiinteistöverot, yleiset ylläpitokustannukset ja vakuutuskulut.</span><span class="sxs-lookup"><span data-stu-id="52330-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="52330-107">Hallinnollisen kulutyypin lisääminen</span><span class="sxs-lookup"><span data-stu-id="52330-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="52330-108">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Kulutyypit**.</span><span class="sxs-lookup"><span data-stu-id="52330-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="52330-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="52330-109">Select **New**.</span></span>
3. <span data-ttu-id="52330-110">Anna soveltuviin kenttiin uusi kulutyyppi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="52330-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="52330-111">Tilien määrittäminen hallintokuluille</span><span class="sxs-lookup"><span data-stu-id="52330-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="52330-112">Seuraavaksi sinun tulee liittää tilit kulutyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="52330-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="52330-113">Näitä tilejä veloitetaan, kun kuluaikatauluviennit kirjataan.</span><span class="sxs-lookup"><span data-stu-id="52330-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="52330-114">Vastatili on määritetty **Toimeenpanokustannusten maksuaikataulu** -riveille jokaisessa vuokrasopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="52330-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="52330-115">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.</span><span class="sxs-lookup"><span data-stu-id="52330-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="52330-116">Valitse **Tilit**-välilehden **Toimeenpanokustannukset**-pikavälilehden **Kulutyyppi**-kentässä kulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="52330-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="52330-117">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="52330-117">Select **Add**.</span></span>
4. <span data-ttu-id="52330-118">Valitse **Kirjan tyyppi** -kentässä tyyppi, joka linkitetään hallinnollisiin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="52330-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52330-119">Samaan kulutiliin voi linkittää useita kirjatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="52330-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="52330-120">Määritä **Tkoodi**-kentässä, mihin vuokrasopimuksiin kirja kohdistetaan:</span><span class="sxs-lookup"><span data-stu-id="52330-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="52330-121">**Kaikki** – Kirja kohdistetaan kaikkiin vuokrasopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="52330-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="52330-122">**Ryhmä** – Kirja kohdistetaan tiettyyn vuokrasopimusryhmään.</span><span class="sxs-lookup"><span data-stu-id="52330-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="52330-123">**Taulukko** – Kirja kohdistetaan tiettyihin vuokrasopimuksiin.</span><span class="sxs-lookup"><span data-stu-id="52330-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="52330-124">Jos olet valinnut **Ryhmä** tai **Taulukko** **Tilikoodi**-kentässä, valitse tilinumero tai ryhmänumero **Tili-/ryhmänumero**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="52330-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="52330-125">Valitse asianmukaisten kenttien rahoitusleasingsopimuksen päätili ja käyttöleasingsopimuksen päätili.</span><span class="sxs-lookup"><span data-stu-id="52330-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="52330-126">Kun olet tehnyt nämä vaiheet, voit lisätä kuluja valitun vuokrasopimuksen **Toimeenpanokustannusten maksuaikataulu** -riveillä **Vuokrauksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="52330-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="52330-127">Vaihtoehtoisesti voit lisätä kuluja, kun luot uuden vuokrasopimuksen.</span><span class="sxs-lookup"><span data-stu-id="52330-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
