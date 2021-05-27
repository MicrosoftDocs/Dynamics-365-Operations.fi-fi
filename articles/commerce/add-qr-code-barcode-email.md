---
title: QR-koodin tai viivakoodin lisääminen tapahtuma- ja kuittisähköposteihin
description: Tässä aiheessa kerrotaan, miten QR-koodeja ja viivakoodeja, jotka kuvaavat tilaustunnuksia, lisätään Microsoft Dynamics 365 Commercessa tapahtuma- ja kuittisähköposteihin.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9eea69f9618d4387f5d6320620dfee5d74813fc0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019536"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="2a9fd-103">QR-koodin tai viivakoodin lisääminen tapahtuma- ja kuittisähköposteihin</span><span class="sxs-lookup"><span data-stu-id="2a9fd-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a9fd-104">Tässä aiheessa kerrotaan, miten QR-koodeja ja viivakoodeja, jotka kuvaavat tilaustunnuksia, lisätään Microsoft Dynamics 365 Commercessa tapahtuma- ja kuittisähköposteihin.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2a9fd-105">Tapahtumasähköposteihin voidaan helposti sisällyttää QR-koodeja ja viivakoodeja, jotka nopeuttavat tilausten hakuprosessia vähittäismyyntiympäristössä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="2a9fd-106">Jos haluat lisätä sähköpostiviesteihin QR-koodeja ja viivakoodeja, käytät HTML:n **\<img\>**-tunnisteita, jotka pyytävät luomis- ja muodostamispalvelusta QR-koodin tai viivakoodin kuvan.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="2a9fd-107">Microsoft ei toimita tätä palvelua.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="2a9fd-108">On kuitenkin monia maksuttomia tai edullisia palveluita, jotka voivat tuottaa QR-koodeja ja viivakoodeja,, jotka luodaan dynaamisesti kyselymerkkijonossa välitetyn arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="2a9fd-109">QR-koodin tai viivakoodin lisääminen tapahtumasähköpostiin</span><span class="sxs-lookup"><span data-stu-id="2a9fd-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="2a9fd-110">Jos haluat lisätä QR-koodeja ja viivakoodeja tapahtumasähköpostiviestiin, joka lähetetään osana sähköistä ostoa, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="2a9fd-111">Avaa tapahtumasähköpostimallin lähde-HTML-koodi ja lisää **\<img\>**-HTML-tunniste, joka osoittaa QR-koodien tai viivakoodien palveluun.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2a9fd-112">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="2a9fd-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="2a9fd-113">Seuraavassa on selitetty edellinen esimerkki:</span><span class="sxs-lookup"><span data-stu-id="2a9fd-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2a9fd-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** edustaa QR-koodien ja viivakoodien palvelun toimialuetta.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2a9fd-115">**data** edustaa parametria, jonka QR-koodi- tai viivakoodipalvelu vastaanottaa sisällöt, jotka tulee antaa QR-koodina tai viivakoodina.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2a9fd-116">Arvo **%salesid%** on määritettävä tähän parametriin.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2a9fd-117">Huomaa tässä esimerkissä, että arvoa käytetään myös kuvan alt-tekstinä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2a9fd-118">**param1** ja **param2** edustavat valinnaisia lisäparametreja.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2a9fd-119">Siirry kohtaan **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit** ja lataa päivitetty HTML palvelimeen oikeaan tapahtumasähköpostin malliin.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="2a9fd-120">Parametrit voivat vaihdella eri QR-koodi- ja viivakoodipalveluiden välillä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2a9fd-121">Varmista siksi, että otat yhteyttä palveluntarjoajaan ja vahvistat parametrit, jotka on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="2a9fd-122">QR-koodin tai viivakoodin lisääminen kuittisähköpostiin</span><span class="sxs-lookup"><span data-stu-id="2a9fd-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="2a9fd-123">Kun haluat lisätä oston jälkeen myyntipisteestä lähetettävään kuittisähköpostiviestiin QR-koodin tai viivakoodin, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="2a9fd-124">Avaa kuittisähköpostimallin lähde-HTML-koodi ja lisää **\<img\>**-HTML-tunniste, joka osoittaa QR-koodien tai viivakoodien palveluun.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2a9fd-125">Alla on esimerkki.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="2a9fd-126">Seuraavassa on selitetty edellinen esimerkki:</span><span class="sxs-lookup"><span data-stu-id="2a9fd-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2a9fd-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** edustaa QR-koodien ja viivakoodien palvelun toimialuetta.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2a9fd-128">**data** edustaa parametria, jonka QR-koodi- tai viivakoodipalvelu vastaanottaa sisällöt, jotka tulee antaa QR-koodina tai viivakoodina.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2a9fd-129">Arvo **%receiptid%** on määritettävä tähän parametriin.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2a9fd-130">Huomaa tässä esimerkissä, että arvoa käytetään myös kuvan alt-tekstinä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2a9fd-131">**param1** ja **param2** edustavat valinnaisia lisäparametreja.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2a9fd-132">Siirry kohtaan **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit** ja lataa päivitetty HTML palvelimeen sähköpostimalliin, jolla on sähköpostitunnus **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="2a9fd-133">Parametrit voivat vaihdella eri QR-koodi- ja viivakoodipalveluiden välillä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2a9fd-134">Varmista siksi, että otat yhteyttä palveluntarjoajaan ja vahvistat parametrit, jotka on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a9fd-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2a9fd-135">Additional resources</span></span>

[<span data-ttu-id="2a9fd-136">Sähköpostikuittien lähettäminen Modern POS:stä (MPOS)</span><span class="sxs-lookup"><span data-stu-id="2a9fd-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="2a9fd-137">Tapahtuman tapahtumien sähköpostimallien luominen</span><span class="sxs-lookup"><span data-stu-id="2a9fd-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
