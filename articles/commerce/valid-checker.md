---
title: Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistus
description: Tässä aiheessa kuvataan tapahtumien yhdenmukaisuuden tarkistuksen toiminnot ohjelmassa Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004248"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="7adbc-103">Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistus</span><span class="sxs-lookup"><span data-stu-id="7adbc-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="7adbc-104">Tässä aiheessa kuvataan tapahtumien yhdenmukaisuuden tarkistuksen toiminnot ohjelmassa Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7adbc-104">This topic describes the transaction consistency checker functionality in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="7adbc-105">Yhdenmukaisuuden tarkistus tunnistaa ja osoittaa ei-yhdenmukaiset tapahtumat, ennen kuin laskelmien kirjaamisprosessi ottaa ne käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="7adbc-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="7adbc-106">Kun laskelma kirjataan, kirjaus saattaa epäonnistua kaupan transaktiotauluissa olevien ei-yhdenmukaisten tietojen johdosta.</span><span class="sxs-lookup"><span data-stu-id="7adbc-106">When a statement is posted, posting can fail due to inconsistent data in the commerce transaction tables.</span></span> <span data-ttu-id="7adbc-107">Ongelma tiedoissa saattaa johtua odottamattomista ongelmista myyntipistesovelluksessa, tai siitä, että tapahtumat on tuotu virheellisesti kolmannen osapuolen myyntipistejärjestelmistä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-107">The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="7adbc-108">Nämä ristiriidat voivat näyttää esimerkiksi seuraavanlaisilta:</span><span class="sxs-lookup"><span data-stu-id="7adbc-108">Examples of how these inconsistencies may appear include:</span></span> 

- <span data-ttu-id="7adbc-109">Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
- <span data-ttu-id="7adbc-110">Otsikkotaulun rivimäärä ei vastaa transaktiotaulun rivimäärää.</span><span class="sxs-lookup"><span data-stu-id="7adbc-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
- <span data-ttu-id="7adbc-111">Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää.</span><span class="sxs-lookup"><span data-stu-id="7adbc-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 

