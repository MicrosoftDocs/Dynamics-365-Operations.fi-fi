---
title: Määritä arvonlisäverokoodit
description: Tässä artikkelissa kuvataan, kuinka voit määrittää arvonlisäverokoodit Dynamics 365 Financessa.
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
ms.openlocfilehash: b12133583f40cc17cb85f6dbd86697592af25caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858465"
---
# <a name="set-up-sales-tax-codes"></a>Määritä arvonlisäverokoodit

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit määrittää arvonlisäverokoodit. Arvonlisäverokoodit luodaan jokaiselle epäsuoralle verolle tai tullimaksulle, jonka yritys on velvollinen laskemaan, perimään ja maksamaan veroviranomaisille.

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
