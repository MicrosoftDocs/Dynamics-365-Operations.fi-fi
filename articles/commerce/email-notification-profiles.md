---
title: Sähköpostin ilmoitusprofiilin määrittäminen
description: Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792654"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="48f78-103">Sähköposti-ilmoitusprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48f78-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48f78-104">Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="48f78-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="48f78-105">Kun luot kanavia, voit määrittää sähköposti-ilmoitusprofiilin.</span><span class="sxs-lookup"><span data-stu-id="48f78-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="48f78-106">Näin asiakkaille voidaan lähettää sähköposteja erilaisista tapahtumista, kuten tilausten luomisesta, tilausten lähetystilasta ja maksuvirheistä.</span><span class="sxs-lookup"><span data-stu-id="48f78-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="48f78-107">Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="48f78-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="48f78-108">Sähköpostin ilmoitusprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="48f78-108">Create an email notification profile</span></span>

<span data-ttu-id="48f78-109">Luo sähköposti-ilmoitusprofiili noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="48f78-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="48f78-110">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.</span><span class="sxs-lookup"><span data-stu-id="48f78-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="48f78-111">Napsauta Toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="48f78-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="48f78-112">Anna **Sähköposti-ilmoitusprofiili**-kentässä profiilille nimi.</span><span class="sxs-lookup"><span data-stu-id="48f78-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="48f78-113">Syötä **Kuvaus**-kenttään asianmukainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="48f78-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="48f78-114">Aseta **Aktiivinen**-kytkin asentoon **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="48f78-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="48f78-115">Luo sähköpostimalli</span><span class="sxs-lookup"><span data-stu-id="48f78-115">Create an email template</span></span>

<span data-ttu-id="48f78-116">Ennen sähköposti-ilmoitustyypin käyttöä on luotava organisaation sähköpostimalli Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="48f78-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="48f78-117">Tässä mallissa määritetään kullakin tuettavalla kielellä sähköpostien aihe, lähettäjä, oletuskieli ja sähköpostin perusteksti.</span><span class="sxs-lookup"><span data-stu-id="48f78-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="48f78-118">Voit luoda sähköpostimallin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="48f78-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="48f78-119">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="48f78-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="48f78-120">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="48f78-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="48f78-121">Anna **Sähköpostitunnus** kentässä tunnus auttamaan tämän mallin tunnistamisessa.</span><span class="sxs-lookup"><span data-stu-id="48f78-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="48f78-122">Kirjoita **Lähettäjän nimi**-kenttään lähettäjän nimi.</span><span class="sxs-lookup"><span data-stu-id="48f78-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="48f78-123">Syötä **Sähköpostin kuvaus**-kenttään asianmukainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="48f78-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="48f78-124">Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="48f78-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="48f78-125">Valitse **Yleiset**-osasta sähköpostimallin oletuskieli.</span><span class="sxs-lookup"><span data-stu-id="48f78-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="48f78-126">Oletuskieltä käytetään, kun määritetyllä kielellä ei ole lokalisoitua mallia.</span><span class="sxs-lookup"><span data-stu-id="48f78-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="48f78-127">Laajenna **Sähköpostiviestin sisältö** -osa ja valitse **Uusi**, kun haluat luoda mallin sisällön.</span><span class="sxs-lookup"><span data-stu-id="48f78-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="48f78-128">Valitse kunkin sisällön kohteen osalta kieli ja sähköpostiviestin aiherivi.</span><span class="sxs-lookup"><span data-stu-id="48f78-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="48f78-129">Jos sähköpostiin tulee teksti, varmista, että **Leipäteksti on** -ruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="48f78-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="48f78-130">Valitse toimintoruudussa **Sähköpostiviesti** määrittääksesi sähköpostin leipätekstimallin.</span><span class="sxs-lookup"><span data-stu-id="48f78-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="48f78-131">Seuraavassa kuvassa näkyy esimerkkejä sähköpostimallin asetuksista.</span><span class="sxs-lookup"><span data-stu-id="48f78-131">The following image shows some example email template settings.</span></span>

![Sähköpostimallin asetukset](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="48f78-133">Luo sähköpostitapahtuma</span><span class="sxs-lookup"><span data-stu-id="48f78-133">Create an email event</span></span>

<span data-ttu-id="48f78-134">Voit luoda sähköpostitapahtuman seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="48f78-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="48f78-135">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.</span><span class="sxs-lookup"><span data-stu-id="48f78-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="48f78-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="48f78-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="48f78-137">Valitse sähköpostimalliryhmän avattavasta **Sähköpostitunnus**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="48f78-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="48f78-138">Valitse avattavasta luettelosta asianmukainen **Sähköposti-ilmoitustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="48f78-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="48f78-139">Valitse **Käytössä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="48f78-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="48f78-140">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="48f78-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="48f78-141">Seuraavassa kuvassa näkyy esimerkkejä tapahtuman ilmoitusasetuksista.</span><span class="sxs-lookup"><span data-stu-id="48f78-141">The following image shows some example event notification settings.</span></span>

![Tapahtuman ilmoitusasetukset](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="48f78-143">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="48f78-143">Next steps</span></span>

<span data-ttu-id="48f78-144">Ennen kuin voit lähettää viestejä, sinun on määritettävä lähtevä postipalvelu ja määritettävä erätyö.</span><span class="sxs-lookup"><span data-stu-id="48f78-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="48f78-145">Lisätietoja on kohdassa [Sähköpostin lähettäminen ja määrittäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="48f78-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="48f78-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="48f78-146">Additional resources</span></span>

[<span data-ttu-id="48f78-147">Sähköpostiviestin määrittäminen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="48f78-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="48f78-148">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="48f78-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="48f78-149">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="48f78-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="48f78-150">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="48f78-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
