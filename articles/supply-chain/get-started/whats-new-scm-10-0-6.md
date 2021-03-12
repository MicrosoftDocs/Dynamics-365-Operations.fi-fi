---
title: Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio10.0.6 (marraskuu 2019)
description: Tässä ohjeaiheessa käsitellään Dynamics 365 Supply Chain Managementin version 10.0.6 uusia tai muuttuneita ominaisuuksia.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983672"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="fb6cf-103">Dynamics 365 Supply Chain Managementin uudet tai muuttuneet ominaisuudet, versio10.0.6 (marraskuu 2019)</span><span class="sxs-lookup"><span data-stu-id="fb6cf-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb6cf-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.6 uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="fb6cf-105">Tämän version koontiversion numero on 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="fb6cf-106">Kun yleisen saatavuuden päivämäärä on marraskuussa, uudet toiminnot ovat käytettävissä lokakuun esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="fb6cf-107">Lisätietoja versiosta 10.0.6 on kohdassa [Lisäresurssit](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="fb6cf-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="fb6cf-108">Tuotekonfiguraatiomallien V2:n tietoyksikkö</span><span class="sxs-lookup"><span data-stu-id="fb6cf-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="fb6cf-109">Toinen tuotekonfiguraatiomallien tietoyksikön versio julkaistaan (nimeltä tuotekonfiguraatiomallit V2).</span><span class="sxs-lookup"><span data-stu-id="fb6cf-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="fb6cf-110">418-tuotekonfiguraatiomallit-oletusmalli tarvitaan myös. Se käyttää uutta tuotekonfiguraatiomallit V2 -tietoyksikköä tuonnin ja viennin ympäristömalleissa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="fb6cf-111">Mallia ei päivitetä automaattisesti. Se on siis ladattava oletustiedoista manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="fb6cf-112">V2-yksikkö vie yhden rivin erillisenä tiedostona liitteeseen sisäisen rivin sijaan. Näin ratkaistaan V1-yksikön kokorajoitukset.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="fb6cf-113">Mitä tarvitaan, jotta tämä muutos voidaan tehdä?</span><span class="sxs-lookup"><span data-stu-id="fb6cf-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="fb6cf-114">Koska V1-yksikkö on vanhentunut, tulee alkaa siirtyä V1-yksiköstä V2-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="fb6cf-115">Jos käytössä on 418-tuotekonfiguraatiomallit-malli, voit valita Lataa oletusmallit -painikkeen ja ladata 418-tuotekonfiguraatiomallit-mallin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="fb6cf-116">Jos haluat säilyttää yhteensopivuuden olemassa olevien järjestelmien kanssa, voit nyt jatkaa olemassa olevan mallin ja vanhentuneen V1-yksikön käyttämistä niin kauan, kunnes siirrät integroinnit uuteen malliin.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="fb6cf-117">Ominaisuuksien hallinnan parannukset</span><span class="sxs-lookup"><span data-stu-id="fb6cf-117">Feature management enhancements</span></span>
<span data-ttu-id="fb6cf-118">Ominaisuuksien hallinnan avulla voit nyt ottaa käyttöön kaikki uudet toiminnot oletusarvoisesti, pyytää vahvistusta toiminnon käyttöönottoa varten ja ottaa käyttöön kaikki toiminnot, jotka vielä eivät ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="fb6cf-119">Ostosopimuksen vastuullinen osapuoli</span><span class="sxs-lookup"><span data-stu-id="fb6cf-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="fb6cf-120">Nyt voit määrittää ensisijaiset ja toissijaiset vastuulliset osapuolet Ostosopimuksen luokitus -lomakkeessa ja tuloksena olevissa ostosopimuksissa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="fb6cf-121">Tämä antaa käyttäjille mahdollisuuden valvoa sopimuksia.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="fb6cf-122">Tarjouspyynnön linkki ostotilausriviin</span><span class="sxs-lookup"><span data-stu-id="fb6cf-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="fb6cf-123">Voit lisätä viitelinkin ostotilausriveiltä takaisin vastaaviin tarjouspyyntöriveihin, joista linkit ovat lähtöisin. Näin käyttäjät voivat helposti käyttää tarjousasiakirjan tukipyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb6cf-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fb6cf-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fb6cf-125">Ohjelmavirhekorjaukset</span><span class="sxs-lookup"><span data-stu-id="fb6cf-125">Bug fixes</span></span>
<span data-ttu-id="fb6cf-126">Saat lisätietoja version 10.0.6 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="fb6cf-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="fb6cf-127">Ympäristön update 30 -päivitys</span><span class="sxs-lookup"><span data-stu-id="fb6cf-127">Platform update 30</span></span>
<span data-ttu-id="fb6cf-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 sisältää Platform update 30:n.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="fb6cf-129">Lisätietoja Platform update 30:sta on kohdassa [Platform update 30:n uudet ja muuttuneet ominaisuudet](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="fb6cf-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="fb6cf-130">Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelma</span><span class="sxs-lookup"><span data-stu-id="fb6cf-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="fb6cf-131">Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?</span><span class="sxs-lookup"><span data-stu-id="fb6cf-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="fb6cf-132">Tutustu kohtaan [Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelma](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="fb6cf-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="fb6cf-133">Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="fb6cf-134">Poistetut ja vanhentuneet Supply Chain Management -toiminnot</span><span class="sxs-lookup"><span data-stu-id="fb6cf-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="fb6cf-135">[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="fb6cf-136">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="fb6cf-137">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="fb6cf-138">Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="fb6cf-139">Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="fb6cf-140">Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.</span><span class="sxs-lookup"><span data-stu-id="fb6cf-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
