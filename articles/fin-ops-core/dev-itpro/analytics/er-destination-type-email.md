---
title: Sähköpostin ER-kohteen tyyppi
description: Tässä ohjeaiheessa annetaan tietoja siitä, miten kullekin lähteviä asiakirjoja luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin sähköpostikohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019746"
---
# <span data-ttu-id="3a2ac-103"><a name="EmailDestinationType">Sähköpostikohde</a></span><span class="sxs-lookup"><span data-stu-id="3a2ac-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a2ac-104">Voit määrittää sähköpostikohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentille.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="3a2ac-105">Luotu asiakirja toimitetaan sähköpostiviestin liitteenä kohdeasetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="3a2ac-106">Lähetä tulostetiedosto sähköpostitse valitsemalla **Käytössä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="3a2ac-107">Kun tämä asetus on otettu käyttöön, voit muokata sähköpostin aihetta ja määrittää sähköpostin vastaanottajat.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="3a2ac-108">Voit määrittää vakiotekstit sähköpostiviestin aiheelle ja perustekstille tai voit ER-[kaavojen ](er-formula-language.md) avulla dynaamisesti luoda sähköpostitekstejä.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="3a2ac-109">Voit määrittää sähköisen raportoinnin sähköpostiosoitteet kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="3a2ac-110">Määritys voidaan suorittaa loppuun samalla tavalla kuin Tulostuksenhallinta-ominaisuus suorittaa sen loppuun. Voit myös ratkaista sähköpostiosoitteen käyttämällä suoraa viitettä ER-määritykseen kaavan kautta.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="3a2ac-111">[![Sähköpostikohteen käyttöönotto](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="3a2ac-112">Sähköpostiosoitteen tyyppi</span><span class="sxs-lookup"><span data-stu-id="3a2ac-112">Email address types</span></span>

<span data-ttu-id="3a2ac-113">Kun valitset **Muokkaa** kentässä **Vastaanottaja** tai **Kopio**, **Sähköpostin vastaanottaja** -valintaikkuna tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="3a2ac-114">Voit sitten valita minkä tyyppistä sähköpostiosoitetta haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="3a2ac-115">Tällä hetkellä tuetaan sähköpostityyppejä **Määrityssähköposti** ja **Tulostuksenhallinta**.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="3a2ac-116">[![Valitse sähköpostityyppi](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="3a2ac-117">Tulostuksenhallinta</span><span class="sxs-lookup"><span data-stu-id="3a2ac-117">Print management</span></span>

<span data-ttu-id="3a2ac-118">Jos valitset **Tulostuksenhallinta** -sähköpostityypin, voit syöttää kiinteät sähköpostiosoitteet **Vastaanottaja**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="3a2ac-119">[![Kiinteiden sähköpostiosoitteiden määritys](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="3a2ac-120">Jos haluat käyttää muita kuin kiinteitä sähköpostiosoitteita, tiedostokohteen sähköpostin lähdetyyppi on valittava.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="3a2ac-121">Seuraavia arvoja tuetaan: **Asiakas**, **Toimittaja**, **Prospekti**, **Yhteyshenkilö**, **Kilpailija**, **Työntekijä**, **Hakija**, **Mahdollinen toimittaja** ja **Ei-sallittu toimittaja**.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="3a2ac-122">Kun olet valinnut sähköpostin lähdetyypin, käytä **Sähköpostin lähdetili** -kentän vieressä olevaa painiketta, jos haluat avata **Reseptien suunnittelu** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="3a2ac-123">Voit käyttää tätä muotoa liittääksesi kaavan, joka palautta suorituksen aikana valitun lähdetyypin **osapuolen tilin** käsitellystä asiakirjasta sähköpostikohteeseen.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="3a2ac-124">[![Sähköpostilähdetilin määritys](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="3a2ac-125">Kaavat ovat ER-määrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="3a2ac-126">Kirjoita **Kaava**-kenttään asiakirjakohtainen viittaus asiakas- tai toimittajaosapuolen tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="3a2ac-127">Kirjoittamisen asemesta voit etsiä tietolähdesolmun, joka vastaa asiakkaan tai toimittajan tiliä, ja päivittää kaavan valitsemalla **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="3a2ac-128">Jos käytössä on esimerkiksi **ISO 20022 Tilisiirto** -määritys, toimittajatiliä vastaava solmu on `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="3a2ac-129">Jos annat merkkijonoarvon, kuten `"DE-001"`, ja tallennat kaavan, toimittajan **DE-001** yhteyshenkilölle lähetetään sähköpostiviesti.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="3a2ac-130">[![ER-kaavan suunnittelusivu](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="3a2ac-131">[![Sähköpostilähdetilin määritys](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="3a2ac-132">Määrityssähköposti</span><span class="sxs-lookup"><span data-stu-id="3a2ac-132">Configuration email</span></span>

<span data-ttu-id="3a2ac-133">Käytä tätä sähköpostityyppiä, jos käyttämässäsi määrityksessä tietolähteissä solmu, joka palauttaa **sähköpostiosoitteen**.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="3a2ac-134">Voit käyttää reseptien suunnittelun tietolähteitä ja funktioita saadaksesi oikein muotoillun sähköpostiosoitteen.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="3a2ac-135">Jos käytössä on esimerkiksi **ISO 20022 Tilisiirto** -määritys, toimittajan yhteyshenkilön sähköpostiositetta vastaava solmu on `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="3a2ac-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="3a2ac-136">[![Sähköpostiositelähteen määritys](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="3a2ac-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a2ac-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3a2ac-137">Additional resources</span></span>

- [<span data-ttu-id="3a2ac-138">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3a2ac-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="3a2ac-139">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="3a2ac-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="3a2ac-140">Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="3a2ac-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
