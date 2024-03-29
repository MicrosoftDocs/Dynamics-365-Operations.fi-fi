---
title: Bonuspoisto
description: Tämä artikkeli sisältää bonuspoiston toimintojen yleiskatsauksen.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: kfend
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 801747f06d16e70cd04b727787f0bfa6b6baefc0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711142"
---
# <a name="bonus-depreciation"></a>Bonuspoisto

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää bonuspoiston toimintojen yleiskatsauksen.

Bonuspoisto mahdollistaa ylimääräiset poistosummat sinä vuonna, jolloin käyttöomaisuus otetaan käyttöön ja siitä tehdään poisto ensimmäistä kertaa. Bonuspoisto on suoritettava ennen muiden poistojen laskemista. Näin kannattaa käyttää bonuspoistoa kirjoissa, joissa Kirjaa kirjanpitoon -toiminto on poistettu käytöstä. Voit käyttää **Poista kirjanpitoon kirjaamattomat tapahtumat** ja poistaa aiempia tapahtumia kirjoista, joita ei kirjata kirjanpitoon. Bonuspoisto voidaan sisällyttää myöhemmin käyttöomaisuuserän elinkaareen poistamalla aiemmin kirjattuja poistotapahtumia. 

Bonuspoisto voidaan laskea ehdotusprosessia käyttäen tai luomalla manuaalisia bonuspoistotapahtumia. Bonuspoistotapahtumia ei voi luoda, jos kyseisessä käyttöomaisuuskirjassa on jo poistotapahtumia tai poistojen oikaisutapahtumia.

Kun lasket bonuspoiston ehdotusprosessin avulla, kaikki olemassa olevat bonustapahtumat sisältyvät perustan laskentaan. Laskenta sisältää myös aiemmat käyttöomaisuudelle manuaalisesti kirjatut bonuspoistot. 

Jos käyttöomaisuuserälle tehdään useita bonuspoistoja, myös prioriteetti otetaan huomioon. Jokainen bonus vähentää seuraavan bonuksen perustaa. Bonuspoiston laskennassa käytetyssä käyttöomaisuuden perustassa ei oteta huomioon jäännösarvoa eikä bonuspoistoon sovelleta poistomenetelmää. 

Yhdysvalloissa jotkut omaisuustyypit voidaan katsoa tällä hetkellä Section 179 -omaisuudeksi. Section 179 -vähennystä käyttämällä omaisuuden koko tai osittainen arvo voidaan saada takaisin tiettyyn rajaan asti. Arvon voi saada takaisin vähentämällä se sinä vuonna, jolloin omaisuus otettiin käyttöön.

## <a name="example"></a>Esimerkki
Oletetaan, että käyttöomaisuuden poistokirjaan liittyvät seuraavat bonuspoistot:

-   **Osa 179:** 1 000,00, Prioriteetti 1
-   **Liberty Zone-poisto:** 30 prosenttia, prioriteetti 2

Omaisuuden hankintahinta on 5 000. Kun bonuspoisto lasketaan, ensimmäinen bonuspoistosumma on Osa 179 -poisto 1 000. 

Seuraava bonuspoistosumma, Liberty Zone -poisto, lasketaan seuraavasti: 

Hankintahinta - 1 000 (Osa 179 -poisto) x 30 % = 1 200 

Jos bonuspoistosumma on suurempi kuin jäljelle jäävä hankintahinta, bonuspoistosummaksi tulee joko laskettu bonuspoiston tulos tai jäljelle jäävä hankintahinta sen mukaan, kumpi summa on pienempi. 

Jos jäljelle jäävä hankintahinta on 0 (nolla) tai pienempi, bonuspoistotapahtumia ei luoda. 

Kun bonuspoisto lasketaan ehdotusprosessia käyttäen, luodaan kaikille poistokirjaan kuuluville soveltuville bonuspoistotietueille bonuspoistotapahtuma. 

Bonuspoistotietueita voidaan luoda rajaton määrä. Kun tietueet on määritetty käyttöomaisuusryhmän kirjaan, niitä käytetään käyttöomaisuuserän poistokirjassa. 

Bonuspoisto ilmoitetaan joko prosenttina tai kiinteänä summana. Kun kirjataan poistoehdotuksia, bonuspoistotapahtumat kirjataan kirjaan poistotapahtumista erillisinä tapahtumina.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
