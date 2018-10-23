---
title: Dynamics 365 for Talent Core HR -ohjelman uudet tai muuttuneet ominaisuudet (10. syyskuuta 2018)
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR -ohjelman uusia tai muuttuneita ominaisuuksia."
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/12/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Dynamics 365 for Talent Core HR -ohjelman uudet tai muuttuneet ominaisuudet (10. syyskuuta 2018)

[!include [banner](includes/banner.md)]

**Koontiversio 8.1.138.0**

Tässä aiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Salli poissaolopyyntöjä koskeva erityinen kellonaika (puoli päivää)

Jos lomat ja poissaolot on määritetty siten, että poissaolo merkitään päivinä, voit nyt myös ottaa käyttöön puolen päivän määrityksen. Kun käyttäjä sitten lähettää poissaolopyynnön, hän voi määrittää, pyytääkö hän poissaoloa päivän ensimmäiselle vai toiselle puoliskolle.

Oletusarvon mukaan tämä asetus on pois käytöstä. Jos työntekijät ovat pyytäneet poissaoloa päivän ensimmäiselle tai toiselle puoliskolle, sinun on otettava tämä asetus käyttöön henkilöstöhallinnon parametrien **Lomat ja poissaolot** -alueella.

Tämän toiminnon suojausoikeus on henkilöstöhallinnon parametrien ylläpitäminen.

## <a name="validation-of-leave-and-absence-entries"></a>Lomien ja poissaolojen syötteiden oikeellisuustarkistus

Loman määrityksestä riippuen työntekijät, jotka yrittävät lähettää työpäivää pidemmän poissaolopyynnön, saavat varoitusviestin. Toisin sanoen heitä varoitetaan, jos he yrittävät ottaa vapaaksi enemmän kuin yhden kokonaisen päivän jonakin tiettynä päivämääränä.

Tämä oikeellisuustarkistus on aina käytössä. Aina kun työntekijät ylittävät määritetyn päivärajan, he saavat varoituksen poissaolopyyntönsä yhteydessä.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Lisäkenttiä ehdollisille selvityksille työnkuluissa

Core HR:n useisiin työnkulkuihin on lisätty kenttiä ehdollisille selvityksille ja paikkamerkeille.

Seuraavat kentät on lisätty kompensaation, irtisanomisen ja siirron työnkulkuihin:

- Työsuhteen tyyppi
- Oikeushenkilö
- Korjattu työntekijän aloituspäivä
- Työnantajan ilmoituksen summa
- Työnantajan ilmoitusyksikkö
- Siirtopäivämäärä
- Työntekijän ilmoituksen summa
- Työntekijän aloituspäivä
- Työntekijän ilmoitusyksikkö
- Koeajan lopetuspäivä
- Toimi
- Unioni
- Osasto
- Toimityyppi
- Yrityksen sijainti
- Tehtävänimike
- Työ
- Työtyyppi
- Työluokka
- Työtehtävä

Seuraavat kentät on lisätty toimen työnkulkuun:

- Toimi
- Unioni
- Osasto
- Toimityyppi
- Yrityksen sijainti
- Tehtävänimike
- Työ
- Työtyyppi
- Työluokka
- Työtehtävä

Ehdollisten selvitysten ja paikkamerkkien kenttiä voivat käyttää kaikki käyttäjät, jotka voivat määrittää edellä mainittuja työnkulkuja.

## <a name="navigation-to-attract-from-personnel-management"></a>Siirtyminen Attractiin henkilöstöhallinnosta

Jos Attractia ei ole määritetty henkilöstöhallinnossa, **Palkattavat ehdokkaat** -osiossa käyttäjiä kehotetaan aloittamaan Attractin käyttö sen sijaan, että näytettäisiin viesti "Emme löytäneet mitään näytettävää tähän”.

## <a name="other-changes"></a>Muut muutokset

Tämä versio sisältää useita muita ohjelmavirhekorjauksia:

- Kun palkataan alihankkija, **Kompensaatio**-välilehden ei pitäisi olla saatavilla pyyntö-/toimintosivulla.
- Pyynnön päättymisprosessin aikana et voi jatkaa, ennen kuin kaikki vaaditut kentät sisältävät tietoja.
- Lajittelujärjestyksen ja päivämäärän näyttöongelmat on korjattu henkilöstöhallinnon analyysissa.

