---
title: Sähköisen kaupan kehitysympäristön määrittäminen Tier 1 Retail Server -näennäiskoneen virheenkorjausta varten
description: Tässä aiheessa on ohjeet sähköisen kaupan kehitysympäristön määrittämiseksi Tier 1 Retail Server -näennäiskoneen (VM) virheenkorjausta varten.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801480"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="e52d5-103">Sähköisen kaupan kehitysympäristön määrittäminen Tier 1 Retail Server -näennäiskoneen virheenkorjausta varten</span><span class="sxs-lookup"><span data-stu-id="e52d5-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e52d5-104">Tässä aiheessa on ohjeet sähköisen kaupan kehitysympäristön määrittämiseksi Tier 1 Retail Server -näennäiskoneen (VM) virheenkorjausta varten.</span><span class="sxs-lookup"><span data-stu-id="e52d5-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="e52d5-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e52d5-105">Description</span></span>

<span data-ttu-id="e52d5-106">Microsoft Dynamics 365 Commerce Tier 1 -ympäristöt otetaan yleensä käyttöön Commerce Runtimen (CRT) ja myyntipisteen (POS) laajennusten kehitystyössä.</span><span class="sxs-lookup"><span data-stu-id="e52d5-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="e52d5-107">Ne ovat itsenäisiä ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="e52d5-107">They are standalone environments.</span></span> <span data-ttu-id="e52d5-108">Ohjelmisto ei sisällä sähköisen kaupankäynnin komponentteja, koska arkkitehtuuri tarjoataan ohjelmisto palveluna (SaaS) -tyyppisesti.</span><span class="sxs-lookup"><span data-stu-id="e52d5-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="e52d5-109">Joissain tilanteissa kannattaa testata laajennuksia Tier 1 -ympäristössä, jotta voit tehdä virheenkorjausta laajennuksille sähköisen kaupan komponenteista.</span><span class="sxs-lookup"><span data-stu-id="e52d5-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="e52d5-110">Yleiset ohjeet: [Virheenkorjaus tason 1 Commerce-kehitysympäristössä](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="e52d5-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="e52d5-111">Kun teet virheenkorjausta Tier 1 -ympäristössä, koska sivusto kutsuu nyt eri Retail Server -palvelinta, palvelintenväliset kutsut voivat aiheuttaa erilaisia sisällön suojauskäytäntöön liittyviä virheitä.</span><span class="sxs-lookup"><span data-stu-id="e52d5-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="e52d5-112">Seuraavassa kuvassa on esimerkki virheestä, joka voi ilmetä, kun variantti valitaan tuotteen tietosivulla.</span><span class="sxs-lookup"><span data-stu-id="e52d5-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Virhe, kun variantti valitaan tuotteen tiedot -sivulla](media/unhandled-rejection-error.jpg)

<span data-ttu-id="e52d5-114">Seuraavassa kuvassa on esimerkki samanlaisesta virheestä selaimen virheenkorjaustyökaluissa (F12 Developer Tools).</span><span class="sxs-lookup"><span data-stu-id="e52d5-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="e52d5-115">Virhesanomassa mainitaan sisällön suojauskäytännön direktiivin rike.</span><span class="sxs-lookup"><span data-stu-id="e52d5-115">The error message mentions violation of the content security policy directive.</span></span>

![Virheenkorjaustyökalujen virhe](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="e52d5-117">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e52d5-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="e52d5-118">Sivuston sisällön suojauskäytännön poistaminen käytöstä Commercen sivuston muodostintyökalussa</span><span class="sxs-lookup"><span data-stu-id="e52d5-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="e52d5-119">Valitse sivusto, jota käsittelet.</span><span class="sxs-lookup"><span data-stu-id="e52d5-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="e52d5-120">Valitse **Asetukset** ja valitse sitten **Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="e52d5-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="e52d5-121">Valitse **Sisällön suojauskäytäntö** -välilehdestä **Poista sisällön suojauskäytäntö käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="e52d5-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="e52d5-122">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e52d5-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e52d5-123">Yritysten ja kuluttajien välinen (B2C) kirjautuminen ei toimi paikallisessa kehitysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="e52d5-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="e52d5-124">Voit kuitenkin simuloida vierailijan kirjautumisen tai luoda näytesivuja simuloidaksesi käyttäjien kirjautumista tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e52d5-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e52d5-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e52d5-125">Additional resources</span></span>

[<span data-ttu-id="e52d5-126">Sähköisen kaupankäynnin online-laajennusten kehittämisen aloittaminen</span><span class="sxs-lookup"><span data-stu-id="e52d5-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="e52d5-127">Sisällön suojauskäytännön (CSP) hallinta sähköisen kaupankäynnin sivustossa</span><span class="sxs-lookup"><span data-stu-id="e52d5-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
