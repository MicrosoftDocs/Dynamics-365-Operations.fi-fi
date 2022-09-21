---
title: Maksuvälineperusteiset alennukset
description: Tässä artikkelissa kerrotaan maksuvälineperusteisesta alennustoiminnosta, jonka avulla vähittäiskauppiaat voivat määrittää alennuksia tietyille maksuvälinetyypeille Microsoft Dynamics 365 Commercessa.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473777"
---
# <a name="tender-based-discount"></a>Maksuvälineperusteinen alennus

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan maksuvälineperusteisesta alennustoiminnosta, jonka avulla vähittäiskauppiaat voivat määrittää alennuksia tietyille maksuvälinetyypeille Microsoft Dynamics 365 Commercessa.

Vähittäiskauppiaiden keskuudessa on yleistä julkaista yksityisiä brändättyjä luottokortteja. Vähittäiskauppiaat hyötyvät siitä, koska he saavat edullisia palveluja pankeilta. Koska nämä luottokortit voivat lisäksi kannustaa asiakkaita käymään kaupassa useammin, ne auttavat kauppiaan tuloksen parantamisessa. Siksi vähittäiskauppiaiden kannattaa lisätä asiakkaidensa brändättyjen luottokorttien käyttöä. Tämän tavoitteen saavuttamiseksi kauppiaat tarjoavat usein lisäalennuksia näitä kortteja käyttäville asiakkaille.

Sellaiset kauppiaat, jotka eivät tarjoa brändättyjä luottokortteja, taas saattavat kannustaa asiakkaitaan maksamaan muilla maksuvälineillä, kuten käteisellä, lahjakorteilla tai kanta-asiakaspisteillä. Tällä tavoin kauppiaat voivat vähentää luottokorttien käsittelymaksuista aiheutuvia kuluja. Tämän vuoksi vähittäiskauppiaat saattavat tarjota alennuksia asiakkaille, jotka käyttävät näitä vaihtoehtoisia maksuvälineitä.

## <a name="tender-based-discount"></a>Maksuvälineperusteinen alennus

Commerce tukee *maksuvälineperusteista alennusta*, jonka avulla vähittäismyyjät voivat määrittää tapahtumaan kohdistettavan alennusprosentin, jos tapahtuman kokonaissumma ylittää tietyn summan ja asiakas maksaa käyttämällä ensisijaista maksutyyppiä. Maksuvälineperusteinen alennus perustuu tasoihin, joten eri alennusprosentit voidaan liittää erilaisiin summarajoihin. Asiakas voi päättää, suorittaako hän kokonaisen vai osittaisen maksun, ja hinnoittelumoduuli määrittää asianmukaisen alennusmäärän. Maksuvälineperusteinen alennus annetaan aina myyntirivien veroja edeltävää summaa.

Maksuvälineperusteinen alennus voidaan kohdistaa vain myyntiriveille, joilla hintoja ei ole lukittu, ja joilla alennus on jaettu suhteellisesti kelvollisille riveille. Jos tilaukseen lisätään uusia myyntirivejä, maksuvälineperusteistä alennusta sovelletaan uusiin myyntiriveihin vasta maksamisen yhteydessä. Kun asiakkaan nouto- tai toimitustilausta tehdään, maksuvälineperusteista alennusta sovelletaan vain talletussummaan. Kun tilaus on tehty, myyntirivien hinnat lukitaan sen täyttämisen ajaksi. Yhtäkään maksuvälineperusteista alennusta ei sovelleta mihinkään saldoon, joka maksetaan noudon yhteydessä tai hyväksytään toimituksen yhteydessä. Maksuvälineperusteista alennusta voidaan soveltaa asiakkaan tilauksen koko summaan vain, jos vähittäiskauppias kerää koko summan talletuksena tilauksen tekemisen yhteydessä.

Maksuvälineperusteiset alennukset eivät kilpaile nimikeperusteisten alennusten kanssa. Nimikeperusteisia alennuksia ovat esimerkiksi yksinkertaiset alennukset, laatualennukset, raja-alennukset, yhdistelmäalennukset sekä manuaaliset alennukset. Maksuvälineperusteiset alennukset muodostuvat aina nimikeperusteisten alennusten päälle. Siten, vaikka nimikkeeseen sovellettaisiin eksklusiivista alennusta, maksuvälineperusteista alennusta voi silti käyttää edelleen eksklusiivisen alennuksen lisäksi. Samoin, jos tapahtumaan sovelletaan kynnysalennusta ja maksuvälineperusteinen alennus vähentää summan kynnyksen alittavaksi, kynnysalennusta sovelletaan edelleen tapahtumaan.

