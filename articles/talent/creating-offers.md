---
title: Tarjousten luominen, hyväksyminen ja allekirjoittaminen
description: Tässä ohjeaiheessa käsitellään hakijalle tehtävän tarjouksen luomista, hyväksymistä ja allekirjoittamista Dynamics 365 Talentissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: acc484ea57ce13d8a7c48a0ca7a2aa8723558dc9
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551046"
---
# <a name="create-approve-and-sign-offers"></a>Tarjousten luominen, hyväksyminen ja allekirjoittaminen

[!include[banner](../includes/banner.md)]

Hakijalle valmisteltava tarjouspaketti on tehtävä usein erittäin nopeasti.
Attractin järjestelmänvalvojan määrittämien mallien käyttö nopeuttaa ja yksinkertaistaa hakijalle lähettävien tarjousten valmistelua.

## <a name="create-an-offer"></a>Tarjouksen luominen

Kun tarjouksen hallintasovellus on otettu käyttöön, jokainen käyttäjä, jonka rooli on työhön ottava esimies tai työhönottaja, voi valmistella hakijan tarjouspaketin. Valmistele tarjous seuraavasti:

1.  Siirry siihen työhön ja hakijan hakemukseen, jolle olet luomassa tarjousta.

1.  Valitse ensin **Tarjousvaihe** ja sitten **Valmistele tarjous**.

    Sinut ohjataan tarjoussovellukseen, jossa hakijan tilana on **Uusi**. Näkyvissä voi olla myös muita tarjouksia, joihin osallistut tarjouksen luojana tai hyväksyjänä.

1.  Valitse **Valmistele tarjous**. 
    
    Näkyviin tulee järjestelmänvalvojan valitsema valikoima erilaisia tarjouspaketteja.

1.  Valitse paketti ja aloita tarjouksen valmistelu valitsemalla **Valmis**.

    Tarjouspakettimalli latautuu, ja tarjoukseen on lisätty työn ja hakijan tiedot.

1.  Kaikki tarjouspakettiin kuuluvat tarjoustietojen paikkamerkit näkyvät saapumissivulla. Voit täyttää paketin kaikki arvot tällä sivulla.

    Purkamisen sivulla näkyy myös kaikkien tarjouksen malleja, jotka kuuluvat tarjouksen paketin.

1.  On mahdollista, että voit nyt muokata tarjouksen sisältöä sen mukaan, miten järjestelmänvalvoja määritti mallin.

1.  Jos haluat poistaa tiedostoja, joita ei ole merkitty pakollisiksi, voit tehdä sen.

1. Kun kaikki tarjoustietojen paikkamerkit on täytetty, tallenna tarjousluonnos valitsemalla **Tallenna**.

>[!NOTE]
> Kun luonnos on tallennettu, voit poistaa tarjouksen luonnosversion tai valita tarvittaessa uuden pakettimallin.


## <a name="approve-an-offer"></a>Tarjouksen hyväksyminen

Useimmissa tarjouksissa käytetään hyväksyntäprosessia, sillä niin voidaan varmistaa, että tarjous on standardien mukainen. Jos tarjous ei vastaa standardeja esimerkiksi silloin, kun tarjouksen luoja ei noudattanut tarjoustietojen sääntöjä ja korvasi tarjouksen arvot, hyväksyntäprosessia noudatetaan. Lähetä tarjous hyväksyttäväksi seuraavasti.

1.  Kun tarjous on luonnostilassa, lisää hyväksyjät **hyväksyjäpaneelissa**. 
    >[!NOTE]
    > Työhön ottavat esimiehet lisätään oletusarvoisesti hyväksyjiksi. Voit tarjouksen hyväksyjäksi kenet tahansa organisaatiossa.

1.  Määritä tarvittaessa peräkkäisen tai rinnakkaisen hyväksyntämenetelmän hyväksyjät. Tämä asetus on käytettävissä vain, jos järjestelmänvalvoja on määrittänyt sen käytettäväksi.
    >[!NOTE]
    > Jos hyväksyntäprosessin on peräkkäinen, voit tarvittaessa muokata hyväksyjäjärjestystä.

