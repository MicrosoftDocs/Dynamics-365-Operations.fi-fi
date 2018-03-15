---
title: "Käyttöomaisuuden eteenpäin siirron raportti"
description: "Tässä ohjeaiheessa käsitellään käyttöomaisuuden eteenpäin siirron raporttia."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7a81697a8e90fb6b0695a02db0868f5708fdbddf
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Käyttöomaisuuden eteenpäin siirron raportti

[!include[banner](../includes/banner.md)]

**Käyttöomaisuuden siirto eteenpäin** -raportti on helposti luettava Microsoft Excel -muotoinen raportti, jossa eritellään kauden sulkemista, tilipäätöksiä ja veroilmoituksia varten tarvittavat käyttöomaisuustiedot. Raportti sisältää käyttöomaisuuden alku- ja loppusaldot sekä kauden arvostuksen muutokset. Lisäksi siinä on kauden aikana tapahtuneet uudet käyttöomaisuuden hankinnat ja luovutukset. Tiedot raportoidaan käyttöomaisuuseräkohtaisesti, ja arvojen yhteenveto on saatavana käyttöomaisuusryhmille ja yritykselle.

**Käyttöomaisuuden siirto eteenpäin** -raportti käyttää sähköistä raportointi- eli ER-kehystä. Käyttömaisuusmallin ja käyttöomaisuuden eteenpäinsiirron määrityksen on tuotava ennen raportin suorittamista Microsoft Dynamics Lifecycle Servicesistä (LCS). Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Raportti on saatavana Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin versiossa 7.3 tai hotfix-korjauksena Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin heinäkuun 2017 versiossa. Heinäkuun 2017 versiota käyttävissä ympäristöissä on otettava käyttöön kolme hotfix-korjausta:

- **KB 4041754:** sähköisen raportoinnin (ER) määritystä ei voi ladata LCS:stä, sillä sitä ei voi käyttää nykyisessä sovellusversiossa sen jälkeen, kun ympäristön päivityspaketti on otettu käyttöön
- **KB 4056107:** sähköisen raportoinnin (GER) kumulatiivinen päivitys 5
- **KB 4056353:** Käyttöomaisuuden ilmoitusten ja huomautusten raportit eivät vastaa GAAP- ja IFRS-vaatimuksia

Seuraavassa taulussa käsitellään raportissa valittavina olevat kentät.

| Kenttä                                       | kuvaus |
|---------------------------------------------|-------------|
| Saldot: alku                           | Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä alkupäivämääränä. |
| Saldot: loppu                           | Käyttöomaisuuden nettokirjanpitoarvo raportissa määritettynä päättymismääränä. |
| Hankinnat: alkuarvo                 | Kaikkien **Hankinta**- ja **Hankintaoikaisu**-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka. |
| Hankinnat: kauden hankinnat           | Kaikkien **Hankinta**- ja **Hankintaoikaisu**-tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Hankinnat: kauden luovutukset              | Kaikkien sellaisten kirjattujen hankinnan peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana. |
| Hankinnat: loppuarvo                 | Kaikkien **Hankinta**- ja **Hankintaoikaisu**-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka. |
| Poistot: alkuarvo                | Kaikkien **Poisto**-, **Poistojen oikaisu**-, **Erityinen poistovähennys**- ja **Erikoispoisto**-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka. |
| Poistot: kauden poistot         | Kaikkien **Poisto**, **Poistojen oikaisu**- ja **Erikoispoisto**--tyyppisten tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Poistot: kauden erikoispoistot | Kaikkien **Erityinen poistovähennys**-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Poistot: kauden luovutukset             | Kaikkien sellaisten kirjattujen poiston peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana. |
| Poistot: loppuarvo                | Kaikkien **Poisto**-, **Poistojen oikaisu**-, **Erityinen poistovähennys**- ja **Erikoispoisto**-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka. |
| Kirjanpitoarvon korotus/alennus: alkuarvo        | Kaikkien **Kirjanpitoarvon korotus**-, **Kirjanpitoarvon alennus**- ja **Uudelleenarvostus**-tyyppisten tapahtumien summa raportissa määritettyyn alkupäivämäärään saakka. |
| Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon korotus     | Kaikkien **Kirjanpitoarvon korotus** -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Kirjanpitoarvon korotus/alennus: kauden kirjanpitoarvon alennus   | Kaikkien **Kirjanpitoarvon alennus** -tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Kirjanpitoarvon korotus/alennus: kauden uudelleenarvostukset  | Kaikkien **Uudelleenarvostus**-tyypin tapahtumien summa, jotka kirjattiin raportin päivämäärävälin aikana. |
| Kirjanpitoarvon korotus/alennus: kauden luovutukset     | Kaikkien sellaisten kirjattujen kirjanpitoarvon korotuksen, kirjanpitoarvon alennuksen ja uudelleenarvostuksen peruutusten summa, joiden luovutustapahtuma oli raportin päivämäärävälin aikana. |
| Kirjanpitoarvon korotus/alennus: loppuarvo        | Kaikkien **Kirjanpitoarvon korotus**-, **Kirjanpitoarvon alennus**- ja **Uudelleenarvostus**-tyyppisten tapahtumien summa raportissa määritettyyn päättymismäärään saakka. |
| Luovutukset: luovutuksen päivämäärä                    | Käyttöomaisuuskirjan luovutuksen päivämäärä. |
| Luovutukset: nettokirjanpitoarvon luovutus       | Käyttöomaisuuskirjan nettokirjanpitoarvo luovutushetkellä. |
| Luovutukset: myyntiarvo                       | Käyttöomaisuuskirjan luovutuksen myyntiarvo – myyntitapahtuma. |
| Luovutukset: hävikkiarvo                      | Käyttöomaisuuskirjan luovutuksen hävikkiarvo – hävikkitapahtuma. |
| Luovutukset: tulos                      | Käyttöomaisuuskirjan luovutustapahtuman osana lasketun voiton tai tappion arvo. |

