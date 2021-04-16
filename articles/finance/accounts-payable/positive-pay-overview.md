---
title: Positive pay -yhteenveto
description: Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä.
author: panolte
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c72b50c3becb305cff6e21bc281962f5372bc273
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828007"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="ea8cd-103">Positive pay -yhteenveto</span><span class="sxs-lookup"><span data-stu-id="ea8cd-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea8cd-104">Tässä artikkelissa on tietoja Positive pay -palvelusta, jonka avulla luodaan pankille esitettävä sähköinen luettelo sekeistä.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="ea8cd-105">Positive pay -palvelun avulla luodaan pankille esitettävä sähköinen luettelo sekeistä.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="ea8cd-106">Positive pay -tiedostot auttavat pankkeja estämään sekkipetoksia.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="ea8cd-107">Kun määrität Positive pay -toiminnon, sekeistä luodaan sähköinen luettelo aina, kun sekkejä tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="ea8cd-108">Kun sekki esitetään pankille, pankki vertaa sekkiä aiemmin lähetettyyn sekkiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="ea8cd-109">Jos sekki on sama kuin luettelossa, pankki selvittää sekin.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="ea8cd-110">Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="ea8cd-111">Positiivisesta maksusta käytetään myös nimitystä SafePay.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="ea8cd-112">Positiiviset maksutiedostot voivat sisältää luottamuksellisia tietoja maksun saajista ja sekkisummista.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="ea8cd-113">Varmista tämän vuoksi, että käytät riittäviä suojaustoimenpiteitä tiedostojen luontihetkestä pankin vastaanottoon asti.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="ea8cd-114">Positive pay -tiedostot ladataan verkkoselaimen latausohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="ea8cd-115">Positive pay -tiedostot luodaan käyttämällä tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="ea8cd-116">Ennen kuin voit luoda Positive pay -tiedoston, määritä XML-muuntomuodot, jotka kääntävät tiedot pankin käyttämään muotoon.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="ea8cd-117">Jokaiselle pankkitilille, jolle halutaan luoda Positive pay -tietoja, on määritettävä Positive pay -muoto.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="ea8cd-118">Kun olet luonut maksuja, voit luoda Positive pay -tiedoston yksittäiselle yritykselle ja yksittäiselle pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="ea8cd-119">Voit myös luoda Positive pay -tiedostoja useille yrityksille ja pankkitileille samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="ea8cd-120">Kun positive pay -tiedostossa listatut sekit on maksettu, saat pankiltasi vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="ea8cd-121">Voit sitten vahvistaa Positive Pay -tiedoston järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="ea8cd-122">Jos haluat muuttaa Positive pay -tiedosto, voit kutsua sen takaisin.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="ea8cd-123">Jokaisen Positive pay -tiedostossa olevan sekin kenttä ilmaisee, onko Positive pay -tiedostoon sisältyvä sekki peruutettu.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="ea8cd-124">Lisätietoja: [Määritä ja luo Positive Pay -tiedostoja](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="ea8cd-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]