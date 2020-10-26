---
title: Huoltosopimusten ja projektien integrointi
description: Kun käsittelet huoltosopimuksia ja huoltosopimusrivejä, käytät tietoja, jotka on määritetty Projektinhallinta ja kirjanpito -osan alueissa.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578e4b9fe5ef487e999fd0de28d7566bad21fd89
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985580"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="5e54e-103">Huoltosopimusten ja projektien integrointi</span><span class="sxs-lookup"><span data-stu-id="5e54e-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5e54e-104">Kun käsittelet huoltosopimuksia ja huoltosopimusrivejä, käytät tietoja, jotka on määritetty seuraavissa **Projektinhallinta ja kirjanpito** -osan alueissa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="5e54e-105">Projektihinnat</span><span class="sxs-lookup"><span data-stu-id="5e54e-105">Project prices</span></span>

<span data-ttu-id="5e54e-106">Huoltosopimustapahtuman kustannus- ja myyntihinnat johdetaan kustannushinta-asetuksista, joita sovelletaan huoltosopimukseen liitettyyn projektiin.</span><span class="sxs-lookup"><span data-stu-id="5e54e-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="5e54e-107">Kustannus- ja myyntihinnat voidaan määrittää projekti-, työntekijä- ja luokkakohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="5e54e-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="5e54e-108">Projektin oikeellisuustarkistus</span><span class="sxs-lookup"><span data-stu-id="5e54e-108">Project validation</span></span>

<span data-ttu-id="5e54e-109">Huoltosopimusriville valittavissa olevia projekteja, työntekijöitä ja luokkia voidaan rajata **Projektinhallinta ja kirjanpito** -osan oikeellisuustarkistusasetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="5e54e-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="5e54e-110">Määrittämällä oikeellisuustarkistusasetuksia voit yhdistää työntekijöitä, projekteja ja luokkia ja määrittää niille käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="5e54e-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="5e54e-111">Projektirivin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5e54e-111">Project line properties</span></span>

<span data-ttu-id="5e54e-112">Rivin ominaisuus määritetään automaattisesti huoltosopimusriville.</span><span class="sxs-lookup"><span data-stu-id="5e54e-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="5e54e-113">Rivin ominaisuudet luodaan **Rivin ominaisuudet** -lomakkeella **Projektinhallinta ja kirjanpito** -osassa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="5e54e-114">Huoltosopimukseen määritetty rivin ominaisuus liitetään huoltosopimukseen valittuun projektiin ja lisätään sen jälkeen automaattisesti huoltosopimusriville.</span><span class="sxs-lookup"><span data-stu-id="5e54e-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="5e54e-115">Oletusvastatilit</span><span class="sxs-lookup"><span data-stu-id="5e54e-115">Default offset accounts</span></span>

<span data-ttu-id="5e54e-116">Jos kirjaat kulutapahtuman, tapahtumalle valitaan automaattisesti oletusarvoinen kulun vastatili.</span><span class="sxs-lookup"><span data-stu-id="5e54e-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="5e54e-117">Oletusarvoinen kulutili määritetään nykyiseen huoltosopimukseen liitetyssä projektissa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5e54e-118">Projektin luokat</span><span class="sxs-lookup"><span data-stu-id="5e54e-118">Project categories</span></span>

<span data-ttu-id="5e54e-119">Huoltosopimusriveille valittavissa olevat luokat määritetään **Tuoteluokat**-lomakkeella **Projektinhallinta ja kirjanpito** -osassa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="5e54e-120">Luokat, joiden <STRONG>Käytössä kirjauskansioissa</STRONG>- valintaruutu on valittuna <STRONG>Projekti</STRONG>-välilehdellä <STRONG>Projektiluokat</STRONG>-lomakkeessa, ovat valittavissa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="5e54e-121">Jos <STRONG>Luokat, jotka eivät ole käytössä</STRONG> -valintaruutu on valittuna <STRONG>Kirjauskansiot</STRONG> -välilehdellä <STRONG>Projektinhallinta ja kirjanpito</STRONG> -lomakkeessa, kaikki luokat ovat valittavissa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="5e54e-122">Projektiparametrit</span><span class="sxs-lookup"><span data-stu-id="5e54e-122">Project parameters</span></span>

<span data-ttu-id="5e54e-123">Jos **Poistetut työntekijät** -kenttä **Kirjauskansiot**-välilehdellä **Projektinhallinta ja kirjanpito** -lomakkeessa on valittuna, voit valita ei-aktiivisia ja aktiivisia työntekijöitä **Huoltosopimukset**- ja **Huoltotilaukset** -lomakkeissa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="5e54e-124">Lisäksi voit ottaa käyttöön **Aloitusaika**- ja **Päättymisaika**-kentät **Projekti**-välilehdellä **Huoltotilaukset**-lomakkeessa, jos haluat määrittää huoltotilausriveille aloitus- ja päättymisajat.</span><span class="sxs-lookup"><span data-stu-id="5e54e-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="5e54e-125">Aloitus- ja päättymisaikaominaisuuden ottaminen käyttöön huoltotilauksissa</span><span class="sxs-lookup"><span data-stu-id="5e54e-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="5e54e-126">Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="5e54e-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="5e54e-127">Valitse **Kirjauskansiot**-välilehti ja valitse sitten **Näytä aloitus-/ lopetusajat** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5e54e-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="5e54e-128">Napsauta **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Kirjauskansiot** \> **Kirjauskansioiden nimet**.</span><span class="sxs-lookup"><span data-stu-id="5e54e-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="5e54e-129">Valitse huoltotilaukseen liitetyn kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="5e54e-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="5e54e-130">Valitse **Yleinen**-välilehti ja valitse sitten **Näytä aloitus-/ lopetusajat** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5e54e-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5e54e-131">Valitse huoltotilauksen kirjauskansion nimi <STRONG>Tunti</STRONG>-kentässä <STRONG>Kirjauskansiot</STRONG>-välilehdellä <STRONG>Huoltohallinnan parametrit</STRONG> -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="5e54e-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





