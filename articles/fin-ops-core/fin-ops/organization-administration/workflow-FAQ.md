---
title: Työnkulun usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä työnkulkujärjestelmästä.
author: ChrisGarty
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0068f7e678b069a6a2563ed227e42393ddacf5d78d988ca73f576cdcff5e3f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749385"
---
# <a name="workflow-faq"></a>Työnkulun usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä työnkulkujärjestelmästä.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Miksi ilmoituksia on useita, kun työnimike hylätään?
Kun työnimike hylätään, kyseinen työnimike valmistuu hylättynä. Toinen työnimike luodaan ja määritetään aloittajalle. Tämä tarkoittaa, että aloittaja saa ilmoituksen hylätystä työnimikkeestä. Käyttäjä, joka on määritetty uuteen muutospyynnön työnimikkeeseen, saa erillisen ilmoituksen. 

Nämä ilmoitukset on tarkoitettu eri työnimikkeelle, mutta niiden samankaltaisuus voi aiheuttaa hämmennystä. Pyrimme parantamaan tätä myöhemmissä julkaisuissa.

## <a name="why-are-my-workflow-exports-failing"></a>Miksi työnkulun vienti ei ole mahdollista?
Työnkulun viennissä on tällä hetkellä rajoitus, joka estää työnkulkujen nimiä ylittämästä 48 merkkiä. Jos nimi on pidempi kuin 48 merkkiä, palvelin ei voi todentaa pyyntöä ja / tai estää tiedoston viemisen ilman tiedostotyyppiä. Saat lisätietoja blogikirjoituksesta [Työnkulun viennin vianmääritys](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Voiko työnkulun lähettäjä myös hyväksyä työnkulun?
Kyllä, Työnkulun lähettäjä voi myös hyväksyä työnkulun, jos määritys sen sallii. Voit estää tämän valitsemalla kohdassa **Järjestelmänhallinta > Työnkulku > Työnkulun parametrit > Yleinen > Hyväksyjä > Estä lähettäjän hyväksyntä** **Kyllä**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Voinko lisätä työnkulkuihin hälytyksiä toimittamaan ilmoituksia käyttäjille?
Seuraavat seikat on otettava huomioon, kun työnkulkuihin lisätään hälytyksiä toimittamaan ilmoituksia:
- Hälytys- ja työnkulkuilmoitusmekanismien vertailu
    - Tietueiden muutoksille voidaan määrittää hälytyksiä. Työnkulut muuttavat tietueita, joten työnkulun aiheuttamaan tietuemuutokseen voi määrittää hälytyksen. Koska työnkuluissa on erilaisia sisäisiä ilmoitusasetuksia, hälytysten käyttäminen ei ole paras mahdollinen vaihtoehto.
- Työnkulkujen vakioilmoitukset 
    - Työnkulut sisältävät valmiita sähköposti-ilmoituksia. Asiakas voi määrittää ilmoitukset lähettämään käyttäjille sähköpostiviestejä. Nämä ilmoitukset eivät aiheuta toimintokeskuksen sanomien lähettämistä käyttäjille.
    - Tulevaan päivitykseen lisätään toimintokeskuksen sanoma, jotta työnkulun työnimike määritetään käyttäjälle. 
- Ilmoitusten lisääminen työnkulkuihin
    - Toimintokeskuksen sanomat voidaan luoda tietyille käyttäjille, kuten työnkulusta luotu sanoma X++-kielessä.
    - [Työnkuluissa on liiketoimintatapahtumia](../../dev-itpro/business-events/business-events-workflow.md), joilla asiakas voi käynnistää työnkulut, joissa on heidän etsimänsä ilmoitukset.   

Tiivistäen voi todeta, että jos käyttäjä ei saa oikeaa ilmoitusta toimintokeskuksesta, kun heille määritetään työnkulun työnimike, he voivat muodostaa lisäilmoituksia tai toisia ilmoituksia käyttämällä [työnkulun liiketoimintatapahtumia](../../dev-itpro/business-events/business-events-workflow.md) yhdessä Microsoft Power Automate'n kanssa.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Miksi työnkulkueditori ei voi käynnistyä AD FS -palvelun avulla?
Kun Active Directory -liittämispalvelut (AD FS) suoritetaan päivitetyssä ympäristössä, työnkulkueditorilla saattaa olla ongelmia käynnistymisen yhteydessä. Jos näin on, varmista, että URL-osoite https://dynamicsaxworkfloweditor/ lisätään ominaisuuteen **Microsoft Dynamics 365 for Operationsin paikallinen - työnkulku - natiivisovellus** ADFS-asetuksissa.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Miksi SQL lukkiutuu työnkulun käsittelyn aikana? 
**Työnkulun nimikkeiden määrä erää kohti** -kentän oletusarvo on **Työnkulun parametrit** -sivulla on 0. Arvo 0 aiheuttaa sen, että oletusarvoksi muuttuu 20 nimikettä erää kohden. Ole varovainen tätä arvoa muuttaessasi, koska nimikkeiden suuri määrä erää kohti (> 40) voi aiheuttaa SQL-lukituksia.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Mikä työnkulun parannettu virhetoiminto on?
Version 10.0.13 työnkulun parannettu virhetoiminto lisää virhekoodit erojen tekemiseksi työnkulun virheiden luokkien välillä. Ilmoitetut virhesanomat ovat enimmäkseen samoja, mutta pienin selkeyttävin eroin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