1.  Kun olet määrittänyt hyväksyntäketjun, voit muokata hyväksyntäviestin sisältöä ja lähettää sitten ilmoituksen hyväksyjille. Valitse **Lähetä hyväksyjille**.
    >[!NOTE]
    > Jos tarjous ei ole vakiomuotoinen, se on perusteltava.

1.  Jos tarjouksen luoja valitsee hyväksyjän ohittamisen, he voivat lisätä huomautuksen ja siirtyä seuraavaan hyväksyjään.

Hyväksyjät saavat sähköpostiviestin, joka pyytää heitä hyväksymään tarjouksen. He voivat avata tarjouksen sähköpostin linkkiä napsauttamalla, tarkistaa tarjouspaketin ja sitten joko hyväksyä tarjouksen tai lähettää sen takaisin tarjouksen luojalle. Tarjouksen hyväksyjien on lisättävä huomautus, jos he hylkäävät tarjouspaketin, koska sitä on vielä muokattava. 

Jos tarjouksesta luodaan uusi versio, ennen kuin hyväksyjä tekee mitään, hyväksyjä ei voi hyväksyä eikä hylätä tarjousta.

## <a name="offer-versioning"></a>Tarjouksen versiointi 

Kun tarjous on hyväksytty tai lähetetty takaisin muokattavaksi, voit luoda tarjouksesta uuden version valitsemalla **Ota muokkaus käyttöön**. Tarjousversion uudessa versiossa on kaikki tarjouksen edellisestä versiosta siirretyt tietoarvot ja hyväksyjät. 

Hyväksyjät voivat siirtyä tarjousversioiden välillä, jos versiot on jaettu heille hyväksyttäväksi. Hyväksyjä tai tarjouksen luoja voi myös palata edelliseen tilaan poistamalla tietyn tarjouksen luonnosversion.


## <a name="send-an-offer-to-a-candidate"></a>Tarjouksen lähettäminen hakijalle 

Kun tarjous on tallennettu, hyväksytty ja valmis lähetettäväksi hakijalle, valitse **Lähetä ehdokkaalle**.

Voit tehdä useita toimintoja, ennen kuin lähetät tarjouksen hakijalle.
-  Voit tarkastella hakijalle lähetettävään tarjouspakettiin sisältyvien tiedostojen luetteloa.

-  Voit määrittää tarjouksen vanhentumispäivän. Hakijoiden oletetaan hyväksyvän tai hylkäävän tarjouksen ennen vanhentumispäivää.  Hakijalle lähetetään muistutus 48 tuntia ennen tarjouksen vanhentumista.

-  Hyväksyntäprosessiin voi olla mahdollista sisällyttää myös muita asiakirjoja. Voit halutessasi ilmoittaa tarvittavan tiedostotyypin.

- Sähköinen allekirjoitus -asetus: Valitsemasi sähköinen allekirjoituspalvelu voidaan yhdistää kahdella tavalla. Yhdistä **Adobe Sign** tai **DocuSign** valitsemalla **Yhteydet**-kohdassa **Käyttäjäasetukset** **Tarjous**-kohdassa. Vaihtoehtoisesti sinua voidaan pyytää yhdistämään **Lähetä tarjous hakijalle** -sivulle, jos yhteyttä ei ole vielä muodostettu käyttäjäasetusten perusteella. Sähköinen allekirjoitustili tarvitsee yhdistää vain kerran. Samaa käyttäjän käyttöoikeutta käytetään kaikissa tulevissa saman käyttäjän lähettämissä tarjouspaketeissa. 

### <a name="adobe-sign"></a>Adobe Sign
Jos Adobe Sign valittiin ensisijaiseksi sähköiseksi allekirjoitusmenetelmäksi, tarjouksen tekijöiden on yhdistettävä Adobe Sign -käyttöoikeus tässä vaiheessa. 

