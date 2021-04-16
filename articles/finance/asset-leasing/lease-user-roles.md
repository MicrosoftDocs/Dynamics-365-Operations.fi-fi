---
title: Vuokrasopimuksen käyttäjäroolien liittäminen
description: Tässä ohjeaiheessa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa. Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16719576dde73f096c0102a89c43cbc75594cc80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819839"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="422ae-104">Vuokrasopimuksen käyttäjäroolien liittäminen</span><span class="sxs-lookup"><span data-stu-id="422ae-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="422ae-105">Tässä ohjeaiheessa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa.</span><span class="sxs-lookup"><span data-stu-id="422ae-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="422ae-106">Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="422ae-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="422ae-107">Resurssin vuokrauksessa on kolme erilaista käyttäjäroolia.</span><span class="sxs-lookup"><span data-stu-id="422ae-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="422ae-108">Yksi rooli sopii vuokrasopimusten ylläpitämiseen, toinen vuokrasopimusten tarkasteluun ja kolmas vuokrasopimuksen tehtäviä suorittavalle vuokravirkailijalle.</span><span class="sxs-lookup"><span data-stu-id="422ae-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="422ae-109">Kullakin roolilla on tietyt käyttöoikeudet kaikilla vuokrauksen sivuilla, ja kukin käyttäjä voi tarkastella, luoda, muokata tai poistaa vuokrasopimuksia työtehtäviensä mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="422ae-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="422ae-110">Rooli</span><span class="sxs-lookup"><span data-stu-id="422ae-110">Role</span></span>           | <span data-ttu-id="422ae-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="422ae-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="422ae-112">Vuokrasopimuksen ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="422ae-112">Maintain Lease</span></span> | <span data-ttu-id="422ae-113">Tämän roolin käyttäjät voivat lisätä, muokata, poistaa ja tarkastella vuokrasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="422ae-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="422ae-114">Tämä rooli on suunniteltu päivittäiselle käyttäjälle, jonka tehtäviin kuuluu kuukausittaisten kirjauskansiovientien luominen ja kirjaaminen sekä uusien vuokrasopimusten lisääminen.</span><span class="sxs-lookup"><span data-stu-id="422ae-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="422ae-115">Tämä rooli mahdollistaa kaikkien resurssin vuokrauksen toimintojen käyttämisen.</span><span class="sxs-lookup"><span data-stu-id="422ae-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="422ae-116">Vuokrasopimuksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="422ae-116">View Lease</span></span>     | <span data-ttu-id="422ae-117">Tämän roolin käyttäjät voivat tarkastella vain vuokrasopimuksen tietueita ja aikatauluja sekä suorittaa raportteja.</span><span class="sxs-lookup"><span data-stu-id="422ae-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="422ae-118">He eivät voi luoda uusia vuokrasopimuksia, muokata olemassa olevia vuokrasopimuksia tai luoda kirjauskansiovientejä vuokrasopimuksille.</span><span class="sxs-lookup"><span data-stu-id="422ae-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="422ae-119">Rooli on tarkoitettu käyttäjille, joiden on vain tarkasteltava vuokrasopimuksia, vuokrasopimusten aikatauluja ja tapahtumia, joita vuokrasopimuksille tehdään.</span><span class="sxs-lookup"><span data-stu-id="422ae-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="422ae-120">Vuokravirkailija</span><span class="sxs-lookup"><span data-stu-id="422ae-120">Lease Clerk</span></span>    | <span data-ttu-id="422ae-121">Tämän roolin käyttäjät voivat vain luoda uusia vuokrasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="422ae-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="422ae-122">He eivät voi muokata tai poistaa olemassa olevia vuokrasopimuksia, tarkastella vuokrausaikatauluja tai kirjata leasingvuokrauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="422ae-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="422ae-123">Tämä rooli on suunniteltu käyttäjille, jotka syöttävät tietoja.</span><span class="sxs-lookup"><span data-stu-id="422ae-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="422ae-124">Noudattamalla näitä ohjeita voit määrittää käyttäjät resurssin vuokrauksessa.</span><span class="sxs-lookup"><span data-stu-id="422ae-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="422ae-125">Siirry kohtaan **Järjestelmänhallinta \> Suojaus \> Liitä käyttäjät rooleihin**.</span><span class="sxs-lookup"><span data-stu-id="422ae-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="422ae-126">Valitse **Vuokrasopimuksen ylläpitäminen**-, **Vuokravirkailija**- tai **Vuokrasopimuksen tarkasteleminen** -rooli ja valitse sitten **Manualainen liittäminen / sulje pois käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="422ae-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="422ae-127">Valitse rooliin liitettävä käyttäjä ja valitse sitten **Liitä rooliin**.</span><span class="sxs-lookup"><span data-stu-id="422ae-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]