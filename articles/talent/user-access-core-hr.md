---
title: Käyttäjä voi käyttää Core HR:ää, mutta ei Onboardia tai Attractia
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 Talent - Core HR:ää mutta ei Attractia tai Onboardia.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772916"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="f1679-103">Käyttäjä voi käyttää Core HR:ää, mutta ei Onboardia tai Attractia</span><span class="sxs-lookup"><span data-stu-id="f1679-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1679-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="f1679-104">**Environment details**</span></span>

- <span data-ttu-id="f1679-105">Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.</span><span class="sxs-lookup"><span data-stu-id="f1679-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="f1679-106">Käyttäjä A lisäsi käyttäjän B käyttäjäksi Microsoft Dynamics 365 Talent: Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="f1679-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="f1679-107">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="f1679-107">**Issue**</span></span>

<span data-ttu-id="f1679-108">Käyttäjä B voi käyttää Core HR:ää mutta ei Talent: Attract- tai Talent: Onboard -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="f1679-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="f1679-109">Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f1679-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="f1679-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="f1679-110">**Solution**</span></span>

<span data-ttu-id="f1679-111">Käyttäjälle B on määritettävä sen Microsoft Power Apps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="f1679-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="f1679-112">Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="f1679-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="f1679-113">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="f1679-113">**Long-term solution**</span></span>

<span data-ttu-id="f1679-114">Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="f1679-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
