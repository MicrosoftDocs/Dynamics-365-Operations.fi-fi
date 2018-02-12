---
title: Inventointi
description: "Tässä artikkelissa kuvataan, miten inventointia voi käyttää Varastonhallinnassa käytettävissä olevassa varastoratkaisussa. Artikkeli ei koske Inventoinnin- ja varastonhallinnassa käytettävissä olevaa varastoratkaisua."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ddb035eaa496a7c84f117f0523d509eccdf58505
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="cycle-counting"></a>Inventointi

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, miten inventointia voi käyttää Varastonhallinnassa käytettävissä olevassa varastoratkaisussa. Artikkeli ei koske Inventoinnin- ja varastonhallinnassa käytettävissä olevaa varastoratkaisua.

Inventointi on varastoprosessi, jota voit käyttää käytettävissä olevien varastonimikkeiden tarkastamiseen. Inventointiprosessia voidaan kuvata kolmessa vaiheessa:

1.  **Inventointityön luonti** – inventointityö voidaan luoda automaattisesti nimikkeiden raja-arvoparametrien perusteella tai käyttämällä inventointisuunnitelmaa. Voit myös luoda inventointityön manuaalisesti nimikkeen tai varaston parametrien avulla **Inventointityö nimikkeen mukaan**-sivulla tai **Inventointityö sijainnin mukaan** -sivulla.
2.  **Inventoinnin käsittely** – kun inventointityö on luotu, voit suorittaa sen laskemalla varastosijainnin nimikkeet ja kirjaamalla tuloksen Microsoft Dynamics 365 for Finance and Operationsiin mobiililaitteella. Vaihtoehtoisesti voit laskea varastosijainnin nimikkeet inventointityötä luomatta. Tätä prosessia kutsutaan nimellä *spot-inventointi*.
3.  **Lasketussa arvossa ilmenevien erojen selvittäminen** – inventoinnin jälkeen nimikkeillä, joiden lasketussa arvossa on eroja, työn tilana on **Odottaa tarkistusta** **Kaikki työ** -sivulla. Voit selvittää erot **Tarkistusta odottava inventointityö** -sivulla.

