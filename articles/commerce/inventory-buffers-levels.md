---
title: Varastopuskureiden ja varastotasojen konfiguroiminen
description: Tässä ohjeaiheessa selitetään, miten määritetään varastopuskureita ja varastotasoja, jotka määrittävät varaston käytettävyysviestit Microsoft Dynamics 365 Commerce -sivustoissa.
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: cbc1f5f6fb2c35b009d65b03ffcaffc75a73f188
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417504"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Varastopuskureiden ja varastotasojen konfiguroiminen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa selitetään, miten määritetään varastopuskureita ja varastotasoja, jotka määrittävät varaston käytettävyyttä koskevat viestit Microsoft Dynamics 365 Commerce -sivustoissa.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce -pääkonttori sisältää varastotiedot ja erilaisia kanavia, kuten myyntipisteen (POS) sovellukset, sähköisen kaupankäynnin julkisivut ja muut mukautetut integroidut sovellukset, jotka vetävät ja työntävät varastoa ympäri asynkronisesti. Näin ollen käytettävissä olevat varastoarvot, jotka saadaan Commerce Headquarters -sovelluksen myyntipistekäyttöliittymän (POS) ja sähköisen kaupan varaston käytettävyyden API-liittymien kautta, eivät aina ole 100-prosenttisen oikeita reaaliaikaisesti.

Sen sijaan, että todettaisiin todelliset varastoarvot verkkokaupassa, monet vähittäismyyjät haluavat vain näyttää viestit varaston käytettävyystilasta (esimerkiksi "saatavilla" tai "ei varastossa") ilmoittaakseen asiakkaille, onko nimike ostettavissa tai mahdollisesti varastossa. Tässä lähestymistavassa varastopuskureita ja varastotasoja, jotka määräävät varaston käytettävyyssanoman, on oltava käytettävissä ja ne on konfiguroitava.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Edellytys: Ota käyttöön varastopuskurit ja varastotasot-ominaisuus

Varastopuskureiden ja varastotasojen ominaisuutta hallitaan toimintojen hallinnan avulla Commerce Headquarters -sovelluksessa. Ominaisuudet otetaan käyttöön seuraavasti.

1. Valitse **Järjestelmänvalvoja** \> **Työtilat** \> **Ominaisuuksien hallinta**.
1. Etsi **Ota käyttöön varastopuskurit ja varastotasot** -ominaisuus, valitse sen rivi ja valitse sitten **Ota käyttöön nyt**.

Kun ominaisuus on otettu käyttöön, voit etsiä varastotasoja kohteen **Retail and Commerce \> Varastonhallinta** avulla.

## <a name="create-and-configure-an-inventory-level-profile"></a>Varastotaso profiilin luominen ja konfiguroiminen

*Varastotason profiili* määrittää, otetaanko tietyn tuotemäärän tila huomioon varastossa, ei-varastossa tai jossakin muussa mukautetussa tilassa. Voit luoda ja konfiguroida useita varastotasoprofiileja kutakin yritystä kohden. Kukin profiili koostuu joukosta varastotasoja, ja kukin taso määräytyy *alueen*, *koodin* ja *otsikon* mukaan.

- **Alue** – Kukin alue määritetään *aloitusmäärän* ja *loppumäärän* mukaan. Määräarvo kuuluu alueeseen, jos se on suurempi kuin kyseisen alueen aloitusmäärä ja loppumäärä.
- **Koodi** – Koodi on sisäinen lyhenne, joka edustaa tasoa. Asiakkaat, jotka integroituvat suoraan varasto-API-liittymien kanssa, voivat luoda lisälogiikkaa tietylle varastotasolle koodien avulla. He voivat esimerkiksi poistaa tuotteen ostotoiminnon käytöstä, kun sen varastotason koodi on **OOS** ("loppunut varastosta").
- **Etiketti** – Etiketti on mielekäs asiakkaille näkyvä sanoma, joka välittää varastotason verkkokauppasivuston asiakkaille.

### <a name="create-an-inventory-level-profile"></a>Varastotasoprofiilin luominen

Luo varastotason profiili noudattamalla seuraavia ohjeita.

