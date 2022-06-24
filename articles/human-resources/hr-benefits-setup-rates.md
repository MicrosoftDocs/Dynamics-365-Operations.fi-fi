---
title: Hintojen määrittäminen
description: Hinnat Microsoft Dynamics 365 Human Resourcesissa määrittävät, kuinka paljon työnantajat ja työntekijät edistävät etua.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039b4aa3f044cda29944bcd4f5c42fc35818c58b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868156"
---
# <a name="configure-rates"></a>Hintojen määrittäminen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hinnat määrittävät, kuinka paljon työnantajat ja työntekijät maksavat edusta. Arvo voi olla summa tai määrä liukumakrediittejä määrityksestä riippuen.

Käytä useisiin tekijöihin perustuvia hintoja määrittämään, kuinka paljon työntekijät ja työnantajat maksavat jokaisesta edusta. Kattavuusprosentit ovat voimassa, joten voit säilyttää historiallisen hinnat. 

## <a name="set-up-rates"></a>Määritä hinnat

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Hinnat**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Osuus** | Yksilöivä nimi, joka yksilöi edun hinnan. |
   | **Kuvaus** | Edun hinnan kuvaus. |
   | **Voimassa** | Päivämäärä, jolloin hinta tulee voimaan. Nykyinen järjestelmän päivämäärä on oletusarvo. Tämän päivämäärän tulee olla etuusjaksolla tai sitä ennen. Hyvä käytäntö on asettaa tämä päivämäärä etuussuunnitelman päivämääräksi. |
   | **Vanhentumisaika** | Hinnan päättymispäivämäärä. 12/31/2154, (joka vastaa ei koskaan -arvoa) on oletusarvo. |
   | **Käytä tasoja** |  Käytä tätä kenttää, jos sinulla on logiikka, jota on käytettävä hinnan määrittämiseen. Jos hinnan on esimerkiksi noustava iän perusteella, valitse arvo tästä. Valitse **Yksi taso** yksitasoiselle etuuden hinnalle tai **Kaksi tasoa** kaksitasoiselle etuuden hinnalle. Kaksi tasoa on esimerkiksi sukupuoleen ja ikään perustuva taso. Kun olet valinnut arvon, valitse **Toiminnot** ja valitse sitten **Tasohinnat**. Jos kiinteä hinta ei muutu, jätä tämä kenttä tyhjäksi. |
   | **Maksun toistuvuus** | Määritä, kuinka usein etuusvakuutusmaksu maksetaan etuuden tarjoajalle. Myöhemmin tässä artikkelissa kuvatulla sivulla syöttämäsi hinnat perustuvat tässä määrittämääsi maksuväliin. Jos esimerkiksi kirjoitat tähän kenttään **Kuukausittain** ja kirjoitat työntekijämaksuksi **100** euroa, oletetaan, että etu maksaa työntekijälle 100 euroa kuukaudessa. Työntekijälle voidaan kuitenkin maksaa kaksi kertaa kuukaudessa työntekijätietueeseen määritettyjen etuuksien maksutiheyden perusteella. Tässä tapauksessa, kun työntekijä kirjautui **työntekijän itsepalveluun**, hänen maksamaansa summa on 50 euroa, koska **työntekijän itsepalvelun** näyttämä hinta perustuu työntekijän maksutiheyteen. |
   | **Maksutiheyden asteen pyöristys** | Pyöristystavat ovat vakio-, katkaistu, normaali, alaspäin ja ylöspäin pyöristys. </br></br><ul><li>**Vakio** - Pyöristä aina ylöspäin. Esimerkiksi 10,611 pyöristetään 10,62:ksi. -10,231 pyöristetään -10,23:ksi. </li><li>**Katkaistu** - Pyöristä aina alaspäin. Esimerkiksi 10,619 pyöristetään 10,61:ksi. -10,231 pyöristetään -10,24:ksi. </li><li>**Normaali** - Desimaaliarvot, jotka päättyvät tai ovat suurempia kuin 5, pyöristyvät nollasta pois päin. Desimaaliarvot, jotka päättyvät enintään 4:ään pyöristetään nollaa kohti. Esimerkiksi 10,615 pyöristetään 10,62:ksi. -10,235 pyöristetään -10,24:ksi. 10,614 pyöristetään 10,61:ksi. -10,234 pyöristetään -10,23:ksi. </li><li>**Alaspäin** - Pyöristys nollaa kohti. Esimerkiksi 10,619 pyöristetään 10,61:ksi. -10,231 pyöristetään -10,23:ksi. </li><li>**Pyöristys ylös** - Pyöristys nollasta pois päin. Esimerkiksi 10,619 pyöristetään 10,62:ksi. -10,231 pyöristetään -10,24:ksi. |
   | **Tupakoimaton - työntekijän summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoimaton - työnantajan summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoitsija - työntekijän summa** | Summa, jonka edun toimittaja veloittaa tupakoivasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoitsija - työnantajan summa** | Summa, jonka edun toimittaja veloittaa tupakoivasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Hallinnollinen summa** | Kolmannen osapuolen järjestelmänvalvojan veloittama hallinnollinen summa. Tämä on summa, jonka työnantaja maksaa kolmannen osapuolen hallinnoijalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Bonushyvitysten määrä** | Liukumahyvitysten määrä, joka hyödyttää kustannuksia. Tämä koskee vain joustoluotto-ohjelmiin liittyvien etuusjärjestelyjen hintoja. Jos käytät tasohintoja, liukumaluoton korko määritetään toiminnot-> tasohintojen mukaan. |
   | **Muutoksen voimaantulopäivämäärä** | Päivämäärä, jolloin edun hintamuutos tulee voimaan. Järjestelmä muuttaa automaattisesti etuuskurssia ja päivittää kaikki tähän kurssiin liittyvät etuuspalvelupaketit, kunhan suoritat kurssimuutoksen päivityskäsittelyn. Älä määritä tätä päivää, ellet halua, että järjestelmä päivittää työntekijän etuussuunnitelmat automaattisesti tämän taksan perusteella. Tämä on tavallisesti varattu automaattiseen tulevaan kurssimuutosten käsittelyyn. **Muutoksen voimaantulopäivämäärän** on oltava voimaantulo ja voimassaolon päättymispäivien sisällä. |
   | **Asteen muutos on valmis** | **Kurssimuutos suoritettu** -valintaruutu valitaan automaattisesti sen jälkeen, kun edun hinnanmuutokset on tehty hinnanmuutoksen päivityksen käsittelyn jälkeen. |

4. Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot** ja sitten **Versioiden ylläpito**.

5. Valitse **Tallenna**. 

## <a name="set-up-tier-rates"></a>Määritä tason hinnat

Voit käyttää tasoprosentteja hinnanmäärityksessä, jos hinta vaihtelee eri tekijöistä riippuen. Voit esimerkiksi määrittää tason, joka ilmoittaa, että jos ikäsi on enintään 34,99, tupakoimattomien summa on 2. Jos ikäsi on enintään 39,99, niin tupakoimattoman summa on 3.

Voit myös käyttää kaksinkertaista tasoa. Jos valitset **hinta-asetus**-lomakkeen **käyttötasojen** arvoksi **kaksitasoinen**, voit määrittää hinnat kahden dimension perusteella. Voit esimerkiksi määrittää kaksitasoisen järjestelmän, joka ilmoittaa, että jos olet mies ja ikäsi on enintään 34,99, tupakoimattomien summa on 2. Jos olet mies ja ikäsi on enintään 39,99, niin tupakoimattoman summa on 3. Jos olet nainen ja ikäsi on enintään 34,99, niin tupakoimattoman summa on 1,8. Jos olet nainen ja ikäsi on enintään 39,99, niin tupakoimattoman summa on 2,8.

> [!IMPORTANT]
> Työntekijätietueen **Henkilötiedot**-kentässä olevalla vaihtoehdolla ilmaistaan, onko työntekijä tupakoitsija. Jos työntekijä kirjataan tupakoitsijaksi, käytetään tupakoitsijan hintaa. (Tupakoitsijanäyttöä ei koskaan näytetä työntekijälle.)
   
1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Hinnat**.

2. Valitse luettelosta yksi tai useita hintoja, valitse **Toiminnot** ja sitten **Tasohinnat**.

3. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | kuvaus |
   | --- | --- | 
   | **Kuvaus** | **Kuvaus**-kentän arvo otetaan käyttöön kurssimääritystietueessa olevasta kuvauksesta. Tämän avulla voit määrittää, mihin hinnan asetuksiin tasohinnat on linkitetty. |
   | **Tasokoodi** | Tasokoodin valitseminen. **Tasokoodit** määritetään tasokoodit-lomakkeessa. Järjestelmä näyttää automaattisesti tasokoodin kuvauksen vasemmalla puolella olevassa ruudukossa. |
   | **Tasotyyppi** | Määrittää, mitä kenttää tulisi käyttää valintakriteerinä tason hinnan laskennassa. Esimerkki:</br></br><ul><li>Jos **ikää** käytetään, järjestelmä käyttää työntekijän syntymäaikaa edun hinnan laskennassa.</li><li>Jos **palkkaa** käytetään, järjestelmä käyttää työntekijän vuosittaista etuuspalkkaa edun hinnan laskennassa.</li><li>Jos **työtyyppiä** käytetään, työntekijän nykyistä aktiivista toimitietuetta käytetään työtyypin määrittämiseen toimeen liitetyn työtietueen perusteella.</li></ul></br></br>Määrittämistasotyypit ovat **ikä**, **palkka**, **fyysinen**, **sukupuoli**, **kokopäiväinen**, **työlaji**, **kompensaatioalue** ja **taso**. | 
   | **Tasaa** | Arvo, jota käytetään tasotyypin kanssa edun hinnan laskennassa. Esimerkki:</br></br><ul><li>Jos tasotyyppi on **ikä**, tämä on ikäarvo.</li><li>Jos tasotyyppi on **palkka**, tämä on palkka-arvo.</li><li> Jos tasotyyppi on **työtyyppi**, tämä on työtyyppi.</li></ul></br></br>Kun tasotyyppi on **ikä** tai **palkka**, **Taso**-kentän arvo esittää tason ylemmän sidonnan. Kun tasotyyppi on **työlaji**, käytetään tarkan vastaavuuden määrittämistapaa tason valinnassa. |
   | **Laskentalaji** | Määrittää, miten summaa käytetään Laske summa -kentässä ja mitä matemaattisia laskelmia tarvittaessa suoritetaan. Jos laskentatyyppi on tasasumma, käytetään summakenttiä sellaisenaan. Jos laskutyyppi on per $ palkan tai kattavuuden summa, käytetään laskutoimituksia ja laskusuuntaa matemaattisessa laskennassa.</br></br>Jos laskenta tyyppi on per $ summapalkkaa, käytetään seuraavaa matemaattista yhtälöä:</br></br>Vuotuinen etuuspalkka jaettuna laskun summalla (pyöristettynä ylös tai alas) kertaa työntekijän tai työnantajan tupakoitsijan tai tupakoimattomien määrät.</br></br>Jos laskenta tyyppi on per $ kattavuuden summa, käytetään seuraavaa matemaattista yhtälöä:</br></br>Kattavuussumma jaettuna laskun summalla (pyöristettynä ylös tai alas) kertaa työntekijän tai työnantajan tupakoitsijan tai tupakoimattomien määrät.)</br></br>Molemmissa laskelmissa laskentasuuntaa käytetään sen määrittämiseen, pyöristetäänkö vuosittainen etuuspalkka vai kattavuussumma laskemalla summa ylös- tai alaspäin. |
   | **Laskentasumma** | Edun hinnan laskentaprosessissa käytettävä summa. Tämä summa on jakajana tasokoron matemaattisen laskemisen aikana. |
   | **Laskelman suunta** | Lasketun tulosmäärän pyöristyksen suunta. Järjestelmä tukee kolmea laskentasuuntaa: tyhjää (tarkkaa menetelmää), **lisäystä** ja **laskua**.</br></br><ul><li>Jos arvo on tyhjä, järjestelmä käyttää palkan tai kattavuuden tarkkaa laskemista jaettuna laskennassa. Jos tällä arvolla on murtoluku, tätä käytetään laskennassa.</li><li>Jos **korotus**, kasvatetaan palkan/kattavuuden matemaattisten arvojen laskemista jaettuna laskusummalla seuraavaan kokonaislukuun, mikä tarkoittaa, että 12,25 suurenisi arvoon 13.</li><li>Jos **lasku**, vähennetään palkan/kattavuuden matemaattisten arvojen laskemista jaettuna laskusummalla tämänhetkiseen kokonaislukuun, mikä tarkoittaa, että 12,25 pienenisi arvoon 12.</li></ul> |
   | **Tupakoimaton - työntekijän summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoimaton - työnantajan summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoitsija - työntekijän summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Tupakoitsija - työnantajan summa** | Summa, jonka edun toimittaja veloittaa tupakoimattomasta työntekijästä. Tämä on summa, jonka työnantaja maksaa edun tarjoajalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Hallinnollinen summa** | Kolmannen osapuolen järjestelmänvalvojan veloittama hallinnollinen summa. Tämä on summa, jonka työnantaja maksaa kolmannen osapuolen hallinnoijalle ja joka perustuu hinta-asetusten maksutiheyteen. |
   | **Bonushyvitys - määrä tupakoimattomalle** | Joustohyvitysten määrä, joka perustuu lisäkustannuksiin, jotka perustuvat tupakoimattomien tasolla määritettyyn tasoon. Jos esimerkiksi laskentatyyppi on **Per $ kattavuus**, laskentasumma on 10 000 ja joustohyvityksen tupakoimattoman hinta on 6, mikä tarkoittaa, että jos työntekijä on valinnut $10 000 kattavuuden, se maksaa 6 liukumapistettä. Jos he valitsevat $ 20 000 kattavuuden, se maksaa 12 joustohyvitystä, ja niin edelleen. |
   | **Bonushyvitykset - määrä tupakoivalle** | Joustohyvitysten määrä, joka perustuu lisäkustannuksiin, jotka perustuvat tupakoivien tasolla määritettyyn tasoon. |

5. Valitse **Tallenna**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
