---
title: Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa
description: Tässä ohjeaiheessa on tietoja uuden asiakirjojen käyttöliittymän (UI) käyttämisestä sähköisen raportoinnin (ER) kehyksen liiketoiminta-asiakirjojen hallintaominaisuuden käyttämisestä.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681349"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="269e7-103">Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa</span><span class="sxs-lookup"><span data-stu-id="269e7-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="269e7-104">Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="269e7-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="269e7-105">Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista.</span><span class="sxs-lookup"><span data-stu-id="269e7-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="269e7-106">Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="269e7-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="269e7-107">Uusi asiakirjojen käyttöliittymä on selkeämpi ja mukavampi käyttää.</span><span class="sxs-lookup"><span data-stu-id="269e7-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="269e7-108">**Liiketoiminta asiakirja** -alueella näkyvät vain ne mallit, jotka ovat käytettävissä kulloisenkin toimittajan osalta.</span><span class="sxs-lookup"><span data-stu-id="269e7-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="269e7-109">**Uusi asiakirja** -painikkeen käyttäjät voivat luoda ja muokata mallia sähköisen raportoinnin (ER) muotomäärityksessä, joka on peräisin toiselta toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="269e7-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="269e7-110">Tämän ohjeaiheen esimerkissä toimittaja on Microsoft.</span><span class="sxs-lookup"><span data-stu-id="269e7-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="269e7-111">Uuden liiketoiminta-asiakirjojen hallinnan asiakirjojen käyttöliittymän käyttöön tarjoaminen</span><span class="sxs-lookup"><span data-stu-id="269e7-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="269e7-112">Aloittaaksesi uuden asiakirjojen käyttöliittymän käyttämisen liiketoiminta-asiakirjojen hallinnassa sinun on otettava **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="269e7-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="269e7-113">Noudata seuraavia ohjeita ottaaksesi tämän ominaisuuden käyttöön kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="269e7-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="269e7-114">Valitse **Ominaisuuksien hallinta** -työtila **Uusi** -välilehden luettelosta **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="269e7-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="269e7-115">Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="269e7-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="269e7-116">Voit avata uuden toiminnon päivittämällä sivun.</span><span class="sxs-lookup"><span data-stu-id="269e7-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="269e7-117">Muokkaa muiden toimittajien omistamia malleja</span><span class="sxs-lookup"><span data-stu-id="269e7-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="269e7-118">Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="269e7-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="269e7-120">Valitse valintaruudussa mallina käytettävä asiakirja ja sitten **Luo tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="269e7-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Liiketoiminta-asiakirjojen valintaruutu](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="269e7-122">Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="269e7-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="269e7-123">Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen.</span><span class="sxs-lookup"><span data-stu-id="269e7-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="269e7-124">Huomaa, että tämän määrityksen luonnosta (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="269e7-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="269e7-125">ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="269e7-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="269e7-126">Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.</span><span class="sxs-lookup"><span data-stu-id="269e7-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="269e7-127">Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.</span><span class="sxs-lookup"><span data-stu-id="269e7-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="269e7-128">Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="269e7-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Tiedoston luonnin valintaruutu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="269e7-130">**Uusi asiakirja** -painiketta käytetään luomaan ja muokkaamaan mallia toisen toimittajan toimittamassa ER-muotomäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="269e7-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="269e7-131">Tässä esimerkissä toimittajana on Microsoft.</span><span class="sxs-lookup"><span data-stu-id="269e7-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="269e7-132">Kun valitset **Uusi tiedosto**, näet kaikki nykyisen toimittajan tai muiden toimittajien omistamat mallit.</span><span class="sxs-lookup"><span data-stu-id="269e7-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="269e7-133">Kun olet valinnut mallin, se avautuu muokattavaksi.</span><span class="sxs-lookup"><span data-stu-id="269e7-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="269e7-134">Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="269e7-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="269e7-135">Lisätietoja on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="269e7-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
