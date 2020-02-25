---
title: Sähköisen kaupankäynnin käyttäjien ja roolien hallinta
description: Tässä ohjeaiheessa kerrotaan, kuinka voit myöntää käyttäjille Microsoft Dynamics 365 Commerce -sivuston muokkausympäristön käyttöoikeudet.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003530"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="4ea9d-103">Sähköisen kaupankäynnin käyttäjien ja roolien hallinta</span><span class="sxs-lookup"><span data-stu-id="4ea9d-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4ea9d-104">Tässä ohjeaiheessa kerrotaan, kuinka voit myöntää käyttäjille Microsoft Dynamics 365 Commerce -sivuston muokkausympäristön käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="4ea9d-105">Sivuston muokkausympäristössä käytetään Microsoft Azure Active Directoryssä (Azure AD) luomiasi käyttöoikeusryhmiä, joiden avulla voit hallita käyttäjien käyttöoikeuksia ja myöntää käyttäjille oikeuden suorittaa tiettyjä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="4ea9d-106">Määritä ensin uusi tai olemassa oleva käyttöoikeusryhmä Azure AD:sta jokaiselle muokkausympäristön roolille.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="4ea9d-107">Tämän jälkeen voit myöntää käyttöoikeudet yksittäisille käyttäjille tai peruuttaa ne lisäämällä kyseiset käyttäjät asianmukaiseen käyttöoikeusryhmään tai poistamalla heidät käyttöoikeusryhmästä.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="4ea9d-108">Tietoja muokkausympäristön rooleista</span><span class="sxs-lookup"><span data-stu-id="4ea9d-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="4ea9d-109">Dynamics 365 for Commercen muokkausympäristö tukee seuraavia rooleja.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="4ea9d-110">Rooli</span><span class="sxs-lookup"><span data-stu-id="4ea9d-110">Role</span></span>                 | <span data-ttu-id="4ea9d-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ea9d-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="4ea9d-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="4ea9d-112">System Administrator</span></span> | <span data-ttu-id="4ea9d-113">Käyttäjillä, joilla on tämä rooli, on kaikki oikeudet kaikkiin työkaluihin sekä kaikkiin luokituksiin ja arvosteluihin.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="4ea9d-114">He voivat myös luoda sivustoja.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-114">They can also create sites.</span></span> |
| <span data-ttu-id="4ea9d-115">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="4ea9d-115">Administrator</span></span>   | <span data-ttu-id="4ea9d-116">Käyttäjillä, joilla on tämä rooli, on kaikki tietyn sivuston rakenteen työkalujen ja RnR:n oikeudet.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="4ea9d-117">Verkon tuottaja</span><span class="sxs-lookup"><span data-stu-id="4ea9d-117">Web Producer</span></span>         | <span data-ttu-id="4ea9d-118">Käyttäjät, joilla on tämä rooli, voivat luoda sivuja, osia ja malleja, ladata ja hallita resursseja sekä täydentää tuotteita ja luokkia.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="4ea9d-119">Lukija</span><span class="sxs-lookup"><span data-stu-id="4ea9d-119">Reader</span></span>               | <span data-ttu-id="4ea9d-120">Käyttäjät, joilla on tämä rooli, voivat tarkastella sivuja, malleja, resursseja, osia, asetteluja ja asetuksia, mutta he eivät välttämättä voi tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="4ea9d-121">RnR-valvoja</span><span class="sxs-lookup"><span data-stu-id="4ea9d-121">RnR Moderator</span></span>        | <span data-ttu-id="4ea9d-122">Käyttäjät, joilla on tämä rooli, voivat valvoa tuotearvosteluita.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="4ea9d-123">Järjestelmänvalvojan rooli</span><span class="sxs-lookup"><span data-stu-id="4ea9d-123">System Administrator role</span></span>

<span data-ttu-id="4ea9d-124">Kun Dynamics 365 Commerce valmistellaan Microsoft Dynamics Lifecycle Services (LCS) -ympäristössä, sinua pyydetään antamaan käyttöoikeusryhmä **järjestelmänvalvojan** roolille.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="4ea9d-125">Tämän jälkeen tätä roolia käytetään automaattisesti kaikissa sivustoissa, jotka luot määritettävässä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="4ea9d-126">Tämän roolin käyttöoikeusryhmän voi päivittää vain LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="4ea9d-127">Se näkyy **Sivuston hallinta** -sivuilla kaikissa sivustoissa vain luku -muodossa. Se on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="4ea9d-128">Valvojan rooli</span><span class="sxs-lookup"><span data-stu-id="4ea9d-128">Administrator role</span></span>

<span data-ttu-id="4ea9d-129">Kun luotu uuden sivuston Commercessa, sinua pyydetään antamaan käyttöoikeusryhmä **valvojan** roolille.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="4ea9d-130">Tämän roolin myöntämien oikeuksien yleiskatsaus on tämän ohjeaiheen aiemmassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="4ea9d-131">Käyttöoikeusryhmien lisääminen tai päivittäminen</span><span class="sxs-lookup"><span data-stu-id="4ea9d-131">Add or update security groups</span></span>

<span data-ttu-id="4ea9d-132">Kun sivusto on määritetty, vain käyttöoikeusryhmään kuuluvat käyttäjät, jotka on liitetty **järjestelmänvalvojan** ja **valvojan** rooleihin, voivat käyttää sivuston muokkausympäristöä.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="4ea9d-133">Jos haluat määrittää käyttäjät **verkon tuottajan**, **RnR-valvojan** ja **lukijan** rooleille, sinun on liitettävä näille rooleille käyttöoikeusryhmät.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="4ea9d-134">Voit lisätä käyttöoikeusryhmän rooliin tai päivittää käyttöoikeusryhmän, joka on tällä hetkellä määritetty roolille, seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="4ea9d-135">Siirry päivitettävälle sivustolle.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="4ea9d-136">Avaa **sivuston hallinnassa** **Suojaus**-sivu.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="4ea9d-137">Valitse muokattava rooli.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-137">Select the role to modify.</span></span>
1. <span data-ttu-id="4ea9d-138">Lisää käyttöoikeusryhmät rooleihin tai poista ne rooleista.</span><span class="sxs-lookup"><span data-stu-id="4ea9d-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ea9d-139">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4ea9d-139">Additional resources</span></span>

[<span data-ttu-id="4ea9d-140">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="4ea9d-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="4ea9d-141">Sivuston hakukoneoptimointia (SEO) koskevia tietoja</span><span class="sxs-lookup"><span data-stu-id="4ea9d-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="4ea9d-142">Sisällön suojauskäytännön (CSP) hallinta</span><span class="sxs-lookup"><span data-stu-id="4ea9d-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
