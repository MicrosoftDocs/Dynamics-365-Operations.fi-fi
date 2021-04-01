---
title: Kassavirtaennusteiden asetusten vianmääritys
description: Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita. Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232486"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="b8536-104">Kassavirtaennusteiden asetusten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="b8536-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8536-105">Tässä aiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität kassavirtaennusteita.</span><span class="sxs-lookup"><span data-stu-id="b8536-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="b8536-106">Se käsittelee usein kysyttyjä kysymyksiä kassavirran asetuksista, kassavirran päivityksistä ja kassavirran Power BI -ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="b8536-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="b8536-107">Miksi kassavirta näkyy vain yhdessä yrityksessä?</span><span class="sxs-lookup"><span data-stu-id="b8536-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="b8536-108">Kassavirtaennusteet konfiguroitaan ja lasketaan yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="b8536-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="b8536-109">Power BI -raportit ja kassavirtaennusteiden ominaisuus taloushallinnon tiedoissa osoittavat tulokset.</span><span class="sxs-lookup"><span data-stu-id="b8536-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="b8536-110">Kassavirtaennusteet on määritettävä kullekin yritykselle, jota varten haluat nähdä ennusteen.</span><span class="sxs-lookup"><span data-stu-id="b8536-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="b8536-111">Tarkista kaikkien yritysten kassavirtaennusteiden konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="b8536-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="b8536-112">Vaihtoehtoisesti voit tarkistaa kaikkien yritysten kassavirtaennusteiden konfiguraatiot ja varmistaa, että ne on määritetty suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b8536-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="b8536-113">Miksi Power BI ei näytä kaikkia kassavirtatietoja?</span><span class="sxs-lookup"><span data-stu-id="b8536-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="b8536-114">Useita vaiheita on suoritettava, ennen kuin kassavirtaennusteet voivat näkyä Power BI -näkymissä.</span><span class="sxs-lookup"><span data-stu-id="b8536-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="b8536-115">Tarkista seuraava tarkistusluettelo ja varmista, että kaikki vaiheet on suoritettu loppuun:</span><span class="sxs-lookup"><span data-stu-id="b8536-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="b8536-116">Määritä kunkin yrityksen kassavirta.</span><span class="sxs-lookup"><span data-stu-id="b8536-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="b8536-117">Määritä kirjanpitoparametreissa järjestelmän valuutta ja järjestelmän vaihtokurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="b8536-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="b8536-118">Määritä kirjanpidon valuutta ja vaihtokurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="b8536-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="b8536-119">Anna tapahtumavaluutan ja kirjanpitovaluutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="b8536-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="b8536-120">Anna kirjanpitovaluutan ja järjestelmävaluutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="b8536-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="b8536-121">Anna kirjanpitovaluutan ja kunkin pankin valuutan väliset valuutan vaihtokurssit.</span><span class="sxs-lookup"><span data-stu-id="b8536-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="b8536-122">Miksi kassavirran Power BI toimi aiemmissa versioissa, mutta on nyt tyhjä?</span><span class="sxs-lookup"><span data-stu-id="b8536-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="b8536-123">Tarkista, että yksikkösäilön mitat "Kassavirran mitta V2" ja "LedgerCovLiquidityMeasurement" on konfiguroitu.</span><span class="sxs-lookup"><span data-stu-id="b8536-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="b8536-124">Lisätietoja yksikkösäilön tietojen tarkastelemista varten on ohjeessa [Power BI:n integrointi yksikkösäilön kanssa](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Varmista, että kaikki Power BI -sisällön tarkastelemisen edellyttämät vaiheet on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="b8536-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="b8536-125">Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="b8536-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="b8536-126">Onko yksikkösäilön entiteetit päivitetty?</span><span class="sxs-lookup"><span data-stu-id="b8536-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="b8536-127">Entiteetit on päivitettävä säännöllisesti, jotta tiedot ovat ajan tasalla ja oikein.</span><span class="sxs-lookup"><span data-stu-id="b8536-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="b8536-128">Jos haluat päivittää tietyn yksikön manuaalisesti, siirry kohtaan **Järjestelmänvalvonta \> Määritys \> Yksikkösäilö** valitse yksikkö ja sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="b8536-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="b8536-129">Tiedot voidaan myös päivittää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b8536-129">The data can also be updated automatically.</span></span> <span data-ttu-id="b8536-130">Määritä **Yksikkösäilö**-sivulla **Automaattinen päivitys käytössä** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b8536-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]