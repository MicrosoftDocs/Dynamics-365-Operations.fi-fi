---
title: SQL Server Reporting Servicesin määrittäminen paikallisissa käyttöönotoissa
description: Tässä ohjeaiheessa on tietoja SQL Server Reporting Servicesin (SSRS) määrittämisestä paikallista käyttöönottoa varten.
author: PeterRFriis
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: e3acd96e686260da3ed67b8ac823be45b8ea870f
ms.sourcegitcommit: 708b3966b1c2bd4999f528d4a03a89d9bb530616
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100495"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="9f9a8-103">SQL Server Reporting Servicesin määrittäminen paikallisissa käyttöönotoissa</span><span class="sxs-lookup"><span data-stu-id="9f9a8-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f9a8-104">Määritä Microsoft Dynamics 365 Finance + Operationsin (paikallinen) käyttöönoton SQL Server Reporting Services (SSRS) tämän ohjeaiheen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="9f9a8-105">Avaa Reporting Services -määritystenhallintasovellus</span><span class="sxs-lookup"><span data-stu-id="9f9a8-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="9f9a8-106">Jätä oletusarvoinen **Palvelimen nimi**, jonka pitäisi olla nykyisen laitteen nimi, ja **Report Server -esiintymä**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="9f9a8-107">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-107">Click **Connect**.</span></span>

    <span data-ttu-id="9f9a8-108">[![Reporting Servicesin määritysyhteys](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="9f9a8-109">Valitse **Palvelutili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-110">[![Palvelutili-välilehti](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="9f9a8-111">Valitse **Internet-palvelun URL**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-112">[![Internet-palvelun URL -välilehti](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="9f9a8-113">Valitse **Tietokanta**-välilehti ja tarkista, että **Tietokannan nimi** ja **Tunnistetietojen asetukset** ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f9a8-114">Sinun on luotava uusi tietokanta.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-114">You will need to create a new database.</span></span> <span data-ttu-id="9f9a8-115">Tee se valitsemalla **Muuta tietokantaa** ja tarkista sitten, että uuden tietokannan nimi on **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="9f9a8-116">[![tietokanta-välilehti](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="9f9a8-117">Valitse **Internet-portaalin URL** -välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f9a8-118">Sinun on valittava **Käytä**, jotta voit luoda ja määrittää portaalin oikein.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="9f9a8-119">[![Internet-portaalin url -välilehti](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="9f9a8-120">Kun portaali on määritetty, **Internet-portaali**-välilehden on vastattava seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-121">[![Internet-portaali-välilehti](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="9f9a8-122">Avaa SQL Server Reporting Services -verkkoportaali napsauttamalla raporttien URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="9f9a8-123">Luo portaalissa uusi **Dynamics**-niminen kansio.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="9f9a8-124">[![dynamics-kansio](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="9f9a8-125">Valitse **Reporting Servicesin määritystenhallinnassa** **Sähköpostiasetukset**-välilehti ja varmista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-126">[![sähköpostiasetukset-välilehti](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="9f9a8-127">Valitse **Toimeenpanotili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-128">[![toimeenpanotili-välilehti](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="9f9a8-129">Älä muuta **Salausavaimet**-välilehden oletusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="9f9a8-130">[![salausavaimet-välilehti](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="9f9a8-131">Valitse **Tilausasetukset**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="9f9a8-132">[![tilausasetukset-välilehti](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="9f9a8-133">Älä muuta **Skaalauskäyttöönotto**-välilehden oletusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="9f9a8-134">[![skaalauskäyttöönotto-välilehti](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="9f9a8-135">Älä muuta **Power BI -integrointi** -välilehden oletusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="9f9a8-136">[![power bi -integrointi -välilehti](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="9f9a8-137">Sulje **Reporting Services -määritystenhallintasovellus** valitsemalla **Lopeta**.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="9f9a8-138">[![reporting Servicesin määritystenhallinnan sulkeminen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="9f9a8-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
