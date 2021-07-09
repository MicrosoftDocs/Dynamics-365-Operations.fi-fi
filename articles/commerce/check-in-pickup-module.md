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
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270580"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="98b47-103">Noutomoduulin sisäänkuittaus</span><span class="sxs-lookup"><span data-stu-id="98b47-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98b47-104">Tässä aiheessa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="98b47-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="98b47-105">Noutomoduulin sisäänkuittaus toimii vahvistussivuna asiakkaille, jotka käyttävät Dynamics 365 Commercen asiakkaan sisäänkuittaustoimintoja ilmoittaakseen myymälälle saapumisestaan.</span><span class="sxs-lookup"><span data-stu-id="98b47-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="98b47-106">Noutomoduulin sisäänkuittauksessa voi myös konfiguroida lomakkeen, joka kerää asiakkailta lisätietoja tilausten toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="98b47-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="98b47-107">Näitä tietoja ovat asiakkaan pysäköintipaikan numero sekä ajoneuvon merkki ja malli.</span><span class="sxs-lookup"><span data-stu-id="98b47-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="98b47-108">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="98b47-108">Module properties</span></span>

| <span data-ttu-id="98b47-109">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="98b47-109">Property name</span></span> | <span data-ttu-id="98b47-110">Arvot</span><span class="sxs-lookup"><span data-stu-id="98b47-110">Values</span></span> | <span data-ttu-id="98b47-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="98b47-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="98b47-112">Vahvistusteksti</span><span class="sxs-lookup"><span data-stu-id="98b47-112">Confirmation text</span></span> | <span data-ttu-id="98b47-113">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="98b47-113">Text string</span></span> | <span data-ttu-id="98b47-114">Sisäänkuittauksen vahvistussivulla näkyvän otsikon sisältö.</span><span class="sxs-lookup"><span data-stu-id="98b47-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="98b47-115">Näytä QR-koodi</span><span class="sxs-lookup"><span data-stu-id="98b47-115">Show QR code</span></span> | <span data-ttu-id="98b47-116">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="98b47-116">**True** or **False**</span></span> | <span data-ttu-id="98b47-117">Kun ominaisuuden arvoksi määritetään **Tosi**, sisäänkuittauksen vahvistussivulla näkyy tilauksen vahvistustunnusta vastaava QR-koodi.</span><span class="sxs-lookup"><span data-stu-id="98b47-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="98b47-118">Lisätieto-otsikko</span><span class="sxs-lookup"><span data-stu-id="98b47-118">Additional information heading</span></span> | <span data-ttu-id="98b47-119">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="98b47-119">Text string</span></span> | <span data-ttu-id="98b47-120">Sisältö otsikolle, joka tulee näkyviin, kun lisätietokentät on konfiguroitu.</span><span class="sxs-lookup"><span data-stu-id="98b47-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="98b47-121">Lisätietoavaimet</span><span class="sxs-lookup"><span data-stu-id="98b47-121">Additional information keys</span></span> | <span data-ttu-id="98b47-122">Resurssitunnus/resurssiarvo-pari</span><span class="sxs-lookup"><span data-stu-id="98b47-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="98b47-123">Kukin avain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="98b47-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="98b47-124">Lisätietoavaimet \> Resurssitunnus</span><span class="sxs-lookup"><span data-stu-id="98b47-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="98b47-125">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="98b47-125">Text string</span></span> | <span data-ttu-id="98b47-126">Kukin tietoavain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta.</span><span class="sxs-lookup"><span data-stu-id="98b47-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="98b47-127">Tämä ominaisuus määrittää lisätietoavaimen.</span><span class="sxs-lookup"><span data-stu-id="98b47-127">This property identifies the additional information key.</span></span> <span data-ttu-id="98b47-128">Myyntipisteessä luodussa tehtävässä tämän ominaisuuden arvo näkyy ohjeet-kentässä otsikkona.</span><span class="sxs-lookup"><span data-stu-id="98b47-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="98b47-129">Lisätietoavaimet \> Resurssiarvo</span><span class="sxs-lookup"><span data-stu-id="98b47-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="98b47-130">Tekstimerkkijono</span><span class="sxs-lookup"><span data-stu-id="98b47-130">Text string</span></span> | <span data-ttu-id="98b47-131">Myyntipisteen tehtävän tekstikentän otsikko.</span><span class="sxs-lookup"><span data-stu-id="98b47-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="98b47-132">Lisätietoavaimet \> Vaaditaan</span><span class="sxs-lookup"><span data-stu-id="98b47-132">Additional information keys \> Required</span></span> | <span data-ttu-id="98b47-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="98b47-133">**True** or **False**</span></span> | <span data-ttu-id="98b47-134">Tämä ominaisuus määrittää, onko asiakkaiden täytettävä lomakekenttä ennen jatkamista.</span><span class="sxs-lookup"><span data-stu-id="98b47-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="98b47-135">Kun ominaisuuden arvoksi määritetään **Tosi**, lomakkeen otsikon viereen muodostetaan tähti ja tyhjäarvon tarkistuksen tekeminen estää asiakkaita jatkamasta, jos arvoa ei ole annettu.</span><span class="sxs-lookup"><span data-stu-id="98b47-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="98b47-136">Noutomoduulin sisäänkuittauksen lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="98b47-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="98b47-137">Noutomoduulin sisäänkuittaus tulee lisätä uudelle sivulle, joka luodaan sisäänkuittauksen vahvistusta varten.</span><span class="sxs-lookup"><span data-stu-id="98b47-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="98b47-138">Tätä sivua käytetään sisäänkuittauksen vahvistuskokemuksena asiakkaille, jotka valitsevat sähköpostinsa **Olen paikalla** -linkin tai -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="98b47-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="98b47-139">Lisätietolomakkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="98b47-139">Configure the additional information form</span></span>

<span data-ttu-id="98b47-140">Jos lisätietoavaimia ei ole määritetty, moduulissa näkyy asiakkaille oletusarvon mukaan sisäänkuittauksen vahvistussivu.</span><span class="sxs-lookup"><span data-stu-id="98b47-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="98b47-141">Kun sisäänkuittauksen vahvistus on näkyvissä, myyntipistepäätteessä luodaan tehtävä myymälälle, josta tilaus kerätään.</span><span class="sxs-lookup"><span data-stu-id="98b47-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="98b47-142">Kun vähintään yksi lisätietoavain on konfiguroitu, asiakkaita pyydetään syöttämään tiedot.</span><span class="sxs-lookup"><span data-stu-id="98b47-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="98b47-143">Kun he valitsevat **Lähetä**, he näkevät sisäänkuittauksen vahvistuksen ja tehtävä luodaan myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="98b47-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="98b47-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="98b47-144">Additional resources</span></span>

[<span data-ttu-id="98b47-145">Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="98b47-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
