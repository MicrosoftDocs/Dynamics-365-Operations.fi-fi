---
title: Takuukirje
description: "Tässä artikkelissa on tietoja takausasiakirjoista. Takausasiakirjan avulla pankki suostuu maksamaan tietyn summan henkilölle, jos pankin asiakas laiminlyö maksun tai sitoumuksen suorittamisen saajalle."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: d7144a979b98b3dbd2052661945e6d4fe22220a7
ms.contentlocale: fi-fi
ms.lasthandoff: 08/09/2017

---

# <a name="letters-of-guarantee"></a>Takuukirje

[!include[banner](../includes/banner.md)]


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


