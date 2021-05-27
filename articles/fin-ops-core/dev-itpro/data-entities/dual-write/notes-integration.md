---
title: Muistiinpanojen integrointi
description: Tässä aiheessa kuvataan muistiinpanotietojen integraatiota kaksoiskirjoituksessa.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018383"
---
# <a name="note-integration"></a><span data-ttu-id="53034-103">Muistiinpanojen integrointi</span><span class="sxs-lookup"><span data-stu-id="53034-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="53034-104">Liiketoimintaprosessien aikana Microsoft Dynamics 365 -käyttäjät usein keräävät tietoja asiakkaistaan.</span><span class="sxs-lookup"><span data-stu-id="53034-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="53034-105">Nämä tiedot tallennetaan aktiviteetteina ja muistiinpanoina.</span><span class="sxs-lookup"><span data-stu-id="53034-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="53034-106">Tässä aiheessa kuvataan muistiinpanotietojen integraatiota kaksoiskirjoituksessa.</span><span class="sxs-lookup"><span data-stu-id="53034-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="53034-107">Asiakastiedot voidaan luokitella seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="53034-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="53034-108">**Toiminnan perustana toimivat tiedot, joita Dynamics 365 -käyttäjä käsittelee asiakkaan puolesta** – Esimerkiksi Contoso (Dynamics 365 -käyttäjä) pitää pelinäytöksen.</span><span class="sxs-lookup"><span data-stu-id="53034-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="53034-109">Yksi Contoson asiakkaista (asiakas) haluaa osallistua pelinäytökseen.</span><span class="sxs-lookup"><span data-stu-id="53034-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="53034-110">Asiakas pyytää Contoso-työntekijää varaamaan paikan pelinäytökseen.</span><span class="sxs-lookup"><span data-stu-id="53034-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="53034-111">Varaus tehdään Contoson tapahtuman osallistujan kalenterissa.</span><span class="sxs-lookup"><span data-stu-id="53034-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="53034-112">**Dynamics 365 -käyttäjän tiedot toiminnan pohjaksi** – Esimerkiksi Surface-yksikköä ostava asiakas määrittää erityisohjeet, jotka ilmaisevat, että laitteen tulee olla lahjapaketissa ennen toimitusta.</span><span class="sxs-lookup"><span data-stu-id="53034-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="53034-113">Nämä ohjeet ovat toimintakelpoisia tietoja, joita pakkauksesta vastaavan Contoso-työntekijän tulisi käsitellä.</span><span class="sxs-lookup"><span data-stu-id="53034-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="53034-114">**Ei-toimittavissa olevat tiedot** – Asiakas esimerkiksi käy Contoso-myymälässä ja ilmaisee myyjälle kiinnostuksen *Halo*-peleihin ja -pelivälineisiin.</span><span class="sxs-lookup"><span data-stu-id="53034-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="53034-115">Myyjä kirjoittaa nämä tiedot muistiinpanoihin.</span><span class="sxs-lookup"><span data-stu-id="53034-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="53034-116">Tämän jälkeen tuotesuositusten ohjelma antaa asiakkaalle suosituksia tiedon perusteella.</span><span class="sxs-lookup"><span data-stu-id="53034-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="53034-117">Yleisesti ottaen toiminnalliset tiedot siepataan *aktiviteetteina* Finance and Operations -sovelluksissa ja asiakasvuorovaikutussovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="53034-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="53034-118">Ei-toiminnalliset tiedot siepataan *muistiinpanoina* Finance and Operations -sovelluksissa ja *huomautuksina* asiakasvuorovaikutussovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="53034-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="53034-119">Vaikka muistiinpanot on tarkoitettu ei-toimintakelpoisten tietojen käsittelemiseen, sovellukset eivät estä niiden käyttämistä toimintakelpoisten tietojen tallennukseen ja käsittelyyn, jos haluat käyttää niitä tällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="53034-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="53034-120">Microsoft julkaisee parhaillaan muistiinpanojen integraation toiminnallisuutta.</span><span class="sxs-lookup"><span data-stu-id="53034-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="53034-121">(Aktiviteettien integroinnin toiminnot julkaistaan myöhemmin.) Muistiinpanojen integrointi on käyettävissä asiakkaille, toimittajille, myyntitilauksille ja ostotilauksille.</span><span class="sxs-lookup"><span data-stu-id="53034-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="53034-122">Muistiinpanon luominen asiakasvuorovaikutussovelluksessa</span><span class="sxs-lookup"><span data-stu-id="53034-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="53034-123">Noudattamalla seuraavia ohjeita voit luoda muistiinpanon asiakasvuorovaikutussovelluksessa ja sitten synkronoida sen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="53034-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="53034-124">Avaa asiakkaan tilitietue asiakasvuorovaikutussovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53034-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="53034-125">Valitse **Aikajana**-ruudusta plusmerkki (**+**) ja luo muistiinpano valitsemalla **Muistiinpano**.</span><span class="sxs-lookup"><span data-stu-id="53034-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Muistiinpanon luominen asiakasvuorovaikutussovelluksessa](media/notes-ce-1.png)