Vaikka maksuvälineperusteiset alennukset pienentävät tapahtuman välisummaa, ne eivät vaikuta tapahtumaan sovellettaviin automaattisiin veloituksiin. Jos toimitusmaksuksi lasketaan 5 euroa, koska välisumma oli yli 100 euroa, ja maksuvälineperusteinen alennus pienentää summaa alle 100 euroon, toimitusmaksu pysyy 5 eurossa.

Maksuvälineperusteinen alennus on tällä hetkellä rajoitettu kahteen maksutapaan, jotka ovat luottokortti ja käteinen. Jos maksutyypille määritetään useita maksuvälineperusteisia alennuksia, sovelletaan vain parasta maksuvälineperusteista alennusta.

## <a name="pos-user-experience"></a>POS:n käyttökokemus

Jos maksuvälineperusteinen alennus on määritetty käteiselle ja kassavirkailija valitsee myyntipisteessä (POS) **Maksa käteisellä** -painikkeen itsepalvelutukkutapahtuman maksamiseksi, maksuvälineperusteista alennusta sovelletaan tapahtumaan automaattisesti. Tällöin saldona näkyy pienennetty summa. Jos kassavirkailija kuitenkin valitsee maksuruudulla **Takaisin**-painikkeen, alennus poistetaan ja tapahtumaruudulla näkyy alkuperäinen summa. Maksuvälineperusteinen alennus poistetaan, jos maksurivi mitätöidään.

Luottokorttimaksuille vähittäiskauppiaat voivat määrittää maksuvälineperusteisen alennuksen yhdelle tai useammalle luottokorttityypille. Järjestelmä ei kuitenkaan pysty vahvistamaan käytettävän luottokortin tyyppiä, ellei korttia ole hyväksytty, Jos alennus sovelletaan hyväksymisen jälkeen, maksun hyväksynnässä käytetään suurempaa summaa, mutta maksun taltioinnissa käytetään pienempää summaa. Tämän tilanteen ehkäisemiseksi kassavirkailijalle näytetään asiakkaan luottokorttimaksun yhteydessä valintaikkuna, joka sisältää mahdolliset ensisijaiset luottokortit, jotka tarjoavat asiakkaalle lisäalennuksen. Kassavirkailija voi tällöin kysyä, haluaako asiakas käyttää jotakin lisäalennukseen oikeuttavista korteista. Jos kassavirkailija valitsee alennukseen oikeuttavan kortin, maksuvälineperusteista alennusta sovelletaan tapahtumaan ja pienennetty summa näkyy maksuruudussa. Hyväksyntä koskee tällöin pienennettyä summaa. Jos asiakas syöttää kassavirkailijan valinnan vastaisen kortin, näkyviin tulee virhesanoma ja hyväksyntä mitätöidään.

## <a name="call-center-user-experience"></a>Puhelinkeskuksen käyttökokemus

Kun puhelinkeskuksen käyttäjä valitsee **Valmis**-kohdan puhelintilauksen aikana, näkyviin tulle **Summat**-ruutu. Tämän ruudun summissa ei alkuun näy maksuperäisiä alennuksia, koska maksutapaa ei vielä ole valittu. Jos käyttäjä valitsee **Lisää maksu** -ruudussa maksutavan, jolle maksuvälineperusteinen alennus on määritetty, maksun summa korjataan automaattisesti ottamaan alennus huomioon. Puhelinkeskuksen asiakas voi päättää samalla tavalla kuin myyntipisteellä, haluaako hän suorittaa maksun kokonaan vai osittain. Myyntitilaukseen sovelletaan maksuvälineperusteista alennusta maksetun summan perusteella.

> [!NOTE]
> Puhelinkeskustilauksissa ei varmenneta kortteja. Jos puhelinkeskuksen käyttäjä esimerkiksi valitsee Visan luottokortiksi, mutta asiakas käyttää Mastercardia, järjestelmä soveltaa alennusta tästä huolimatta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
