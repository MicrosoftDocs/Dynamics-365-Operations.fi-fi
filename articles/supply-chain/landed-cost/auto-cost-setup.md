---
title: Automaattisten kustannusten määrittäminen
description: Tässä aiheessa kuvataan, miten voit määrittää kustannussääntöjä saapuvien merikuljetusten eri tasoille. Järjestelmä laskee kustannukset ja lisää ne automaattisesti näiden sääntöjen perusteella. Käyttäjien ei siis tarvitse lisätä kustannuksia manuaalisesti.
author: sherry-zheng
manager: tfehr
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 86dcbfbe6e00e7324e29541da6d682794e7487b3
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501147"
---
# <a name="auto-costs-setup"></a>Automaattisten kustannusten määrittäminen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Voit käyttää **Automaattiset kustannukset** -sivua määrittääksesi kustannussääntöjä erilaisille kustannusalueille (kuten merikuljetuksille, konteille, pakkauksille, ostotilauksille, nimikkeille tai siirtotilausriveille). Järjestelmä laskee kustannukset ja lisää ne automaattisesti näiden sääntöjen perusteella sekä niiden kenttien perusteella, jotka käyttäjät valitsevat luodessaan tietueita jollekin kustannusalueista. Käyttäjien ei siis tarvitse lisätä kustannuksia manuaalisesti.

Voit työstää automaattisia kustannuksia valitsemalla **Aiheutunut kustannus \> Kustannuslaskennan asetukset \> Automaattiset kustannukset**. Määritä sitten automaattisten kustannusten sääntösi tässä aiheessa kuvatulla tavalla.

## <a name="work-with-cost-areas"></a>Kustannusalueiden työstäminen

Automaattiset kustannukset toimivat kuten kauppasopimukset tai automaattiset sekalaiset kulut. Jokainen automaattisen kustannuksen tietue kuuluu tiettyyn kustannustasoon. Valitse haluamasi kustannusalue **Automaattiset kustannukset** -sivun luetteloruudun **Kustannusalue**-kentästä. Luetteloruudussa näytetään vain automaattiset kustannukset, jotka kuuluvat valittuun kustannusalueeseen. Kaikki luomasi automaattiset kustannukset kuuluvat sillä hetkellä valittuun kustannusalueeseen.

Kustannusalueet sallivat järjestelmän jakaa kustannusalueen ostotilausrivien kustannukset tasaisesti. Esimerkiksi yhden kontin kustannuksen arvo jaetaan kyseisen kontin kaikille tuotteille. Jos kontteja on kaksi tai enemmän, niille kaikille voidaan määrittää sama kustannustyyppi. Näin oikea automaattinen kustannus löytyy käyttämällä kontin tyyppiä.

## <a name="buttons-on-the-action-pane"></a>Toimintoruudun painikkeet

Seuraavassa taulukossa kuvataan painikkeet, jotka ovat käytettävissä **Automaattiset kustannukset** -sivun toimintoruudussa.

| Painike | kuvaus |
|---|---|
| Muokkaa | Muokkaa aiemmin luotua automaattista kustannusta. |
| Luo uusi | Luo automaattinen kustannus. |
| Delete-näppäin | Poista automaattinen kustannus. |
| Kopioi kohteesta | Luo uusi automaattisen kustannuksen tietue aiemmin luodun tietueen perusteella. Sen jälkeen voit muokata uutta tietuetta vapaasti. Tämän painikkeen avulla voit luoda nopeasti uusia automaattisia kustannuksia. |
| Näytä dimensiot | Avaa valintaikkuna, jossa voit valita tarkastelemiasi kustannustapahtumia varten näytettävät varastodimensiot. Jos poistat valintaruutujen valintoja, kustannustapahtumille näytetään vähemmän varastodimensioita. Näin ollen tapahtumasta näytetään vähemmän tietoja. Jos automaattiselle kustannukselle on määritetty varastodimensio, automaattinen kustannus lisätään vain, kun määritettyä varastodimensiota käytetään merikuljetukseen kuuluvalle nimikkeelle. |

## <a name="settings-on-the-header"></a>Ylätunnisteessa olevat asetukset

