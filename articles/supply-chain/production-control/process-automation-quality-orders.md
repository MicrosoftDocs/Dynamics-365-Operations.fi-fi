---
title: Prosessin automaation aktivoiminen laatutilausten luontia varten
description: Tämä aihe tarjoaa resursseja Power Automaten käyttämiseen liiketoimintaprosessien automatisointiin laatutilausten esimerkin avulla.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115180"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="eefe9-103">Prosessin automaation aktivoiminen laatutilausten luontia varten</span><span class="sxs-lookup"><span data-stu-id="eefe9-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="eefe9-104">Organisaatioiden tarve standardiprosessien automatisoinnissa, henkilökunnan kätevämpi vuorovaikutus sekä erilaisten tietojen käyttö ja liiketoimintaprosessien automaattinen ajaminen edellyttävät organisaatioiden välistä tiedonsiirtoa.</span><span class="sxs-lookup"><span data-stu-id="eefe9-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="eefe9-105">Ohjelmistorobotiikan (RPA) ja Microsoft Power Automaten avulla yritykset voivat käyttää koodittomia kokemuksia toistuvien prosessien automatisoimiseksi, mikä parantaa tehokkuutta ja tarkkuutta.</span><span class="sxs-lookup"><span data-stu-id="eefe9-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="eefe9-106">Supply Chain Managementin ladattavan automaatioratkaisun mallissa näytetään esimerkiksi, miten Power Automatea voidaan käyttää liiketoimintaprosessien automatisointiin laatutilausten avulla.</span><span class="sxs-lookup"><span data-stu-id="eefe9-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="eefe9-107">Voit ladata automaatioratkaisun mallin [tästä](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="eefe9-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="eefe9-108">Yleisiä tietoja tästä ominaisuudesta ja sen ominaisuuksista on seuraavassa videossa: [RPA:n käyttäminen laatutilausten luomiseen Dynamics 365 Supply Chain Managementissa](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="eefe9-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="eefe9-109">![Automaatioasetukset ja RPA](media/rpa-automation-options.png "Automaatioasetukset ja RPA")</span><span class="sxs-lookup"><span data-stu-id="eefe9-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="eefe9-110">Power Automate -ratkaisumalli sisältää pilvipalvelutyönkulun ja työpöytätyönkulun automaation, joka automatisoi laatutilausten luonnin Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="eefe9-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="eefe9-111">Automaation voi aloittaa vastauksena moniin tapahtumiin ja signaaleihin, mukaan lukien käyttäjän syötön tai konesignaalit (kuten esineiden Internet (IoT)).</span><span class="sxs-lookup"><span data-stu-id="eefe9-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="eefe9-112">*Q-Order* Power Application -esimerkki sisältyy ratkaisumalliin.</span><span class="sxs-lookup"><span data-stu-id="eefe9-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="eefe9-113">Sen avulla käyttäjä voi skannata nimikkeen QR-koodin, lisätä määrän ja liittää kuvia käyttämällä kameraa.</span><span class="sxs-lookup"><span data-stu-id="eefe9-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="eefe9-114">Mukana on ratkaisuparametreja, jotka määrittävät automaation tiettyä käyttötapausta varten tuotantolaitoksessa.</span><span class="sxs-lookup"><span data-stu-id="eefe9-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="eefe9-115">![Luo laatutilaus](media/rpa-create-quality-roder.png "Luo laatutilaus")</span><span class="sxs-lookup"><span data-stu-id="eefe9-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="eefe9-116">Täydellinen vaiheittainen opas siitä, kuinka ladataan, asennetaan ja käytetään malliratkaisua tilausten laadun automatisointiin, on kohdassa [Automaattisen laatutilauksen luominen Dynamics 365 Supply Chain Managementissa ohjelmistorobotiikan avulla käyttäen Power Automate Desktopia](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="eefe9-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

