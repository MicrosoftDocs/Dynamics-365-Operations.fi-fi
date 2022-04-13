---
title: Negatiiviset päivät ja dynaamiset negatiiviset päivät
description: Tässä ohjeaiheessa on tietoja negatiivisista ja dynaamisista negatiivisista päivistä sekä siitä, miten niillä voi edistää liiketoimintaa.
author: t-benebo
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d88517c99a274911e8abd8de4bcd318139822a5
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469866"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negatiiviset päivät ja dynaamiset negatiiviset päivät

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja negatiivisista ja dynaamisista negatiivisista päivistä sekä siitä, miten niillä voi edistää liiketoimintaa. *Negatiivisten päivien aikaraja* ilmaisee päivien määrän, jonka olet valmis odottamaan ennen uuden täydennyksen tilaamista, kun varasto on negatiivinen.

Ohjeaiheessa käsitellään seuraavia tietoja:

- Suunniteltujen tilausten luonti
- Negatiivisen päivien aikarajan ja nimikkeen läpimenoajan välinen korrelaatio
- Dynaamisten negatiivisten päivien aikarajan laskeminen ja nimikkeen läpimenoajan ottaminen huomioon laskelmassa
- Negatiivisiin päiviin liittyvien [materiaalitarpeiden suunnittelun (MRP) (pääsuunnittelun) suoritusajan parannusehdotukset](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx)

Tässä ohjeaiheessa käytetään kolmea hypoteettista skenaariota, jotka auttavat ymmärtämään näitä tietoja. Skenaarioiden välinen ero on kohta, jossa kysyntä saadaan: ennen nimikkeen läpimenoajankohtaa, sen aikana tai sen jälkeen.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Skenaario 1: kysyntä saadaan ennen nimikkeen läpimenokautta

Voit saada kysynnän joko suhteellisen aikaisessa vaiheessa nimikkeen läpimenokaudella tai juuri ennen läpimenokauden alkamista. Esimerkki tästä skenaariosta:

- DemoProduct-nimikkeen oston läpimenoaika on kuusi päivää.
- DemoProduct-tuotteen varastotaso nollapäivänä (1. tammikuuta) on 0 (nolla).
- Saat nollapäivänä (1. tammikuuta) DemoProduct-nimikkeen myyntitilauksen, jonka määrä on 10.
- Seitsemäntenä päivänä (8. tammikuuta) on olemassa DemoProduct-nimikkeen ostotilaus, jonka määrä on 10.

Seuraava kuva on tämän skenaarion graafinen esitys.

![Skenaarion 1 graafinen esitys.](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tapaus A: negatiivisten päivien arvo on pienempi kuin nimikkeen läpimenoaika

Jos määrität negatiivisten päivien arvoksi määrän, joka on pienempi kuin nimikkeen läpimenoaika, tarvesuunnittelu etsii DemoProduct-nimikkeen vastaanotot negatiivisten päivien aikarajan sisältä. Koska vastaanottoja ei löydy, tarvesuunnittelu luo uuden suunnitellun ostotilauksen. Tämä suunniteltu tilaus viivästyy heti kuudella päivällä (läpimenoaika). Tämän vuoksi saapuu 7. tammikuuta. Aiemmin luotu ostotilaus saa **Peruuta**-toimenpidesanoman, koska uuden suunnitellun ostotilauksen luonti teki sen tarpeettomaksi.

Seuraavassa kuvassa näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 1 tapauksesta A.](./media/negative-days-2.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 1 tapauksen A graafinen esitys.](./media/negative-days-3.png)

Jos otetaan huomioon MRP-suorituskyky ja suunnitelman ailahtelevuus, tapaus ei suoriutunut hyvin. MRP-suunnittelun on luotava uusi suunniteltu tilaus ja laskettava viiveet ja toimenpiteet. Nämä tehtävät vievät paljon aikaa. Tämä tapaus lisää myös kaksi muuta tapahtumaa suunnitelmaan. Toisaalta myyntitilaus viivästyy vain kuusi eikä seitsemän päivää.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tapaus B: negatiivisten päivien arvo on suurempi kuin nimikkeen läpimenoaika

Voit parantaa tarvesuunnittelun suorituskykyä määrittämällä negatiivisten päivien arvon suuremmaksi kuin nimikkeen läpimenoaika. Tässä skenaariossa voit etsiä vastaanottoja niin kauan kuin haku järkevää, jos et toimitusta läpimenoajan aikana. Vaikka tarvesuunnittelun suoritusaika on lyhyempi, varo ettei tilauksiin tule ylimääräisiä viiveitä.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tapaus C: nimikkeen läpimenoajan automaattinen korrelaatio negatiivisten päivien aikarajaan

