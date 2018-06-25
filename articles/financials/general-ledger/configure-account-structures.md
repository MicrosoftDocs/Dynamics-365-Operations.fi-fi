---
title: "Määritä tilirakenteet"
description: "Tässä aiheessa on tietoja tilirakenteista ja taloushallinnon dimensioista."
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.contentlocale: fi-fi
ms.lasthandoff: 05/21/2018

---

# <a name="configure-account-structures"></a><span data-ttu-id="d2c63-103">Määritä tilirakenteet</span><span class="sxs-lookup"><span data-stu-id="d2c63-103">Configure account structures</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d2c63-104">Tilirakenteet käyttävät päätiliä ja taloushallinnon dimensioita luodakseen sääntöjä, jotka määrittävät järjestyksen ja arvot määrittäessäsi tilinumeron.</span><span class="sxs-lookup"><span data-stu-id="d2c63-104">Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</span></span> <span data-ttu-id="d2c63-105">Voit määrittää niin monta tilirakennetta kuin on tarpeen yrityksesi kannalta.</span><span class="sxs-lookup"><span data-stu-id="d2c63-105">You can set up as many account structures as you need for your business.</span></span> <span data-ttu-id="d2c63-106">Tilirakenteet määritetään yrityksen kirjausasetuksiin, jotta ne voidaan jakaa.</span><span class="sxs-lookup"><span data-stu-id="d2c63-106">The account structures are assigned to a company’s ledger setup, so they can be shared.</span></span>

<span data-ttu-id="d2c63-107">Tilirakennetta luotaessa segmenttien enimmäismäärä on 11.</span><span class="sxs-lookup"><span data-stu-id="d2c63-107">When creating an account structure, the maximum number of segments is 11.</span></span> <span data-ttu-id="d2c63-108">Jos tarvitset enemmän segmenttejä, arvioi huolellisesti asetukset ja vaatimukset, koska se vaikuttaa käyttökokemukseen.</span><span class="sxs-lookup"><span data-stu-id="d2c63-108">If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</span></span> <span data-ttu-id="d2c63-109">Harkitse, jos segmentti voidaan johtaa käyttämällä hierarkiaa tietojen syöttöhetken sijaan tai käyttämällä käyttäjän määrittämää kenttää.</span><span class="sxs-lookup"><span data-stu-id="d2c63-109">Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</span></span> <span data-ttu-id="d2c63-110">Esimerkiksi jos haluat raportoida sijainnista, mutta voit määrittää sijainnin kustannuspaikan tai osaston mukaan, et tarvitse siajintia taloushallinnon dimensioksi.</span><span class="sxs-lookup"><span data-stu-id="d2c63-110">For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</span></span> <span data-ttu-id="d2c63-111">Jos arvioinnin jälkeen, että tarvitse enemmän kuin 11 segmenttiä, voit lisätä uusia segmenttejä lisäsääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="d2c63-111">If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</span></span>

<span data-ttu-id="d2c63-112">Tilirakenteet edellyttävät päätilin.</span><span class="sxs-lookup"><span data-stu-id="d2c63-112">Account structures require the main account.</span></span> <span data-ttu-id="d2c63-113">Päätilin ei tarvitse olla rakenteen ensimmäinen segmentti, mutta se yksilöi, mitä tilirakennetta käytetään syötettäessä tilinumeroa.</span><span class="sxs-lookup"><span data-stu-id="d2c63-113">The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</span></span> <span data-ttu-id="d2c63-114">Näin ollen päätilin arvo voi olla vain yhdessä kirjanpitoon määritetyssä rakenteessa, jotta ne eivät ole päällekkäiset.</span><span class="sxs-lookup"><span data-stu-id="d2c63-114">Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</span></span> <span data-ttu-id="d2c63-115">Tilirakenteen tunnistuksen jälkeen suodatetaan sallittujen arvojen luettelo ohjatakseen käyttäjää valitsemaan vain voimassa olevia dimensioarvoja, näin vähentäen kirjauskansion virheellisen kirjauksen mahdollisuutta.</span><span class="sxs-lookup"><span data-stu-id="d2c63-115">After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</span></span>

> [!NOTE] 
> <span data-ttu-id="d2c63-116">Jos aiot budjetoida taloushallinnon dimension mukaan, sen on kuuluttava tilirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="d2c63-116">If you plan to budget against a financial dimension, it will need to be part of an account structure.</span></span> <span data-ttu-id="d2c63-117">Budjetointi ei tällä hetkellä käytä lisäsääntöjä.</span><span class="sxs-lookup"><span data-stu-id="d2c63-117">Budgeting does not currently utilize advanced rules.</span></span>

