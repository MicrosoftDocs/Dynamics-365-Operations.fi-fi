---
title: Tiedon etsiminen hakujen avulla
description: "Monessa Microsoft Dynamics 365 for Finance and Operations -kentässä on hakuja, jotka auttavat sinua löytämään oikean tai halutun arvo. Hakuihin on lisätty useita parannuksia, jotka helpottavat näiden ohjausobjektien käyttöä ja parantavat käyttäjien tuottavuutta. Tässä ohjeaiheessa tutustutaan uusiin hakuominaisuuksiin ja annetaan joitain vinkkejä, joiden avulla käytät järjestelmän hakuja optimaalisesti."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6c3499e483331eeef88e65f5f3bf1288dd71b268
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="use-lookups-to-find-information"></a><span data-ttu-id="dd905-105">Tiedon etsiminen hakujen avulla</span><span class="sxs-lookup"><span data-stu-id="dd905-105">Use lookups to find information</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd905-106">Monessa Microsoft Dynamics 365 for Finance and Operations -kentässä on hakuja, jotka auttavat sinua löytämään oikean tai halutun arvo.</span><span class="sxs-lookup"><span data-stu-id="dd905-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="dd905-107">Hakuihin on lisätty useita parannuksia, jotka helpottavat näiden ohjausobjektien käyttöä ja parantavat käyttäjien tuottavuutta.</span><span class="sxs-lookup"><span data-stu-id="dd905-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="dd905-108">Tässä ohjeaiheessa tutustutaan uusiin hakuominaisuuksiin ja annetaan joitain vinkkejä, joiden avulla käytät järjestelmän hakuja optimaalisesti.</span><span class="sxs-lookup"><span data-stu-id="dd905-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>  

<a name="responsive-lookups"></a><span data-ttu-id="dd905-109">Reagoivat haut</span><span class="sxs-lookup"><span data-stu-id="dd905-109">Responsive lookups</span></span>
------------------

<span data-ttu-id="dd905-110">Aiemmissa Finance and Operations -versioissa haku-ohjausobjektin käyttäminen edellytti käyttäjiltä valikon avaamista erikseen.</span><span class="sxs-lookup"><span data-stu-id="dd905-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="dd905-111">Tämä saattoi olla toteutettu kirjoittamalla ohjausobjektiin tähti (\*), jolla hakua suodatettiin ohjausobjektin nykyisen arvon mukaisesti, napsauttamalla valikon painiketta, tai käyttämällä **Alt**+**Alanuoli** -pikanäppäintä.</span><span class="sxs-lookup"><span data-stu-id="dd905-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="dd905-112">Hakuobjekteja on muutettu seuraavilla tavoilla, jotta ne vastaisivat nykyisiä verkkosivukäytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="dd905-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

-   <span data-ttu-id="dd905-113">Haku-pudotusvalikot aukeavat nyt automaattisesti hetken kuluttua, kun kirjoittaminen on päättynyt, ja valikon sisältö suodatetaan hakuobjektin arvon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dd905-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>
    -   <span data-ttu-id="dd905-114">Huomaa, että vanha tapa avata hakuvalikko automaattisesti tähden (\*) kirjoittamisen jälkeen on poistunut.</span><span class="sxs-lookup"><span data-stu-id="dd905-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>
-   <span data-ttu-id="dd905-115">Kun hakuvalikko on avattu, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="dd905-115">After the lookup drop-down menu has opened, the following will occur:</span></span>
    -   <span data-ttu-id="dd905-116">Kohdistin jää hakuobjektiin (sen sijaan, että se siirtyisi valikkoon), jotta voit jatkaa hakusanan kirjoittamista.</span><span class="sxs-lookup"><span data-stu-id="dd905-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="dd905-117">Käyttäjä voi kuitenkin käyttää **Ylä**- ja **Alanuoli** -näppäimiä vaihtaakseen valikon riviä ja Enter-painiketta valitakseen valikossa valitun rivin.</span><span class="sxs-lookup"><span data-stu-id="dd905-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    -   <span data-ttu-id="dd905-118">Valikon sisältö mukautuu hakuobjektin muutosten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dd905-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="dd905-119">Otetaan esimerkiksi hakukenttä **Kaupunki**.</span><span class="sxs-lookup"><span data-stu-id="dd905-119">For example, consider a lookup field called **City**.</span></span> 

<span data-ttu-id="dd905-120">Kun kohdistus on **Kaupunki**-kentässä, voit aloittaa haluamasi kaupungin etsinnän kirjoittamalla muutaman kirjaimen, kuten "col".</span><span class="sxs-lookup"><span data-stu-id="dd905-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span>  <span data-ttu-id="dd905-121">Kun lopetat kirjoittamisen, haku avautuu automaattisesti ja se suodatetaan näyttämään kaupungit, jotka alkavat kirjaimilla "col".</span><span class="sxs-lookup"><span data-stu-id="dd905-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span> 

<span data-ttu-id="dd905-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="dd905-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span> 

<span data-ttu-id="dd905-123">Tässä vaiheessa kohdistin on edelleen hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="dd905-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="dd905-124">Jos jatkat kirjoittamista, niin, että arvo on "colum", haun sisältö mukautuu automaattisesti vastaamaan hakuobjektin uusinta arvoa.</span><span class="sxs-lookup"><span data-stu-id="dd905-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span> 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

