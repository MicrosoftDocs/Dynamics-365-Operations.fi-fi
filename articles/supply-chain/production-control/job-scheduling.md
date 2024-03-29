---
title: Töiden ajoitus
description: Tässä artikkelissa on tietoja töiden ajoituksessa, joka on tarkempi kuin työvaiheiden ajoitus. Töiden ajoitusta voi käyttää on valmistusympäristön hallintaan sekä yksittäisten töiden (tai työtilauksien) ajoittamiseen.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 698fb31b1a2790b737b30f15b50f0f8ecdd59286
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570246"
---
# <a name="job-scheduling"></a>Töiden ajoitus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja töiden ajoituksessa, joka on tarkempi kuin työvaiheiden ajoitus. Töiden ajoitusta voi käyttää on valmistusympäristön hallintaan sekä yksittäisten töiden (tai työtilauksien) ajoittamiseen.

Töiden ajoitusta voi käyttää on valmistusympäristön hallintaan sekä yksittäisten töiden (tai työtilauksien) ajoittamiseen. Se erittelee kunkin työvaiheen yksittäisiksi tehtäviksi tai töiksi. Nämä työt määritetään sitten ne suorittaville operatiivisille resursseille. Sen avulla on myös mahdollista synkronoida kaikki valitussa työssä viitatut työt. Voit määrittää työlle aloitus- ja päättymispäivän sekä -ajan ja suorittaa sitten ajoituksen. Määrittämäsi aika voi olla aloitus- vai päättymisaika, valitusta ajoitussuunnasta riippuen. Tämä toiminto on hyödyllinen esimerkiksi silloin, kun työ voidaan suorittaa ainoastaan yhdellä koneella kerrallaan, tai jos haluat optimoida ajettavan työn jokaiselle resurssille.

## <a name="tasks-in-the-job-scheduling-process"></a>Töiden ajoitusprosessin tehtävät
Töiden ajoitusprosessi sisältää seuraavat tehtävät:

-   Työvaiheiden jakaminen töiksi.
-   Ajoita työt liittyvälle työvaiheelle määritettyjen resurssien päivämäärien ja kellonaikojen mukaan.
-   Laske kunkin työn aloitus- ja päättymisaika. Voit varmistaa, että ajoitukset eivät ole päällekkäisiä käyttämällä rajallista kapasiteettia.
-   Määritä, mille resurssiryhmän resursseille työ ajetaan. Tämä tehtävä edellyttää, että työvaiheelle on määritetty resurssiryhmä. Töiden ajoitus valitsee resurssit tai resurssiryhmät lyhimmän läpimenoajan perusteella ja ottaa lisäksi huomioon myös resurssien edeltävät varaukset.
-   Hajota työvaiheet töiksi, kun suoritat töiden ajoituksen. Työt ajoitetaan päivien ja kellonajan perusteella tuotantoreititykseen määritetyn järjestyksen mukaisesti. Työvaiheen asetuksissa määritetään työt, jotka jaetaan ajoitusprosessin aikana. Työvaiheelle liitetty reititysryhmä ohjaa töiden luontia. Työn luonti edellyttää, että työlle on määritetty kesto. Esimerkiksi kuljetusaikatyö luodaan, jos valitulle työvaiheelle on määritetty kuljetusaika.

## <a name="scheduling-direction"></a>Ajoituksen suunta
Voit ajoittaa töitä joko eteen- tai taaksepäin.

-   **Eteenpäin** – Käytä eteenpäin ajoituksen menetelmää aloittaaksesi tuotannon mahdollisimman aikaisin. Tämä tunnetaan myös työntömenetelmänä, sillä siinä tuotantoa työnnetään eteenpäin tuotantoprosessin läpi. Tuotanto ajoitetaan alkamaan ja päättymään aikaisimpina mahdollisina päivämäärinä.
-   **Taaksepäin** – Käytä taaksepäin ajoituksen menetelmää aloittaaksesi tuotannon mahdollisimman myöhään. Tämä tunnetaan myös vetomenetelmänä, sillä se perustuu päivämäärään, jona tuotannon on oltava valmis. Taaksepäin ajoituksen menetelmä laskee aikaa määräpäivästä taaksepäin myöhäisimpään mahdolliseen päivämäärään, jolloin tuotannon voi aloittaa niin, että se saadaan valmiiksi määräaikaan mennessä.

## <a name="finite-capacity"></a>Rajallinen kapasiteetti
Voit ajoittaa töitä käyttämällä rajallista kapasiteettia. Rajallista kapasiteettia käytettäessä ajoitettu kapasiteetti ei voi olla suurempi kuin resurssin käytettävissä oleva kapasiteetti. Käytettävissä oleva aika määritetään aikavälinä, jolloin resurssi on käytettävissä eikä kapasiteetille ole muuta varauksia. Rajoitettuun kapasiteettiin perustuva ajoittaminen varmistaa, että työvaiheen aloitus- ja päättymisajoissa ei ole päällekkäisyyksiä tiettynä päivänä. Resurssille jo varattu kapasiteetti sekä aloitus- ja päättymisaikojen päällekkäisyydet otetaan huomioon. Rajoitettu kapasiteetti määrittää kapasiteetin määrän, jonka on oltava saatavilla resurssille sen optimaalisen käytön varmistamiseksi. Tämä määritys täsmäytetään laskelmaan lyhyimmästä mahdollisesta läpimenoajasta työvaiheiden välillä.