## <a name="example"></a><span data-ttu-id="d2c63-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d2c63-118">Example</span></span>
<span data-ttu-id="d2c63-119">Kuvataksemme tilirakenteen määrittämisen parhaita käytäntöjä, oletetaan, että yritys haluaa seurata tasetilejänsä (100000..399999) tasolla tilin ja liiketoimintayksikön taloushallinnon dimension tasolla.</span><span class="sxs-lookup"><span data-stu-id="d2c63-119">To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</span></span> <span data-ttu-id="d2c63-120">Tuotto-ja kulutileissä (400000..999999) he seuraavat taloushallinnon dimensioita Liiketoimintayksikkö, Osasto ja Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="d2c63-120">For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</span></span> <span data-ttu-id="d2c63-121">Jos he myyvät, he myös haluavat seurata kohdetta Asiakas.</span><span class="sxs-lookup"><span data-stu-id="d2c63-121">If they make a sale, they also like to track Customer.</span></span> <span data-ttu-id="d2c63-122">Käyttämällä tätä skenaariota on suositeltavaa käyttää kahta tilirakennetta, jotka on määritetty yrityksen kirjanpitoon - yksi tasetileille ja toinen tulos- ja tappiotileille.</span><span class="sxs-lookup"><span data-stu-id="d2c63-122">Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</span></span> <span data-ttu-id="d2c63-123">Käyttäjäkokemuksen ja oikeellisuustarkistuksen optimoimiseksi Asiakas tulisi olla lisäsääntö, jota käytetään vain, kun myynnin tiliä käytetään.</span><span class="sxs-lookup"><span data-stu-id="d2c63-123">To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</span></span>

<span data-ttu-id="d2c63-124">**Tasetilirakenne**</span><span class="sxs-lookup"><span data-stu-id="d2c63-124">**Balance sheet account structure**</span></span>

|<span data-ttu-id="d2c63-125">Päätili</span><span class="sxs-lookup"><span data-stu-id="d2c63-125">Main account</span></span>          | <span data-ttu-id="d2c63-126">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="d2c63-126">Business unit</span></span>    |
|----------------------|-----------|
|<span data-ttu-id="d2c63-127">100000..399999</span><span class="sxs-lookup"><span data-stu-id="d2c63-127">100000..399999</span></span> | <span data-ttu-id="d2c63-128">\*;” “</span><span class="sxs-lookup"><span data-stu-id="d2c63-128">\*;” “</span></span>|

<span data-ttu-id="d2c63-129">**Voitt- ja tappiotilirakenne**</span><span class="sxs-lookup"><span data-stu-id="d2c63-129">**Profit and loss account structure**</span></span>

|<span data-ttu-id="d2c63-130">Päätili</span><span class="sxs-lookup"><span data-stu-id="d2c63-130">Main account</span></span>          | <span data-ttu-id="d2c63-131">Liiketoimintayksikkö</span><span class="sxs-lookup"><span data-stu-id="d2c63-131">Business unit</span></span>    |<span data-ttu-id="d2c63-132">Osasto</span><span class="sxs-lookup"><span data-stu-id="d2c63-132">Department</span></span>          | <span data-ttu-id="d2c63-133">Kustannuspaikka</span><span class="sxs-lookup"><span data-stu-id="d2c63-133">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="d2c63-134">400000..999999</span><span class="sxs-lookup"><span data-stu-id="d2c63-134">400000..999999</span></span> | <span data-ttu-id="d2c63-135">\*;” “</span><span class="sxs-lookup"><span data-stu-id="d2c63-135">\*;” “</span></span>|<span data-ttu-id="d2c63-136">\*;” “</span><span class="sxs-lookup"><span data-stu-id="d2c63-136">\*;” “</span></span>|<span data-ttu-id="d2c63-137">\*;” “</span><span class="sxs-lookup"><span data-stu-id="d2c63-137">\*;” “</span></span>|<span data-ttu-id="d2c63-138">\*;” “</span><span class="sxs-lookup"><span data-stu-id="d2c63-138">\*;” “</span></span>|

<span data-ttu-id="d2c63-139">**Lisäsääntö asiakkaan lisäämiseksi**</span><span class="sxs-lookup"><span data-stu-id="d2c63-139">**Advanced rule for adding a Customer**</span></span>

<span data-ttu-id="d2c63-140">Ehto: Kun Päätili on välillä 400000–499999, lisää asiakas.</span><span class="sxs-lookup"><span data-stu-id="d2c63-140">Criteria: Where Main account is between 400000 and 499999, then add customer.</span></span> <span data-ttu-id="d2c63-141">Tätä ei voi jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="d2c63-141">It cannot be left blank.</span></span>

|<span data-ttu-id="d2c63-142">Asiakas</span><span class="sxs-lookup"><span data-stu-id="d2c63-142">Customer</span></span>         |
|-----------------|
|* |

