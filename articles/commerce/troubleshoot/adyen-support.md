---
title: Dynamics 365 Payment Connector Adyenia varten -ongelmien vianmääritys
description: Tämä ohjeaihe sisältää vianmäärityksen ohjeita, jotka voivat auttaa tuen saamiseen, kun Microsoft Dynamics 365 Payment Connector Adyenia varten -yhdistimeen liittyy ongelmia.
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
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801816"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="6816f-103">Dynamics 365 Payment Connector Adyenia varten -ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="6816f-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6816f-104">Tämä ohjeaihe sisältää vianmäärityksen ohjeita, jotka voivat auttaa tuen saamiseen, kun Microsoft Dynamics 365 Payment Connector Adyenia varten -yhdistimeen liittyy ongelmia.</span><span class="sxs-lookup"><span data-stu-id="6816f-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="6816f-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6816f-105">Description</span></span>

<span data-ttu-id="6816f-106">Dynamics 365 Payment Connector Adyenia varten -liittimessä on ongelmia seuraavilla alueilla, ja tarvitset tukea Adyen-tiimiltä:</span><span class="sxs-lookup"><span data-stu-id="6816f-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="6816f-107">Myyntipisteen (POS), Modernin myyntipisteen (MPOS), puhelinkeskuksen tai Dynamics 365 Commercen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="6816f-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="6816f-108">Adyen-maksupalveluntarjoajan (PSP) viitenumero (esimerkiksi jos sinulla on kysymyksiä hylkäämisistä, mukaan lukien manuaaliset \[MKE\]-hylkäämiset)</span><span class="sxs-lookup"><span data-stu-id="6816f-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="6816f-109">Mikä tahansa, joka ei toimi testi- tai live-kauppiasympäristöissä</span><span class="sxs-lookup"><span data-stu-id="6816f-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="6816f-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6816f-110">Resolution</span></span>

<span data-ttu-id="6816f-111">Seuraavan sähköpostimallin avulla voit aloittaa tukiprosessin Adyen-tiimin kanssa.</span><span class="sxs-lookup"><span data-stu-id="6816f-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="6816f-112">Voit nopeuttaa vianmääritystä varmistamalla, että sähköpostiviestissä on kaikki tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="6816f-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="6816f-113">Kenttä</span><span class="sxs-lookup"><span data-stu-id="6816f-113">Field</span></span>        | <span data-ttu-id="6816f-114">Arvo</span><span class="sxs-lookup"><span data-stu-id="6816f-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="6816f-115">Loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6816f-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="6816f-116">Kopio</span><span class="sxs-lookup"><span data-stu-id="6816f-116">Cc</span></span>           | |
| <span data-ttu-id="6816f-117">Aiherivi</span><span class="sxs-lookup"><span data-stu-id="6816f-117">Subject line</span></span> | <span data-ttu-id="6816f-118">Microsoft Dynamics -tukipyyntö</span><span class="sxs-lookup"><span data-stu-id="6816f-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="6816f-119">Tekstiosa</span><span class="sxs-lookup"><span data-stu-id="6816f-119">Body</span></span>         | <p><span data-ttu-id="6816f-120">Hei tukitiimi,</span><span class="sxs-lookup"><span data-stu-id="6816f-120">Hi Support,</span></span></p><p><span data-ttu-id="6816f-121">Pyydän tukea seuraavaan ongelmaan:</span><span class="sxs-lookup"><span data-stu-id="6816f-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="6816f-122">Myyjän tili</span><span class="sxs-lookup"><span data-stu-id="6816f-122">Merchant account</span></span></li><li><span data-ttu-id="6816f-123">Ympäristö (testi/tuotanto)</span><span class="sxs-lookup"><span data-stu-id="6816f-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="6816f-124">Kanava (myyntipiste/puhelinkeskus/Commercen sähköinen kauppa)</span><span class="sxs-lookup"><span data-stu-id="6816f-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="6816f-125">PSP-viitenumero, jos tapahtumaan liittyy tietty tapahtuma (voit löytää PSP-viitenumeron kuitista, Adyenin asiakasalueesta tai kassapäätteen tapahtumavalikosta).</span><span class="sxs-lookup"><span data-stu-id="6816f-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="6816f-126">Virhesanoman näyttökuva tai valokuva, jos käytettävissä</span><span class="sxs-lookup"><span data-stu-id="6816f-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="6816f-127">Tapahtumienvalvontalokit (.txt-muodossa)</span><span class="sxs-lookup"><span data-stu-id="6816f-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="6816f-128">Kuvaus ongelmasta ja kokeilemistasi vianmääritysvaiheista.</span><span class="sxs-lookup"><span data-stu-id="6816f-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="6816f-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6816f-129">Additional resources</span></span>

[<span data-ttu-id="6816f-130">Hyväksy maksuja Dynamics 365 Commercen Adyen-yhdistimen avulla</span><span class="sxs-lookup"><span data-stu-id="6816f-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="6816f-131">Dynamics 365 -maksuyhdistin Adyenia varten</span><span class="sxs-lookup"><span data-stu-id="6816f-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="6816f-132">Dynamics 365:n Adyen-maksuyhdistimen määritys</span><span class="sxs-lookup"><span data-stu-id="6816f-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
