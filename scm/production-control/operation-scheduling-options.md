---
title: "Työvaiheen ajoitusvaihtoehdot"
description: "Tässä aiheessa kuvataan työvaiheiden ajoittamisen asetuksia. Työvaiheiden ajoitusta voidaan käyttää, kun tuotantoprosessin kestosta halutaan yleisarvio."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ede111a8c7e8fe17b95747aadef30d1af1fea6aa
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="operations-scheduling-options"></a>Työvaiheen ajoitusvaihtoehdot

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan työvaiheiden ajoittamisen asetuksia. Työvaiheiden ajoitusta voidaan käyttää, kun tuotantoprosessin kestosta halutaan yleisarvio.

Työvaiheiden ajoitus laskee tuotantotilauksen seuraavat tiedot:

-   Tuotantotilauksen ja kunkin työvaiheen määritetään alkamis- ja päättymispäivät.
-   Resurssit määritetään toimintoihin.

Useat asetukset määrittävät tuotantoaikataulujen laskemistavan. Nämä asetukset määritetään **Työvaiheiden ajoitus** -sivulla. Seuraavassa kuvataan eri ajoitusvaihtoehdot.

## <a name="operations-scheduling"></a>Työvaiheiden ajoitus
### <a name="scheduling-direction"></a>Ajoituksen suunta

Ajoitussuunta on perustava osa ajoitusprosessia. Tuotanto voidaan ajoittaa eteenpäin tai taaksepäin mistä tahansa päivämäärästä alkaen ajoitus- ja suunnitteluvaatimusten mukaisesti.

-   **Eteenpäinajoitus**: voit ajoittaa tuotannon alkamaan mahdollisimman aikaisin. Tuotanto voidaan aloittaa tänään, huomenna tai minä tahansa tulevana päivänä. Tuotanto ajoitetaan alkamaan aikaisimpana mahdollisena päivänä ja sitä suunnitellaan siitä eteenpäin aikaisimpaan mahdolliseen päättymispäivään saakka.
-   **Taaksepäinajoitus**: voit ajoittaa tuotannon alkamaan mahdollisimman myöhään. Aikataulu perustuu päivämäärään, jolloin tuotannon on oltava valmis, ja aikaa lasketaan määräpäivästä taaksepäin myöhäisimpään mahdolliseen päivämäärään, jolloin tuotannon voi aloittaa niin, että se saadaan valmiiksi määräaikaan mennessä.

Valittavissa ovat seuraavat vaihtoehdot:

-   **Tästä päivästä eteenpäin**: ajoitus kuluvasta päivästä eteenpäin. (Kuluvana päivänä käytetään järjestelmän päivämäärää.)
-   **Eteenpäin ajoitetusta alusta lähtien**: ajoitus aiemmasta aloituspäivästä eteenpäin. Jos aiempaa ajoitusta ei ole, ajoituksen suunta on kuluvasta päivästä eteenpäin.
-   **Ajoituspäivästä eteenpäin**: **Ajoituspäivä**-kentässä määritetystä ajoituspäivästä alkaen. Jos ajoituspäivää ei määritetä, ajoituksen suunta on kuluvasta päivästä eteenpäin.
-   **Lähetyspäivästä taaksepäin**: ajoitus taaksepäin tuotantotilauksessa määritetystä päivästä lukien. Jos valitset tämän ajoitusvaihtoehdon eikä toimituspäivää ole määritetty, toimituspäivänä käytetään kuluvaa päivää.
-   **Taaksepäin, alkaen ajoitetusta lopusta**: ajoitus aiemmin lasketusta päättymispäivästä taaksepäin. Jos aiempaa ajoitusta ei ole, päättymispäivänä käytetään kuluvaa päivää.
-   **Ajoituspäivästä taaksepäin**: **Ajoituspäivä**-kentässä määritetystä ajoituspäivästä taaksepäin. Jos ajoituspäivää ei määritetä, käytetään kuluvaa päivää. Ajoitus toimenpiteen ajoituspäivästä taaksepäin lasketaan tuotantotilausta varten silloin, kun tarve lasketaan viimeisen kerran. Jos tuotantotilaukselle ei ole määritetty toimenpiteen päivämäärää, käytetään kuluvaa järjestelmän päivämäärää.
-   **Lasketusta viivästyspäivästä taaksepäin**: ajoitus taaksepäin viivästyspäivästä, joka on laskettu, kun tuotantotilauksen tarve on laskettu viimeisen kerran. Jos tuotantotilaukselle ei ole määritetty laskettua viivästyspäivää, käytetään kuluvaa järjestelmän päivämäärää.
-   **Kuten viime ajoituksessa**: kun työvaiheet ja työt ajoitetaan, järjestelmä tallentaa valitun ajoitussuunnan ja -päivämäärän. Tämän vuoksi voit valita tämän vaihtoehdon seuraavaa ajoitusta varten. Jos tuotantotilausta ei ole aiemmin ajoitettu, ajoitus tehdään kuluvasta järjestelmän päivämäärästä taaksepäin.
-   **Huomisesta eteenpäin**: ajoitus kuluvaa päivää seuraavasta päivästä eteenpäin.
-   **Edellisestä työstä eteenpäin**: tämä vaihtoehto sopii vain töiden ajoitukseen. Jos tämä vaihtoehto valitaan työvaiheiden ajoitukselle, tuotantotilaus ajoitetaan kuluvasta päivästä eteenpäin. Töiden ajoituksessa tehdään ensin yhden työn ajoitus, ja kaikki muut tuotannon työt ajoitetaan kyseisen työn perusteella.
-   **Edellisestä työstä taaksepäin**: tämä vaihtoehto sopii vain töiden ajoitukseen. Jos tämä vaihtoehto valitaan työvaiheiden ajoitukselle, suunnitellut tilaukset ajoitetaan kuluvasta päivästä taaksepäin. Töiden ajoituksessa tehdään ensin yhden työn ajoitus, ja kaikki muut tuotannon työt ajoitetaan kyseisen työn perusteella.

