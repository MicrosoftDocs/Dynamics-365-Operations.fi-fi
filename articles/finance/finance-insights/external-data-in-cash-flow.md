---
title: Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)
description: Tässä ohjeaiheessa kuvataan määritysvaiheet, jotka on suoritettava, jotta ulkoiset tiedot voidaan syöttää tai tuoda kassavirtaennusteisiin.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186687"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="08fda-103">Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)</span><span class="sxs-lookup"><span data-stu-id="08fda-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="08fda-104">Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="08fda-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="08fda-105">Tässä ohjeaiheessa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.</span><span class="sxs-lookup"><span data-stu-id="08fda-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="08fda-106">ULkoisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="08fda-106">External data setup</span></span>

<span data-ttu-id="08fda-107">Syötä ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen**).</span><span class="sxs-lookup"><span data-stu-id="08fda-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="08fda-108">Lisätietoja määrityksestä on kohdassa [Kassavirran ennustaminen](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="08fda-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="08fda-109">Jos haluat syöttää ulkoisia tietoja kassavirtaennusteisiin, voit käyttää Avaa Excelissä -käyttökokemusta ulkoisten tietojen syöttämiseen ja muokkaamiseen.</span><span class="sxs-lookup"><span data-stu-id="08fda-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="08fda-110">Valitse **Ulkoiset tiedot** -painike ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**.</span><span class="sxs-lookup"><span data-stu-id="08fda-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="08fda-111">Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="08fda-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="08fda-112">**Kirjaustunnus**</span><span class="sxs-lookup"><span data-stu-id="08fda-112">**Entry ID**</span></span>
- <span data-ttu-id="08fda-113">**Kuvaus** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="08fda-113">**Description** (optional)</span></span>
- <span data-ttu-id="08fda-114">**Ulkoisen lähteen nimi** – Valitse jokin sen luettelon arvoista, jonka määritit Finance Insightsin määrittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="08fda-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="08fda-115">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="08fda-115">**Legal Entity**</span></span>
- <span data-ttu-id="08fda-116">**Päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="08fda-116">**Date**</span></span>
- <span data-ttu-id="08fda-117">**Summa tapahtuman valuuttana**</span><span class="sxs-lookup"><span data-stu-id="08fda-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="08fda-118">**Valuuttakoodi**</span><span class="sxs-lookup"><span data-stu-id="08fda-118">**Currency Code**</span></span>
- <span data-ttu-id="08fda-119">**Oletusdimensio** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="08fda-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="08fda-120">**Asiakirjanumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="08fda-120">**Document number** (optional)</span></span>
- <span data-ttu-id="08fda-121">**Tilinumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="08fda-121">**Account number** (optional)</span></span>
- <span data-ttu-id="08fda-122">**Tilin nimi** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="08fda-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="08fda-123">Ulkoisten tietojen tuominen käyttämällä tiedonhallinnan kehystä</span><span class="sxs-lookup"><span data-stu-id="08fda-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="08fda-124">Voit tuoda kassavirtaennusteiden ulkoisia tietoja käyttämällä **Tiedonhallinta**-työtilaa ja entiteettiä, jonka nimi on **Kassavirtaennusteen ulkoinen lähdemerkintä**.</span><span class="sxs-lookup"><span data-stu-id="08fda-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="08fda-125">Jos sinun on siirrettävä asetustiedot ympäristöstä toiseen, tarvittavat asetustaulukot ovat käytettävissä seuraaville entiteeteille:</span><span class="sxs-lookup"><span data-stu-id="08fda-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="08fda-126">Kassavirtaennusteen ulkoisen lähteen asetukset</span><span class="sxs-lookup"><span data-stu-id="08fda-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="08fda-127">Kassavirtaennusteen ulkoisen lähdeyrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="08fda-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
