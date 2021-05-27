---
title: Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia
description: Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026490"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="e71b6-103">Järjestelmänvalvojat eivät voi poistaa tilausten pitoja, koska heillä ei ole valtuuksia</span><span class="sxs-lookup"><span data-stu-id="e71b6-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="e71b6-104">Tietopankin numero: 4614642</span><span class="sxs-lookup"><span data-stu-id="e71b6-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="e71b6-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="e71b6-105">Symptoms</span></span>

<span data-ttu-id="e71b6-106">Järjestelmänvalvojat eivät voi poistaa myyntitilausten pitoja, ellei heillä ole tilauksen järjestyskoodissa määritettyä roolia.</span><span class="sxs-lookup"><span data-stu-id="e71b6-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="e71b6-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e71b6-107">Resolution</span></span>

<span data-ttu-id="e71b6-108">Joidenkin toimien, kuten myyntitilauksen pitojen poistamisen, käyttö perustuu liiketoimintakäytännön määritykseen.</span><span class="sxs-lookup"><span data-stu-id="e71b6-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="e71b6-109">Järjestelmänvalvojilla ei yleensä ole valtuuksia tämäntyyppisten toimintojen suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="e71b6-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="e71b6-110">Yleensä tietyn tehtävän suorittamiseen sovelletaan liiketoimintakäytäntöjä, ja vain organisaation tietyt henkilöt hyväksytään suorittamaan tämä tehtävä.</span><span class="sxs-lookup"><span data-stu-id="e71b6-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="e71b6-111">Esimerkkejä tällaisista ovat työnkulun hyväksynnän tuloksena tehtävät hyväksynnät sekä työnkulun konfiguraation tuloksena olevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="e71b6-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="e71b6-112">Vaikka tilausten pitoon ei ole liitetty työnkulkua, periaate on samanlainen.</span><span class="sxs-lookup"><span data-stu-id="e71b6-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="e71b6-113">Asianmukainen rooli määrittää organisaation tietyn henkilöryhmän, jolla on oikeus poistaa tilausten pito.</span><span class="sxs-lookup"><span data-stu-id="e71b6-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="e71b6-114">Tätä oikeutta ei välttämättä pidä myöntää kaikille järjestelmänvalvojille, koska se rikkoo määritettyä liiketoimintakäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e71b6-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
