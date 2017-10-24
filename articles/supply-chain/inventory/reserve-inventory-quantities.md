---
title: "Varastomäärien varaaminen"
description: "Tässä aiheessa kuvataan varastomäärien varaamisen eri vaihtoehtoja."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 67c7582665255e65995be688ef133e71938e7c28
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="reserve-inventory-quantities"></a>Varastomäärien varaaminen

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan varastomäärien varaamisen eri vaihtoehtoja.

Myyntitilaukselle voidaan varata automaattisesti varastomääriä. Tämä tarkoittaa, että varattua varastoa ei voida käyttää varastosta muita tilauksia varten, jollei varausta tai osaa siitä peruta.

Varastomäärien varaamiseen on useita syitä:
-   Ensimmäisenä tilattu, ensimmäisenä toimitettu eli saatavissa olevat nimikkeet toimitetaan asiakkaille siinä järjestyksessä, jossa asiakkaat ovat tehneet tilauksensa.
-   Puute nimikkeistä toimittajan pitkän tai tuntemattoman toimitusajan takia. Halutaan varmistaa, että saataviin tulevat nimikkeet käytetään ensin tiettyjen asiakkaiden tai tietyntyyppisten tilausten toimituksiin.
-   Tietyt asiakkaat ja tietyntyyppiset tilaukset ovat toimituksissa etusijalla.
-   Nimikkeet, joilla on sarja- tai eränumero. On mahdollista merkitä tiettyjen tilausten toimitukseen käytetyt tai käytettävät nimikkeet.
-   Erikoistilatut nimikkeet, jotka on varattu määrättyjä tilauksia varten.
-   Tuotantotilaukset. On mahdollista merkitä esimerkiksi tiettyjä tilauksia varten tuotetut ja mukautetut nimikkeet.

Varasto voidaan varata automaattisesti, kun luodaan uusi tilausrivi, tai se voidaan varata manuaalisesti yksittäisten tilausten yhteydessä. On myös mahdollista tehdä varastovaraus tuotantoprosessin eri vaiheissa. Vain varastoidut tuotteet voidaan varata. Palveluita ei voi varata, sillä niillä ei ole varastoa. Sekä fyysinen käytettävissä oleva varasto että tilattu mutta ei vielä vastaanotettu varasto voidaan varata. Jos varataan suurempi määrä kuin mitä käytettävissä oleva varasto sisältää, näyttöön tulee viesti, jossa todetaan, ettei näin suurta määrää voida varata. Voit sitten joko varata määrän tai muuttaa tilattua määrää. Määrää voidaan joko varata tai muuttaa. Jos varataan enemmän nimikkeitä kuin on saatavissa, puute katetaan seuraavalla kerralla, kun nimikkeitä on saatavissa toimituksiin.

## <a name="inventory-reservation-policies"></a>Varastovarauskäytännöt
Varastovarauskäytännöt on määritetty **Nimikemalliryhmät**-sivulla **Varasto ja varastonhallinnan parametrit**-sivulla ja **Tuotantoparametrit**-sivulla.
### <a name="policies-on-the-item-model-groups-page"></a>Nimikemalliryhmän sivun käytännöt

