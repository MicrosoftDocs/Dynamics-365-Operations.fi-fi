---
title: (ER) Konfiguraatioiden tuonti RCS:stä
description: Tässä ohjeaiheessa on tietoja tavasta, jolla käyttäjä voi tuoda ER-konfiguraation uuden version RCS:stä.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143220"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="3134f-103">(ER) Konfiguraatioiden tuonti RCS:stä</span><span class="sxs-lookup"><span data-stu-id="3134f-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3134f-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Regulatory Configuration Servicesista (RCS).</span><span class="sxs-lookup"><span data-stu-id="3134f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="3134f-105">Tässä esimerkissä voit valita RCS-esiintymässä määritetyn ER-konfiguraation version ja tuoda sen malliyrityksen Litware, Inc:n nykyiseen esiintymään. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3134f-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="3134f-106">Näitä vaiheita varten on ensin suoritettava ohjeaiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3134f-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="3134f-107">Näiden vaiheiden suorittamista varten tarvitset sen RCS-esiintymän käyttöoikeuden, jossa on vähintään yksi ER-konfiguraatio joko **Valmis**- tai **Jaettu**-tilassa.</span><span class="sxs-lookup"><span data-stu-id="3134f-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="3134f-108">Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="3134f-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="3134f-109">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="3134f-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="3134f-110">Jos konfiguraation lähde ei ole näkyvissä, suorita ohjeaiheen [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3134f-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="3134f-111">Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse ulkoinen **Regulatory Services – määritys** -linkki ja valmistele RCS-ympäristö ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3134f-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="3134f-112">Valitse **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3134f-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="3134f-113">Valitse **RCS**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3134f-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="3134f-114">Jos yrityksessä on jo valmisteltu RCS-ympäristö, käytä sitä sivun URL-osoitteiden avulla.</span><span class="sxs-lookup"><span data-stu-id="3134f-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="3134f-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3134f-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="3134f-116">Rekisteröi uusi ER-säilö.</span><span class="sxs-lookup"><span data-stu-id="3134f-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="3134f-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3134f-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="3134f-118">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3134f-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="3134f-119">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="3134f-119">Click Repositories.</span></span> 
4. <span data-ttu-id="3134f-120">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="3134f-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="3134f-121">Syötä Konfiguraatiosäilön tyyppi -kentän arvoksi RCS.</span><span class="sxs-lookup"><span data-stu-id="3134f-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="3134f-122">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="3134f-122">Click Create repository.</span></span> 
7. <span data-ttu-id="3134f-123">Anna tai valitse arvo RCS-ympäristön näyttönimen kentässä.</span><span class="sxs-lookup"><span data-stu-id="3134f-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="3134f-124">Valitse haluamasi RCS-esiintymä.</span><span class="sxs-lookup"><span data-stu-id="3134f-124">Select the desired RCS instance.</span></span> <span data-ttu-id="3134f-125">Huomaa, että niitä voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="3134f-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="3134f-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3134f-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="3134f-127">ER-konfiguraatioiden tuominen RCS-pohjaisesta säiliöstä</span><span class="sxs-lookup"><span data-stu-id="3134f-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="3134f-128">Valitse **Näytä suodattimet**.</span><span class="sxs-lookup"><span data-stu-id="3134f-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="3134f-129">Anna **Nimi**-kenttään suodatusarvoksi RCS käyttämällä **sisältää**-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="3134f-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="3134f-130">Kun avaat valitun säilön, valitse **Yhdistä Regulatory Configuration Servicesiin** -sivulla **Muodosta yhteys Regulatory Configuration Servicesiin napsauttamalla tästä** -linkki.</span><span class="sxs-lookup"><span data-stu-id="3134f-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="3134f-131">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="3134f-131">Click **Open**.</span></span> 
5. <span data-ttu-id="3134f-132">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="3134f-132">Click **Close**.</span></span> 
6. <span data-ttu-id="3134f-133">Valitse sopiva ER-konfiguraation versio ja tuo se nykyiseen esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="3134f-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

