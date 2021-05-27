---
title: Palautustilauksen palautus on hylätty
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa palautustilauksen palautuksen hylkäämisen yhteydessä, jos laskutuksessa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020753"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="071e1-103">Palautustilauksen palautus on hylätty</span><span class="sxs-lookup"><span data-stu-id="071e1-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="071e1-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa palautustilauksen palautuksen hylkäämisen yhteydessä, jos laskutuksessa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista.</span><span class="sxs-lookup"><span data-stu-id="071e1-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="071e1-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="071e1-105">Description</span></span>

<span data-ttu-id="071e1-106">Hyvitys hylätään, kun palautustilauksen laskussa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista.</span><span class="sxs-lookup"><span data-stu-id="071e1-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="071e1-107">Näyttöön tulee seuraava virhesanoma: "Jotkin maksut eivät ole oikeassa tilassa kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="071e1-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="071e1-108">Tarkista kaikkien maksujen tila uudelleen ennen laskutusta."</span><span class="sxs-lookup"><span data-stu-id="071e1-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="071e1-109">Maksun varmennustiedot sisältävät seuraavan virhesanoman: "Adyen-yhdyskäytävän SendRequest() epäonnistui. Tila: 'InternalServerError'.22144; Adyen palautti tyhjän vastauksen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="071e1-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Hylätty palautustilauksen palautus -virhe](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="071e1-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="071e1-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="071e1-112">Sokkopalautusten käyttöönotto Adyenissa</span><span class="sxs-lookup"><span data-stu-id="071e1-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="071e1-113">Voit ottaa sokkopalautukset käyttöön noudattamalla [Dynamics 365 Payment Connector Adyenia varten – vianmääritys](adyen-support.md) -ohjeen vaiheita, jotta voit ottaa yhteyttä Adyenin tukiryhmään ja pyytää, että sokkopalautukset otetaan käyttöön Adyen-myyjätilillä.</span><span class="sxs-lookup"><span data-stu-id="071e1-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="071e1-114">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="071e1-114">Additional resources</span></span>

[<span data-ttu-id="071e1-115">Dynamics 365 -maksuyhdistin Adyenia varten</span><span class="sxs-lookup"><span data-stu-id="071e1-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="071e1-116">Dynamics 365:n Adyen-maksuyhdistimen määritys</span><span class="sxs-lookup"><span data-stu-id="071e1-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