3. <span data-ttu-id="53034-127">Kirjoita otsikko ja kuvaus ja valitse sitten **Lisää muistiinpano**.</span><span class="sxs-lookup"><span data-stu-id="53034-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Kirjoita otsikko ja kuvaus](media/notes-ce-2.png)

    <span data-ttu-id="53034-129">Uusi muistiinpano lisätään asiakkaan aikajanaan.</span><span class="sxs-lookup"><span data-stu-id="53034-129">The new note is added to the customer timeline.</span></span>

    ![Asiakkaan aikajanan uusi muistiinpano](media/notes-ce-3.png)

4. <span data-ttu-id="53034-131">Kirjaudu Finance and Operations -sovellukseen ja avaa sama asiakastietue.</span><span class="sxs-lookup"><span data-stu-id="53034-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="53034-132">Huomaa, että oikeassa yläkulmassa oleva **Liitteet**-painike (paperiliitinsymboli) ilmaisee, että tietueella on liite.</span><span class="sxs-lookup"><span data-stu-id="53034-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Ilmoitus liitteestä](media/notes-ce-4.png)

5. <span data-ttu-id="53034-134">Avaa **Liitteet**-sivu valitsemalla **Liitteet**-painike.</span><span class="sxs-lookup"><span data-stu-id="53034-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="53034-135">Sinu pitäisi nähdä muistiinpano, jonka olet luonut asiakasvuorovaikutussovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53034-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Muistiinpano asiakasvuorovaikutussovelluksesta](media/notes-ce-5.png)

<span data-ttu-id="53034-137">Muistiinpanon päivitykset synkronoidaan Finance and Operations -sovelluksen ja asiakasvuorovaikutussovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="53034-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="53034-138">Muistiinpanon luominen Finance and Operations -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="53034-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="53034-139">Voit luoda muistiinpanon myös Finance and Operations -sovelluksessa ja se sitten synkronoidaan asiakasvuorovaikutussovellukseen.</span><span class="sxs-lookup"><span data-stu-id="53034-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="53034-140">Noudattamalla seuraavia ohjeita voit luoda muistiinpanon Finance and Operations -sovelluksessa ja sitten synkronoida sen asiakasvuorovaikutussovellukseen.</span><span class="sxs-lookup"><span data-stu-id="53034-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="53034-141">Valitse Finance and Operations -sovelluksessa **Liitteet**-sivulla **Uusi** \> **Muistiinpano**.</span><span class="sxs-lookup"><span data-stu-id="53034-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Muistiinpanon luominen Finance and Operations -sovelluksessa](media/notes-fo-1.png)

2. <span data-ttu-id="53034-143">Kirjoita otsikko, lyhyt ohjejoukko ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="53034-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Kirjoita otsikko ja ohjeet](media/notes-fo-2.png)

3. <span data-ttu-id="53034-145">Päivitä tietue asiakasvuorovaikutussovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53034-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="53034-146">Uuden muistiinpanon pitäisi olla aikajanalla.</span><span class="sxs-lookup"><span data-stu-id="53034-146">You should find the new note on the timeline.</span></span>

    ![Aikajanan uusi muistiinpano asiakasvuorovaikutussovelluksessa](media/notes-fo-3.png)

