---
title: Kuljetustenhallinnan vyöhykkeen päätiedot
description: Tässä aiheessa käsitellään tapaa, jolla maantieteelliset sijainnit jaetaan kuljetustenhallinnassa vyöhykkeiksi.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6527c4887ccd3085d63dd64c104a94e6354f536b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996451"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="64319-103">Kuljetustenhallinnan vyöhykkeen päätiedot</span><span class="sxs-lookup"><span data-stu-id="64319-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64319-104">Kuljetustenhallinnassa maantieteelliset sijainnit voidaan jakaa vyöhykkeiksi.</span><span class="sxs-lookup"><span data-stu-id="64319-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="64319-105">Sijaintien jakamisesta vyöhykkeisiin on hyötyä seuraavissa:</span><span class="sxs-lookup"><span data-stu-id="64319-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="64319-106">**Kuljetuksen hinnoittelun yksinkertaistaminen** – vyöhyketietoinen hinnoittelu voi olla yksinkertaisempaa kuin sijaintiin perustuva hinnoittelu etenkin silloin, kun kuljetussijainnit ovat hajallaan.</span><span class="sxs-lookup"><span data-stu-id="64319-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="64319-107">**Kuormasuunnittelun optimointi** – kuormien konsolidointi vyöhykkeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="64319-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="64319-108">**Reittisuunnittelun optimointi** – tiettyjen reittisuunnitelmien määrittäminen tiettyihin vyöhykkeisiin.</span><span class="sxs-lookup"><span data-stu-id="64319-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="64319-109">Vyöhykkeet määritetään kunkin vyöhykkeen määrittävän metatietokentän arvojen perustella. Tällaisia arvoja ovat esimerkiksi maa, postinumeroalue tai rahdinkuljetuspalvelu.</span><span class="sxs-lookup"><span data-stu-id="64319-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="64319-110">Vyöhykemääritelmiä ei edellytetä, jos kuljetuksen hinnoittelussa ei käytetä vyöhykkeitä.</span><span class="sxs-lookup"><span data-stu-id="64319-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
