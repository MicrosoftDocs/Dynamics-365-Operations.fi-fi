---
title: Sähköpostimallit
description: Tässä ohjeaiheessa on tietoja Dynamics 365 for Talent - Attractissa luotavista ja käytettävistä sähköpostimalleista.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
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
ms.openlocfilehash: 1c7c017cce26b6b250d899bba891d6823b40c282
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729723"
---
# <a name="email-templates"></a>Sähköpostimallit
[!include[banner](../includes/banner.md)]

Järjestelmänvalvojat voivat luoda sähköpostimallikirjaston avulla kaikille yhteisen teeman ja brändin kaikille Microsoft Dynamics 365 for Talent: Attractin ja Offerin kautta lähetettäville sähköposteille. Järjestelmänvalvojat voivat myös valita sähköpostisisältöjen valikoiman muiden käyttäjien käyttöön. Työhönottoryhmä voi tehostaa sähköpostien lähettämistä omassa työnkulussaan näiden mallien avulla. Jotkin sähköpostiviestit on määritetty automaattisesti lähettäviksi, ja järjestelmänvalvoja voi mukauttaa näiden viestien sisältöä sähköpostimallikirjaston avulla.

> [!NOTE]
> Jos haluat käyttää sähköpostimalleja, organisaatiossa on oltava kattava työhönottolaajennus.

## <a name="global-template-configurations"></a>Yleiset mallimääritykset

Jos järjestelmänvalvoja haluaa luoda yhtenäisen brändin kaikelle sähköpostiviestinnälle, hänen on ensin määritettävä yleinen ylä- ja alatunniste kaikille sähköpostimalleille. Järjestelmänvalvoja voi ladata hallintakeskuksen **Sähköpostimallin asetukset** -välilehden **Ylätunniste**-osassa kuvan, jota käytetään kaikkien sähköpostiviestin ylätunnisteena tai bannerina. Kuva voi olla yrityksen logo, lomakelogo tai muu soveltuva kuva. Kuvan suositeltu leveys on 25–800 kuvapistettä ja korkeus 25–150 kuvapistettä, koska nämä mitat soveltuvat parhaiten useimpiin sähköpostiohjelmiin, kuten Microsoft Microsoft Outlookiin. Kuvan on oltava JPEG-, JPG-, PNG- tai SVG-tiedosto ja tiedoston koon on oltava alle 1 Mt. Kun kuva ladattu, ylätunnisteesta muodostuva esikatselu näytetään. Jos ylätunnisteen kuva poistettava tai vaihdettava, järjestelmänvalvoja voi tehdä sen esikatselun yläpuolella olevalla **Poista**-asetuksella.

Järjestelmänvalvoja voi lisätä **Alatunniste**-osaan linkit yrityksen viestinnässä käyttämään tietosuojakäytäntöön ja käyttöehtoihin. Nämä linkit sisältyvät automaattisesti muodostettavaan alatunnisteeseen. Alatunnisteen esikatselu avautuu. Järjestelmänvalvoja voi myös valita tietyn kielen, jolla sähköpostin alatunnisteet lähetetään sähköpostien osana. Samaa kielimääritystä käytetään myös haastattelun yhteenvetotaulun luomiseen. 

Muista tallentaa muutokset, ennen kuin suljet hallintakeskuksen.

> [!NOTE] 
> Ylä- ja alatunniste ovat kaikkien sähköpostiviestien yleisiä asetuksia. Niinpä ne näkyvät kaikissa Attractin kautta lähetettävissä sähköpostiviesteissä. Jos asetuksia ei ole määritetty, ylä- ja tunniste jätetään pois kaikista sähköpostiviesteistä.

## <a name="email-template-library"></a>Sähköpostimallikirjasto 

Kun yleiset mallinmääritykset on tehty, järjestelmänvalvoja voi aloittaa kaikkien Attractista ja Offerista lähetettävien sähköpostiviestien mallien luominen ja järjestäminen. Vain järjestelmänvalvojat voivat käyttää sähköpostimallikirjastoa. Voit avata kirjaston valitsemalla pääsiirtymisvalikossa **Sähköpostimallit**-välilehden. Kirjaston luokat perustuvat erilaisiin Attractin tehtäviin, joista lähetetään sähköpostiviestejä. Näitä tehtäviä ovat esimerkiksi aikatauluttaminen, arviointi sekä työn luonti ja tarjoaminen. Järjestelmänvalvoja voi valita minkä tahansa luokan ja tarkastella kaikkia tehtävään liitettyjä sähköpostityyppejä. Valitse esimerkiksi **Aikatauluttaminen**, jos haluat tarkastella erilaisia sähköpostityyppejä, joita lähetetään aikataulutusprosessin aikana, ja kaikkia kuhunkin sähköpostityyppiin liittyviä malleja. Luokan jokainen aliosa vastaa sähköpostityyppiä.