<span data-ttu-id="dd905-126">Vaikka kohdistus on yhä hakuobjektissa, voit käyttää lisäksi **Ylä-** ja **Alanuoli**-näppäimiä korostaaksesi rivin, jonka haluat valita.</span><span class="sxs-lookup"><span data-stu-id="dd905-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="dd905-127">Painamalla **Enter**-näppäintä korostettu rivi valitaan hausta ja ohjausobjektin arvo päivittyy.</span><span class="sxs-lookup"><span data-stu-id="dd905-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span> 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="dd905-129">Muiden kuin tunnisteiden kirjoittaminen</span><span class="sxs-lookup"><span data-stu-id="dd905-129">Typing in more than IDs</span></span>
<span data-ttu-id="dd905-130">Kun kirjoitat tietoja, on luonnollista yrittää tunnistaa yksikkö, kuten asiakas tai toimittaja, nimen perusteella yksikköä edustavan tunnisteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="dd905-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="dd905-131">Nykyisessä Finance and Operations -versiossa moni (ei kuitenkaan kaikki) haku sallii nyt kontekstitietojen kirjoittamisen.</span><span class="sxs-lookup"><span data-stu-id="dd905-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="dd905-132">Tämä ominaisuus sallii käyttäjän kirjoittaa tunnisteen tai sitä vastaavan nimen hakuobjektiin.</span><span class="sxs-lookup"><span data-stu-id="dd905-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span> 

<span data-ttu-id="dd905-133">Esimerkkinä voimme käyttää **Asiakkaan tili** -kenttää, kun luot myyntitilausta.</span><span class="sxs-lookup"><span data-stu-id="dd905-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="dd905-134">Tässä kentässä näytetään asiakkaan **Tilitunnus**, mutta käyttäjä kirjoittaa yleensä mieluummin tähän kenttään **tilin nimen** **tilitunnuksen** sijaan luodessaan myyntitilauksia, kuten "Forest Wholesales" "US-003":n sijaan.</span><span class="sxs-lookup"><span data-stu-id="dd905-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="dd905-135">Jos käyttäjä syöttää **tilitunnuksen** hakuobjektiin, valikko aukeaa automaattisesti edellisessä osassa kuvatun mukaisesti, ja käyttäjä näkee alla olevan kuvan mukaisen haun.</span><span class="sxs-lookup"><span data-stu-id="dd905-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="dd905-136">[![Kontekstihaku, kun asiakkaan tilitunnus on syötetty](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="dd905-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="dd905-137">Käyttäjät voivat nyt myös aloittaa **tilin nimen** kirjoittamisen.</span><span class="sxs-lookup"><span data-stu-id="dd905-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="dd905-138">Jos tämä havaitaan, käyttäjä näkee seuraavanlaisen haun.</span><span class="sxs-lookup"><span data-stu-id="dd905-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="dd905-139">Huomaa, kuinka **Nimi**-sarake siirretään haun ensimmäiseen sarakkeeseen ja kuinka haku järjestetään ja suodatetaan **Nimi**-sarakkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="dd905-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="dd905-140">[![Kontekstihaku, kun asiakkaan tilin nimi on syötetty](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="dd905-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="dd905-141">Ruudukon sarakeotsikoiden käyttäminen edistyneempään suodattamiseen ja lajitteluun</span><span class="sxs-lookup"><span data-stu-id="dd905-141">Using grid column headers for more advanced filtering and sorting</span></span>
<span data-ttu-id="dd905-142">Edellisissä osiossa käsitellyt haun parannukset helpottavat käyttäjän mahdollisuuksia siirtyä haun rivien välillä "alkaa"-tyyppisen **tunnus**- tai **nimi**-kenttähaun perusteella.</span><span class="sxs-lookup"><span data-stu-id="dd905-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="dd905-143">On kuitenkin tilanteita, joissa oikean rivin löytäminen vaatii edistyneempiä suodattimia tai lajittelua.</span><span class="sxs-lookup"><span data-stu-id="dd905-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="dd905-144">Näissä tilanteissa käyttäjän on käytettävä haun sisäisiä ruudukon sarakeotsikoiden suodatus- ja lajitteluasetuksia.</span><span class="sxs-lookup"><span data-stu-id="dd905-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="dd905-145">Otetaan esimerkiksi työntekijä, joka on syöttämässä myyntitilausriviä, johon on haettava oikea "kaapeli" tuotteeksi.</span><span class="sxs-lookup"><span data-stu-id="dd905-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="dd905-146">Kirjoittamalla "kaapeli" **Nimiketunnus**-objektiin ei auta, sillä järjestelmässä ei ole "kaapeli"-alkuisia tuotenimiä.</span><span class="sxs-lookup"><span data-stu-id="dd905-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span> 

![emptyitemlookup](./media/emptyitemlookup.png) 

<span data-ttu-id="dd905-148">Sen sijaan käyttäjän on tyhjennettävä hakuobjektin arvo ja avattava haun valikko, jota hänen on suodatettava ruudukon sarakeotsikon avulla, alla olevan kuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dd905-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="dd905-149">Hiiren (tai kosketusnäytön) käyttäjä voi yksinkertaisesti napsauttaa (tai koskettaa) mitä tahansa sarakkeen otsikkoa avatakseen kyseisen sarakkeen suodatus- ja lajitteluvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="dd905-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="dd905-150">Näppäimistön käyttäjän on yksinkertaisesti painettava **Alt**+**Ala****nuoli**-näppäintä toisen kerran, joka siirtää kohdistuksen avattavaan valikkoon, jonka jälkeen käyttäjä siirtyä oikeaan sarakkeeseen sarkaimella ja painaa sitten **Ctrl**+**G** -pikanäppäintä avatakseen ruudukon sarakeotsikon valikon.</span><span class="sxs-lookup"><span data-stu-id="dd905-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span> 

<span data-ttu-id="dd905-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="dd905-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span> 

<span data-ttu-id="dd905-152">Kun suodatin on otettu käyttöön (ks. alla oleva kuva), käyttäjä voi paikantaa rivin tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="dd905-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span> 

![filtereditemlookup](./media/filtereditemlookup.png)




