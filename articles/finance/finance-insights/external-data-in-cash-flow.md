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
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 03318eaae0b3329dc758c48202f8f47ca2c4ab08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245565"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="5f34d-103">Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)</span><span class="sxs-lookup"><span data-stu-id="5f34d-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5f34d-104">Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="5f34d-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="5f34d-105">Tässä ohjeaiheessa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.</span><span class="sxs-lookup"><span data-stu-id="5f34d-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="5f34d-106">ULkoisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5f34d-106">External data setup</span></span>

<span data-ttu-id="5f34d-107">Syötä ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen**).</span><span class="sxs-lookup"><span data-stu-id="5f34d-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="5f34d-108">Lisätietoja määrityksestä on kohdassa [Kassavirran ennustaminen](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="5f34d-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="5f34d-109">Jos haluat syöttää ulkoisia tietoja kassavirtaennusteisiin, voit käyttää Avaa Excelissä -käyttökokemusta ulkoisten tietojen syöttämiseen ja muokkaamiseen.</span><span class="sxs-lookup"><span data-stu-id="5f34d-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="5f34d-110">Valitse **Ulkoiset tiedot** -painike ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**.</span><span class="sxs-lookup"><span data-stu-id="5f34d-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="5f34d-111">Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="5f34d-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="5f34d-112">**Kirjaustunnus**</span><span class="sxs-lookup"><span data-stu-id="5f34d-112">**Entry ID**</span></span>
- <span data-ttu-id="5f34d-113">**Kuvaus** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="5f34d-113">**Description** (optional)</span></span>
- <span data-ttu-id="5f34d-114">**Ulkoisen lähteen nimi** – Valitse jokin sen luettelon arvoista, jonka määritit Finance Insightsin määrittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="5f34d-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="5f34d-115">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="5f34d-115">**Legal Entity**</span></span>
- <span data-ttu-id="5f34d-116">**Päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="5f34d-116">**Date**</span></span>
- <span data-ttu-id="5f34d-117">**Summa tapahtuman valuuttana**</span><span class="sxs-lookup"><span data-stu-id="5f34d-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="5f34d-118">**Valuuttakoodi**</span><span class="sxs-lookup"><span data-stu-id="5f34d-118">**Currency Code**</span></span>
- <span data-ttu-id="5f34d-119">**Oletusdimensio** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="5f34d-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="5f34d-120">**Asiakirjanumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="5f34d-120">**Document number** (optional)</span></span>
- <span data-ttu-id="5f34d-121">**Tilinumero** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="5f34d-121">**Account number** (optional)</span></span>
- <span data-ttu-id="5f34d-122">**Tilin nimi** (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="5f34d-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="5f34d-123">Ulkoisten tietojen tuominen käyttämällä tiedonhallinnan kehystä</span><span class="sxs-lookup"><span data-stu-id="5f34d-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="5f34d-124">Voit tuoda kassavirtaennusteiden ulkoisia tietoja käyttämällä **Tiedonhallinta**-työtilaa ja entiteettiä, jonka nimi on **Kassavirtaennusteen ulkoinen lähdemerkintä**.</span><span class="sxs-lookup"><span data-stu-id="5f34d-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="5f34d-125">Jos sinun on siirrettävä asetustiedot ympäristöstä toiseen, tarvittavat asetustaulukot ovat käytettävissä seuraaville entiteeteille:</span><span class="sxs-lookup"><span data-stu-id="5f34d-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="5f34d-126">Kassavirtaennusteen ulkoisen lähteen asetukset</span><span class="sxs-lookup"><span data-stu-id="5f34d-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="5f34d-127">Kassavirtaennusteen ulkoisen lähdeyrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="5f34d-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="5f34d-128">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="5f34d-128">Privacy notice</span></span>
<span data-ttu-id="5f34d-129">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="5f34d-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]