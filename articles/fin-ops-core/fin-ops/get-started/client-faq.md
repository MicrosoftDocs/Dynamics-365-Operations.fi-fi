---
title: Asiakasohjelmasta usein kysytyt kysymykset
description: Tässä artikkelissa on vastauksia Finance and Operations -asiakasohjelmaa koskeviin usein kysyttyihin kysymyksiin.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc6b1a56c2ad4b109d6658bcb66416102e091e54
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180757"
---
# <a name="client-faq"></a><span data-ttu-id="12909-103">Asiakasohjelmasta usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="12909-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12909-104">Tässä artikkelissa on vastauksia Finance and Operations -asiakasohjelmaa koskeviin usein kysyttyihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="12909-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="12909-105">Miksi symbolit eivät latautuneet?</span><span class="sxs-lookup"><span data-stu-id="12909-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="12909-106">Selaimesi suojausasetukset voivat estää symbolien oikein lataamisen.</span><span class="sxs-lookup"><span data-stu-id="12909-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="12909-107">Voit ratkaista tämän ongelman yrittämällä seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="12909-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="12909-108">Jos ongelma ilmenee Internet Exploreria käytettäessä, valitse ensin **Työkalut** ja sitten **Internet-asetukset**.</span><span class="sxs-lookup"><span data-stu-id="12909-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="12909-109">Valitse Internet-asetukset-valintaikkunassa **Tietosuoja**-välilehdessä **Mukautettu taso**, ja varmista, että **Fonttien lataaminen** -vaihtoehto on valittuna.</span><span class="sxs-lookup"><span data-stu-id="12909-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="12909-110">Muussa tapauksessa sinun on lisättävä sovelluksen sivusto luotettujen sivustojen luetteloon.</span><span class="sxs-lookup"><span data-stu-id="12909-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="12909-111">Dynamics AX 2012:ssä ei ole valintanauhaa</span><span class="sxs-lookup"><span data-stu-id="12909-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="12909-112">Voinko pitää toimintoruudun välilehdet aina auki?</span><span class="sxs-lookup"><span data-stu-id="12909-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="12909-113">Olemme aikeissa toteuttaa tämän ominaisuuden pian.</span><span class="sxs-lookup"><span data-stu-id="12909-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="12909-114">Käyttäjät voivat sitten halutessaan pitää välilehtien toimintoruudut aina avattuina.</span><span class="sxs-lookup"><span data-stu-id="12909-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="12909-115">Muussa tapauksessa välilehdet painuvat kokoon, kun niitä ei käytetä, jotta sivun näyttötilaa voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="12909-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="12909-116">Miksi näen joskus eri pikavalikon, kun napsautan hiiren kakkospainiketta?</span><span class="sxs-lookup"><span data-stu-id="12909-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="12909-117">Jos napsautat hiiren kakkospainikkeella muokattavaa kenttää (tai jos teksti on valittu), selaimen pikavalikko ilmestyy näkyviin.</span><span class="sxs-lookup"><span data-stu-id="12909-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="12909-118">Tämän valikon avulla voiy käyttää **leikkaa**, **kopioi** ja **liitä** komentoja.</span><span class="sxs-lookup"><span data-stu-id="12909-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="12909-119">Microsoft ei voi upottaa komentoja pikavalikkoihin, koska turvallisuussyistä selaimet eivät salli ohjelmallista pääsyä järjestelmän leikepöydälle.</span><span class="sxs-lookup"><span data-stu-id="12909-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="12909-120">Jos kaksoisnapsautat kenttäotsikkoa tai ohjausobjektin vain luku -arvoa, näkyviin tulee pikavalikko.</span><span class="sxs-lookup"><span data-stu-id="12909-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="12909-121">Näppäimistön käyttämisen helpottamiseksi aiomme tulevaisuudessa ottaa käyttöön pikanäppäimen, joka avaa pikavalikon.</span><span class="sxs-lookup"><span data-stu-id="12909-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="12909-122">Missä on Näytä tiedot -toiminto?</span><span class="sxs-lookup"><span data-stu-id="12909-122">Where is the View details functionality?</span></span>

<span data-ttu-id="12909-123">**Näytä tiedot** -vaihtoehtoa voi käyttää useilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="12909-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="12909-124">Jos ohjausobjektissa on **Näytä tiedot**-valmius ja ohjausobjektilla on arvo, kyseinen arvo näytetään hyperlinkkinä.</span><span class="sxs-lookup"><span data-stu-id="12909-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="12909-125">Napsauttamalla hyperlinkkiä voit avata sivun, jossa on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="12909-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="12909-126">**Näytä tiedot** on myös pikavalikkojen vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="12909-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="12909-127">Edellisessä osassa on lisätietoja siitä, milloin pikavalikot tulee näkyviin hiiren oikealla painikkeella napsautettaessa.</span><span class="sxs-lookup"><span data-stu-id="12909-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>
