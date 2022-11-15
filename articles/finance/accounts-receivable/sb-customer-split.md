---
title: Asiakkaan jako laskutusaikatauluissa
description: Tässä artikkelissa kuvataan, kuinka asiakas jaetaan tilauslaskutusta käytettäessä.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746312"
---
# <a name="customer-split-on-billing-schedules"></a>Asiakkaan jako laskutusaikatauluissa

Laskutusaikataulun *laskutustili* on asiakas, joka vastaanottaa ja maksaa myyntitilauslaskun. Joissakin tilanteissa laskun voi maksaa useampi kuin yksi asiakas. **Asiakkaan jako** -ominaisuuden avulla voit lisätä asiakkaita, joita voidaan laskuttaa samasta laskutusaikataulusta. Jos haluat ottaa tämän toiminnon käyttöön, siirry kohtaan **Tilauslaskutus \> Toistuvan sopimuksen laskutus \> Asetukset \> Toistuvan sopimuksen laskutusparametrit** ja määritä **Asiakkaan jako** -vaihtoehdoksi **Kyllä**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Asiakkaan jako laskutusaikataulun otsikossa

Kun laskutusaikataulu on luotu, voit lisätä enemmän asiakkaita laskutusaikataulun otsikkoon.

Lisää asiakas noudattamalla seuraavia ohjeita.

1. Valitse **Laskutusaikataulu**-välilehdestä **Asiakkaan jako**. Ylälaidassa olevat **Asiakastili**- ja **Asiakastilin nimi** -kentät määrittävät asiakkaan, joka delegoidaan **laskutusaikataulun asiakkaaksi**.

    > [!NOTE]
    > Lisäämäsi asiakastili ei voi olla sama kuin laskutustili.

2. Valitse **Asiakkaan jaon rivit** -välilehdestä **Lisää rivi**.
3. Valitse asiakas ja syötä sitten asiakkaan prosenttiosuus kustakin laskusta.
4. Alkamis- ja päättymispäivinä käytetään oletusarvoisesti laskutusaikataulun alkamis- ja päättymispäiviä. Syötä eri alkamis- ja päättymispäivät, jos uusi asiakas maksaa laskutusaikataulusta vain määritetyn prosenttiosuuden. Jos laskutusaikataulun alkamispäivä on esimerkiksi 1. tammikuuta ja päättymispäivä 31. joulukuuta ja uutta asiakasta laskutetaan 40 prosenttia ensimmäiseltä yhdeksältä kuukaudelta, määritä alkamispäiväksi 1. tammikuuta, päättymispäiväksi 30. syyskuuta ja prosenttiosuudeksi **40,00**.

Voit lisätä asiakkaan jaon riveillä useamman kuin yhden asiakkaan. Tällöin määritetty kokonaisprosentti ei voi ylittää 100 prosenttia. Määritä asiakasviite ja asiakkaan tilausnumero tietokentiksi, jotka näytetään myyntitilausrivillä **Luo lasku** -prosessin aikana.

Rivin tiedoissa näytetään myös lisättyjen asiakkaiden yhteystiedot, toimitusosoite, laskutusosoite ja maksutiedot. Nämä tiedot näytetään myös asiakkaiden myyntitilauksessa.

Kun lisäät asiakkaan jaon tietoja laskutusaikataulun otsikkoon ja laskutusaikataulussa on laskuttamattomia laskutusaikataulurivejä, näet seuraavan viestin, joka kehottaa sinua siirtämään muutokset: "Haluatko siirtää muutoksen otsikosta riveille? Muutoksilla päivitetään vain ne laskutusaikataulun rivit, joita ei ole laskutettu." Valitse **Kyllä** päivittääksesi asiakkaan jaon tiedot laskutusaikataulun rivillä. Muutoksia ei päivitetä, jos laskutusaikataulun rivi on jo laskutettu.

Jos laskutusaikataulu on luotu **Kopioi aikataulu** -vaihtoehdon avulla, asiakkaan jaon otsikon riveille syötetään oletustiedot. Se ei voi olla sama kuin asiakastili.

Kun **Luo lasku** -prosessi on suoritettu, järjestelmä luo useita myyntitilauksia. (Järjestelmä luo useita myyntilaskuja myös, jos automaattinen kirjaus on käytössä). Näitä myyntitilauksia ja myyntilaskuja voidaan tarkastella **Näytä laskutustiedot** -sivun **Rivin tiedot** -pikavälilehden **Lasku**-välilehdessä. Laskutustietojen rivillä lukee **Useita** merkkinä siitä, että useita myyntitilauksia ja myyntilaskuja luotiin.

## <a name="customer-split-on-billing-schedule-lines"></a>Asiakkaan jako laskutusaikataulun riveillä

Asiakkaan jako voidaan lisätä yksittäisille laskutusaikataulun riveille, jos haluat jakaa vain tietyt laskutusaikataulun rivit. Valitse riviltä **Asiakkaan jako** -valintaruutu ja valitse sitten laskutusaikataulun rivin valikosta **Asiakkaan jako** päivittääksesi tai syöttääksesi asiakkaan jaon tiedot.

Kirjaustiedot päivitetään, jos laskutusaikataulu on jo laskutettu, mutta laskutusaikataulun rivin prosenttiarvoa on muutettu sen jälkeen. Kaikki muutoksen jälkeen laskutetut rivit käyttävät uutta prosenttiosuutta.

> [!NOTE]
> - Asiakkaan jaon vaihtoehtoa ei voi käyttää varastoitavien tuotteiden kanssa.
> - Jos **Laskuttamaton tuotto** -valintaruutu on valittuna, **Asiakkaan jako** -valintaruutua ei voi valita.
> - Jos käytät **Vain tuoton jako** -vaihtoehtoa, päärivillä on **Asiakkaan jako** -vaihtoehto, mutta alitason rivinimikkeillä ei.
