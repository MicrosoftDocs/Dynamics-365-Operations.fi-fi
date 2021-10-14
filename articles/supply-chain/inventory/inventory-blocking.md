---
title: Varastoesto
description: Tässä aiheessa on yleiskatsaus varastoestosta, joka on osa Supply Chain Managementin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen.
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6169362c9e8cb3a9ace2f300dd9d80aa9cd085
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568876"
---
# <a name="inventory-blocking"></a>Varastoesto

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleiskatsaus varastoestosta, joka on osa Supply Chain Managementin laaduntarkastusprosessia. Varastoeston avulla voit estää tuotteiden käsittelyn tai kulutuksen.

Voit estää varastonimikkeitä seuraavilla tavoilla:

- Manuaalisesti
- Laatutilauksen luomalla
- Käyttämällä prosessia, joka muodostaa laatutilauksen
- Käyttämällä varaston tilan estoa

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

|Asennus |Käyttäjätoiminto |Tulos |
|----|---|---|
| Laatuliitos määrittää, että ostotilauksen pakkausluettelon kirjauksen yhteydessä on luotava laatutilaus. Laatutilauksen nimikkeen ottoasetus määrittää, että 10 prosenttia ostotilausrivin määrästä on tarkistettava. Lisäksi, koska **Täysi esto**-asetus on valittuna nimikkeen ottoasetukset ilmaisevat, että ostotilausrivin koko määrä pitää estää tarkastuksen aikana riippumatta määrästä, joka lähetetään tarkastettavaksi. | Pakkausluettelo kirjataan. | Laatutilaus on luotu. Kymmenen prosenttia nimikkeen ostotilauksen määrästä lähetetään tarkistukseen. Ostotilausrivin täysi määrä on estetty. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Nimikkeiden esto käyttämällä varaston tilan estoa

Voit määrittää, mitkä varaston tilat saavat aikaan eston käyttämällä **Varastoesto**-parametria **Varaston tilat** -sivulla.  Varaston tiloja ei voi käyttää tuotanto-, myynti-, tai siirtotilauksien, lähtevien tapahtumien tai projekti-integrointien estotiloina. Ulosmeneville töille käytetään nimikkeitä, joilla on saatavilla oleva varaston tila. Jos on nimikkeitä, joiden tila on **Hajonnut**, ja pääsuunnittelu suoritetaan näillä nimikkeillä, niitä pidetään puuttuvina ja varasto täydennetään automaattisesti.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Ole varovainen estäessäsi nimikkeitä, jotka käyttävät sekä varaston tilan estoa että laatutilauksen estoa

Voit luoda laatutilauksen, joka liittyy varastoon, jonka varastotilalla on **Varastoesto**-parametri käytössä. Tässä tapauksessa laatutilaus luo ylimääräisen varaston estotietueen varastotilan luoman tietueen lisäksi. Koska laatutilauksen varastoestossa on käytössä **Oletetut vastaanotot** -parametri käytössä, tämä luo ylimääräisen *tilatun varastotapahtuman*, jonka myös varaston tila estää. Tämä yhdistelmä voi johtaa vaikeuksiin ymmärtää luotujen varastotapahtumien merkitystä, koska se näyttää siltä, että estetty kokonaismäärä ylittää käytettävissä olevan kokonaismäärän. Tutkimme tapahtumia esimerkissä, jossa vastaanotetaan 10 kpl A0001-nimikkeitä ja laatutilaus luodaan 1 kappaleelle. Käyttäytyminen riippuu myös siitä, onko **Varaa tilatut nimikkeet** -asetus käytössä **Varasto ja varastonhallinnan parametrit** -sivulla.

>[!NOTE]
>Jos käytät varaston tilan estoa ja laatutilauksia yhdessä, suosittelemme, että **Varaa tilatut nimikkeet** -asetus on otettu käyttöön.

### <a name="example-with-reserve-ordered-items-enabled"></a>Esimerkki, jossa Varaa tilatut nimikkeet on käytössä

Kun **Varaa tilatut nimikkeet** on käytössä, kaikkien varaston estotapahtumien tilaksi tulee joko *Varattu fyysinen* tai *Tilaukseen varattu*.

| Varastotapahtumaviite | Vastaanotto | Varasto-otto | Määrä | Toimipaikka | Varasto | Varaston tila | Toimipaikka | Rekisterikilpi | Kommentti |
|---|---|---|---|---|---|---|---|---|---|
| Ostotilaus | Ostettu | | 10 kpl | 2 | 24 | Esto | RECV | receiptLp1 | | 
| Varastoesto | | Varattu fyysinen | -9 kpl | 2 | 24 | Esto | | | Varaston tilan eston luoma tapahtuma |
| Varastoesto | | Varattu fyysinen | -1 kpl | 2 | 24 | Esto | RECV | receiptLp1 | Laatutilauksen otantaeston luoma tapahtuma |
| Varastoesto | Tilattu | | 1 kpl | 2 | 24 | Esto | RECV | receiptLp1 | Laatutilauksen otantaestossa odotetut vastaanotot |
| Varastoesto | | Tilaukseen varattu | 1 kpl | 2 | 24 | Esto | | | Varaston tilan eston luoma tapahtuma

### <a name="example-with-reserve-ordered-items-disabled"></a>Esimerkki, jossa Varaa tilatut nimikkeet on pois käytöstä

Kun **Varaa tilatut nimikkeet** poistetaan käytöstä, odotettuja vastaanottoja ei voi varata, koska niiden tilana on *Tilattu*, joten osa estosta jätetään tilaan *Tilauksessa*.

| Varastotapahtumaviite | Vastaanotto | Varasto-otto | Määrä | Toimipaikka | Varasto | Varaston tila | Toimipaikka | Rekisterikilpi | Kommentti |
|---|---|---|---|---|---|---|---|---|---|
| Ostotilaus | Ostettu | | 10 kpl | 2 | 24 | Esto | RECV | receiptLp1 | |
| Varastoesto | | Varattu fyysinen | -9 kpl | 2 | 24 | Esto | | | Varaston tilan eston luoma tapahtuma |
| Varastoesto | | Varattu fyysinen | -1 kpl | 2 | 24 | Esto | RECV | receiptLp1 | Laatutilauksen otantaeston luoma tapahtuma |
| Varastoesto | Tilattu | | 1 kpl | 2 | 24 | Esto | RECV | receiptLp1 | Laatutilauksen otantaestossa odotetut vastaanotot |
| Varastoesto | | Tilauksessa | 1 kpl | 2 | 24 | Esto | RECV | receiptLp1 | Varaston tilan eston luoma tapahtuma

Huomaa ero tapahtuman tilassa ja dimensioissa kahden tapauksen välillä. Tästä syystä on suositeltavaa ottaa käyttöön **Varaa tilatut nimikkeet** -vaihtoehto.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Lisäresurssit

[Luo ja ylläpidä varastoesto](tasks/create-maintain-inventory-blocking.md)

[Laadunhallintaprosessit](quality-management-processes.md)

[Tarkista tavaroiden laatu](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]