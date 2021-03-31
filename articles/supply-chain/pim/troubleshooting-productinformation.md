---
title: Tuotetietojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotetietojen käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223359"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="aa1bb-103">Tuotetietojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="aa1bb-103">Troubleshoot product information</span></span>

<span data-ttu-id="aa1bb-104">Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotetietojen käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="aa1bb-105">Vapautettua tuotetta ei voi poistaa</span><span class="sxs-lookup"><span data-stu-id="aa1bb-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-106">Issue description</span></span>

<span data-ttu-id="aa1bb-107">Vapautetun tuotteen ja kaikki sen variantit voidaan poistaa vain, jos vapautetussa tuotteessa ei ole liittyviä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-108">Issue resolution</span></span>

<span data-ttu-id="aa1bb-109">Poista vapautettu tuote tai päätuote seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa1bb-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="aa1bb-110">Sulje kaikki nimikkeiden avoimet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="aa1bb-111">Vähennä varaston arvoksi 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="aa1bb-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="aa1bb-112">Suorita varaston sulkeminen.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="aa1bb-113">Poista kaikki poistettavan päätuotteen tuotevariantit.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="aa1bb-114">Voiko vapautetun tuotteen nimiketunnuksen vaihtaa?</span><span class="sxs-lookup"><span data-stu-id="aa1bb-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="aa1bb-115">Useimmissa tapauksissa vapautettujen tuotteiden nimiketunnuksia ei voi muokata, koska tiedot vaurioituisivat muutoksen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="aa1bb-116">Nimiketunnusta voi muokata vain, jos on korjattava vapautetun tuotteen ensisijaisen avaimen uudelleennimeämisen aiheuttama tietojen vaurioituminen. Tästä oli maininta [Finance and Operations 10.0.0:n ja Platform update 24:n poistettujen tai vanhentuneiden toimintojen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) luettelossa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="aa1bb-117">Jos haluat mahdollisuuden muokata vapautettujen tuotteiden nimiketunnusta, [äänestä ideaa ideaportaalissa](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="aa1bb-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="aa1bb-118">Tuotteen oletusmateriaaliottosääntöä ei anneta tuoterakenneriville.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-119">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-119">Issue description</span></span>

<span data-ttu-id="aa1bb-120">Kun nimike lisätään tuoterakenneriville, järjestelmä ei käytä nimikkeelle määritettyjä oletusmateriaaliottosäännön tietoja.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="aa1bb-121">Nimikkeen materiaaliottosääntö ei siis näytä **Tuoterakenteen rivi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-122">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-122">Issue resolution</span></span>

<span data-ttu-id="aa1bb-123">Jos määrität materiaaliottosäännön tuoterakennerivillä, sitä käytetään kyseisellä tuoterakennerivillä.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="aa1bb-124">Jos materiaaliottosääntö on kuitenkin tyhjä tai jos sitä ei määritä tuoterakennerivillä, nimikkeellä määritettyä materiaaliottosääntöä käytetään siltä kyseisellä tuoterakennerivillä, vaikka sitä ei kyseisellä rivillä näytetä.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="aa1bb-125">Muiden Microsoft Dynamics 365 Supply Chain Managementin toimintojen oletuslogiikka ei yleensä toimi tällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="aa1bb-126">Nykyistä toimintaa ei kuitenkaan voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="aa1bb-127">Muutoin tietyt siihen perustuvat aiemmin luodut mukautukset saattaisivat lakata toimimasta.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="aa1bb-128">Järjestelmä sallii viivakoodien kaksoiskappaleiden tallentamisen eri nimikkeille tai samalle nimikkeelle, jolla on eri dimensiot</span><span class="sxs-lookup"><span data-stu-id="aa1bb-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="aa1bb-129">Järjestelmä ei tällä hetkellä pakota käyttämään yksilöiviä viivakoodeja ja tämän rajoituksen lisääminen olisi häiriöitä aiheuttava muutos.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="aa1bb-130">Microsoftilla on itse asiassa tieto siitä, että tämä muutos aiheuttaisi joidenkin aiemmin luotujen asiakasasennusten rikkoutumisen.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="aa1bb-131">Laajaa uudelleensuunnittelua kuitenkin pohditaan, jotta tämä toiminto olisi mahdollinen tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="aa1bb-132">Nimiketietuemallia muokatessa avautuu seuraava virhesanoma: Varastosijaintia ei voi luoda, koska nimikettä ei ole varastoitu.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="aa1bb-133">Jotta voit varastoida nimikkeitä, liitetyn nimikemalliryhmän Varastoitu tuote -asetuksen on oltava valittuna.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-134">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-134">Issue description</span></span>

<span data-ttu-id="aa1bb-135">Tämä ongelma esiintyy, jos yrität luoda näiden ohjeiden mukaan mallin nimikkeelle, jota ei ole varastoitu.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="aa1bb-136">Avaa vapautettu tuote, jota ei ole varastoitu.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="aa1bb-137">Valitse toimintoruudun **Asetukset**-välilehdessä **Tietueen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="aa1bb-138">Valitse **Tietueen tiedot** -valintaikkunassa **Yrityksen tilien malli**.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="aa1bb-139">Tässä tapauksessa avautuu seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="aa1bb-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="aa1bb-140">Varastosijaintia ei voi luoda, koska nimikettä ei ole varastoitu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="aa1bb-141">Jotta voit varastoida nimikkeitä, liitetyn nimikemalliryhmän Varastoitu tuote -asetuksen on oltava valittuna.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-142">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-142">Issue resolution</span></span>

<span data-ttu-id="aa1bb-143">Tuotemallien luontiprosessi edellyttää tuotekohtaista lisälogiikkaa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="aa1bb-144">Tämän vuoksi tässä yhteydessä ei voi käyttää yleistä **Yrityksen tilien malli** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="aa1bb-145">Toimi sen sijaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa1bb-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="aa1bb-146">Avaa vapautettu tuote.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-146">Open a released product.</span></span>
1. <span data-ttu-id="aa1bb-147">Valitse toimintoruudun **Tuote**-välilehden **Uusi**-ryhmässä **Malli \> Luo jaettu malli**.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="aa1bb-148">Tuotemääritteisiin lisättävää oletusohjetekstiä ei ole vapautetussa tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="aa1bb-149">Tuotemääritteisiin lisättävä kuvaus ja ohjeteksti eivät näy tai niitä ei oletusarvoisesti anneta vapautetuissa tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="aa1bb-150">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="aa1bb-151">Annettu oletusmäärä vaihtelee sen mukaan, rekisteröidäänkö se tuoterakenteesta vai tuoterakenteen versiosta</span><span class="sxs-lookup"><span data-stu-id="aa1bb-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-152">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-152">Issue description</span></span>

<span data-ttu-id="aa1bb-153">Kun nimike lisätään tuoterakenteeseen, määräksi määritetään oletusarvoisesti 1 eikä valitun tuotteen **Tilauksen oletusasetukset** -sivun **Väh.tilausmäärä** -kentässä määritetty määrä.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="aa1bb-154">Jos nimike kuitenkin lisätään tuoterakenneversiosta ja nimike ja variantti valitaan, oletusarvoisesti annettava määrä ottaa huomioon tiettyjen dimensioiden tilauksen oletusasetuksissa määritetyn vähimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-155">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-155">Issue resolution</span></span>

<span data-ttu-id="aa1bb-156">Tämä toiminta on tarkoituksellista.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-156">This behavior is expected.</span></span> <span data-ttu-id="aa1bb-157">Tuoterakenteen ja tuoterakenteen version välinen logiikkaero on kuitenkin tunnettu ongelma.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="aa1bb-158">Tätä toimintaa ei siitä huolimatta tulla muuttamaan, koska muutos voisi vaikuttaa moniin erilaisiin asiakasskenaarioihin.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="aa1bb-159">Tuotteen asiakirjaliitteiden tietoentiteetistä ladattuja liitettyjä kuvia ei vaihtaa vapautetun tuotteen tiedoissa</span><span class="sxs-lookup"><span data-stu-id="aa1bb-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-160">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-160">Issue description</span></span>

<span data-ttu-id="aa1bb-161">Tämä ongelma voi esiintyä, kun kuva liitetään nimikkeeseen *Tuotteen asiakirjaliitteet* -tietoentiteetin avulla.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="aa1bb-162">Tässä tapauksessa nimikkeen kuva näytetään nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="aa1bb-163">Jos kuitenkin valitaan **Vaihda kuva**, ladattujen kuvien luettelossa ei ole mitään.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="aa1bb-164">Myöskään liitteitä ei näytetä nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-165">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-165">Issue resolution</span></span>

<span data-ttu-id="aa1bb-166">*EcoResProductDocumentAttachmentEntity*-entiteetti (*Tuotteen asiakirjaliitteet*) tuo *tuotteiden* mutta ei *vapautettujen tuotteiden* asiakirjaliitteet.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="aa1bb-167">(Vapautettuja tuotteita kutsutaan myös *nimikkeiksi*.) Nimikkeen liitteiden tarkasteleminen **Vapautetun tuotteen tiedot** -sivulla onnistuu, kun käytössä on *EcoResReleasedProductDocumentAttachmentEntity*-entiteetti (*Vapautetun tuotteen asiakirjaliitteet*).</span><span class="sxs-lookup"><span data-stu-id="aa1bb-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="aa1bb-168">Microsoft Flow -yhdistimessä avautuu seuraava virhesanoma: Päivitystä ei sallita kentälle ProductNumber.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-169">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-169">Issue description</span></span>

<span data-ttu-id="aa1bb-170">Tämä ongelma esiintyy, jos **Tuotenumero**-kenttä päivitystä yritetään *Vapautetut tuotteet* -entiteetin V2 ja Microsoft Flow'n avulla.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-171">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-171">Issue resolution</span></span>

<span data-ttu-id="aa1bb-172">Tämä toiminta on tarkoituksellista.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-172">This behavior is expected.</span></span> <span data-ttu-id="aa1bb-173">Mahdollisuus muokata vapautetun tuotteen tuotenumeroa poistettiin Dynamics 365 Finance and Operations 10.0.0:n platform update 24:stä, koska näin haluttiin estää tietojen vioittuminen.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="aa1bb-174">Poikkeustapauksissa, joissa on korjattava vapautetun tuotteen ensisijaisen avaimen aiemman uudelleennimeämisen aiheuttama tietojen vioittuminen, Microsoft-tukea voidaan pyytää poistamaan tämä rajoitus tilapäisesti.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="aa1bb-175">Vapautetun tuotevariantin luominen ei onnistu toisessa yrityksessä</span><span class="sxs-lookup"><span data-stu-id="aa1bb-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-176">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-176">Issue description</span></span>

<span data-ttu-id="aa1bb-177">Jos päätuote yritetään vapauttaa ilman variantteja ja sitten variantteja yritetään luoda tarpeen mukaan kussakin yrityksessä, variantteja voi vapauttaa varianttiehdotuksia käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="aa1bb-178">Variantteja ei myöskään voi luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-179">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-179">Issue resolution</span></span>

<span data-ttu-id="aa1bb-180">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-180">This behavior is by design.</span></span> <span data-ttu-id="aa1bb-181">Päätuotteen ja päätuotteen käyttämien dimensioiden suhteita säilytetään jaetulla tasolla.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="aa1bb-182">Niinpä jaetun päätuotteen käytettävissä olevia dimensioita ei voi luoda tietyssä yrityksessä, jossa kyseiset dimensiot vapautetaan, ja sitten replikoida prosessia kussakin yrityksessä, jossa dimensioita tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="aa1bb-183">Sen sijaan vapautusprosessi on muutettava mukautumaan suunniteltuun prosessiin.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="aa1bb-184">Tuotteiden vapauttamisprosessi:</span><span class="sxs-lookup"><span data-stu-id="aa1bb-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="aa1bb-185">Luo jaettu päätuote ja dimensiot, jotka voidaan vapauttaa yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="aa1bb-186">Vapauta tuotteet yrityksiin, joka käyttämällä varianttiehdotuksia ja manuaalisesti lisäämällä vapautettavat yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="aa1bb-187">Vaihtoehtoiesti voit luoda vapautetun tuotteen myös suoraan.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="aa1bb-188">Kun variantti vapautetaan toisessa yrityksessä seuraava virhesanoma avautuu: Tuotevariantti, jolla on määritetyt dimensiot, on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="aa1bb-189">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa1bb-189">Issue description</span></span>

<span data-ttu-id="aa1bb-190">Jos tuotevariantti on jo vapautettu yrityksessä A ja yrität vapauttaa sen yrityksessä B käyttämällä **Uusi**-painiketta **Vapautetut tuotevariantit** -sivulla, seuraava virhesanoma avautuu:</span><span class="sxs-lookup"><span data-stu-id="aa1bb-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="aa1bb-191">Tuotevariantti, jolla on määritetyt dimensiot, on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="aa1bb-192">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="aa1bb-192">Issue resolution</span></span>

<span data-ttu-id="aa1bb-193">**Vapautetut tuotevariantit** -sivun **Uusi**-painike luo variantin ja vapauttaa sen yrityskontekstissa.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="aa1bb-194">Jos variantti on jo luotu, sitä ei voi vapauttaa toisessa yrityksessä **Uusi**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="aa1bb-195">Korjaa ongelma vapauttamalla aiemmin luotu variantti toivotussa yrityksessä avaamalla **Päätuote**-sivu ja valitsemalla **Vapauta tuote**.</span><span class="sxs-lookup"><span data-stu-id="aa1bb-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]