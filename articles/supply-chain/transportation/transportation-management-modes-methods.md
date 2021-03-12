---
title: Kuljetustenhallinnan tilat ja menetelmät
description: Tässä aiheessa käsitellään kuljetustenhallinnan tilojen ja menetelmien määrittämistä.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973907"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="a19a4-103">Kuljetustenhallinnan tilat ja menetelmät</span><span class="sxs-lookup"><span data-stu-id="a19a4-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a19a4-104">Kuljetustenhallinnan tila kuvaa kuljetustyyppiä, jota rahdinkuljettaja käyttää rahtitoimituksiin, kuten vähemmän kuin kuorma (LTL), rekkakuorma (TL) tai paketti.</span><span class="sxs-lookup"><span data-stu-id="a19a4-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="a19a4-105">Kuljetusmenetelmä edustaa sellaista kuljetusmuotoa, jota rahdinkuljettaja käyttää rahtitoimituksiin, kuten lento-, maa-, meri- tai rautatiekuljetus.</span><span class="sxs-lookup"><span data-stu-id="a19a4-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="a19a4-106">Tiloja ja kuljetusmenetelmiä käytetään useissa yhteyksissä.</span><span class="sxs-lookup"><span data-stu-id="a19a4-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="a19a4-107">Reittisuunnitelmissa käytetään vain tiloja, kun taas lähetyksen rahdinkuljettajien ja rahdinkuljettajapalvelujen määrittämiseen käytetään sekä tiloja että kuljetusmenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="a19a4-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="a19a4-108">Tilojen ja kuljetusmenetelmien välillä ei ole mitään nimenomaista suhdetta tai hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="a19a4-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="a19a4-109">Tilan luominen</span><span class="sxs-lookup"><span data-stu-id="a19a4-109">Create a mode</span></span>

<span data-ttu-id="a19a4-110">Tila luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a19a4-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="a19a4-111">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Tila**.</span><span class="sxs-lookup"><span data-stu-id="a19a4-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="a19a4-112">Luo uusi tila valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a19a4-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="a19a4-113">Anna tilalle yksilöivä tunnus ja kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="a19a4-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="a19a4-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a19a4-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="a19a4-115">Kuljetusmenetelmän luominen</span><span class="sxs-lookup"><span data-stu-id="a19a4-115">Create a transportation method</span></span>

<span data-ttu-id="a19a4-116">Kuljetusmenetelmä luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a19a4-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="a19a4-117">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Kuljetusmenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="a19a4-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="a19a4-118">Luo uusi kuljetusmenetelmä valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a19a4-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="a19a4-119">Anna kuljetusmenetelmälle yksilöivä tunnus ja kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="a19a4-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="a19a4-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a19a4-120">Close the page.</span></span>
