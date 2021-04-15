---
title: Yleistä tietuemalleista
description: Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa.
author: pvillads
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d802d8bb86313dba512f52ec977b4dd18aa25c61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747534"
---
# <a name="record-templates-overview"></a><span data-ttu-id="9a7f9-103">Yleistä tietuemalleista</span><span class="sxs-lookup"><span data-stu-id="9a7f9-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a7f9-104">Tässä artikkelissa esitellään tietuemallien käsite ja tietuemallien käyttäminen tietoja jakavien tietueiden luomisessa.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="9a7f9-105">Tietuemallien avulla voit luoda tietueita nopeammin, mutta voit luoda tietuemalleja vain joillekin tietuetyypeille.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="9a7f9-106">Esimerkki: Kuvittele, että syötät autonvuokrausta koskevia tietoja autonvuokrausyritykselle, joka sijaitsee San Franciscossa.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="9a7f9-107">Koska suurin osa asiakkaista asuu todennäköisesti San Franciscon alueella, olisi mukavaa, jos voisit täyttää automaattisesti arvot kentille **Osavaltio**, **Maa** ja **Kaupunki** vuokrauslomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="9a7f9-108">Voit kohdistaa malleja vain alueisiin, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="9a7f9-109">Kaikkien mallien otsikot ovat kuitenkin näkyvissä, kun luot uuden tietueen. Ne näkyvät myös muille käyttäjille, jos luot kaikkien käyttäjien käytettävissä olevia malleja.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="9a7f9-110">Varmista, että huomioit tämän nimetessäsi malleja.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="9a7f9-111">Älä esimerkiksi käytä nimiä, jotka sisältävät sanan "komissio", jos yrityksen joidenkin työntekijöiden palkka perustuu komissioihin ja tämä on luottamuksellista tietoa.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="9a7f9-112">Jos lomakkeella, johon sinulla on käyttöoikeus, on yksi tai useampia malleja ja yrität luoda uuden tietueen lomakkeella, näkyville avautuu **Valitse malli kohteelle** -sivu.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="9a7f9-113">Kun valitset mallin luettelosta, järjestelmä luo uuden tietueen, joka sisältää valitsemaasi malliin perustuvat oletustiedot.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="9a7f9-114">Jos et halua käyttää malleja uusien tietueiden luomiseen, valitse **Valitse malli kohteelle** -sivulla **Älä kysy uudelleen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="9a7f9-115">Voit tuoda mallinvalintaikkunan uudelleen näkyviin napsauttamalla mitä tahansa tietuetta hiiren kakkospainikkeella, kun valitset **Tietueen tiedot** ja tämän jälkeen **Näytä mallivalinta**.</span><span class="sxs-lookup"><span data-stu-id="9a7f9-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]