Joillakin sähköpostityypeillä voi olla useita vastaanottajia. Esimerkiksi **Aikataulutus**-luokan sähköpostiviestit, jotka lähetetään, kun tarvitaan haastatteluaikataulun yhteenveto, lähetetään sekä hakijoille että haastattelijoille. Jokaisessa osassa on kaksi pääsaraketta: **Mallin otsikko** ja **Vastaanottaja**. Kukin osan rivi vastaa sähköpostityypin yhtä mallia. Aluksi jokaisen mallin rivillä on lukkokuvake. Tämä kuvake ilmaisee, että malli on Attractin vakiomalli, jota ei voi poistaa. Järjestelmänvalvoja voi käyttää kunkin mallin ellipsipainiketta (**...**) ja kopioida mallin, määrittää sen oletukseksi tai poistaa sen. Kun malli on määritetty oletusmalliksi, vaihtoehtoja on kaksi. Mallin rivin merkintä tai merkinnät ilmaisevat, kumpi vaihtoehto on käytössä.

- **Oletus** – tämä merkintä ilmaisee, että malli on lähetetyn sähköpostiviestin oletusmalli ja että siihen lisätään tietoja, kun käyttäjä lähettää kyseisen tyypin sähköpostiviestin.
- **Oletus** + **Automaattilähetys** – tämä merkintäyhdistelmä ilmaisee, että malli on järjestelmän muodostamien automaattisesti lähetettävien sähköpostiviestien aktiviinen malli.

Voit muokata mallia valitsemalla rivin ja tekemällä malliin muutoksia.

> [!NOTE]
> Jokaisella tietyn sähköpostityypin vastaanottajalla on oletusmalli. Kaikki Attractin vakiomallit määritetään oletusmalleiksi siihen saakka, että järjestelmänvalvoja luo uuden mallin tietylle sähköpostityypille ja määrittää sen oletusmalliksi.

## <a name="create-a-template"></a>Luo malli

Voit luoda mallin valitsemalla sähköpostimallikirjaston oikeassa yläkulmassa **+ Uusi malli**. Voit valita sähköpostityypin, jolle olet luomassa mallia, valitsemalla vastaanottajan, prosessin ja tapahtuman, jonka vuoksi sähköpostiviesti lähetetään. Valitse sitten **Luo**.

Malli avautuu muokkausnäkymässä ja voit nimetä mallin. Jos malli on esimerkiksi tarkoitettu yhdysvaltalaisen yliopiston hakijoille mutta sisältö on kirjoitettu ranskaksi, voit kirjoittaa otsikoksi **Yliopisto\_USA\_ranska**. Mallin otsikko, aiherivi ja tekstisisältö voivat tukea muitakin kieliä kuin englantia.

Mallin **Vastaanottaja**-kenttää ei voi muokata, koska valitsit vastaanottajan jo siinä vaiheessa, kun loit mallin ensimmäisen kerran.

Voit lisätä Kopio-riville rooleja, kuten **Työhönottaja** tai **Työhön ottava esimies**. Kun sähköpostiviesti lähetetään, nämä rooli korvataan automaattisesti soveltuvilla käyttäjillä työkontekstin perusteella.

Aiherivi ja tekstisisältö tukevat paikkamerkkejä. Voit lisätä paikkamerkin kirjoittamalla **\#** ja valitsemalla sitten sopivan paikkamerkin automaattisen täytön avattavasta luettelosta. Luettelo käytettävissä olevista paikkamerkeistä on sivun oikealla puolella. Kun sähköpostiviesti lähetetään, paikkamerkit korvataan automaattisesti työn ja vastaanottajan perusteella. Esimerkiksi hakijoille lähetettävän sähköpostin mallissa on paikkamerkki \#{Ehdokkaan\_nimi}. Kun sähköposti lähetetään Cameron-nimiselle hakijalle, kyseinen paikkamerkki korvataan Cameronin nimellä.

Tekstisisältöeditori on RTF-editori, jolla tekstiin voi lisätä tyylejä ja muotoiluja. Sen avulla voi lisätä myös hyperlinkkejä ja ankkureita.

Kun tietylle sähköpostityypille on luotu malli, valitse mallirivin ellipsipainike (**...**) ja määritä se oletusmalliksi.

## <a name="consume-templates"></a>Mallit käyttäminen

Kun työhönottoryhmä lähettää sähköpostiviestin, se voi käyttää järjestelmänvalvojan luomia malleja. Jos käyttäjä on lähettämässä sähköpostiviestiä, jolle on luotu useita malleja, sähköpostin kirjoitustyönkulussa tulee näkyviin avattava luettelo. Oletusmalli lisätään automaattisesti, mutta käyttäjä voi valita toisen mallin.

> [!NOTE] 
> Automaattisesti lähetettäville sähköpostiviesteille voidaan luoda useita malleja. Kuitenkin vain yksi malli voidaan määrittää aktiiviseksi malliksi. Koska tapahtumat käynnistävät tämän prosessin, vain järjestelmänvalvoja voi määrittää käytettävän mallin mallikirjaston **Oletus**- ja **Automaattilähetys**-merkintäyhdistelmän perusteella.
