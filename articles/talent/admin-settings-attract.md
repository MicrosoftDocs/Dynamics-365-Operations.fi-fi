---
title: Attractin järjestelmänvalvojan asetukset
description: Tässä ohjeaiheessa käsitellään toimintojen käyttöönottoa Attractissa organisaatioiden ja käyttäjien osalta.
author: ''
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: fb7b5e5b98ddb8e0e44fccbb0ddbb05199265414
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304199"
---
# <a name="admin-settings-in-attract"></a>Järjestelmänvalvojan asetukset Attractissa
[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attractin hallintakeskus sisältää Attract-sovelluksen määritysvaihtoehdot, integrointivaihtoehdot ja asetusvaihtoehdot.

## <a name="company-information"></a>Yrityksen tiedot

Kirjoita yrityksen näyttönimi ja lisää yrityksen logo. Näyttönimeä ja logoa voidaan sitten käyttää työpaikkailmoituksissa ja perehdyttämisen aikana.

## <a name="linkedin-integration"></a>LinkedIn-integrointi

Määritä LinkedIn Recruiter System Connect (RSC) -integraatio. Kun olet muodostanut LinkedIn-yhteyden LinkedIn-tunnistetiedoilla, voit synkronoida ehdokkaan LinkedIn-profiilin, hakemukset, haastattelun palautteen ja työhönottoryhmän muistiinpanot. Täysi LinkedIn Recruiter -käyttöoikeus on pakollinen. Lisätietoja LinkedIn Recruiterista on kohdassa [Recruiter System Connect (RSC) – usein kysytyt kysymykset](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Käyttöoikeudet

Määritä rooleja käyttäjille organisaatiossa. Käytettävissä on seuraavat roolit: **Järjestelmänvalvoja**, **Työhönottaja**, **Työhön ottava esimies** ja **Vain luku**. Lisätietoja käyttöoikeuksista on kohdassa [Suojaus ja roolien hallinta Attractissa](./security-attract.md).

## <a name="feature-management"></a>Ominaisuuksien hallinta

Kun uusia ominaisuuksia lisätään, on mahdollista, että julkaistaan julkisessa esiversiossa. Julkisen esiversion ominaisuudet eivät vastaa kaikkia palveluvaatimuksia. Näiden ominaisuuksien vastaanottaminen on samalla suostumus siihen, että tietosi jaetaan ulkoisten järjestelmien kanssa. Voit huomata, että organisaatio ei tarvitse kaikki julkaistuja uusia ominaisuuksia. Voit poistaa julkisen esiversion ominaisuudet käytöstä ja ottaa ne takaisin käyttöön organisaation tarpeiden mukaan.

## <a name="template-management"></a>Mallien hallinta

Prosessimalli sisältää kaikki tehtävät, joiden on sisällyttävä työn työhönottoprosessiin. Organisaatio voi päättää, saavatko kaikki ryhmän jäsenet vai vain järjestelmänvalvojat luoda työhönottoprosessimalleja. Jos haluat antaa ryhmän jäsenille mahdollisuuden luoda omat työhönottoprosessimallit, ota Mallien hallinta -toiminnot käyttöön. Lisätietoja prosessimalleista on kohdassa [Attractin prosessimallit](./process-templates-attract.md).

## <a name="email-template-settings"></a>Sähköpostimallin asetukset

Organisaatiot voivat luoda sähköpostimalleja erilaisia tilanteita varten. Voit valita sähköpostimalleihin sisällytettävän ylätunnistekuvan. Valittu ylätunniste näkyy sitten kaikissa sähköpostimalleissa. Voit lisätä mallin alatunnisteeseen organisaation tietosuojatiedot ja viestintää koskevat käyttöehdot. Lisätietoja on kohdassa [Attractin sähköpostimallit](./email-templates.md).

## <a name="offer-process"></a>Tarjousprosessi

Voit määrittää työtarjousten hyväksyntäprosessin. Voit esimerkiksi määrittää, onko tarjous hyväksyttävä, ennen kuin se lähetetään ehdokkaalle. Voit myös edellyttää, että hyväksyjien on annettava kommentti tarjoukseen liittyvästä päätöksestä.

Käytettävissä on kaksi hyväksyntätyönkulkua: **Rinnakkainen** ja **Peräkkäinen**.

- **Rinnakkainen** – hyväksynnät lähetetään kaikki hyväksyjille samaan aikaan.
- **Peräkkäinen** – hyväksynnät lähetetään hyväksyjille tietyssä järjestyksessä.

Voit määrittää myös ehdokaskokemukseen liittyviä asetuksia. Yksi asetuksista esimerkiksi määrittää, voivatko ehdokkaat hylätä tarjouksen ilman jatkokeskustelua. Jos valitset **Salli ehdokkaiden hylätä tarjous ilman jatkokeskustelua** -asetukseksi **Ei**, ehdokkaat voivat käyttää **Hylkää tarjous** -painiketta. Jos valitset asetukseksi **Kyllä**, ehdokkaat voivat hylätä tarjouksen valitsemalla ensin syyn ja sitten **Hylkää tarjous**.

Voit määrittää myös tarjouksen vanhentumispäivän ja pakottaa sen ottamisen käyttöön. Jos valitset **Vaadi vanhentumispäivä kaikille tarjouksille** -asetukseksi **Kyllä**, tarjoukset vanhentuvat, kun määrittämäsi määrä tunteja tai päiviä on kulunut.

Lisätietoja tarjoustenhallinnasta on kohdassa [Tarjoustenhallinnan määrittäminen](./offer-setup.md).
