---
title: Kassavirtaennusteiden asetusten vianmääritys
description: Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita. Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827311"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="6abf1-104">Kassavirtaennusteiden asetusten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="6abf1-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6abf1-105">Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="6abf1-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="6abf1-106">Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="6abf1-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="6abf1-107">Miksi kassavirta näkyy vain yhdessä yrityksessä?</span><span class="sxs-lookup"><span data-stu-id="6abf1-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="6abf1-108">Kassavirtaennusteet konfiguroitaan ja lasketaan yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="6abf1-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="6abf1-109">Power BI -raportit ja kassavirtaennusteiden ominaisuus taloushallinnon tiedoissa osoittavat tulokset.</span><span class="sxs-lookup"><span data-stu-id="6abf1-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="6abf1-110">Kassavirtaennusteet on määritettävä kullekin yritykselle, jota varten haluat nähdä ennusteen.</span><span class="sxs-lookup"><span data-stu-id="6abf1-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="6abf1-111">Tarkista kaikkien yritysten kassavirtaennusteiden konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="6abf1-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="6abf1-112">Vaihtoehtoisesti voit tarkistaa kaikkien yritysten kassavirtaennusteiden konfiguraatiot ja varmistaa, että ne on määritetty suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6abf1-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="6abf1-113">Miksi Power BI ei näytä kaikkia kassavirtatietoja?</span><span class="sxs-lookup"><span data-stu-id="6abf1-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="6abf1-114">Useita vaiheita on suoritettava, ennen kuin kassavirtaennusteet voivat näkyä Power BI -näkymissä.</span><span class="sxs-lookup"><span data-stu-id="6abf1-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="6abf1-115">Tarkista seuraava tarkistusluettelo ja varmista, että kaikki vaiheet on suoritettu loppuun:</span><span class="sxs-lookup"><span data-stu-id="6abf1-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="6abf1-116">Määritä kunkin yrityksen kassavirta.</span><span class="sxs-lookup"><span data-stu-id="6abf1-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="6abf1-117">Määritä kirjanpitoparametreissa järjestelmän valuutta ja järjestelmän vaihtokurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="6abf1-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="6abf1-118">Määritä kirjanpidon valuutta ja vaihtokurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="6abf1-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="6abf1-119">Anna tapahtumavaluutan ja kirjanpitovaluutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="6abf1-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="6abf1-120">Anna kirjanpitovaluutan ja järjestelmävaluutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="6abf1-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="6abf1-121">Anna kirjanpitovaluutan ja kunkin pankin valuutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="6abf1-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="6abf1-122">Miksi kassavirran Power BI toimi aiemmissa versioissa, mutta on nyt tyhjä?</span><span class="sxs-lookup"><span data-stu-id="6abf1-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="6abf1-123">Tarkista, että yksikkösäilön mitat "Kassavirran mitta V2" ja "LedgerCovLiquidityMeasurement" on konfiguroitu.</span><span class="sxs-lookup"><span data-stu-id="6abf1-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="6abf1-124">Lisätietoja yksikkösäilön tietojen ksäittelystä on kohdassa [Power BI:n ja yksikkösäilön integrointi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6abf1-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="6abf1-125">Varmista, että kaikki Power BI -sisällön tarkastelemiseen tarvittavat vaiheet on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="6abf1-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="6abf1-126">Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="6abf1-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="6abf1-127">Onko yksikkösäilön entiteetit päivitetty?</span><span class="sxs-lookup"><span data-stu-id="6abf1-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="6abf1-128">Entiteetit on päivitettävä säännöllisesti, jotta tiedot ovat ajan tasalla ja oikein.</span><span class="sxs-lookup"><span data-stu-id="6abf1-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="6abf1-129">Jos haluat päivittää tietyn yksikön manuaalisesti, siirry kohtaan **Järjestelmänvalvonta \> Määritys \> Yksikkösäilö** valitse yksikkö ja sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="6abf1-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="6abf1-130">Tiedot voidaan myös päivittää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6abf1-130">The data can also be updated automatically.</span></span> <span data-ttu-id="6abf1-131">Määritä **Yksikkösäilö**-sivulla **Automaattinen päivitys käytössä** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6abf1-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="6abf1-132">Mitä laskentamenetelmää tulisi käyttää kassavirtaennusteita laskettaessa?</span><span class="sxs-lookup"><span data-stu-id="6abf1-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="6abf1-133">Kassavirtaennusteen laskentamenetelmässä on kaksi tärkeää valintavaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="6abf1-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="6abf1-134">**Uusi**-vaihtoehto laskee kassavirtaennusteet uusille asiakirjoille ja asiakirjoille, jotka ovat muuttuneet edellisen eräajon jälkeen.</span><span class="sxs-lookup"><span data-stu-id="6abf1-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="6abf1-135">Tämä asetus suoritetaan yleensä nopeammin, koska se käsittelee pienemmän asiakirjajoukon.</span><span class="sxs-lookup"><span data-stu-id="6abf1-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="6abf1-136">**Yhteensä**-vaihtoehto laskee uudelleen kassavirtaennusteet järjestelmän jokaiselle asiakirjalle.</span><span class="sxs-lookup"><span data-stu-id="6abf1-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="6abf1-137">Tämä vaihtoehto vie enemmän aikaa, koska sillä on enemmän työtä suoritettavana.</span><span class="sxs-lookup"><span data-stu-id="6abf1-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="6abf1-138">Miten parannan kassavirtaennusteen toistuva eräajon suorituskykyä?</span><span class="sxs-lookup"><span data-stu-id="6abf1-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="6abf1-139">Suosittelemme, että kassavirtaennuste suoritetaan kerran päivässä ruuhka-aikojen ulkopuolella **Uusi**-laskentamenetelmällä.</span><span class="sxs-lookup"><span data-stu-id="6abf1-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="6abf1-140">Suosittelemme käyttämään tätä lähestymistapaa 6 päivänä viikossa.</span><span class="sxs-lookup"><span data-stu-id="6abf1-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="6abf1-141">Suorita sitten kassavirtaennuste kerran viikossa käyttämällä **Yhteensä**-laskentamenetelmää päivänä, jolloin on vähiten aktiviteettia.</span><span class="sxs-lookup"><span data-stu-id="6abf1-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

