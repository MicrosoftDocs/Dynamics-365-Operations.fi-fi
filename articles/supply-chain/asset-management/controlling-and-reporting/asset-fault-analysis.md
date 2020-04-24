---
title: Resurssien vika-analyysi
description: Tässä ohjeaiheessa kerrotaan resurssivikojen analyysista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 67ccbb742bb4e2283c30b4dec055d137b4a51e40
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216410"
---
# <a name="asset-fault-analysis"></a>Resurssien vika-analyysi

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuuden hallinnassa voit analysoida käyttöomaisuuden vikamerkintöjä, jolloin saat yleiskuvan tietyn kauden aikana rekisteröityjen vikojen kokonaismäärästä. Vikarekisteröintejä voidaan analysoida eri näkökulmista, esimerkiksi resurssien, resurssityyppien, toiminnallisten sijaintien, vian oireiden tai vikatyyppien näkökulmista.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen analyysi**.

2. **Resurssin vika-analyysin laskenta** -valintaikkunassa voit määrittää **Taso** -kentän avulla, miten yksityiskohtaisia haluat käyttöomaisuusvirherivien olevan toiminnallisia sijainteja ajatellen. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssivikarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
        
    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

3. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät, virheiden syyt ja vikojen korjaukset **Sisällytettävät tietueet** -pikavälilehdessä.

4. Aloita laskenta valitsemalla **OK**.

5. Valitse **Resurssin vika-analyysi** -välilehdestä yksi tai useita **Ryhmittely...** -painikkeita, jolloin näkyviin tulee haluamasi yksityiskohtaisuuden taso. Aktivoidut painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

6. Valitse **Päivitä laskelmat**, jos haluat näyttää valintasi näytössä. 

>[!NOTE]
>Aina kun otat käyttöön **Ryhmittele...**-painikkeen tai poistat sellaisen käytöstä, muista napsauttaa **Päivitä laskelmat**-painiketta. Tämä on tarpeen, koska suuri määrä tietoja käsitellään, kun virheiden todennäköisyys lasketaan uudelleen.

## <a name="examples"></a>Esimerkkejä

Vikamerkintöjä voi analysoida monella tavalla. Tämä osa sisältää viisi esimerkkiä siitä, miten erilaiset tietovalinnat voivat tuottaa erilaisia tietoa ja yksityiskohtia, kun käyttöomaisuusvirheiden rekisteröintejä analysoidaan.

### <a name="group-by-symptoms"></a>Oireiden mukaan ryhmittely

Alla olevassa kuvassa vain **Oire**-painike on valittuna.

- Vikarekisteröintejä on tehty kolmesta vian oireesta: "Air leak", "Blown fuse" ja "Equipment jammed".  
- **Todennäköisyys-%**-sarakkeessa kaikki prosentit ovat yhteensä 100 %. Todennäköisyys perustuu tämän vika-analyysin kaikkiin **Oire**-rekisteröinteihin.

![Kuva 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Oireiden ja ajanjakson mukaan ryhmittely

Alla olevassa kuvakaappauksessa lisätään **Vuosi** ja **Kuukausi**, joiden mukaan voit tarkastella vikamerkintöjä valitulta ajanjaksolta.

- Vikaoireet näkyvät nyt rekisteröinteinä vuodessa/kuukaudessa.  
- Jos lisäät kullekin kuukaudelle kaikki prosentit **Todennäköisyys-%**-sarakkeeseen, ne ova yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.

![Kuva 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Useiden oireiden ja resurssien mukaan ryhmittely

Resurssin ja resurssityypin yhdistelmää käytetään seuraavien kolmen kuvaruudun laskelmien perustana, mikä lisää yksityiskohtaisuutta.  

Yleisesti ottaen **Ryhmittele päivämäärän mukaan**-, **Ryhmittele resurssin mukaan**-, **Ryhmittele toiminnallisen sijainnin mukaan** toimintoruuturyhmät samoin kuin **Vika**-painike (vian tunnus) sisältävät kausia tai resurssisuhteita. **Oire**-, **Alue**-, **Tyyppi**-, **Syy**- ja **Korjaus**-painikkeet ovat luokitteluja, joita käytetään vikojen hallinnassa analysoimaan vikarekisteröintejä ja merkitsemään ongelma-alueita.  

**Ryhmittele oireen, resurssin ja resurssityypin mukaan**

Alla olevassa kuvakaappauksessa **Resurssi** ja **Resurssityyppi** on lisätty antamaan tarkempia tietoja vikarekisteröinneistä.

- Vian oireet on nyt jaettu **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmiin.  
- Jos lisäät **Todennäköisyys-%**-sarakkeeseen kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ova yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-rekisteröinteihin. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikaoireista, joiden avulla voidaan selvittää, miten kyseisen vian oireiden rekisteröinnin määrää voidaan rajoittaa.

![Kuva 3](media/08-controlling-and-reporting.png)

**Ryhmittele kahden oireen, resurssin ja resurssityypin mukaan**

Alla olevassa kuvakaappauksessa **Alue** lisättiin **Oire**-, **Resurssi**- ja **Resurssityyppi** -yhdistelmään antamaan tarkempia tietoja vikarekisteröinneistä.

- Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**- ja **Alue**-yhdistelmään. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vika-alueista, joiden avulla voidaan selvittää, miten kyseisen vika-alueiden rekisteröinnin määrää voidaan rajoittaa.  

![Kuva 4](media/09-controlling-and-reporting.png)

**Ryhmittele kolmen oireen, resurssin ja resurssityypin mukaan**

Alla olevaan kuva kaappausruutuun lisättiin **Tyyppi**ja tässä esimerkissä näytetään tarkimmat laskennat.
 
- Jos lisäät **Todennäköisyys-%**-sarakkeeseen resurssin kaikki prosentit **Resurssi** / **Resurssityyppi** / **Oire** -yhdistelmälle, ne ovat yhteensä enintään 100 %. Todennäköisyys perustuu tämän vika-analyysin **Oire**-, **Alue**- ja **Tyyppi**-yhdistelmään. Jos käyttöomaisuuserälle on suuri määrä rivejä, mutta suuri prosenttiosuus erottuu riviltä, se on merkki vikatyypeistä, joiden avulla voidaan selvittää, miten kyseisen vikatyypin rekisteröinnin määrää voidaan rajoittaa.

![Kuva 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Saat yleiskuvan kaikista työtilauksiin ja ylläpitopyyntöihin luoduista vikarekisteröinneistä valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**. Valitse **Resurssin viat** -sivulla käyttöomaisuus virheiden kirjaaminen ja laajenna **Aiheeseen liittyviä tietoja** -ruutu, josta näet tietoja asiaan liittyvästä työtilauksesta tai ylläpitopyynnöstä.

