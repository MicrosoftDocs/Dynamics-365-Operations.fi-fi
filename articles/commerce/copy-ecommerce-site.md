---
title: Sähköisen kaupankäynnin sivuston kopioiminen
description: Tässä aiheessa kuvataan, kuinka voit kopioida aiemmin luodun sähköisen kaupankäynnin sivuston sähköisen kaupankäynnin ympäristön sisällä tai ympäristöjen välillä Microsoft Dynamics 365 Commerce -sivustonmuodostajassa.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 284a33099fecc5a8e8d5d5d31612abab51735773
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8386977"
---
# <a name="copy-an-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston kopioiminen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan, kuinka voit kopioida aiemmin luodun sähköisen kaupankäynnin sivuston sähköisen kaupankäynnin ympäristön sisällä tai ympäristöjen välillä Microsoft Dynamics 365 Commerce -sivustonmuodostajassa.

Dynamics 365 Commerce tukee sivustojen kopioimista tai kloonaamista itsepalvelutoiminnointina Commerce-sivustonmuodostimessa. Sivustot voidaan kopioida yhdessä verkkokauppaympäristössä tai kahden sähköisen kaupankäyntiympäristön välillä. Sivuston kopiointitoiminnon aloittavan käyttäjän on oltava vuokraajan järjestelmänvalvoja sekä lähde- että kohdeverkkokauppaympäristössä.

Sivuston kopiotoiminto kopioi kaikki lähdesivuston sähköisen kaupankäynnin tiedot. Tämä sisältö sisältää sivut, katkelmat, mallit, URL-osoitteet ja resurssit. Ennen kuin uutta sivustoa voi käyttää, se on alustettava ensimmäisen suorituskerran FRE (first run experience) -prosessin avulla. Kanavia voi määrittää ja hallita sivustonmuodostimessa kohdassa **Sivuston asetukset \> Kanavat**.

Sivuston kopiointitoiminnon kesto määräytyy ensisijaisesti lähdesivuston resurssien määrän mukaan. Tavallista suuremmissa sivustoissa suosittelemme, että harkitset ympäristön kopiointitoiminnon käyttöä sen sijaan. (Tätä työvaihetta kutsutaan myös tietojen siirrettävyyden työvaiheeksi).

> [!NOTE]
> - Lähdesivusto on vain luku -tilassa sivuston kopiointitoiminnon ajan.
> - Vain julkaisut tiedostoversiot kopioidaan. Jos versioita ei ole julkaistu, vain uusimmat versiot kopioidaan.
> - Sisällön versiohistoria ei ole käytettävissä kohdesivustossa.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Sivuston kopioiminen sähköisen kaupankäynnin ympäristön sisällä

Voit kopioida sivuston sähköisen kaupankäynnin ympäristön sisällä noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään sen ympäristön sivustonmuodostajaan, jossa haluat suorittaa kopiointitoiminnon.
1. Avaa sivustoluettelonäkymän valitsemalla oikeasta yläkulmasta **Sivuston valitsin** ja valitsemalla sitten **Sivustojen hallinta**.
1. Etsi sivustoista ja valitse kopioitavan tai kloonattavan sivuston vieressä valintaruutu.
1. Valitse toimintoruudussa **Kopioi sivusto**.
1. Anna uuden sivuston nimi **Kopioi sivusto** -valintaikkunan **Uuden sivuston nimi** -kenttään. Uuden sivuston nimen on oltava yksilöivä sähköisen kaupankäynnin ympäristössä. **Lähdevuokraaja**- ja **Lähdesivusto**-kenttiin määritetään automaattisesti nykyisen vuokraajan ja valitun sivuston tiedot.
1. Valitse **Luo kopio**.

