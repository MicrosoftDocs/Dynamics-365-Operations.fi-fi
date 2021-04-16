---
title: Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota
description: Tässä aiheessa käsitellään tilannetta, jossa nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830831"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="83bbb-103">Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota</span><span class="sxs-lookup"><span data-stu-id="83bbb-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83bbb-104">Tässä aiheessa käsitellään tilannetta, jossa nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit.</span><span class="sxs-lookup"><span data-stu-id="83bbb-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="83bbb-105">Vastaanottoassistentti tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="83bbb-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="83bbb-106">Mallitietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="83bbb-106">Enable sample data</span></span>

<span data-ttu-id="83bbb-107">Tässä skenaariossa voi käyttää tässä ohjeaiheessa määritettyjä esimerkkitietueita ja -arvoja, kun vakiosittelytiedot asennettuna ja *USMF*-yritys on valittava ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="83bbb-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="83bbb-108">Voit myös käyttää tätä skenaariota korvaamalla arvot omista tiedoista, jos käytettävissäsi ovat seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="83bbb-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="83bbb-109">Olet vahvistanut ostotilauksen, jossa on avoin ostotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="83bbb-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="83bbb-110">Rivin nimike on varastoitava.</span><span class="sxs-lookup"><span data-stu-id="83bbb-110">The item on the line must be stocked.</span></span> <span data-ttu-id="83bbb-111">Se ei saa käyttää tuotevariantteja eikä sillä saa olla seurantadimensioita.</span><span class="sxs-lookup"><span data-stu-id="83bbb-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="83bbb-112">Nimike on liitettävä varastodimensioryhmään, jossa varastonhallintaprosessi on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="83bbb-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="83bbb-113">Varastonhallintaprosessit on oltava otettuna käyttöön käytettävässä varastossa ja vastaanottoa on ohjattava käytettävässä toimipaikassa rekisterikilvillä.</span><span class="sxs-lookup"><span data-stu-id="83bbb-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="83bbb-114">Varastonhallintaa käyttävän nimikkeen saapumisen kirjauskansion otsikon luominen</span><span class="sxs-lookup"><span data-stu-id="83bbb-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="83bbb-115">Seuraavassa skenaariossa näytetään, miten varastonhallintaa käyttävä nimikkeen saapumisen kirjauskansion otsikko luodaan:</span><span class="sxs-lookup"><span data-stu-id="83bbb-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="83bbb-116">Varmista, että järjestelmässä on vahvistettu ostotilaus, joka täyttää edellisessä osassa kuvatut vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="83bbb-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="83bbb-117">Tässä skenaariossa käytetään ostotilausta yritykselle *USMF* toimittajatilille *1001*, varastolle *51* ja tilausriviä, jossa on *10 PL* (10 kuormalavaa) nimikenumeroa *M9200*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="83bbb-118">Kirjoita käytettävä ostotilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="83bbb-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="83bbb-119">Valitse **Inventoinnin- ja varastonhallinta \> Kirjauskansioviennit \> Nimikkeen saapuminen \> Nimikkeen saapuminen**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="83bbb-120">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="83bbb-121">Näyttöön avautuu **Luo varastonhallinnan kirjauskansio** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="83bbb-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="83bbb-122">Valitse **Nimi**-kentästä kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="83bbb-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="83bbb-123">Jos käytät *USMF*-yrityksen demotietoja, valitse *WHS*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="83bbb-124">Jos käytät omia tietojasi, valitussa kirjauskansiossa **Tarkista keräilysijainti** -asetuksen on oltava *Ei* ja **Karanteeninhallinta**-arvoksi on määritettävä *Ei*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="83bbb-125">Määritä **Viite**-arvoksi *Ostotilaus*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="83bbb-126">Määritä **Tilinumero**-arvoksi *1001*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="83bbb-127">Määritä **Numero** tätä harjoitusta varten tunnistamasi ostotilauksen numeroon.</span><span class="sxs-lookup"><span data-stu-id="83bbb-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="83bbb-128">![Nimikkeen saapumisen kirjauskansio](../media/item-arrival-journal-header.png "Nimikkeen saapumisen kirjauskansio")</span><span class="sxs-lookup"><span data-stu-id="83bbb-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="83bbb-129">Luo kirjauskansion otsikko valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="83bbb-130">Valitse **Kirjauskansion rivit**  -osasta **Lisää rivi** ja kirjoita seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="83bbb-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="83bbb-131">**Nimikenumero** – määritä arvoksi *M9200*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="83bbb-132">**Toimipaikka**, **Varasto** ja **Määrä** asetetaan 10 kuormalavan (1 000 kpl) varastotapahtumatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="83bbb-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="83bbb-133">**Sijainti** – Määritä arvoksi *001*.</span><span class="sxs-lookup"><span data-stu-id="83bbb-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="83bbb-134">Tämä tietty sijainti ei seuraa rekisterikilpiä.</span><span class="sxs-lookup"><span data-stu-id="83bbb-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="83bbb-135">![Nimikkeen saapumisen kirjauskansion rivi](../media/item-arrival-journal-line.png "Nimikkeen saapumisen kirjauskansion rivi")</span><span class="sxs-lookup"><span data-stu-id="83bbb-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="83bbb-136">**Päivämäärä**-kenttä määrittää päivämäärän, jolloin tämän nimikkeen käytettävissä oleva määrä rekisteröidään varastoon.</span><span class="sxs-lookup"><span data-stu-id="83bbb-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="83bbb-137">Järjestelmä lisää **erätunnuksen** tiedot, jos erä voidaan yksilöivästi tunnistaa annetuista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="83bbb-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="83bbb-138">Muussa tapauksessa tiedot on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="83bbb-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="83bbb-139">Tämä on pakollinen kenttä, joka linkittää tämän rekisteröinnin tietylle lähdeasiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="83bbb-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="83bbb-140">Valitse toimintoruudussa **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="83bbb-141">Tämä tarkistaa, että kirjauskansio on valmis kirjattavaksi.</span><span class="sxs-lookup"><span data-stu-id="83bbb-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="83bbb-142">Jos vahvistus epäonnistuu, virheet on korjattava ennen kirjausta kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="83bbb-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="83bbb-143">Näyttöön avautuu **Tarkista kirjauskansio** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="83bbb-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="83bbb-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-144">Select **OK**.</span></span>
1. <span data-ttu-id="83bbb-145">Tarkista sanomapalkki.</span><span class="sxs-lookup"><span data-stu-id="83bbb-145">Review the message bar.</span></span> <span data-ttu-id="83bbb-146">Sanoman pitäisi ilmoittaa, että toiminto on valmis.</span><span class="sxs-lookup"><span data-stu-id="83bbb-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="83bbb-147">Valitse toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="83bbb-148">Näyttöön avautuu **Kirjaa kirjauskansio** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="83bbb-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="83bbb-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-149">Select **OK**.</span></span>
1. <span data-ttu-id="83bbb-150">Tarkista sanomapalkki.</span><span class="sxs-lookup"><span data-stu-id="83bbb-150">Review the message bar.</span></span> <span data-ttu-id="83bbb-151">Sanomien pitäisi ilmoittaa, että toiminto onnistui.</span><span class="sxs-lookup"><span data-stu-id="83bbb-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="83bbb-152">Päivitä ostotilausrivi ja kirjaa tuotteen vastaanotto valitsemalla toimintoruudusta **Toiminnot > Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="83bbb-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
