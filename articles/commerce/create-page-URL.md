---
title: Sivun URL-osoitteen luominen
description: Tässä artikkelissa kerrotaan sivuston URL-osoitteiden luomisen peruskäsitteistä ja proseduureista.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8718a3a2854ecdc7aec0853569dcba9e26a86d67
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270151"
---
# <a name="create-a-page-url"></a>Sivun URL-osoitteen luominen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan sivuston URL-osoitteiden luomisen peruskäsitteistä ja proseduureista.

Täydellinen tai absoluuttinen URL-osoite, joka osoittaa sivuston tietyt osat sisältävälle sivulle. Esimerkiksi URL-osoitteessa `https://www.contoso.com/en-us/contactus` on seuraavat osat:

- `https://www.contoso.com` – HTTP-protokolla ja sivuston toimialue.
- `/en-us` – Sivuston kielipolku.
- `/contactus` – **Ota yhteyttä** -sivun relatiivinen URL-osoite. Suhteellinen URL-osoite tunnetaan myös nimellä URL-osoitteen *kuvaava osa*.

Voit määrittää sivuston toimialueen ja valinnaisen kielipolun sivuston määrittämisen yhteydessä. Voit lisätä sivustoon toimialueita ja kielipolkuja sivuston asetusten verkkokauppasivun avulla.

Sivun URL-osoitteen kuvaava osa on olemassa yksittäisenä entiteettinä sivuston muokkausympäristössä. Sivun URL-osoite koostuu kahdesta osasta: nimi, joka edustaa URL-osoitteen kuvaavaa osaa ja sivun osoittimesta omassa sivustossa tai ulkoisessa sivustossa. Sivun URL-osoite voidaan määrittää myös niin, että se välittää käyttäjän toiselle sivulle omassa sivustossa tai ulkoisessa sivustossa.

## <a name="create-a-page-url"></a>Sivun URL-osoitteen luominen

Sivun URL-osoitteita voi luoda kahdella seuraavalla tavalla:

- Automaattisesti sivun luomisen yhteydessä
- Manuaalisesti **URL-osoitteet**-sivulla

### <a name="create-a-page-url-when-you-create-a-page"></a>Sivun URL-osoitteen luominen sivun luomisen yhteydessä

Jos annat nimen **URL-osoite**-kenttään uuden sivun luomisen yhteydessä, sivulle osoittava sivun URL-osoite luodaan automaattisesti **URL-osoitteet**-sivulla. Kun URL-osoite ja sivu, johon se osoittaa, on julkaistu, sivuston käyttäjät (asiakkaat) voivat käyttää URL-osoitteeseen liitettyä sivua.

> [!NOTE]
> Jos julkaiset URL-osoitteen ilman sen sivun julkaisemista, johon osoite osoittaa, sivuston käyttäjille näytetään 404-virhe, kun he yrittävät käyttää sivua. Jos julkaiset sivun ilman sen URL-osoitteen julkaisemista, johon sivu osoittaa, sivua ei voi käyttää URL-osoitteen avulla.

### <a name="manually-create-a-page-url"></a>Sivun URL-osoitteen manuaalinen luominen

Kun luotu uusia sivuja, sinun ei tarvitse määrittää tiettyä sivun URL-osoitetta. Jos jätät URL-osoite-kentän tyhjäksi, sivu luodaan ilman linkkejä. Tällöin asiakkaat eivät voi käyttää sivua vaikka se olisi julkaistu. Jotta sivu olisi käytettävissä, sinun on luotava URL-osoite manuaalisesti ja linkitettävä se sivulle.

Voit luoda sivun URL-osoitteen manuaalisesti seuraavasti.

1. Valitse **URL-osoitteet**-sivulla **Uusi**.
1. Valitse sivuston sivu, joka liitetään URL-osoitteeseen.
1. Kirjoita URL-osoitteen kuvaava osa ja valitse **OK**.

Tässä vaiheessa URL-osoite on luonnostilassa. Se on julkaistava, ennen kuin sivuston käyttäjät voivat käyttää liittyvää sivua.

## <a name="update-a-page-url"></a>Sivun URL-osoitteen päivittäminen

Voit päivittää sivun URL-osoitteen kohdesivun seuraavasti.

1. Valitse **URL-osoitteet**-sivulla päivitettävä URL-osoite.
1. Valitse oikeanpuoleisessa ominaisuusruudussa kohdesivun kentän vieressä oleva kolmen pisteen painike (**...**).
1. Valitse valintaikkunassa toinen sivu ja valitse sitten **OK**.
1. Tallenna ja julkaise URL-osoite.

## <a name="redirect-a-page-url"></a>Sivun URL-osoitteen uudelleenohjaus

Joskus asiakkaat on hyvä ohjata eri sivulle kuin sille, jonka URL-osoitteen he valitsevat. Tällöin paras ja helpoin tapa on usein muuttaa sivua, johon sivun URL-osoite osoittaa. Voit kuitenkin perustellusti käyttää HTTP 301- tai 3023-uudelleenohjauksia ja ohjata URL-osoitteen pyynnöt toiseen URL-osoitteeseen.

Voit ohjata URL-osoitteen toiseen URL-osoitteeseen seuraavasti.

1. Valitse **URL-osoitteet**-sivulla päivitettävä URL-osoite.
1. Valitse oikealla olevassa ominaisuusruudussa **Ohjaa uudelleen**.
1. Valitse uudelleenohjauksen kohde seuraavasti:

    - Jos haluat osoittaa sivuston toiseen sivuun, valitse **Sisäinen URL-osoite**. Valitse kolmen pisteen painike (**...**) ja valitse sitten uudelleenohjattava URL-osoite.
    - Voit osoittaa ulkoisen sivuston sivuun valitsemalla **Ulkoinen URL-osoite** ja syöttämällä kyseisen sivun täydellisen URL-osoitteen. Varmista, että sisällytät protokollan. Syötä arvoksi esimerkiksi `https://domain.com/new/page`. Jos URL-osoite ohjaa jo uudelleen sisäiseen URL-osoitteeseen, valitse **Tyhjennä valinta**, ennen kuin syötät ulkoisen URL-osoitteen.

1. Valitse uudelleenohjauksen tyyppi seuraavasti:

    - **Pysyvä uudelleenohjaus (301)** – Valitse tämä vaihtoehto, kun tiedät, että sisältösi liikkuu pysyvästi eikä palaa aiempaan URL-osoitteeseen. Hakukoneet määrittävät uudelleenohjauksen URL-osoitteen hakukoneoptimoinnin arvon URL-osoitteelle. joka uudelleenohjataan. Se myös päivittää uuden URL-osoitteen niiden tietueeseen. 
    - **Väliaikainen uudelleenohjaus (302)** – Valitse tämä vaihtoehto, jos haluat uudelleenohjata liikenteen päivittämättä hakukoneita. Tätä menetelmää käytetään yleensä, jos sisältö palaa pian edelliseen URL-osoitteeseen.

1. Kun olet valmis toteuttamaan uudelleenohjauksen, tallenna ja julkaise URL-osoite.

## <a name="additional-resources"></a>Lisäresurssit

[Sivuston selauksen mukauttaminen](customize-site-navigation.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