### <a name="scheduling-date"></a>Ajoituspäivämäärä

Tätä päivämäärää käytetään ajoitussuunnille **Ajoituspäivästä eteenpäin** tai **Ajoituspäivästä taaksepäin**. Ajoitus on kyseisestä päivästä eteen- tai taaksepäin. Lisätietoja on edellisessä kohdassa "Ajoituksen suunta".

### <a name="recalculate-bom-levels"></a>Laske tuoterakenteen tasot uudelleen

Kun valitset **Laske tuoterakenteen tasot uudelleen**, valitun tuoterakenteen (BOM) tasot lasketaan uudelleen oikean ajoitusjärjestyksen varmistamiseksi.

## <a name="limitations"></a>Rajoitukset
### <a name="finite-capacity"></a>Rajallinen kapasiteetti

Ajoitus riippuu tuotannon valmistumiseen tarvittavien resurssien saatavuudesta. Jos kapasiteettia ei ole tarpeeksi, tuotantotilaukset voivat viivästyä tai keskeytyä. Jos rajallista kapasiteettia käytetään työvaiheiden ajoituksessa, aiemmat kapasiteetin varaukset, jotka on tehty resursseille, otetaan huomioon, ja kapasiteetin ei katsota olevan käytettävissä. Tuotantotilaus ajoitetaan tuotannon valmistumiseen tarvittavien resurssien saatavuuden perusteella. Työvaiheiden ajoituksessa käytetään määritettyä työvaiheiden järjestystä, jonka perusteella voidaan määrittää tuotantoreitin työvaiheiden järjestys. Työvaiheiden ajoitus varaa kapasiteettia resurssiryhmistä tuotannon reititykselle määritettyjen työvaiheaikojen perusteella. Resurssiryhmän kapasiteetti on kaikkien resurssiryhmien käytettävissä olevien resurssien summa.

### <a name="finite-material"></a>Rajallinen materiaali

Ajoitukseen vaikuttaa myös tuotantoon tarvittavien materiaalien saatavuus. Riittämätön komponentin saatavuus voi myös aiheuttaa tuotannon viiveitä. Ajoitus voi perustua myös materiaalien käyttöön. Määritä ainoastaan tuotannolle välttämättömät materiaalit sellaisten materiaalien sijaan, jotka eivät ole kriittisiä. Tämäntyyppinen ajoitusta kutsutaan rajalliseen materiaaliin perustuvaksi ajoitukseksi. Kun määrität rajallisen materiaalin, tuotanto ajoitetaan sen perusteella, ovatko materiaalit käytettävissä. **Huomautus:** Kun optimointi perustuu sekä kapasiteettiin että materiaaleihin, tuotanto lasketaan molempien rajoitteiden mukaiseksi. Kapasiteetin ja materiaalin saatavuus otetaan huomioon, ja tuotantotilauksen toimintoja ei voi ajoittaa alkamaan ennen kuin kapasiteetti ja materiaalit ovat käytettävissä samaan aikaan ja vaaditun määrän mukaisesti. Valitse tämä valintaruutu, jos haluat määrittää, että materiaalien rajallisuus on huomioitava ajoituksessa. Jos materiaalit ovat rajallisia, materiaalin kattavuus kyseisenä ajankohtana otetaan huomioon. Toisin sanoen ajoituksessa otetaan huomioon nimikkeille laskettavat viivästyspäivät. Ajoitustoiminto varaa raaka-aineet ja hajottaa valitun tuotannon. Jos ajoitus tehdään useita kertoja, hajotus ja varaukset tehdään ainoastaan ensimmäisellä ajoituskerralla. Jos tuotannon tuoterakennetta tai reititystä muutetaan, hajotus suoritetaan seuraavan ajoituksen yhteydessä. Hajotuksessa oletetaan, että materiaaleja tarvitaan samana päivänä. Koska tuotantoa ei ajoiteta pääajoituksen hajotusajankohtana, nimikkeiden saatavuuden paras arvio on kuluva päivä. Hajotus tarkistaa, ovatko nimikkeet käytettävissä. Jos nimikkeet ovat käytettävissä, tuotannon vaatimukset voidaan täyttää. Jos nimikkeet eivät ole käytettävissä nykyiseen päivämäärään mennessä, järjestelmä luo suunnitellun tilauksen ja suunnitellulle tilaukselle tehdään vastavalinta. Jos suunnitellussa tilauksessa käytetään automaattista vahvistusta, suunniteltu tilaus vahvistetaan automaattisesti ostoa tai tuotantoa varten. Tuotannon tila muuttuu automaattisesti **Kattavuusryhmät**-valintaikkunan **Haluttu tuotannon tila** -kentässä määritetyksi tilaksi. Jos valintaruudun valinta poistetaan, järjestelmä olettaa, että materiaaleja on aina saatavana. Tällöin ajoituksessa ei oteta huomioon sitä, ovatko materiaalit käytettävissä tarveajankohtana.

