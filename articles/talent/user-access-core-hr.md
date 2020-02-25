---
title: Käyttäjä voi käyttää henkilöstöhallintosovellusta, mutta ei Onboardia tai Attractia
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, jossa käyttäjä voi käyttää Microsoft Dynamics 365 Talent - Human Resourcesia mutta ei Attractia tai Onboardia.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006307"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="78f5e-103">Käyttäjä voi käyttää henkilöstöhallintosovellusta, mutta ei Onboardia tai Attractia</span><span class="sxs-lookup"><span data-stu-id="78f5e-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78f5e-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="78f5e-104">**Environment details**</span></span>

- <span data-ttu-id="78f5e-105">Käyttäjä A vastasi Microsoft Dynamics Lifecycle Servicesin (LCS) käyttöönotosta.</span><span class="sxs-lookup"><span data-stu-id="78f5e-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="78f5e-106">Käyttäjä A lisäsi käyttäjän B käyttäjäksi Microsoft Dynamics 365 Human Resources:ään.</span><span class="sxs-lookup"><span data-stu-id="78f5e-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="78f5e-107">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="78f5e-107">**Issue**</span></span>

<span data-ttu-id="78f5e-108">Käyttäjä B voi käyttää Human Resourcesia mutta ei Talent: Attract- tai Talent: Onboard -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="78f5e-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="78f5e-109">Jos käyttäjä yrittää siirtyä **sovelluskokemukseen**, hän siirtyykin kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="78f5e-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="78f5e-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="78f5e-110">**Solution**</span></span>

<span data-ttu-id="78f5e-111">Käyttäjälle B on määritettävä sen Microsoft Power Apps -ympäristön tarkasteluoikeudet, jonka käyttäjä A loi valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="78f5e-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="78f5e-112">Lisätietoja on kohdan [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) osassa Ympäristön käyttöoikeuksien myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="78f5e-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="78f5e-113">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="78f5e-113">**Long-term solution**</span></span>

<span data-ttu-id="78f5e-114">Microsoft harkitsee soveltuvien Onboard- ja Attract-oikeuksien määrittämistä automaattisesti, kun käyttäjä lisätään Human Resourceen.</span><span class="sxs-lookup"><span data-stu-id="78f5e-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
