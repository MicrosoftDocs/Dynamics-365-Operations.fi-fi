---
title: EUR-00012 EU-saapumistodistuksen myöntäminen
description: Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95c1f3f87175a2c2a2887a4ed2ebde1bd7d1c0b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227963"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 EU-saapumistodistuksen myöntäminen

[!include [banner](../../includes/banner.md)]
Tässä menettelyssä selvitetään, miten EU-saapumistodistus otetaan käyttöön, miten asiakastiliä muutetaan varmenteiden käyttöä varten ja miten varmenne myönnetään. Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.


## <a name="enable-entry-certificate-management"></a>Ota käyttöön merkinnän varmenteen hallinta
1. Valitse Myyntireskontra > Asetukset > Myyntireskontran parametrit.
2. Valitse Lähetykset-välilehti.
3. Laajenna Merkinnän varmenne -osaa.
4. Valitse Ota käyttöön merkinnän varmenteen hallinta -kentässä Kyllä.
5. Valitse Ota käyttöön merkinnän varmenteen myöntäminen -kentässä Kyllä.
6. Valitse Numerojärjestykset-välilehti.
7. Etsi ja valitse luettelosta Merkinnän varmenne -rivi.
8. Anna tai valitse Numerojärjestyskoodi-kentässä arvo.

## <a name="set-up-a-customer"></a>Määritä asiakas
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Tili-kenttää arvolla DE-015.
3. Avaa asiakastilin tiedot.
4. Valitse Muokkaa.
5. Laajenna Lasku ja toimitus -osa.
6. Valitse Merkinnän varmenne tarvitaan -kentässä Kyllä.
7. Valitse Myönnä merkinnän varmenne -kentässä Kyllä.
8. Valitse Tallenna.

## <a name="create-an-eu-entry-certificate-automatically"></a>Luo EU-saapumistodistus automaattisesti
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
4. Valitse OK.
5. Syötä tai valitse arvo Nimiketunnus-kentässä.
6. Valitse Tallenna.
7. Valitse toimintoruudussa Kerää ja pakkaa.
8. Valitse Kirjaa pakkausluettelo.
9. Laajenna Parametrit-osa.
10. Valitse Määrä-kentässä Kaikki.
11. Poista Myönnä merkinnän varmenne -valintaruudun valinta.
    * Saapumistodistus voidaan myöntää pakkausluettelon kirjauksen aikana tai tilausta laskutettaessa. Älä valitse Myönnä merkinnän varmenne -valintaruutua ja myönnä se myöhemmin.  
12. Valitse OK.
13. Valitse OK.
14. Valitse toimintoruudussa Lasku.
15. Valitse Lasku.
    * Tarkista, että Merkinnän varmenne tarvitaan- ja Myönnä merkinnän varmenne -valintaruudut on valittu Yhteenveto-kohdassa.  Jos valitset Tulosta merkinnän varmenne - valintaruudun, voit tulostaa varmenteen.  
16. Valitse OK.
17. Valitse OK.
18. Valitse toimintoruudussa Lasku.
19. Valitse Lasku.
20. Valitse toimintoruudussa Lasku.
21. Valitse Näytä myönnetyt merkinnän varmenteet.
22. Valitse Tulosta.
23. Sulje sivu.
24. Voit muuttaa tilaa valitsemalla Muuta.
25. Valitse Uusi tila -kentässä vaihtoehto.
26. Valitse OK.
27. Sulje sivu.

## <a name="create-an-eu-entry-certificate-manually"></a>Luo EU-saapumistodistus manuaalisesti
1. Valitse toimintoruudussa Lasku.
2. Valitse Luo merkinnän varmenne.
3. Valitse OK.
4. Valitse toimintoruudussa Lasku.
5. Valitse Näytä myönnetyt merkinnän varmenteet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]