### <a name="finite-property"></a>Rajallinen ominaisuus

Valitse tämä valintaruutu, jos töiden ajoituksessa pitää ottaa huomioon ominaisuusvaatimukset.

### <a name="keep-production-unit"></a>Säilytä tuotantoyksikkö

Valitse, pitääkö ajoitusmoduulin ajoittaa vain resursseja, jotka on jo määritetty tuotantoyksikölle.

### <a name="keep-warehouse-from-resource"></a>Säilytä resurssin varasto

Valitse, pitääkö ajoitusmoduulin ajoittaa vain resursseja, jotka on liitetty resurssille määritettyyn syöttövarastoon.

## <a name="references"></a>Viitteet
### <a name="schedule-references"></a>Aikatauluta viitteet

Kun viitteet määräytyvät tuotantotilauksen perusteella, niistä käytetään myös alituotanto-nimitystä. Alituotannot voidaan ajoittaa tuotantotilauksen ajoituksen osana. Valitse tämä valintaruutu, jos alituotantojen ajoitus perustuu päätuotannon ajoitukseen. Päätuotantoon perustuvat tuotannot ajoitetaan eteenpäin ja tuotannon pohjana olevat tuotannot taaksepäin. Tuotantotilausviitteitä voidaan tarkastella **Tuotantotilaus**-sivun **Viitetaso**-kentässä.

### <a name="synchronize-references"></a>Synkronoi viitteet

Voit myös halutessasi synkronoida viitteet tuotantotilauksen kanssa. Jos valitset tämän vaihtoehdon, alituotantojen päivämäärät siirtyvät ja ne kohdistetaan, kun tuotantotilauksen ajoitusta muutetaan. Jos tuotantotilaus sisältää vähintään yhden osatuotannon, haluat ehkä ajoittaa osatuotannon yhdessä päätuotannon kanssa. Tässä tapauksessa päätuotantoa ei voi käynnistää, ennen kuin siihen liittyvät osatuotannot ovat valmiita. Tästä syystä valitse tämä valintaruutu, jos osatuotantojen ajoitus perustuu valitun tuotannon aloitus- ja päättymisaikoihin. Voit valita tämän valintaruudun vain, jos **Aikatauluta viitteet** -valintaruutua on myös valittu.

## <a name="cancellation"></a>Peruutus
### <a name="cancel-queue-time"></a>Peruuta jonotusaika

Valitse tämä valintaruutu, jos haluat poistaa jonotusajan ajoituksesta.

### <a name="cancel-setup"></a>Peruuta asetus

Valitse tämä valintaruutu, jos haluat poistaa asetusajan ajoituksesta.

### <a name="cancel-process"></a>Peruuta prosessi

Valitse tämä valintaruutu, jos haluat poistaa ajoajan ajoituksesta.

### <a name="cancel-overlap"></a>Peruuta limitys

Valitse tämä valintaruutu, jos haluat poistaa päällekkäisajan ajoituksesta.

### <a name="cancel-transport"></a>Peruuta kuljetus

Valitse tämä valintaruutu, jos haluat poistaa siirtoajan ajoituksesta.

## <a name="set-default"></a>Määritä oletus
Voit tallentaa nykyiset arvot oletusarvoiksi. Käytettävissä ovat seuraavat kaksi vaihtoehtoa:

-   Aseta omaksi oletukseksi
-   Aseta oletukseksi kaikille


<a name="see-also"></a>Lisätietoja
--------

[Työvaiheiden ajoitus](operations-scheduling.md)




