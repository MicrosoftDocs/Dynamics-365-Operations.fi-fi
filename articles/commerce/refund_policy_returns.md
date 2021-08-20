---
title: Kanavan palautus- ja hyvityskäytännön luominen ja päivittäminen
description: Tässä ohjeaiheessa kerrotaan, miten kanavan palautus- ja hyvityskäytäntö määritetään.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 5c32156aea5f43d41b51f34b45b5b6dfedb5cad0f948924ecea9b3d89e6bb402
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763689"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanavan palautus- ja maksuhyvityskäytännön luominen ja päivittäminen

[!include [banner](includes/banner.md)]

Kanavan palautuskäytännön avulla jälleenmyyjät voivat määrittää Dynamics 365 Commercessa, mitkä maksutarjoukset voidaan sallia myyntipisteen (POS) palautuksen käsittelyyn.  

Tässä ohjeaiheessa kuvataan, miten kanavan palautus- ja hyvityskäytäntö määritetään.

Tämän käytännön soveltamisala rajoittuu tällä hetkellä siihen, että voidaan määrittää kanaville sallitut maksutarjoukset. Sallittu-luettelo perustuu oston tekemiseen käytettyihin maksutapoihin. Esimerkki:

- Jos osto on tehty käyttämällä lahjakorttia, myymäläkäytännöllä on tarkoitus käsitellä palautuksia vain uuteen lahjakorttiin tai tallentaa myymäläluottoa. 
- Jos myynti tehdään käteisellä, hyvityksen sallitut vaihtoehdot ovat käteinen, lahjakortti ja asiakastili, mutta ei luottokorttia. 

## <a name="enable-return-policy"></a>Ota käyttöön palautuskäytäntö

Jos haluat ottaa käyttöön kanavanpalautuskäytäntötoiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.

1. Avaa **Ominaisuuksien hallinta** -työtilaan Dynamics 365 Commercessa.
1. Etsi ominaisuuksien nimien luettelosta **Ota käyttöön kanavan palautuksen käytännöt** -toiminto.
1. Valitse **Ota käyttöön nyt**.
1. Suorita **1110** (Yleinen konfigurointi) -työ **Jakeluaikataulu**-sivulta jakaaksesi ominaisuuden muutoksen.

## <a name="initialize-the-commerce-scheduler"></a>Commerce-ajastuksen alustaminen

Kun kanavan **Ota kanavan palautuskäytännöt käyttöön** -ominaisuus on käytössä, Commerce-ajastus on alustettava, jotta uudet ominaisuustietokannan muutokset voidaan lisätä Commerce Data Exchange (CDX) -synkronoinnin avulla. 

Voit määrittää Commerce-ajoitustoiminnon Commerce Headquarters -sovelluksessa seuraavasti.

- Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Alusta Commerce-ajastus**. Vaihtoehtoisesti voit tehdä haun käyttämällä Alusta Commerce -ajoitustoiminto -lausetta.
- Varmista **Alusta Commerce-ajoitustoiminto** -valintaikkunassa, että **Poista olemassa oleva määritys** -vaihtoehdon arvoksi on määritetty **Ei**. Valitse sitten **OK**.

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
