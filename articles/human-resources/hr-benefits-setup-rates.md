---
title: Hintojen määrittäminen
description: Hinnat Microsoft Dynamics 365 Human Resourcesissa määrittävät, kuinka paljon työnantajat ja työntekijät edistävät etua.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f846dcd0a15424ac681dd7e6a229d9da445a54e1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092404"
---
# <a name="configure-rates"></a>Hintojen määrittäminen

[!include [banner](includes/preview-feature.md)]

Hinnat Microsoft Dynamics 365 Human Resourcesissa määrittävät, kuinka paljon työnantajat ja työntekijät edistävät etua. Arvo voi olla summa tai liukumakrediittejä määrityksestä riippuen.

Käytä useisiin tekijöihin perustuvia hintoja määrittämään, kuinka paljon työntekijät ja työnantajat maksavat jokaisesta edusta. Kattavuusprosentit ovat voimassa, joten voit säilyttää historiallisen hinnat. 

## <a name="set-up-rates"></a>Määritä hinnat

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Hinnat**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | Osuus | Yksilöivä nimi, joka yksilöi edun hinnan. |
   | Kuvaus | Edun hinnan kuvaus. |
   | Voimassa | Päivä, jolloin hinta on voimassa. Nykyinen järjestelmän päivämäärä on oletusarvo. 
   | Vanhentumisaika | Hinnan päättymispäivämäärä. 12/31/2154, (joka vastaa ei koskaan -arvoa) on oletusarvo. |
   | Käytä tasoja | Edun hinnan laskennassa käytettävä taso. Yhden kerroksen yhden tason edun kurssi tai kaksinkertainen taso kahden tason edun osalta. Kaksinkertainen taso on esimerkiksi sukupuoleen ja ikään perustuva taso. |
   | Maksun toistuvuus | Maksutiheys, joka määrittää, kuinka usein etupalkkio maksetaan edun tarjoajalle. Jos esimerkiksi toimitustiheys on kuukausi, edun korko vastaa kuukausittaista maksun määrää. |
   | Maksutiheyden asteen laskenta | Maksun tiheyslaskentamenetelmä: vakio tai vuosi. |
   | Maksutiheyden asteen pyöristys | Hinnan pyöristyksen menetelmä: vakio tai katkaistu. |
   | Tupakoimaton - työntekijän summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoimaton - työnantajan summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoitsija - työntekijän summa | Summa, jonka edun toimittaja veloittaa tupakoivasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoitsija - työnantajan summa | Summa, jonka edun toimittaja veloittaa tupakoivasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Hallinnollinen summa | Kolmannen osapuolen järjestelmänvalvojan veloittama hallinnollinen summa. Tämä on summa, jonka työnantaja maksaa kolmannen osapuolen hallinnoijalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Bonushyvitysten määrä | Liukumahyvitysten määrä, joka hyödyttää kustannuksia. Tämä koskee vain joustoluotto-ohjelmiin liittyvien etuusjärjestelyjen hintoja. Jos käytät tasohintoja, liukumaluoton korko määritetään toiminnot-> tasohintojen mukaan. |
   | Muutoksen voimaantulopäivämäärä | Päivämäärä, jolloin edun hintamuutos tulee voimaan. Järjestelmä muuttaa automaattisesti etuuskurssia ja päivittää kaikki tähän kurssiin liittyvät etuussuunnitelmat, kunhan suoritat kurssimuutoksen päivityskäsittelyn. Älä määritä tätä päivää, ellet halua, että järjestelmä päivittää työntekijän etuussuunnitelmat automaattisesti tämän taksan perusteella. Tämä on tavallisesti varattu automaattiseen tulevaan kurssimuutosten käsittelyyn. Muutoksen voimaantulopäivämäärän on oltava voimaantulo ja voimassaolon päättymispäivien sisällä. |
   | Asteen muutos on valmis | Kurssimuutos suoritettu -valintaruutu valitaan automaattisesti sen jälkeen, kun edun hinnanmuutokset on tehty hinnanmuutoksen päivityksen käsittelyn jälkeen. |

4. Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot**ja sitten **Versioiden ylläpito**.

5. Valitse **Tallenna**. 

## <a name="set-up-tier-rates"></a>Määritä tason hinnat

Voit käyttää tasoprosentteja hinnanmäärityksessä, jos hinta vaihtelee eri tekijöistä riippuen. Voit esimerkiksi määrittää tason, joka ilmoittaa, että jos ikäsi on enintään 34,99, tupakoimattomien summa on 2. Jos ikäsi on enintään 39,99, niin tupakoimattoman summa on 3.

Voit myös käyttää kaksinkertaista tasoa. Jos valitset **hinta-asetus**-lomakkeen **käyttötasojen** arvoksi **kaksitasoinen**, voit määrittää hinnat kahden dimension perusteella. Voit esimerkiksi määrittää kaksitasoisen järjestelmän, joka ilmoittaa, että jos olet mies ja ikäsi on enintään 34,99, tupakoimattomien summa on 2. Jos olet mies ja ikäsi on enintään 39,99, niin tupakoimattoman summa on 3. Jos olet nainen ja ikäsi on enintään 34,99, niin tupakoimattoman summa on 1,8. Jos olet nainen ja ikäsi on enintään 39,99, niin tupakoimattoman summa on 2,8.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Hinnat**.

2. Valitse luettelosta yksi tai useita hintoja, valitse **Toiminnot** ja sitten **Tasohinnat**.

3. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- | 
   | Kuvaus | Kuvaus-kentän arvo otetaan käyttöön kurssimääritystietueessa olevasta kuvauksesta. Tämän avulla voit määrittää, mihin hinnan asetuksiin tasohinnat on linkitetty. |
   | Tasokoodi | Tasokoodin valitseminen. Tasokoodit määritetään tasokoodit-lomakkeessa. Järjestelmä näyttää automaattisesti tasokoodin kuvauksen vasemmalla puolella olevassa ruudukossa. |
   | Tasotyyppi | Määrittää, mitä kenttää tulisi käyttää valintakriteerinä tason hinnan laskennassa. Esimerkki:</br></br><ul><li>Jos ikää käytetään, järjestelmä käyttää työntekijän syntymäaikaa edun hinnan laskennassa.</li><li>Jos hintaa käytetään, järjestelmä käyttää työntekijän vuosittaista etuuspalkkaa edun hinnan laskennassa.</li><li>Jos työtyyppiä käytetään, järjestelmä määrittää työntekijän nykyisen aktiivisen toimitietueen avulla työlajin työtyypin työtietueen perusteella.</li></ul></br></br>Määrittämistasotyypit ovat ikä, palkka, fyysinen, sukupuoli, kokopäiväinen, työlaji, kompensaatioalue ja taso. | 
   | Tasaa | Arvo, jota käytetään tasotyypin kanssa edun hinnan laskennassa. Esimerkki:</br></br><ul><li>Jos tasotyyppi on ikä, tämä on ikäarvo.</li><li>Jos tasotyyppi on palkka, tämä on palkka-arvo.</li><li> Jos tasotyyppi on työtyyppi, tämä on työtyyppi.</li></ul></br></br>Kun tasotyyppi on ikä tai palkka, järjestelmä käyttää nousevaa menetelmää tason valinnassa, mikä tarkoittaa, että Taso-kentän arvo edustaa tason alarajaa. Kun tasotyyppi on työlaji, järjestelmä käyttää tarkan vastaavuuden määrittämistapaa tason valinnassa. |
   | Laskentatyyppi | Määrittää, miten summaa käytetään Laske summa -kentässä ja mitä matemaattisia laskelmia tarvittaessa suoritetaan. Jos laskentatyyppi on tasasumma, järjestelmä käyttää summakenttiä sellaisenaan. Jos laskutyyppi on per $ palkan tai kattavuuden summa, järjestelmä käyttää laskutoimituksia ja laskusuuntaa matemaattisessa laskennassa.</br></br>Jos laskenta tyyppi on per $ summapalkkaa, järjestelmä käyttää seuraavaa matemaattista yhtälöä:</br></br>Vuotuinen etuuspalkka jaettuna laskun summalla (pyöristettynä ylös tai alas) kertaa työntekijän tai työnantajan tupakoitsijan tai tupakoimattomien määrät.</br></br>Jos laskentatyyppi on per $ kattavuuden summa, järjestelmä käyttää seuraavaa matemaattista yhtälöä:</br></br>Kattavuussumma jaettuna laskun summalla (pyöristettynä ylös tai alas) kertaa työntekijän tai työnantajan tupakoitsijan tai tupakoimattomien määrät.)</br></br>Molemmissa laskelmissa laskentasuuntaa käytetään sen määrittämiseen, pyöristetäänkö vuosittainen etuuspalkka vai kattavuussumma laskemalla summa ylös- tai alaspäin. |
   | Laskentasumma | Edun hinnan laskentaprosessissa käytettävä summa. Tämä summa on jakajana tasokoron matemaattisen laskemisen aikana. |
   | Laskelman suunta | Lasketun tulosmäärän pyöristyksen suunta (lisäys tai vähennys). Järjestelmä tukee kolmea laskentasuuntaa: tyhjää (tarkkaa menetelmää), lisäystä ja laskua.</br></br><ul><li>Jos arvo on tyhjä, järjestelmä käyttää palkan tai kattavuuden tarkkaa laskemista jaettuna laskennassa. Jos tällä arvolla on murtoluku, järjestelmä käyttää sitä laskennassa.</li><li>Jos korotus, järjestelmä kasvattaa palkan/kattavuuden matemaattisten arvojen laskemista jaettuna laskusummalla seuraavaan kokonaislukuun, mikä tarkoittaa, että 12,25 kasvaisi arvoon 13.</li><li>Jos lasku, järjestelmä vähentää palkan/kattavuuden matemaattisten arvojen laskemista jaettuna laskusummalla tämänhetkiseen kokonaislukuun, mikä tarkoittaa, että 12,25 vähentyisi arvoon 12.</li></ul> |
   | Tupakoimaton - työntekijän summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoimaton - työnantajan summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoitsija - työntekijän summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Tupakoitsija - työnantajan summa | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Hallinnollinen summa | Kolmannen osapuolen järjestelmänvalvojan veloittama hallinnollinen summa. Tämä on summa, jonka työnantaja maksaa kolmannen osapuolen hallinnoijalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | Bonushyvitys - määrä tupakoimattomalle | Joustohyvitysten määrä, joka perustuu lisäkustannuksiin, jotka perustuvat tupakoimattomien tasolla määritettyyn tasoon. Jos esimerkiksi laskentatyyppi on Per $ kattavuus, laskentasumma on 10 000 ja joustohyvityksen tupakoimattoman hinta on 6, mikä tarkoittaa, että jos työntekijä on valinnut $10 000 kattavuuden, se maksaa 6 liukumapistettä. Jos he valitsevat $ 20 000 kattavuuden, se maksaa 12 joustohyvitystä, ja niin edelleen. |
   | Bonushyvitykset - määrä tupakoivalle | Joustohyvitysten määrä, joka perustuu lisäkustannuksiin, jotka perustuvat tupakoivien tasolla määritettyyn tasoon. |

5. Valitse **Tallenna**. 
