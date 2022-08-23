---
title: Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa Dynamics 365 Salesin avulla
description: Tässä artikkelissa kuvataan, miten Microsoft Dynamics 365 Salesia käytetään liikekumppanien hyväksymisten hallitsemiseen Dynamics 365 Commercen yritysten välisten (B2B) verkkosivustojen osalta.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: d178e619fca7915286181aa803376cd564f60a26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278648"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa Dynamics 365 Salesin avulla

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten Microsoft Dynamics 365 Salesia käytetään liikekumppanien hyväksymisten hallitsemiseen Dynamics 365 Commercen yritysten välisten (B2B) verkkosivustojen osalta. Organisaatiot, jotka ovat jo sijoittaneet Dynamics 365 Sales -ratkaisuun, voivat liidi- ja mahdollisuuskonseptejaan B2B-verkkokaupan liikekumppaneiden hyväksymisprosessissa.

Taustatietoja B2B-liikekumppaneiden hyväksymisprosessista: [Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa](manage-b2b-users.md).

Mahdolliset liikekumppanit voivat käynnistää käyttöönottoprosessin B2B-verkkokauppasivustolle lähettämällä käyttöönottopyynnön B2B-verkkosivuston linkin kautta. Kun pyyntö on lähetetty ja asiaan liittyvät työt (kuten **P-0001** ja **Synkronoi tilaukset ja kanavoi pyynnöt**) on suoritettu Commerce headquarters -sovelluksessa, käyttöönottopyyntö tallennetaan Commerce headquarters -sovelluksen **Kaikki prospektit** -sivulle. Tämän jälkeen liikekumppanin prospektin hyväksymisprosessi voidaan suorittaa loppuun Salesissa.

Kun Salesin ja Commercen välinen integrointi on otettu käyttöön, liikekumppaniprospektin luominen Commercessä johtaa *liidin* luomiseen Salesissa.

Seuraavassa kuvassa on esimerkki liidinluontisivusta liikekumppaniprospektille Salesissa.

![Liidinluontisivu Dynamics 365 Salesissa.](../media/LeadInSales.png)

Kuvassa **Yhteyshenkilö**-osassa näkyy henkilö, joka lähetti käyttöönottopyynnön, ja **Yritys**-osassa näkyy organisaatio. **Aikajana**-osassa oleva huomautus ilmaisee, että liidin on luonut kaksoiskirjoitusinfrastruktuuri. Koska liidin on luonut kaksoiskirjoitusinfrastruktuuri, se ei tule näkyviin avattavassa **Omat avoimet liidit** -luettelossa. Sen sijaan se tulee näkyviin uudessa näkymässä, jonka nimi on **Kaikki Commercen B2B-liidit**.

Salesin vakiomuotoisen liidinhyväksymisprosessin mukaan luodaan *mahdollisuus*-, *yhteyshenkilö*- ja *tili*-tietue, kun käyttäjä hyväksyy liidin. Kaksoiskirjoitusinfrastruktuuria käytetään yhteyshenkilö- ja tilitietueiden Commerceen kirjoittamiseen. Yhteyshenkilö luodaan *henkilö*-tyypin asiakkaana ja yritys luodaan *organisaatio*-tyypin asiakkaana. Jos käyttäjä valitsee mahdollisuuden osalta **Sulje voitettuna**, prospekti hyväksytään Commercessä. Prospektin hyväksyminen aiheuttaa asiakashierarkian luomisen.

Kaikki muut liiketoimintaprosessit tapahtuvat Commercessä. Näitä prosesseja ovat esimerkiksi sähköpostin lähettäminen liikekumppanille, luottorajan hallinnan määrittäminen käyttäjille ja käyttäjien lisääminen B2B-verkkosivustolle. Jos käyttäjä sen sijaan hylkää liidin tai merkitsee mahdollisuuden hävityksi liidin hyväksymisen sijaan, prospekti merkitään Commercessä hylätyksi ja pyytäjälle lähetetään käyttöönoton hylkäämistä koskeva sähköposti.

## <a name="enable-integration-between-sales-and-commerce"></a>Salesin ja Commercen välisen integroinnin käyttöönotto

Salesin ja Commercen välinen integrointi perustuu kaksoiskirjoitusinfrastruktuuriin. Siksi kaksoiskirjoituksen pitäisi olla käytössä ja toimia, jotta yhdessä järjestelmässä luodut asiakkaat kirjoitetaan toiseen järjestelmään. Lisätietoja kaksoiskirjoitusinfrastruktuurista: [Kaksoiskirjoituksen yleiskatsaus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Kun kaksoiskirjoitus on määritetty, täytäntöönpanokumppani voi siirtyä [Microsoft AppSourceen](https://appsource.microsoft.com/) ja etsiä ratkaisua nimeltään [Kaksoiskirjoituksen Commerce-ratkaisut](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Asenna paketti käyttämällä ohjattua vakioasennustoimintoa ja testaa se luomalla prospekti B2B-sivustolla. Kun prospekti on luotu, tarkista, että pyyntö näkyy **Kaikki prospektit** -sivulla, ja tarkista sitten, että prospekti näkyy liidinä Salesissa.

## <a name="additional-resources"></a>Lisäresurssit

[Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
