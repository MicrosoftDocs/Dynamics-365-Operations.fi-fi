---
title: "Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset"
description: "Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Retail Modern -myyntipisteessä (MPOS) ja pilvimyyntipisteessä."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: b49450a7deab94c62e173f730007bc40de23b267
ms.contentlocale: fi-fi
ms.lasthandoff: 01/25/2018

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="23439-103">Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset</span><span class="sxs-lookup"><span data-stu-id="23439-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="23439-104">Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Retail Modern -myyntipisteessä (MPOS) ja pilvimyyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="23439-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="23439-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="23439-105">Overview</span></span>
<span data-ttu-id="23439-106">Retail Modern -myyntipiste (MPOS) ja pilvimyyntipiste tukevat ympäristöjä, joissa kielisetukset ja käännökset voivat vaihdella myymälän ja käyttäjäasetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="23439-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="23439-107">Esimerkiksi myymälä saattaa sijaita alueella, jossa englannin kieli on asiakkaiden yleisimmin käyttämä, mutta jotkut työntekijät käyttävät mieluummin sovellusta ranskankielisillä käännöksillä.</span><span class="sxs-lookup"><span data-stu-id="23439-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="23439-108">Tietojen kieli</span><span class="sxs-lookup"><span data-stu-id="23439-108">Data language</span></span>
<span data-ttu-id="23439-109">Käyttäjän asetuksista riippumatta, Retail Modern -myyntipiste ja pilvimyyntipiste käyttävät aina myymälän kieliasetuksia tietojen käännöksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="23439-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="23439-110">Näin voidaan varmistaa, että kaikilla käyttäjillä ja asiakkailla on yhtenevä kokemus.</span><span class="sxs-lookup"><span data-stu-id="23439-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="23439-111">Esimerkkejä tiedoista ovat:</span><span class="sxs-lookup"><span data-stu-id="23439-111">Examples of data include:</span></span>

-   <span data-ttu-id="23439-112">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="23439-112">Products</span></span>
-   <span data-ttu-id="23439-113">Määritteet ja arvot</span><span class="sxs-lookup"><span data-stu-id="23439-113">Attributes and values</span></span>
-   <span data-ttu-id="23439-114">Luokkien nimet</span><span class="sxs-lookup"><span data-stu-id="23439-114">Category names</span></span>
-   <span data-ttu-id="23439-115">Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit</span><span class="sxs-lookup"><span data-stu-id="23439-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="23439-116">Maksutapojen nimet</span><span class="sxs-lookup"><span data-stu-id="23439-116">Payment method names</span></span>
-   <span data-ttu-id="23439-117">Riveillä näytettävät sanomat</span><span class="sxs-lookup"><span data-stu-id="23439-117">Line display messages</span></span>

<span data-ttu-id="23439-118">Myymälän kieltä käytetään myös myyntipisteen pääkirjautumissivulla, koska käyttäjää ei tunneta ennen kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="23439-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="23439-119">Jos myymälän kielellä olevaa käännöstä ei ole saatavilla, myyntipiste palaa yrityksen kieleen.</span><span class="sxs-lookup"><span data-stu-id="23439-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="23439-120">Myymälän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="23439-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="23439-121">Myymälän kieliasetukset määritetään **Kaikki vähittäismyymälät**-kohdassa **Vähittäismyymälä**-sivulla kohdassa Yleinen &gt; Alueasetukset &gt; Kieli.</span><span class="sxs-lookup"><span data-stu-id="23439-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="23439-122">**Valitse kunkin myymälän kieli avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="23439-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="23439-123">Käyttöliittymän kieli</span><span class="sxs-lookup"><span data-stu-id="23439-123">User interface language</span></span>
<span data-ttu-id="23439-124">Myyntipisteen käyttäjän kieliasetukset määrittävät sovelluksen käyttöliittymässä käytettävät käännökset.</span><span class="sxs-lookup"><span data-stu-id="23439-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="23439-125">Tähän sisältyvät kaikki otsikot, valikot ja luettelot, joita ei pidetä tietoina.</span><span class="sxs-lookup"><span data-stu-id="23439-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="23439-126">Yksi poikkeus tähän on teksti, joka näytetään myyntipisteen painikeruudukoissa.</span><span class="sxs-lookup"><span data-stu-id="23439-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="23439-127">Ne eivät tue käännöksiä, joten ne näyttävät aina tekstin siten, kuin se on määritetty painikkeessa.</span><span class="sxs-lookup"><span data-stu-id="23439-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="23439-128">Jos haluat, että ne tukevat käännettyjä painikkeita, sinun on kopioitava erilliset painikeruudukot ja ylläpidettävä niitä, ja määritettävä ne soveltuville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="23439-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="23439-129">Käyttäjän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="23439-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="23439-130">Myyntipisteen kieliasetukset määritetään kohdassa **Kaikki työntekijät** **Työntekijä**-sivulla kohdassa **Vähittäismyynti &gt; Kieli**.</span><span class="sxs-lookup"><span data-stu-id="23439-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="23439-131">Sitä ei määritetä Profiilin päävälilehdellä. Myyntipiste ei käytä tätä asetusta.</span><span class="sxs-lookup"><span data-stu-id="23439-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="23439-132">Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.</span><span class="sxs-lookup"><span data-stu-id="23439-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="23439-133">** **</span><span class="sxs-lookup"><span data-stu-id="23439-133">** **</span></span>       | <span data-ttu-id="23439-134">**Käyttöliittymän kieli**</span><span class="sxs-lookup"><span data-stu-id="23439-134">**UI language** ** **</span></span>      | <span data-ttu-id="23439-135">**Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.)**</span><span class="sxs-lookup"><span data-stu-id="23439-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="23439-136">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="23439-136">**Company**</span></span> | <span data-ttu-id="23439-137">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="23439-137">Default</span></span>                    | <span data-ttu-id="23439-138">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="23439-138">Default</span></span>                                                           |
| <span data-ttu-id="23439-139">**Myymälä**</span><span class="sxs-lookup"><span data-stu-id="23439-139">**Store**</span></span>   | <span data-ttu-id="23439-140">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="23439-140">Overrides company</span></span>          | <span data-ttu-id="23439-141">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="23439-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="23439-142">**Käyttäjä**</span><span class="sxs-lookup"><span data-stu-id="23439-142">**User**</span></span>    | <span data-ttu-id="23439-143">Ohittaa myymälän tai yrityksen</span><span class="sxs-lookup"><span data-stu-id="23439-143">Overrides store or company</span></span> | <span data-ttu-id="23439-144">En koskaan</span><span class="sxs-lookup"><span data-stu-id="23439-144">Never</span></span>                                                             |






