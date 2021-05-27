---
title: Vähittäismyymälä ei näy noutomyymälöiden luettelossa
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020817"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="25539-103">Vähittäismyymälä ei näy noutomyymälöiden luettelossa</span><span class="sxs-lookup"><span data-stu-id="25539-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25539-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="25539-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="25539-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="25539-105">Description</span></span>

<span data-ttu-id="25539-106">Vähittäismyyntiliike ei näy myymälöiden luettelossa, joista nimikkeitä voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="25539-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="25539-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="25539-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="25539-108">Myymälän osoitteen pituus- ja leveysasteen konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="25539-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="25539-109">Myymälän osoitteen pituus- ja leveysasteen konfiguroimisen Commerce headquarters -sovelluksessa voit tehdä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="25539-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="25539-110">Valitse **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="25539-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="25539-111">Etsi myymälä, jonka haluat näkyvän noutovaihtoehdoissa sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="25539-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="25539-112">Merkitse sen **Toimintayksikön numero** -arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="25539-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="25539-113">Valitse **Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**.</span><span class="sxs-lookup"><span data-stu-id="25539-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="25539-114">Hae aiemmin muistiin merkittyä toimintayksikön numeroa ja valitse sitten toimintayksikkö hakutuloksista.</span><span class="sxs-lookup"><span data-stu-id="25539-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="25539-115">Valitse **Osoitteet**-pikavälilehdessä **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="25539-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="25539-116">Varmista **Yleiset**-pikavälilehdessä, että **Pituuaste**- ja **Leveysaste**-kentät on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="25539-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="25539-117">Varmista osana tätä vaihetta, että arvot on määritetty oikein positiivisiksi tai negatiivisiksi luvuiksi.</span><span class="sxs-lookup"><span data-stu-id="25539-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="25539-118">Täydennysryhmien konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="25539-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="25539-119">Voit määrittää täydennysryhmät Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="25539-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="25539-120">Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.</span><span class="sxs-lookup"><span data-stu-id="25539-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="25539-121">Valitse määritettävä verkkokauppa.</span><span class="sxs-lookup"><span data-stu-id="25539-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="25539-122">Valitse toimintoruudussa ensin **Asetukset** ja sitten **Täytäntöönpanoryhmän määritys**.</span><span class="sxs-lookup"><span data-stu-id="25539-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="25539-123">Valitse **Täytäntöönpanoryhmän määritys** -sivulla verkkokaupan täytäntöönpanoryhmä.</span><span class="sxs-lookup"><span data-stu-id="25539-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="25539-124">Varmista **Asetukset**-kohdasta, että vähittäiskauppa on määritetty oikein täytääntöpanoryhmälle.</span><span class="sxs-lookup"><span data-stu-id="25539-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25539-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="25539-125">Additional resources</span></span> 

[<span data-ttu-id="25539-126">Toimintayksikön luominen</span><span class="sxs-lookup"><span data-stu-id="25539-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="25539-127">Online-kanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="25539-127">Set up an online channel</span></span>](../channel-setup-online.md)