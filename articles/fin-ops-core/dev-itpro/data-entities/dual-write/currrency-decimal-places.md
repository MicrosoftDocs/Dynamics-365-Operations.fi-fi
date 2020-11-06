---
title: Valuutta-tietotyypin siirto kaksoiskirjoitusta varten
description: Tässä ohjeaiheessa käsitellään kaksoiskirjoituksen valuutan osalta tukemien desimaalien määrän muuttamista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 7e1f70d95f29dc154044f09c6020300a8e4f8987
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997475"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="b3970-103">Valuutta-tietotyypin siirto kaksoiskirjoitusta varten</span><span class="sxs-lookup"><span data-stu-id="b3970-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3970-104">Valuutta-arvoissa tuettujen desimaalien määrän voi kasvattaa enintään kymmeneen.</span><span class="sxs-lookup"><span data-stu-id="b3970-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="b3970-105">Oletusraja on neljä desimaalia.</span><span class="sxs-lookup"><span data-stu-id="b3970-105">The default limit is four decimal places.</span></span> <span data-ttu-id="b3970-106">Desimaalien määrää lisäämällä voi estää tietojen menettämisen, kun tietojen synkronointiin käytetään kaksoiskirjoitusta.</span><span class="sxs-lookup"><span data-stu-id="b3970-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="b3970-107">Desimaalien määrän lisääminen on muutos, joka on hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="b3970-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="b3970-108">Muutoksen tekemiseen tarvitaan Microsoftin apua.</span><span class="sxs-lookup"><span data-stu-id="b3970-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="b3970-109">Desimaalien määrään muuttamisessa on kaksi vaihetta:</span><span class="sxs-lookup"><span data-stu-id="b3970-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="b3970-110">Siirtoa pyydetään Microsoftilta.</span><span class="sxs-lookup"><span data-stu-id="b3970-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="b3970-111">Desimaalien määrää muutetaan Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="b3970-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="b3970-112">Finance and Operations -sovelluksen ja Common Data Servicen on tuettava samaa valuutta-arvojen desimaalimäärää.</span><span class="sxs-lookup"><span data-stu-id="b3970-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="b3970-113">Muussa tapauksessa tietoja menetetään, kun tietoja synkronoidaan sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="b3970-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="b3970-114">Vaikka siirtoprosessi määrittää uudelleen tavan, jolla valuutta- ja vaihtokurssiarvot tallennetaan, itse tiedot eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="b3970-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="b3970-115">Kun siirto on valmis, desimaalien määrää voi lisätä valuuttakoodeissa ja hinnoittelussa, minkä lisäksi käyttäjien antamien ja tarkastelemien tietojen desimaalitarkkuus voi parantua.</span><span class="sxs-lookup"><span data-stu-id="b3970-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="b3970-116">Siirto on valinnainen toiminto.</span><span class="sxs-lookup"><span data-stu-id="b3970-116">Migration is optional.</span></span> <span data-ttu-id="b3970-117">Jos desimaalien lisäämisestä saattaa olla hyötyä, siirtoa kannattaa harkita.</span><span class="sxs-lookup"><span data-stu-id="b3970-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="b3970-118">Organisaatioiden, jotka eivät tarvitse yli neljän desimaalin arvoja, ei tarvitse siirtyä.</span><span class="sxs-lookup"><span data-stu-id="b3970-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="b3970-119">Siirron pyytäminen Microsoftilta</span><span class="sxs-lookup"><span data-stu-id="b3970-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="b3970-120">Common Data Servicen nykyisten valuuttakenttien tallennustila hyväksyy enintään neljä desimaalia.</span><span class="sxs-lookup"><span data-stu-id="b3970-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="b3970-121">Tämän vuoksi valuutta-arvot kopioidaan siirtoprosessin aikana tietokannan uusiin, sisäisiin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="b3970-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="b3970-122">Tämä prosessi jatkuu siihen saakka, että kaikki tiedot on siirretty.</span><span class="sxs-lookup"><span data-stu-id="b3970-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="b3970-123">Vaikka siirron päätyttyä uudet tallennustilatyypit korvaavat sisäisesti vanhat tallennustilat, tietoarvot eivät ole muuttuneet.</span><span class="sxs-lookup"><span data-stu-id="b3970-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="b3970-124">Valuuttakentät voivat tämän jälkeen tukea enintään 10 desimaalia.</span><span class="sxs-lookup"><span data-stu-id="b3970-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="b3970-125">Common Data Servicen käyttöä voi jatkaa siirtoprosessin aikana ilman keskeytyksiä.</span><span class="sxs-lookup"><span data-stu-id="b3970-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="b3970-126">Valuuttakursseja muokataan samanaikaisesti siten, että ne tukevat enintään 12 desimaalia nykyisen 10 desimaalin rajan sijaan.</span><span class="sxs-lookup"><span data-stu-id="b3970-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="b3970-127">Tämä muutos on välttämätön, jotta desimaalien määrä on sama Finance and Operations -sovelluksessa ja Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="b3970-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="b3970-128">Siirto ei muuta tietoja millään tavalla.</span><span class="sxs-lookup"><span data-stu-id="b3970-128">Migration doesn't change any data.</span></span> <span data-ttu-id="b3970-129">Kun valuutta- ja vaihtokurssikentät on muunnettu, järjestelmänvalvojat voivat määrittää järjestelmän käyttämään valuuttakentissä 10 desimaalia. Se tehdään määrittämällä kunkin tapahtuman valuutan ja hinnoittelun desimaalien määrä.</span><span class="sxs-lookup"><span data-stu-id="b3970-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="b3970-130">Siirron pyytäminen</span><span class="sxs-lookup"><span data-stu-id="b3970-130">Request a migration</span></span>

