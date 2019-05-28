---
title: Hakijan profiilien ja sovellusten lähteiden seuraaminen
description: Tässä ohjeaiheessa kerrotaan hakijaprofiilien ja -sovellusten lähteiden seurannasta.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517928"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Hakijan profiilien ja sovellusten lähteiden seuraaminen 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Tässä ohjeaiheessa mainitut toiminnot ovat saatavilla ennakkoversion osana. Sisältö ja toiminnot voivat muuttua. Voit käyttää tätä toimintoa pyytämällä järjestelmänvalvojaa ottamaan sen käyttöön Attractin **järjestelmänvalvojan asetuksissa**. Tuleva julkaisu tarjoaa lähdeseurantaraportteja. Lisätietoja on kohdassa [Talentin esiversiotoimintojen käyttö](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

Kun hakijat hakevat työtä, Attract seuraa automaattisesti sovellustensa lähdettä ja antaa sinulle arvokasta tietoa, jonka avulla voit kohdistaa rekrytointityösi. Rekrytoijat ja rekrytointipäälliköt voivat myös valita sovelluslähteen samalla, kun lisäät hakijan manuaalisesti työ- tai lahjakkuusalueelle.

Voit tarkastella sovelluksen lähdettä sovelluksen toiminnan yksityiskohdissa **Tehtävä**-välilehdellä samoin kuin sovellushistoria kohdassa **Profiili** kykypooleissa. Löydät hakijan profiililähteen hakijan tiedoista kohdasta **Profiili** sekä sovellusten ja kykypoolien välilehdeltä.

> [!NOTE] 
> Prosessimallit löytyvät kohdasta [Kattava työhönottolaajennus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Ennalta määritetyt lähteet

Oletuslähteiden luettelo sisältää yleisiä sovelluslähteitä. Joillakin lähdetyypeillä, kuten **Työtaulu** ja **Sosiaalinen verkko**, on ylimääräisiä lähdetietoja. Esimerkiksi **Sosiaalinen verkko** sisältää Facebookin ja Twitterin. **Viittauksen** lähdetyypin avulla voit määrittää sisäisen työntekijän viittaajaksi. Oletuslähteiden luettelo sisältää seuraavat ennalta määritetyt lähteet:

-   Attract-urasivusto

-   Virasto

-   Uramessut

-   Yrityksen markkinointi

-   Konferenssit ja messut

-   Asiantuntijayhteisö

-   Työtaulu

    -   Itse asiassa

    -   Haku

    -   CareerBuilder

    -   Google työt

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Aikakauslehdet ja julkaisut

-   Sosiaalinen verkko

    -   Facebook

    -   Twitter

-   Yliopiston rekrytointi

-   LinkedIn

-   Luokittelemattomat

-   Viite

-   Rekrytoijan lisäämä

-   Muu

## <a name="customize-the-source-list"></a>Lähdeluettelon mukauttaminen 

Voit laajentaa lähdeluetteloa lisäämällä muita sovelluslähteitä. Voit mukauttaa tätä luetteloa noudattamalla ohjeita kohdassa [Vaihtoehtoasetusten määrittäminen Attractissa](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Muokkaa **TalentSource**-yksikköä sisällyttääksesi muita lähteitä. 

Voit välttää käyttöliittymän (UI) negatiivista vaikutusta muokkaamalla tai poistamalla **TalentCategory** valintalistojen arvoja (ei nimiä) seuraaviin tarkoituksiin:

- **Viite**
- **LinkedIn**
- **Muu**

Voit laajentaa sen sijaan **TalentSource**-valintalistaa lisätäksesi muita lähdetyyppejä.