Seuraavassa kuvassa on esitetty inventointiprosessi. ![Inventointiprosessin kulku](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Inventoinnin edellytykset
Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen inventointia.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nimike</td>
<td>Nimike on otettava käyttöön varastonhallintaprosesseille.</td>
</tr>
<tr class="even">
<td>Varasto</td>
<td>Varastossa on oltava käytössä varastonhallintaprosessit. Valitse <strong>Varastot</strong>-sivulta varasto ja sitten <strong>Käytä varastonhallintaprosesseja</strong> -vaihtoehto, jos haluat aktivoida varaston varastonhallintaprosesseja varten. Jos haluat sallia työntekijöille kuormalavojen siirtämisen inventoinnin aikana, valitse <strong>Varastonhallinta</strong>-pikavälilehdestä <strong>Salli kuormalavojen siirto inventoinnin aikana</strong> -valintaruutu.</td>
</tr>
<tr class="odd">
<td>Työpoolit</td>
<td>Valinnainen: Luo työpooli varastotyön erotteluun työn tyypin (tässä tapauksessa inventointityön) perusteella.</td>
</tr>
<tr class="even">
<td>Sijainnit</td>
<td>Ota käyttöön inventointi toimipaikoille. Salli inventointi varastosijainnille valitsemalla <strong>Sijaintiprofiilit</strong>-lomakkeessa <strong>Salli inventointi</strong> -vaihtoehto.</td>
</tr>
<tr class="odd">
<td>Varastonhallinnan parametrit</td>
<td>Määritä parametrit inventointia varten. Valitse <strong>Varastonhallinnan parametrit</strong> -sivulta oletusarvoinen oikaisutyypin koodi, työluokan tunnus ja työn prioriteetti inventoinnille.</td>
</tr>
<tr class="even">
<td>Mobiililaite</td>
<td><ul>
<li>Luo valikkokohde yhdelle seuraavista menetelmistä <strong>Mobiililaitteen valikkovaihtoehdot</strong> -sivulla:
<ul>
<li>Käyttäjän ohjaama inventointi</li>
<li>Järjestelmän ohjaama inventointi</li>
<li>Inventoinnin ryhmittely</li>
<li>Pistoinventointi</li>
</ul>
</li>
<li>Määritä valikot kannettavalle laitteelle.</li>
<li>Luo työn käyttäjätili ja määritä mobiililaitteen valikko työn käyttäjätunnukselle.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Liittyvä asetustehtävä</td>
<td>Määritä syklilaskennan suunnitelma varastosijaintiin.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Inventointityön luominen automaattisesti
Voit ajoittaa toistuvan inventointityön luonnin kahdella tavalla: määrittämällä inventoinnin raja-arvot tai inventointisuunnitelmat.

-   Inventointikynnys osoittaa varastonimikkeiden määrä- tai suhderajan. Inventointityö luodaan automaattisesti, kun raja-arvo on saavutettu.
-   Inventointisuunnitelma luo inventointityön suoritettavaksi heti tai säännöllisesti eräajona. Kun inventointityö luodaan, sen rivi sisältää tiedot siitä, mikä sijainti inventoidaan. Tähän sijaintiin kohdistettua käytettävissä olevaa varastoa ei estetä ja se on siten käytettävissä varaukseen ja lähtevien käsittelyyn, vaikka avoimia inventointitöitä on olemassa.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Inventointityön luonti nimikkeiden raja-arvoparametrien perusteella

Inventointityö voidaan luoda, kun sijainnin nimikkeiden määrä alittaa tietyn raja-arvon. Esimerkiksi sijainnissa, jonka inventoinnin raja-arvo on 40, on 60 nimikettä. Myyntitilaustapahtuman aikana poimitaan 25 nimikettä kyseisestä sijainnista ja sijoitetaan väliaikaiseen paikkaan. Uusi nimikkeiden määrä 35 on pienempi kuin raja-arvo, joten inventointityö luodaan sijainnille automaattisesti.

### <a name="schedule-cycle-counting-work"></a>Ajoita inventointityö

Voit ajoittaa inventointisuunnitelmat luomaan inventointityön heti tai säännöllisesti. Määrittämällä inventointisuunnitelmia voit ohjata työpoolia, jolle inventointityö luodaan, eri sijainnissa oleville nimikkeille luotavien inventointien enimmäismäärää sekä sitä, miten monen päivän kuluttua varastosijainti inventoidaan uudelleen. Esimerkki: Nimike on käytettävissä kolmessa varastosijainnissa, ja inventointien enimmäismääräksi on määritetty **2**. Kun suoritat inventointisuunnitelman, se luo kaksi inventointia kahteen sijaintiin, joissa nimike on käytettävissä. Toisessa esimerkissä inventointien väliseksi päivien määräksi määritetään **5**. Tällöin inventointityö luodaan viiden päivän välein. Jos inventointityö kuitenkin käsitellään kolmantena päivänä, seuraava inventointityö luodaan viiden päivän jälkeen edellisen inventoinnin käsittelystä, 8. päiväksi.

## <a name="create-cycle-counting-work-manually"></a>Luo inventointityö manuaalisesti
Jos haluat luoda inventointityön manuaalisesti, voit käyttää **Inventointityö nimikkeen mukaan**- tai **Inventointityö sijainnin mukaan** -sivua. Voit määrittää luotavien inventointien enimmäismäärän. Jos esimerkiksi varastopäällikkö määrittää arvoksi **5**, inventointityö luodaan viidelle sijainnille, vaikka nimikettä on 10 eri sijainnissa. Voit myös valita työpoolin tunnuksen, johon liitetään luotavien inventointitöiden tunnukset. Kun työpoolin tunnusta käsitellään inventoinnissa, tähän työpooliin liitettyjä inventointityön tunnuksia käsitellään ryhmänä.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Inventoinnin suorittaminen mobiililaitteella
Inventointityöt voidaan käsitellä useilla menetelmillä käyttämällä Dynamics 365 for Finance and Operationsia mobiililaitteessa:

-   **Käyttäjän ohjaama** – Työntekijä voi määrittää inventointityön tunnuksen, joka on **Avoin**-tilassa.
-   **Järjestelmän ohjaama** – Finance and Operations määrittää työntekijälle inventointityön tunnuksen.
-   **Inventoinnin ryhmittely** – Työntekijä voi ryhmitellä inventointitöiden tunnukset, jotka liittyvät tiettyyn sijaintiin, vyöhykkeeseen tai työpooliin.
-   **Pistoinventointi** – Työntekijä voi laskea varastosijainnin nimikkeet milloin tahansa inventointityötä luomatta. Työntekijä suorittaa pistoinvestoinnin sijainnissa syöttämällä sijainnin tunnuksen.

Seuraava esimerkki osoittaa, miten voit suorittaa pisteinventoinnin mobiililaitteella. Ohjeet, jotka työntekijä näkee laitteessa, vaihtelevat pistoinventoinnille määritettyjen valikkovaihtoehtojen mukaan.

1.  Valitse mobiililaitteella valikkokohta inventointiyön havaitsemisen käsittelemiseksi.
2.  Rekisteröi sijainti, jolle pistoinventointi tehdään.
3.  Rekisteröi ja vahvista nimikkeen numero sekä laskettu nimikemäärä. **Huomautus:** Inventointityön tilaksi päivittyy **Odottaa tarkistusta** tai **Suljettu** **Kaikki työ** -sivulla **Työntekijä**-sivulla määritettyjen parametrien mukaan.
4.  Valinnainen: Toista vaihe 3 sijainnissa jäljellä oleville nimikkeille ja vahvista, ettei muita inventoitavia nimikkeitä ole käytettävissä.

## <a name="resolve-cycle-counting-differences"></a>Inventointierojen selvittäminen
Inventointiero ilmenee seuraavissa skenaarioissa, jos **On inventoinnin valvoja** -vaihtoehdon asetukseksi työn käyttäjätunnukselle on valittu **Ei**:

-   Inventoitu arvo ei ole **Työn käyttäjät** -lomakkeen **Prosenttiosuuden enimmäisraja**- tai **Määrän enimmäisraja** -kentissä määritettyjen poikkeamarajojen sisällä. Esimerkiksi sijainnin käytettävissä oleva varastomäärä on 50 ja työn käyttäjän poikkeaman raja on 10. Jos työn käyttäjä kirjoittaa arvon, joka ei ole välillä 40–60, ero esiintyy.
-   Inventointiarvo poikkeaa käytettävissä olevan varaston määrästä, eikä poikkeamarajoja aseteta.

Voit oikaista inventointiarvojen eroja ja hyväksyä lasketun arvon **Inventointi odottaa tarkistusta** -sivulla. Voit tarkistaa nimikemäärän muunnetun määrän **Varastosaldon sijainnin mukaan** -sivulla. Inventoitu arvo hylätään, jos eroa ei voida hyväksyä.

## <a name="see-also"></a>Lisätietoja
[Konfiguroi varastotyön mobiililaitteet](configure-mobile-devices-warehouse.md)




