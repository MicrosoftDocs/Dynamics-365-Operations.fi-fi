---
title: Maksuvälineperusteiset alennukset
description: Tässä aiheessa esitetään yleiskatsaus toimintoon, jonka avulla vähittäiskauppiaat voivat määrittää alennuksia tietyille maksuvälinetyypeille.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 98631d8f9fb2c05621f69fa67c9b60472198ee6b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232564"
---
# <a name="tender-based-discounts"></a>Maksuvälineperusteiset alennukset

[!include [banner](includes/banner.md)]


Vähittäiskauppiaiden keskuudessa on yleistä julkaista yksityisiä brändättyjä luottokortteja. Vähittäiskauppiaat hyötyvät siitä, koska he saavat edullisia palveluja pankeilta. Koska nämä luottokortit voivat lisäksi kannustaa asiakkaita käymään kaupassa useammin, ne auttavat kauppiaan tuloksen parantamisessa. Siksi vähittäiskauppiaiden kannattaa lisätä asiakkaidensa brändättyjen luottokorttien käyttöä. Tämän tavoitteen saavuttamiseksi kauppiaat tarjoavat usein lisäalennuksia näitä kortteja käyttäville asiakkaille.

Sellaiset kauppiaat, jotka eivät tarjoa brändättyjä luottokortteja, taas saattavat kannustaa asiakkaitaan maksamaan muilla maksuvälineillä, kuten käteisellä, lahjakorteilla tai kanta-asiakaspisteillä. Tällä tavoin kauppiaat voivat vähentää luottokorttien käsittelymaksuista aiheutuvia kuluja. Tämän vuoksi vähittäiskauppiaat saattavat tarjota alennuksia asiakkaille, jotka käyttävät näitä vaihtoehtoisia maksuvälineitä.

Microsoft Dynamics 365 Commercessa jälleenmyyjät voivat määrittää alennusprosentin, jota sovelletaan kelvollisiin riveihin, jos asiakas maksaa halutulla maksuvälineellä. Asiakas voi päättää, suorittaako hän kokonaisen vai osittaisen maksun, ja Commerce määrittää asianmukaisen alennusmäärän. Huomaa, että alennus annetaan aina kelvollisten nimikkeiden hinnasta ennen veroja.

Maksuvälineperusteiset alennukset eivät kilpaile nimikeperusteisten alennusten, kuten kausittaisten tai manuaalisten alennusten, kanssa. Ne muodostuvat aina nimikealennusten päälle. Siten, vaikka nimikkeeseen sovellettaisiin eksklusiivista kausialennusta, maksuvälineperusteista alennusta sovelletaan edelleen kausialennuksen lisäksi. Samoin, jos tapahtumaan sovelletaan kynnysalennusta ja maksuvälineperusteinen alennus vähentää summan kynnyksen alittavaksi, kynnysalennusta sovelletaan edelleen tapahtumaan.

Vaikka maksuvälineperusteiset alennukset pienentävät tapahtuman välisummaa, ne eivät vaikuta tapahtumaan sovellettaviin automaattisiin veloituksiin. Jos toimitusmaksuksi lasketaan 5 euroa, koska välisumma oli yli 100 euroa, ja maksuvälineperusteinen alennus pienentää summaa alle 100 euroon, toimitusmaksu pysyy 5 eurossa.


> [!NOTE]
> Maksuvälineperusteiset alennukset jaetaan suhteellisesti kelvollisille myyntiriveille, ja ne pienentävät yksittäisten rivien veroja edeltävää summaa. Jos maksuvälineelle (kuten käteiselle) määritetään useita maksuvälineperusteisia alennuksia, sovelletaan vain parasta maksuvälineperusteista alennusta.

Maksuvälineperusteisia alennuksia voi soveltaa vain myyntiriveihin, joiden hinnat eivät ole lukittuja. Jos tilaukseen lisätään uusia myyntirivejä, maksuvälineperusteistä alennusta sovelletaan uusiin myyntiriveihin vasta maksamisen yhteydessä. Kun asiakkaan nouto- tai toimitustilausta tehdään, maksuvälineperusteista alennusta sovelletaan vain talletussummaan. Kun tilaus on tehty, myyntirivien hinnat lukitaan sen täyttämisen ajaksi. Siksi mitään maksuvälineperusteista alennusta ei sovelleta mihinkään saldoon, joka maksetaan noudon yhteydessä tai hyväksytään toimituksen yhteydessä. Maksuvälineperusteista alennusta voidaan soveltaa asiakkaan tilauksen koko summaan vain, jos vähittäiskauppias kerää koko summan talletuksena tilauksen tekemisen yhteydessä.