Kun tiedot on vahvistettu, ilmoitus ilmaisee, että uusi sivuston kopio on luotu. Voit valvoa työn etenemistä [**Vuokraajan työt** -sivun oikeanpuoleisessa ruudussa](#monitor-the-site-copy-operation). Kun kopiointitoiminto on suoritettu onnistuneesti loppuun, uusi sivusto tulee näkyviin sivustojen luetteloon sivustoluettelonäkymässä.

Seuraavassa kuvassa näkyy esimerkki **Kopioi sivusto**- valintaikkunasta sivustonmuodostimessa.

![Kopioi sivusto -valintaruutu sivuston luontiohjelmassa.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Sivuston kopioiminen kahden eri sähköisen kaupankäynnin ympäristön välillä

Voit kopioida sivuston kahden sähköisen kaupankäynnin ympäristön välillä noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään sivuston luontiohjelmaan sähköisen kaupankäynnin kohdeympäristössä.
1. Valitse toimintoruudussa **Kopioi sivusto**.
1. Anna uuden sivuston nimi **Kopioi sivusto** -valintaikkunan **Uuden sivuston nimi** -kenttään. Uuden sivuston nimen on oltava yksilöivä sähköisen kaupankäynnin ympäristössä.
1. Valitse **Lähdevuokraaja**-kentässä lähdevuokraaja.
1. Valitse **Lähdesivusto**-kentässä lähdesivusto.
1. Valitse **Luo kopio**.

> [!NOTE]
> Vuokraajan järjestelmänvalvojan käyttöoikeudet tarvitaan sekä sähköisen kaupankäynnin lähde- että kohdeympäristöissä.

Kun tiedot on vahvistettu, ilmoitus ilmaisee, että uusi sivuston kopio on luotu. Voit valvoa työn etenemistä [**Vuokraajan työt** -sivun oikeanpuoleisessa ruudussa](#monitor-the-site-copy-operation). Kun kopiointitoiminto on suoritettu onnistuneesti loppuun, uusi sivusto tulee näkyviin sivustojen luetteloon sivustoluettelonäkymässä.

## <a name="monitor-the-site-copy-operation"></a>Sivuston kopiointitoiminnon valvominen

Noudattamalla seuraavia ohjeita voit valvoa sivuston kopiointitoiminnon etenemistä.

1. Kirjaudu sisään sivuston luontiohjelmaan sähköisen kaupankäynnin kohdeympäristössä.
1. Valitse vasemmanpuoleisessa ruudussa **Vuokraajan työt**.
1. Etsi ja valitse luettelosta sivuston kopiointityö **Vuokraajan työt** -sivulla. Oikealla puolella näkyy ruutu, joka sisältää valitun työn tilan ja tiedot.

Voit peruuttaa työn, jonka tila on **Käynnissä**. Valitse työ luettelosta ja valitse sitten toimintoruudussa **Peruuta**.

Voit yrittää uudelleen työtä, jonka tila on **Epäonnistunut** tai **Valmis, sisältää virheitä**. Valitse työ luettelosta ja valitse sitten toimintoruudussa **Yritä uudelleen**.

> [!NOTE]
> Videoresurssien käsittely saattaa jatkua, kun sivuston kopiointityö on valmis.

Seuraavassa kuvassa näkyy **Vuokraajan työt** -sivun oikeanpuoleinen ruutu sivuston luontiohjelmassa.

![Työn tiedot sivuston muodostimen Vuokraajan työt -sivun oikeanpuoleisessa ruudussa.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Uuden sivuston alustaminen FRE-prosessin avulla

Ennen kuin uutta sivustoa voi käyttää, se on alustettava ensimmäisen suorituskerran FRE-prosessin avulla.

Kun haluat alustaa uuden sivuston FRE-prosessia käyttäen, noudata seuraavia ohjeita.

1. Kirjaudu sivustonmuodostajaan uutta sivustoa varten.
1. Avaa sivustoluettelonäkymän valitsemalla oikeasta yläkulmasta **Sivuston valitsin** ja valitsemalla sitten **Sivustojen hallinta**.
1. Etsi ja valitse alustettava uusi sivusto.
1. Valitse toimialue **Määritä sivusto** -valintaikkunan **Valitse toimialue** -kentästä. Kaikki alustuksen aikana sähköiseen kaupankäynnin ympäristöön liitetyt toimialueet ovat valittavissa.
1. Valitse **Valitse oletuskanava** -kentässä liittyvä verkkokauppakanava. Valittu kanava tarjoaa valikoimia ja muita Commerce Headquarters -sovellukseen tallennettuja tietoja.
1. Valitse **Valitse oletuskieli** -kentästä laatimisen oletuskieli. Kaikki valitulle verkkokauppakanavalle määritetyt kielet ovat valittavissa.
1. **Polku**-kentässä arvo koostuu perustoimialueesta ja valinnaisesta URL-polusta, jonka voit syöttää. Voit jättää URL-polun tyhjäksi, jos kanava avataan toimialueen juurihakemistosta tai jos haluat syöttää nämä tiedot myöhemmin sivustonmuodostimen kanavan konfiguraationäkymässä. Sivuston polun on oltava yksilöivä sähköisen kaupankäynnin ympäristössä.
1. Valitse **OK**. Sivuston alustus sisältää toimittamasi tiedot ja siirryt sivuston hallintanäkymään.

Seuraavassa kuvassa näkyy esimerkki **Määritä sivusto**- valintaikkunasta sivustonmuodostimessa.

![Määritä sivusto -valintaikkuna sivuston luontiohjelmassa.](media/site-copy_3.png)

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-b2c-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