Ylätunnisteessa olevien asetusten yhdistelmä määrittää, milloin ja miten tietty automaattinen kustannus lisätään merikuljetukseen. Automaattinen kustannus lisätään merikuljetukseen, konttiin tai pakkaukseen vain, kun automaattisen kustannuksen tiedot vastaavat kyseisen kustannusalueen ylätunnisteessa olevia tietoja. Kaikkien vastaavien automaattisten kustannusten summa määrittää merikuljetuksen arvioidut aiheutuneet kustannukset. Tämä kustannus jaetaan tasaisesti kaikille konttiin tai merikuljetukseen kuuluville nimikkeille.

Seuraavassa taulukossa kuvataan kaikki ylätunnisteessa näytettävät kentät. Käytettävissä olevat kentät kuitenkin vaihtelevat valitun kustannusalueen ja valittujen näyttödimensioiden mukaan.

| Kenttä | kuvaus |
|---|---|
| **Tilikoodi** | <p>Valitse jokin seuraavista:</p><ul><li>**Taulukko** – Kustannussääntö koskee vain tiettyä toimittajaa.</li><li>**Ryhmä** – Kustannussääntö koskee tiettyä toimittajien ryhmää. Järjestelmä etsii toimittajatietueeseen liitettyä [toimittajan kustannustyyppien ryhmää](costing-parameters-setup.md).</li><li>**Kaikki** – Kustannussääntö koskee kaikkia toimittajia. |
| **Kuljetusyritys** | Valitse toimittaja tai toimittajaryhmä, jota kustannussääntö koskee. Tämä kenttä on käytettävissä vain, jos valitset **Tilikoodi**-kentässä *Taulukko* tai *Ryhmä*. |
| **Tulliasiamies** | Valitse toimittaja tai toimittajaryhmä, jota kustannussääntö koskee. Tämä kenttä on käytettävissä vain, jos valitset **Tilikoodi**-kentässä *Taulukko* tai *Ryhmä*. |
| **Nimikekoodi** | <p>Valitse jokin seuraavista:</p><ul><li>**Taulukko** – Kustannussääntö koskee vain tiettyä nimikettä.</li><li>**Ryhmä** – Kustannussääntö koskee tiettyä nimikkeiden ryhmää. Järjestelmä etsii nimiketietueeseen liitettyä [nimikkeen kustannustyyppien ryhmää](costing-parameters-setup.md).</li><li>**Kaikki** – Kustannussääntö koskee kaikkia nimikkeitä.|
| **Nimikkeen suhde** | Valitse nimike tai nimikeryhmä, jota kustannussääntö koskee. Tämä kenttä on käytettävissä vain, jos valitset **Nimikekoodi**-kentässä *Taulukko* tai *Ryhmä*. |
| **Toimitustapa** | Valitse toimitustapa (kuten lento- tai meriteitse), jota kustannussääntö koskee. |
| **Konttityyppi** | Tavaroiden kuljettamiseen käytetyn kontin tyyppi. Automaattista kustannusta voidaan käyttää merikuljetukselle vain, jos automaattisen kustannuksen asetuksissa määritetty konttityyppi vastaa merikuljetuksen konttityyppiä. |
| **Lähtösatama** ja **Kohdesatama** | Merikuljetuksen lähtösatama ja kohdesatama. (Joillakin konteilla voi olla eri kohdesatamat, koska merikuljetus voi pysähtyä useissa satamissa). Automaattista kustannusta voidaan käyttää merikuljetukselle vain, jos automaattisen kustannuksen asetuksissa määritetyt lähtö- ja kohdesatamat vastaavat merikuljetuksen lähtö-ja kohdesatamia. |
| **Automaattisen kustannuksen numero** | Automaattisen kustannussäännön yksilöivä tunniste. Tämän kentän arvo luodaan automaattisesti **Aiheutuneen kustannuksen parametrit** -sivulla määritetyn numerojärjestyksen perusteella. |
| **Varastodimensiot** | Jotkin kustannusalueet sallivat sinun lisätä ylätunnisteeseen yhden tai useamman nimikedimension (kuten koon, värin, varaston ja eränumeron). Valitse toimintoruudusta **Näytä dimensiot** valitaksesi lisättävät dimensiot. |

