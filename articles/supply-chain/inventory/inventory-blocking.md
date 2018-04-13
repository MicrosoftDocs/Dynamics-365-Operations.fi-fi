---
title: Varastoesto
description: "Tässä artikkelissa on yleiskatsaus varastoestosta, joka on osa Microsoft Dynamics 365 for Finance and Operationsin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 0567cdad6f9f27097f534381655e5b468884bed8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="inventory-blocking"></a>Varastoesto

[!INCLUDE [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskatsaus varastoestosta, joka on osa Microsoft Dynamics 365 for Finance and Operationsin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen.

Voit estää varastonimikkeitä seuraavilla tavoilla:
-   Manuaalisesti
-   Laatutilauksen luomalla
-   Käyttämällä prosessia, joka muodostaa laatutilauksen
-   Käyttämällä varaston tilan estoa

## <a name="blocking-items-manually"></a>Nimikkeiden manuaalinen esto
Voit estää nimikkeen määrä luomalla tapahtuman **Varastoesto**-sivulla. Vain käytettävissä olevassa varastossa olevat nimikkeet voidaan asettaa toimituskieltoon manuaalisesti. Manuaalisesti estetyille määrille sinun tulee harkita, pitäisikö odotettujen kuittien sisältyä suunnittelutoimintoihin odotettuina ja saatavilla olevina määrinä. Oletetut vastaanotot ovat estettyjä nimikkeitä, joiden oletetaan olevan käytettävissä tarkastuksen jälkeen käytettävissä olevana varastona. Arvioidun päivämäärän voi säilyttää. Oletusarvon mukaan **Oletetut vastaanotot** -asetus on valittuna nimikkeille, jotka on estetty laatutilauksen kautta. Voit peruuttaa määrän manuaalisen eston poistamalla tapahtuman **Varastoestot**-sivulta.

## <a name="blocking-items-by-creating-a-quality-order"></a>Estä nimikkeet luomalla laatutilaus
Voit määrittää nimikkeet, jotka on tarkistettava luomalla laatutilauksen **Laatutilaukset**-sivulla. Kun laatutilaus luodaan, nimikkeelle määritetty määrä estetään. Laatutilaukseen liitetty otantasuunitelma hallitsee ainoastaan tarkastettavien nimikkeiden määrää, ei estettyä määrää. Riippumatta määrästä, joka lähetetään tarkastettavaksi, otantasuunnitelman määritysten mukaan nimikemäärä, joka on määritetty laatutilauksessa, on määrä, joka on estetty.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Estä nimikkeet käyttämällä laatutilauksen luovaa prosessia
Jos laatuprosessi määrittää, että nimike on tarkastettava, nimikemäärä estetään automaattisesti. Kun laatutilaus luodaan automaattisesti, laatutilaukseen liitetty nimikeotantasuunnitelma hallitsee sekä estettyjen nimikkeiden määrää että tarkistettavien nimikkeiden määrää. Jos **Täysi esto** -asetus on valittuna **Nimikeotanta**-sivulla, koko määrä esimerkiksi ostotilausrivistä estetään riippumatta nimikeotannan määrästä tarkastuksen aikana.
### <a name="example"></a>Esimerkki

Seuraavassa esimerkissä laatutilaus luodaan ostotilauksen pakkausluettelon kirjaamisen yhteydessä. **Laatuliitokset**-sivulla on määritetty, että ostotilauksen pakkausluettelon kirjaus on määritetty prosessiksi, joka aktivoi laatutilauksen.

|Asennus                                                                     |Käyttäjätoiminto                 |Tulos             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Laatuliitos määrittää, että ostotilauksen pakkausluettelon kirjauksen yhteydessä on luotava laatutilaus. Laatutilauksen nimikkeen ottoasetus määrittää, että 10 prosenttia ostotilausrivin määrästä on tarkistettava. Lisäksi, koska **Täysi esto**-asetus on valittuna nimikkeen ottoasetukset ilmaisevat, että ostotilausrivin koko määrä pitää estää tarkastuksen aikana riippumatta määrästä, joka lähetetään tarkastettavaksi. | Pakkausluettelo kirjataan. | Laatutilaus on luotu. Kymmenen prosenttia nimikkeen ostotilauksen määrästä lähetetään tarkistukseen. Ostotilausrivin täysi määrä on estetty. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Nimikkeiden esto käyttämällä varaston tilan estoa
Voit määrittää, mitkä varaston tilat saavat aikaan eston käyttämällä **Varastoesto**-parametria **Varaston tilat** -sivulla.  Varaston tiloja ei voi käyttää tuotanto-, myynti-, tai siirtotilauksien, lähtevien tapahtumien tai projekti-integrointien estotiloina. Ulosmeneville töille käytetään nimikkeitä, joilla on saatavilla oleva varaston tila. Jos on nimikkeitä, joiden tila on **Hajonnut**, ja pääsuunnittelu suoritetaan näillä nimikkeillä, niitä pidetään puuttuvina ja varasto täydennetään automaattisesti.



<a name="see-also"></a>Lisätietoja
--------

[Luo ja ylläpidä varastoesto](tasks/create-maintain-inventory-blocking.md)

[Laadunhallintaprosessit](quality-management-processes.md)

[Tavaroiden laadun tarkistaminen (tehtäväopas)](tasks/inspect-quality-goods.md)

