---
title: Tilikauden sulkeminen
description: Tässä toimintaohjeessa selvitetään tilinkauden lopetusprosessi, joka siirtää saldot uuteen tilikauteen.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82cc7e4077a1bd50eab30f234c2f63c79e81d84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994687"
---
# <a name="close-the-fiscal-year"></a>Tilikauden sulkeminen

[!include [banner](../../includes/banner.md)]

Tässä toimintaohjeessa selvitetään tilinkauden lopetusprosessi, joka siirtää saldot uuteen tilikauteen.


## <a name="validate-year-end-close-parameters"></a>Vahvista tilikauden lopetuksen parametrit
1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**.
2. Laajenna **Tilikauden lopetus** -osa.
3. Valitse Kyllä tai Ei -arvo asetukselle **Poista päätöstapahtumat siirron yhteydessä**.
    
    Jos tilikausi on jo päätetty ja tilikauden lopetus suoritetaan uudelleen, tämä asetus on tärkeä. Jos arvoksi asetetaan Kyllä, edellisen tilikauden lopetustosite poistetaan ja uusi tosite luodaan kaikkien tilien alkusaldoille. Jos arvoksi asetetaan Ei, edellinen tosite säilytetään ja uusi tosite luodaan vain oikaisutapahtumille, jotka kirjattiin tilikauden lopetuksen jälkeen.

4. Valitse Kyllä- tai Ei-arvo asetukselle **Luo päätöstapahtumat siirron yhteydessä**.

    Jos arvoksi asetetaan Kyllä, luodaan kaksi tapahtumaa. Yksi tosite luodaan lopetettavaan tilivuoteen, jotta tuloskirjanpitotilit ovat tasassa, ja toinen tosite luodaan seuraavaan tilivuoteen alkusaldoille. Jos arvo on Ei, yksi tosite luodaan uuden tilikauden alkusaldoille.  

5. Valitse Kyllä- tai Ei-arvo asetukselle **Muuta tilivuoden tilaksi pysyvästi suljettu**.

    Jos arvoksi on asetettu Kyllä, tilikauden tilaksi asetetaan olla Suljettu pysyvästi.  Koska pysyvästi suljettua kautta ei voi avata uudelleen, on parasta asettaa tämän asetuksen arvoksi Ei.  

6. Valitse Kyllä- tai Ei-arvo asetukselle **Tositenumero syötettävä manuaalisesti tilikauden lopetusprosessin aikana**.

    Jos arvoksi asetetaan Kyllä, tositenumero on syötettävä manuaalisesti tilikauden lopetusprosessin aikana. Tositenumeron luomiseen ei käytetä numerosarjaa. On suositeltavinta arvoksi Kyllä.  

7. Sulje sivu.
8. Valitse **Kirjanpito > Kausi suljettu > Tilikauden lopetus**.
9. Luo tilikauden lopetusmalli valitsemalla **Uusi**.

    Mallin voi luoda yritysjoukolle, jolle tilikauden lopetus suoritetaan. Tätä mallia voidaan käyttää uudelleen vuodesta toiseen.  

10. Kirjoita **Ryhmän nimi** -kenttään tilikauden lopetusmallin nimi.
11. Valitse **Kirjanpidon vuosikalenteri** -kentässä tilikausi, jolle malli luodaan.

    Vain yritykset, jotka käyttävät samaa tilikautta, voidaan liittää tilikauden lopetusmallin ryhmään. Tämä johtuu siitä, että tilikauden lopetus tehdään valitsemalla tilikausi, ei päivämäärä.  

12. Valitse **toimintoruudussa** **Tallenna**.
13. Valitse **Oikeushenkilöt** -osasta **Lisää** valitaksesi tämän mallin juridiset entiteetit.
    
    Yritykset voidaan lisätä joko valitsemalla ne tai valitsemalla organisaatiohierarkia.  Organisaatiohierarkiasta lisätään ainoastaan yritykset, joilla on sama tilikausi.  

14. Valitse joko yritykset tai organisaatiohierarkia.
15. Valitse **OK**.
16. Valitse Kyllä tai Ei asetuksessa **Siirrä tasedimensiot**.

    Suositeltavinta on asettaa tämän asetuksen arvoksi Kyllä tasetileille. Tämä säilyttää kirjattujen tapahtumien taloushallinnon dimensiot, kun alkusaldot luodaan tasetileille. Tulostileille voit valita, säilytetäänkö taloushallinnon dimensiot (Sulje kaikki), kun saldot siirretään jakamattomiin voittoihin tai voit valita, että taloushallinnon dimension vaihdetaan eri dimensioarvoihin (Sulje yksi). Jos valitset arvoksi Sulje yksi, voit määrittää tietyn dimensioarvon kullekin dimensiolle tai halutessaan myös jättää arvon tyhjäksi.  

17. Valitse **Tallenna**.
18. Aloita tilikauden lopetus valitsemalla **Suorita tilikauden lopetus** **toimintoruudusta**. Tilikauden lopetus ajetaan valitulle mallille.  
19. Valitse kaikki mallin yritykset tai niiden osajoukko, joille tilikauden lopetus suoritetaan.

    Kun tilikauden lopetus ajetaan ensimmäisen kerran, useimmat organisaatiot tuottavat alkusaldot ajamalla tilikauden lopetuksen kaikille mallin yrityksille. Jos oikaisuja tehdään lopetuksen jälkeen, tilikauden lopetuksen voi ajaa vain niille yrityksille, joilla oikaisuja on.  

20. Valitse **OK**.
21. Valitse lopetettava tilikausi.
22. Kirjoita arvo kenttään **Tosite**. Se on suositeltavinta sisällyttää tilikausi tositteen numeroon, jotta luotu tilikauden lopetustosite on helpompi löytää.  
23. Tilikauden lopetus ajetaan oletusarvoisesti eräajona. On suositeltavinta ajaa pitkään kestävät prosessit eräajona. Tämä on yleensä pitkäkestoinen prosessi, minkä vuoksi oletusasetus on eräajon käyttäminen.  
24. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]