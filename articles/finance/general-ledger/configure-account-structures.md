---
title: Tilirakenteiden määrittäminen
description: Tässä artikkelissa on tietoja tilirakenteista ja taloushallinnon dimensioista.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713940"
---
# <a name="configure-account-structures"></a>Määritä tilirakenteet

[!include[banner](../includes/banner.md)]

Tilirakenteet käyttävät päätiliä ja taloushallinnon dimensioita luodakseen sääntöjä, jotka määrittävät järjestyksen ja arvot määrittäessäsi tilinumeron. Voit määrittää niin monta tilirakennetta kuin on tarpeen yrityksesi kannalta. Tilirakenteet määritetään yrityksen kirjausasetuksiin, jotta ne voidaan jakaa.

Tilirakennetta luotaessa segmenttien enimmäismäärä on 11. Jos tarvitset yli 11 segmenttiä, arvioi huolellisesti asetukset ja vaatimukset, koska se vaikuttaa käyttökokemukseen. Harkitse, jos segmentti voidaan johtaa käyttämällä hierarkiaa tietojen syöttöhetken sijaan tai käyttämällä käyttäjän määrittämää kenttää. Esimerkiksi jos haluat raportoida sijainnista, mutta voit määrittää sijainnin kustannuspaikan tai osaston mukaan, et tarvitse sijaintia taloushallinnon dimensioksi. Jos arvioinnin jälkeen, että tarvitse enemmän kuin 11 segmenttiä, voit lisätä uusia segmenttejä lisäsääntöjen avulla.

Tilirakenteet edellyttävät päätilin. Päätilin ei tarvitse olla rakenteen ensimmäinen segmentti, mutta se yksilöi, mitä tilirakennetta käytetään syötettäessä tilinumeroa. Näin ollen päätilin arvo voi olla vain yhdessä kirjanpitoon määritetyssä rakenteessa, jotta ne eivät ole päällekkäiset. Tilirakenteen tunnistuksen jälkeen suodatetaan sallittujen arvojen luettelo ohjatakseen käyttäjää valitsemaan vain voimassa olevia dimensioarvoja, näin vähentäen kirjauskansion virheellisen kirjauksen mahdollisuutta.

> [!NOTE] 
> Jos aiot budjetoida taloushallinnon dimension mukaan, sen on kuuluttava tilirakenteeseen. Budjetointi ei tällä hetkellä käytä lisäsääntöjä.

## <a name="example"></a>Esimerkki
Kuvataksemme tilirakenteen määrittämisen parhaita käytäntöjä, oletetaan, että yritys haluaa seurata tasetilejänsä (100000..399999) tasolla tilin ja liiketoimintayksikön taloushallinnon dimension tasolla. Tuotto-ja kulutileissä (400000..999999) he seuraavat taloushallinnon dimensioita Liiketoimintayksikkö, Osasto ja Kustannuspaikka. Jos he myyvät, he myös haluavat seurata kohdetta Asiakas. Käyttämällä tätä skenaariota on suositeltavaa käyttää kahta tilirakennetta, jotka on määritetty yrityksen kirjanpitoon. Yksi määritetään tasetileille ja toinen tulos- ja tappiotileille. Käyttäjäkokemuksen ja oikeellisuustarkistuksen optimoimiseksi Asiakas tulisi olla lisäsääntö, jota käytetään vain, kun myynnin tiliä käytetään.

**Tasetilirakenne**

|Päätili          | Liiketoimintayksikkö    |
|----------------------|-----------|
|100000..399999 | *;"&nbsp;"|

**Voitt- ja tappiotilirakenne**

|Päätili          | Liiketoimintayksikkö    |Osasto          | Kustannuspaikka    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"|

**Lisäsääntö asiakkaan lisäämiseksi**

Ehto: Kun Päätili on välillä 400000–499999, lisää asiakas. Tätä ei voi jättää tyhjäksi.

|Asiakas         |
|-----------------|
|\* |

Tässä yksinkertaistetussa esimerkissä kaikki arvot ja tyhjät sallitaan. Tämän vuoksi käytössä ovat \* ja "&nbsp;".

## <a name="segments-and-allowed-values"></a>Segmentit ja sallitut arvot
**Segmentit**- ja **Sallitun arvon tiedot**-osa sisältää ruudukon kaltaisen kokemuksen lisäämään sääntöjä, joita noudatetaan tarkistuksessa kirjauksen aikana. Voit kirjoittaa suoraan soluihin ruudukossa, tuoda sen Excelistä tai käyttää **Sallitun arvon tiedot** -osaa prosessin opastuksena.

**Sallitun arvon tiedot** -osa ohjaa, kun luot ehtoja käyttäen **operaattoreita**, kuten alkaa merkillä, on välillä, sisältää ja monia muita.

[![Salli arvot.](./media/account.png)](./media/account.png) 

