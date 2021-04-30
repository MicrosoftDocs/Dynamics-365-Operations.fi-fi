---
title: Asiakasportaalin mukauttaminen ja käyttäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka asiakasportaalia mukautetaan sen jälkeen, kun se on lisätty järjestelmään.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6d4cc52a90b25406080032c7a98caa59f53ce188
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908997"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="2373a-103">Asiakasportaalin mukauttaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2373a-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2373a-104">Tässä ohjeaiheessa esitellään eri sivut, jotka ovat valmiina käytettävissä asiakasportaalissa.</span><span class="sxs-lookup"><span data-stu-id="2373a-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="2373a-105">Siinä selitetään, mitä sivut tekevät ja miten niitä voi mukauttaa.</span><span class="sxs-lookup"><span data-stu-id="2373a-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="2373a-106">Asiakasportaali tarjoaa joitakin valmiita verkkosivuja ja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="2373a-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="2373a-107">Seuraavassa sivustokartassa on yleiskatsaus kyseisistä verkkosivuista ja toiminnoista sekä tehtävistä, jotka voivat suorittaa toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="2373a-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="2373a-108">![Asiakkaan portaalisivuston sivustokartta](media/customer-portal-site-map.png "Asiakkaan portaalisivuston sivustokartta")</span><span class="sxs-lookup"><span data-stu-id="2373a-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="2373a-109">Tyypilliset mukautukset</span><span class="sxs-lookup"><span data-stu-id="2373a-109">Typical customizations</span></span>

<span data-ttu-id="2373a-110">Seuraavissa ohjeaiheissa on tietoja Power Apps -portaalien perustoiminnoista ja portaalien mukauttamisesta:</span><span class="sxs-lookup"><span data-stu-id="2373a-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="2373a-111">[Mallien käsitteleminen](/powerapps/maker/portals/work-with-templates) – Tämä ohjeaihe sisältää yleiskatsauksen Power Apps -portaalien toiminnasta ja siitä, miten voit tehdä portaalien yksinkertaisia mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="2373a-111">[Work with templates](/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="2373a-112">[Portaalin sisällönhallinta](/dynamics365/portals/manage-portal-content) – Tässä ohjeaiheessa kerrotaan, kuinka voit hallita ja mukauttaa portaalissasi näkyvää sisältöä.</span><span class="sxs-lookup"><span data-stu-id="2373a-112">[Manage portal content](/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="2373a-113">[Muokkaa CSS:tä](/powerapps/maker/portals/edit-css) – Tämän ohjeaiheen avulla voit tehdä monimutkaisempia mukautuksia portaalin käyttöliittymään.</span><span class="sxs-lookup"><span data-stu-id="2373a-113">[Edit CSS](/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="2373a-114">[Luo portaaliin teema](/dynamics365/portals/create-theme) – Tämän ohjeaiheen avulla voit luoda portaalin käyttöliittymän teeman.</span><span class="sxs-lookup"><span data-stu-id="2373a-114">[Create a theme for your portal](/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="2373a-115">[Portaalin sisällön luominen ja tuominen näkymiin helposti](/dynamics365/portals/create-expose-portal-content) – Tämä aiheen auttaa hallitsemaan portaalissa käytettyjä tietoja ja tauluja.</span><span class="sxs-lookup"><span data-stu-id="2373a-115">[Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="2373a-116">[Yhteyshenkilön määrittäminen käytettäväksi portaalissa](/powerapps/maker/portals/configure/configure-contacts) – Tässä ohjeaiheessa kerrotaan, kuinka käyttäjärooleja luodaan ja mukautetaan sekä kuinka suojaus ja todennus toimivat Power Apps -portaaleissa.</span><span class="sxs-lookup"><span data-stu-id="2373a-116">[Configure a contact for use on a portal](/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="2373a-117">[Taululomakkeiden ja portaalien verkkolomakkeiden huomautusten määrittäminen](/powerapps/maker/portals/configure-notes) – Tässä aiheessa käsitellään asiakirjojen ja tallennustilan lisäämistä portaaliin.</span><span class="sxs-lookup"><span data-stu-id="2373a-117">[Configure notes for table forms and web forms on portals](/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="2373a-118">[Portaalin verkkosivuston virheenkäsittely](/powerapps/maker/portals/admin/view-portal-error-log) – Tässä ohjeaiheessa kerrotaan, kuinka portaalin virhelokeja voidaan tarkastella ja tallentaa Microsoft Azure -Blob-objektisäilötilille.</span><span class="sxs-lookup"><span data-stu-id="2373a-118">[Error handling for portal website](/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="2373a-119">Tilauksen luomisprosessin mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2373a-119">Customize the order creation process</span></span>

