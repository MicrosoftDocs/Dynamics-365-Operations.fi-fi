---
title: "Luotujen XML-tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella"
description: "Tässä aiheessa on tietoja siitä, miten voit jakaa luodut tiedostot koon ja sisältönimikemäärän mukaan."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0f13194575e2f19f585f09ffad99144c9a9fc3b1
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Luotujen XML-tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella

[!include[banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muotoja luodaksesi lähteviä tiedostoja XML-muodossa. Joskus nämä asiakirjat voidaan hyväksyä vain, kun ne täyttävät tietyt ehdot, kuten tiedoston enimmäiskoko tai joidenkin XML-solmujen enimmäismäärä. Voit suunnitella ER-muotoja luodaksesi sähköisiä asiakirjoja, jotka täyttävät tiedostojen vastaanottajien vaatimukset.

- FILE-muotoelementille voit määrittää tiedostokoon rajoituksen ER-lausekkeena. Jos määritetty raja ylittyy ER-raporttia luotaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.
- Kaikille XML ELEMENT -muodoille voit määrittää elementtien määrän rajoituksen ER-lausekkeena. Jos luotavan tiedoston XML-solmujen määritetty raja ylittyy ER-raporttia suoritettaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.
- Kaikille XML SEQUENCE -muotoelementeille voit määrittää alielementtien määrän rajoituksen ER-lausekkeena. Jos luotavan tiedoston muotoelementin sisäkkäisten XML-solmujen määritetty raja ylittyy ER-raporttia suoritettaessa, ER viimeistelee nykyisen tiedoston luonnin ja siirtyy sitten seuraavan tiedoston luomiseen.
- Voit merkitä minkä tahansa XML ELEMENT muotoelementin katkeamattomaksi. Näin voit säilyttää sisäkkäiset nimikkeet XML-solmuille, jotka on luodaan muotoelementin alle yhdessä muodostetussa tiedostossa.

XML ELEMENT- ja XML SEQUENCE -muotoelementtien lisäksi voit lisätä XML-solmuja luotavaan tiedostoon myös RAW XML -muotoelementin avulla. Kuitenkaan solmuja, jotka lisäät RAW XML -muotoelementin avulla, ei oteta huomioon laskettaessa solmujen määrää, kun arvioidaan elementtien määrien rajoituksia.

Jos olet määrittänyt tiedostokohteita FILE-muotoelementille, joka on määritetty jakamaan luodun tuloksen aina, kun tietyt rajat ylittyvät, muodostetun tuloksen kukin osa lähetetään määritettyyn tiedostokohteeseen yksittäisenä tiedostona. Jotta voisit nimetä tulostetta jakamalla luodut tiedostot yksilöllisesti, sinun on määritettävä ER-lauseke FILE-muotoelementille. Jos lisäät NUMBER SEQUENCE -tyypin ER-tietolähteen, numerosarjaa kasvatetaan kullekin tuloksen jaon osalle.

Lisätietoja tästä toiminnosta saat toistamalla tehtäväoppaan **ER – XML-tiedostojen jakaminen tiedoston koon tai sisältökohteiden määrän perusteella**, joka on osa **7.5.4.3 Hanki/Kehitä IT-palvelu/ratkaisukomponentit (10677)** -liiketoimintaprosessia, jonka voi ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684). Tässä tehtäväoppaassa näet, miten voit määrittää ER-muodon jakamaan luotavat tiedostot rajoitusten koon ja sisällön nimikemäärän perusteella. Lataa seuraavat tiedostot suorittaaksesi tehtäväoppaan:

- [ER-mallin määritys - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER-muodon määritys - XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Lisäresurssit
[Sähköisen raportoinnin kohteet](electronic-reporting-destinations.md)

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

