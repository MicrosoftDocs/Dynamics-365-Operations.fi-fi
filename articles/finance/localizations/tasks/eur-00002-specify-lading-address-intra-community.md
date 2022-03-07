---
title: EUR-00002 Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle
description: Tässä toimintaohjeessa kuvataan, miten määrität kuormausosoitteen yhteisönsisäiselle kauppatapahtumalle.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68a62a26be418b7a0cb8e17532d022d76cd552411f438ffc5a0ddad589a9e476
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780790"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle

[!include [banner](../../includes/banner.md)]

Tässä toimintaohjeessa kuvataan, miten määrität kuormausosoitteen yhteisönsisäiselle kauppatapahtumalle. Esimerkkinä saksalainen yritys tilaa nimikkeitä toimittajalta, jolla on saksalainen osoite. Toimittajalla on varasto Italiassa ja toimittaa nimikkeet sieltä. Tämä toimitus on raportoitava Intrastatiin. Sama menettely koskee asiakaspalautuksia.
Tämä menettely koskee kaikkia Euroopan maita/alueita. Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa. Intrastat-raportointi on määritettävä ennen tämän menettelyn suorittamista. Menettely on tarkoitettu kirjanpitäjille. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

1. Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Anna tai valitse arvo
    * Voit valita esimerkiksi arvon DE-001 Tällä toimittajalla on saksalainen käyntiosoite.  
4. Valitse OK.
5. Merkitse valittu rivi luettelossa.
6. Syötä tai valitse Nimiketunnus-kentän arvoksi D0001.
7. Valitse Tallenna.
8. Valitse toimintoruudussa Vastaanota.
9. Valitse Kuljetustiedot.
10. Syötä päivämäärä ja kellonaika Kuormauspäivämäärä ja -aika -kenttään.
11. Valitse Lisää uusi osoite.
12. Valitse Uusi ja luo uusi osoite, jonka tarkoitus on Kuormaus.
13. Kirjoita Nimi tai kuvaus -kenttään "italialainen".
14. Valitse arvoksi Kuormaus.
    * Huomaa, että osoitteen tarkoituksen tulee olla Kuormaus.  
15. Syötä tai valitse arvoksi ITA Maa/alue-kentässä.
16. Valitse Tallenna.
17. Sulje sivu.
18. Valitse Tallenna.
    * Varmista, että kuormausosoite on oikein.  
19. Sulje sivu.
20. Valitse toimintoruudussa Osta.
21. Valitse Vahvista.
22. Valitse toimintoruudussa Lasku.
23. Valitse Lasku.
24. Kirjoita arvo Numero-kenttään.
25. Kirjoita päivämäärä Laskun päivämäärä -kenttään.
26. Valitse Oletusarvo kohteesta: Tuotteen vastaanottomäärä, kun haluat avata valintaikkunan.
27. Valitse "Tilattu määrä" -vaihtoehto Rivien oletusmäärä -kentässä.
28. Valitse OK.
29. Valitse Kuljetustiedot.
    * Varmista, että tavarat toimitettiin Italiasta. Voit muokata kuormauksen tietoja tarvittaessa.  
30. Sulje sivu.
31. Valitse Kirjaa.
32. Sulje sivu.
33. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
34. Valitse Siirrä.
35. Valitse Toimittajan lasku -kentässä Kyllä.
36. Valitse OK.
37. Valitse Yleiset-välilehti.
    * Etsi juuri luotu rivi ja varmista, että lähettäjä toimitti tavarat Italiasta.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]