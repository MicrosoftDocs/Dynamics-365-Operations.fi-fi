---
title: Maksutavat
description: "Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä artikkelissa kuvataan määritettävissä olevat maksutyypit ja niiden määrittämisessä vaadittava prosessi."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b9570efe8b90dc6402fef67cf7838e5d8546cf02
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="payment-methods"></a>Maksutavat

[!include[banner](includes/banner.md)]


Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä artikkelissa kuvataan määritettävissä olevat maksutyypit ja niiden määrittämisessä vaadittava prosessi.

Vähittäismyyjät voivat hyväksyä useantyyppisiä maksutapoja myymistään tuotteista ja palveluista. Käteinen on yleisin maksutapa, mutta vähittäismyyjät voivat myös vastaanottaa maksuja sekkeinä, maksukorteilla, lahjakorteilla ja niin edelleen. Kunkin jälleenmyyjän hyväksymä maksutapa on määritettävä Microsoft Dynamics 365 for Retailin määrityksen yhteydessä. Seuraavassa taulukossa kuvaillaan kaikki maksutavat, jotka ovat määritettävissä Microsoft Dynamics 365 for Retailissa:

-   **Käteinen** – Valuutan fyysisessä muodossa oleva raha, kuten setelit ja kolikot. Tämä valuutta voi olla joko yrityksen valuutta tai myymälän paikallinen valuutta.
-   **Sekki** – Siirrettävissä oleva maksuväline, jonka mukaan tiettynä valuuttana maksetaan tietty summa määritetystä pankista. Sekki on yleensä voimassa rajattoman ajan tai kuusi kuukautta sen antopäivämäärästä, ellei toisin ole määritetty. Voimassaoloaika vaihtelee sekin maksavasta pankista riippuen. Erilaisia sekkityyppejä ovat esimerkiksi määrännäissekit, avoimet sekit, haltijasekit ja sekä sekit, joita ei voida siirtää toiselle. Voit määrittää sekit maksutavaksi kullekin myymälälle erikseen. Sekit voi hyväksyä valuuttana, joka määritetään joko yritystasolla tai myymälän tasolla. Sekit on määritettävä maksutavaksi ennen kuin myymälä voi vastaanottaa maksuja sekkeinä.
-   **Valuutta** – Ensisijainen muu maksuväline kuin yrityksen oletusvaluutta. Kolikot ja setelit ovat valuutan muotoja. Valuutan maksutapaa edustaa kaikkia käytettäviä valuuttoja. Ennen tämän maksutavan käyttöönottoa on määritettävä valuutat sekä vähittäismyynnin valuuttojen vaihtokurssitiedot.
-   **Kortti** – Kaikki käytettävät kortit, kuten pankki- ja luottokortit. Suosittelemme, että määrität yhden korttimaksutavan organisaatiotasolla, joka edustaa kaikkia korttityyppejä. Voit sitten määrittää maksutavan kussakin myymälässä kullekin kortille tai korttijoukolle, jota käsitellään käyttäen samoja asetuksia. Jotta voit hyväksyä korttimaksuja kaupassa, sinun on määritettävä markkinoilla saatavilla olevat eri valmistajien pankki- ja luottokortit.
-   **Hyvityslasku** – Hyvityslaskut, jotka annetaan tai hyvitetään myyntipisteessä. Hyvityslasku voi olla joko hyvitys tai palautuslasku, joka annetaan palautetulle myynnille. Jos hyvityslaskut hyvitetään vain osittain, ohjelma myöntää uudella numerolla uuden hyvityslaskun jäljelle jäävästä saldosummasta. Uudella hyvityslaskulla on uusi numero. Hyvityslaskua voi käyttää vain kerran, ja järjestelmä pitää yllä tietuetta kaikista käytetyistä numeroista. Tietuetta voi tarkastella **Hyvityslaskutaulukko**-sivulla. Asiakas ei voi lunastaa hyvityslaskun arvoa suurempaa summaa.
-   **Lahjakortti** – Lahjakortit, jotka myönnetään ja hyvitetään myyntipisteessä. Liikamaksu ei ole sallittu lahjakorteissa.
-   **Asiakastili** – Maksuja, jotka voidaan veloittaa myyntiajankohtana kassakoneelta asiakastilille. Tämän maksutavan avulla voit kerätä myyntitietoja tai asiakaskohtaisia alennuksia, kun asiakas tekee maksuja toista maksutapaa käyttäen. Tätä varten on määritettävä asiakaskohtaiset tiedot.
-   **Kanta-asiakkuuspisteet** – Pisteitä, joita asiakkaat kerryttävät osana kanta-asiakasohjelmaa. Jos luot kanta-asiakasohjelmia, asiakkaat voivat ansaita pisteitä ja saada niistä hyvityksen useilla tavoilla. Joissain kanta-asiakasohjelmissa asiakkaat voivat esimerkiksi lunastaa kanta-asiakaspisteensä alennuksen muodossa tai jopa käyttää niitä maksamiseen.

Maksutapojen määrittämistä varten on suoritettava seuraavat tehtävät:

1.  Aseta maksutavat organisaatiolle. Luo maksutavat, jotka hyväksytään koko organisaatiossa.
2.  Organisaation laajuisten korttityyppien ja korttien numeroiden luominen. Jos luottokortit tai pankkikortit hyväksytään, luo ensin yksi korttimaksuvälinetyyppi ja luo sitten organisaation laajuiset korttityypit ja korttien numerot.
3.  Myymälän maksutavan määrittäminen. Liitä maksutavat kuhunkin myymälään ja määritä sitten myymäläkohtaiset asetukset kullekin myymälän maksutavalle.
4.  Aseta liikkeille korttimaksutavat. Suorita korttimaksujen määritys loppuun kaikille korttimaksutavoille, jotka hyväksyt liikkeessä.




