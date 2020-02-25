---
title: Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset
description: Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49bfcaa4c05ea8e6cc6bf0a8f855f2474cea35bc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022446"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="514a5-103">Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset</span><span class="sxs-lookup"><span data-stu-id="514a5-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="514a5-104">Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.</span><span class="sxs-lookup"><span data-stu-id="514a5-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="514a5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="514a5-105">Overview</span></span>
<span data-ttu-id="514a5-106">Modern POS (MPOS) ja Cloud POS tukevat ympäristöjä, joissa kielisetukset ja käännökset voivat vaihdella myymälän ja käyttäjäasetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="514a5-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="514a5-107">Esimerkiksi myymälä saattaa sijaita alueella, jossa englannin kieli on asiakkaiden yleisimmin käyttämä, mutta jotkut työntekijät käyttävät mieluummin sovellusta ranskankielisillä käännöksillä.</span><span class="sxs-lookup"><span data-stu-id="514a5-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="514a5-108">Tietojen kieli</span><span class="sxs-lookup"><span data-stu-id="514a5-108">Data language</span></span>

<span data-ttu-id="514a5-109">Käyttäjän asetuksista riippumatta, MPOS ja Cloud POS käyttävät aina myymälän kieliasetuksia tietojen käännöksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="514a5-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="514a5-110">Näin voidaan varmistaa, että kaikilla käyttäjillä ja asiakkailla on yhtenevä kokemus.</span><span class="sxs-lookup"><span data-stu-id="514a5-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="514a5-111">Esimerkkejä tiedoista ovat:</span><span class="sxs-lookup"><span data-stu-id="514a5-111">Examples of data include:</span></span>

- <span data-ttu-id="514a5-112">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="514a5-112">Products</span></span>
- <span data-ttu-id="514a5-113">Määritteet ja arvot</span><span class="sxs-lookup"><span data-stu-id="514a5-113">Attributes and values</span></span>
- <span data-ttu-id="514a5-114">Luokkien nimet</span><span class="sxs-lookup"><span data-stu-id="514a5-114">Category names</span></span>
- <span data-ttu-id="514a5-115">Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit</span><span class="sxs-lookup"><span data-stu-id="514a5-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="514a5-116">Maksutapojen nimet</span><span class="sxs-lookup"><span data-stu-id="514a5-116">Payment method names</span></span>
- <span data-ttu-id="514a5-117">Riveillä näytettävät sanomat</span><span class="sxs-lookup"><span data-stu-id="514a5-117">Line display messages</span></span>

<span data-ttu-id="514a5-118">Myymälän kieltä käytetään myös myyntipisteen pääkirjautumissivulla, koska käyttäjää ei tunneta ennen kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="514a5-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="514a5-119">Jos myymälän kielellä olevaa käännöstä ei ole saatavilla, myyntipiste palaa yrityksen kieleen.</span><span class="sxs-lookup"><span data-stu-id="514a5-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="514a5-120">Myymälän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="514a5-120">Configuring the store's language setting</span></span>

<span data-ttu-id="514a5-121">Myymälän kieliasetukset määritetään **Kaikki myymälät** -kohdassa **Myymälä**-sivulla valitsemalla **Yleinen &gt; Alueasetukset &gt; Kieli**.</span><span class="sxs-lookup"><span data-stu-id="514a5-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="514a5-122">Valitse kunkin myymälän kieli avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="514a5-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="514a5-123">Käyttöliittymän kieli</span><span class="sxs-lookup"><span data-stu-id="514a5-123">User interface language</span></span>

<span data-ttu-id="514a5-124">Myyntipisteen käyttäjän kieliasetukset määrittävät sovelluksen käyttöliittymässä käytettävät käännökset.</span><span class="sxs-lookup"><span data-stu-id="514a5-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="514a5-125">Tähän sisältyvät kaikki otsikot, valikot ja luettelot, joita ei pidetä tietoina.</span><span class="sxs-lookup"><span data-stu-id="514a5-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="514a5-126">Yksi poikkeus tähän on teksti, joka näytetään myyntipisteen painikeruudukoissa.</span><span class="sxs-lookup"><span data-stu-id="514a5-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="514a5-127">Ne eivät tue käännöksiä, joten ne näyttävät aina tekstin siten, kuin se on määritetty painikkeessa.</span><span class="sxs-lookup"><span data-stu-id="514a5-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="514a5-128">Jos haluat, että ne tukevat käännettyjä painikkeita, sinun on kopioitava erilliset painikeruudukot ja ylläpidettävä niitä, ja määritettävä ne soveltuville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="514a5-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="514a5-129">Käyttäjän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="514a5-129">Configuring the user's language setting</span></span>

<span data-ttu-id="514a5-130">Myyntipisteen kieliasetukset määritetään kohdassa **Työntekijä**-sivun **Kaikki työntekijät** -kohdassa valitsemalla **Retail ja Commerce &gt; Kieli**.</span><span class="sxs-lookup"><span data-stu-id="514a5-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="514a5-131">Sitä ei määritetä profiilin päävälilehdellä. Myyntipiste ei käytä tätä asetusta.</span><span class="sxs-lookup"><span data-stu-id="514a5-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="514a5-132">Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.</span><span class="sxs-lookup"><span data-stu-id="514a5-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="514a5-133">Käyttöliittymän kieli   </span><span class="sxs-lookup"><span data-stu-id="514a5-133">UI language</span></span>                | <span data-ttu-id="514a5-134">Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.)</span><span class="sxs-lookup"><span data-stu-id="514a5-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="514a5-135">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="514a5-135">**Company**</span></span> | <span data-ttu-id="514a5-136">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="514a5-136">Default</span></span>                    | <span data-ttu-id="514a5-137">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="514a5-137">Default</span></span>                                                       |
| <span data-ttu-id="514a5-138">**Myymälä**</span><span class="sxs-lookup"><span data-stu-id="514a5-138">**Store**</span></span>   | <span data-ttu-id="514a5-139">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="514a5-139">Overrides company</span></span>          | <span data-ttu-id="514a5-140">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="514a5-140">Overrides company</span></span>                                             |
| <span data-ttu-id="514a5-141">**Käyttäjä**</span><span class="sxs-lookup"><span data-stu-id="514a5-141">**User**</span></span>    | <span data-ttu-id="514a5-142">Ohittaa myymälän tai yrityksen</span><span class="sxs-lookup"><span data-stu-id="514a5-142">Overrides store or company</span></span> | <span data-ttu-id="514a5-143">En koskaan</span><span class="sxs-lookup"><span data-stu-id="514a5-143">Never</span></span>                                                         |
