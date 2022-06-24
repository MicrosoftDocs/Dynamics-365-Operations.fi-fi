---
title: Ostohyvitysten hallinnan parametrit
description: Tässä artikkelissa kuvataan Ostohyvityksen hallinnan parametrit -sivua. Tällä sivulla on asetuksia, jotka vaikuttavat kirjaamiseen, tilan päivityksiin, numerosarjoihin ja muuhun toiminnallisuuteen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 218c54d97f3ac204e8613f5efdda0cc9d713ee04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895522"
---
# <a name="rebate-management-parameters"></a>Ostohyvitysten hallinnan parametrit

[!include [banner](../includes/banner.md)]

**Ostohyvitysten hallinnan parametrit** -sivulla määritetään **Ostohyvityksen hallinta** -moduulissa käytettävät asetukset. Nämä asetukset vaikuttavat kirjaamiseen, tilan päivityksiin, numerosarjoihin ja muuhun toiminnallisuuteen. Tämän sivun asetukset ovat yhteisiä eri yrityksille, ja käyttäjät, joilla on tarvittavat suojauskäyttöoikeudet, voivat muokata näitä asetuksia.

Voit avata **Ostohyvitysten hallinnan parametrit** -sivun kohdassa **Ostohyvitysten hallinta \> Asetukset \> Ostohyvitysten hallinnan parametrit**. Määritä sitten kentät seuraavissa osioissa kuvatulla tavalla.

## <a name="rebate-management-tab"></a>Ostohyvitysten hallinta -välilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Ostohyvitysten hallinnan parametrit** -sivun **Ostohyvitysten hallinta** -välilehdessä.

| Kenttä | kuvaus |
|---|---|
| Oletustila | Valitse kaikkien uusien sopimusten oletustila. Voit määrittää valittavissa olevien tila-arvojen joukon [**Ostohyvityksen tilat** -sivulla](rebate-statuses.md). |
| Käsittele dimensioittain | Valitse, käsitelläänkö varaus-, ostohyvitys- ja poiskirjaustapahtumat taloushallinnon dimension mukaan. Kun tämä vaihtoehto on käytössä, järjestelmä käyttää lähdetapahtumille taloushallinnon dimensioita kohdetapahtumissa. |
| Tarkista, onko aiemmin kirjattu | <p>Valitse tämä järjestelmän toimintatapa, jos kirjaamattomia ostohyvitystapahtumia käsitellään useammin kuin kerran saman kauden aikana:</p><ul><li>**Varoitus** – Järjestelmä sallii käyttäjien ohittaa alkuperäiset tapahtumarivit, mutta näyttöön tulee varoitus.</li><li>**Virhe** – Järjestelmä estää käyttäjiä ohitamasta alkuperäisiä tapahtumarivejä, ja näyttöön tulee virhesanoma. |
| Kirjauskansioiden automaattinen kirjaaminen | Valitse, kirjaako järjestelmä ehdotetut kirjauskansiot automaattisesti. Näihin kirjauskansioihin kuuluvat kirjauskansiot, joita käytetään varauksia ja asiakkaiden vähennyksiä varten, sekä toimittajien verolaskukirjauskansiot. |
| Kirjaa vapaatekstilaskut automaattisesti | Valitse, kirjaako järjestelmä vapaatekstilaskut automaattisesti. Tämä asetus koskee vain vapaatekstilaskuja, joissa maksutyypiksi on määritetty *Verota laskujen asiakasvähennyksiä*. |
| Ostohyvityksen nimiketilauksen viite | Valitse ostohyvitysprosessista luoduissa myynti- ja ostotilauksissa käytettävä ostohyvitysviite (*Ei mitään*, *Ostohyvitysten hallintasopimus*, *Ostohyvitysten hallintanumero*, *Ostohyvitystapahtuman numero* tai *Asiakirjan huomautukset*). |
| Käytä vaatimusprosessia | <p>Määritä tämä vaihtoehto arvoon *Kyllä*, jos haluat käyttää vaatimusprosessia. Näin voit merkitä tapahtumat, jotka ostohyvityksen hallinta luo, joko vaadituiksi tai ei-vaadituiksi, ja kirjata sitten vain vaaditut tapahtumat.</p><p>Ostohyvitykset lasketaan esimerkiksi kuukauden tapahtumien perusteella, mutta asiakas on jättänyt kaksi päivää ei-vaadituiksi. Tässä tapauksessa ei-vaaditut tapahtumat luodaan uudelleen seuraavan kerran, kun suoritat *Käsittele*-toiminnon seuraavalle jaksolle.</p><p>Jos määrität tämän asetuksen arvoksi *Ei*, kaikki vaatimustapahtumat kirjataan.</p> |
| Sisällytä tilaustyypin kirjauskansio | Jos kyseessä on sopimus tai sopimusrivi, jossa tapahtumatyypiksi on määritetty *Tilaus*, tämä asetus määrittää, sisällytetäänkö *Kirjauskansio*- tyyppinen myyntitilaus. Tämä tuo joustavuutta, jos näitä tilaustyyppejä käytetään tilanteissa, joissa ostohyvitys ei ole vielä voimassa. |

