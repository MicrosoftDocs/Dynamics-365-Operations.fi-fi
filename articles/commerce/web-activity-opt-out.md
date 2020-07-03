---
title: Verkkotoiminnan tapahtumien keräämisestä kieltäytyminen
description: Tässä ohjeaiheessa käsitellään tapaa, jolla sivustossa vierailijat voivat kieltäytyä verkkotoiminnan tapahtumien keräämisestä Microsoft Dynamics 365 Commercessa.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378989"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="c86d9-103">Verkkotoiminnan tapahtumien keräämisestä kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="c86d9-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="c86d9-104">Tässä ohjeaiheessa käsitellään, miten asiakkaat voivat kieltäytyä verkkotoiminnan tapahtumien keräämisestä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="c86d9-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c86d9-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="c86d9-105">Overview</span></span>

<span data-ttu-id="c86d9-106">Dynamics 365 Commerce antaa sivuston järjestelmänvalvojille mahdollisuuden analysoida käyttäjien verkkotoimintaa omissa sähköisen kaupankäynnin sivustoissa.</span><span class="sxs-lookup"><span data-stu-id="c86d9-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="c86d9-107">Tällä tavoin he saavat paremman käsityksen tavasta, jolla sivustoja käytetään. Lisäksi he voivat optimoida sivustoja niin, että niiden käyttökokemus paranee ja liiketoimintatavoitteet saavutetaan.</span><span class="sxs-lookup"><span data-stu-id="c86d9-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="c86d9-108">Tapoja, joilla järjestelmänvalvojat voivat toteuttaa kieltäytymiskokemuksen</span><span class="sxs-lookup"><span data-stu-id="c86d9-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="c86d9-109">Järjestelmänvalvojat voivat toteuttaa kieltäytymiskokemuksen kolmella tavalla.</span><span class="sxs-lookup"><span data-stu-id="c86d9-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="c86d9-110">Kieltäytyminen käyttäjien puolesta</span><span class="sxs-lookup"><span data-stu-id="c86d9-110">Opt out on behalf of users</span></span>

<span data-ttu-id="c86d9-111">Järjestelmänvalvojat voivat kieltäytyä käyttäjien puolesta Commercen pääkonttoriosan (HQ) tilien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="c86d9-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="c86d9-112">Asiakas voidaan hakea ja valita HQ-asiakasohjelman **Kaikki asiakkaat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c86d9-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="c86d9-113">**Älä seuraa verkkotoimintaa** -asetukseksi määritetään **Kyllä** asiakastietosivun **Vähittäismyynti**-pikavälilehden **Tietosuoja**-osassa.</span><span class="sxs-lookup"><span data-stu-id="c86d9-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Tietosuoja-asetukset](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="c86d9-115">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="c86d9-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="c86d9-116">Moduulipohjainen opt-out-kokemus</span><span class="sxs-lookup"><span data-stu-id="c86d9-116">Module-based opt-out experience</span></span>

<span data-ttu-id="c86d9-117">Järjestelmänvalvojat voivat antaa todennettujen käyttäjien kieltäytyä itse verkkotoiminnan tapahtumien keräämisestä.</span><span class="sxs-lookup"><span data-stu-id="c86d9-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="c86d9-118">Voit antaa tämän opt-out-käyttökokemuksen lisäämällä käyttäjän opt-out-moduulin asiakastilin profiilisivuille.</span><span class="sxs-lookup"><span data-stu-id="c86d9-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="c86d9-119">Mukautetut laajennukset</span><span class="sxs-lookup"><span data-stu-id="c86d9-119">Custom extensions</span></span>

<span data-ttu-id="c86d9-120">Järjestelmänvalvojat voivat luoda omia laajennuksia, joilla hallitaan käyttäjien käyttöoikeustietoja.</span><span class="sxs-lookup"><span data-stu-id="c86d9-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="c86d9-121">Lisätietoja on kohdassa [Soita Retail-palvelimen ohjelmointirajapinnalle](e-commerce-extensibility/call-retail-server-apis.md) ja [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c86d9-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>