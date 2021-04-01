---
title: Toimittajapyynnön konfiguroinnit
description: Tässä aiheessa käsitellään kenttiä, jotka on täytettävä uudessa toimittajapyynnössä.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 61ef9ba4eb683fea030f06b3bacf687d7f146de4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246570"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="eaa58-103">Toimittajapyynnön konfiguroinnit</span><span class="sxs-lookup"><span data-stu-id="eaa58-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaa58-104">Toimittajapyynnön viimeistely edellyttää, että toimittajan yhteyshenkilö suorittaa ohjatun mahdollisen toimittajan rekisteröintitoiminnon.</span><span class="sxs-lookup"><span data-stu-id="eaa58-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="eaa58-105">Voit luoda **Toimittajapyynnön konfiguroinnit** -lomakkeessa profiileja, jotka määrittävät pakolliset ja näkyvät kentät ohjatussa mahdollisen toimittajan rekisteröintitoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="eaa58-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="eaa58-106">Ohjattu toimittajan rekisteröintitoiminto kysyy aluksi mahdollisen toimittajan käyttäjältä, missä maassa tai millä alueella toimittaja harjoittaa liiketoimintaa.</span><span class="sxs-lookup"><span data-stu-id="eaa58-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="eaa58-107">Tämä tieto määrittää käytettävän konfiguroinnin.</span><span class="sxs-lookup"><span data-stu-id="eaa58-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="eaa58-108">Jos maalle tai alueelle ei ole määritettyä tiettyä konfigurointia, käytetään oletuskonfigurointia.</span><span class="sxs-lookup"><span data-stu-id="eaa58-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="eaa58-109">Toimittajapyynnön konfiguroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eaa58-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="eaa58-110">Toimittajapyynnön konfiguroinnit -lomakkeessa on oletusarvoisesti käytössä toimittajakonfigurointi.</span><span class="sxs-lookup"><span data-stu-id="eaa58-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="eaa58-111">Oletuskonfiguroinnin maata tai alueita ei voi valita, joten **Maat/alueet**-osaa ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="eaa58-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="eaa58-112">Valitse ensin **Hankinta** > **Asetukset** > **Toimittajat** ja sitten **Toimittajapyynnön konfiguroinnit**.</span><span class="sxs-lookup"><span data-stu-id="eaa58-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="eaa58-113">Määritä luettelon kenttien tila napsauttamalla **Kentät**-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="eaa58-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="eaa58-114">Piilotettu (ei näy)</span><span class="sxs-lookup"><span data-stu-id="eaa58-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="eaa58-115">Näytetty (näkyvissä mutta ei pakollinen)</span><span class="sxs-lookup"><span data-stu-id="eaa58-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="eaa58-116">Pakollinen (näkyvissä ja pakollinen)</span><span class="sxs-lookup"><span data-stu-id="eaa58-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="eaa58-117">Määritä **Sisältö**-välilehdessä, näytetäänkö teksti ohjatussa toiminnossa ja onko ilmoitettava, että mahdollisen toimittajan käyttäjän on hyväksyttävä se ennen siirtymistä ohjatun toiminnon seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="eaa58-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="eaa58-118">Hyväksyntä pyydetään kaikille ehdoille, jotka käyttäjän on hyväksyttävä ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="eaa58-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="eaa58-119">Voit antaa lisäksi vahvistussanoman, joka näytetään, kun ohjattu toiminto on valmis. Voit myös lisätä yhden kyselylomakkeen tai useita lomakkeita.</span><span class="sxs-lookup"><span data-stu-id="eaa58-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="eaa58-120">Tietyn maan tai alueen toimittajakonfiguroinnin luonti</span><span class="sxs-lookup"><span data-stu-id="eaa58-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="eaa58-121">Valitse ensin **Hankinta** > **Asetukset** > **Toimittajat** ja sitten **Toimittajapyynnön konfiguroinnit**.</span><span class="sxs-lookup"><span data-stu-id="eaa58-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="eaa58-122">Luo uusi konfigurointi valitsemalla **Uusi** ja nimeä konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="eaa58-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="eaa58-123">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="eaa58-123">Click **Save**.</span></span>
4.  <span data-ttu-id="eaa58-124">Avaa **Maa/alueet**-välilehti ja valitse maa tai alue, jossa konfigurointia on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="eaa58-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="eaa58-125">Viimeistele konfigurointi noudattamalla oletuskonfiguroinnin ohjeita.</span><span class="sxs-lookup"><span data-stu-id="eaa58-125">Complete the configuration by following the guidelines for the default configuration.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]