## <a name="finite-materials"></a>Rajallinen materiaali
Rajallisiin materiaaleihin perustuva töiden ajoittaminen varmistaa, että vaadittavat materiaalit ovat käytettävissä työvaiheen alkaessa. Nimikkeiden kattavuussäännöt määrittävät nämä rajat. Ajoituksessa käytetään tarpeiden hajotusta määrittämään, milloin komponenttinimikkeet ovat käytettävissä. Jos et suorita ajoitusta rajoitetulla materiaalilla, järjestelmä olettaa kaikkien nimikkeiden olevan käytettävissä silloin, kun niitä tarvitaan.

## <a name="finite-properties"></a>Rajallinen ominaisuus
Erityisiin ominaisuuksiin perustuva töiden ajoitus edellyttää, että tuotantoreitityksen työvaiheille määritetään ominaisuudet. Ominaisuudet on määritettävä kapasiteetin varaamiseksi.

## <a name="references"></a>Viitteet
Töiden ajoitus ajoittaa kaikki nykyiseen tuotantoon liittyvät viitetuotannot. Jos tuotannolla on alituotantoja, ne on ajoitettava yhdessä päätuotannon kanssa, sillä päätuotantoa ei voi käynnistää, ennen kuin siihen liittyvät alituotannot ovat valmiit.

## <a name="schedule-resources"></a>Resurssien suunnittelu
Ajoitusmoduuli tarkastelee resurssien yhdistelmiä tunnistaakseen yhdistelmät, jotka voivat täyttää vaatimukset. Voit määrittää valintaehdot valitsemalla jonkin seuraavista arvoista **Ajoitusparametrit**-sivun **Ensisijaisen resurssin valinta** -kentässä:

-   **Kesto** – Ajoitusmoduuli valitsee resurssin, jolla on lyhin läpimenoaika. **Huomautus:** Keston mukaan ajoittaminen voi heikentää suorituskykyä, jos sama resurssiryhmä sisältää useita resursseja ja toissijaiset työvaiheet ovat käytössä. Voit ajoittaa enintään 32 resurssia työvaiheelle. Jos tämä määrä ylitetään, järjestelmä näyttää infolokisanoman eikä töiden ajoitustoiminto löydä parasta vaihtoehtoista resurssia.
-   **Prioriteetti** – Ajoitusmoduuli valitsee resurssin, jolla on suurin prioriteetti, jos kahden tai useamman resurssin ominaisuudet ja tasot ovat identtiset. Resurssilla, jolla on pienin numeerinen arvo tässä kentässä on korkein prioriteetti.

Kun töiden ajoitus suoritetaan, järjestelmä suunnittelee resurssit resurssin parametreissä määriteltyjen rajoituksen mukaisesti. Resurssien kapasiteettia hallitaan kalenteriasetuksissa. Järjestelmä laskee resurssien kapasiteettikuormituksen ajoitusprosessin aikana. **Huomautus:** Kun tuotanto käyttää työvaiheiden ajoitustoimintoa, voit käyttää työn ajoitusta työvaiheiden ajoituksen jälkeen. Jos et käytä työvaiheiden ajoitusta, voit suorittaa pelkästään työn ajoituksen.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Resurssien työtilauskohtainen enimmäiskapasiteetti
Resurssit kohdistetaan töihin ajoitusprosessin välityksellä. Voit määrittää resurssien työtilauskohtaisen enimmäiskapasiteetin. Voit esimerkiksi määrittää järjestelmän ajoittamaan korkeintaan puolet kokonaiskapasiteetista yhdelle tuotantotilaukselle. Näin voit hallita resurssien ajoitusta tarkemmin työn ajoitustasolla. Se voi siis estää ongelmia, jotka johtuvat siitä, että kapasiteettia ei riitä samanaikaisten tuotantojen suorittamiseen.

## <a name="resource-efficiency"></a>Resurssin tehokkuus
Töiden ajoitus ottaa resursseille määritetyt tehokkuusprosentit huomioon. Tehokkuusprosentit vähentävät tai lisäävät resurssille varattua aikaa. Sen seurauksena siis myös läpimenoaika lisääntyy tai vähenee. Laskutoimituksessa käytetään seuraavaa kaavaa: Ajoitusaika = Aika x 100 ÷ Tehokkuusprosentti Tässä kaavassa *Aika* sisältää sekä asetus- että ajoajan.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]