<span data-ttu-id="d2c63-143">Tässä yksinkertaistetussa esimerkissä kaikki arvot ja tyhjät sallitaan - siksi käytetään merkkejä \* ja ” ”.</span><span class="sxs-lookup"><span data-stu-id="d2c63-143">In this simplified example, all values and blank are allowed so \* and “ “ are used.</span></span>

## <a name="segments-and-allowed-values"></a><span data-ttu-id="d2c63-144">Segmentit ja sallitut arvot</span><span class="sxs-lookup"><span data-stu-id="d2c63-144">Segments and allowed values</span></span>
<span data-ttu-id="d2c63-145">**Segmentit**- ja **Sallitun arvon tiedot**-osa sisältää ruudukon kaltaisen kokemuksen lisäämään sääntöjä, joita noudatetaan tarkistuksessa kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="d2c63-145">The **Segments** and **Allowed values details** section provides a grid like experience for entering the rules that will be followed on validation during posting.</span></span> <span data-ttu-id="d2c63-146">Voit kirjoittaa suoraan soluihin ruudukossa, tuoda sen Excelistä tai käyttää **Sallitun arvon tiedot** -osaa prosessin opastuksena.</span><span class="sxs-lookup"><span data-stu-id="d2c63-146">You can type directly in the cells in the grid, import it from Excel, or use the **Allowed value details** section to guide you through it.</span></span>

<span data-ttu-id="d2c63-147">**Sallitun arvon tiedot** -osa ohjaa, kun luot ehtoja käyttäen **operaattoreita**, kuten alkaa merkillä, on välillä, sisältää ja monia muita.</span><span class="sxs-lookup"><span data-stu-id="d2c63-147">The **Allowed value details** section guides you through creating criteria using **Operators** such as begins with, is between, includes, and many others.</span></span>

<span data-ttu-id="d2c63-148">[![Salli arvot](./media/account.png)](./media/account.png)</span><span class="sxs-lookup"><span data-stu-id="d2c63-148">[![Allow values](./media/account.png)](./media/account.png)</span></span> 

## <a name="more-than-7-criteria-needed"></a><span data-ttu-id="d2c63-149">Tarvitaan yli 7 ehtoa</span><span class="sxs-lookup"><span data-stu-id="d2c63-149">More than 7 criteria needed</span></span>

<span data-ttu-id="d2c63-150">Jos tarvitset yli 7 ehtoa, voit jatkaa lisäämällä niitä seuraavalla rivillä.</span><span class="sxs-lookup"><span data-stu-id="d2c63-150">If you have more than 7 criteria that are needed, you can continue adding them on the next line.</span></span> <span data-ttu-id="d2c63-151">Huomaat, kun käytät **Sallitun arvon tiedot** -osaa, että **+Lisää uusi** -ehto ei ole enää aktiivinen seitsemännen ehdon syöttämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d2c63-151">You will notice when working in the **Allowed value details** section that the **+Add new** criteria is nt longer active after the seventh criteria is entered.</span></span> <span data-ttu-id="d2c63-152">Tämä johtuu monista tekijöistä, esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="d2c63-152">This is due to many factors such as:</span></span> 
 - <span data-ttu-id="d2c63-153">Sarakkeen leveys</span><span class="sxs-lookup"><span data-stu-id="d2c63-153">Column width</span></span> 
 - <span data-ttu-id="d2c63-154">Miten tiedot on tallennettu</span><span class="sxs-lookup"><span data-stu-id="d2c63-154">How the data is stored</span></span> 
 - <span data-ttu-id="d2c63-155">**Sallitun arvon tiedot** -ohjausobjektin tehokkuudesta</span><span class="sxs-lookup"><span data-stu-id="d2c63-155">Performance of the **Allowed value details** control</span></span>
 - <span data-ttu-id="d2c63-156">Käyettävyydestä</span><span class="sxs-lookup"><span data-stu-id="d2c63-156">Usability</span></span>  
 
<span data-ttu-id="d2c63-157">Jatkaaksesi lisäehtojen lisäämistä, valitse **Monista segmentissä** ja **Sallitut arvot -osa**.</span><span class="sxs-lookup"><span data-stu-id="d2c63-157">To continue to add additional criteria, click **Duplicate in the Segment** and **Allowed values section**.</span></span> <span data-ttu-id="d2c63-158">Ehdot kopioidaan uudelle riville.</span><span class="sxs-lookup"><span data-stu-id="d2c63-158">This will copy the criteria to a new line.</span></span> <span data-ttu-id="d2c63-159">Voit kirjoittaa päälle tai muokata **Sallitun arvon tiedot** -osaa.</span><span class="sxs-lookup"><span data-stu-id="d2c63-159">You can then type over or modify the **Allowed value details** section.</span></span>

