---
title: Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla
description: Tässä ohjeaiheessa kerrotaan, miten ulkoisen luettelon avulla voit luoda ja lähettää ostoehdotuksia.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adeffa101aa5a17543ca531aacde2130a07086e9
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826801"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a><span data-ttu-id="99a71-103">Siirtyminen sähköiseen hankintaan ulkoisten luetteloiden avulla</span><span class="sxs-lookup"><span data-stu-id="99a71-103">Use external catalogs for PunchOut e-procurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99a71-104">Käyttämällä ulkoisia luetteloita sähköiseen hankintaan siirryttäessä ei tarvitse ylläpitää toimittajien tuotetietoja omissa päätiedoissa.</span><span class="sxs-lookup"><span data-stu-id="99a71-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="99a71-105">Sen sijaan toimittajan sivuston ostoskori muunnetaan varasto-ottoehdotusriveiksi, joissa on oikeat tuotetiedot.</span><span class="sxs-lookup"><span data-stu-id="99a71-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="99a71-106">Vältä toimittajien tuotekuvausten ja -hintojen säilyttämistä omissa tuotteen päätiedoissa.</span><span class="sxs-lookup"><span data-stu-id="99a71-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="99a71-107">Käytä sen sijaan ulkoisia luetteloita siirryttäessä sähköiseen hankintaan</span><span class="sxs-lookup"><span data-stu-id="99a71-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="99a71-108">Kun työntekijät tämän jälkeen luovat ostoehdotuksia, he voivat siirtyä toimittajan ulkoiseen tuoteluettelosivustoon (toisin sanoen he voivat poistua sinun järjestelmästäsi ja siirtyä toimittajan sivustoon).</span><span class="sxs-lookup"><span data-stu-id="99a71-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="99a71-109">Tuotteet, jotka on lisätty ostoskoriin toimittajan sivustossa, voidaan muuntaa sitten varasto-ottoehdotusriveiksi.</span><span class="sxs-lookup"><span data-stu-id="99a71-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="99a71-110">Näin saat oikean tuotetiedot: tuotteen tunnuksen, nimen ja hinnan jne.</span><span class="sxs-lookup"><span data-stu-id="99a71-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="99a71-111">Käyttääkseen ulkoisia luetteloita työntekijän on luotava varasto-ottoehdotus **Omat ostoehdotukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="99a71-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="99a71-112">Työntekijästä, joka luo ehdotuksen, käytetään nimitystä ehdotuksen valmistelija.</span><span class="sxs-lookup"><span data-stu-id="99a71-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="99a71-113">Valmistelijana voit myös toteuttaa seuraavia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="99a71-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="99a71-114">Käytä **Ulkoiset luettelot** -rivin toimenpidettä sivun avaamiseen, joka sisältää kaikki ulkoiset luettelot, jotka ovat määritetyn ehdottajan, ostavan yrityksen ja vastaanottava toimintayksikön käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="99a71-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="99a71-115">Käyttöoikeuksiesi mukaan muuttaa ehdottajaa, ostavaa yritystä ja vastaanottavalle toimintayksikölle.</span><span class="sxs-lookup"><span data-stu-id="99a71-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="99a71-116">Arvojen muutos voi muuttaa ulkoisia luetteloita, jotka ovat käytettävissä ehdottajalle.</span><span class="sxs-lookup"><span data-stu-id="99a71-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="99a71-117">Ulkoiset luettelot, jotka ovat käytettävissä, määräytyvät nykyisen aktiivisten ostomenettelyiden perusteella ostavalle yritykselle tai vastaanottavalle toimintayksikölle.</span><span class="sxs-lookup"><span data-stu-id="99a71-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="99a71-118">Nämä käytännöt voivat sallia tai estää tiettyjen hankintaluokkien käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="99a71-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="99a71-119">Tämä voi vaikuttaa ulkoisiin luetteloihin, jotka on yhdistetty näihin hankintaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="99a71-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="99a71-120">Lisätietoja käytännöistä on kohdassa [Ostokäytäntöjen yleiskatsaus](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="99a71-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="99a71-121">Voit etsiä tiettyä hankintaluokkaa vastaavia ulkoisia luetteloita kirjoittamalla tekstiä luettelon hakukenttään.</span><span class="sxs-lookup"><span data-stu-id="99a71-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="99a71-122">Lisää tuotteita toimittajan tuoteluettelosta toimittajan sivustossa valitse ulkoinen luettelo.</span><span class="sxs-lookup"><span data-stu-id="99a71-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="99a71-123">Lisää tuotteita ostoskärryyn ja siirry eteenpäin. Ostoskorin rivit siirretään Microsoft Dynamics 365:een.</span><span class="sxs-lookup"><span data-stu-id="99a71-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="99a71-124">Jos hankintaluokille on useita eri vaihtoehtoja, valitse oikea hankintaluokka ennen kuin lisäät rivejä varasto-ottoehdotuksiin.</span><span class="sxs-lookup"><span data-stu-id="99a71-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="99a71-125">Kun rivit on lisätty varasto-ottoehdotukseen, voit lisätä lisää rivejä käyttämättä ulkoisia luetteloita.</span><span class="sxs-lookup"><span data-stu-id="99a71-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="99a71-126">Vaihtoehtoisesti voit edelleen lisätä rivejä ulkoisten luetteloiden avulla.</span><span class="sxs-lookup"><span data-stu-id="99a71-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="99a71-127">Kun varasto-ottoehdotus on valmis, käytä **Työnkulku** > **Lähetä** -toimintoa ja lähetä se hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="99a71-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="99a71-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="99a71-128">Additional resources</span></span>

- [<span data-ttu-id="99a71-129">Sähköiseen hankintaan siirtymisessä käytettyjen ulkoisten luetteloiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99a71-129">Set up an external catalog for PunchOut e-procurement</span></span>](set-up-external-catalog-for-punchout.md)
- [<span data-ttu-id="99a71-130">Ostojen cXML-parannukset</span><span class="sxs-lookup"><span data-stu-id="99a71-130">Purchasing cXML enhancements</span></span>](purchasing-cxml-enhancements.md)