Voit korreloida nimikkeen läpimenoajan automaattisesti negatiivisten päivien aikarajaan käyttämällä dynaamisia negatiivisia päiviä. Voit käyttää dynaamisia negatiivisia päiviä valitsemalla **Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit** ja määritä sitten **Yleiset**-välilehden **Kattavuus**-osan **Käytä dynaamisia negatiivisia päiviä** -asetukseksi **Kyllä**. Tarvesuunnittelu etsii sitten vastaanottoja dynaamisten negatiivisten päivien aikarajan sisältä. Tämä aikaraja lasketaan seuraavalla kaavalla:

dynaamisen negatiivisen päivän aikaraja = oston läpimenoaika + negatiivisten päivien aikaraja + (kuluva päivä – tarvepäivä).

(Jos DemoProduct-nimikkeen oletustilaustyyppi on **Tuotanto** tai **Siirto**, läpimenoaika on **varaston** läpimenoaika.)

Dynaamisia negatiivisia päiviä käytettäessä aikaraja, jota tarvesuunnittelu käyttää vastaanottojen hakemiseen, on nyt 6 + 2 + 0 = 8 päivää. Tarvesuunnittelu etsii aiemmin luodun ostotilauksen ja määrittää myyntitilauksen sen perusteella. Uusia suunniteltuja tilauksia ei luoda. Tämän vuoksi tarvesuunnittelun suoritusaika on lyhyempi. Seuraavassa kuvassa on DemoProduct-nimikkeen nettotarpeet.

