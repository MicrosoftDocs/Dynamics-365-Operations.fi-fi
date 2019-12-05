---
title: Tehtävien lisääminen työhönottoprosessiin
description: Tässä ohjeaiheessa on tietoja erityyppisistä tehtävistä, joita voidaan lisätä Microsoft Dynamics 365 Talent – Attractin työhönottoprosessiin.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
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
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833274"
---
# <a name="add-activities-to-a-hiring-process"></a>Tehtävien lisääminen työhönottoprosessiin

[!include [banner](includes/banner.md)]

Tehtävät voidaan lisätä työhönottoprosessin osaksi Microsoft Dynamics 365 Talent: Attractissa. Tehtävät voidaan lisätä prosessimalliin, tai ne voidaan lisätä suoraan työn työhönottoprosessiin. Työn määrittämisen jälkeen valitaan prosessimalli, jonka jälkeen malliin sisältyvät tehtävät liitetään työhön. Jos mallia ei ole valittu, käytetään oletusmallia. Työhönottoprosessia voidaan muokata työn osalta myös mallin liittämisen jälkeen.

> [!NOTE] 
> Prosessimallit sisältyvät kattavaan työhönottolaajennukseen. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Potentiaalinen ehdokas -tehtävä

Potentiaalinen ehdokas -tehtävä määrittää, voidaanko potentiaaliset ehdokkaat lisätä työhön. Potentiaaliset ehdokkaat voidaan oletusarvoisesti lisätä työhön. Voit poistaa Potentiaalinen ehdokas -tehtävän käytöstä valitsemalla **Ota potentiaaliset ehdokkaat käyttöön** -asetukseksi **Ei käytössä**. Kun Potentiaalinen ehdokas -tehtävä on otettu käyttöön, rekrytointipäälliköt voivat lisätä ja tarkastella potentiaalisia ehdokkaita työn kohdalla näkyvässä **Potentiaalinen ehdokas** -välilehdessä.

> [!NOTE]
> Voit sallia ehdokkaiden lisäämisen työhön LinkedInistä määrittämällä **Ota potentiaaliset ehdokkaat käyttöön** -asetukseksi **Käytössä**.

## <a name="application-activity"></a>Hakemus-tehtävä

Työhönottoprosessimallissa on oltava Hakemus-tehtävä. Jos haluat lähettää sähköpostia ehdokkaille, kun lähettävät hakemuksen tai kun heidät lisätään Hakemus-vaiheeseen, valitse **Lähetä viesti ehdokkaalle** -asetukseksi **Käytössä**.

## <a name="interview-schedule-and-feedback-activity"></a>Haastattelujen aikataulu- ja palautetehtävä

