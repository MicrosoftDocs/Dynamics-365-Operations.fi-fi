---
title: (ER) Konfiguraatioiden tuonti RCS:stä
description: Tässä ohjeaiheessa on tietoja tavasta, jolla käyttäjä voi tuoda ER-konfiguraation uuden version RCS:stä.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799abeafe5f0929e6dd2f8a5f437f3c10b3b06d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570533"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="524a4-103">(ER) Konfiguraatioiden tuonti RCS:stä</span><span class="sxs-lookup"><span data-stu-id="524a4-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="524a4-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Regulatory Configuration Servicesista (RCS).</span><span class="sxs-lookup"><span data-stu-id="524a4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="524a4-105">Tässä esimerkissä voit valita RCS-esiintymässä määritetyn ER-konfiguraation version ja tuoda sen malliyrityksen Litware, Inc:n nykyiseen esiintymään. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="524a4-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="524a4-106">Näitä vaiheita varten on ensin suoritettava ohjeaiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="524a4-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="524a4-107">Näiden vaiheiden suorittamista varten tarvitset sen RCS-esiintymän käyttöoikeuden, jossa on vähintään yksi ER-konfiguraatio joko **Valmis**- tai **Jaettu**-tilassa.</span><span class="sxs-lookup"><span data-stu-id="524a4-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="524a4-108">Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="524a4-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="524a4-109">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="524a4-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="524a4-110">Jos konfiguraation lähde ei ole näkyvissä, suorita ohjeaiheen [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="524a4-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="524a4-111">Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse ulkoinen **Regulatory Services – määritys** -linkki ja valmistele RCS-ympäristö ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="524a4-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="524a4-112">Valitse **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="524a4-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="524a4-113">Valitse **RCS**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="524a4-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="524a4-114">Jos yrityksessä on jo valmisteltu RCS-ympäristö, käytä sitä sivun URL-osoitteiden avulla.</span><span class="sxs-lookup"><span data-stu-id="524a4-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="524a4-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="524a4-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="524a4-116">Rekisteröi uusi ER-säilö.</span><span class="sxs-lookup"><span data-stu-id="524a4-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="524a4-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="524a4-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="524a4-118">Valitse lähteeksi Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="524a4-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="524a4-119">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="524a4-119">Select Repositories.</span></span> 
4. <span data-ttu-id="524a4-120">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="524a4-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="524a4-121">Syötä Konfiguraatiosäilön tyyppi -kentän arvoksi RCS.</span><span class="sxs-lookup"><span data-stu-id="524a4-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="524a4-122">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="524a4-122">Select Create repository.</span></span> 
7. <span data-ttu-id="524a4-123">Anna tai valitse arvo RCS-ympäristön näyttönimen kentässä.</span><span class="sxs-lookup"><span data-stu-id="524a4-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="524a4-124">Valitse haluamasi RCS-esiintymä.</span><span class="sxs-lookup"><span data-stu-id="524a4-124">Select the desired RCS instance.</span></span> <span data-ttu-id="524a4-125">Niitä voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="524a4-125">You can have several of them.</span></span> 
9. <span data-ttu-id="524a4-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="524a4-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="524a4-127">ER-konfiguraatioiden tuominen RCS-pohjaisesta säiliöstä</span><span class="sxs-lookup"><span data-stu-id="524a4-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="524a4-128">Valitse **Näytä suodattimet**.</span><span class="sxs-lookup"><span data-stu-id="524a4-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="524a4-129">Anna **Nimi**-kenttään suodatusarvoksi RCS käyttämällä **sisältää**-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="524a4-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="524a4-130">Kun avaat valitun säilön, valitse **Yhdistä Regulatory Configuration Servicesiin** -sivulla **Muodosta yhteys Regulatory Configuration Servicesiin valitsemalla tämä** -linkki.</span><span class="sxs-lookup"><span data-stu-id="524a4-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="524a4-131">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="524a4-131">Select **Open**.</span></span> 
5. <span data-ttu-id="524a4-132">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="524a4-132">Select **Close**.</span></span> 
6. <span data-ttu-id="524a4-133">Valitse sopiva ER-konfiguraation versio ja tuo se nykyiseen esiintymään valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="524a4-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]