---
title: Tapahtumasähköpostien mukauttaminen toimitustilan mukaan
description: Tässä aiheessa kuvataan, kuinka voit määrittää mukautettuja sähköpostimalleja tiettyjä ilmoitustyyppejä ja toimitustapoja varten Microsoft Dynamics 365 Commercessa.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799370"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="373ae-103">Tapahtumasähköpostien mukauttaminen toimitustilan mukaan</span><span class="sxs-lookup"><span data-stu-id="373ae-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="373ae-104">Tässä aiheessa kuvataan, kuinka voit määrittää mukautettuja sähköpostimalleja tiettyjä ilmoitustyyppejä ja toimitustapoja varten Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="373ae-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="373ae-105">Tapahtumakohtaisia sähköposteja voi nyt mukauttaa ilmoitustyypin (esimerkiksi **Tilauksen luonti**, **Tilaus pakattu** tai **Tilaus laskutettu**) ja toimitustavan yhdistelmän mukaan (esimerkiksi yön yli, myymälästä nouto tai nouto tien reunasta).</span><span class="sxs-lookup"><span data-stu-id="373ae-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="373ae-106">Mukautettujen tapahtumasähköpostien avulla vähittäiskauppiaat voivat tarjota asiakkailleen tilauksen toimitustavan mukaan räätälöityjä kokemuksia.</span><span class="sxs-lookup"><span data-stu-id="373ae-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="373ae-107">Esimerkiksi Tilaus pakattu -tapahtumaa voidaan mukauttaa niin, että se sisältää tien vierestä noudon ohjeet asiakkaille, jotka valitsevat tien vierestä noudon.</span><span class="sxs-lookup"><span data-stu-id="373ae-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="373ae-108">Vaihtoehtoisesti se voi tarjota rahdinkuljettajan ja toimituksen tiedot asiakkaille, jotka päättävät, että tilaus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="373ae-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="373ae-109">Jotta voisit käyttää mukautettuja tapahtumasähköposteja, sinun on ensin otettava käyttöön **Mukauta tapahtumasähköpostimallit toimitustavan mukaan** siirtymällä kohtaan **Työtilat \> Ominaisuuksien hallinta** Commerce-pääkonttorisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="373ae-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="373ae-110">Sähköposteja voi mukauttaa toimitustavan mukaan seuraaville ilmoitustyypeille:</span><span class="sxs-lookup"><span data-stu-id="373ae-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="373ae-111">**Tilauksen peruutus** – Tämä sähköposti-ilmoituksen tyyppi on uusi.</span><span class="sxs-lookup"><span data-stu-id="373ae-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="373ae-112">**Tilaus luotu**</span><span class="sxs-lookup"><span data-stu-id="373ae-112">**Order created**</span></span>
- <span data-ttu-id="373ae-113">**Tilaus vahvistettu**</span><span class="sxs-lookup"><span data-stu-id="373ae-113">**Order confirmed**</span></span>
- <span data-ttu-id="373ae-114">**Tilaus laskutettu** – Tämä sähköposti-ilmoituksen tyyppi on uusi.</span><span class="sxs-lookup"><span data-stu-id="373ae-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="373ae-115">Sitä voidaan käyttää **Tilaus lähetetty** -ilmoitustyypin asemesta, joka lähettää ilmoituksen mille tahansa laskutapahtumalle, jossa on lähetystoimitustapa (ei nouto tai sähköinen toimitustapa).</span><span class="sxs-lookup"><span data-stu-id="373ae-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="373ae-116">**Tilaus keräilty**</span><span class="sxs-lookup"><span data-stu-id="373ae-116">**Order picked**</span></span>
- <span data-ttu-id="373ae-117">**Tilaus pakattu**</span><span class="sxs-lookup"><span data-stu-id="373ae-117">**Order packed**</span></span>
- <span data-ttu-id="373ae-118">**Tilaus valmis noudettavaksi** – Tätä ilmoitus tyyppiä voi mukauttaa toimitustavan mukaan vain, jos **Useiden noutotoimitustapojen tuki** -ominaisuus on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="373ae-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="373ae-119">Tässä tapauksessa tämä ilmoitustyyppi vastaa toiminnallisesti **Tilaus pakattu** -ilmoitustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="373ae-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="373ae-120">**Maksu epäonnistui**</span><span class="sxs-lookup"><span data-stu-id="373ae-120">**Payment failed**</span></span>
- <span data-ttu-id="373ae-121">**Luotiin korvaava tilaus**</span><span class="sxs-lookup"><span data-stu-id="373ae-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="373ae-122">Tiettyjen toimitustapojen sähköpostimallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="373ae-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="373ae-123">Tässä menetelmässä oletetaan, että olet jo luonut uudet mukautetut sähköpostimallit ja lisännyt ne **Organisaation sähköpostimallit** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="373ae-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="373ae-124">Lisätietoja sähköpostimallien luomisesta ja lataamisesta palvelimeen on kohdassa [Sähköpostimallien luominen tapahtumille](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="373ae-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="373ae-125">Voit määrittää tiettyjen toimitustapojen sähköpostimallit Commerce-pääkonttorisovelluksessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="373ae-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="373ae-126">Siirry **Commerce-sähköpostiprofiili** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="373ae-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="373ae-127">Valitse aiemmin luotu ilmoitustyyppi **Vähittäismyyntitapahtuman ilmoitusasetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="373ae-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="373ae-128">Kun ilmoitustyyppi on edelleen valittuna, valitse **Määritä toimitustavat**.</span><span class="sxs-lookup"><span data-stu-id="373ae-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="373ae-129">Valitse **Toimitustavat**-valintaruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="373ae-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="373ae-130">Valitse uudella rivillä **Toimitustapa**-kentässä toimitustapa.</span><span class="sxs-lookup"><span data-stu-id="373ae-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="373ae-131">Valitse **Sähköpostin tunnus** -kentästä sähköpostimalli, jonka haluat yhdistää toimitustapaan.</span><span class="sxs-lookup"><span data-stu-id="373ae-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="373ae-132">Valitse **Käytössä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="373ae-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="373ae-133">Voit lisätä uusia toimitustapoja toistamalla vaiheet 4–7.</span><span class="sxs-lookup"><span data-stu-id="373ae-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="373ae-134">Kun olet valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="373ae-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="373ae-135">Jos myyntitilauksen riveillä on useita toimitustapoja, käytetään oletusmallia.</span><span class="sxs-lookup"><span data-stu-id="373ae-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="373ae-136">Oletusmalli on malli, joka on yhdistetty ilmoitustyyppiin **Commerce-sähköposti-ilmoituksen profiili** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="373ae-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="373ae-137">Jos myyntitilauksessa on toimitustapa, jota ei ole määritetty mukautetulle sähköpostimallille, käytetään oletussähköpostimallia.</span><span class="sxs-lookup"><span data-stu-id="373ae-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="373ae-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="373ae-138">Additional resources</span></span>

[<span data-ttu-id="373ae-139">Puhelinkeskustilausten luominen</span><span class="sxs-lookup"><span data-stu-id="373ae-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="373ae-140">Toimitustavan muuttaminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="373ae-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]