1. Siirry **Retail and Commerce** \> **Varaston hallinta** \> **Varastotasot**.
1. Valitse toimintoruudussa **Uusi** ja syötä sitten arvot **Profiilin tunnus**- ja **Kuvaus**-kenttiin.
1. Valitse **Alueet**-pikavälilehdessä **Lisää**, jos haluat lisätä uuden tason, ja kirjoita sitten arvot **Aloitusmäärä** -, **Loppumäärä**-, **Koodi**- ja **Etiketti**-sarakkeisiin kyseiselle tasolle. Toista tämä vaihe lisätäksesi tasoja. Voit tarvittaessa muokata tietoruudukon arvoja tai voit poistaa tason valitsemalla **Poista**.
1. Valitse toimintoruudussa **Tallenna**.

Kun uusi profiili luodaan, järjestelmä alustaa automaattisesti kaksi varastotasoa:

- **OOS** – Loppunut varastosta -taso, jossa alueen alaraja on negatiivinen ääretön. Aloitusmäärää ja -koodia ei voi muokata tälle tasolle.
- **SAATAVUUS** – Käytettävissä-taso, jossa ylempi sidottu alue on ääretön. Lopetusmäärää ja -koodia ei voi muokata tälle tasolle.

> [!NOTE]
> Profiilimäärityksen alueiden välillä ei voi olla aukkoja tai päällekkäisyyksiä.

Toimintoruudun **Käännökset**-painikkeen avulla voit määrittää etikettisanoman lokalisoidut merkkijonot. Tämän jälkeen sinun on suoritettava **1110** (**Yleinen konfiguraatio**)-jakelun ajoitustyö synkronoimalla lokalisoidut merkkijonot kanaviin.

### <a name="configure-an-inventory-level-profile"></a>Varastotasoprofiilin määrittäminen

Voit määrittää varastotason profiilin joko tuoteluokkatasolla tai yksittäisellä tuotetasolla. Kun tuotteelle on konfiguroitu varastotasoprofiili, varastotaso määräytyy linkitetyssä profiilissa määritettyjen alueiden mukaan. Muussa tapauksessa varastotaso "käytettävissä" tai "ei varastossa" määräytyy sen mukaan, onko tuotteella positiivinen määrä.

Määritä varastotason profiili luokalle noudattamalla seuraavia ohjeita.

1. Valitse **Retail ja Commerce** \> **Tuotteet ja luokat** \> **Commerce-tuotehierarkia**.
1. Valitse luokka, johon haluat määrittää varastotasotason profiilin.
1. Valitse **Myyntituotteen ominaisuudet** -pikavälilehdessä yritys.
1. Valitse **Commerce-varasto** -osan **Varastotason profiili** -kentästä jokin esimääritetyistä varastotasoprofiileista.

Toimintoruudun **Päivitä tuotteet** -painikkeen avulla voit levittää luokkatason profiilin arvon luokan pohjana oleville tuotteille. Lisätietoja on kohdassa [Tuoteluokkien ja tuotteiden hallinta](category-management-product-creation.md).

Määritä varastotason profiili vapautetulle tuotteelle noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail and Commerce** \> **Tuotteet ja luokat** \> **Vapautetut tuotteet luokittain**.
1. Valitse tuote ja avaa sitten sen tuotetiedot-sivu.
1. Valitse **Myy**-pikavälilehdellä **Commerce-varasto**-osan **Varastotason profiili** -kentästä jokin esimääritetyistä varastotasoprofiileista.

Kun uusi tuote luodaan, **Varastotason profiili** -kenttä, kuten monet muutkin tuotetason määritteet, asetetaan arvoon, joka on määritetty luokalle, johon tuote liittyy.

> [!NOTE]
> Varastotason profiili on yritys – tietty määrite. Jos kyseessä on sama luokka tai tuote, varastotason profiilin arvo voi vaihdella eri yritysten välillä.

Jos haluat synkronoida kanavien varastotasoprofiilien kokoonpanot, toimi seuraavasti.

1. Mene kohtaan **Retail ja Commerce** \> **Retail ja Commerce IT** \> **Jakeluaikataulu**.
1. Suorita **1040** (**Tuote**)-jakeluaikataulu.

## <a name="configure-an-inventory-buffer"></a>Varastopuskurin konfiguroiminen

*Varastopuskuri* on käyttäjän määrittämä arvo, joka vähentää nimikkeen alkuperäisen määrän lisämäärän laskeakseen arvioidun määrän. Tämä arvioitu määrä antaa vähittäismyyjille turvallisen puskurin niin, että ne eivät ylimyy tuotetta myymällä enemmän kuin sen todellinen käytettävissä oleva varasto. Voit määrittää varastopuskurin joko tuoteluokkatasolla tai yksittäisellä tuotetasolla. Jos varastopuskuria ei määritetä, käytössä on oletusarvo **0** (nolla).