<span data-ttu-id="2373a-120">Kun käyttäjä lähettää tilauksen asiakasportaalin kautta, tilaus synkronoidaan automaattisesti vastaavaan Dynamics 365 Supply Chain Management -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="2373a-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="2373a-121">Koska käyttäjä on ulkopuolinen asiakas, jotkin pakolliset tiedot on tarkoituksellisesti piilotettu häneltä.</span><span class="sxs-lookup"><span data-stu-id="2373a-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="2373a-122">Nämä tiedot täytetään automaattisesti, kun lomake lähetetään.</span><span class="sxs-lookup"><span data-stu-id="2373a-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="2373a-123">Tässä osassa näkyy, miten yhteyshenkilöt on määritettävä virheiden välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="2373a-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="2373a-124">Siinä selitetään kentät, jotka määritetään automaattisesti, ja voit muokata kenttien arvoa, jos niitä on.</span><span class="sxs-lookup"><span data-stu-id="2373a-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="2373a-125">Valmis tilauksen luomisprosessi</span><span class="sxs-lookup"><span data-stu-id="2373a-125">The out-of-box order creation process</span></span>

<span data-ttu-id="2373a-126">Tässä ovat vakiovaiheet tilauksen lähettämiselle asiakasportaalista.</span><span class="sxs-lookup"><span data-stu-id="2373a-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="2373a-127">Avaa ohjattu **Luo tilaus** -toiminto valitsemalla aloitussivulla **Luo tilaus** -ohjattu toiminto.</span><span class="sxs-lookup"><span data-stu-id="2373a-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="2373a-128">Määritä **Tilauksen tiedot** -sivulla seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="2373a-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="2373a-129">**Pyydetty vastaanottopäivä** – Määritä toimituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2373a-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="2373a-130">**Toimitusosoite** – Syötä osoite, johon tilaus toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="2373a-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="2373a-131">**Yritys** – Valitse asiakasyrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="2373a-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="2373a-132">Tämä kenttä määritetään automaattisesti muille kuin järjestelmänvalvoja-käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="2373a-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="2373a-133">**Hankintanumero** – Syötä tilauksen tilausnumero.</span><span class="sxs-lookup"><span data-stu-id="2373a-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="2373a-134">Tämä kenttä ei ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="2373a-134">This field isn't required.</span></span>
    - <span data-ttu-id="2373a-135">**Toimita maahan/alueelle** – Määritä maa tai alue, johon nimikkeet toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="2373a-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="2373a-136">Tämä kenttä määritetään automaattisesti muille kuin järjestelmänvalvoja-käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="2373a-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="2373a-137">![Tilauksen tiedot -sivu](media/customer-portal-order-information.png "Tilauksen tiedot -sivu")</span><span class="sxs-lookup"><span data-stu-id="2373a-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="2373a-138">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2373a-138">Select **Next**.</span></span>
