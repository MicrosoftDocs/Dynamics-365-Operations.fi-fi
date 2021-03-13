---
title: Varastoesto
description: Tässä aiheessa on yleiskatsaus varastoestosta, joka on osa Supply Chain Managementin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen.
author: perlynne
manager: tfehr
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 646ddc231b1ee25b13fdeb779b2bbeae6dd8c2a9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011594"
---
# <a name="inventory-blocking"></a>Varastoesto

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleiskatsaus varastoestosta, joka on osa Supply Chain Managementin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen.

Voit estää varastonimikkeitä seuraavilla tavoilla:
-   Manuaalisesti
-   Laatutilauksen luomalla
-   Käyttämällä prosessia, joka muodostaa laatutilauksen
-   Käyttämällä varaston tilan estoa

## <a name="blocking-items-manually"></a>Nimikkeiden manuaalinen esto
Voit estää nimikkeen määrä luomalla tapahtuman **Varastoesto**-sivulla. Vain käytettävissä olevassa varastossa olevat nimikkeet voidaan asettaa toimituskieltoon manuaalisesti. Manuaalisesti estetyille määrille sinun tulee harkita, pitäisikö odotettujen kuittien sisältyä suunnittelutoimintoihin odotettuina ja saatavilla olevina määrinä. Oletetut vastaanotot ovat estettyjä nimikkeitä, joiden oletetaan olevan käytettävissä tarkastuksen jälkeen käytettävissä olevana varastona. Arvioidun päivämäärän voi säilyttää. Oletusarvon mukaan **Oletetut vastaanotot** -asetus on valittuna nimikkeille, jotka on estetty laatutilauksen kautta. Voit peruuttaa määrän manuaalisen eston poistamalla tapahtuman **Varastoestot**-sivulta.

## <a name="blocking-items-by-creating-a-quality-order"></a>Estä nimikkeet luomalla laatutilaus
Voit määrittää nimikkeet, jotka on tarkistettava luomalla laatutilauksen **Laatutilaukset**-sivulla. Kun laatutilaus luodaan, nimikkeelle määritetty määrä estetään. Laatutilaukseen liitetty otantasuunitelma hallitsee ainoastaan tarkastettavien nimikkeiden määrää, ei estettyä määrää. Riippumatta määrästä, joka lähetetään tarkastettavaksi, otantasuunnitelman määritysten mukaan nimikemäärä, joka on määritetty laatutilauksessa, on määrä, joka on estetty.

> [!NOTE]
> Pääsuunnittelu ei tue sekä erän vanhentumispäivämäärää että varaston tila -ominaisuuksien estämistä. Tämä voi johtaa siihen, että käytettävissä oleva varasto suljetaan pois käytöstä, mikä voi tapahtua pääsuunnittelun aikana. On suositeltavaa käyttää eräkäsittelykoodeja varaston tilan asemesta vanhentuneiden erien estämiseen.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Estä nimikkeet käyttämällä laatutilauksen luovaa prosessia
Jos laatuprosessi määrittää, että nimike on tarkastettava, nimikemäärä estetään automaattisesti. Kun laatutilaus luodaan automaattisesti, laatutilaukseen liitetty nimikeotantasuunnitelma hallitsee sekä estettyjen nimikkeiden määrää että tarkistettavien nimikkeiden määrää. Jos **Täysi esto** -asetus on valittuna **Nimikeotanta**-sivulla, koko määrä esimerkiksi ostotilausrivistä estetään riippumatta nimikeotannan määrästä tarkastuksen aikana.
### <a name="example"></a>Esimerkki

Seuraavassa esimerkissä laatutilaus luodaan ostotilauksen pakkausluettelon kirjaamisen yhteydessä. **Laatuliitokset**-sivulla on määritetty, että ostotilauksen pakkausluettelon kirjaus on määritetty prosessiksi, joka aktivoi laatutilauksen.

|Asennus                                                                     |Käyttäjätoiminto                 |Tulos             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Laatuliitos määrittää, että ostotilauksen pakkausluettelon kirjauksen yhteydessä on luotava laatutilaus. Laatutilauksen nimikkeen ottoasetus määrittää, että 10 prosenttia ostotilausrivin määrästä on tarkistettava. Lisäksi, koska **Täysi esto**-asetus on valittuna nimikkeen ottoasetukset ilmaisevat, että ostotilausrivin koko määrä pitää estää tarkastuksen aikana riippumatta määrästä, joka lähetetään tarkastettavaksi. | Pakkausluettelo kirjataan. | Laatutilaus on luotu. Kymmenen prosenttia nimikkeen ostotilauksen määrästä lähetetään tarkistukseen. Ostotilausrivin täysi määrä on estetty. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Nimikkeiden esto käyttämällä varaston tilan estoa
Voit määrittää, mitkä varaston tilat saavat aikaan eston käyttämällä **Varastoesto**-parametria **Varaston tilat** -sivulla.  Varaston tiloja ei voi käyttää tuotanto-, myynti-, tai siirtotilauksien, lähtevien tapahtumien tai projekti-integrointien estotiloina. Ulosmeneville töille käytetään nimikkeitä, joilla on saatavilla oleva varaston tila. Jos on nimikkeitä, joiden tila on **Hajonnut**, ja pääsuunnittelu suoritetaan näillä nimikkeillä, niitä pidetään puuttuvina ja varasto täydennetään automaattisesti.



<a name="additional-resources"></a>Lisäresurssit
--------

[Luo ja ylläpidä varastoesto](tasks/create-maintain-inventory-blocking.md)

[Laadunhallintaprosessit](quality-management-processes.md)

[Tarkista tavaroiden laatu](tasks/inspect-quality-goods.md)
