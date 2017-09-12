---
title: Tietuemallien luominen
description: "Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa."
author: pvillads
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9b184800ce845fa046e0cae38392e07141378dbb
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="create-record-templates"></a><span data-ttu-id="c715c-103">Tietuemallien luominen</span><span class="sxs-lookup"><span data-stu-id="c715c-103">Create record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c715c-104">Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa.</span><span class="sxs-lookup"><span data-stu-id="c715c-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="c715c-105">Tietuemallien avulla voit luoda tietueita nopeammin Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="c715c-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c715c-106">Voit luoda tietuemalleja vain joillekin Microsoft Dynamics 365 for Finance and Operationsin tietuetyypeille.</span><span class="sxs-lookup"><span data-stu-id="c715c-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c715c-107">Esimerkki: **** Kuvittele, että syötät autonvuokrausta koskevia tietoja autonvuokrausyritykselle, joka sijaitsee San Franciscossa.</span><span class="sxs-lookup"><span data-stu-id="c715c-107">For example, **** imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="c715c-108">Koska suurin osa asiakkaista asuu todennäköisesti San Franciscon alueella, olisi mukavaa, jos voisit täyttää automaattisesti arvot kentille **Osavaltio**, **Maa** ja **Kaupunki** vuokrauslomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="c715c-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> <span data-ttu-id="c715c-109">**Huomautus:** Voit ottaa käyttöön malleja vain niillä Finance and Operationsin alueilla, joihin sinulla on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="c715c-109">**Note:** You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="c715c-110">Kaikkien mallien otsikot ovat kuitenkin näkyvissä, kun luot uuden tietueen. Ne näkyvät myös muille käyttäjille, jos luot kaikkien käyttäjien käytettävissä olevia malleja.</span><span class="sxs-lookup"><span data-stu-id="c715c-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="c715c-111">Varmista, että huomioit tämän nimetessäsi malleja.</span><span class="sxs-lookup"><span data-stu-id="c715c-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="c715c-112">Älä esimerkiksi käytä nimiä, jotka sisältävät sanan "komissio", jos yrityksen joidenkin työntekijöiden palkka perustuu komissioihin ja tämä on luottamuksellista tietoa.</span><span class="sxs-lookup"><span data-stu-id="c715c-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> <span data-ttu-id="c715c-113">Jos lomakkeella, johon sinulla on käyttöoikeus, on yksi tai useampia malleja ja yrität luoda uuden tietueen lomakkeella, näkyville avautuu **Valitse malli kohteelle** -sivu.</span><span class="sxs-lookup"><span data-stu-id="c715c-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="c715c-114">Kun valitset mallin luettelosta, järjestelmä luo uuden tietueen, joka sisältää valitsemaasi malliin perustuvat oletustiedot.</span><span class="sxs-lookup"><span data-stu-id="c715c-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="c715c-115">Jos et halua käyttää malleja uusien tietueiden luomiseen, valitse **Valitse malli kohteelle** -sivulla **Älä kysy uudelleen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="c715c-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="c715c-116">Voit tuoda mallinvalintaikkunan uudelleen näkyviin napsauttamalla mitä tahansa tietuetta hiiren kakkospainikkeella, kun valitset **Tietueen tiedot** ja tämän jälkeen **Näytä mallivalinta**.</span><span class="sxs-lookup"><span data-stu-id="c715c-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




