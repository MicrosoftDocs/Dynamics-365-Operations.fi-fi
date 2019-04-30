---
title: Project Timesheet -mobiilisovellus
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksesta. Project Timesheet -mobiilisovelluksen avulla käyttäjät lähettävät ja hyväksyvät projektien aikaraportteja mobiililaitteellaan.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "969649"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Microsoft Dynamics 365 Project Timesheet -mobiilisovellus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen avulla käyttäjät lähettävät ja hyväksyvät projektien aikaraportteja mobiililaitteellaan (iPhone tai Android). Tämä mobiilisovellus näyttää Microsoft Dynamics 365 for Finance and Operationsin projektinhallinnan ja kirjanpidon alueen aikaraporttitoiminnot parantaen käyttäjien tuottavuutta ja tehokkuutta sekä mahdollistamalla projektin aikaraporttien nopean syöttämisen ja hyväksynnän.

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Lataa ja asenna Microsoft Dynamics 365 Project Timesheet -mobiilisovellus Androidille tai iPhonelle laitteesi sovelluskaupasta.

## <a name="enable-the-app"></a>Sovelluksen käyttöönotto 

Dynamics 365 for Finance and Operationsissa Project Timesheet -mobiilisovellus on otettava käyttöön. Voit ottaa toiminnon käyttöön siirtymällä kohtaan **Projektinhallinnan ja kirjanpidon parametrit \> Aikaraportti** ja valitsemalla **Ota Microsoft Dynamics 365 Project Timesheet käyttöön** -parametrin.

## <a name="sign-in-to-the-app"></a>Kirjautuminen sovellukseen

1.  Käynnistä sovellus mobiililaitteessa.

2.  Syötä Microsoft Dynamics 365 for Finance and Operationsin URL-osoite.

3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.

4.  Kirjaudut oletusarvoiseen yritykseesi.

## <a name="submit-a-project-timesheet"></a>Lähetä projektin aikaraportti

Voit luoda ja lähettää projektin aikaraportin sovelluksessa. Voit luoda uuden aikaraportin aiemman aikaraportin tietojen, tallennettujen rivien tai projektin liitosten perusteella. Jos sinut on nimetty edustajaksi, voit kirjoittaa aikaraportin myös toiselle työntekijälle. Voi luoda aikaraportin edustajana valitsemalla **Valikko**-painikkeen ja sitten valitse resurssinimi.

Aikaraporttisivu luo uuden aikaraportin aikaraporttiajanjaksolle nykyisen päivämäärän perusteella. Työviikko tulee näkyviin. Jos aikaraportin jaksot kattavat useita viikkoja, voit valita työviikkojen välilehdistä toisen työviikon.
Jos olemassa aikaraportti nykyiselle päivämäärälle, se näkyy. Jos haluat luoda uuden aikaraportin eri aikaraporttiajanjaksolle, valitse **Valikko**-painike ja sitten **Uusi aikaraportti**.

Voit syöttää projektitiedot valitsemalla **Lisää aika** -toimenpiteen tai **Kopioi aika kohteesta** -toimenpiteen. **Kopioi aika kohteesta** -toiminto kopioi projektirivin tietoja, mutta ei tunteja. **Kopioi aika kohteesta** -valikko sisältää seuraavat vaihtoehdot:

- **Kopioi aiemmin määritetystä aikaraportista** – Kopioi aikaraportin rivit aiemmin määritetystä aikaraportista.

- **Kopioi suosikista** – luo uudet aikaraportin rivit käyttämällä aikaraportin asetuksia, jotka valitsit suosikkeina.

- **Kopioi määrityksestä** – Luo uudet aikaraportin rivit määritetyistä projekteista.

Näytettävät projektitiedot riippuvat mobiiliparametreista, jotka määritit **Projektinhallinnan ja kirjanpidon parametrit** -sivulla.

Valitse **Yritys** -kentässä oikeushenkilö, jolle suoritit projektityön. **Yritys**-kenttä on käytettävissä vain, jos konsernin sisäinen aikaraportin tuki on otettu käyttöön yrityksessä.

Valitse asiakas, joka on liitetty aikaraportin projektin. Androidin alkuperäisessä versiossa, tietojen syöttöä asiakkaan mukaan ei tueta, koska projekti on valittava ensin. Jos valitsit ensin projektin **Asiakas**-kenttä täytetään automaattisesti.

Valitse **Projekti**-kentässä projekti, jolle olet kirjoittamassa aikaa. **Asiakas**-kenttä täytetään automaattisesti.

Asiakas- ja projektihakujen avulla voit etsiä sekä asiakkaista että projekteista.

Valitse tiedot **Luokka**-, **Tehtävä**-, **Rivin ominaisuus**-, **Arvonlisäveroryhmä** ja **Nimikkeen arvonlisäveroryhmä** -kenttiin tarpeen mukaan. Nämä kentät voidaan ohittaa.

**Rivin ominaisuus** -kentän arvoksi määritetään oletusarvo projektinhallinnan ja kirjanpidon parametrien mukaan. Kun projekti/luokka- ja luokka/resurssi -parametrit on otettu käyttöön **Rivin ominaisuus** -arvoksi määritetään oletusarvo, joka on määritetty tälle oikeellisuustarkistukselle. Kun projekti/luokka- ja luokka/resurssi -parametreja ei ole otettu käyttöön **Rivin ominaisuus** -kenttään tulee oletusarvo, joka on määritetty **Ota käyttöön oletusrivin ominaisuus** -kentässä **Projektinhallinnan ja kirjanpidon parametrit** -sivulla. **Rivin ominaisuus** -arvo voidaan ohittaa.

Valitse lisättävä päivä. Kirjoita tuntimäärä, jonka työskentelit päivittäin.

Voit lisätä huomautuksia syöttämiisi tunteihin valitsemalla **Lisää kommentteja** ja kirjoittamalla kommentit sisäiselle käyttäjäryhmälle, asiakkaan käyttäjäryhmälle tai molemmille.
Projektipäälliköt voivat tarkastella sisäisiä kommentteja. Asiakaskommentit sisällytetään laskuihin.

Voit tallentaa rivin suosikkina valitsemalla valintaruudun ja valitsemalla sitten **Tallenna suosikkina**.

Taloushallinnon dimension ja liitetiedostojen tukea ei ole mobiilisovelluksessa.

Jatka tarvittaessa projektin rivien lisäämistä aikaraportin täydentämiseksi.

Voit lähettää aikaraportin hyväksyntätyönkulkuun napsauttamalla **Lähetä**.

## <a name="review-timesheets"></a>Tarkista aikaraportit

Tarkistettavat aikaraportit näkyvät luettelona valikossa. Tämä vaihtoehto on käytettävissä vain, jos sinut on määritetty työnkulun hyväksyjäksi. Sekä otsikon että rivien hyväksymistä tuetaan. Rivitason hyväksyminen mahdollistaa yhden tai useamman rivin merkitsemisen hyväksyttäväksi. Kun aikaraportin tiedot on tarkistettu, jatka työnkulkua valitsemalla **Hyväksy**, **Delegoi** tai **Palauta**.