Sallitut arvot tulevat oletusarvon mukaan kirjauskansioon tai kirjanpidollisen jaon aloitussivulle, jos muita mahdollisia arvoja ei ole valittavissa tilirakenteen asetusten mukaan.

Tässä on esimerkki **tulostilin rakenteesta**.

|Päätili          | Liiketoimintayksikkö    |Osasto          | Kustannuspaikka    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Kun kirjauskansio avataan ja valitaan tili tulosalueelta, liiketoimintayksikkö "002" -vaihtoehdon valitseminen aiheuttaa sen, että arvot 022 ja 014 ovat tilien valvonnan oletusarvoja. Tämä ongelma ilmenee myös kirjanpidollisen jaon sivulla. 

## <a name="more-than-seven-criteria-needed"></a>Tarvitaan yli seitsemän ehtoa

Jos tarvitset yli seitsemän ehtoa, voit jatkaa lisäämällä niitä seuraavalla rivillä. Huomaat, kun käytät **Sallitun arvon tiedot** -osaa, että **+Lisää uusi** -ehto ei ole enää aktiivinen seitsemännen ehdon syöttämisen jälkeen. Tämä johtuu monista tekijöistä, esimerkiksi: 
 - Sarakkeen leveys 
 - Miten tiedot on tallennettu 
 - **Sallitun arvon tiedot** -ohjausobjektin tehokkuudesta
 - Käyettävyydestä  

> [!NOTE]
> Päivitystä Microsoft Dynamics AX 2012:sta, jossa on määritetty yli seitsemän ehtoa, ei tueta. Tämä on korjattava, ennen kuin teet päivityksen talous- ja toimintosovelluksiin. 

Jatkaaksesi lisäehtojen lisäämistä, valitse **Monista segmentissä** ja **Sallitut arvot -osa**. Ehdot kopioidaan uudelle riville. Voit kirjoittaa päälle tai muokata **Sallitun arvon tiedot** -osaa.

## <a name="best-practices"></a>Parhaat käytännöt
Määrittäessäsi tilirakenteita on suositeltavia parhaita käytäntöjä. Kuitenkin nämä ovat vain ohjeita, joten kokonaisvaltainen keskustelu liiketoiminnastasi, kasvusuunnitelmasta ja huoltosuunnitelmasta tulisi olla osa tätä keskustelua.

- Tee päätilistä ensimmäinen tai tilirakenteen mahdollisimman alussa, jotta käyttäjät saavat parhaimman ohjatun kokemuksen tilille syötettäessä.
  
  - Tarkista, että tuen päätiliä käytetään ensimmäisessä sijainnissa niissä kolmannen osapuolen sovelluksissa, jotka on tarkoitus ottaa käyttöön.

- Käytä tilirakenteita mahdollisimman paljon uudelleen vähentääksesi ylläpitoa yritystesi välillä.

- Eri yritysten vaihteluissa harkitse lisäsääntöjä siten, että tilirakenteita voidaan käyttää uudelleen.

- Kun määrität sallittuja arvoja,käytä arvoalueita ja yleismerkkejä mahdollisimman paljon. Paitsi että näin yritys voi kasvaa ja muuttua ilman ylläpitoa, myös järjestelmä suorittaa paremmin tällä kokoonpanolla.

- Älä aseta tilirakenteen jokaiseen segmenttiin tähtimerkkiä ja sitten luota ainoastaan lisäsääntöihin. Tämä voi olla hankalaa hallita ja se johtaa usein käyttäjän virheeseen ylläpidossa, mikä voi tehdä järjestelmästä sellaiseksi, että sinne ei voi kirjata.

## <a name="account-structure-activation"></a>Tilirakenteen aktivointi
Kun olet tyytyväinen uusiin asetuksiin tai tilirakenteen muutokseen, se on aktivoitava. Jos tilirakenne on määritty kirjanpitoon, tämä aktivointi voi kestää pitkään, koska järjestelmän kaikki kirjaamattomat tapahtumat on synkronoitava uuteen rakenteeseen. Tilirakenteen muutokset eivät vaikuta kirjattuihin tapahtumiin. Sovelluksen versiosta 10.0.31 lähtien ominaisuuksien hallinnassa on käytettävissä uusi ominaisuus nimeltä **Tilirakenteen aktivoinnin suorituksen parannus**. Lisätietoja tästä tilirakenteen aktivoinnin uudesta ominaisuudesta on kohdassa [Tilirakenteen aktivoinnin suorituksen parannus](account-structure-improvement.md). 

Lisätietoja on kohdassa [Tilikartan suunnittelu](plan-chart-of-accounts.md), [Taloushallinnon dimensiot](financial-dimensions.md) ja [Kirjoita tilien ja dimensioiden yhdistelmät (komponentin segmentoidun syötön tarkistus)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