**Varastokäytännöt**-osa sisältää seuraavat varauskäytännöt.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Varauskäytäntö**  | **Kuvaus**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Päivämäärän mukaan ohjattu FIFO    | Jos valitset **Päivämäärän mukaan ohjattu FIFO** -vaihtoehdon, varastovaraukset tehdään lajittelupäivän mukaan FIFO (first in, first out) -periaatteella. Erät voidaan varata myös FIFO-periaatteella aikaisimman vastaanottopäivän perusteella.                                                                                                                                                                                                                                                                       |
| Lähetyspäivästä taaksepäin | Tämä vaihtoehto on käytettävissä vain, jos olet valinnut **Päivämäärän mukaan ohjattu FIFO** -vaihtoehdon. Jos valitset **Lähetyspäivästä taaksepäin**, varastovaraus tehdään LIFO (last in, first out) -periaatteella halutusta toimituspäivästä taaksepäin laskien. Jos lähetyspäivää ennen ei ole vastaanottoja, käytetään FIFO-varausta.                                                                                                                                                                                                           |
| Nimikemyynnin varaus  | Määrittää, tehdäänkö nimikkeiden varaus manuaalisesti tai automaattisesti. Jos varaaminen tapahtuu automaattisesti, varastovaraus tehdään kun tilausrivit luodaan. Voit tehdä tuoterakennevarauksia nimiketunnustasolla (**Automaattinen**-vaihtoehto), tai kutakin tuoterakenteen osaa varten erikseen (**Hajotus**-vaihtoehto). **Nimikemyynnin varauksen** oletusarvo voi periytyä **Myyntireskontran parametrit** -kohdasta. Kyseisellä sivulla arvo määritetään Varaus-kenttään **Myynnin oletusarvot** **-osan** **Yleistä**-välilehdessä. |
| Saman erän valinta    | Saman erän varaamisen avulla voit varata myyntitilausriville varaston yhden varastoerän mukaan. Jos haluat käyttää tätä vaihtoehtoa, määritä myös **Konsolidoi tarve** -asetukseksi **Kyllä**. Seurantadimensioryhmää ja varastodimensioryhmää varten tarvitaan lisäasetuksia. Lisätietoja on kohdassa [Saman erän varaaminen myyntitilausta varten](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsolidoi tarve | Tämä vaihtoehto on samanlainen kuin **Saman erän valinta** -asetus ja se konsolidoi myyntitilausrivejä varten varatun varaston yhdeksi tarpeeksi.                                                                                                                                                                                                                                                                                                                                                                                      |
| Päivämäärän mukaan ohjattu FEFO    | Tämän vaihtoehdon avulla voit varata erät, joiden parasta ennen -päivä ja erääntymispäivämäärä ovat lähellä. Sinun on myös määritettävä **Keräilyehto** kenttä valitaksesi joko **erääntymispäivän** tai **parasta ennen -päivän**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Esimerkki päivämäärän mukaan ohjatusta FIFO-varauksesta ja lähetyspäivästä taaksepäin -varauksesta

Tässä esimerkissä nimiketunnuksen A käytettävissä olevalla varastolla on kolme eri eränumeroa.
| Nimiketunnus | Eränumero | Määrä | Päivämäärä             |
|-------------|--------------|----------|------------------|
| A           | 1 000         | 5        | 2.2.2016 |
| A           | 1001         | 3        | 1.1.2006  |
| A           | 1002         | 7        | 3. maaliskuuta 2016    |

Automaattisesti varattava myyntitilaus, jonka toimituspäivä on 4.4.2002, varaa erän seuraavasti:
-   Jos **Päivämäärän mukaan ohjattu FIFO** ja **Lähetyspäivästä taaksepäin** -valintaruutujen valinta on poistettu, erä 1000 on varattu, koska sillä on pienin eränumero.
-   Jos **Päivämäärän mukaan ohjattu FIFO** -valintaruutu on valittuna ja **Lähetyspäivästä taaksepäin** -valintaruutu ei ole valittuna, varataan erä 1001, koska sen vastaanottopäivä on varhaisin (FIFO).
-   Jos **Päivämäärän mukaan ohjattu FIFO** ja **Lähetyspäivästä taaksepäin** -valintaruudut on valittu, erä 1002 on varattu, koska sen vastaanottopäivä on lähinnä myyntitilauksen toimituspäivää.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Varastonhallintaparametrit-sivun käytännöt

Varauksiin liittyy kaksi vaihtoehtoa **Varasto ja varastonhallinnan parametrit** -sivulla:
-   Valitse **Varaa tilatut nimikkeet** -vaihtoehto **Yleistä**-välilehdessä, jos haluat varata nimikkeiden vastaanotot, jotka on tilattu nimikkeiden varasto-ottoja kohden Myyntireskontra-, Projektinhallinta ja kirjanpito- sekä Tuotannonhallinta-kohdissa. Jos poistat tämän vaihtoehdon valinnan, voit varata vain fyysisesti vastaanotettuja nimikkeitä. Jos jonkin nimikkeen asetuksissa hyväksytään negatiivinen varasto, tällä kentällä ei ole merkitystä.
-   **Varaa nimikkeet automaattisesti** -vaihtoehto **Kuljetus** -välilehdessä määrittää oletusasetukseksi, että nimikkeet varataan automaattisesti siirtotilauksia varten. Oletusasetuksen voi ohittaa yksittäisissä tilauksissa.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Varastovarauskäytännöt Tuotantoparametrit -sivulla

**Varaus**-kentän arvo **Yleistä**-välilehdessä **Tuotantoparametrit** sivulla määrittää tuotantoprosessin oletuskohdan, jossa varasto pitää varata. Esimerkiksi varasto voidaan varata, kun työ on ajoitettu tai kun työ alkaa.

