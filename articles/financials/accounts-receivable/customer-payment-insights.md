---
title: Asiakkaan maksutavat (esikatselu)
description: Tässä aiheessa kuvataan, miten voit asiakkaan maksutapojen avulla arvioida, milloin lasku maksetaan ja auttaa organisaatioita luomaan optimointistrategioita, jotka parantavat maksujen ajallaan maksamisen todennäköisyyttä.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "344659"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="a99c9-103">Asiakkaan maksutavat (esikatselu)</span><span class="sxs-lookup"><span data-stu-id="a99c9-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="a99c9-104">Tämä ominaisuus on kohdistetun version osa ja on saatavilla vain käyttäjille, jotka ovat valinneet yksityisen esikatselun.</span><span class="sxs-lookup"><span data-stu-id="a99c9-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="a99c9-105">Tämä ominaisuus sisältyy tulevaan yleisesti saatavilla olevaan versioon.</span><span class="sxs-lookup"><span data-stu-id="a99c9-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="a99c9-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="a99c9-106">Overview</span></span>

<span data-ttu-id="a99c9-107">Organisaatiot pitävät usein haastavana ennustaa milloin asiakas maksaa laskut.</span><span class="sxs-lookup"><span data-stu-id="a99c9-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="a99c9-108">Näiden tietojen puute voi aiheuttaa virheellisiä kassavirtaennusteita, tehottomia perintäprosesseja ja tilausten toimittamista asiakkaille, jotka voivat luoda luottoriskin.</span><span class="sxs-lookup"><span data-stu-id="a99c9-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="a99c9-109">Asiakkaan maksutavat (esikatselu) käyttää automaattianalyysiä ennustaakseen milloin lasku maksetaan.</span><span class="sxs-lookup"><span data-stu-id="a99c9-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a99c9-110">Se tarjoaa myös optimointistrategioita, joita voidaan räätälöidä niin, että voidaan maksimoida todennäköisyys sille, että asiakkaat maksavat ajoissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="a99c9-111">Ennusteet</span><span class="sxs-lookup"><span data-stu-id="a99c9-111">Predictions</span></span>

<span data-ttu-id="a99c9-112">Maksuennusteiden avulla organisaatiot voivat parantaa yritysprosessejaan seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="a99c9-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="a99c9-113">Tunnistaa helposti laskut, jotka todennäköisesti maksetaan myöhässä.</span><span class="sxs-lookup"><span data-stu-id="a99c9-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="a99c9-114">Tehdä tarvittavat toimenpiteet parantaakseen todennäköisyyttä, että maksu maksetaan ajoissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="a99c9-115">Asiakkaan maksutavat (esikatselu) käyttää automaattianalyysiä ennustaakseen milloin lasku maksetaan.</span><span class="sxs-lookup"><span data-stu-id="a99c9-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a99c9-116">Käyttää historiatietoja laskuista, maksuista ja asiakastiedoista luodakseen automaattianalyysin, jonka avulla voi ennustaa milloin lasku maksetaan.</span><span class="sxs-lookup"><span data-stu-id="a99c9-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="a99c9-117">Asiakkaan maksutavat (esikatselu) ennustaa kolme maksun todennäköisyyttä kullekin avoimelle laskulle:</span><span class="sxs-lookup"><span data-stu-id="a99c9-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="a99c9-118">Todennäköisyys sille, että maksu suoritetaan ajoissa (laskun eräpäivään mennessä).</span><span class="sxs-lookup"><span data-stu-id="a99c9-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="a99c9-119">Todennäköisyys sille, että maksu suoritetaan 30 päivän kuluessa laskun eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="a99c9-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="a99c9-120">Todennäköisyys sille, että maksu suoritetaan 30 päivän jälkeen laskun eräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="a99c9-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="a99c9-121">Maksujen todennäköisyyksiä voidaan tarkastella ennusteosiossa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="a99c9-122">[![Maksuennusteet](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="a99c9-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="a99c9-123">Jokaisella laskulla on myös määritetty voittava maksujen todennäköisyys käyttäen jotakin yllä kuvatuista kolmesta ennalta määritellystä maksun todennäköisyysskenaariosta.</span><span class="sxs-lookup"><span data-stu-id="a99c9-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="a99c9-124">Skenaario, jolla on suurin maksun todennäköisyys on voittanut skenaario.</span><span class="sxs-lookup"><span data-stu-id="a99c9-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="a99c9-125">Oletetaan esimerkiksi, että laskun ennuste näyttää 71 prosenttia sille, että lasku maksetaan ajoissa, 13 prosenttia sille, että lasku maksettu 30 päivän sisällä eräpäivästä ja 16 prosentin todennäköisyyttä sille, että lasku maksetaan yli 30 päivää eräpäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a99c9-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="a99c9-126">Suurin todennäköisyys ilmaisee, että lasku on ajoissa-skenaariossa siten, että lasku merkitään todennäköisesti ajallaan maksettavaksi.</span><span class="sxs-lookup"><span data-stu-id="a99c9-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="a99c9-127">[![Maksuennusteet](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="a99c9-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="a99c9-128">Optimointistrategiat</span><span class="sxs-lookup"><span data-stu-id="a99c9-128">Optimization strategies</span></span>

<span data-ttu-id="a99c9-129">Maksuennusteiden lisäksi asiakkaan maksutapojen (esikatselu) avulla voit käyttää optimointistrategioita parantaaksesi mahdollisuuksia saada maksu ajoissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="a99c9-130">Tämä antaa organisaatioille mahdollisuuden tehdä ”mitä jos” -analyysejä antamalla käyttäjien oikaista laskuja ja asiakasparametrejä ja sitten verrata vaikuttaako tämä todennäköisyyteen saada maksut ajoissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="a99c9-131">Organisaatio voi esimerkiksi halutessaan arvioida vaikuttaako käteisalennuksen päivittäminen laskuihin maksujen ajallaan saamisen todennäköisyyttä.</span><span class="sxs-lookup"><span data-stu-id="a99c9-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="a99c9-132">Kun laskut on optimoitu käyttämään uutta alennusta, käyttäjät voivat tarkistaa parantaako alennuksen lisääminen todennäköisyyttä saada maksu ajoissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="a99c9-133">Mikäli alennuksen lisääminen kustantaa vain vähän verrattuna sen tuomaan etuun ajallaan saadusta maksusta, organisaatio voi valita kohdistavansa alennuksen kaikkiin tuleviin avoimiin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="a99c9-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="a99c9-134">Tällä hetkellä vain alennus on käytettävissä optimointistrategiana asiakkaan maksutavassa (esikatselu).</span><span class="sxs-lookup"><span data-stu-id="a99c9-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="a99c9-135">[![Optimoidut ennusteet](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="a99c9-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="a99c9-136">Miten saada asiakkaan maksutavat (esikatselu)</span><span class="sxs-lookup"><span data-stu-id="a99c9-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="a99c9-137">Mikäli haluat kokeilla asiakkaanmaksutapoja (esikatselu), lähetä sähköpostia [Finance Insights Preview team](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a99c9-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="a99c9-138">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="a99c9-138">Privacy Statement</span></span>

<span data-ttu-id="a99c9-139">Esikatselut tallentavat asiakkaan tiedot Yhdysvalloissa.</span><span class="sxs-lookup"><span data-stu-id="a99c9-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="a99c9-140">Lisäksi esikatselut (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 for Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) ei pidä käyttää henkilötietojen tai muiden sellaisten tietojen prosessoimiseen, joita koskevat lait tai määräykset, ja (4) sillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="a99c9-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