<span data-ttu-id="53034-148">Voit luokitella muistiinpanon sisäiseksi tai ulkoiseksi.</span><span class="sxs-lookup"><span data-stu-id="53034-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="53034-149">Avaa Finance and Operations -sovelluksessa **Liitteet**-sivulla muistiinpano ja valitse sitten **Rajoitus**-kentästä **Sisäinen** tai **Ulkoinen**.</span><span class="sxs-lookup"><span data-stu-id="53034-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Rajoituskenttä](media/notes-fo-4.png)

<span data-ttu-id="53034-151">Voit myös luoda URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="53034-151">You can also create a URL.</span></span>

1. <span data-ttu-id="53034-152">Valitse Finance and Operations -sovelluksessa **Liitteet**-sivulla **Uusi** \> **URL-osoite**.</span><span class="sxs-lookup"><span data-stu-id="53034-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="53034-153">Kirjoita otsikko ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="53034-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="53034-154">Valitse **Rajoitus**-kentästä **Sisäinen** tai **Ulkoinen**.</span><span class="sxs-lookup"><span data-stu-id="53034-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![URL-osoitteen luominen Finance and Operations -sovelluksessa](media/notes-fo-5.png)

4. <span data-ttu-id="53034-156">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="53034-156">Select **Save**.</span></span>

    <span data-ttu-id="53034-157">Koska asiakasvuorovaikutussovelluksissa ei ole URL-tyyppiä, URL-osoite integroidaan kaksoiskirjoituksen avulla muistiinpanona.</span><span class="sxs-lookup"><span data-stu-id="53034-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL-osoitteen näkyminen asiakasvuorovaikutussovelluksessa](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="53034-159">Tiedostoliitteitä ei tueta.</span><span class="sxs-lookup"><span data-stu-id="53034-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="53034-160">Mallit</span><span class="sxs-lookup"><span data-stu-id="53034-160">Templates</span></span>

<span data-ttu-id="53034-161">Muistiinpanojen integraatio sisältää taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="53034-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="53034-162">Finance and Operations -sovellus</span><span class="sxs-lookup"><span data-stu-id="53034-162">Finance and Operations app</span></span> | <span data-ttu-id="53034-163">Asiakkaiden aktivointisovellus</span><span class="sxs-lookup"><span data-stu-id="53034-163">Customer engagement app</span></span> | <span data-ttu-id="53034-164">kuvaus</span><span class="sxs-lookup"><span data-stu-id="53034-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="53034-165">Asiakkaan liitteet</span><span class="sxs-lookup"><span data-stu-id="53034-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="53034-166">Huomautukset</span><span class="sxs-lookup"><span data-stu-id="53034-166">Annotations</span></span> | <span data-ttu-id="53034-167">Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita asiakaskohtaisten tietojen keräämiseen (sekä organisaatioille että henkilöille).</span><span class="sxs-lookup"><span data-stu-id="53034-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="53034-168">Toimittajan asiakirjaliitteet</span><span class="sxs-lookup"><span data-stu-id="53034-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="53034-169">Huomautukset</span><span class="sxs-lookup"><span data-stu-id="53034-169">Annotations</span></span> | <span data-ttu-id="53034-170">Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita toimittajakohtaisten tietojen keräämiseen (sekä organisaatioille että henkilöille).</span><span class="sxs-lookup"><span data-stu-id="53034-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="53034-171">Myyntitilauksen otsikkoasiakirjan liitteet</span><span class="sxs-lookup"><span data-stu-id="53034-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="53034-172">Huomautukset</span><span class="sxs-lookup"><span data-stu-id="53034-172">Annotations</span></span> | <span data-ttu-id="53034-173">Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita myyntitilauskohtasten tietojen sieppaamiseen.</span><span class="sxs-lookup"><span data-stu-id="53034-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="53034-174">Ostotilauksen otsikkoasiakirjan liitteet</span><span class="sxs-lookup"><span data-stu-id="53034-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="53034-175">Huomautukset</span><span class="sxs-lookup"><span data-stu-id="53034-175">Annotations</span></span> | <span data-ttu-id="53034-176">Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita ostotilauskohtaisten tietojen sieppaamiseen.</span><span class="sxs-lookup"><span data-stu-id="53034-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="53034-177">Lisätietoja on [kaksoiskirjoituksen yhdistämismäärityksen viitteessä](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="53034-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
