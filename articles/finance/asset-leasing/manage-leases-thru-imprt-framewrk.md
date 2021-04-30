---
title: Vuokrausten hallinta vuokrauksen tuonnin kehyksen kautta
description: Tässä ohjeaiheessa kerrotaan, miten vuokrauksen tuonnin kehystä käytetään useiden vuokrausten muokkaamisessa kerralla.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 083adf0a4bb74ac65e6f8b5077f65c74eb3fa337
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880907"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="30783-103">Vuokrausten hallinta vuokrauksen tuonnin kehyksen kautta</span><span class="sxs-lookup"><span data-stu-id="30783-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30783-104">Tässä ohjeaiheessa kerrotaan, miten vuokrauksen tuonnin kehystä käytetään useiden vuokrausten muokkaamisessa yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="30783-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="30783-105">Tämän ominaisuuden käyttäminen säästää aikaa, ja voit myös varmistaa tarkat oikaisut vähentämällä inhimillisten virheiden mahdollisuutta.</span><span class="sxs-lookup"><span data-stu-id="30783-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="30783-106">Lisäksi tämä ominaisuus voi yhdistää Microsoft Dynamics 365 Financen ulkoisiin tietoentiteetteihin. Näin voit ladata tietoja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="30783-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="30783-107">Seuraavia tietoentiteettejä voidaan käyttää resurssin vuokrauksen yhdistämisessä ulkoisiin järjestelmiin:</span><span class="sxs-lookup"><span data-stu-id="30783-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="30783-108">Vuokran valmistelu</span><span class="sxs-lookup"><span data-stu-id="30783-108">Lease staging</span></span>
- <span data-ttu-id="30783-109">Maksusopimusten valmistelu</span><span class="sxs-lookup"><span data-stu-id="30783-109">Payment contract staging</span></span>
- <span data-ttu-id="30783-110">Toimeenpantava sopimusten valmistelu</span><span class="sxs-lookup"><span data-stu-id="30783-110">Executory contract staging</span></span>

<span data-ttu-id="30783-111">Tuontiprosessin avulla voit oikaista vuokrasopimusta, päivittää muita kuin taloudellisia tietoja ja lisätä uusia vuokrasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="30783-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="30783-112">Voit tarkastella ja muokata vuokraustietoja ennen tuontia.</span><span class="sxs-lookup"><span data-stu-id="30783-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="30783-113">Järjestelmä voi suorittaa seuraavat kolme prosessia vuokrauksen tuontiohjelman kautta.</span><span class="sxs-lookup"><span data-stu-id="30783-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="30783-114">Käsittelyn tyyppi</span><span class="sxs-lookup"><span data-stu-id="30783-114">Process type</span></span>  | <span data-ttu-id="30783-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="30783-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="30783-116">Tietueen lisääminen</span><span class="sxs-lookup"><span data-stu-id="30783-116">Add record</span></span>    | <span data-ttu-id="30783-117">Siirretyt vuokrasopimukset, joilla on tämä prosessityyppi, luovat vuokrasopimuksen järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="30783-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="30783-118">Aikataulu on vahvistettava manuaalisesti, ja alkuperäisen tuloutuksen kirjauskansiovienti on kirjattava manuaalisesti siirron jälkeen.</span><span class="sxs-lookup"><span data-stu-id="30783-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="30783-119">Päivitä tietue</span><span class="sxs-lookup"><span data-stu-id="30783-119">Update record</span></span> | <span data-ttu-id="30783-120">Siirretyt vuokrasopimukset, joilla tämä prosessityyppi, päivittävät järjestelmässä jo olevan vuokrasopimuksen kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="30783-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="30783-121">Vain kentät, jotka on valittu **Kenttien valinnan päivittäminen** -sivulla, päivitetään.</span><span class="sxs-lookup"><span data-stu-id="30783-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="30783-122">Muut kuin taloushallinnon kentät kannattaa valita **Kenttien valinnan päivittäminen** -sivulla, koska tämä prosessityyppi ei oikaise vuokrasopimusta.</span><span class="sxs-lookup"><span data-stu-id="30783-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="30783-123">Säädä tietuetta</span><span class="sxs-lookup"><span data-stu-id="30783-123">Adjust record</span></span> | <span data-ttu-id="30783-124">Siirretyt vuokrasopimukset, joilla on tämä prosessityyppi, muokkaavat vuokrasopimusta.</span><span class="sxs-lookup"><span data-stu-id="30783-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="30783-125">Tämä oikaisu aiheuttaa vuokrasopimuksen rahoitusleasingsopimuksen muokkauksen.</span><span class="sxs-lookup"><span data-stu-id="30783-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="30783-126">Kun vuokrasopimus on käsitelty, järjestelmä luo uuden maksuaikataulun käyttämällä vuokrasopimuksen tuontiohjelman uusia tietoja.</span><span class="sxs-lookup"><span data-stu-id="30783-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="30783-127">Järjestelmä ei vahvista maksuaikataulua tai kirjaa oikaisukirjauskansiovientiä.</span><span class="sxs-lookup"><span data-stu-id="30783-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="30783-128">Kun tiedot on ladattu **Tietojen hallinta** -työtilan avulla, avaa **Tuonnin otsikko** -sivu (**Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Tuonnin otsikko**).</span><span class="sxs-lookup"><span data-stu-id="30783-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="30783-129">Tällä sivulla luetellaan kaikki kolmen aiemmin mainitun tietoentiteetin tuonnit.</span><span class="sxs-lookup"><span data-stu-id="30783-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="30783-130">Jos haluat tarkastella vuokrasopimuksen väliaikaisia tietoja ennen käsittelyn suorittamista, valitse **Väliaikaiset tiedot**.</span><span class="sxs-lookup"><span data-stu-id="30783-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="30783-131">Vertailutoiminnon avulla voit vertailla tuotavaa tietuetta vastaavaan järjestelmän tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="30783-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="30783-132">Jos haluat verrata yksittäisen vuokrasopimuksen tietuetta, valitse vuokrasopimus ja valitse sitten **Vertaa**.</span><span class="sxs-lookup"><span data-stu-id="30783-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="30783-133">Tee tämä vaihe, jos haluat luoda **Erot**-raportin ennen vuokrasopimustietueiden siirtoa.</span><span class="sxs-lookup"><span data-stu-id="30783-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="30783-134">Vertailutoiminto vertaa väliaikaisten tietojen arvoja järjestelmässä olevien vuokrasopimusten arvoihin.</span><span class="sxs-lookup"><span data-stu-id="30783-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="30783-135">Vertailutoiminto ei toimi vuokrasopimuksissa, joiden prosessityyppi on **Lisää tietue**, koska vuokrasopimus ei sisällä vertailtavia kohteita.</span><span class="sxs-lookup"><span data-stu-id="30783-135">The Compare functionality won't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="30783-136">Jos haluat vertailla useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen** ja valitse **Vertaa**.</span><span class="sxs-lookup"><span data-stu-id="30783-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Compare**.</span></span>

