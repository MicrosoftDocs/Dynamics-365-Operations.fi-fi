---
title: "SQL Server Reporting Servicesin määrittäminen paikallisessa käyttöönotossa"
description: "Tässä ohjeaiheessa on tietoja SQL Server Reporting Servicesin (SSRS) määrittämisestä paikallista käyttöönottoa varten."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, UnifiedOperations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5ee1b93b92516e14e9581c3b2fe6a2527403ae1e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="c2bca-103">SQL Server Reporting Servicesin määrittäminen paikallisessa käyttöönotossa</span><span class="sxs-lookup"><span data-stu-id="c2bca-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

<span data-ttu-id="c2bca-104">Tässä ohjeaiheessa kerrotaan, miten SQL Server Reporting Services (SSRS) määritetään Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin paikallista käyttöönottoa varten.</span><span class="sxs-lookup"><span data-stu-id="c2bca-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="c2bca-105">Avaa Reporting Services -määritystenhallintasovellus</span><span class="sxs-lookup"><span data-stu-id="c2bca-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="c2bca-106">Jätä oletusarvoinen **Palvelimen nimi**, jonka pitäisi olla nykyisen laitteen nimi, ja **Report Server -esiintymä**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="c2bca-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="c2bca-107">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="c2bca-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="c2bca-108">[![Reporting Servicesin määritysyhteys](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="c2bca-109">Valitse **Palvelutili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c2bca-110">[![Palvelutili-välilehti](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="c2bca-111">Valitse **Internet-palvelun URL**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="c2bca-112">[![Internet-palvelun URL -välilehti](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="c2bca-113">Valitse **Tietokanta**-välilehti ja tarkista, että **Tietokannan nimi** ja **Tunnistetietojen asetukset** ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="c2bca-114">**Huomautus:** Sinun on luotava uusi tietokanta.</span><span class="sxs-lookup"><span data-stu-id="c2bca-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="c2bca-115">Tee se valitsemalla **Muuta tietokantaa** ja tarkista sitten, että uuden tietokannan nimi on **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="c2bca-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="c2bca-116">[![tietokanta-välilehti](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="c2bca-117">Valitse **Internet-portaalin URL** -välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="c2bca-118">**Huomautus:** sinun on valittava **Käytä**, jotta voit luoda ja määrittää portaalin oikein.</span><span class="sxs-lookup"><span data-stu-id="c2bca-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="c2bca-119">[![Internet-portaalin url -välilehti](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="c2bca-120">Kun portaali on määritetty, **Internet-portaali**-välilehden on vastattava seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="c2bca-121">[![Internet-portaali-välilehti](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="c2bca-122">Avaa SQL Server Reporting Services -verkkoportaali napsauttamalla raporttien URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="c2bca-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="c2bca-123">Luo portaalissa uusi **Dynamics**-niminen kansio.</span><span class="sxs-lookup"><span data-stu-id="c2bca-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="c2bca-124">[![dynamics-kansio](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="c2bca-125">Valitse **Reporting Servicesin määritystenhallinnassa** **Sähköpostiasetukset**-välilehti ja varmista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c2bca-126">[![sähköpostiasetukset-välilehti](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="c2bca-127">Valitse **Toimeenpanotili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c2bca-128">[![toimeenpanotili-välilehti](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="c2bca-129">Älä muuta **Salausavaimet**-välilehden oletusasetuksia. [![salausavaimet-välilehti](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="c2bca-130">Valitse **Tilausasetukset**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c2bca-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c2bca-131">[![tilausasetukset-välilehti](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="c2bca-132">Älä muuta **Skaalauskäyttöönotto**-välilehden oletusasetuksia. [![skaalauskäyttöönotto-välilehti](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="c2bca-133">Älä muuta **Power BI -integrointi** -välilehden oletusasetuksia. [![power bi -integrointi -välilehti](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="c2bca-134">Sulje **Reporting Services -määritystenhallintasovellus** valitsemalla **Lopeta**.</span><span class="sxs-lookup"><span data-stu-id="c2bca-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="c2bca-135">[![reporting Servicesin määritystenhallinnan sulkeminen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="c2bca-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


