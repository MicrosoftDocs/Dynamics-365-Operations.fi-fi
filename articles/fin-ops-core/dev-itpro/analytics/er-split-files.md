---
title: Luotujen XML-tiedostojen jakaminen tiedoston koon ja sisällön määrän perusteella
description: Tässä artikkelissa on tietoja siitä, miten voit jakaa luodut tiedostot koon ja sisältönimikemäärän mukaan.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280092"
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

- [ER-mallin määritys - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER-muodon määritys - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Lisäresurssit
[Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)

[Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