## <a name="number-sequences-tab"></a>Numerosarjat-välilehti

**Ostohyvityksen hallinnan parametrit** -sivun **Numerosarjat**-välilehdessä voit määrittää numerosarjakoodeja erilaisille numerosarjoille, joita Ostohyvityksen hallinta käyttää. Seuraavassa taulukossa kuvataan näiden numerosarjojen tarkoitukset. Lisätietoja numerosarjoista on kohdassa [Numerosarjojen yleiskuvaus](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) ja siihen liittyvissä artikkeleissa.

| Viite | Kuvaus |
|---|---|
| Ostohyvitysten hallintasopimus | Numerosarja määrittää kullekin ostohyvityssopimukselle yksilöivän avaimen arvon. Tätä avainta käytetään, kun sopimuksia luodaan. |
| Ostohyvitysten hallintanumero | Numerosarja määrittää kullekin ostohyvitykselle yksilöivän avaimen arvon. Tätä avainta käytetään ostohyvityssuhteiden tunnistamiseen. |
| Ostohyvityksen tapahtumanumero | Numerosarja määrittää kullekin ostohyvitystapahtumalle yksilöivän avaimen arvon. Tätä avainta käytetään ostohyvitystapahtumien tunnistamiseen. |
| Verolasku | Numerosarja määrittää kullekin ostohyvityslaskulleyksilöivän avaimen arvon. Tätä avainta käytetään, kun ostohyvityskirjauskansiot kirjataan automaattisesti. |

## <a name="feature-visibility-tab"></a>Ominaisuuden näkyvyys -välilehti

Ostohyvitysten hallinta lisää ominaisuuksia (kenttiä ja toimintoja) useisiin usein käytettyihin Microsoft Dynamics 365 Supply Chain Managementin sivuihin. Nämä sivut sisältävät myyntitilauksiin ja myyntisopimuksiin liittyviä sivuja. Jos käytät ostohyvitysten hallintaa, nämä toiminnot on laitettava näkyville kaikkialla, ennen kuin niistä voi olla hyötyä. Jos et käytä ostohyvitysten hallintaa, voit piilottaa ominaisuudet ja näin pitää ne poissa tieltä.

Määritä **Ostohyvitysten hallinnan parametrit** -sivun **Ominaisuuden näkyvyys** -välilehdessä **Aktivoi**-asetuksen arvoksi *Kyllä*, jos haluat, että ostohyvitysten hallinnan ominaisuudet ovat näkyvissä aina, kun ne ovat käytettävissä. Määritä arvoksi *Ei*, jos haluat piilottaa ominaisuuden yhteisillä sivuilla **Ostohyvitysten hallinta** -moduulin ulkopuolella. Kuitenkin vaikka asetuksena olisi *Ei*, itse moduuli, mukaan lukien **Ostohyvitysten hallinnan parametrit** -sivu, on kuitenkin niiden käyttäjien käytettävissä, joilla on soveltuvat käyttöoikeudet.
