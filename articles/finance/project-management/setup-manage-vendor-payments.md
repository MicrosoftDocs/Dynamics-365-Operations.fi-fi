---
title: Maksettaessa maksettavien toimittajan maksujen määrittäminen ja käyttäminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan maksa, kun maksettu (PWP)-ehtoja, jotta voit vapauttaa osittaiset toimittajamaksut asiakasmaksujen perusteella.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284110"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Maksettaessa maksettavien toimittajan maksujen määrittäminen ja käyttäminen

[!include [banner](../includes/banner.md)]

Kun hyväksyt toimittajan työskentelemään alihankkijaksi, haluat ehkä pidättää toimittajan maksun, kunnes asiakas on maksanut sinulle projektista. Tämän skenaarion tukemiseksi voit pidättää maksun toimittajalle määrittämällä toimittajan ostotilaukseen (PO) Maksa, kun maksettu -ehdon.

Voit esimerkiksi vapauttaa joitakin tai kaikki toimittajan laskut maksettaviksi, kun asiakas maksaa projektilaskun summan. Määritä Maksu, kun maksettu -ehdot määrittämään, että toimittajalle maksetaan sen jälkeen, kun vastaanotat asiakkaalta tietyn prosenttiosuuden liittyvästä maksusta. Jos vastaanotat asiakkaalta osamaksun, voit vapauttaa manuaalisesti maksun osan liittyvistä toimittajan laskuista.

Seuraavassa esimerkissä kuvataan prosessi, jossa PWP-termejä käytetään.

## <a name="example"></a>Esimerkki

Organisaatiosi sitoutuu tarjoamaan asiakkaalle 100 tietokonetta, joissa on asennettuna ohjelmisto, jonka hinta on 150,00 Yhdysvaltain dollaria (USD) tietokonetta kohden. Tämän jälkeen voit palkata toimittajan tarjoamaan tietokoneita, joihin on asennettu ohjelmisto. Sopimuksen mukaan asiakkaan on hyväksyttävä tietokoneiden laatu, ennen kuin se maksaa organisaatiollesi. Organisaatiosi käytäntö on evätä toimittajalle maksu, kunnes asiakas on maksanut sinulle. Tämän vuoksi voit määrittää projektin niin, että sen PWP-prosenttiosuus on 100 prosenttia.

Toimittaja lähettää 100 tietokonetta, joihin on asennettu ohjelmisto, sekä 10 000,00 USD:n laskun. Koska PWP-ehdot on määritetty projektiasi varten, et maksa toimittajalle tietokoneiden vastaanottamisen jälkeen. Sen sijaan lähetät tietokoneet asiakkaalle sekä laskun, jonka summa on 15 000,00. Asiakas tarkastaa tietokoneet ja hyväksyy projektilaskun täyden määrän.

Kun koko maksu on vastaanotettu asiakkaalta, maksat toimittajalle, 10 000,00, koko toimittajan laskun summan.

## <a name="set-up-pwp-terms-for-a-project"></a>Määritä projektin PWP-ehdot

Kun määrität projektin PWP-ehdot, sinun on määritettävä prosenttiosuutena vähimmäissumma, joka asiakkaan on maksettava projektista, ennen kuin maksat toimittajalle. Summan raja-arvo lasketaan automaattisesti projektin myyntilaskuihin. Seuraa näitä ohjeita määrittääksesi kynnysprosentin PWP-ehdoille.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Etsi ja avaa projekti, jolle haluat määrittää PWP-ehdot.
3. Valitse **Toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.
3. Valitse **Tilikoodi** -kentästä jokin seuraavista vaihtoehdoista:

    - **Taulu** – PWP-ehtoja sovelletaan yksittäiseen toimittajaan.
    - **Ryhmä** – PWP-ehtoja sovelletaan kaikkiin toimittajaryhmän toimittajiin.
    - **Kaikki** – PWP-ehtoja sovelletaan kaikkiin toimittajiin.

4. Jos valitsit edellisessä vaiheessa **Taulu** tai **Ryhmä**, valitse **toimittaja/toimittajaryhmä**-kentästä toimittaja tai toimittajaryhmä, joita PWP-ehdot koskevat. Jos valitsit edellisessä vaiheessa **Kaikki**, **Toimittaja/toimittajaryhmä**-kenttää ei voi muokata.
5. Jos toimittajan pidätysehdot on määritetty myyjälle projektissa **Toimittajan pidätysehdot** -kentässä, valitse säännön tunnus pidätysehdoille.
6. Syötä **PWP-kynnysprosentti**-kentässä projektin kynnysprosenttiarvo. Syöttämäsi prosentti määrittää projektin vähimmäissumman, joka asiakkaan on maksettava sinulle, ennen kuin maksat toimittajalle.

## <a name="create-a-po-that-has-pwp-terms"></a>Luo ostotilaus, jossa on PWP-termejä

Kun kirjaat toimittajan laskun ja toimittajaan pätevät PWP-ehdot, PWP-ehdot näkyvät PO:n riveillä. Jos haluat luoda ostotilauksen, jossa on PWP-ehtoja, toimi seuraavasti.

1. Siirry kohtaan **Hankinta ja alihankinta** \> **Ostotilaukset** \> **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**. Kirjoita sitten **Luo ostotilaus** -valintaikkunaan tarvittavat tiedot ja valitse **OK**.

    Vaihtoehtoisesti voit avata olemassa olevan ostotilauksen **Kaikki ostotilaukset** -luettelosivulla.

4. Tarkasta **Ostotilaus**-lomakkeen **Ostotilausrivit**-pikavälilehdessä toimittajan PO:n tiedot. **Maksu, kun maksettu** -vaihtoehto valitaan automaattisesti, ja **PWP-kynnysprosentti**-kentän arvo kopioidaan automaattisesti **PWP-kynnysprosentti** -kentästä **Projektit**-sivulta.
6. Jos et halua käyttää PWP-ehtoja ostotilausrivin toimittajalle, poista **Maksu, kun maksettu** -vaihtoehto. Tässä tapauksessa ostotilausrivin **PWP-kynnysprosentti** -kentän arvoksi palautetaan 0 (nolla).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Päivitä asiakkaan maksut ja maksa toimittajalle

Kun toimittajan työ tässä projektissa on valmis, ja hän lähettää laskun, tarkasta projektin tila ja asiakkaan laskut määrittääksesi, ovatko projektin PWP-ehdot täyttyneet. Jos toimittajan PWP-ehdot on täytetty, voit määrittää mitkä rivit toimittajan laskusta maksetaan projektin asiakasmaksujen perusteella. Jos päätät maksaa toimittajalle, vaikka PWP-ehtoja ei olisi täytetty, voit ohittaa PWP-ehdot **Toimittajalasku maksa, kun maksettu -ehto** -sivulla.

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kyselyt ja raportit** \> **Pidätyskysely** \> **Toimittajalasku maksa, kun maksettu -ehto**.
2. Syötä tarkastettavien toimittajien laskujen haku-kenttään arvot, joissa on **Toimittajalasku maksa, kun maksettu -ehto** -sivu, ja valitse sitten **Hae**.
3. Valitse muutettavien rivien **Toimittajalaskun rivit** -pikavälilehdessä.
4. Jos laskurivin **Maksu, kun maksettu** -ehdot täyttyvät, valitse **Vapauta toimittajan maksu**. **Maksu, kun maksettu** -vaihtoehto tyhjennetään, ja **Valmis maksettavaksi** -kentän arvoksi vaihdetaan **Kyllä**.
