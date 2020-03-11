---
title: Sähköpostin ilmoitusprofiilin määrittäminen
description: Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 320f21916a5f451ebf4f21e0075017a121ba6d6a
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057611"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="bd806-103">Sähköpostin ilmoitusprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bd806-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bd806-104">Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="bd806-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bd806-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bd806-105">Overview</span></span>

<span data-ttu-id="bd806-106">Ennen kanavien luomista kannattaa määrittää profiili sen varmistamiseksi, että sähköposti-ilmoituksia voidaan lähettää eri tapahtumia, kuten tilausten luomista, tilauksen lähetystilaa ja epäonnistuneita maksuja varten.</span><span class="sxs-lookup"><span data-stu-id="bd806-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="bd806-107">Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="bd806-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="bd806-108">Sähköpostin ilmoitusprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="bd806-108">Create an email notification profile</span></span>

<span data-ttu-id="bd806-109">Luo sähköposti-ilmoitusprofiili noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="bd806-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="bd806-110">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.</span><span class="sxs-lookup"><span data-stu-id="bd806-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="bd806-111">Napsauta Toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bd806-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="bd806-112">Anna **Sähköposti-ilmoitusprofiili**-kentässä profiilille nimi.</span><span class="sxs-lookup"><span data-stu-id="bd806-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="bd806-113">Syötä **Kuvaus**-kenttään asianmukainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bd806-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="bd806-114">Aseta **Aktiivinen**-kytkin asentoon **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bd806-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="bd806-115">Luo sähköpostimalli</span><span class="sxs-lookup"><span data-stu-id="bd806-115">Create an email template</span></span>

<span data-ttu-id="bd806-116">Ennen kuin sähköposti-ilmoitus voidaan luoda, sinun on luotava organisaation sähköpostimalli, joka sisältää lähettäjän sähköpostitiedot ja sähköpostimallin.</span><span class="sxs-lookup"><span data-stu-id="bd806-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="bd806-117">Voit luoda sähköpostimallin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bd806-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="bd806-118">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="bd806-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="bd806-119">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bd806-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bd806-120">Anna **Sähköpostitunnus** kentässä tunnus auttamaan tämän mallin tunnistamisessa.</span><span class="sxs-lookup"><span data-stu-id="bd806-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="bd806-121">Kirjoita **Lähettäjän nimi**-kenttään lähettäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="bd806-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="bd806-122">Syötä **Sähköpostin kuvaus**-kenttään asianmukainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bd806-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="bd806-123">Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="bd806-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="bd806-124">Täytä **Yleiset** -osaan kaikki tarvittavat valinnaiset tiedot (kuten sähköpostin prioriteetti).</span><span class="sxs-lookup"><span data-stu-id="bd806-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="bd806-125">Laajenna **Sähköpostiviestin sisältö** -osa ja valitse **Uusi**, kun haluat luoda mallin sisällön.</span><span class="sxs-lookup"><span data-stu-id="bd806-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="bd806-126">Valitse kunkin sisällön kohteen osalta kieli ja sähköpostiviestin aiherivi.</span><span class="sxs-lookup"><span data-stu-id="bd806-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="bd806-127">Jos sähköpostiin tulee teksti, varmista, että **Leipäteksti on** -ruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="bd806-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="bd806-128">Valitse toimintoruudussa **Sähköpostiviesti** määrittääksesi sähköpostin leipätekstimallin.</span><span class="sxs-lookup"><span data-stu-id="bd806-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="bd806-129">Seuraavassa kuvassa näkyy esimerkkejä sähköpostimallin asetuksista.</span><span class="sxs-lookup"><span data-stu-id="bd806-129">The following image shows some example email template settings.</span></span>

![Sähköpostimallin asetukset](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="bd806-131">Luo sähköpostitapahtuma</span><span class="sxs-lookup"><span data-stu-id="bd806-131">Create an email event</span></span>

<span data-ttu-id="bd806-132">Voit luoda sähköpostitapahtuman seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bd806-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="bd806-133">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.</span><span class="sxs-lookup"><span data-stu-id="bd806-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="bd806-134">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bd806-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="bd806-135">Valitse sähköpostimalliryhmän avattavasta **Sähköpostitunnus**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="bd806-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="bd806-136">Valitse avattavasta luettelosta asianmukainen **Sähköposti-ilmoitustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="bd806-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="bd806-137">Valitse **Käytössä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="bd806-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="bd806-138">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="bd806-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bd806-139">Seuraavassa kuvassa näkyy esimerkkejä tapahtuman ilmoitusasetuksista.</span><span class="sxs-lookup"><span data-stu-id="bd806-139">The following image shows some example event notification settings.</span></span>

![Tapahtuman ilmoitusasetukset](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="bd806-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bd806-141">Additional resources</span></span>

[<span data-ttu-id="bd806-142">Sähköpostiviestin määrittäminen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="bd806-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="bd806-143">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bd806-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="bd806-144">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="bd806-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="bd806-145">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bd806-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
