---
title: Kanavan palautus- ja hyvityskäytännön luominen ja päivittäminen
description: Tässä ohjeaiheessa kerrotaan, miten kanavan palautus- ja hyvityskäytäntö määritetään.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412071"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanavan palautus- ja hyvityskäytännön luominen ja päivittäminen

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Kanavan palautuskäytännön avulla jälleenmyyjät voivat määrittää Dynamics 365 Commercessa, mitkä maksutarjoukset voidaan sallia myyntipisteen (POS) palautuksen käsittelyyn.  

Tässä ohjeaiheessa kuvataan, miten kanavan palautus- ja hyvityskäytäntö määritetään.

Tämän käytännön soveltamisala rajoittuu tällä hetkellä siihen, että voidaan määrittää kanaville sallitut maksutarjoukset. Sallittu-luettelo perustuu oston tekemiseen käytettyihin maksutapoihin. Esimerkki:

- Jos osto on tehty käyttämällä lahjakorttia, myymäläkäytännöllä on tarkoitus käsitellä palautuksia vain uuteen lahjakorttiin tai tallentaa myymäläluottoa. 
- Jos myynti tehdään käteisellä, hyvityksen sallitut vaihtoehdot ovat käteinen, lahjakortti ja asiakastili, mutta ei luottokorttia. 


## <a name="enable-return-policy"></a>Ota käyttöön palautuskäytäntö

Voit ottaa kanavan palautuksen käytäntötoiminnon käyttöön seuraavasti:

1. Avaa **Ominaisuuksien hallinta** -työtilaan Dynamics 365 Commercessa.
2. Etsi ominaisuuksien nimien luettelosta **Ota käyttöön kanavan palautuksen käytännöt** -toiminto.
3. Valitse **Ota käyttöön nyt**. 

## <a name="configure-return-policy"></a>Määritä palautuskäytäntö

Noudattamalla näitä ohjeita voit määrittää jälleenmyyntimyymälän tai online-vähittäismyyntikanavan palautuksen.

1. Siirry kohtaan **Retail ja Commerce** \> **Kanava-asetukset** \> **Palautukset** \> **Kanavan palautuskäytäntö**.

2. Valitse **Uusi** luodaksesi uuden palautuskäytännön mallin. Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta. Lisää uusille malleille nimi ja kuvaus, joiden avulla voit tunnistaa käytännön, kun sitä käytetään kanavassa.

   ![Uuden palautuskäytännön lisääminen](media/Return-policy-page1.png "Uuden palautuskäytännön lisääminen")
     
   
3. Määritä **Sallittu palautuksen maksutapa** -osassa **Sallitut** palautusmaksutarjoukset, jotka koskevat kutakin maksutapaa.
   ![Lisää maksutavat](media/Return-policy-page2.PNG "Määritä sallitut toimitustavat maksutyypeittäin")
   
    > [!IMPORTANT]
    > - Maksut johdetaan organisaatiolle määritetyistä toimitustavoista.
    > - Kun lisäät sallitun palautusmaksuvälinetyypin jokaiselle luetellulle maksutavalle, voit varmistaa, että palautusmaksuvälinetyyppiin voidaan tehdä palautus.
    
4. Liitä palautuskäytäntömalli myymälöihin, joissa sitä käytetään. Valitse **Lisää** **vähittäismyyntikanavat** -välilehdestä ja liitä käytettävissä olevat kanavat. 

    - Valitse **Valitse organisaatiosolmut** -valintaikkunassa ne myymälät, alueet ja organisaatiot, joihin malli liitetään.
    - Kuhunkin myymälään voidaan liittää vain yksi myymälän palautuskäytäntömalli.
    - Valitse myymälät, alueet tai organisaatiot nuolipainikkeiden avulla.
    - Käytännön voimaan tulopäivämäärä on aika, jolloin käytäntöjä käytetään kanavissa, ja kanavatyöt suoritetaan. 

    ![Valitse organisaatiosolmujen valintaikkuna](media/Return-policy-page3.PNG "Valitse organisaatiosolmujen valintaikkuna")

5. Suorita **1070**-työ **Jakeluaikataulu**-sivulla, jotta kanavan palautuskäytäntö tulisi käytettäväksi POS:issa.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Kanavien palauttamisen käytännön esikatselu POS-sovelluksessa

Voit tarkastella myyntipisteen sallittuja palautuksen maksuvälinetyyppejä noudattamalla jommankumman seuraavan esimerkin ohjeita.

1. Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.
2. Valitse **Vaihto ja laatikko** -kohdasta **Näytä kirjauskansio**.
3. Valitse tapahtuma, joka on osa palautusta. 
4. Valitse palautettavat nimikkeet ja valitse maksutapa.  
- Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.
- Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.
- Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.

-tai-

1. Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.
2. Valitse **Palauta tapahtuma** ja syötä kuitin tunnus viivakoodin tarkistuksen tai manuaalisen merkinnän avulla. 
3. Valitse tapahtuma, joka on osa palautusta. 
4. Valitse palautettavat nimikkeet ja valitse maksutapa.  
- Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.
- Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.
- Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.

![Palautus ei sallittu](media/Return-policy-page6.png "Palautustyyppi ei sallittu")



![Maksutapaluettelo](media/Return-policy-page5.PNG "Palautustyypit eivät ole sallittuja")


[!INCLUDE[footer-include](../includes/footer-banner.md)]