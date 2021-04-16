---
title: EUR-00011 EU:n myyntiluetteloraportin luominen
description: Tässä menettelyssä käsitellään EU-myyntiluettelon raportin muodostamista.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce3fa3eaae48499e58228d9d6dbf7ce7e97d2bd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821830"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011 EU:n myyntiluetteloraportin luominen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään EU-myyntiluettelon raportin muodostamista. Tällaisia toimintoja ovat yhteisön sisäisen kaupan tapahtumien siirtäminen EU-myyntiluetteloon ja raportin muodostaminen. Menettely sisältää myös yhteisön sisäisen kauppatapahtuman luomisen demokäyttöön. Lisätietoja EU:n myyntiluettelon raportoinnista ja edellytyksistä on ohjeissa.

Tämä menettely koskee kaikkia Euroopan maita/alueita. Menettelyssä on käytetty DEMF-yrityksen demotietoja ja Saksaa esimerkkinä kotimaasta tai -alueesta. Menettelyssä käytetään myös Portugalia esimerkkinä EU-maasta tai -alueesta. EU-myyntiluettelon raportointi on määritettävä ennen tämän menettelyn suorittamista.

Menettely on tarkoitettu kirjanpitäjille.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Luo yhteisön sisäinen myyntitapahtuma demokäyttöä varten
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Kirjoita Asiakastili-kenttään PRT-001.
4. Valitse OK.
5. Kirjoita Nimiketunnus-kenttään D0001.
6. Laajenna Rivin erittely -osa.
7. Valitse Asetukset-välilehti.
8. Kirjoita Nimikkeen arvonlisäveroryhmä -kenttään FULL.
9. Valitse Lisää rivi.
10. Kirjoita Nimiketunnus-kenttään D0003.
11. Kirjoita Nimikkeen arvonlisäveroryhmä -kenttään RED.
12. Valitse Tallenna.
13. Valitse toimintoruudussa Lasku.
14. Valitse Lasku.
15. Laajenna Parametrit-osa.
16. Valitse Määrä-kentässä Kaikki.
17. Laajenna osa Asetukset.
18. Lisää Laskun päivämäärä -kenttään päivämäärä 11.1.2016.
19. Valitse OK.
20. Valitse OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Siirrä yhteisön sisäisen kaupan tapahtumat EU-myyntiluetteloon
1. Valitse Vero > Ilmoitukset > Ulkomaankauppa > EU-myyntiluettelo.
2. Valitse Siirrä.
3. Siirrä nimiketapahtumat valitsemalla Nimike-kentässä Kyllä.
4. Siirrä palvelutapahtumat valitsemalla Palvelu-kentässä Kyllä.
    * Voit myös määrittää lisäsuodattimia siirrettäville yhteisön sisäisen kaupan tapahtumille.  
5. Valitse Siirrä.
    * Tarkista, että yhteisön sisäiset myyntitapahtumat on siirretty EU-myyntiluetteloon.  

## <a name="generate-the-eu-sales-list-report"></a> EU-myyntiluettelon raportin luominen
1. Valitse Raportointi.
2. Valitse Raportointikausi-kentässä Kuukausittain.
3. Lisää Päivämäärästä-kenttään päivämäärä 1.1.2016.
4. Valitse Luo tiedosto -kentässä Kyllä.
5. Valitse Luo raportti -kentässä Kyllä.
6. Kirjoita Tiedostonimi-kenttään EUSalesList.
7. Kirjoita Raporttitiedoston nimi -kenttään EUSalesList.
8. Kirjoita EU-myyntiluettelon rekisteröintitunnus -kenttään 123.
    * Tämä kenttä on käytettävissä vain Saksassa.  
    * Voit myös määrittää lisäsuodattimia raporttiin sisällytettäville yhteisön sisäisen kaupan tapahtumille.  
9. Valitse OK.
    * Tarkista, että avautuvassa ponnahdusikkunassa varmistetaan tiedoston ja valvontaraportin latautuminen.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Merkitse EU-myyntiluettelon rivien tilaksi Raportoitu
1. Valitse Merkitse.
2. Valitse Merkitse raportoiduksi.
3. Valitse luettelosta Laskun päivämäärä -kentän rivi.
4. Kirjoita Ehdot-kenttään 01/01/2016..01/31/2016.
5. Valitse luettelosta Raportoinnin tila -kentän rivi.
6. Valitse Ehdot-kentässä Sisällytetty.
    * Voit myös määrittää lisäsuodattimia raportoiduiksi merkittäville yhteisön sisäisen kaupan tapahtumille.  
7. Valitse OK.
8. Valitse Valinta-kentässä Raportoitu.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Merkitse EU-myyntiluettelon rivien tilaksi Suljettu
1. Valitse Merkitse.
2. Valitse Merkitse suljetuksi.
3. Merkitse luettelossa Laskun päivämäärä -kentän rivi.
4. Kirjoita Ehdot-kenttään 01/01/2016..01/31/2016.
5. Merkitse luettelossa Raportoinnin tila -kentän rivi.
6. Valitse Ehdot-kentässä Raportoitu.
    * Voit myös määrittää lisäsuodattimia suljetuiksi merkittäville yhteisön sisäisen kaupan tapahtumille.  
7. Valitse OK.
8. Valitse Valinta-kentässä Suljettu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]