---
title: Konfiguraatiosäännöt
description: Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä. Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0eb925253962df6c85e935b8d8e53d93af38c16
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208567"
---
# <a name="configuration-rules"></a><span data-ttu-id="64c8c-104">Konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="64c8c-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64c8c-105">Tässä artikkelissa on yleistietoja konfiguraatiosäännöistä.</span><span class="sxs-lookup"><span data-stu-id="64c8c-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="64c8c-106">Konfiguraatiosäännöt määrittävät sellaisten tuotteiden tuoterakenteen nimikkeiden väliset suhteet, jotka käyttävät dimensioihin perustuvaa konfiguraatiotekniikkaa.</span><span class="sxs-lookup"><span data-stu-id="64c8c-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="64c8c-107">Konfiguraatiosääntöjä voi käyttää määritettäessä dimensioihin perustuvia konfiguraatiomalleja.</span><span class="sxs-lookup"><span data-stu-id="64c8c-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="64c8c-108">Konfiguraatiosääntöjä käytetään joko tiettyjen nimikeyhdistelmien ottamiseksi käyttöön tai estämiseksi tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="64c8c-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="64c8c-109">Kun tuoterakenne on luotu ja sitä vastaavat nimikkeet on määritetty omiin konfiguraatioryhmiinsä, voidaan määrittää yksi tai useampi konfiguraatiosääntö.</span><span class="sxs-lookup"><span data-stu-id="64c8c-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="64c8c-110">Jos kaksi nimikettä kuuluu yhteen, sisällytys varmistetaan **Valitse**-operaattorilla.</span><span class="sxs-lookup"><span data-stu-id="64c8c-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="64c8c-111">Jos kaksi nimikettä kumoavat toisensa, poissulkeminen varmistetaan **Poista valinta** -operaattorilla.</span><span class="sxs-lookup"><span data-stu-id="64c8c-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="64c8c-112">**Huomautus:** Nämä tiedot koskevat vain päätuotteita, jotka käyttävät dimensioihin perustuvaa konfiguraatiomääritelmää.</span><span class="sxs-lookup"><span data-stu-id="64c8c-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="64c8c-113">Konfigurointisääntöjen muutokset eivät vaikuta aiemmin luotuihin konfiguraatioihin.</span><span class="sxs-lookup"><span data-stu-id="64c8c-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="64c8c-114">On kuitenkin tärkeää määrittää säännöt ennen uuden konfiguraation määrittämistä tai tarkistaa säännöt, jos ne saattavat olla muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="64c8c-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="64c8c-115">**Huomautus:** **Valitse**-menetelmä tarkoittaa, että johdettu konfigurointiryhmä, nimiketunnus ja konfiguraatio valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="64c8c-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="64c8c-116">**Poista valinta** -menetelmä tarkoittaa, että johdettua konfigurointiryhmää, nimiketunnusta ja konfiguraatiota ei voi valita.</span><span class="sxs-lookup"><span data-stu-id="64c8c-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="64c8c-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="64c8c-117">Additional resources</span></span>
--------

[<span data-ttu-id="64c8c-118">Dimensioihin perustuvat tuotekonfiguraatiot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64c8c-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)



