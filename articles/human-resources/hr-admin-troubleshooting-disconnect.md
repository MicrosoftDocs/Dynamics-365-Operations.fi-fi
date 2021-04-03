---
title: Asiakasohjelma katkaisee yhteyden
description: Tässä artikkelissa kerrotaan, miten toimitaan, jos asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6808132e182ea6fed4fb0605fd07c008d208e89f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468176"
---
# <a name="client-disconnects"></a><span data-ttu-id="f21e7-103">Asiakasohjelma katkaisee yhteyden</span><span class="sxs-lookup"><span data-stu-id="f21e7-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f21e7-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="f21e7-104">**Environment details**</span></span> 

<span data-ttu-id="f21e7-105">Tämä ongelma voi esiintyä kaikissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="f21e7-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="f21e7-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="f21e7-106">**Symptom**</span></span> 

<span data-ttu-id="f21e7-107">Asiakkaan yhteys ympäristöön katkeaa tuntemattomasta syystä.</span><span class="sxs-lookup"><span data-stu-id="f21e7-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="f21e7-108">Asiakas saa jonkin seuraavista virhesanomista:</span><span class="sxs-lookup"><span data-stu-id="f21e7-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="f21e7-109">Yhteys on katkennut.</span><span class="sxs-lookup"><span data-stu-id="f21e7-109">We've lost your connection.</span></span> <span data-ttu-id="f21e7-110">Jatka työskentelyä valitsemalla Sulje.</span><span class="sxs-lookup"><span data-stu-id="f21e7-110">Click Close to continue working.</span></span>
- <span data-ttu-id="f21e7-111">Vaikuttaa siltä, että verkkoyhteys katkesi. Yritä uudelleen napsauttamalla Yritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f21e7-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="f21e7-112">**Varoitusmerkki**</span><span class="sxs-lookup"><span data-stu-id="f21e7-112">**Red flag**</span></span>

<span data-ttu-id="f21e7-113">Tämä ongelma ilmenee usein silloin, kun käyttäjät ovat käyttöönottovaiheessa, kun he vertailevat tietoja eri tuotanto-ja testiympäristöistä ja kun he unohtavat, että siirtyvät istuntojen välillä.</span><span class="sxs-lookup"><span data-stu-id="f21e7-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="f21e7-114">Tämä ongelma tulee esille todennäköisimmin, jos käyttäjät ovat tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="f21e7-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="f21e7-115">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="f21e7-115">**Issue**</span></span> 

<span data-ttu-id="f21e7-116">**Selaintyypit:** Google Chrome, Internet Explorer ja Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f21e7-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="f21e7-117">Microsoft Dynamics 365 Human Resources katkaisee käyttäjien yhteyden, kun samalla käyttäjällä on samanaikaisesti avoinna samassa selaintyypissä kaksi eri istuntoa.</span><span class="sxs-lookup"><span data-stu-id="f21e7-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="f21e7-118">(Esimerkki: käyttäjä A katsoo sekä ympäristöä 1 että ympäristöä 2 Chromessa.) Sillä ei ole merkitystä, onko käyttäjä avannut eri selainikkunoita tai välilehtiä.</span><span class="sxs-lookup"><span data-stu-id="f21e7-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="f21e7-119">Jos samoilla käyttäjän tunnistetiedoilla kirjaudutaan samanaikaisesti samassa selaintyypissä sekä ympäristöön 1 että ympäristöön 2, Human Resources katkaisee yhteyden toiseen istuntoon.</span><span class="sxs-lookup"><span data-stu-id="f21e7-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="f21e7-120">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="f21e7-120">**Solution**</span></span>

<span data-ttu-id="f21e7-121">Varmista, että kussakin selaintyypissä on aina avoinna vain yksi ympäristö.</span><span class="sxs-lookup"><span data-stu-id="f21e7-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="f21e7-122">Käyttäjät voivat avata useita saman ympäristön istuntoja (eli useita välilehtiä samassa selaimessa).</span><span class="sxs-lookup"><span data-stu-id="f21e7-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="f21e7-123">Jos käyttäjät haluavat siirtyä kahden ympäristön välillä samanaikaisesti, heidän on avattavat ympäristöt eri selaintyypissä.</span><span class="sxs-lookup"><span data-stu-id="f21e7-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="f21e7-124">(Esimerkki: käyttäjä A voi tarkastella ympäristöä 1 Chromessa ja ympäristöä 2 Microsoft Edgessä.)</span><span class="sxs-lookup"><span data-stu-id="f21e7-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]