1. <span data-ttu-id="2373a-139">Valitse **Nimikkeet**-sivulla **Lisää nimike**.</span><span class="sxs-lookup"><span data-stu-id="2373a-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="2373a-140">![Tuotesivu](media/customer-portal-items.png "Tuotesivu")</span><span class="sxs-lookup"><span data-stu-id="2373a-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="2373a-141">**Tuotetieto**-valintaikkunassa kuvaillaan seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="2373a-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="2373a-142">**Tuotteen nimi** – Etsi ja valitse tilaukseen lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="2373a-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="2373a-143">**Määrä** – Syötä valitun tuotteen määrä.</span><span class="sxs-lookup"><span data-stu-id="2373a-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="2373a-144">**Yksikkö** – Määritä mittayksikkö (esimerkiksi **kpl**, **kg** tai **laatikko**).</span><span class="sxs-lookup"><span data-stu-id="2373a-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="2373a-145">**Arvioitu nettosumma** – Arvo lasketaan nimikkeen arvioituna hintana valitun yksikkömäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="2373a-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="2373a-146">![Tuotetieto-valintaikkuna](media/customer-portal-item-information.png "Tuotetieto-valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="2373a-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="2373a-147">Lisää nimike tilaukseen valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="2373a-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="2373a-148">Toista vaiheet 4 - 6, kunnes olet lisännyt kaikki tilattavat nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="2373a-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="2373a-149">Kun olet lisännyt haluamasi nimikkeet, valitse **Nimikkeet**-sivulta **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2373a-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="2373a-150">**Tilauksen tiedot** -sivulla on tilauksen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="2373a-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="2373a-151">Tarkista tilauksen sisältö ja toimitustiedot.</span><span class="sxs-lookup"><span data-stu-id="2373a-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="2373a-152">Jos kaikki näyttää oikealta, lähetä tilaus valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="2373a-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="2373a-153">![Tilauksen tiedot -sivu](media/customer-portal-order-submit.png "Tilauksen tiedot -sivu")</span><span class="sxs-lookup"><span data-stu-id="2373a-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="2373a-154">Tietojen vakioasetus</span><span class="sxs-lookup"><span data-stu-id="2373a-154">Standard data setup</span></span>