### <a name="docusign"></a>DocuSign
Jos DocuSign valittiin ensisijaiseksi sähköiseksi allekirjoitusmenetelmäksi, tarjouksen tekijöiden on yhdistettävä DocuSign-käyttöoikeus. Kirjautumisen jälkeen käyttäjän DocuSign-profiiliin liitetyt oletustili ja -käyttöoikeudet on yhdistetty Talent: Attractiin. 

-  Voit tarkastella sähköpostimallia ja muokata sitä tarvittaessa.

Kun tarjous on valmis ja valitset **Lähetä ehdokkaalle**, hakija saa sähköpostitse ilmoituksen, että tarjous odottaa arviointia.

>[!NOTE]
> Jos käytät Adobe Signia tai DocuSignia ja näkyviin tulee virhe, kun tarjousta lähetetään ehdokkaalle, yritä katkaista yhteys sähköisen allekirjoituksen käyttäjätiliin ja muodosta se uudelleen **käyttäjäasetuksissa**. Jos ongelma jatkuu, ota yhteys tukeen käyttämällä **Ilmoita ongelmasta** -linkkiä.

## <a name="candidates-actions-after-receiving-an-offer"></a>Hakijan toimet tarjouksen vastaanottamisen jälkeen

Kun hakijalle on ilmoitettu, että hänelle on jaettu tarjous, hakija voi napsauttaa sähköpostissa olevaa linkkiä ja siirtyä sovelluksen koontinäyttöön katsomaan tarjousta. Hakija näkee koontinäytössä, onko hänellä keskeneräisiä tehtäviä.

1.  Hakija pääsee katsomaan tarjousta ja kaikkia siihen liittyviä asiakirjoja valitsemalla **Näytä tarjous**.

    Hakijat voivat myös ladata tarjouspaketin .zip-tiedostona.

1.  Tarjouksen hyväksymistä varten hakijan on valittava jokaisen tarjouspakettiin kuuluvan asiakirjan kohdalla **Siirry allekirjoitukseen**.

1.  Kun jokainen asiakirja on allekirjoitettu ja hyväksytty, hakijan on lopetettava hyväksyntäprosessi valitsemalla sivun yläosassa **Hyväksy tarjous**.

1.  Jos hakija haluaa hylätä tarjouksen, hänen on valittava ensin sivun yläosassa **Hylkää tarjous** ja sitten sopiva syy, lisättävä tarpeen mukaan kommentti ja valittava lopuksi **Hylkää**.

1.  Hyväksyttyään tai hylättyään tarjouksen hakija voi jäädä tarjousnäkymään tai palata sovelluksen koontinäyttöön.

1.  Jos hyväksyntäprosessin osana on pyydetty muita asiakirjoja, hakijan on valittava tarvittavien asiakirjojen lataaminen ja niiden merkitseminen pyydetyn tiedostotyypin mukaisesti.

1.  Tarjouksen luojalle ilmoitetaan, kun kaikki asiakirjat on ladattu ja tarjouspaketti on allekirjoitettu.


## <a name="withdrawing-an-offer"></a>Tarjouksen peruuttaminen

Hakijalle tehty tarjous voidaan peruuttaa koska tahansa erilaisista syistä. 
1.  Peruuta tarjous napsauttamalla ellipsipainiketta (**…**) ja valitsemalla sitten **Peruuta tarjous**. 

2. Avautuva viesti kysyy, onko hakijalle ilmoitettu tilan muutoksesta. Jos hakijaan ei ole vielä otettu yhteyttä, voit valita sähköpostin lähettämisen hakijalle. Tässä sähköpostiviestissä kerrotaan toiminnoista. 

   Hakija ei voi enää käyttää tarjousta.


## <a name="closing-an-offer"></a>Tarjouksen sulkeminen 

Kun tarjous on hyväksytty, hylätty tai peruutettu eikä lisätoimintoja tarvita, voit sulkea tarjouksen, jolloin kyseiseen tarjouspakettiin ei voi tehdä enää muutoksia.
