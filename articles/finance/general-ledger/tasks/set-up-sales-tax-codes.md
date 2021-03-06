---
title: Määritä arvonlisäverokoodit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit Dynamics 365 Financessa.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c7208fa65905fcc902d9c08b5b90178745e76d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815041"
---
# <a name="set-up-sales-tax-codes"></a>Määritä arvonlisäverokoodit

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit. Arvonlisäverokoodit luodaan jokaiselle epäsuoralle verolle tai tullimaksulle, jonka yritys on velvollinen laskemaan, perimään ja maksamaan veroviranomaisille.

Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Vero > Välilliset verot > Arvonlisävero > Arvonlisäverokoodit**.
2. Valitse **Uusi**.
3. Kirjoita **Arvonlisäverokoodi**-kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **tilityskausi** avaamalla avattava luettelo, kun haluat määrittää, arvonlisäveroviranomaiset, joille arvonlisävero ilmoitetaan ja maksetaan sekä ilmoitus- ja maksuvälit.
6. Valitse **kirjanpidon kirjausryhmä**, kun haluat määrittää päätilit arvonlisäveron kirjanpitoon kirjaamista varten.
7. Laajenna **Laskenta**-pikavälilehti. Se sisältää useita kenttiä, jotka ohjaavat arvonlisäverosummien laskentaa. Täytä nämä kentät tarpeen mukaan.  
8. Valitse käyttöliittymän yläosan **toimintoruudussa** **Arvonlisäverokoodi**.
9. Valitse **Arvot**.
10. Kirjoita tämän verokoodin arvo **Arvo**-sarakkeeseen.
    - Jos Summa Alkuperäinen-kentän Yksikkökohtainen summa -kohta on valittu, **Laskenta**-pikavälilehdessä arvo kerrotaan tapahtuman määrällä, kun arvonlisäverosumma lasketaan.  Jos verokoodi ei ole yksikköperusteinen vero, arvo esitetään prosenttiosuutena, joka kohdistetaan tämän verokoodin alkuperään arvonlisäverosumman laskemiseksi.     
11. Valitse **Tallenna**.
12. Sulje sivu.
13. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]