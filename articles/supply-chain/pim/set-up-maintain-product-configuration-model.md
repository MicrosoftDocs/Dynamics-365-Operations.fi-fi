---
title: Määritä tuotemääritysmalli
description: Tässä artikkelissa kuvataan tuotemääritysmallin määrityksen ja luonnin vaiheet.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a0adc1f553c8f92c62310c28478407fb53ee98915999f10c0fa4f42e00995f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714905"
---
# <a name="set-up-a-product-configuration-model"></a>Määritä tuotemääritysmalli

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan tuotemääritysmallin määrityksen ja luonnin vaiheet.

| Tehtävä                                                        | kuvaus                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luo päätuote.                                    | Luo päätuote **Päätuote**-luettelosta. Vapauta päätuote kaikille yrityksille, joihin se liittyy. Jos päätuotetta käytetään tuotemääritysmallin versiona tai alikomponenttina, määritystekniikaksi on valittava **Rajoituspohjainen määritys** ja konfiguraatiodimensio täytyy valita vain tuotedimensioryhmälle. |
| Luo komponentteja.                                          | Luo komponentteja **Komponentit**-sivulla. Komponentit ovat tuotemääritysmallin rakenneosia, ja niitä voidaan käyttää useissa tuotemääritysmalleissa.                                                                                                                                                                                                                      |
| Luo määritetyyppejä.                                     | Luo määritetyyppejä **Määritetyypit**-sivulla. Määritetyypit määrittelevät tietotyypit kaikille tuotemääritysmalleissa käytettäville määritteille. Jos määritteenä on **totuusarvo**, kiinteän luettelon **teksti** tai tietyllä alueella oleva **kokonaisluku**, siinä näkyvät arvot, jotka ovat käytettävissä, kun määrität tuotemääritysmalliin perustuvaa tuotevarianttia.       |
| Luo tuotemääritysmalli.                       | Luo tuotemääritysmalli **Uusi tuotemääritysmalli** -sivulla.                                                                                                                                                                                                                                                                                                              |
| Lisää tuotemääritysmalliin määritteitä.            | Luo määrite **Määritteet**-pikavälilehdessä **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla. Määritteet kuvailevat tuotemääritysmallin ominaisuuksia.                                                                                                                                                                                                       |
| Lisää tuotemääritysmalliin rajoituksia.           | Luo rajoituksia **Rajoitukset**-pikavälilehdessä **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla. Tuotemäärityksen on täytettävä kyseiset rajoitukset. Rajoitukset ovat joko lausekerajoituksia tai taulukkorajoituksia.                                                                                                                                 |
| Lisää tuotemääritysmalliin alikomponentteja.         | Luo alikomponentteja **Alikomponentit**-pikavälilehdessä **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla. Alikomponentit liittyvät komponentteihin, ja ne on linkitetty nimikkeisiin, jotka edustavat alikomponenttia.                                                                                                                                                                       |
| Lisää tuotemääritysmalliin käyttäjän vaatimuksia.     | Käyttäjän vaatimukset ovat samankaltaisia alikomponentit, mutta ne eivät viittaa mihinkään nimikkeeseen. Käyttäjän vaatimukset ovat ikään kuin haamutuoterakenteita. Kaikki tuoterakennerivit tai reitityksen työvaiheet, jotka sijoitetaan suoraan käyttäjän vaatimuksen alle, tiivistetään pääkomponenttiin.                                                                                                                       |
| Lisää tuotemääritysmalliin tuoterakennerivejä.             | Luo tuoterakennerivejä **Tuoterakenteen rivit** -pikavälilehdessä **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla. Tuoterakennerivejä tarvitaan tuotevarianttia luotaessa.                                                                                                                                                                                                 |
| Lisää tuotemääritysmalliin reitityksen työvaiheita.      | Luo reitityksen työvaiheita **Reitityksen työvaihe** -pikavälilehdessä **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla. Reitityksen työvaiheet edustavat yhtä vaihetta vaihesarjassa, jolla luodaan tuotevariantti.                                                                                                                                                    |
| Luo tuotemääritysmallille aktiivinen versio. | Luo tuotemääritysmallille aktiivinen versio **Versiot**-sivulla. Versio on tuotemääritysmallin ja päätuotteen välinen suhde. Tuotemääritysmalli, jolla on aktiivinen versio, voidaan määrittää myyntitilauksesta, myyntitarjouksesta, ostotilauksesta tai tuotantotilauksesta.                                                               |
| Kokeile tuotemääritysmallia.                         | Testaa tuotemääritysmalli joko **Rajoituspohjaisen tuotemääritysmallin tiedot**- tai **Tuotemääritysmallien luettelo** -sivulla. Tuotemääritysmallin testaus simuloi tilauksen käsittelyn aikana tapahtuvaa tuotemallin määritysprosessia.                                                                                                |
| Luo tuotemääritysmallille mallipohja.                | Luo tuotemääritysmallin mallipohja **Määritysmallit**-sivulla. Määritysmalli sisältää arvot tuotemääritysmallin määritteille. Valitse määritteiden arvot **Konfiguroi rivi** -sivulta. Voit myös ladata tuotemääritysmallin mallipohjan määrittäessäsi tuotemallia.                                                   |
| Määritä nimike.                                          | Tuotemääritysmalleja voidaan määrittää myyntitilauksesta, myyntitarjouksesta, ostotilauksesta tai tuotantotilauksesta.                                                                                                                                                                                                                                                                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]