Tässä tehtävässä on kolme osaa: Ehdokkaan käytettävyystietojen pyytäminen, Aikataulu ja Palaute. Käytä työmallin haastattelutehtävää, jos haluat sisällyttää ehdokkaan käytettävyystietojen pyytämisen, aikataulun ja palautteen prosessin osaksi sen sijaan, että käyttäisit niitä työhönottoprosessin erillisinä osina. Lisätietoja on kohdassa [Haastattelujen aikataulutus ja palaute](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps-tehtävä

Power Apps-tehtävän avulla Microsoft Power Apps -sovelluksen voi upottaa työhönottoprosessiin. Sovellus voi olla pakollinen kaikille hakijoille, vain sisäisille hakijoille, vain ulkoisille hakijoille tai ei millekään hakijoille. Jos sovellus on merkitty pakolliseksi, sen on oltava valmis, ennen kuin vaiheessa voi edetä. Jotta se voidaan laskea valmiiksi, **JobApplicationStatus**-kentän arvoksi on määritettävä **Valmis**. Kenttä sijaitsee JobApplicationActivity-yksikössä, joten Power Apps-sovelluksen on päivitettävä se ennen kuin vaiheessa voidaan edetä. Jos sovellusta ei ole merkitty pakolliseksi, tehtävä on valinnainen vaihe ja vaiheessa voidaan siirtyä, vaikka sovellus ei olisi valmis.

Jos haluat tallentaa Power Apps-tehtävän työhönottoprosessiin, sinun on annetta Power Apps-tunnus. Voit etsiä Power Apps-tunnuksen valitsemalla ensin [Power Apps](https://web.powerapps.com), sitten **Sovellukset** ja lopuksi **Tiedot**.

Oletusarvoisesti Power Apps-tehtävä on rekrytointipäällikön, työhönottajan ja heidän edustajiensa käytettävissä. Jos valitset asetuksen, joka **sallii osallistujien lisäämisen tehtävään**, Power Apps-tehtävää käyttävään sovellukseen voidaan lisätä osallistujia työhönottotiimistä. Esimerkki: Organisaatio on luonut Power Apps-sovelluksen, joka on teknisten tehtävien haastattelukysymyksistä koostuva kirjasto. Organisaatio on nyt palkkaamassa uutta ohjelmistokehittäjää ja on lisännyt Power Apps-tehtävän ohjelmistokehittäjäroolin työhönottoprosessiin. Jos asetus, joka **sallii osallistujien lisäämisen tehtävään**, on valittu, hakijaa ohjelmistokehittäjän rooliin harkitseva rekrytoija tai rekrytointipäällikkö voi lisätä haastattelijoita Power Apps-tehtävään. Kyseiset henkilöt voivat sitten tarkastella haastattelukysymykset sisältävää sovellusta.

> [!NOTE]
> Power Apps-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube-tehtävä

Voit jakaa YouTube-tehtävässä YouTube-videon työhönottoprosessin osana. Jos haluat tallentaa YouTube-tehtävän työhönottoprosessiin, sinun on määritettävä YouTube-videon URL-osoite. Voit valita näytätkö sisältöä **työhönottotiimille**, **sisäisille hakijoille**, **ulkoisille hakijoille** vai **kaikille hakijoille**. Voit sallia työhönottotiimin osallistujien lisäämisen tehtävään samoin kuin Power Apps-tehtävässä. Jos päätät näyttää sisällön hakijoille, video näytetään vain osana hakijakokemusta eikä palkkaamisprosessissa.

> [!NOTE]
> YouTube-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Internet-sisältö-tehtävä

Internet-sisältö-tehtävässä voit upottaa verkkosisältöä työhönottoprosessiin. Jos haluat tallentaa Internet-sisältö-tehtävän työhönottoprosessiin, sinun on määritettävä sisällön URL-osoite. Voit valita näytätkö sisältöä **työhönottotiimille**, **sisäisille hakijoille**, **ulkoisille hakijoille** vai **kaikille hakijoille**. Voit sallia työhönottotiimin osallistujien lisäämisen tehtävään samoin kuin Power Apps- ja YouTube-tehtävissä. Jos päätät näyttää sisällön hakijoille, verkkosisältö näytetään vain osana hakijakokemusta eikä palkkaamisprosessissa. Voit valita näytettävän sisällön koon.

> [!NOTE]
> Internet-sisältö-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Microsoft Forms -tehtävä

Microsoft Forms -tehtävän avulla voi upottaa Microsoft Forms -tehtävän työhönottoprosessiin. Voit luoda Microsoft Formsin avulla tietovisoja ja erilaisia kyselyjä. Jos haluat tallentaa Microsoft Forms -tehtävän työhönottoprosessiin, sinun on määritettävä lomakkeen URL-osoite. Voit valita näytätkö sisältöä **työhönottotiimille**, **sisäisille hakijoille**, **ulkoisille hakijoille** vai **kaikille hakijoille**. Voit sallia työhönottotiimin osallistujien lisäämisen tehtävään samoin kuin Power Apps-, YouTube- ja verkkosisältötehtävissä. Jos päätät näyttää sisällön hakijoille, lomake näytetään vain osana hakijakokemusta eikä palkkaamisprosessissa.

Tekijät voivat muuttaa Microsoft Formsissa asetuksia siten, että organisaation ulkopuoliset käyttäjät voivat vastata kyselyyn tai tietovisaan. Siinä tapauksessa käyttäjät lähettävät vastaukset anonyymisti. Jos haluat nähdä, kuka on vastannut kyselyyn tai tietovisaan, voit edellyttää, että vastaajat ilmoittavat nimensä kyselyn tai tietovisan osana.

> [!NOTE]
> Microsoft Forms -tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Tarjoustehtävät

Työntekijän palkkausprosessimalli edellyttää tarjoustehtävää. Integroidun tarjoushallintasovelluksen käyttämiseksi aseta **käynnistä tarjoushallintasovellus tarjouksen laadinnassa** arvoksi **Päällä**. Jos tämä asetus on pois päältä, ehdokas ei näy tarjoussovelluksessa, joten sinun on seurattava ehdokkaan tarjoustoimintojen päivityksiä manuaalisesti. Voit määrittää, voivatko esimiehet valmistella hakijalle tarjouksen tarjoussovelluksessa määrittämällä **Rekrytointipäälliköt voivat valmistella tarjouksen** arvoksi **Päällä**. Jos työhön on liitetty useita toimia, voit päättää, haluatko valmistella useita tarjouksia samalla sijaintinumerolla. Jos haluat sallia vain yhden tarjouksen toimea ja työtä kohti, määritä **Salli toimien käyttö tietyn työn sisällä uudelleen** arvoksi **pois käytöstä**.

> [!NOTE]
> Integroitua tarjoushallintasovellusta voi käyttää vain kattavan työhönottolaajennuksen kanssa. Lisätietoja on kohdassa [Mikä Microsoft Dynamics 365 Talent – Attractin versio?](./attract-comprehensive-hiring.md).