<span data-ttu-id="7adbc-112">Kun laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodaan yhteensopimattomia myyntilaskuja ja maksutietoja, ja koko laskelmien kirjausprosessi epäonnistuu tämän seurauksena.</span><span class="sxs-lookup"><span data-stu-id="7adbc-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="7adbc-113">Laskelmien palauttaminen sellaisesta tilasta vaatii monimutkaisia tietojen korjauksia moneen transaktiotauluun.</span><span class="sxs-lookup"><span data-stu-id="7adbc-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="7adbc-114">Tapahtumien yhdenmukaisuuden tarkistus estää tällaiset ongelmat.</span><span class="sxs-lookup"><span data-stu-id="7adbc-114">The transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="7adbc-115">Seuraavassa kaaviossa havainnollistetaan kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="7adbc-116">![Laskelman kirjausprosessi ja tapahtuman yhdenmukaisuuden tarkistus](./media/validchecker.png "Laskelman kirjausprosessi ja vähittäismyyntitapahtuman yhdenmukaisuuden tarkistus")</span><span class="sxs-lookup"><span data-stu-id="7adbc-116">![Statement posting process with transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="7adbc-117">**Vahvista myymälän tapahtumat** -eräprosessi tarkistaa seuraavien seikkojen yhdenmukaisuuden kaupan transaktiotauluista.</span><span class="sxs-lookup"><span data-stu-id="7adbc-117">The **Validate store transactions** batch process checks the consistency of the commerce transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="7adbc-118">**Asiakkaan tili** – Tarkistaa, että transaktiotauluissa oleva asiakastili on olemassa asiakkaan alkuperäisissä tiedoissa pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-118">**Customer account** – Validates that the customer account in the transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="7adbc-119">**Rivien määrä** – Tarkistaa, että rivien määrä transaktioiden otsikkotaulussa vastaa myynnin transaktiotauluissa olevien rivien määrää.</span><span class="sxs-lookup"><span data-stu-id="7adbc-119">**Line count** – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>
- <span data-ttu-id="7adbc-120">**Hinta sisältää veron** – Tarkistaa, että **Hinta sisältää veron** -parametri on yhdenmukainen kaikilla tapahtumariveillä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-120">**Price includes tax** – Validates that the **Price includes tax** parameter is consistent across transaction lines.</span></span>
- <span data-ttu-id="7adbc-121">**Maksun summa** -tarkistaa, että maksut vastaavat otsikon maksuja.</span><span class="sxs-lookup"><span data-stu-id="7adbc-121">**Payment amount** - Validates that the payment records match the payment amount on header.</span></span>
- <span data-ttu-id="7adbc-122">**Bruttosumma** – Tarkistaa, että otsikon bruttosumma on sama kuin rivien nettosummien ja veron määrä laskettuna yhteen.</span><span class="sxs-lookup"><span data-stu-id="7adbc-122">**Gross amount** – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</span></span>
- <span data-ttu-id="7adbc-123">**Nettosumma** – Tarkistaa, että otsikon nettosumma on sama kuin rivien nettosummien ja veron määrä laskettuna yhteen.</span><span class="sxs-lookup"><span data-stu-id="7adbc-123">**Net amount** – Validates that the net amount on the header is the sum of the net amounts on the lines.</span></span>
- <span data-ttu-id="7adbc-124">**Liika-/alimaksu** – Tarkistaa, että otsikon bruttosumman ja maksusumman välinen ero ei ylitä määritettyä ali- ja ylimaksun enimmäismäärää.</span><span class="sxs-lookup"><span data-stu-id="7adbc-124">**Under / Over payment** – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</span></span>
- <span data-ttu-id="7adbc-125">**Alennuksen summa** – Tarkistaa, että tapahtumien rivien taulukon alennuksen summan alennustaulukoiden alennuksen summa on yhdenmukainen ja että otsikon alennuksen summa on sama kuin rivien alennusten summien kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-125">**Discount amount** – Validates that the discount amount on the discount tables and the discount amount on the transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</span></span>
- <span data-ttu-id="7adbc-126">**Rivialennus** – Tarkistaa, että tapahtumarivin rivialennus on kaikkien tapahtumariviin liittyvien alennustaulukon rivien summa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-126">**Line discount** – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</span></span>
- <span data-ttu-id="7adbc-127">**Lahjakorttinimike** – Commerce ei tue lahjakorttinimikkeiden palautusta.</span><span class="sxs-lookup"><span data-stu-id="7adbc-127">**Gift card item** – Commerce doesn't support the return of gift card items.</span></span> <span data-ttu-id="7adbc-128">Lahjakortin saldo voidaan kuitenkin lunastaa. Kaikki lahjakorttinimikkeet, jotka on käsitelty palautusrivinä lunastusrivin sijaan, epäonnistuvat laskelman kirjausprosessissa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-128">However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</span></span> <span data-ttu-id="7adbc-129">Lahjakorttien tarkistusprosessin avulla voidaan varmistaa, että transaktiotaulujen kaikki palautuksen lahjakorttirivinimikkeet ovat lahjakortin lunastuksen rivejä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-129">The validation process for gift card items helps guarantee that the only return gift card line items on the transaction tables are gift card cash-out lines.</span></span>
- <span data-ttu-id="7adbc-130">**Negatiivinen hinta** – Tarkistaa, että negatiivisen hinnan tapahtumarivejä ei ole.</span><span class="sxs-lookup"><span data-stu-id="7adbc-130">**Negative price** – Validates that there are no negative price transaction lines.</span></span>
- <span data-ttu-id="7adbc-131">**Nimike ja variantti** – Tarkistaa, että tapahtumarivien nimikkeet ja variantit ovat nimikkeen ja variantin päätiedostossa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-131">**Item & Variant** – Validates that items and variants on the transaction lines exist in the item and variant master file.</span></span>
- <span data-ttu-id="7adbc-132">**Veron summa** – Tarkistaa, että verotietueen oikeellisuustarkistus vastaa rivien verosummia.</span><span class="sxs-lookup"><span data-stu-id="7adbc-132">**Tax amount** - Validates that tax records match the tax amounts on the lines.</span></span>
- <span data-ttu-id="7adbc-133">**Sarjanumero** – Tarkistaa, että sarjanumero on sarjanumeroseurannassa olevien nimikkeiden tapahtumariveillä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-133">**Serial number** - Validates that the serial number is present in the transaction lines for items that are controlled by serial number.</span></span>
- <span data-ttu-id="7adbc-134">**Allekirjoita** – Tarkistaa, että määrän ja nettosumman etumerkki on sama kaikilla tapahtumariveillä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-134">**Sign** - Validates that the sign on the quantity and the net amount are the same in all the transaction lines.</span></span>
- <span data-ttu-id="7adbc-135">**Liiketoiminnan päivämäärä** – Tarkistaa, että tapahtumien liiketoiminnan päivämäärien tilikaudet ovat avoimia.</span><span class="sxs-lookup"><span data-stu-id="7adbc-135">**Business date** - Validates that the financial periods for all the business dates for the transactions are open.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="7adbc-136">Yhdenmukaisuuden tarkistuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7adbc-136">Set up the consistency checker</span></span>

<span data-ttu-id="7adbc-137">Määritä Tarkista myymälän tapahtumat -eräprosessi tapahtumaan säännöllisesti kohdassa **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Myyntipistekirjaus**.</span><span class="sxs-lookup"><span data-stu-id="7adbc-137">Configure the "Validate store transactions" batch process, at **Retail and Commerce \> Retail and Commerce IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="7adbc-138">Eräprosessi voidaan aikatauluttaa myymälän organisaatiohierarkian perusteella samaan tapaan kuin "Laskelman laskeminen erässä"- ja "Laskelman kirjaaminen erässä" -prosessit on määritetty.</span><span class="sxs-lookup"><span data-stu-id="7adbc-138">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="7adbc-139">Suosittelemme määrittelemään tämän eräprosessin käynnistymään useita kertoja päivässä ja aikatauluttamaan sen siten, että se käynnistyy jokaisen P-tehtävän suorituskerran lopuksi.</span><span class="sxs-lookup"><span data-stu-id="7adbc-139">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="7adbc-140">Tarkistusprosessin tulokset</span><span class="sxs-lookup"><span data-stu-id="7adbc-140">Results of validation process</span></span>

<span data-ttu-id="7adbc-141">Eräprosessin suorittaman tarkistuksen tulokset yhdistetään asianmukaiseen tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="7adbc-141">The results of the validation check by the batch process are tagged on the appropriate transaction.</span></span> <span data-ttu-id="7adbc-142">**Vahvistuksen tila** -kenttä tapahtumatietueessa on joko **Onnistui** tai **Virhe**, ja edellisen tarkistusajon päivämäärä näkyy **Edellisen tarkistuksen aika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7adbc-142">The **Validation status** field on the transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="7adbc-143">Katso kuvaavampi tarkistuksen epäonnistumiseen liittyvä virheteksti valitsemalla asiaankuuluva transaktiotietue ja napauttamalla **Oikeellisuustarkistusvirheet**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="7adbc-143">To view more descriptive error text relating to a validation failure, select the relevant store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="7adbc-144">Tapahtumia, jotka eivät läpäise tarkistusta, ja tapahtumia, joita ei ole vielä tarkistettu, ei tuoda laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="7adbc-144">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="7adbc-145">”Laske laskelma” -prosessin aikana käyttäjille lähetetään ilmoitus, jos on tapahtumia, jotka olisi voitu sisällyttää laskelmaan mutta joita ei ole siihen sisällytetty.</span><span class="sxs-lookup"><span data-stu-id="7adbc-145">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="7adbc-146">Jos löydetään tarkistusvirhe, ainoa tapa sen korjaamiseksi on ottaa yhteyttä Microsoftin tukeen.</span><span class="sxs-lookup"><span data-stu-id="7adbc-146">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="7adbc-147">Tulevissa versioissa ohjelmaan lisätään toiminto, jonka avulla käyttäjät voivat korjata käyttöliittymän kautta ne tietueet, jotka aiheuttivat virheen.</span><span class="sxs-lookup"><span data-stu-id="7adbc-147">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="7adbc-148">Tapahtumaloki- ja auditointiominaisuudet tulevat myös saataville muutoshistorian seurantaa varten.</span><span class="sxs-lookup"><span data-stu-id="7adbc-148">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="7adbc-149">Tarkistussääntöjä useamman mahdollisen tilanteen kattamiseksi lisätään tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="7adbc-149">Additional validation rules to support more scenarios will be added in a future release.</span></span>