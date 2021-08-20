---
title: Varaston tilat
description: Tässä artikkelissa kuvataan, miten varaston tiloja voidaan käyttää varaston luokittelussa ja seuraamisessa.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58e9895afecf24a84281049c63d661e690fe2a2f7963d4711dc7cc4d5630322b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735228"
---
# <a name="inventory-statuses"></a>Varaston tilat

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten varaston tiloja voidaan käyttää varaston luokittelussa ja seuraamisessa.

## <a name="set-up-and-use-inventory-statuses"></a>Varastotilojen määrittäminen ja käyttäminen

Voit käyttää varaston tilaa luokitellaksesi varaston. Sitten voit aloittaa asianmukaiset toiminnot, kuten täydennys tai poislaitettava työ.

Seuraavassa on esimerkkejä tavoista, joilla voit käyttää varaston tiloja:

- Luo varaston tiloja käytettävissä olevalle varastolle, saapuville tapahtumille ja lähteville tapahtumille.
- Määritä varaston oletustila varastotapahtumille.
- Muuta nimikkeiden varastotilaa ennen saapumista, saapumisen yhteydessä tai kun nimikkeet sijoitetaan pois varastosiirrossa.
- Käytä varaston tilaa niiden nimikkeiden hinnoitteluun, jotka palautetaan ja suunnitellaksesi nimikkeiden kattavuuden pääsuunnittelun aikana.

Varaston tila on yksi varastodimensioryhmän dimensioista. Varaston tiloja voidaan luokitella käytettävissä oleviin ja ei-käytettävissä oleviin ja voit käyttää **Varaston esto** -parametria estämään nimikkeet, joilla on ei-käytettävissä oleva varaston tila. Toimituskiellossa olevien nimikkeiden katsotaan olevan osa fyysistä varastoa, eikä niitä vodai käyttää tuotantotilauksessa, myyntitilauksessa, siirtotilauksessa tai lähtevässä tapahtumassa.

Voit käyttää saapuville töille varastonimikkeitä, joiden varastotila on joko käytettävissä tai ei käytettävissä. Voit luoda esimerkiksi käytettävissä oleville tilan, jonka nimi on *Valmis*, ei-käytettävissä oleville tilan, jonka nimi on *Vioittuneet* ja toimituskiellossa oleville tilan, jonka nimi on *Suljettu*. Luodessasi ostotilauksen vastaanotetuille tai palautetuille nimikkeille, jos mitkään nimikkeet ovat vahingoittuneita tai rikkoutuneita, voit muuttaa niiden varaston tilan *Vioittuneet*-ostotilauksen rivillä. Sen jälkeen, kun nimikkeet on otettu vastaan, tilaksi määritetään automaattisesti *Suljettu*. Jos luet vioittuneet nimikkeet mobiililaitteella, Supply Chain Management voi käyttää sijainnin direktiivejä ja työn malleja näyttääkseen tietoja sopivasta sijainnista tai ne sijainnit, jossa voit laittaa pois nuo nimikkeet. Palautetuille nimikkeille luodaan jakelutyyppi *Varaus* **Varastotapahtumat** -lomakkeessa.

Voit määrittää, mitkä varaston tilat saavat aikaan eston käyttämällä **Varastoesto**-valintaruutua **Varaston tilat** -sivulla. Varaston tiloja ei voi käyttää myynti-, tai siirtotilauksien tai projekti-integrointien estotiloina.

Lähteville töille voidaan käyttää erilaisia ei-estäviä varastotiloja, joilla ohjataan varastoa, josta varataan. Jos on nimikkeitä, joiden tila on *Estossa* ja pääsuunnittelu suoritetaan näillä nimikkeillä, niitä pidetään puuttuvina ja varasto täydennetään automaattisesti. Lisäksi lähteviin töihin liittyvien laatutilausten **varastotilaa** ei voi päivittää laatutilauksen vahvistuksen osana.

