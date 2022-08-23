---
title: Kanavan palautus- ja maksuhyvityskäytännön luominen ja päivittäminen
description: Tässä artikkelissa kerrotaan, miten kanavan palautus- ja hyvityskäytäntö määritetään.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: b93852bfb7c6f5a9f2f83f30a1f76da3f9559c7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286834"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanavan palautus- ja maksuhyvityskäytännön luominen ja päivittäminen

[!include [banner](includes/banner.md)]

Kanavan palautuskäytännön avulla jälleenmyyjät voivat määrittää Dynamics 365 Commercessa, mitkä maksutarjoukset voidaan sallia myyntipisteen (POS) palautuksen käsittelyyn.  

Tässä artikkelissa kuvataan, miten kanavan palautus- ja hyvityskäytäntö määritetään.

Tämän käytännön soveltamisala rajoittuu tällä hetkellä siihen, että voidaan määrittää kanaville sallitut maksutarjoukset. Sallittu-luettelo perustuu oston tekemiseen käytettyihin maksutapoihin. Esimerkki:

- Jos osto on tehty käyttämällä lahjakorttia, myymäläkäytännöllä on tarkoitus käsitellä palautuksia vain uuteen lahjakorttiin tai tallentaa myymäläluottoa. 
- Jos myynti tehdään käteisellä, hyvityksen sallitut vaihtoehdot ovat käteinen, lahjakortti ja asiakastili, mutta ei luottokorttia. 

## <a name="enable-return-policy"></a>Ota käyttöön palautuskäytäntö

Jos haluat ottaa käyttöön kanavanpalautuskäytäntötoiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.

1. Avaa **Ominaisuuksien hallinta** -työtilaan Dynamics 365 Commercessa.
1. Etsi ominaisuuksien nimien luettelosta **Ota käyttöön kanavan palautuksen käytännöt** -toiminto.
1. Valitse **Ota käyttöön nyt**.
1. Suorita **1110** (Yleinen konfigurointi) -työ **Jakeluaikataulu**-sivulta jakaaksesi ominaisuuden muutoksen.

## <a name="configure-return-policy"></a>Määritä palautuskäytäntö

Noudattamalla näitä ohjeita voit määrittää jälleenmyyntimyymälän tai online-vähittäismyyntikanavan palautuksen.

1. Siirry kohtaan **Retail ja Commerce** \> **Kanava-asetukset** \> **Palautukset** \> **Kanavan palautuskäytäntö**.

1. Valitse **Uusi** luodaksesi uuden palautuskäytännön mallin. Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta. Lisää uusille malleille nimi ja kuvaus, joiden avulla voit tunnistaa käytännön, kun sitä käytetään kanavassa.

   ![Uuden palautuskäytännön lisääminen.](media/Return-policy-page1.png)
     
   
1. Määritä **Sallittu palautuksen maksutapa** -osassa **Sallitut** palautusmaksutarjoukset, jotka koskevat kutakin maksutapaa.
   ![Määritä sallitut toimitustavat maksutyypeittäin.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Maksut johdetaan organisaatiolle määritetyistä toimitustavoista.
    > - Kun lisäät sallitun palautusmaksuvälinetyypin jokaiselle luetellulle maksutavalle, voit varmistaa, että palautusmaksuvälinetyyppiin voidaan tehdä palautus.
    
1. Liitä palautuskäytäntömalli myymälöihin, joissa sitä käytetään. Valitse **Lisää** **vähittäismyyntikanavat** -välilehdestä ja liitä käytettävissä olevat kanavat. 

    - Valitse **Valitse organisaatiosolmut** -valintaikkunassa ne myymälät, alueet ja organisaatiot, joihin malli liitetään.
    - Kuhunkin myymälään voidaan liittää vain yksi myymälän palautuskäytäntömalli.
    - Valitse myymälät, alueet tai organisaatiot nuolipainikkeiden avulla.
    - Käytännön voimaan tulopäivämäärä on aika, jolloin käytäntöjä käytetään kanavissa, ja kanavatyöt suoritetaan. 

    ![Valitse organisaatiosolmujen valintaikkuna.](media/Return-policy-page3.png)

1. Suorita **1070**-työ **Jakeluaikataulu**-sivulla, jotta kanavan palautuskäytäntö tulisi käytettäväksi POS:issa.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Kanavien palauttamisen käytännön esikatselu POS-sovelluksessa

Voit tarkastella myyntipisteen sallittuja palautuksen maksuvälinetyyppejä noudattamalla jommankumman seuraavan esimerkin ohjeita.

1. Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.
1. Valitse **Vaihto ja laatikko** -kohdasta **Näytä kirjauskansio**.
1. Valitse tapahtuma, joka on osa palautusta. 
1. Valitse palautettavat nimikkeet ja valitse maksutapa.  
    - Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.
    - Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.
    - Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.

-tai-

1. Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.
1. Valitse **Palauta tapahtuma** ja syötä kuitin tunnus viivakoodin tarkistuksen tai manuaalisen merkinnän avulla. 
1. Valitse tapahtuma, joka on osa palautusta. 
1. Valitse palautettavat nimikkeet ja valitse maksutapa.  
    - Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.
    - Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.
    - Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.

![Palautustyyppi ei ole sallittu.](media/Return-policy-page6.png)



![Sallitut palautustyypit.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
