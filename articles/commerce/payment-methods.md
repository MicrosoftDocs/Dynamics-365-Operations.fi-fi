---
title: Maksutavat
description: Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä artikkelissa kuvataan määritettävissä olevat maksutyypit ja niiden määrittämisessä vaadittava prosessi.
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: d16cdf237042471d367adb7081bf34e9c8a9460f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272819"
---
# <a name="payment-methods"></a>Maksutavat

[!include [banner](includes/banner.md)]

Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä artikkelissa kuvataan määritettävissä olevat maksutyypit ja niiden määrittämisessä vaadittava prosessi.

Vähittäismyyjät voivat hyväksyä useantyyppisiä maksutapoja myymistään tuotteista ja palveluista. Käteinen on yleisin maksutapa, mutta vähittäismyyjät voivat myös vastaanottaa maksuja sekkeinä, maksukorteilla, lahjakorteilla ja niin edelleen. Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä Dynamics 365 Commercessa, kun järjestelmä määritetään. Seuraavassa taulukossa kuvaillaan kaikki maksutavat, jotka ovat määritettävissä:

- **Käteinen** – Valuutan fyysisessä muodossa oleva raha, kuten setelit ja kolikot. Tämä valuutta voi olla joko yrityksen valuutta tai myymälän paikallinen valuutta.
- **Sekki** – Siirrettävissä oleva maksuväline, jonka mukaan tiettynä valuuttana maksetaan tietty summa määritetystä pankista. Sekki on yleensä voimassa rajattoman ajan tai kuusi kuukautta sen antopäivämäärästä, ellei toisin ole määritetty. Voimassaoloaika vaihtelee sekin maksavasta pankista riippuen. Erilaisia sekkityyppejä ovat esimerkiksi määrännäissekit, avoimet sekit, haltijasekit ja sekä sekit, joita ei voida siirtää toiselle. Voit määrittää sekit maksutavaksi kullekin myymälälle erikseen. Sekit voi hyväksyä valuuttana, joka määritetään joko yritystasolla tai myymälän tasolla. Sekit on määritettävä maksutavaksi ennen kuin myymälä voi vastaanottaa maksuja sekkeinä.
- **Valuutta** – Ensisijainen muu maksuväline kuin yrityksen oletusvaluutta. Kolikot ja setelit ovat valuutan muotoja. Valuutan maksutapaa edustaa kaikkia käytettäviä valuuttoja. Ennen tämän maksutavan käyttöönottoa on määritettävä valuutat sekä valuuttojen vaihtokurssitiedot.
- **Kortti** – Kaikki käytettävät kortit, kuten pankki- ja luottokortit. Suosittelemme, että määrität yhden korttimaksutavan organisaatiotasolla, joka edustaa kaikkia korttityyppejä. Voit sitten määrittää maksutavan kussakin myymälässä kullekin kortille tai korttijoukolle, jota käsitellään käyttäen samoja asetuksia. Jotta voit hyväksyä korttimaksuja kaupassa, sinun on määritettävä markkinoilla saatavilla olevat eri valmistajien pankki- ja luottokortit.
- **Hyvityslasku** – Hyvityslaskut, jotka annetaan tai hyvitetään myyntipisteessä. Hyvityslasku voi olla joko hyvitys tai palautuslasku, joka annetaan palautetulle myynnille. Jos hyvityslaskut hyvitetään vain osittain, ohjelma myöntää uudella numerolla uuden hyvityslaskun jäljelle jäävästä saldosummasta. Uudella hyvityslaskulla on uusi numero. Hyvityslaskua voi käyttää vain kerran, ja järjestelmä pitää yllä tietuetta kaikista käytetyistä numeroista. Tietuetta voi tarkastella **Hyvityslaskutaulukko**-sivulla. Asiakas ei voi lunastaa hyvityslaskun arvoa suurempaa summaa.
- **Lahjakortti** – Lahjakortit, jotka myönnetään ja hyvitetään myyntipisteessä. Liikamaksu ei ole sallittu lahjakorteissa. Kaikissa lahjakorteissa on oltava korttinumeroiden yhdistämismääritykset. 
- **Asiakastili** – Maksuja, jotka voidaan veloittaa myyntiajankohtana kassakoneelta asiakastilille. Tämän maksutavan avulla voit kerätä myyntitietoja tai asiakaskohtaisia alennuksia, kun asiakas tekee maksuja toista maksutapaa käyttäen. Tätä varten on määritettävä asiakaskohtaiset tiedot.
- **Kanta-asiakkuuspisteet** – Pisteitä, joita asiakkaat kerryttävät osana kanta-asiakasohjelmaa. Jos luot kanta-asiakasohjelmia, asiakkaat voivat ansaita pisteitä ja saada niistä hyvityksen useilla tavoilla. Joissain kanta-asiakasohjelmissa asiakkaat voivat esimerkiksi lunastaa kanta-asiakaspisteensä alennuksen muodossa tai jopa käyttää niitä maksamiseen.

Maksutapojen määrittämistä varten on suoritettava seuraavat tehtävät:

1. Aseta maksutavat organisaatiolle. Luo maksutavat, jotka hyväksytään koko organisaatiossa.
2. Organisaation laajuisten korttityyppien ja korttien numeroiden luominen. Jos luottokortit tai pankkikortit hyväksytään, luo ensin yksi korttimaksuvälinetyyppi ja luo sitten organisaation laajuiset korttityypit ja korttien numerot.
3. Myymälän maksutavan määrittäminen. Liitä maksutavat kuhunkin myymälään ja määritä sitten myymäläkohtaiset asetukset kullekin myymälän maksutavalle.
4. Aseta liikkeille korttimaksutavat. Suorita korttimaksujen määritys loppuun kaikille korttimaksutavoille, jotka hyväksyt liikkeessä.

## <a name="handle-change-tendering-for-payment-methods"></a>Vaihtorahan maksuvälineen käsitteleminen maksutavoissa

Jotkin maksutavat eivät tue suoraa vaihtorahan maksuvälinetapahtumaa, jos asiakkaille on maksettava vaihtorahaa myyntipistetapahtuman aikana. Vaihtorahan maksuvälineenä voi käyttää vain **Käteinen**- ja **Valuutta**-maksutapoja. 

Sellaisia tilanteita varten, joissa vaihtorahan maksuvälinetapahtumaa tarvitaan tapahtuman aikana mutta maksutapa ei tue sitä, voidaan määrittää **Vaihtorahan maksuväline** -maksutapa. Käytettävä maksutapa valitaan, kun myymälän maksutapoja määritetään. Anna sen jälkeen **Vaihtoraha**-osan **Vaihtorahan maksuväline** -kentässä vaihtorahan maksuvälinemaksun vaihtoehto. Esimerkiksi **1** voidaan antaa ilmaisemaan, että käteistä voidaan käyttää vaihtorahan maksuvälinemaksun vaihtoehtona.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
