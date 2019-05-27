---
title: Konfiguraatiosäännöt
description: Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä. Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13f37cb4e472e91862e963a4952adcf61e6adcea
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555928"
---
# <a name="configuration-rules"></a><span data-ttu-id="52136-104">Konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="52136-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52136-105">Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä.</span><span class="sxs-lookup"><span data-stu-id="52136-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="52136-106">Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa.</span><span class="sxs-lookup"><span data-stu-id="52136-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="52136-107">Konfiguraatiosääntöjä voi käyttää määritettäessä dimensioihin perustuvia konfiguraatiomalleja.</span><span class="sxs-lookup"><span data-stu-id="52136-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="52136-108">Konfiguraatiosääntöjä käytetään joko tiettyjen nimikeyhdistelmien ottamiseksi käyttöön tai estämiseksi tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="52136-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="52136-109">Kun tuoterakenne on luotu ja sitä vastaavat nimikkeet on määritetty omiin konfiguraatioryhmiinsä, voidaan määrittää yksi tai useampi konfiguraatiosääntö.</span><span class="sxs-lookup"><span data-stu-id="52136-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="52136-110">Jos kaksi nimikettä kuuluu yhteen, sisällytys varmistetaan **Valitse**-operaattorilla.</span><span class="sxs-lookup"><span data-stu-id="52136-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="52136-111">Jos kaksi nimikettä kumoavat toisensa, poissulkeminen varmistetaan **Poista valinta** -operaattorilla.</span><span class="sxs-lookup"><span data-stu-id="52136-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="52136-112">**Huomautus:** Nämä tiedot koskevat vain päätuotteita, jotka käyttävät dimensioihin perustuvaa konfiguraatiomääritelmää.</span><span class="sxs-lookup"><span data-stu-id="52136-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="52136-113">Konfigurointisääntöjen muutokset eivät vaikuta aiemmin luotuihin konfiguraatioihin.</span><span class="sxs-lookup"><span data-stu-id="52136-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="52136-114">On kuitenkin tärkeää määrittää säännöt ennen uuden konfiguraation määrittämistä tai tarkistaa säännöt, jos ne saattavat olla muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="52136-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="52136-115">**Huomautus:** **Valitse**-menetelmä tarkoittaa, että johdettu konfigurointiryhmä, nimiketunnus ja konfiguraatio valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="52136-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="52136-116">**Poista valinta** -menetelmä tarkoittaa, että johdettua konfigurointiryhmää, nimiketunnusta ja konfiguraatiota ei voi valita.</span><span class="sxs-lookup"><span data-stu-id="52136-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="52136-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="52136-117">Additional resources</span></span>
--------

[<span data-ttu-id="52136-118">Dimensioon perustuva tuotekonfigurointi</span><span class="sxs-lookup"><span data-stu-id="52136-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)



