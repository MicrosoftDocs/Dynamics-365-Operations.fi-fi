---
title: Kuljetustenhallinnan muut kulut
description: Tässä aiheessa käsitellään kuljetuksesta syntyviä kuluja, joihin on liitettävä kulukoodi
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 53c25f204e98a911e9697f5bb950706555749a55
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828308"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="4e28d-103">Kuljetustenhallinnan muut kulut</span><span class="sxs-lookup"><span data-stu-id="4e28d-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e28d-104">Muiden kulujen tavoin kuljetuksesta syntyviin kuluihin on liitettävä kulukoodi.</span><span class="sxs-lookup"><span data-stu-id="4e28d-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="4e28d-105">Muussa tapauksessa niitä ei lisätä takaisin tilaukseen muina kuluina.</span><span class="sxs-lookup"><span data-stu-id="4e28d-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="4e28d-106">**Kulujen koodi** määrittää, miten kulut käsitellään suhteessa tilaukseen ja tilausriviin, jossa se lisättiin.</span><span class="sxs-lookup"><span data-stu-id="4e28d-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="4e28d-107">Valitsemalla **Kuljetuksenhallinta > Määritys > Luokitus > Muut kulut** voit määrittää ehdot, joiden mukaan määritetään, milloin **kulujen koodia** käytetään kuluun.</span><span class="sxs-lookup"><span data-stu-id="4e28d-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="4e28d-108">Kullekin sopivalle **Kulumoduuli**-asetukselle (*Asiakas* ja *Toimittaja*) on oltava vähintään yksi määritys, jossa **Muun kulun tyyppi** -asetuksena on *Ei mitään*.</span><span class="sxs-lookup"><span data-stu-id="4e28d-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="4e28d-109">Jos tämä puuttuu, muuta kulua *ei* lisätä tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="4e28d-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]