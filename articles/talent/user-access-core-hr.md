---
title: "Core HR:n käyttö onnistuu mutta Onboard- tai Attract-sovelluksen ei"
description: "Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 for Talent Core HR:ää mutta ei Attract- tai Onboard-sovellusta."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="cb3f3-103">Core HR:n käyttö onnistuu mutta Onboard- tai Attract-sovelluksen ei</span><span class="sxs-lookup"><span data-stu-id="cb3f3-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb3f3-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="cb3f3-104">**Environment details**</span></span>

- <span data-ttu-id="cb3f3-105">Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="cb3f3-106">Käyttäjä A lisäksi käyttäjän B Microsoft Dynamics 365 for Talent Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="cb3f3-107">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="cb3f3-107">**Issue**</span></span>

<span data-ttu-id="cb3f3-108">Käyttäjä B voi käyttää Core HR:ää mutta ei Talent: Attract- tai Talent: Onboard -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="cb3f3-109">Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="cb3f3-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="cb3f3-110">**Solution**</span></span>

<span data-ttu-id="cb3f3-111">Käyttäjälle B on määritettävä sen Microsoft PowerApps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="cb3f3-112">Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="cb3f3-113">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="cb3f3-113">**Long-term solution**</span></span>

<span data-ttu-id="cb3f3-114">Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Core HR:ään.</span><span class="sxs-lookup"><span data-stu-id="cb3f3-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

