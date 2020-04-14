---
title: Määritä arvonlisäverokoodit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit Dynamics 365 Financeissa.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144740"
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

