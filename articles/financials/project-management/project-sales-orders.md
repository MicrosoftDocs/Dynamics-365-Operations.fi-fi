---
title: Projektin myyntitilaukset
description: Tässä ohjeaiheessa käsitellään projektiin perustuvia myyntitilauksia aika-ja materiaaliprojekteissa.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "976652"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="b04df-103">Aika- ja materiaaliprojektien myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="b04df-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="b04df-104">Tämä ohjeaihe kuvaa myyntitilauksen luomisen projektille.</span><span class="sxs-lookup"><span data-stu-id="b04df-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="b04df-105">Vain **aika- ja materiaali** -tyyppisille projekteille voidaan luoda myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="b04df-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="b04df-106">Jos aika- ja materiaaliprojektilla on useita rahoituslähteitä projektisopimuksessa, on otettava käyttöön **Salli myyntitilaukset projekteissa, joissa on useita rahoituslähteitä** -parametri **Projektinhallinnan ja kirjanpidon parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b04df-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="b04df-107">Tuki useiden rahoituslähteiden projektien myyntitilauksille on käytettävissä sovelluksen versiosta 10.0.2 lähtien.</span><span class="sxs-lookup"><span data-stu-id="b04df-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="b04df-108">Useita rahoituslähteitä sisältävien projektien myyntitilausten tuen parametri poistetaan huhtikuun 2020 julkaisuaallossa, minkä jälkeen toiminto on aina käytössä.</span><span class="sxs-lookup"><span data-stu-id="b04df-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="b04df-109">Voit luoda myyntitilauksia projektiin perustuen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="b04df-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="b04df-110">Siirry projektiin.</span><span class="sxs-lookup"><span data-stu-id="b04df-110">Go to the project itself.</span></span> <span data-ttu-id="b04df-111">Valitse toimintoruudussa **Hallinta > Nimiketehtävät > Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="b04df-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="b04df-112">Projektista luotuun myyntitilaukseen täytetään oletusarvoisesti projektin tiedot.</span><span class="sxs-lookup"><span data-stu-id="b04df-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="b04df-113">Jos projektisopimuksessa on enemmän kuin yksi rahoituslähde, rahoituslähde on valittava, jotta voit määrittää myyntitilauksen asiakkaan.</span><span class="sxs-lookup"><span data-stu-id="b04df-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="b04df-114">Jos projektissa on vain yksi rahoituslähde, asiakas määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b04df-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="b04df-115">Siirry **Kaikki myyntitilaukset** -luettelosivulle ja luo uusi myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="b04df-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="b04df-116">Myyntitilaukselle on valittava projekti.</span><span class="sxs-lookup"><span data-stu-id="b04df-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="b04df-117">Sen jälkeen, kun projekti on valittu, asiakas määritetään rahoituslähteestä tai täytyy valita rahoituslähde, jos projektisopimuksessa on useita rahoituslähteitä.</span><span class="sxs-lookup"><span data-stu-id="b04df-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

