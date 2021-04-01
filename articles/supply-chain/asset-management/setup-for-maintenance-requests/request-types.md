---
title: Ylläpitopyynnön tyypit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitopyynnön tyypit määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4f622cda62cad13a8146cbc26bc2e5f1a45222
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261186"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="ddd13-103">Ylläpitopyynnön tyypit</span><span class="sxs-lookup"><span data-stu-id="ddd13-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ddd13-104">Ylläpitopyynnön tyyppejä käytetään ylläpitopyyntöjen luokittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="ddd13-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="ddd13-105">Sinulla voi esimerkiksi olla ylläpitopyyntötyyppejä, jotka liittyvät ennakoivaan ja korjaavaan ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="ddd13-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="ddd13-106">Tai sinulla voi olla erityinen ylläpitopyynnön tyyppi, jota käytetään resurssin korjauksen hallintaan (varastokorjaus).</span><span class="sxs-lookup"><span data-stu-id="ddd13-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="ddd13-107">Ylläpitopyynnön tyyppi määrittää liitoksen ylläpitopyynnön elinkaaren tilaryhmään (ylläpidon elinkaarimalli).</span><span class="sxs-lookup"><span data-stu-id="ddd13-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="ddd13-108">Ylläpitopyynnön elinkaarimallit määrittävät elinkaaritilat, jotka voidaan määrittää ylläpitopyynnölle.</span><span class="sxs-lookup"><span data-stu-id="ddd13-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="ddd13-109">(Esimerkkejä ylläpitopyynnön elinkaaren tiloista ovat **Luotu**,**Aktiivinen** ja **Päättynyt**.)</span><span class="sxs-lookup"><span data-stu-id="ddd13-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="ddd13-110">Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Ylläpitopyynnön tyypit**.</span><span class="sxs-lookup"><span data-stu-id="ddd13-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="ddd13-111">Luo ylläpitopyyntötyyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ddd13-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="ddd13-112">Kirjoita **Ylläpitopyynnön tyyppi** -kenttään ylläpitopyynnön tyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="ddd13-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="ddd13-113">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ddd13-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="ddd13-114">Valitse **Yleiset**-pikavälilehdessä **Ylläpitopyynnön elinkaarimalli** -kentässä ylläpitopyynnön elinkaarimalli.</span><span class="sxs-lookup"><span data-stu-id="ddd13-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="ddd13-115">Valitse **Työtilaustyyppi**-kentässä työtilauksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="ddd13-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="ddd13-116">Kun ylläpitopyyntö muunnetaan työtilaukseksi, työtilaus hakee automaattisesti työtilauksen tyypin, joka liittyy ylläpitopitopyynnön tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="ddd13-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="ddd13-117">Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön tyypit** -luettelosivusta.</span><span class="sxs-lookup"><span data-stu-id="ddd13-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Ylläpitopyyntöjen tyyppisivu](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]