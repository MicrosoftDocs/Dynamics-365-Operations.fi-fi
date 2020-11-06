---
title: Toimittajan laskuautomaation määritysasetukset (esiversio)
description: Tässä ohjeaiheessa käsitellään asetuksia, joilla toimittajan laskuautomaatio voidaan asentaa ja määrittää.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: articl
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c3ee1112a409f87fdb433d5d43442a858dbd1798
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022587"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Toimittajan laskutusautomaation asetusvaihtoehdot

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään asetuksia, joilla toimittajan laskuautomaatio voidaan asentaa ja määrittää. Laskuautomaatio-ominaisuus käyttää seuraavia määritysparametrityyppejä:

- Parametrit, joilla lähetetään tuodut toimittajan laskut työnkulkujärjestelmään ja täsmäytetään kirjatut tuotteen vastaanottorivit odottaviin toimittajan laskurivit.
- Prosessin automatisoinnin taustatehtävien parametrit. Prosessin automatisointikehyksellä lähetetään tuodut toimittajan laskut työnkulkujärjestelmään. Sen avulla täsmäytetään myös automaattisesti kirjatut tuotteen vastaanottorivit odottaviin toimittajan laskuriveihin. Eri liiketoimintaprosessit käyttävät tätä kehystä määrittämään, kuinka usein valittu prosessi suoritetaan. **Täsmäytä tuotteen vastaanotto laskuriveihin** - ja **Lähetä toimittajan laskut työnkulkuun** -taustaprosesseissa on valittavana toistuvuusasetukseksi **Tunti** ja **Päivittäin**.

Voit määrittää taustatehtävän tai määrittää sen tiedot valitsemalla **Järjestelmänvalvonta \> Asetukset \> Prosessin automatisoinnit** ja valitsemalla sitten **Taustatehtävä** -välilehden.

Toimittajan laskutyönkulun määrittäminen on välttämätöntä, jotta automaatio tuontiprosessista toimittajan laskun kirjaamiseen tapahtuu ilman käyttäjän toimintoja. Määritä työnkulku valitsemalla **Ostoreskontra > Asetukset > Ostoreskontran työnkulut**. Laskun käsitteleminen alusta loppuun ilman manuaalisia toimia edellyttää, että automaattinen kirjaustehtävä sisältyy työnkulun määritykseen. .

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametrit tuotujen toimittajan laskujen lähettämiseen työnkulkujärjestelmään

Tuodut toimittajan laskut lähetetään työnkulkujärjestelmään tietyillä parametreilla. Lisäksi joillakin parametreilla täsmäytetään kirjatut tuotteen vastaanottorivit odottaviin toimittajan laskuriveihin. **Ostoreskontran parametrit** -sivun **Toimittajan laskuautomaatio** -välilehdessä määritettävät parametrit on jaettu seuraaviin osiin:

- Toimittajan laskutyönkulku
- Täsmäytä tuotteen vastaanotot automaattisesti

Seuraavat parametrit ovat käytettävissä:

- **Tuotujen laskujen lähettäminen automaattisesti työnkulkuun** – Jos tämän vaihtoehdon asetuksena on **Kyllä** , tuodut laskut lähetetään automaattisesti työnkulkujärjestelmään. Jos asetuksena on **Ei** , laskut on lähetettävä manuaalisesti. Jos asetukseksi valitaan **Kyllä** , otat käyttöön prosessin, jossa käyttäjän toimia ei tarvita missään vaiheessa tulosten tuonnista kirjaamiseen.

    Tämä **Kyllä** -asetus voidaan määrittää vain, jos yrityksessä on määritetty aktiivinen toimittajan laskutyönkulku. Määritä työnkulku valitsemalla **Ostoreskontra \> Asetukset \> Ostoreskontran työnkulku**.

