---
title: Noutomoduulin sisäänkuittaus
description: Tässä aiheessa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937580"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="c7aa1-103">Noutomoduulin sisäänkuittaus</span><span class="sxs-lookup"><span data-stu-id="c7aa1-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c7aa1-104">Tässä aiheessa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c7aa1-105">Noutomoduulin sisäänkuittaus toimii vahvistussivuna asiakkaille, jotka käyttävät Dynamics 365 Commercen asiakkaan sisäänkuittaustoimintoja ilmoittaakseen myymälälle saapumisestaan.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="c7aa1-106">Noutomoduulin sisäänkuittauksessa voi myös konfiguroida lomakkeen, joka kerää asiakkailta lisätietoja tilausten toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="c7aa1-107">Näitä tietoja ovat asiakkaan pysäköintipaikan numero sekä ajoneuvon merkki ja malli.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="c7aa1-108">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="c7aa1-108">Module properties</span></span>

| <span data-ttu-id="c7aa1-109">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="c7aa1-109">Property name</span></span> | <span data-ttu-id="c7aa1-110">Arvot</span><span class="sxs-lookup"><span data-stu-id="c7aa1-110">Values</span></span> | <span data-ttu-id="c7aa1-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="c7aa1-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c7aa1-112">Vahvistusteksti</span><span class="sxs-lookup"><span data-stu-id="c7aa1-112">Confirmation text</span></span> | <span data-ttu-id="c7aa1-113">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="c7aa1-113">Text string</span></span> | <span data-ttu-id="c7aa1-114">Sisäänkuittauksen vahvistussivulla näkyvän otsikon sisältö.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="c7aa1-115">Näytä QR-koodi</span><span class="sxs-lookup"><span data-stu-id="c7aa1-115">Show QR code</span></span> | <span data-ttu-id="c7aa1-116">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="c7aa1-116">**True** or **False**</span></span> | <span data-ttu-id="c7aa1-117">Kun ominaisuuden arvoksi määritetään **Tosi**, sisäänkuittauksen vahvistussivulla näkyy tilauksen vahvistustunnusta vastaava QR-koodi.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="c7aa1-118">Lisätieto-otsikko</span><span class="sxs-lookup"><span data-stu-id="c7aa1-118">Additional information heading</span></span> | <span data-ttu-id="c7aa1-119">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="c7aa1-119">Text string</span></span> | <span data-ttu-id="c7aa1-120">Sisältö otsikolle, joka tulee näkyviin, kun lisätietokentät on konfiguroitu.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="c7aa1-121">Lisätietoavaimet</span><span class="sxs-lookup"><span data-stu-id="c7aa1-121">Additional information keys</span></span> | <span data-ttu-id="c7aa1-122">Resurssitunnus/resurssiarvo-pari</span><span class="sxs-lookup"><span data-stu-id="c7aa1-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="c7aa1-123">Kukin avain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="c7aa1-124">Lisätietoavaimet \> Resurssitunnus</span><span class="sxs-lookup"><span data-stu-id="c7aa1-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="c7aa1-125">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="c7aa1-125">Text string</span></span> | <span data-ttu-id="c7aa1-126">Kukin tietoavain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="c7aa1-127">Tämä ominaisuus määrittää lisätietoavaimen.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-127">This property identifies the additional information key.</span></span> <span data-ttu-id="c7aa1-128">Myyntipisteessä luodussa tehtävässä tämän ominaisuuden arvo näkyy ohjeet-kentässä otsikkona.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="c7aa1-129">Lisätietoavaimet \> Resurssiarvo</span><span class="sxs-lookup"><span data-stu-id="c7aa1-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="c7aa1-130">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="c7aa1-130">Text string</span></span> | <span data-ttu-id="c7aa1-131">Myyntipisteen tehtävän tekstikentän otsikko.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="c7aa1-132">Lisätietoavaimet \> Vaaditaan</span><span class="sxs-lookup"><span data-stu-id="c7aa1-132">Additional information keys \> Required</span></span> | <span data-ttu-id="c7aa1-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="c7aa1-133">**True** or **False**</span></span> | <span data-ttu-id="c7aa1-134">Tämä ominaisuus määrittää, onko asiakkaiden täytettävä lomakekenttä ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="c7aa1-135">Kun ominaisuuden arvoksi määritetään **Tosi**, lomakkeen otsikon viereen muodostetaan tähti ja tyhjäarvon tarkistuksen tekeminen estää asiakkaita jatkamasta, jos arvoa ei ole annettu.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="c7aa1-136">Noutomoduulin sisäänkuittauksen lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="c7aa1-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="c7aa1-137">Noutomoduulin sisäänkuittaus tulee lisätä uudelle sivulle, joka luodaan sisäänkuittauksen vahvistusta varten.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="c7aa1-138">Tätä sivua käytetään sisäänkuittauksen vahvistuskokemuksena asiakkaille, jotka valitsevat sähköpostinsa **Olen paikalla** -linkin tai -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="c7aa1-139">Lisätietolomakkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c7aa1-139">Configure the additional information form</span></span>

<span data-ttu-id="c7aa1-140">Jos lisätietoavaimia ei ole määritetty, moduulissa näkyy asiakkaille oletusarvon mukaan sisäänkuittauksen vahvistussivu.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="c7aa1-141">Kun sisäänkuittauksen vahvistus on näkyvissä, myyntipistepäätteessä luodaan tehtävä myymälälle, josta tilaus kerätään.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="c7aa1-142">Kun vähintään yksi lisätietoavain on konfiguroitu, asiakkaita pyydetään syöttämään tiedot.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="c7aa1-143">Kun he valitsevat **Lähetä**, he näkevät sisäänkuittauksen vahvistuksen ja tehtävä luodaan myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="c7aa1-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c7aa1-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c7aa1-144">Additional resources</span></span>

[<span data-ttu-id="c7aa1-145">Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="c7aa1-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
