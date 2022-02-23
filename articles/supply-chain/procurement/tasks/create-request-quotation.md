---
title: Luo tarjouspyyntö
description: Tässä menettelyssä näytetään, miten tarjouspyyntö luodaan.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59202cb6678660ae035f9f76ebe4267bac01d78f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019901"
---
# <a name="create-a-request-for-quotation"></a>Luo tarjouspyyntö

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten tarjouspyyntö luodaan. Se on yleensä ostoedustajan tehtävä. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Ennen aloittamista on määritettävä pyyntötyypit. Kun olet suorittanut tämän tehtävän ja luonut sekä lähettänyt tarjouspyynnön, voit sitten määrittää toimittajakohtaiset vastaukset, tehdä niistä vertailun ja myöntää sopimuksen.


## <a name="prepare-a-new-rfq"></a>Valmistele uusi tarjouspyyntö
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt**.
2. Valitse **Uusi**.
    Käytettävissä ovat seuraavat ostotyypit: ostotilaus (oletusarvo): asiakirja, jolla vahvistetaan tarjous ostaa tuotteita, tai hyväksyntä tarjouksesta myydä tuotteita maksua vastaan. Ostoehdotus: tämä tyyppi valitaan automaattisesti, jos luot tarjouspyynnön suoraan ostoehdotuksesta. Jos valitset tämän tyypin manuaalisesti, saat virhesanoman. Ostosopimus: sopimus tietyn tuotemäärän tai tietyn arvoisen tuotemäärän ostamiseksi toimittajalta tiettynä ajanjaksona. Jos valitset tämän asetuksen, ostosopimusta koskeva päivämääräväli on syötettävä.  
3. Syötä **Asiakirjan otsikko** -kenttään arvo.
4. Syötä tai valitse arvo **Pyyntötyyppi**-kentässä.
    + Jos tulosmalli on liitetty pyyntötyyppiin, tämä on luotavan tarjouspyynnön oletusarvoinen pisteytystapa. Pisteytystavan voi muuttaa jälkikäteen.  
    + Kirjoita päivämäärä **Toimituspäivämäärä**-kenttään.  
    + Valitse päivämäärä, johon mennessä haluat saada pyydetyt nimikkeet.  
    + Anna päivämäärä ja kellonaika **Vanhentumispäivä ja -aika** -kenttään.  
    + Määritä päivämäärä ja kellonaika, johon mennessä toimittajien on vastattava tarjouspyyntöön.  
5. Anna tai valitse **Varasto**-kentässä arvo. Oletusarvoinen toimitusosoite on varaston osoite.  
6. Valitse **OK**.

## <a name="add-lines"></a>Lisää rivejä

Kun olet määrittänyt tarjouspyynnön perustiedot, määritä tavarat tai palvelut, joihin haluat saada tarjouksen toimittajilta. Rivin oletustyyppi on nimike.

1. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Jos käytössä on USMF, voit valita T0020.  
2. Anna **Määrä**-kentässä numero.
3. Valitse **Lisää rivi**.
4. Valitse **Rivin tyyppi** -kenttään "Luokka". Luokkarivin tyypin avulla voi luoda tarjouspyyntöjä muille kuin varastotuotteille tai palveluille. Tavaran tai palvelun tyyppi on sitten valittava hankintaluokkien hierarkiasta.  
5. Kirjoita tai valitse arvo **Hankintaluokka**-kenttään.
6. Kirjoita arvo **Tuotteen nimi**-kenttään.
7. Anna **Määrä**-kentässä numero.
8. Syötä tai valitse arvo **Yksikkö**-kenttään.

## <a name="add-vendors"></a>Lisää toimittajia
1. Napsauta **Otsikko** vaihtaaksesi rivinäkymästä otsikkonäkymään. 
2. Laajenna **Toimittaja**-osa.
3. Napsauta kohtaa **Toimittajien lisääminen automaattisesti**. Voit lisätä toimittajia tarjouspyyntöön automaattisesti hankintaluokan pyydettyjen nimikkeiden perusteella. Jos riveillä oleville luokille ei ole hyväksytty toimittajia, voit lisätä toimittajat manuaalisesti.  
4. Valitse **Lisää**.
5. Anna tai valitse arvo **Toimittajatili**-kentässä.
6. Valitse **Lisää**.
7. Anna tai valitse arvo **Toimittajatili**-kentässä. Kun olet valinnut toimittajan, tila on Luotu. Tämä tarkoittaa sitä, että toimittajatiedot on tallennettu tarjouspyyntöön, mutta et ole vielä lähettänyt tarjouspyyntöä toimittajalle. Voit lisätä toimittajan tarjouspyyntöön toimittajan tilasta riippumatta.  

## <a name="send-the-rfq-to-vendors"></a>Lähetä tarjouspyyntö toimittajille
1. Valitse **toimintoruudussa** **Lähetä**. Tarkista Lähetetään tarjouspyyntöä -sivulta, että luettelo sisältää ne toimittajat, jolle haluat lähettää tarjouspyynnön.  
2. Valitse **Tulosta**. Tämän valintaikkunan avulla voit tulostaa tarjouspyynnön. Voit tulostaa halutessasi vastauslomakkeen, jonka sisältö määritellään hankintaparametreissa Voit valita vastauslomakkeiden tulostustavan, napsauttamalla Tulostuksen lisäasetuksia, kun olet avannut Tulosta-valintaikkunan. Yksi tarjouspyyntö tulostetaan kullekin toimittajalle, joka sisältää rivit, joiden tila on Luotu tai Lähetetty. Järjestelmä ei tulosta peruutettuja rivejä eikä rivejä, joilla on rekisteröityjä vastauksia.   
3. Valitse **Peruuta**.
4. Valitse **OK**.
5. Sulje sivu.
6. Sulje sivu.

## <a name="view-the-rfq-journal"></a>Näytä tarjouspyyntöjen kirjauskansio
1. Valitse **Hankinnat > Tarjouspyynnöt > Tarjouspyynnön seuranta > Tarjouspyynnön kirjauskansiot**.
2. Napsauta **Esikatselu/tulostus**.
3. Valitse **Alkuperäisen esikatselu**.
4. Sulje sivu.
5. Sulje sivu.