<span data-ttu-id="30783-137">Voit tarkastella kaikkien entiteettien eroja järjestelmässä olevien tietojen ja väliaikaisten taulukoiden tietojen välillä.</span><span class="sxs-lookup"><span data-stu-id="30783-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="30783-138">Valitse kunkin väliaikaisen taulukon entiteetin **Katso erot** -kohta.</span><span class="sxs-lookup"><span data-stu-id="30783-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="30783-139">Näkyviin tulevassa valintaikkunassa näkyy valittu arvo ja ehdotettu väliaikainen arvo.</span><span class="sxs-lookup"><span data-stu-id="30783-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="30783-140">Voit myös päivittää väliaikaisen arvon muuttamalla sitä **Uusi arvo** -sarakkeessa ja valitsemalla sitten **Päivitä väliaikainen arvo**.</span><span class="sxs-lookup"><span data-stu-id="30783-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="30783-141">Voit vahvistaa vuokrasopimukset ja varmistaa, että ne tietueet voidaan tuoda järjestelmään ilman virheitä.</span><span class="sxs-lookup"><span data-stu-id="30783-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="30783-142">Ennen kuin vuokrasopimustietue siirretään, järjestelmä suorittaa useita tarkistuksia. Niiden avulla varmistetaan, että tietueen tuonti onnistuu.</span><span class="sxs-lookup"><span data-stu-id="30783-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="30783-143">Voit vahvistaa yksittäisen vuokrasopimuksen valitsemalla **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="30783-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="30783-144">Jos haluat vahvistaa useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen** ja valitse **Vertaa**.</span><span class="sxs-lookup"><span data-stu-id="30783-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Validate**.</span></span>

<span data-ttu-id="30783-145">Voit käsitellä yksittäistä vuokrasopimusta valitsemalla **Siirrä vuokrasopimustietueet** **Tuonnin otsikko** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="30783-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="30783-146">Kun vuokrasopimus siirretään, järjestelmä suorittaa toiminnon, joka on määritetty **Prosessityyppi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="30783-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="30783-147">Jos haluat siirtää useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen** ja valitse **Siirrä**.</span><span class="sxs-lookup"><span data-stu-id="30783-147">To migrate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Migrate**.</span></span>

<span data-ttu-id="30783-148">Kun vuokrasopimuksia verrataan, voit tarkastella kunkin tuonnin tunnukseen sisältyvän vuokrasopimuksen erot suorittamalla raportin.</span><span class="sxs-lookup"><span data-stu-id="30783-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="30783-149">Jos haluat suorittaa yhden vuokrasopimuksen raportin, valitse kyseinen vuokrasopimus väliaikaisista tiedoista ja valitse sitten **Vertaile ja tarkastele raporttia \> Erojen raportti**.</span><span class="sxs-lookup"><span data-stu-id="30783-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="30783-150">Jos haluat vertailla useita vuokrasopimuksia kerralla, siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Kausittainen** ja valitse **Vertaa**.</span><span class="sxs-lookup"><span data-stu-id="30783-150">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic** and select **Compare**.</span></span> 

## <a name="set-up-update-fields"></a><span data-ttu-id="30783-151">Kenttien päivittämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="30783-151">Set up update fields</span></span>

<span data-ttu-id="30783-152">Jos käytät vuokrauksen tuonnin kehystä vuokrasopimusten päivittämisessä ja prosessityyppi on **Päivitä tietue**, voit valita tietyt kentät päivittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="30783-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="30783-153">Siirry kohtaan **Resurssin vuokraus \> Vuokrauksen tuonnin kehys \> Asetus \> Päivitä kenttien valinta**.</span><span class="sxs-lookup"><span data-stu-id="30783-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="30783-154">Valitse näkyviin tulevalla sivulla päivitettävät kentät ja siirrä ne sitten **Valitut kentät** -luetteloon vihreän nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="30783-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="30783-155">Vain **Valitut kentät** -luettelossa olevat kentät voidaan päivittää käyttämällä vuokrauksen tuonnin ohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="30783-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