Määritä varastopuskuri luokalle noudattamalla seuraavia ohjeita.

1. Valitse **Retail ja Commerce** \> **Tuotteet ja luokat** \> **Commerce-tuotehierarkia**.
1. Valitse luokka, jolle varastopuskuri määritetään.
1. Valitse **Myyntituotteen ominaisuudet** -pikavälilehdessä yritys.
1. Määritä positiivinen arvo **Commerce-varasto**-osan **Varastopuskuri**-kenttään.

Toimintoruudun **Päivitä tuotteet** -painikkeen avulla voit levittää luokkatason puskurin arvon luokan pohjana oleville tuotteille. Lisätietoja on kohdassa [Tuoteluokkien ja tuotteiden hallinta](category-management-product-creation.md).

Määritä varastopuskuri vapautetuille tuotteille noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail and Commerce** \> **Tuotteet ja luokat** \> **Vapautetut tuotteet luokittain**.
1. Valitse tuote ja avaa sitten sen tuotetiedot-sivu.
1. Määritä positiivinen arvo **Myy**-pikavälilehdellä **Commerce-varasto**-osan **Varastopuskuri**-kenttään.

Kun uusi tuote luodaan, **Varastopuskuri**-kenttä, kuten monet muutkin tuotetason määritteet, asetetaan arvoon, joka on määritetty luokalle, johon tuote liittyy.

> [!NOTE]
> Jos sekä varastopuskuri että varastotasoprofiilit on konfiguroitu tietylle tuotteelle, tuotteen arvioitua määrää (alkuperäistä määrää vähennettynä puskuriarvolla) käytetään aluelaskennassa varastotason määrittämiseen.

Jos haluat synkronoida kanavien varastopuskurien kokoonpanot, toimi seuraavasti.

1. Mene kohtaan **Retail ja Commerce** \> **Retail ja Commerce IT** \> **Jakeluaikataulu**.
1. Suorita **1040** (**Tuote**)-jakeluaikataulu.

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Varastopuskureiden ja varastotasojen käyttäminen sähköisen kaupankäynnin skenaariossa

Commerce-sivustotyökalu käyttää varastopuskuri- ja varastotason ominaisuuksia Commerce Headquarters -sovelluksessa ja määrittää varaston käytettävyysviestit verkkokauppasivustoissa. Lisätietoa kohdassa [Varastoasetusten käyttöönotto](inventory-settings.md).

Vaihtoehtoisesti, jos integroit kolmannen osapuolen verkkokaupparatkaisuun, voit käyttää **GetEstimatedAvailability**- ja **GetEstimatedProductWarehouseAvailability**-API-liittymiä, kun haluat näyttää tuotteen varaston saatavuuden sähköisen kaupankäynnin skenaariossa. Lisätietoja näistä API-rajapinnoista on kohdassa [Varaston käytettävyyden laskeminen vähittäismyyntikanaville](calculated-inventory-retail-channels.md).

Varastopuskureiden ja varastotasojen käyttöönotto mahdollistaa sen, että nämä API-liittymät palauttavat varastotasokoodit ja etikettiviestit, jotka määräytyvät kaikkien käytettävissä olevien ja käytettävissä olevien fyysisten arvojen mukaan. API-liittymiä voidaan määrittää edelleen sen selvittämiseksi, palautetaanko varastomäärä yhdessä sanoman kanssa ja vähennetäänkö käytettävissä oleva määrä varastopuskurin arvolla.

Voit määrittää tuotteen saatavuuden API-liittymissä noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail and commerce** \> **Pääkonttorin asetukset** \> **Parametrit** \> **Kaupan parametrit**.
1. Valitse arvo **Myymälän varasto** -osan **Varasto**-välilehden **Tuotesaatavuus-API-verkkokauppa**-kentässä.
1. Ota asetukset käyttöön kanavissa suorittamalla **1110** (**Yleinen konfigurointi**) -jakelun ajoitustehtävä.

## <a name="additional-resources"></a>Lisäresurssit

[Tuoteluokkien ja -tuotteiden hallinta](category-management-product-creation.md)

[Varastoasetusten käyttäminen](inventory-settings.md)

[Vähittäismyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md)
