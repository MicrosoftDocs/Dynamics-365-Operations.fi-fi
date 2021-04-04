---
title: Sähköisen raportoinnin toimittajan mallisekit
description: Tässä ohjeaiheessa on yleisiä tietoja sähköisen raportoinnin mallisekkimuotojen käyttämisestä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 72581a6d852fe6eb5b4ad894027c1f5a3b5363e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250599"
---
# <a name="electronic-reporting-sample-vendor-checks"></a><span data-ttu-id="c9de8-103">Sähköisen raportoinnin toimittajan mallisekit</span><span class="sxs-lookup"><span data-stu-id="c9de8-103">Electronic reporting sample vendor checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9de8-104">Voit muotoilla toimittajan sekkejä sähköisellä raportoinnilla.</span><span class="sxs-lookup"><span data-stu-id="c9de8-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="c9de8-105">Markkinoilla on monia pankki- ja sekkipalvelukohtaisia sekkimuotoja.</span><span class="sxs-lookup"><span data-stu-id="c9de8-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="c9de8-106">Sähköisen raportoinnin työkalusäilön maksun sekkimalliin sisältyy sekkimuotomalleja.</span><span class="sxs-lookup"><span data-stu-id="c9de8-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="c9de8-107">Näiden mallisekkien nimet ovat **Sekki keskellä (USA)** ja **Sekki ylhäällä, kanta alapuolella (USA)**.</span><span class="sxs-lookup"><span data-stu-id="c9de8-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="c9de8-108">Mitä sekkimuotoja tuetaan tällä hetkellä?</span><span class="sxs-lookup"><span data-stu-id="c9de8-108">What check formats are currently supported?</span></span>

<span data-ttu-id="c9de8-109">Tarkista Microsoft Dynamics Lifecycle Servicesin (LCS) jaetusta omaisuuskirjastosta luettelo tämän hetkisistä käytettävistä olevista tiedostoista, joiden tyyppi on **GER-määritys**.</span><span class="sxs-lookup"><span data-stu-id="c9de8-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="c9de8-110">Seuraavassa Määritettävät asetukset -osiossa on linkki ohjeaiheeseen, jossa kerrotaan, miten luodaan LCS-säilö käytettävissä olevien määritysten tarkastelua varten ja tuodaan valitut määritykset.</span><span class="sxs-lookup"><span data-stu-id="c9de8-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="c9de8-111">Microsoft Dynamics 365 Finance sisältää mallimuodon, jossa sekki on ylimmäisenä ja sen alapuolella on kaksi maksusuoritusosaa.</span><span class="sxs-lookup"><span data-stu-id="c9de8-111">Microsoft Dynamics 365 Finance includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="c9de8-112">Siinä on myös mallimuoto, jossa sekki on keskellä kahden maksusuoritusosan välissä.</span><span class="sxs-lookup"><span data-stu-id="c9de8-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="c9de8-113">Nämä mallimuodot vastaavat Deluxe-yrityssekkimuotoja.</span><span class="sxs-lookup"><span data-stu-id="c9de8-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="c9de8-114">Mitä asetuksia on määritettävä?</span><span class="sxs-lookup"><span data-stu-id="c9de8-114">What do I have to set up?</span></span>

- <span data-ttu-id="c9de8-115">Ennen sekkien tulostusta sähköisessä raportoinnissa ainakin yksi aktiivinen sekkimääritys on tuotava sähköisen raportoinnin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="c9de8-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="c9de8-116">Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="c9de8-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="c9de8-117">Kun määrität pankkitilin maksuliikenteen hallinnan sekkejä, valitse ensin **Yleinen sähköinen vientimuoto** -valintaruutu ja sitten sopiva sekkimuoto vientimuotomääritykseksi.</span><span class="sxs-lookup"><span data-stu-id="c9de8-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="c9de8-118">Määritä myös, kuinka monta luetteloriviä maksusuoritukseen tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="c9de8-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="c9de8-119">Muista, että otsikkorivit lasketaan mukaan tähän lukuun.</span><span class="sxs-lookup"><span data-stu-id="c9de8-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="c9de8-120">Kahdessa mallisekkimuodossa suositeltava luettelorivien määrän on 17.</span><span class="sxs-lookup"><span data-stu-id="c9de8-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="c9de8-121">Tämä luku kuitenkin vaihtelee sekkipaperin ja tulostinohjaimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c9de8-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="c9de8-122">Asettelu kannattaa varmistaa tulostamalla testisekki.</span><span class="sxs-lookup"><span data-stu-id="c9de8-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="c9de8-123">Tulosta sekki valitsemalla **Tulostuskoe**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c9de8-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="c9de8-124">Mallisekkimuodot toimivat parhaiten, kun **Reunukset**-asetukseksi on valittu Microsoft Excelin tulostimen lisäominaisuuksissa **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="c9de8-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="c9de8-125">Kun testisekki on luotu, ota Excel-tulosteen muokkaus käyttöön ja määritä sivun asettelu niin, että kaikkien reunusten asetus on **0** (nolla).</span><span class="sxs-lookup"><span data-stu-id="c9de8-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="c9de8-126">Vertaa sekkien testikappaletta sekkipaperiin ja säädä asetuksia, kunnes olet tyytyväinen kohdistukseen.</span><span class="sxs-lookup"><span data-stu-id="c9de8-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="c9de8-127">Kun luot maksukirjauskansiossa maksuja määritetyllä pankkitilille, sekit tulostetaan määritetyssä muodossa.</span><span class="sxs-lookup"><span data-stu-id="c9de8-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="c9de8-128">Lisätietoja on ohjeaiheessa [Sähköisen raportointimuodon muokkaaminen](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="c9de8-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]