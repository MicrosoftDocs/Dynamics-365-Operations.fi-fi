---
title: Käyttöomaisuuden eteenpäin siirron raportti
description: Tässä artikkelissa käsitellään käyttöomaisuuden eteenpäin siirron raporttia.
author: moaamer
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a4d423b149957e624269231aede510190f0c14c7
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068777"
---
# <a name="fixed-assets-roll-forward-report"></a>Käyttöomaisuuden eteenpäin siirron raportti

[!include [banner](../includes/banner.md)]

**Käyttöomaisuuden siirto eteenpäin** -raportti on helposti luettava Microsoft Excel -muotoinen raportti, jossa eritellään kauden sulkemista, tilipäätöksiä ja veroilmoituksia varten tarvittavat käyttöomaisuustiedot. Raportti sisältää käyttöomaisuuden alku- ja loppusaldot sekä kauden arvostuksen muutokset. Lisäksi siinä on kauden aikana tapahtuneet uudet käyttöomaisuuden hankinnat ja luovutukset. Tiedot raportoidaan käyttöomaisuuseräkohtaisesti, ja arvojen yhteenveto on saatavana käyttöomaisuusryhmille ja yritykselle.

**Käyttöomaisuuden siirto eteenpäin** -raportti käyttää sähköistä raportointi- eli ER-kehystä. Käyttömaisuusmallin ja käyttöomaisuuden eteenpäinsiirron määrityksen on tuotava ennen raportin suorittamista Microsoft Dynamics Lifecycle Servicesistä (LCS). Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Raportti on saatavana Microsoft Dynamics 365 Finance, Enterprise editionin versiossa 7.3 tai hotfix-korjauksena Microsoft Dynamics 365 Finance, Enterprise editionin heinäkuun 2017 versiossa. Heinäkuun 2017 versiota käyttävissä ympäristöissä on otettava käyttöön kolme hotfix-korjausta:

- **KB 4041754:** sähköisen raportoinnin (ER) määritystä ei voi ladata LCS:stä, sillä sitä ei voi käyttää nykyisessä versiossa sen jälkeen, kun ympäristön päivityspaketti on otettu käyttöön
- **KB 4056107:** sähköisen raportoinnin (GER) kumulatiivinen päivitys 5
- **KB 4056353:** Käyttöomaisuuden ilmoitusten ja huomautusten raportit eivät vastaa GAAP- ja IFRS-vaatimuksia

Seuraavassa taulussa käsitellään raportissa valittavina olevat kentät.


|                    Kenttä                    |                                                                                                                                kuvaus                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Saldot: alku              |                                                                                           Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä alkupäivämääränä.                                                                                           |
|              Saldot: loppu              |                                                                                            Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä päättymismääränä.                                                                                            |
|         Hankinnat: alkuarvo         |                                                 Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka.                                                  |
|      Hankinnat: kauden hankinnat      |                                                 Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                                                  |
|       Hankinnat: kauden luovutukset        |                                                                        Kaikkien sellaisten kirjattujen hankinnan peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.                                                                        |
|         Hankinnat: loppuarvo         |                                                  Kaikkien <strong>Hankinta</strong>- ja <strong>Hankintaoikaisu</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.                                                   |
|        Poistot: alkuarvo         | Kaikkien <strong>Poisto</strong>-, <strong>Poistojen oikaisu</strong>-, <strong>Erityinen poistovähennys</strong>- ja <strong>Erikoispoisto</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka. |
|     Poistot: kauden poistot     |                         Kaikkien <strong>Poisto</strong>, <strong>Poistojen oikaisu</strong>- ja <strong>Erikoispoisto</strong>--tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                          |
| Poistot: kauden erikoispoistot |                                                              Kaikkien <strong>Erityinen poistovähennys</strong>-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                                                               |
|       Poistot: kauden luovutukset       |                                                                       Kaikkien sellaisten kirjattujen poiston peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.                                                                        |
|        Poistot: loppuarvo         |  Kaikkien <strong>Poisto</strong>-, <strong>Poistojen oikaisu</strong>-, <strong>Erityinen poistovähennys</strong>- ja <strong>Erikoispoisto</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.  |
|    Kirjanpitoarvon korotus/alennus: alkuarvo     |                              Kaikkien <strong>Kirjanpitoarvon korotus</strong>-, <strong>Kirjanpitoarvon alennus</strong>- ja <strong>Uudelleenarvostus</strong>-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka.                               |
|   Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon korotus   |                                                                    Kaikkien <strong>Kirjanpitoarvon korotus</strong> -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                                                                    |
|  Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon alennus  |                                                                   Kaikkien <strong>Kirjanpitoarvon alennus</strong> -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                                                                   |
| Kirjanpitoarvon korotus/alennus: kauden uudelleenarvostukset  |                                                                        Kaikkien <strong>Uudelleenarvostus</strong>-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana.                                                                        |
|   Kirjanpitoarvon korotus/alennus: kauden luovutukset   |                                                           Kaikkien sellaisten kirjattujen kirjanpitoarvon korotuksen, kirjanpitoarvon alennuksen ja uudelleenarvostuksen peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana.                                                           |
|    Kirjanpitoarvon korotus/alennus: loppuarvo     |                               Kaikkien <strong>Kirjanpitoarvon korotus</strong>-, <strong>Kirjanpitoarvon alennus</strong>- ja <strong>Uudelleenarvostus</strong>-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka.                                |
|          Luovutukset: luovutuksen päivämäärä           |                                                                                                                Käyttöomaisuuskirjan luovutuksen päivämäärä.                                                                                                                |
|    Luovutukset: nettokirjanpitoarvon luovutus    |                                                                                                    Käyttöomaisuuskirjan nettokirjanpitoarvo luovutushetkellä.                                                                                                    |
|            Luovutukset: myyntiarvo            |                                                                                               Käyttöomaisuuskirjan luovutuksen myyntiarvo – myyntitapahtuma.                                                                                                |
|           Luovutukset: hävikkiarvo            |                                                                                               Käyttöomaisuuskirjan luovutuksen hävikkiarvo – hävikkitapahtuma.                                                                                               |
|           Luovutukset: tulos            |                                                                                 Käyttöomaisuuskirjan luovutustapahtuman osana lasketun voiton tai tappion arvo.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

