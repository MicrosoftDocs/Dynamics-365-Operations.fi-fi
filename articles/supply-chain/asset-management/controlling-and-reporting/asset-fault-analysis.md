---
title: Resurssien vika-analyysi
description: Tässä ohjeaiheessa kerrotaan resurssivikojen analyysista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918438"
---
# <a name="asset-fault-analysis"></a>Resurssien vika-analyysi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Käyttöomaisuuden hallinnassa voit analysoida käyttöomaisuuden vikamerkintöjä, jolloin saat yleiskuvan tietyn kauden aikana rekisteröityjen vikojen kokonaismäärästä. Vikarekisteröintejä voidaan analysoida eri näkökulmista, esimerkiksi resurssien, resurssityyppien, toiminnallisten sijaintien, vian oireiden tai vikatyyppien näkökulmista.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen analyysi**.

2. **Resurssin vika-analyysin laskenta** -valintaikkunassa voit määrittää **Taso** -kentän avulla, miten yksityiskohtaisia haluat käyttöomaisuusvirherivien olevan toiminnallisia sijainteja ajatellen. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssivikarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

3. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät, virheiden syyt ja vikojen korjaukset **Sisällytettävät tietueet** -pikavälilehdessä.

4. Aloita laskenta valitsemalla **OK**.

5. Valitse **Resurssin vika-analyysi** -välilehdestä yksi tai useita painikkeita **Ryhmittely...** -toimintoruuturyhmissä, jolloin näkyviin tulee haluamasi yksityiskohtaisuuden taso. Aktivoidut painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

6. Valitse **Päivitä laskelmat**, jos haluat näyttää valintasi näytössä. 

>[!NOTE]
>Joka kerta, kun aktivoit tai poistat **Ryhmittely...**-toimintoruuturyhmien painikkeita, muista napsauttaa **Päivitä laskelmat** -painiketta, kun olet muuttanut valintoja. Tämä on tarpeen, koska suuri määrä tietoja käsitellään, kun virheiden todennäköisyys lasketaan uudelleen.

Vikamerkintöjä voi analysoida monella tavalla. Alla on esimerkkejä viidessä kuvakaappauksessa, joissa eri tietojen valinnat antavat erilaisia tietoja. Näet, miten eri valinnat tuottavat erilaisia tietoa ja yksityiskohtia, kun käyttöomaisuusvirheiden rekisteröintejä analysoidaan.

Alla olevassa kuvassa vain **Oire**-painike on valittuna.

- Vikarekisteröintejä on tehty kolmesta vian oireesta: "Air leak", "Blown fuse" ja "Equipment jammed".  
- **Todennäköisyys-%**-sarakkeessa kaikki prosentit ovat yhteensä 100 %. Todennäköisyys perustuu tämän vika-analyysin kaikkiin **Oire**-rekisteröinteihin.

![Kuva 1](media/06-controlling-and-reporting.png)


Alla olevassa kuvakaappauksessa lisätään **Vuosi** ja **Kuukausi**, joiden mukaan voit tarkastella vikamerkintöjä valitulta ajanjaksolta.

- Vikaoireet näkyvät nyt rekisteröinteinä vuodessa/kuukaudessa.  
- Jos lisäät kullekin kuukaudelle kaikki prosentit **Todennäköisyys-%**-sarakkeeseen, ne ova yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.

![Kuva 2](media/07-controlling-and-reporting.png)


- Resurssin ja resurssityypin yhdistelmää käytetään seuraavien kolmen kuvaruudun laskelmien perustana, mikä lisää yksityiskohtaisuutta.  
- Yleisesti ottaen **Ryhmittele päivämäärän mukaan**-, **Ryhmittele resurssin mukaan**-, **Ryhmittele toiminnallisen sijainnin mukaan** toimintoruuturyhmät samoin kuin **Vika**-painike (vian tunnus) sisältävät kausia tai resurssisuhteita. **Oire**-, **Alue**-, **Tyyppi**-, **Syy**- ja **Korjaus**-painikkeet ovat luokitteluja, joita käytetään vikojen hallinnassa analysoimaan vikarekisteröintejä ja merkitsemään ongelma-alueita.  

Alla olevassa kuvakaappauksessa **Resurssi** ja **Resurssityyppi** on lisätty antamaan tarkempia tietoja vikarekisteröinneistä.

- Vian oireet on nyt jaettu **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmiin.  
- Jos lisäät **Todennäköisyys-%**-sarakkeeseen kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ova yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.

![Kuva 3](media/08-controlling-and-reporting.png)


Alla olevassa kuvakaappauksessa **Alue** lisättiin **Oire**-, **Resurssi**- ja **Resurssityyppi** -yhdistelmään antamaan tarkempia tietoja vikarekisteröinneistä.

- Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**- ja **Alue**-yhdistelmään. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vika-alueista, joiden avulla voidaan selvittää, miten kyseisen vika-alueiden rekisteröinnin määrää voidaan rajoittaa.  

![Kuva 4](media/09-controlling-and-reporting.png)


Alla olevaan kuva kaappausruutuun lisättiin **Tyyppi**ja tässä esimerkissä näytetään tarkimmat laskennat.
 
- Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-, **Alue**- ja **Tyyppi**-yhdistelmään. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikatyypeistä, joiden avulla voidaan selvittää, miten kyseisen vikatyypin rekisteröinnin määrää voidaan rajoittaa.

![Kuva 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Saat yleiskuvan kaikista työtilauksiin ja ylläpitopyyntöihin luoduista vikarekisteröinneistä valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**. Valitse **Resurssin viat** -sivulla käyttöomaisuus virheiden kirjaaminen ja laajenna **Aiheeseen liittyviä tietoja** -ruutu, josta näet tietoja asiaan liittyvästä työtilauksesta tai ylläpitopyynnöstä.

