---
title: Asiakastietueet eivät näy Commerce headquarters -sovelluksessa
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa silloin, kun asiakastietueet eivät näy heti Commerce headquarters -sovelluksessa.
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801792"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="d4a95-103">Asiakastietueet eivät näy Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="d4a95-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4a95-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa silloin, kun asiakastietueet eivät näy heti Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d4a95-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="d4a95-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4a95-105">Description</span></span>

<span data-ttu-id="d4a95-106">Kun luot uuden asiakastietueen käyttämällä sähköisen kaupan myymälän kirjautumistyönkulkua, vastaava asiakastietue ei näy heti Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="d4a95-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4a95-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d4a95-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="d4a95-108">Poista käytöstä asiakkaan luonti asynkronisessa tilassa</span><span class="sxs-lookup"><span data-stu-id="d4a95-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4a95-109">Jos poistat asynkronisen asiakkaan luonnin käytöstä, järjestelmän suorituskyky voi heiketä, koska kunkin tietueen luominen luo reaaliaikaisen pyynnön Commerce headquartersiin.</span><span class="sxs-lookup"><span data-stu-id="d4a95-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="d4a95-110">Jos lisäksi Commerce headquarters ei ole käytössä (esimerkiksi huoltotyönkulkujen yhteydessä), uusien asiakkaiden luontivirroissa syntyy virheitä.</span><span class="sxs-lookup"><span data-stu-id="d4a95-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="d4a95-111">Voit poistaa asiakkaan asynkronisen luonnin käytöstä Commerce headquarters -ohjelmassa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d4a95-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d4a95-112">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan asetukset \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="d4a95-113">Jos et vielä käytä online-kanavassasi toimintoprofiilia, luo sellainen.</span><span class="sxs-lookup"><span data-stu-id="d4a95-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="d4a95-114">Varmista, että **Luo asiakas asynkronisessa tilassa** -asetuksena on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="d4a95-115">Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="d4a95-116">Valitse online-myymälä, jossa asynkroninen asiakkaan luonti poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d4a95-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="d4a95-117">Varmista **Yleiset**-välilehdessä, että **Toimintoprofiili**-kentän arvoksi tulee online-kanavaa varten käytössä oleva toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="d4a95-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4a95-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d4a95-118">Additional resources</span></span>

[<span data-ttu-id="d4a95-119">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="d4a95-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