<span data-ttu-id="b3970-131">Tämä toiminto saadaan käyttöön lähettämällä sähköpostia osoitteeseen **CDSExpandDecimal@microsoft.com** ja lisäämällä viestiin seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="b3970-131">To make this feature available, email **CDSExpandDecimal@microsoft.com** , and include the following information:</span></span>

+ <span data-ttu-id="b3970-132">**Aihe:** Pyyntö ottaa käyttöön laajennettu desimaalituki organisaatiossa \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="b3970-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="b3970-133">**Teksti:** Haluan ottaa käyttöön laajennetun desimaalituen organisaatiossa \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="b3970-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="b3970-134">Microsoftin edustaja ottaa yhteyttä kahden tai kolmen arkipäivän kuluessa, jonka jälkeen tehdään seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="b3970-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="b3970-135">Kun pyydät siirtoa, seuraavat tiedot on hyvä tiedostaa ja ne on otettava huomioon suunnittelussa:</span><span class="sxs-lookup"><span data-stu-id="b3970-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="b3970-136">Tietojen siirtämiseen tarvittava aika määräytyy järjestelmässä olevien tietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b3970-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="b3970-137">Suurten tietokantojen siirtäminen voi kestää useita päiviä.</span><span class="sxs-lookup"><span data-stu-id="b3970-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="b3970-138">Tietokannan koko suurenee tilapäisesti siirron aikana, koska indeksejä varten tarvitaan tilaa.</span><span class="sxs-lookup"><span data-stu-id="b3970-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="b3970-139">Suurin osa tästä tilasta vapautuu, kun siirto on valmis.</span><span class="sxs-lookup"><span data-stu-id="b3970-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="b3970-140">Jos siirtoprosessin aikana tapahtuu virhe, joka estää siirron valmistumisen, järjestelmää ilmoittaa siitä Microsoft-tuelle, jotta tukihenkilöstö voi ratkaista ongelma.</span><span class="sxs-lookup"><span data-stu-id="b3970-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="b3970-141">Common Data Service on kuitenkin koko käytettävissä tavalliseen tapaa, vaikka siirron aikana esiintyisi virheitä.</span><span class="sxs-lookup"><span data-stu-id="b3970-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="b3970-142">Siirtoprosessia ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="b3970-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="b3970-143">Desimaalien määrän muuttaminen</span><span class="sxs-lookup"><span data-stu-id="b3970-143">Changing the number of decimal places</span></span>