> [!IMPORTANT]
> Commercessa maksuvälineperusteiset alennukset on tällä hetkellä rajoitettu kahteen maksutapaan eli luottokortteihin ja käteiseen.

## <a name="pos-user-experience"></a>POS:n käyttökokemus

Jos maksuvälineperusteinen alennus on määritetty käteiselle ja kassavirkailija valitsee myyntipisteessä (POS) painikkeen, joka on liitetty Maksa käteisellä -toimintoon, maksuvälineperusteista alennusta sovelletaan tapahtumaan automaattisesti. Tällöin saldona näkyy pienennetty summa. Jos kassavirkailija kuitenkin valitsee maksuruudulla **Takaisin**-painikkeen, alennus poistetaan ja tapahtumaruudulla näkyy alkuperäinen summa. Maksuvälineperusteinen alennus poistetaan, jos maksurivi mitätöidään.

Korttimaksujen osalta vähittäiskauppiaat voivat määrittää maksuvälineperusteisen alennuksen yhdelle tai useammalle luottokorttityypille. Järjestelmä ei kuitenkaan pysty vahvistamaan käytettävän luottokortin tyyppiä, ellei korttia ole hyväksytty, Jos alennus sovelletaan hyväksymisen jälkeen, maksun hyväksynnässä käytetään suurempaa summaa, mutta maksun taltioinnissa käytetään pienempää summaa.

Tämän tilanteen ehkäisemiseksi kassavirkailija näkee asiakkaan luottokorttimaksun yhteydessä valintaikkunan, joka sisältää luettelon asiakkaalle lisäsäästöä tarjoavista luottokorteista. Kassavirkailija voi tällöin kysyä, haluaako asiakas käyttää jotakin lisäalennukseen oikeuttavista korteista. Jos kassavirkailija käyttää alennukseen oikeuttavaa korttia, maksuvälineperusteista alennusta sovelletaan tapahtumaan ja pienennetty summa näkyy maksuruudussa. Hyväksyntä koskee tällöin pienennettyä summaa. Jos asiakas syöttää kassavirkailijan valinnan vastaisen kortin, näkyviin tulee virhesanoma ja hyväksyntä mitätöidään.


## <a name="call-center-user-experience"></a>Puhelinkeskuksen käyttökokemus

Kun käyttäjä valitsee **Valmis** puhelintilauksen aikana, näkyviin tulle **Summat**-ruutu. Tämän ruudun summissa ei alkuun näy maksuperäisiä alennuksia, koska maksutapaa ei vielä ole valittu. Jos käyttäjä valitsee **Lisää maksu** -ruudussa maksutavan, jolle maksuvälineperusteinen alennus on määritetty, maksun summa korjataan automaattisesti ottamaan alennus huomioon. Puhelinkeskuksen asiakas voi samoin kuin myyntipisteellä päättää, haluaako hän suorittaa maksun kokonaan vai osittain. Myyntitilaukseen sovelletaan maksuvälineperusteista alennusta maksetun summan perusteella.

> [!NOTE]
> Puhelinkeskustilauksissa ei varmenneta kortteja. Jos puhelinkeskuksen käyttäjä esimerkiksi valitsee Visan luottokortiksi, mutta asiakas käyttää Mastercardia, järjestelmä soveltaa alennusta tästä huolimatta.

## <a name="exclude-items-from-discounts"></a>Nimekkeiden ohittaminen alennuksissa

Vähittäiskauppiaat jättävät usein joitakin tuotteita, kuten uusia nimikkeitä tai suosittuja nimikkeitä, pois alennusten piiristä. He voivat kuitenkin tästä huolimatta haluta myöntää maksuvälineperusteisia alennuksia. Vähittäiskauppias voi esimerkiksi määrittää Commercen siten, ettei se salli nimikeperusteisisä tai manuaalisia alennuksia. Jos asiakas kuitenkin maksaa alennukseen oikeuttavalla maksuvälineellä, Commerce soveltaa edelleen maksuvälineperusteista alennusta. Jos jälleenmyyjät haluavat määrittää Commercen tällä tavoin, heidän valittava ensin **Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**, sitten nimike ja määritettävä seuraavaksi **Commerce**-pikavälilehdessä **Estä kaikki alennukset**- ja **Estä maksuvälineperusteiset alennukset** -asetusten arvoksi **Ei** ja **Estä alennukset**- ja **Estä manuaaliset alennukset** -asetusten arvoksi **Kyllä**.

> [!NOTE]
> Kun **Estä kaikki alennukset** -määritykseksi on valittu **Kyllä**, tuotteeseen ei sovelleta alennuksia. Ei edes maksuvälineperusteisia alennuksia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]