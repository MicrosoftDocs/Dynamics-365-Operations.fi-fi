---
title: Takuukirje
description: Tässä artikkelissa on tietoja takausasiakirjoista. Takausasiakirjan avulla pankki suostuu maksamaan tietyn summan henkilölle, jos pankin asiakas laiminlyö maksun tai sitoumuksen suorittamisen saajalle.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: kfend
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24db7e23ec6d360bbae7113e62bb28d4aecd851f
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715337"
---
# <a name="letters-of-guarantee"></a>Takuukirje

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja takausasiakirjoista. Takausasiakirjan avulla pankki suostuu maksamaan tietyn summan henkilölle, jos pankin asiakas laiminlyö maksun tai sitoumuksen suorittamisen saajalle. 

Takauskirja on pankin (takaaja) keino maksaa sovittu rahasumma toiselle henkilölle (saaja), jos pankin asiakas (päävelallinen) laiminlyö maksun tai sitoumuksen suorittamisen saajalle. Takauskirjoja ei voi siirtää. Ne koskevat ainoastaan sopimuksessa mainittua edunsaajaa. Päävelallinen voi pyytää takausasiakirjan arvon suurentamista tai pienentämistä sopimuksen ehtojen mukaisesti. 

Jos edunsaaja haluaa realisoida takauskirjan, hänen on lähetettävä alkuperäinen takausasiakirja ja ilmoitettava pankille päämiehen maksukyvyttömyydestä ennen erääntymispäivää. Pankki maksaa sitten edunsaajan tilille erääntyvän summan takauskirjan ehtojen mukaisesti. Pankki ottaa maksusta prosenttiosuuden katteena. Prosenttiosuus sovitaan ja määritetään sopimuksen ehdoissa. 

Voit luoda takauskirjan tarkoitusta seuraavan koodin. Voit myös määrittää syyt, jotka liitetään takauskirjaan sen peruutuksen yhteydessä. Voit tarkastella tarkoituskoodeja ja pankin syitä **Maksun tarkoituskoodit**- ja **Pankin syyt** -sivulla. 

**Takausasiakirja**-sivulla voit suorittaa seuraavat tehtävät:

-   Luo oikeat kirjanpitomerkinnät ja poista manuaalinen merkintä.
-   Kirjaa kaikki raha- ja tietotapahtumat ja seuraa takausasiakirjojen saldoja.
-   Kirjaa takausasiakirjojen tilat ja vanheneminen ja seuraa niitä.
-   Luo raportti, joka sisältää takausasiakirjat säilyttävien pankkien luettelon.

Seuraava taulukko sisältää toiminnot, jotka takausasiakirjalle voidaan suorittaa.

| Toiminto              | Tarkoitus                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Lähetä pankille      | Lähetä pankille takausasiakirjapyyntö                                                                       |
| Vastaanota pankilta   | Kun pankki hyväksyy lähetetyn pyynnön, voit noutaa takausasiakirjan pankista.                            |
| Anna edunsaajalle | Kun saat takausasiakirjan pankista, anna se edunsaajalle.              |
| Kasvata arvoa      | Edunsaajan ja päävelallisen suostumuksella voit suurentaa rahamääräistä arvoa.                                                  |
| Pienennä arvoa      | Edunsaajan ja päävelallisen suostumuksella voit pienentää rahamääräistä arvoa.                                                  |
| Laajenna              | Kun takausasiakirja on annettu edunsaajalle, voit pidentää voimassaoloaikaa, jos pidennys on mahdollinen. |
| Peruuta              | Kun tarkoitusta, johon takausasiakirja pyydettiin, ei enää ole, voit peruuttaa sopimuksen.                  |
| Realisoi           | Kun edunsaaja esittää takausasiakirjan pankille, takausasiakirja maksetaan käteisellä.                      |


Lisätietoja on seuraavissa aiheissa:

[Takausasiakirjan tapahtuma](tasks/letter-guarantee-transaction.md)

[Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
