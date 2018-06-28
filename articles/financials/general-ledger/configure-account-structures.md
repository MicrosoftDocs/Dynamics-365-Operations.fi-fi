---
title: "Määritä tilirakenteet"
description: "Tässä aiheessa on tietoja tilirakenteista ja taloushallinnon dimensioista."
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.contentlocale: fi-fi
ms.lasthandoff: 05/21/2018

---

# <a name="configure-account-structures"></a>Määritä tilirakenteet

[!include[banner](../includes/banner.md)]

Tilirakenteet käyttävät päätiliä ja taloushallinnon dimensioita luodakseen sääntöjä, jotka määrittävät järjestyksen ja arvot määrittäessäsi tilinumeron. Voit määrittää niin monta tilirakennetta kuin on tarpeen yrityksesi kannalta. Tilirakenteet määritetään yrityksen kirjausasetuksiin, jotta ne voidaan jakaa.

Tilirakennetta luotaessa segmenttien enimmäismäärä on 11. Jos tarvitset enemmän segmenttejä, arvioi huolellisesti asetukset ja vaatimukset, koska se vaikuttaa käyttökokemukseen. Harkitse, jos segmentti voidaan johtaa käyttämällä hierarkiaa tietojen syöttöhetken sijaan tai käyttämällä käyttäjän määrittämää kenttää. Esimerkiksi jos haluat raportoida sijainnista, mutta voit määrittää sijainnin kustannuspaikan tai osaston mukaan, et tarvitse siajintia taloushallinnon dimensioksi. Jos arvioinnin jälkeen, että tarvitse enemmän kuin 11 segmenttiä, voit lisätä uusia segmenttejä lisäsääntöjen avulla.

Tilirakenteet edellyttävät päätilin. Päätilin ei tarvitse olla rakenteen ensimmäinen segmentti, mutta se yksilöi, mitä tilirakennetta käytetään syötettäessä tilinumeroa. Näin ollen päätilin arvo voi olla vain yhdessä kirjanpitoon määritetyssä rakenteessa, jotta ne eivät ole päällekkäiset. Tilirakenteen tunnistuksen jälkeen suodatetaan sallittujen arvojen luettelo ohjatakseen käyttäjää valitsemaan vain voimassa olevia dimensioarvoja, näin vähentäen kirjauskansion virheellisen kirjauksen mahdollisuutta.

> [!NOTE] 
> Jos aiot budjetoida taloushallinnon dimension mukaan, sen on kuuluttava tilirakenteeseen. Budjetointi ei tällä hetkellä käytä lisäsääntöjä.

## <a name="example"></a>Esimerkki
Kuvataksemme tilirakenteen määrittämisen parhaita käytäntöjä, oletetaan, että yritys haluaa seurata tasetilejänsä (100000..399999) tasolla tilin ja liiketoimintayksikön taloushallinnon dimension tasolla. Tuotto-ja kulutileissä (400000..999999) he seuraavat taloushallinnon dimensioita Liiketoimintayksikkö, Osasto ja Kustannuspaikka. Jos he myyvät, he myös haluavat seurata kohdetta Asiakas. Käyttämällä tätä skenaariota on suositeltavaa käyttää kahta tilirakennetta, jotka on määritetty yrityksen kirjanpitoon - yksi tasetileille ja toinen tulos- ja tappiotileille. Käyttäjäkokemuksen ja oikeellisuustarkistuksen optimoimiseksi Asiakas tulisi olla lisäsääntö, jota käytetään vain, kun myynnin tiliä käytetään.

**Tasetilirakenne**

|Päätili          | Liiketoimintayksikkö    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Voitt- ja tappiotilirakenne**

|Päätili          | Liiketoimintayksikkö    |Osasto          | Kustannuspaikka    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Lisäsääntö asiakkaan lisäämiseksi**

Ehto: Kun Päätili on välillä 400000–499999, lisää asiakas. Tätä ei voi jättää tyhjäksi.

|Asiakas         |
|-----------------|
|* |