## <a name="settings-on-the-lines-fasttab"></a>Rivit-pikavälilehden asetukset

Lisää **Rivit**-pikavälilehdessä rivi jokaiselle valuutalle, jota voidaan käyttää, kun kustannusta käytetään merikuljetuksen ostotilausriville. 

Järjestelmä vertaa nimikkeiden ja ostotilausten jokaisen ostostilausrivin valuuttaa **Rivit**-pikavälilehdessä määritettyihin valuuttoihin. Se käyttää vain vastaavalle riville tai nimikkeelle määritettyä kustannusarvoa. Jos rivin tai nimikkeen valuutalle ei ole määritetty riviä, automaattista kustannusta ei käytetä kyseiselle riville tai nimikkeelle.

Muuntyyppisissä kustannusalueissa kaikkia **Rivit**-pikavälilehden rivejä käytetään jokaiselle merikuljetukselle, kontille, pakkaukselle tai siirtotilausriville, joka vastaa ylätunnisteessa määritettyjä arvoja.

Seuraavassa taulukossa kuvataan kaikki riveillä näytettävät kentät. Käytettävissä olevat kentät kuitenkin vaihtelevat valitun kustannusalueen mukaan.

| Kenttä | kuvaus |
|---|---|
| **Valuutta** | Valitse valuutta, jota rivi koskee. Tämä valuutta liittyy ostotilaukseen. Kun järjestelmä yrittää etsiä automaattisia kustannuksia, joita on määrä käyttää merikuljetukselle ja sen riveille, se valitsee rivin, jolla on sama valuutta kuin ostotilauksella. Tämä kenttä on käytettävissä vain, kun **Kustannusalue**-kentän arvoksi on määritetty *Ostotilaus* tai *Nimike*. |
| **Kustannustyypin koodi** | Kustannustyyppi. |
| **Jakomenetelmä** | <p>Menetelmä, jolla kustannukset jaetaan riveille. Käytettävissä ovat seuraavat asetukset:</p><ul><li><p>**Prosentti** – **Kustannusarvo**-kentän arvo on prosentti, joka koskee tavaroiden kokonaisarvoa.</p><p>Jos **Kustannusarvo**-kentän arvoksi on määritetty esimerkiksi *10* ja tavaroiden yhteisarvo on 800 $, kustannusarvo on 80 $ (= 800 $ × 10 prosenttia).</p></li><li>**Määrä** – Kustannus jaetaan tasaisesti tavaroiden määrän mukaan.</li><li>**Summa** – Kustannus jaetaan tasaisesti tavaroiden arvon mukaan.</li><li>**Tilavuus** – Kustannus jaetaan tasaisesti tavaroiden tilavuuden mukaan. Tilavuus määritetään nimikkeen päätietueessa.</li><li>**Paino** – Kustannus jaetaan tasaisesti tavaroiden painon mukaan. Paino määritetään nimikkeen päätietueessa.</li><li>**Tilavuusmitta** – Kustannus jaetaan tasaisesti tavaroiden tilavuusmitan mukaan.</li><li><p>**Mitta** – Tämä vaihtoehto sallii mitan määrittämisen **Aiheutunut kustannus** -moduulissa. Sitä käyttävät usein organisaatiot, jotka eivät tiedä tuotteiden yksilöllisiä tilavuuksia tai painoja, mutta jotka tarvitsevat tarkemman jakoperusteen kuin mitä **Summa**- ja **Määrä**-vaihtoehdot sallivat. Huolitsija tai edustaja ilmoittaa organisaatiolle painon tai tilavuuden joko nimikkeen tai ostotilauksen tasolla.</p><p>Oletetaan esimerkiksi, että merirahti on 900 $ arvoinen. Nimikkeen A paino on 800 kilogrammaa (kg) ja tilavuus 2 kuutiometriä (m³). Nimikkeen B paino on 100 kg ja tilavuus 1 m³. Kustannusten jakaminen painon mukaan johtaisi seuraaviin tuloksiin:</p><ul><li>Nimike A = 800 $</li><li>Nimike B = 100 $</li></ul><p>Kustannusten jakaminen tilavuuden mukaan johtaisi seuraaviin tuloksiin:</p><ul><li>Nimike A = 600 $</li><li>Nimike B = 300 $</li></ul><p>**Huomaa:** Kun **Jakomenetelmä**-kentän arvoksi on määritetty *Mitta*, järjestelmä käyttää mittoja, jotka on syötetty sekä kustannusalueelle (kontille) että riveille. Näiden mittojen summan ei tarvitse välttämättä vastata odotettua kokonaissummaa. Jos kuitenkin haluat, että niiden summat vastaavat odotettua kokonaissummaa, voit tarkastaa kokonaismitan tilastojen avulla. Mitan kehotteen asetus ja mitan automaattinen päivitys kuljetuksen tai kontin tasolla määritetään merikuljetuksen ylätunnisteessa.</p></li></ul> |
| **Päivämäärästä** | Määritä kustannuksen ajanjakson alku, jos ajanjakso on olemassa. Tämä päivämäärä on ensimmäinen päivämäärä, jolloin automaattista kustannusta käytetään. |
| **Päivämäärään** | Määritä kustannuksen ajanjakson loppu, jos ajanjakso on olemassa. Tämä päivämäärä on viimeinen päivämäärä, jolloin automaattista kustannusta käytetään. |
| **Luokka** | <p>Valitse kustannuksen laskentatapa. Käytettävissä ovat seuraavat asetukset:</p><ul><li>**Kiinteä** – Kustannus jaetaan tasaisesti jakomenetelmän mukaan.</li><li>**Kappaletta** – Kustannukset jaetaan kappalemäärän mukaan. Tästä syystä jakomenetelmää ei käytetä.</li><li>**Prosentti** – Prosenttiosuus tavaroiden arvosta lisätään. Tästä syystä jakomenetelmää ei käytetä.</li><li>**Hinta** – Valitse tämä vaihtoehto, jos on sinulla on määrään perustuvia erittelyitä. Rivin **Jakomenetelmä**-kentän arvon täytyy olla *Mitta*.</li><ul> |
| **Eritelty määrän mukaan** | <p>Valitse tämä valintaruutu, jos haluat, että **Määräerittelyt**-painike on käytettävissä **Rivit**-pikavälilehdessä. Määräerittelyt sallivat kustannuksen jakamisen osiin ja eri kustannusten vaihtelun, riippuen merikuljetuksen ostotilausrivillä olevasta määrästä. Tätä ominaisuutta käytetään usein, kun toimitustapa on lentokuljetus. Rivin **Luokka**-kentän arvon täytyy olla *Hinta*.</p><p>Määrä kuuluu **Jakomenetelmä**-kentässä valittuun vaihtoehtoon. Kustannuksen arvo on enintään **Kustannusarvo**-kenttään syötetty määrä.<p>Esimerkiksi 45–100 kg määrät tuottavat kustannukseksi 6,00 $ per mitta (esimerkiksi kg/m³). Yli 100 kg määrät tuottavat kustannukseksi 5,50 $ per mitta (esimerkiksi kg/m³).</p> |
| **Kustannusarvo** | Syötä kustannuksen arvo. |
| **Kustannuksen valuuttakoodi** | Valitse kustannuksen valuutta. |
| **Nimikkeen arvonlisäveroryhmä** | Valitse kustannuksen verokoodi. |
| **Vähimmäiskustannus** | <p>Tämä kenttä on voimassa vain, jos **Eritelty määrän mukaan** -valintaruutu on valittuna. Jos mitta ei saavuta tätä arvoa, vähimmäisarvo valitaan riippumatta **Määräerittelyt**-sivulla määritetyistä kustannuksista.<p>Esimerkiksi 0–45 kg määrät tuottavat kustannukseksi 6 $ per mitta (kg/m³). 46–100 kg määrät tuottavat kustannukseksi 5,50 $ per mitta (kg/m³). Jos lähetetty määrä on 2 kg, määräerittely luo kustannusarvoksi 12 $. Jos **Vähimmäiskustannus**-kentän arvoksi on kuitenkin määritetty *100*, lopullinen kustannus on 100 $.</p> |
| **Yhdistelmä** | Valitse tämä valintaruutu salliaksesi käyttäjien siirtää tämän kustannuksen kontin tasolta merikuljetuksen tasolle. Tällöin kustannukset voidaan laskea automaattisesti kontin tasolla. Ne voidaan kuitenkin myös yhdistää ja jakaa merikuljetuksen kaikkien konttien kaikkien nimikkeiden kesken yksittäisten konttien kaikkien nimikkeiden sijaan. |
| **Linkitetty kustannustyyppi** | <p>Linkitä nykyinen rivi saman automaattisen kustannuksen tietueen toiseen riviin määrittämällä linkitettävän rivin **Kustannustyypin koodi** -arvo. Tämä ominaisuus on käytettävissä vain, kun nykyisen rivin **Luokka**-kentän arvo on *Prosentti*. Kun nykyinen rivi on linkitetty toiseen riviin, sen kustannus perustuu toisen rivin kustannukseen.</p><p>Oletetaan esimerkiksi, että rahdin arvo on 1 000 $ ja haluat polttoaineen lisämaksun olevan 10 prosenttia rahtikustannuksista. Tällöin rivin **Luokka**-arvon täytyy olla *Prosentti*, **Kustannusarvo**-arvon täytyy olla *10 %* ja **Linkitetty kustannustyyppi** -arvon täytyy olla *Rahti*.</p> |
| **Arvon oikaisu** ja **Oikaisusumma** | <p>Käytä näitä kenttiä säätääksesi eri prosenttiarvojen arvoa ja summaa. Ne ovat käytettävissä vain, kun **Kustannusalue**-kentän arvoksi on määritetty *Nimike*.</p><p>Nimikkeen eri komponenteille voidaan määrittää eri kustannuslaskenta. Nimikkeen yhdellä komponentilla voi olla eri kustannusprosentti kuin nimikkeen toisella komponentilla. Tämä lähestymistapa on joskus tarpeen tavaroiden tietyn osan arvojen määrittämiseksi eri hinnoilla.</p><p>Esimerkiksi rannekellon tullimaksut voidaan laskea kahdella tavalla: rannekellon yhden komponentin tullimaksu on 10 prosenttia, ja toisella 2 prosenttia. Tällöin kustannuslaskenta voidaan jakaa kahden komponentin välillä.</p><p>Nimikkeen kustannus lasketaan, mutta kustannusarvoa oikaistaan niiden komponenttien arvolla, joilla on eri kustannusluokka. Jäljellä olevien komponenttien kustannukset voidaan sitten laskea käyttämällä summaa, jolla edellistä laskelmaa oikaistiin.</p><p>Oletetaan esimerkiksi, että rannekellon komponentin A hinta on 9,50 $ ja tullimaksu on 10 prosenttia, ja komponentin B hinta on 0,50 $ ja tullimaksu 2 prosenttia. Kokonaishinta on siis 10,00 $. Ensimmäinen merkintä on 10 prosentin riville. Se käyttää seuraavia arvoja:</p><ul><li>**Luokka:** *Prosentti*</li><li>**Kustannusarvo:** *10*</li><li>**Arvo oikaistu:** *Oikaisun peruste*</li><li>**Oikaistu arvo:** *-0,50*</li></ul><p>Tämä kokoonpano määrittää, että nimikkeen kustannuksista (10 $) on vähennettävä 0,50 $ (komponentin B hinta) ennen 10 prosentin tullimaksun laskemista. Näin ollen 10 prosenttia sovelletaan 9,50 $ summaan.</p><p>Toinen merkintä on 2 prosentin riville (0,50 $, jolla edellistä merkintää oikaistiin). Se käyttää seuraavia arvoja:</p><ul><li>**Luokka:** *Prosentti*</li><li>**Kustannusarvo:** *2*</li><li>**Arvo oikaistu:** *Käytä*</li><li>**Oikaisu:** *0,50*</li></ul><p>Tämä kokoonpano laskee komponentin B jäljellä olevan tullimaksun.</p> |
