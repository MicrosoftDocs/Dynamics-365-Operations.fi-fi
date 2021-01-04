---
title: Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)
description: Tässä ohjeaiheessa kuvataan määritysvaiheet, jotka on suoritettava, jotta ulkoiset tiedot voidaan syöttää tai tuoda kassavirtaennusteisiin.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644942"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="ed6a0-103">Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ed6a0-104">Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="ed6a0-105">Tässä ohjeaiheessa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="ed6a0-106">ULkoisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ed6a0-106">External data setup</span></span>

<span data-ttu-id="ed6a0-107">Syötä ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen**).</span><span class="sxs-lookup"><span data-stu-id="ed6a0-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="ed6a0-108">Lisätietoja määrityksestä on kohdassa [Kassavirran ennustaminen](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="ed6a0-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="ed6a0-109">Jos haluat syöttää ulkoisia tietoja kassavirtaennusteisiin, voit käyttää Avaa Excelissä -käyttökokemusta ulkoisten tietojen syöttämiseen ja muokkaamiseen.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="ed6a0-110">Valitse **Ulkoiset tiedot** -painike ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="ed6a0-111">Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="ed6a0-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="ed6a0-112">**Kirjaustunnus**</span><span class="sxs-lookup"><span data-stu-id="ed6a0-112">**Entry ID**</span></span>
- <span data-ttu-id="ed6a0-113">**Kuvaus** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-113">**Description** (optional)</span></span>
- <span data-ttu-id="ed6a0-114">**Ulkoisen lähteen nimi** – Valitse jokin sen luettelon arvoista, jonka määritit Finance Insightsin määrittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="ed6a0-115">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="ed6a0-115">**Legal Entity**</span></span>
- <span data-ttu-id="ed6a0-116">**Päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="ed6a0-116">**Date**</span></span>
- <span data-ttu-id="ed6a0-117">**Summa tapahtuman valuuttana**</span><span class="sxs-lookup"><span data-stu-id="ed6a0-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="ed6a0-118">**Valuuttakoodi**</span><span class="sxs-lookup"><span data-stu-id="ed6a0-118">**Currency Code**</span></span>
- <span data-ttu-id="ed6a0-119">**Oletusdimensio** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="ed6a0-120">**Asiakirjanumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-120">**Document number** (optional)</span></span>
- <span data-ttu-id="ed6a0-121">**Tilinumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-121">**Account number** (optional)</span></span>
- <span data-ttu-id="ed6a0-122">**Tilin nimi** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="ed6a0-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="ed6a0-123">Ulkoisten tietojen tuominen käyttämällä tiedonhallinnan kehystä</span><span class="sxs-lookup"><span data-stu-id="ed6a0-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="ed6a0-124">Voit tuoda kassavirtaennusteiden ulkoisia tietoja käyttämällä **Tiedonhallinta**-työtilaa ja entiteettiä, jonka nimi on **Kassavirtaennusteen ulkoinen lähdemerkintä**.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="ed6a0-125">Jos sinun on siirrettävä asetustiedot ympäristöstä toiseen, tarvittavat asetustaulukot ovat käytettävissä seuraaville entiteeteille:</span><span class="sxs-lookup"><span data-stu-id="ed6a0-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="ed6a0-126">Kassavirtaennusteen ulkoisen lähteen asetukset</span><span class="sxs-lookup"><span data-stu-id="ed6a0-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="ed6a0-127">Kassavirtaennusteen ulkoisen lähdeyrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="ed6a0-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="ed6a0-128">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="ed6a0-128">Privacy notice</span></span>
<span data-ttu-id="ed6a0-129">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="ed6a0-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