<span data-ttu-id="d2c63-160">(LINKKI VIDEOON, JOKA LUODAAN)</span><span class="sxs-lookup"><span data-stu-id="d2c63-160">(LINK TO VIDEO THAT WILL BE CREATED)</span></span>

## <a name="best-practices"></a><span data-ttu-id="d2c63-161">Parhaat käytännöt</span><span class="sxs-lookup"><span data-stu-id="d2c63-161">Best practices</span></span>
<span data-ttu-id="d2c63-162">Määrittäessäsi tilirakenteita on suositeltavia parhaita käytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="d2c63-162">When setting up your account structures there are some best practices you can follow.</span></span> <span data-ttu-id="d2c63-163">Kuitenkin nämä ovat vain ohjeita, joten kokonaisvaltainen keskustelu liiketoiminnastasi, kasvusuunnitelmasta ja huoltosuunnitelmasta tulisi olla osa tätä keskustelua.</span><span class="sxs-lookup"><span data-stu-id="d2c63-163">However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</span></span>

- <span data-ttu-id="d2c63-164">Tee päätilistä ensimmäinen tai tilirakenteen mahdollisimman alussa, jotta käyttäjät saavat parhaimman ohjatun kokemuksen tilille syötettäessä.</span><span class="sxs-lookup"><span data-stu-id="d2c63-164">Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</span></span>

- <span data-ttu-id="d2c63-165">Käytä tilirakenteita mahdollisimman paljon uudelleen vähentääksesi ylläpitoa yritystesi välillä.</span><span class="sxs-lookup"><span data-stu-id="d2c63-165">Reuse account structures as much as possible to reduce maintenance across your legal entities.</span></span>

- <span data-ttu-id="d2c63-166">Eri yritysten vaihteluissa harkitse lisäsääntöjä siten, että tilirakenteita voidaan käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d2c63-166">For variations across legal entities, consider using advanced rules so that account structures can be reused.</span></span>

- <span data-ttu-id="d2c63-167">Kun määrität sallittuja arvoja,käytä arvoalueita ja yleismerkkejä mahdollisimman paljon.</span><span class="sxs-lookup"><span data-stu-id="d2c63-167">When defining allowed values, use ranges and wildcards as much as possible.</span></span> <span data-ttu-id="d2c63-168">Paitsi että näin yritys voi kasvaa ja muuttua ilman ylläpitoa, myös järjestelmä suorittaa paremmin tällä kokoonpanolla.</span><span class="sxs-lookup"><span data-stu-id="d2c63-168">This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</span></span>

- <span data-ttu-id="d2c63-169">Älä aseta tilirakenteen jokaiseen segmenttiin tähtimerkkiä ja sitten luota ainoastaan lisäsääntöihin.</span><span class="sxs-lookup"><span data-stu-id="d2c63-169">Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</span></span> <span data-ttu-id="d2c63-170">Tämä voi olla hankalaa hallita ja se johtaa usein käyttäjän virheeseen ylläpidossa, mikä voi tehdä järjestelmästä sellaiseksi, että sinne ei voi kirjata.</span><span class="sxs-lookup"><span data-stu-id="d2c63-170">This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</span></span>

## <a name="account-structure-activation"></a><span data-ttu-id="d2c63-171">Tilirakenteen aktivointi</span><span class="sxs-lookup"><span data-stu-id="d2c63-171">Account structure activation</span></span>
<span data-ttu-id="d2c63-172">Kun olet tyytyväinen uusiin asetuksiin tai tilirakenteen muutokseen, se on aktivoitava.</span><span class="sxs-lookup"><span data-stu-id="d2c63-172">When you are satifisfied with your new setup or a change to an account structure, you must activate it.</span></span> <span data-ttu-id="d2c63-173">Jos tilirakenne on määritty kirjanpitoon, tämä aktivointi voi kestää pitkään, koska järjestelmän kaikki kirjaamattomat tapahtumat on synkronoitava uuteen rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="d2c63-173">If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</span></span> <span data-ttu-id="d2c63-174">Tilirakenteen muutokset eivät vaikuta kirjattuihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="d2c63-174">Posted transactions are not impacted with account structure changes.</span></span>

<span data-ttu-id="d2c63-175">Lisätietoja on kohdassa [Tilikartan suunnittelu](plan-chart-of-accounts.md), [Taloushallinnon dimensiot](financial-dimensions.md) ja [Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)](enter-account-dimension-combinations-segmented-entry-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2c63-175">For more information, see [Plan your chart of accounts](plan-chart-of-accounts.md), [Financial dimensions](financial-dimensions.md) and [Enter account and dimension combinations (segmented entry control)](enter-account-dimension-combinations-segmented-entry-control.md).</span></span>
