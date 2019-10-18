---
title: Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansiossa
description: Tässä ohjeaiheessa tapaa, jolla **Ota käyttöön viivästyneen veron laskeminen kirjauskansiossa** -toiminnolla voi tehostaa veron laskemista, kun kirjauskansiossa on erittäin suuri määrä rivejä.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177497"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="6f144-103">Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansiossa</span><span class="sxs-lookup"><span data-stu-id="6f144-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6f144-104">Tässä ohjeaiheessa tapaa, jolla **Ota käyttöön viivästyneen veron laskeminen kirjauskansiossa** -toiminnolla voi tehostaa veron laskemista, kun kirjauskansiossa on erittäin suuri määrä rivejä.</span><span class="sxs-lookup"><span data-stu-id="6f144-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="6f144-105">Tällä hetkellä arvonlisäveron laskenta käynnistyy kirjauskansiossa, kun käyttäjä päivittää veroon liittyviä kenttiä, kuten arvonlisäveroryhmän tai nimikkeen arvonlisäveroryhmän.</span><span class="sxs-lookup"><span data-stu-id="6f144-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="6f144-106">Aina kun kirjauskansion rivitasolla tehdään päivitys, kaikkien kirjauskansion rivien verosumma lasketaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6f144-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="6f144-107">Käyttäjä näkee tällä tavoin reaaliaikaisen lasketun verosumman, mutta seurauksena voi olla suorituskykyongelmia, jos kirjauskansiossa on erittäin paljon rivejä.</span><span class="sxs-lookup"><span data-stu-id="6f144-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="6f144-108">Tämä toiminto antaa mahdollisuuden ratkaista suorituskykyongelma viivästyttämällä veron laskentaa.</span><span class="sxs-lookup"><span data-stu-id="6f144-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="6f144-109">Jos tämä ominaisuus on otettu käyttöön, verosumma lasketaan vain silloin, kun käyttäjä valitsee Arvonlisävero-komennon tai tekee kirjauksen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="6f144-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="6f144-110">Käyttäjä voi ottaa parametrin käyttöön tai poistaa sen käytöstä kolmella tasolla:</span><span class="sxs-lookup"><span data-stu-id="6f144-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="6f144-111">Yrityskohtainen</span><span class="sxs-lookup"><span data-stu-id="6f144-111">By legal entity</span></span>
- <span data-ttu-id="6f144-112">Kirjauskansion nimen perusteella</span><span class="sxs-lookup"><span data-stu-id="6f144-112">By journal name</span></span>
- <span data-ttu-id="6f144-113">Kirjauskansion otsikon perusteella</span><span class="sxs-lookup"><span data-stu-id="6f144-113">By journal header</span></span>

<span data-ttu-id="6f144-114">Järjestelmän pitää kirjauskansion otsikossa olevaa parametrin arvoa lopullisena.</span><span class="sxs-lookup"><span data-stu-id="6f144-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="6f144-115">Kirjauskansion otsikon parametrin oletusarvo saadaan kirjauskansion nimestä.</span><span class="sxs-lookup"><span data-stu-id="6f144-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="6f144-116">Kirjauskansion nimen parametrin oletusarvo saadaan kirjanpitoparametrista kirjauskansion nimen luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6f144-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="6f144-117">Kirjauskansion Toteutunut arvonlisäverosumma- ja Laskettu arvonlisäveron summa -kentät piilotetaan, jos tämä parametri on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6f144-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="6f144-118">Tällä tavoin voidaan estää sekaannukset, koska ennen veron laskemisen käynnistämistä näiden kahden kentän arvo on aina 0.</span><span class="sxs-lookup"><span data-stu-id="6f144-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="6f144-119">Yrityskohtaisen viivästyneen veron laskemisen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6f144-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="6f144-120">Valitse **Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="6f144-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="6f144-121">Valitse **Arvonlisävero**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6f144-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="6f144-122">Etsi **Yleiset**-välilehdessä parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6f144-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="6f144-123">Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansion nimen perusteella</span><span class="sxs-lookup"><span data-stu-id="6f144-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="6f144-124">Valitse **Kirjanpito > Kirjauskansion asetukset > Kirjauskansioiden nimet**.</span><span class="sxs-lookup"><span data-stu-id="6f144-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="6f144-125">Etsi **Yleiset**-välilehdessä parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6f144-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="6f144-126">Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansion perusteella</span><span class="sxs-lookup"><span data-stu-id="6f144-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="6f144-127">Valitse **Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="6f144-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="6f144-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6f144-128">Click **New**</span></span>
3. <span data-ttu-id="6f144-129">Valitse kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="6f144-129">Select a journal name</span></span>
4. <span data-ttu-id="6f144-130">Valitse **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f144-130">Click **Setup**</span></span>
5. <span data-ttu-id="6f144-131">Etsi parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6f144-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
