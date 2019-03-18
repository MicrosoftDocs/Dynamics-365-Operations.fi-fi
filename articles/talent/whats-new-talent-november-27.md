---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (27. marraskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304165"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="92eb2-103">Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (27. marraskuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="92eb2-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92eb2-104">**Koontiversio 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="92eb2-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="92eb2-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="92eb2-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="92eb2-106">Muutokset</span><span class="sxs-lookup"><span data-stu-id="92eb2-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="92eb2-107">Huomautusta voi luoda palvelupyyntöjen hallinnassa</span><span class="sxs-lookup"><span data-stu-id="92eb2-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="92eb2-108">Palvelupyyntöjen hallinnan tapauslokiin liittyvän huomautuksen luontiin tai muokkaukseen liittyvään ongelmaan on tehty muutos.</span><span class="sxs-lookup"><span data-stu-id="92eb2-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="92eb2-109">Kirjoitusvirhe kompensaatiotyötilan analytiikkavälilehden sanassa</span><span class="sxs-lookup"><span data-stu-id="92eb2-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="92eb2-110">Kompensaatiotyötilan kompensaation analyysikaavion etnisen alkuperän kirjoitusvirhe on korjattu.</span><span class="sxs-lookup"><span data-stu-id="92eb2-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="92eb2-111">Työntekijän itsepalvelutyötilan ei näy, kun käyttäjää ei ole määritetty työntekijälle</span><span class="sxs-lookup"><span data-stu-id="92eb2-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="92eb2-112">Muutos tilanteessa, jossa **Työntekijän itsepalvelu** -työtila on valittu sellaisen käyttäjän käynnistyksen ensimmäiseksi sivuksi, jota ei ole määritetty työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="92eb2-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="92eb2-113">Tässä tilanteessa näytetään oletuskoontinäyttö.</span><span class="sxs-lookup"><span data-stu-id="92eb2-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="92eb2-114">Loma- ja poissaolovirhe: objektiviitettä ei ole määritetty objektin esiintymälle</span><span class="sxs-lookup"><span data-stu-id="92eb2-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="92eb2-115">Virhe on korjattu tekemällä muutos lomaan ja poissaoloon sen jälkeen, kun loma- ja poissaolotietueet on hyväksytty **Minulle määritetyt työnimikkeet** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="92eb2-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="92eb2-116">Kuvatyönkulkua ei voi peruuttaa</span><span class="sxs-lookup"><span data-stu-id="92eb2-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="92eb2-117">Kun kuvatyönkulku on peruutettu, työnkulun tilaksi määritetään peruutettu ja aiemmin luotu pyyntö voidaan poistaa työntekijän itsepalvelutyötilassa.</span><span class="sxs-lookup"><span data-stu-id="92eb2-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="92eb2-118">Uudelleenpalkatut työntekijät ja urakoitsijat näkyvät useita kertoja työsuhteen päättymisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="92eb2-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="92eb2-119">Tämän päivityksen jälkeen uudelleenpalkatut työntekijät, joiden työsuhde on päättynyt, näkyvät vain kerran poistuneiden luettelossa.</span><span class="sxs-lookup"><span data-stu-id="92eb2-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="92eb2-120">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="92eb2-120">Known issue</span></span>

- <span data-ttu-id="92eb2-121">**Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina.</span><span class="sxs-lookup"><span data-stu-id="92eb2-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="92eb2-122">**Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu.</span><span class="sxs-lookup"><span data-stu-id="92eb2-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="92eb2-123">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="92eb2-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="92eb2-124">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="92eb2-124">(This issue will be fixed in the next platform update.)</span></span>