![Skenaarion 1 tapauksen C nettotarpeet.](./media/negative-days-4.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 1 tapauksen C graafinen esitys.](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tapaus D: vain dynaamisten negatiivisten päivien käyttäminen

Jos määrität negatiivisten päivien arvoksi **0** (nolla) ja käytät vain dynaamisten negatiivisten päivien aikarajaa, dynaamisten negatiivisten päivien aikaraja on 6 + 0 + 0 = 6 päivää. Tässä tapauksessa tulos on sama kuin tämän skenaarion tapauksen A tulos. MRP-suunnittelun on luotava uusi suunniteltu tilaus ja laskettava viiveet ja toimenpiteet. Nämä tehtävät vievät paljon aikaa ja voivat olla myös turhauttavia. Lisäksi käsiteltävänä on kaksi muuta tapahtumaa. Koska kysyntää ei voida täyttää nimikkeen saapumiseen mennessä, tämä tapaus mutkistaa suunnitelmaa tarpeettomasti.

Seuraavassa kuvassa on näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 1 tapauksesta D.](./media/negative-days-6.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 1 tapauksen D graafinen esitys.](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tapaus E: sekä arvoltaan nimikkeen läpimenoaikaa suuremman negatiivisten päivien että dynaamisten negatiivisten päivien aikarajan käyttäminen

Jos määrität negatiivisten päivien arvon suuremmaksi kuin nimikkeen läpimenoaika ja jos käytät myös dynaamisten negatiivisten päivien aikarajaa, dynaamisten negatiivisten päivien aikaraja on 6 + 6 + 0 = 12 päivää. Tällä tavoin seurauksena voi olla erittäin pitkäkestoinen aikaraja, jossa tarvesuunnittelun on etsittävä tuloksia. Lisätietoja siitä, miten tapaus E liittyy tilanteeseen, jossa negatiivisille päiville määritetään pitkä aikaraja, on tämän ohjeaiheen osassa [Johtopäätökset](#conclusion).

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Skenaario 2: kysyntä saadaan nimikkeen läpimenokauden aikana

Tarve voidaan saada jossain vaiheessa nimikkeen läpimenoajan aikana. Esimerkki tästä skenaariosta:

- DemoProduct-nimikkeen oston läpimenoaika on kuusi päivää. 
- DemoProduct-tuotteen varastotaso nollapäivänä (1. tammikuuta) on 0 (nolla).
- Saat neljäntenä päivänä (5. tammikuuta), joka on nimikkeen läpimenoajan sisällä, DemoProduct-nimikkeen myyntitilauksen, jonka määrä on 10.
- Seitsemäntenä päivänä (8. tammikuuta) on DemoProduct-nimikkeen ostotilaus, jonka määrä on 10.

Seuraava kuva on tämän skenaarion graafinen esitys.

![Skenaarion 2 graafinen esitys.](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tapaus A: negatiivisten päivien arvo on pienempi kuin nimikkeen läpimenoaika

Jos määrität negatiivisten päivien arvoksi määrän, joka on pienempi kuin nimikkeen läpimenoaika, tarvesuunnittelu etsii DemoProduct-nimikkeen vastaanotot negatiivisten päivien aikarajan sisältä. Koska tarvesuunnittelu ei löydä vastaanottoja, se luo uuden suunnittelun ostotilauksen, joka käyttää kuluvaa päivää tilauspäivänä. Tämä suunniteltu tilaus viivästyy heti kuudella päivällä (läpimenoaika). Tämän vuoksi saapuu 7. tammikuuta. Aiemmin luotu ostotilaus saa **Peruuta**-toimenpidesanoman, koska uuden suunnitellun ostotilauksen luonti teki sen tarpeettomaksi.

Seuraavassa kuvassa on näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 2 tapauksesta A.](./media/negative-days-9.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 2 tapauksen A graafinen esitys.](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tapaus B: negatiivisten päivien arvo on suurempi kuin nimikkeen läpimenoaika

Tämä tapaus muistuttaa skenaarion 1 tapausta B. Jos määrität negatiivisten päivien arvon suuremmaksi kuin nimikkeen läpimenoaika, et saa uutta suunniteltua tilausta. Myyntitilaus liitetään aiemmin luotuun ostotilaukseen.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tapaus C: nimikkeen läpimenoajan automaattinen korrelaatio negatiivisten päivien aikarajaan

Tämä tapaus muistuttaa skenaarion 1 tapausta C, koska dynaamiset negatiiviset päivät toimivat yhtä hyvin kuin siinä tapauksessa. Dynaamisten negatiivisten päivien aikaraja on nyt 6 + 2 – 4 = 4 päivää. Jos toimit tällä tavalla, tarvesuunnittelu etsii aiemmin luodun ostotilauksen ja liittää siihen myyntitilauksen. Koska uusia suunniteltuja tilauksia ei luoda, tarvesuunnittelun suoritusaika on lyhyempi.

Seuraavassa kuvassa näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 2 tapauksesta C.](./media/negative-days-11.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 2 tapauksen C graafinen esitys.](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tapaus D: vain dynaamisten negatiivisten päivien käyttäminen

Jos määrität negatiivisten päivien arvoksi **0** (nolla) ja käytät vain dynaamisten negatiivisten päivien aikarajaa, dynaamisten negatiivisten päivien aikaraja on nyt 6 + 0 – 4 = 2 päivää. Tässä tapauksessa tulos on sama kuin tämän skenaarion tapauksen A tulos. Tämän skenaarion tapauksessa A on graafinen esitys tapahtumista.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tapaus E: sekä arvoltaan nimikkeen läpimenoaikaa suuremman negatiivisten päivien että dynaamisten negatiivisten päivien aikarajan käyttäminen

Jos määrität negatiivisten päivien arvon suuremmaksi kuin nimikkeen läpimenoaika ja jos käytät myös dynaamisten negatiivisten päivien aikarajaa, dynaamisten negatiivisten päivien aikaraja on 6 + 6 – 4 = 8 päivää. Tällä tavoin seurauksena voi olla erittäin pitkäkestoinen aikaraja, jossa tarvesuunnittelun on etsittävä tuloksia. Lisätietoja siitä, miten tapaus E liittyy tilanteeseen, jossa negatiivisille päiville määritetään pitkä aikaraja, on tämän ohjeaiheen osassa [Johtopäätökset](#conclusion).

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Skenaario 3: kysyntä saadaan nimikkeen läpimenokauden jälkeen

Voit saada kysynnän nimikkeen läpimenoajan jälkeen. Esimerkki tästä skenaariosta:

- DemoProduct-nimikkeen oston läpimenoaika on kuusi päivää.
- DemoProduct-tuotteen varasto nollapäivänä (1. tammikuuta) on 0 (nolla).
- Saat seitsemäntenä päivänä (8. tammikuuta), joka on nimikkeen läpimenoajan ulkopuolella, DemoProduct-nimikkeen myyntitilauksen, jonka määrä on 10.
- Kymmenentenä päivänä (11. tammikuuta) on DemoProduct-nimikkeen ostotilaus, jonka määrä on 10.

Seuraava kuva on tämän skenaarion graafinen esitys.

![Skenaarion 3 graafinen esitys.](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tapaus A: negatiivisten päivien arvo on pienempi kuin nimikkeen läpimenoaika

Jos negatiivisten päivien määritetty arvo on pienempi kuin nimikkeen läpimenoaika, tarvesuunnittelu tarkkailee kaksi päivää myyntitilauksen tarvepäivän edeltä. Koska tarvesuunnittelu ei löydä mitään, se luo uuden suunnitellun ostotilauksen 2. tammikuuta. Tämä suunniteltu ostotilaus lähetetään juuri ajoissa täyttämään myyntitilauksen kysyntä. Aiemmin luotu ostotilaus saa **Peruuta**-toimenpidesanoman, koska sitä ei tarvita.

Seuraavassa kuvassa näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 3 tapauksesta A.](./media/negative-days-14.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 3 tapauksen A graafinen esitys.](./media/negative-days-15.png)

> [!NOTE]
> Edellisessä näyttökuvassa ostotilauksen tarvepäivä on 12. tammikuuta. Koska kyseinen näyttökuva otettiin 2015, jolloin 11. tammikuuta oli sunnuntai, tarvesuunnittelu muutti tarvepäivän seuraavaan arkipäivään, joka oli maanantai 12. tammikuuta. Ostotilauksen toimituspäivä on kuitenkin 11. tammikuuta.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tapaus B: negatiivisten päivien arvo on suurempi kuin nimikkeen läpimenoaika

Jos määrität negatiivisten päivien arvon suuremmaksi kuin nimikkeen läpimenoaika, et saa uutta suunniteltua tilausta. Myyntitilaus määritetään aiemmin luodun ostotilauksen perusteella. Tämän vuoksi myyntitilaus viivästyy. Jos luot suunnitellun tilauksen, voit lähettää myyntitilauksen ajallaan.

Seuraavassa kuvassa näyttökuva tästä tapauksesta.

![Näyttökuva skenaarion 3 tapauksesta B.](./media/negative-days-16.png)

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 3 tapauksen B graafinen esitys.](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tapaus C: nimikkeen läpimenoajan automaattinen korrelaatio negatiivisten päivien aikarajaan

Tämä tapaus muistuttaa skenaarion 1 tapausta C, koska dynaamiset negatiiviset päivät toimivat yhtä hyvin elleivät jopa paremmin kuin tämän skenaarion tapauksessa B.

Dynaamisten negatiivisten päivien aikaraja on 6 + 2 – 7 = 1 päivä. Tässä tapauksessa järjestelmä kuitenkin ottaa huomioon negatiivisten päivien läpimenoajan (2), koska tarvesuunnittelu ottaa huomioon negatiivisten päivien läpimenoajan ja dynaamisten negatiivisten päivien läpimenoajan välisen maksimiarvon. Tässä vuoksi tulos on tässä tapauksessa sama kuin tämän skenaarion tapauksen A tulos.

Seuraava kuva on graafinen esitys siitä, mitä tapauksessa tapahtuu.

![Skenaarion 3 tapauksen C graafinen esitys.](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tapaus D: vain dynaamisten negatiivisten päivien käyttäminen

Jos määrität negatiivisten päivien arvoksi **0** (nolla) ja käytät vain dynaamisten negatiivisten päivien aikarajaa, dynaamisten negatiivisten päivien aikaraja on nyt 6 + 0 – 7 = -1 päivä. Tässä tapauksessa järjestelmä ottaa edelleen huomioon negatiivisten päivien läpimenoajan (2). Tässä vuoksi tulos on tässä tapauksessa sama kuin tämän skenaarion tapauksen A tulos, ja siinä on myös samat huonot puolet. Skenaarion 2 tapauksessa A on graafinen esitys tapahtumista.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tapaus E: sekä arvoltaan nimikkeen läpimenoaikaa suuremman negatiivisten päivien että dynaamisten negatiivisten päivien aikarajan käyttäminen

Tämä tapaus on sama kuin skenaarioiden 1 ja 2 tapaus E. Se on käytännössä samat hyvät ja huonot puolet.

## <a name="conclusion"></a>Johtopäätökset

Kuten tämän ohjeaiheen kolme skenaariota on osoittanut, negatiivisten päivien arvo kannattaa määrittää suuremmaksi kuin kattavuusryhmän nimikkeiden läpimenoaika. Lisäksi kannattaa käyttää vain dynaamisia negatiivisia päiviä ja määrittää negatiivisten päivien arvoksi se määrä päiviä, jonka olet valmis odottamaan, ennen kuin tilaat uuden täydennyksen varaston ollessa negatiivinen. (Toisin sanoen kyse on siitä, kuinka monta päivää olet valmis viivästyttämään kysyntää lisää). Lisäksi saman kattavuusryhmän nimikkeillä on oltava samanlaiset läpimenoajat.

Jos määrität negatiivisten päivien arvoksi **0** (nolla) etkä käytä dynaamisia negatiivisia päiviä, tarvesuunnittelu luo aina uuden suunnittelun tilauksen täyttämään kysynnän. Tässä tilanteessa on tärkeää, että käytät toimenpidesanomia, sillä voit estää niiden avulla varaston kasaantumisen.

Haluat ehkä määrittää negatiivisten päivien arvoksi pitkän aikarajan ja käyttää sitten toimenpidesanomia. Tällä tavoin saadaan hyvät suunnittelutulokset mutta sen toiminta on hieman hitaampaa. Lisäksi sen analysointi voi olla hankalaa, koska toimenpidesanomia on analysoitava ja käytettävä. Tässä on esimerkki:

- DemoProduct-nimikkeen oston läpimenoaika on kuusi päivää.
- DemoProduct-tuotteen varasto nollapäivänä (1. tammikuuta) on 0 (nolla).
- Saat nollapäivänä (1. tammikuuta) DemoProduct-nimikkeen myyntitilauksen, jonka määrä on 10.
- Saat yhdeksäntenä päivänä (10. tammikuuta) DemoProduct-nimikkeen myyntitilauksen, jonka määrä on 10.
- Yhdentenätoista päivänä (12. tammikuuta) on DemoProduct-nimikkeen ostotilaus, jonka määrä on 10.
- Negatiivisten päivien arvoksi määritetään **20**, joka on paljon suurempi arvo kuin nimikkeen läpimenoaika.

Seuraava kuva on graafinen esitys siitä, mitä tapahtuu.

![Esimerkin graafinen esitys.](./media/negative-days-19.png)

Tarvesuunnittelulla saadaan seuraavat tulokset.

![Tulosesimerkki 1.](./media/negative-days-20.png)

Edellisessä näyttökuvassa myyntitilauksen tarvepäivä on 9. eikä 10. tammikuuta Koska kyseinen näyttökuva otettiin 2015, jolloin 10. tammikuuta oli lauantai, tilauksen tarvepäivän pitäisi olla edellinen arkipäivä, joka oli perjantai 9. tammikuuta.

Tarvesuunnittelu luo suunnitellun ostotilauksen täyttämään ensimmäisen myyntitilauksen pyytämän kysynnän, minkä lisäksi se suosittelee myös suunnitellun tilauksen peruuttamista, koska voit siirtää aiemmin luodun ostotilauksen eteenpäin ja suurentaa sen määrää.

Tulokset eivät ole virheellisiä, mutta tarvesuunnittelun suoritusaika voi pidentyä, koska tarvesuunnittelun on luotava kaikki viiveet ja ehdotukset. Lisäksi suunnittelija tarvitsee ehkä enemmän aikaan tarvesuunnittelun tulosten tulkitsemiseen. Tässä tapauksessa on kuitenkin kaikkein tärkeintä, että suunnittelija ymmärtää toimenpidesanomat ja käyttää niitä.

Jos pienennät negatiivisten päivien arvon lähemmäksi nimikkeen läpimenoaikaa ja käytät dynaamisia negatiivisia päiviä, tarvesuunnittelulla saada seuraavat tulokset.

![Tulosesimerkki 2.](./media/negative-days-21.png)

Tarvesuunnittelu luo ensimmäiseen myyntitilaukseen liitetyn suunnitellun tilauksen. Sen jälkeen toinen myyntitilaus määritetään odotetusta aiemmin luodun myyntitilauksen perusteella negatiivisten päivien asetusten pohjalta. Myös tämä suunnittelutulos on oikein ja tarvesuunnittelun suoritusaika voi olla lyhyempi. Tässä tapauksessa ei ole välttämätöntä, että ymmärrät toimenpidesanomat ja osaat käyttää niitä.

Liiketoiminnan kannalta oikeiden arvojen antaminen edellyttää, että otat huomioon sekä toiminnallisuuden että tarvesuunnittelun suoritusajan. Tämän vuoksi optimaalisten arvojen löytäminen edellyttää ehkä kokeilujen tekemistä.

## <a name="see-also"></a>Lisätietoja

Lisätietoja on alkuperäisessä blogikirjoituksessa [Lisätietoja (dynaamisista) negatiivista päivistä](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