> [!NOTE]
> Et voi muuttaa varaston tilaa sijainnissa, joissa on avoimia töitä. Jos esimerkiksi vastaanotit nimikkeelle oston, mutta et tehnyt hyllytysvaihetta, vastaanottosijainnissa on avoin työ, ja saat virheilmoituksen, jos haluat muuttaa varaston tilan tässä sijainnissa. Liittyvän työn valmiiksi saaminen tai peruuttaminen mahdollistaa tilan muuttumisen.
>
> Tavallisesti käytettävissä olevan varaston tilaa, joka liittyy avoimen varastotyöhön, muutavat vain työntekijät, jotka käyttävät varastonhallinnan mobiilisovellusta esimerkiksi siirtoprosessia suoritettaessa.

Kun olet määrittänyt varaston tilat, voit määrittää varaston oletustilan toimipaikalle, nimikkeelle ja varastolle. Voit myös määrittää oletustilan myyntiin, siirtoon ja ostotilauksiin. Myyntitilausten ja lähtevien siirtotilausten oletustilassa **Varastonesto**-asetus ei voi olla asennossa *Kyllä*. Varaston tila, joka periytyy toimipaikan, varaston, nimikkeen, ostotilauksen, siirtotilauksen tai myyntitilauksen oletusarvoasetuksista, voidaan muuttaa käyttämällä mobiililaitetta tai ostotilauksessa, myyntitilauksessa tai siirtotilausrivillä.

Suunnitellaksesi kattavuusryhmän nimikkeille, joiden varastotila on käytettävissä oleva, valitse **Kattavuussuunnitelma dimension mukaan** -vaihtoehto varastodimensiolle **Varastodimensioryhmät** -sivulla. Avatessasi **Nimikkeen kattavuus**-ohjatun toiminnon, nimikkeet, joilla on käytettävissä oleva tila, näkyvät **Tila**-sivulla. Luo näille nimikkeille kattavuusasetukset valitsemalla saatavilla oleville varastotiloille varastotilatunnus. Kattavuusasetusten perusteella voit laskea nimikevaatimukset sekä käytettävissä olevien nimikkeiden tarjonnan ja kysynnän ennusteen pääsuunnittelun aikana. Et voi luoda nimikkeen kattavuusasetusta, jolla on toimituskiellossa oleva varastotila. Vaihtoehtoisesti, voit käyttää **Nimikekattavuus** -sivua nimikkeen kattavuusparametrien luomiseen tai muokkaamiseen.

## <a name="change-inventory-statuses"></a>Varastotilojen muuttaminen

Varastotiloja voi muuttaa joko **Varastosaldo sijainnin mukaan** -sivulla tai käyttämällä kausittaisen *Varaston tilamuutos* -tehtävää.

- Kausittaista *Varaston tilanmuutos* -tehtävää käytettäessä voit valita sisällytettävät tietueet ja määrittää tehtävän suoritettavan eränä toivotuin väliajoin.
- Varastotilaa voi muuttaa tilapäisprosessina valitsemalla **Varastosaldo sijainnin mukaan** -sivulla sopivat tietueet ja valitsemalla sitten **Varaston tilanmuutos** -painikkeen.

> [!NOTE]
> *Seurantadimensioilla hallittavien nimikkeiden varastotilan muutos* -ominaisuudella voi muuttaa seurantadimensioilla hallittavien nimikkeiden varastotilaa; tähän sisältyy myös mahdollisuus päivittää vain valitut tietueet. Toiminnon voi ottaa tarpeen mukaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Kun ominaisuus on otettu käyttöön, seuraavat ovat toimet ovat mahdollisia:
>
> - **Varastosaldo sijainnin mukaan** -sivulla voi ryhmittää rivejä näkyvissä olevien dimensioiden mukaan käyttämällä **Näytä dimensiot** -painiketta ja muuttamalla valittujen rivien tilaa.
> - **Varastosaldo sijainnin mukaan** -sivulla voi valita useita tietueita ja muuttaa ne sitten kaikki kerralla **Varastosaldo sijainnin mukaan** -painikkeella.
> - Kausittaisia **Varaston tilanmuutos** -tehtävässä voi käyttää suodatusperusteena seurantadimensioita.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