- **Täsmäytä tuotteen vastaanotot laskuriveihin ennen automaattista lähettämistä** – Jos tämän vaihtoehdon asetuksena on **Kyllä** , tuotua laskua ei voi lähettää automaattisesti järjestelmään, ennen kuin täsmäytetty tuotteen vastaanoton määrä on sama kuin laskun määrä. Kun asetukseksi valitaan **Kyllä** , käyttöön otetaan kirjatun tuotteen vastaanottojen automaattinen täsmäytys laskuriveihin, jota varten kolmisuuntainen täsmäytyskäytäntö on määritetty. Kyseistä prosessia suoritetaan, kunnes täsmäytetyn tuotteen vastaanotettu määrä vastaa laskun määrää. Tässä vaiheessa lasku lähetetään automaattisesti työnkulkujärjestelmään.

    Täsmäytä tuotteen vastaanotot laskuriveihin ennen automaattista lähettämistä -asetus on käytettävissä vain, jos **Ota laskun täsmäytyksen vahvistus käyttöön** -vaihtoehto on valittu. Kun tämä vaihtoehto on valittu, **Täsmäytä tuotteen vastaanotot automaattisesti laskuriveihin** -vaihtoehto valitaan automaattisesti.

- **Edellytä automaattisessa työnkulun lähetyksessä, että lasketut yhteissumma on sama kuin tuotu yhteissumma** – Jos tämän vaihtoehdon asetuksena on **Kyllä** , laskua ei voi lähettää työnkulkujärjestelmään, ennen kuin laskulle laskettu yhteissumma on sama kuin tuotu yhteissumma. Jos tämän vaihtoehdon asetuksena on **Ei** , lasku voidaan voi lähettää työnkulkujärjestelmään, mutta sitä voi kirjata, ennen kuin laskettu yhteissumma on korjatut vastaamaan tuotua yhteissummaa. Jos laskun summaa tai arvolisäveron summaa ei tuoda, asetukseksi on määritettävä **Ei**.
- **Täsmäytä tuotteen vastaanotot automaattisesti laskuriveihin** – Jos tämän vaihtoehdon asetuksena on **Kyllä** , taustaprosessia voidaan käyttää kirjatun tuotteen vastaanottojen automaattiseen täsmäytyksen laskuriveihin, jota varten kolmisuuntainen täsmäytyskäytäntö on määritetty. Kyseistä prosessia suoritetaan, kunnes täsmäytetyn tuotteen vastaanotettu määrä vastaa laskun määrää tai kunnes **Automaattisen täsmäytyksen yrityskertojen määrä** -kentän arvo saavutetaan. Prosessia voidaan suorittaa, kunnes lasku on lähetetty työnkulkujärjestelmään.

    Tämä asetus on käytettävissä vain, jos **Ota laskun täsmäytyksen vahvistus käyttöön** -asetus on valittu.

    Jos **Täsmäytä tuotteen vastaanotot laskuriveihin ennen automaattista lähettämistä** -asetuksena on **Kyllä** , tämän vaihtoehdon asetuksena ei voi olla **Ei**. Jos tässä vaihtoehdossa on valittu **Ei** , **Täsmäytä tuotteen vastaanotot laskuriveihin ennen automaattista lähettämistä** -asetukseksi valittava ensin **Ei**.

- **Automaattisen täsmäytyksen yrityskertojen määrä** – Valitse, kuinka monta kertaa järjestelmä yrittää täsmäyttää tuotteen vastaanotot laskuriviin, ennen kuin se päättää prosessin epäonnistuneena. Kun määritetty yrityskertojen määrä saavutetaan, lasku poistetaan automaattisesta käsittelystä.
- **Vahvista vain, kun täsmäytetyn tuotteen vastaanottomäärä on sama kuin laskun määrä** – Jos valitset tämän vaihtoehdon laskun täsmäytys vahvistetaan automaattisesti vain, jos täsmäytetyn tuotteen laskurivin määrä on sama kuin laskun laskurivin määrä. Jos tämän vaihtoehdon valinta poistetaan, laskun täsmäytys vahvistetaan aina, kun järjestelmä automaattisesti täsmäyttää tuotteen vastaanottorivin laskuriviin.
