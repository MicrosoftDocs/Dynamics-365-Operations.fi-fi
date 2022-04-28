---
title: Määritä arvonlisäverokoodit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit Dynamics 365 Financessa.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565850"
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

    Jos **Yksikkökohtainen summa** -kohta on valittu, arvolisävero laskentaan kertomalla **Laskenta**-pikavälilehden **Alkuperä**-kentän arvo tapahtuman määrällä.  Jos verokoodi ei ole yksikköperusteinen vero, arvo ilmaistaan prosenttiosuutena, joka kohdistetaan tämän verokoodin alkuperään arvonlisäverosumman laskemiseksi.     

11. Valitse **Tallenna**.
12. Sulje sivu.
13. Valitse **Tallenna**.

Jos Microsoft Dynamics 365 Financen versiosta 10.0.22 alkaen käytössä on [Veropalvelu](../../localizations/global-tax-calcuation-service-overview.md) ja [**Tue useita ALV-rekisteröintinumeroita**](../../localizations/emea-multiple-vat-registration-numbers.md) -ominaisuus on otettu käyttöön **Ominaisuuksien hallinta** -työtilassa, verokoodin tyyppi voidaan määrittää **Veron tyyppi** -kentässä. Käytettävissä ovat seuraavat arvot:

- Normaali arvonlisäverotus
- Alennettu arvonlisäverotus
- ALV 0 %
- Valmiste
- Muu

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