Tässä yksinkertaistetussa esimerkissä kaikki arvot ja tyhjät sallitaan - siksi käytetään merkkejä * ja ” ”.

## <a name="segments-and-allowed-values"></a>Segmentit ja sallitut arvot
**Segmentit**- ja **Sallitun arvon tiedot**-osa sisältää ruudukon kaltaisen kokemuksen lisäämään sääntöjä, joita noudatetaan tarkistuksessa kirjauksen aikana. Voit kirjoittaa suoraan soluihin ruudukossa, tuoda sen Excelistä tai käyttää **Sallitun arvon tiedot** -osaa prosessin opastuksena.

**Sallitun arvon tiedot** -osa ohjaa, kun luot ehtoja käyttäen **operaattoreita**, kuten alkaa merkillä, on välillä, sisältää ja monia muita.

[![Salli arvot](./media/account.png)](./media/account.png) 

## <a name="more-than-7-criteria-needed"></a>Tarvitaan yli 7 ehtoa

Jos tarvitset yli 7 ehtoa, voit jatkaa lisäämällä niitä seuraavalla rivillä. Huomaat, kun käytät **Sallitun arvon tiedot** -osaa, että **+Lisää uusi** -ehto ei ole enää aktiivinen seitsemännen ehdon syöttämisen jälkeen. Tämä johtuu monista tekijöistä, esimerkiksi: 
 - Sarakkeen leveys 
 - Miten tiedot on tallennettu 
 - **Sallitun arvon tiedot** -ohjausobjektin tehokkuudesta
 - Käyettävyydestä  
 
Jatkaaksesi lisäehtojen lisäämistä, valitse **Monista segmentissä** ja **Sallitut arvot -osa**. Ehdot kopioidaan uudelle riville. Voit kirjoittaa päälle tai muokata **Sallitun arvon tiedot** -osaa.

(LINKKI VIDEOON, JOKA LUODAAN)

## <a name="best-practices"></a>Parhaat käytännöt
Määrittäessäsi tilirakenteita on suositeltavia parhaita käytäntöjä. Kuitenkin nämä ovat vain ohjeita, joten kokonaisvaltainen keskustelu liiketoiminnastasi, kasvusuunnitelmasta ja huoltosuunnitelmasta tulisi olla osa tätä keskustelua.

- Tee päätilistä ensimmäinen tai tilirakenteen mahdollisimman alussa, jotta käyttäjät saavat parhaimman ohjatun kokemuksen tilille syötettäessä.

- Käytä tilirakenteita mahdollisimman paljon uudelleen vähentääksesi ylläpitoa yritystesi välillä.

- Eri yritysten vaihteluissa harkitse lisäsääntöjä siten, että tilirakenteita voidaan käyttää uudelleen.

- Kun määrität sallittuja arvoja,käytä arvoalueita ja yleismerkkejä mahdollisimman paljon. Paitsi että näin yritys voi kasvaa ja muuttua ilman ylläpitoa, myös järjestelmä suorittaa paremmin tällä kokoonpanolla.

- Älä aseta tilirakenteen jokaiseen segmenttiin tähtimerkkiä ja sitten luota ainoastaan lisäsääntöihin. Tämä voi olla hankalaa hallita ja se johtaa usein käyttäjän virheeseen ylläpidossa, mikä voi tehdä järjestelmästä sellaiseksi, että sinne ei voi kirjata.

## <a name="account-structure-activation"></a>Tilirakenteen aktivointi
Kun olet tyytyväinen uusiin asetuksiin tai tilirakenteen muutokseen, se on aktivoitava. Jos tilirakenne on määritty kirjanpitoon, tämä aktivointi voi kestää pitkään, koska järjestelmän kaikki kirjaamattomat tapahtumat on synkronoitava uuteen rakenteeseen. Tilirakenteen muutokset eivät vaikuta kirjattuihin tapahtumiin.

Lisätietoja on kohdassa [Tilikartan suunnittelu](plan-chart-of-accounts.md), [Taloushallinnon dimensiot](financial-dimensions.md) ja [Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun tarkistus)](enter-account-dimension-combinations-segmented-entry-control.md).