<span data-ttu-id="b3970-144">Kun siirto on valmis, Common Data Service voi tallentaa lukuja, joissa on enemmän desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="b3970-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="b3970-145">Järjestelmänvalvojat voivat valita, kuinka monta desimaalia tietyissä valuuttakoodeissa ja hinnoittelussa on.</span><span class="sxs-lookup"><span data-stu-id="b3970-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="b3970-146">Microsoft Power Appsin, Power BI:n ja Power Automaten käyttäjät voivat sitten tarkastella ja käyttää lukuja, joissa on enemmän desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="b3970-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="b3970-147">Tämän muutoksen tekeminen edellyttää, että seuraavat Power Appsin asetukset päivitetään:</span><span class="sxs-lookup"><span data-stu-id="b3970-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="b3970-148">**Järjestelmäasetukset: valuutan tarkkuus hinnoittelussa** – **Määritä desimaalien määrä, jota käytetään hinnoittelussa koko järjestelmässä** -kenttä määrittää, miten valuutta reagoi organisaatiossa, kun **Hinnoittelun tarkkuus** on valittu.</span><span class="sxs-lookup"><span data-stu-id="b3970-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="b3970-149">**Liiketoiminnan hallinta: valuutat** – **Valuutan tarkkuus** -kentässä voi määrittää mukautetun desimaalien määrän tietyn valtuutan osalta.</span><span class="sxs-lookup"><span data-stu-id="b3970-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="b3970-150">Varmistuksena on paluu koko organisaatiota koskevaan asetukseen.</span><span class="sxs-lookup"><span data-stu-id="b3970-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="b3970-151">Rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="b3970-151">There are some limitations:</span></span>

+ <span data-ttu-id="b3970-152">Valuuttakenttää ei voi määrittää entiteetissä.</span><span class="sxs-lookup"><span data-stu-id="b3970-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="b3970-153">Yli neljä desimaalia voidaan määrittää vain **Hinnoittelu** - ja **Tapahtumavaluutta** -tasoilla.</span><span class="sxs-lookup"><span data-stu-id="b3970-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="b3970-154">Järjestelmäasetukset: valuutan tarkkuus hinnoittelussa</span><span class="sxs-lookup"><span data-stu-id="b3970-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="b3970-155">Kun siirto on valmis, järjestelmänvalvojat voivat määrittää valuutan tarkkuuden.</span><span class="sxs-lookup"><span data-stu-id="b3970-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="b3970-156">Valitse ensin **Asetukset \> Hallinta** ja sitten **Järjestelmäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b3970-156">Go to **Settings \> Administration** , and select **System Settings**.</span></span> <span data-ttu-id="b3970-157">Muuta sitten **Yleiset** -välilehden arvo **Määritä desimaalien määrä, jota käytetään hinnoittelussa koko järjestelmässä** -kentässä, kuten seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="b3970-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Valuutan järjestelmäasetukset](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="b3970-159">Liiketoiminta-asiakirjat: valuutat</span><span class="sxs-lookup"><span data-stu-id="b3970-159">Business Management: Currencies</span></span>

<span data-ttu-id="b3970-160">Jos tietyn valuutan tarkkuuden on erottava hinnoittelussa käytetyn valuutan tarkkuudesta, sitä on muutettava.</span><span class="sxs-lookup"><span data-stu-id="b3970-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="b3970-161">Valitse ensin **Asetukset \> Liiketoiminnan hallinta** ja sitten **Valuutat** ja muutettava valuutta.</span><span class="sxs-lookup"><span data-stu-id="b3970-161">Go to **Settings \> Business Management** , select **Currencies** , and select the currency to change.</span></span> <span data-ttu-id="b3970-162">Määritä sitten **Valuutan tarkkuus** -kenttään sopiva desimaalien määrä, mistä on esimerkki seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="b3970-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Tietyn alueen valuutta-asetukset](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="b3970-164">Entiteetit: Valuutta-kenttä</span><span class="sxs-lookup"><span data-stu-id="b3970-164">Entities: Currency field</span></span>

<span data-ttu-id="b3970-165">Tiettyihin valuuttakenttiin määritettävien desimaalien määrä on rajoitettu neljään.</span><span class="sxs-lookup"><span data-stu-id="b3970-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>