<span data-ttu-id="2373a-155">Jotta käyttäjäkokemus olisi sujuva, asiakasportaali täyttää automaattisesti useiden pakollisten kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="2373a-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="2373a-156">Nämä arvot perustuvat tilauksen lähettäneen asiakkaan yhteyshenkilötietueen tietoihin.</span><span class="sxs-lookup"><span data-stu-id="2373a-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="2373a-157">Seuraavien pakollisten kenttien arvot on määritettävä jokaiselle sellaiselle [yhteyshenkilöriville](/powerapps/maker/portals/configure/configure-contacts), joka kuuluu asiakasportaalia tilausten lähettämiseen käyttävälle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="2373a-157">For each [contact row](/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="2373a-158">Muussa tapauksessa tapahtuu virheitä.</span><span class="sxs-lookup"><span data-stu-id="2373a-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="2373a-159">**Yritys** – Yritys, joka omistaa tilauksen</span><span class="sxs-lookup"><span data-stu-id="2373a-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="2373a-160">**Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili</span><span class="sxs-lookup"><span data-stu-id="2373a-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="2373a-161">**Hinnasto** – Asiakkaan mukautettu hinnasto</span><span class="sxs-lookup"><span data-stu-id="2373a-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="2373a-162">**Valuutta** – Hinnan valuutta</span><span class="sxs-lookup"><span data-stu-id="2373a-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="2373a-163">**Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan</span><span class="sxs-lookup"><span data-stu-id="2373a-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="2373a-164">Seuraavat kentät määritetään automaattisesti myyntitilaustauluun:</span><span class="sxs-lookup"><span data-stu-id="2373a-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="2373a-165">**Kieli** – Tilauksen kieli (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-166">**Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-167">**Yhteyshenkilö** – Käyttäjä, jolle voidaan ottaa yhteyttä tilauksen lisätietoja varten (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-168">**Yritys** – Yritys, johon tilaus kuuluu (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-169">**Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-170">**Laskutusasiakas** – Tilauksen laskutustili (Oletusarvo on potentiaalinen asiakas yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="2373a-171">**Myyntitilauksen nimi** – Myyntitilauksen nimi (oletusarvo on **myyntitilaus**.)</span><span class="sxs-lookup"><span data-stu-id="2373a-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="2373a-172">**Valuutta** – Hinnan valuutta (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-173">**Hinnasto** – Asiakkaan mukautettu hinnasto (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)</span><span class="sxs-lookup"><span data-stu-id="2373a-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="2373a-174">**Toimitusosoitteen kuvaus** – Myyntitilauksen toimitusosoite (oletusarvo on **Toimitusosoitteen kuvaus**.)</span><span class="sxs-lookup"><span data-stu-id="2373a-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="2373a-175">Tilauksen luomisprosessin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2373a-175">Modify the order creation process</span></span>

<span data-ttu-id="2373a-176">Voit muokata asiakasportaalin ulkoasua ja käyttöliittymää vapaasti, jos et muuta perustilauksen luomisprosessia.</span><span class="sxs-lookup"><span data-stu-id="2373a-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="2373a-177">Jos haluat muuttaa tilauksen luomisprosessia, on joitakin seikkoja, jotka on syytä pitää mielessä.</span><span class="sxs-lookup"><span data-stu-id="2373a-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="2373a-178">Älä poista seuraavia sarakkeita myyntitilaustaulusta Microsoft Dataversessa, koska niitä tarvitaan myyntitilauksen luomiseen kaksoiskirjoituksessa:</span><span class="sxs-lookup"><span data-stu-id="2373a-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="2373a-179">**Yritys** – Yritys, joka omistaa tilauksen</span><span class="sxs-lookup"><span data-stu-id="2373a-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="2373a-180">**Nimi** – Myyntitilauksen nimi</span><span class="sxs-lookup"><span data-stu-id="2373a-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="2373a-181">**Valuutta** – Hinnan valuutta</span><span class="sxs-lookup"><span data-stu-id="2373a-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="2373a-182">**Hinnasto** – Asiakkaan mukautettu hinnasto</span><span class="sxs-lookup"><span data-stu-id="2373a-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="2373a-183">**Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan</span><span class="sxs-lookup"><span data-stu-id="2373a-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="2373a-184">**Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili</span><span class="sxs-lookup"><span data-stu-id="2373a-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="2373a-185">**Kieli** – Tilauksen kieli (yleensä tämä kieli on mahdollisen asiakkaan kieli.)</span><span class="sxs-lookup"><span data-stu-id="2373a-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="2373a-186">**Toimitusosoitteen kuvaus** – Myyntitilauksen toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="2373a-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="2373a-187">Nimikkeille tarvitaan seuraavat sarakkeet:</span><span class="sxs-lookup"><span data-stu-id="2373a-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="2373a-188">**Tuote** – Tilattava tuote</span><span class="sxs-lookup"><span data-stu-id="2373a-188">**Product** – The product to order</span></span>
- <span data-ttu-id="2373a-189">**Määrä** – Valitun tuotteen määrä</span><span class="sxs-lookup"><span data-stu-id="2373a-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="2373a-190">**Yksikkö** – Mittayksikkö (esimerkiksi **kpl**, **kg** tai **laatikko**)</span><span class="sxs-lookup"><span data-stu-id="2373a-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="2373a-191">**Lähetys maa/alue** – Toimitusmaa tai -alue</span><span class="sxs-lookup"><span data-stu-id="2373a-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="2373a-192">**Toimitusosoitteen kuvaus** – Tilauksen toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="2373a-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="2373a-193">Varmista, että asiakasportaali lähettää jollakin tavalla kaikkien näiden sarakkeiden arvot.</span><span class="sxs-lookup"><span data-stu-id="2373a-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="2373a-194">Jos haluat lisätä sivulle sarakkeita tai poistaa sarakkeita, lisätietoja on kohdassa [Pikaluonnin lomakkeiden luominen tai muokkaaminen selkeytettyä tietojen syöttökokemusta varten](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="2373a-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="2373a-195">Jos haluat muuttaa tapaa, jolla sarakkeet on määritetty valmiiksi ja arvot määritetään, kun sivu tallennetaan, tutustu seuraaviin Power Apps -portaalin käyttöohjeissa oleviin tietoihin:</span><span class="sxs-lookup"><span data-stu-id="2373a-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="2373a-196">Täytä kenttä valmiiksi</span><span class="sxs-lookup"><span data-stu-id="2373a-196">Prepopulate field</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="2373a-197">Aseta arvo tallennettaessa</span><span class="sxs-lookup"><span data-stu-id="2373a-197">Set Value On Save</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="2373a-198">Kotisivun mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2373a-198">Customize the home page</span></span>

<span data-ttu-id="2373a-199">Kaikki asiakasportaalin ohjausobjektit ovat sisäänrakennettuja Power Apps -portaalien ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="2373a-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="2373a-200">Voit mukauttaa niitä noudattamalla ohjeita, jotka liittyvät [sivun luomiseen](/powerapps/maker/portals/compose-page) Power Apps -portaalien dokumentaatiossa.</span><span class="sxs-lookup"><span data-stu-id="2373a-200">You can customize them by following the steps in [Compose a page](/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="2373a-201">Vain asiakasportaalin mallipohjaan sisältyvää mukautettua ohjausobjektia käytetään luotaessa ruutuja kotisivulle.</span><span class="sxs-lookup"><span data-stu-id="2373a-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="2373a-202">![Kotisivun ruudut](media/customer-portal-home-page-tiles.png "Kotisivun ruudut")</span><span class="sxs-lookup"><span data-stu-id="2373a-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="2373a-203">Voit muokata ruutuja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2373a-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="2373a-204">Avaa [Portaalin hallintasovellus](/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="2373a-204">Open the [Portal Management app](/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="2373a-205">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivumallit**.</span><span class="sxs-lookup"><span data-stu-id="2373a-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="2373a-206">![Portaalinhallinnan siirtymisruutu](media/customer-portal-nav.png "Portaalinhallinnan siirtymisruutu")</span><span class="sxs-lookup"><span data-stu-id="2373a-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="2373a-207">Valitse sivupohja, jonka nimi on **Koti**.</span><span class="sxs-lookup"><span data-stu-id="2373a-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="2373a-208">Avaa sivun lähdekoodi valitsemalla **Verkkomalli**-kentässä **Koti**-linkki.</span><span class="sxs-lookup"><span data-stu-id="2373a-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="2373a-209">![Verkkomallin kenttä](media/customer-portal-web-template.png "Verkkomallin kenttä")</span><span class="sxs-lookup"><span data-stu-id="2373a-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="2373a-210">Sinun pitäisi nyt nähdä koko kotisivun lähdekoodi ja voi muokata sitä kuin tarvitset.</span><span class="sxs-lookup"><span data-stu-id="2373a-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="2373a-211">Resurssit</span><span class="sxs-lookup"><span data-stu-id="2373a-211">Resources</span></span>

<span data-ttu-id="2373a-212">Lisätietoja asiakasportaalin määrittämisestä ja mukauttamisesta on seuraavissa resursseissa:</span><span class="sxs-lookup"><span data-stu-id="2373a-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="2373a-213">Power Apps -portaalit -dokumentaatio</span><span class="sxs-lookup"><span data-stu-id="2373a-213">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="2373a-214">Kaksoiskirjoituksen dokumentointi</span><span class="sxs-lookup"><span data-stu-id="2373a-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="2373a-215">Tietoja portaalin elinkaaresta</span><span class="sxs-lookup"><span data-stu-id="2373a-215">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="2373a-216">Portaalin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="2373a-216">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="2373a-217">Portaalin konfiguraation siirtäminen</span><span class="sxs-lookup"><span data-stu-id="2373a-217">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="2373a-218">Ratkaisun elinkaaren hallinta: Dynamics 365 for Customer Engagement -sovellukset</span><span class="sxs-lookup"><span data-stu-id="2373a-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]