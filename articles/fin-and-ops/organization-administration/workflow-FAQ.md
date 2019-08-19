---
title: Työnkulun usein kysytyt kysymykset
description: Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ca04433937d0d7a16b450f190cd3814533e270d
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741053"
---
# <a name="workflow-faq"></a>Työnkulun usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on usein kysyttyjä kysymyksiä Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmässä.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Miksi ilmoituksia on useita, kun työnimike hylätään?
Kun työnimike hylätään, kyseinen työnimike valmistuu hylättynä. Toinen työnimike luodaan ja määritetään aloittajalle. Tämä tarkoittaa, että aloittaja saa ilmoituksen hylätystä työnimikkeestä. Käyttäjä, joka on määritetty uuteen muutospyynnön työnimikkeeseen, saa erillisen ilmoituksen. 

Nämä ilmoitukset on tarkoitettu eri työnimikkeelle, mutta niiden samankaltaisuus voi aiheuttaa hämmennystä. Pyrimme parantamaan tätä myöhemmissä julkaisuissa.

## <a name="why-are-my-workflow-exports-failing"></a>Miksi työnkulun vienti ei ole mahdollista?
Työnkulun viennissä on tällä hetkellä rajoitus, joka estää työnkulkujen nimiä ylittämästä 48 merkkiä. Jos nimi on pidempi kuin 48 merkkiä, palvelin ei voi todentaa pyyntöä ja / tai estää tiedoston viemisen ilman tiedostotyyppiä. Seuraava blogikirjoitus sisältää lisätietoja [Työnkulun viennin vian määrityksestä](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Voiko työnkulun lähettäjä myös hyväksyä työnkulun?
Kyllä, Työnkulun lähettäjä voi myös hyväksyä työnkulun, jos määritys sen sallii. Voit estää tämän valitsemalla kohdassa **Työnkulkuparametrit > Yleiset > Hyväksyjä > Estä lähettäjän hyväksyntä** **Kyllä**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Voinko lisätä työnkulkuihin hälytyksiä toimittamaan ilmoituksia käyttäjille?
Seuraavat seikat on otettava huomioon, kun työnkulkuihin lisätään hälytyksiä toimittamaan ilmoituksia:
- Hälytys- ja työnkulkuilmoitusmekanismien vertailu
    - Tietueiden muutoksille voidaan määrittää hälytyksiä. Työnkulut muuttavat tietueita, joten työnkulun aiheuttamaan tietuemuutokseen voi määrittää hälytyksen. Koska työnkuluissa on erilaisia sisäisiä ilmoitusasetuksia, hälytysten käyttäminen ei ole paras mahdollinen vaihtoehto.
- Työnkulkujen vakioilmoitukset 
    - Työnkulut sisältävät valmiita sähköposti-ilmoituksia. Asiakas voi määrittää ilmoitukset lähettämään käyttäjille sähköpostiviestejä. Nämä ilmoitukset eivät aiheuta toimintokeskuksen sanomien lähettämistä käyttäjille.
    - Tulevaan päivitykseen lisätään toimintokeskuksen sanoma, jotta työnkulun työnimike määritetään käyttäjälle. 
- Ilmoitusten lisääminen työnkulkuihin
    - Toimintokeskuksen sanomat voidaan luoda tietyille käyttäjille, kuten työnkulusta luotu sanoma X++-kielessä.
    - [Työnkuluissa on liiketoimintatapahtumia](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), joilla asiakas voi käynnistää työnkulut, joissa on heidän etsimänsä ilmoitukset.   

Tiivistäen voi todeta, että jos käyttäjä ei saa oikeaa ilmoitusta toimintokeskuksesta, kun heille määritetään työnkulun työnimike, he voivat muodostaa lisäilmoituksia tai toisia ilmoituksia käyttämällä [työnkulun liiketoimintatapahtumia](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) yhdessä Microsoft Flow'n kanssa.
