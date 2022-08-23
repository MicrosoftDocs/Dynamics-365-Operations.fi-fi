---
title: Tyylien esimääritysten käyttäminen
description: Tässä artikkelissa käsitellään sivuston tyylin esiasetuksia Microsoft Dynamics 365 Commercen sivustotyökalussa.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ea22c4c50a25c18d25980b8d2ce9bcf8cd315e87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267509"
---
# <a name="work-with-style-presets"></a>Tyylien esimääritysten käyttäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään sivuston tyylin esiasetuksia Microsoft Dynamics 365 Commercen sivustotyökalussa.

Tyylin esimääritys on tallennettu joukko kaikkia sivuston teemaan tallennettuja tyyliarvoja. Sen avulla voidaan välittömästi muuttaa sivuston ulkoasua sivustonmuodostustyökalun avulla. Tyylien esimääritykset antavat Commercen sivustonmuodostustyökalun kirjoittajien muuttaa, esikatsella ja aktivoida tyyliarvoja koko sivustollaan ilman CSS-tyylisivuja (CSS) tai teemojen käyttöönottoa. Kirjasintyylit, painiketyylit ja sivuston värit ovat tyypillisiä esimerkkejä tyylimuuttujista, joita voidaan hallita tyylien esimääritysten avulla.

Sivustossa käytettävissä olevat tyylimuuttujat määräytyvät sivuston vuokralaiselle käyttöönotettavan teeman ja moduulikirjaston mukaan. Dynamics 365 Commerce Online Software Development Kit (SDK) sallii kehittäjien toteuttaa niin monta (tai vähän) kirjoitettavaa tyylimuuttujaa kuin ne vaativat tietylle teemalle. Ottamalla käyttöön lisää tyylimuuttujia teeman kehittäjä voi tehdä lopullisia valintoja sivustotyyleistä sivustonmuodostustyökalun tekijöiden käsiin. Tämän vuoksi muut kuin kehittäjät voivat päivittää ja esikatsella sivustotyylejä käyttämällä työkalusarja-toimintoa. Ominaisuus on hyödyllinen myös kaikissa tilanteissa, joissa suorat muutokset teemoihin tai CSS:ssään aiheuttavat tarpeettomia yleiskustannuksia.

Teemat, joissa kirjoitettavat tyylimuuttujat on otettu käyttöön, edellyttävät oletusarvon mukaista tyylin esimääritystä. Ne voivat valinnaisesti lisätä valmiiksi määritettyjä asetuksia osana käyttöönotettua teemapakettia. Voit esimerkiksi ottaa käyttöön teeman, jossa on yksi oletusarvoinen "moderni valo" -tyylin esimääritys. Vaihtoehtoisesti se voi olla myös muita oletusasetuksia, kuten "moderni tumma", "vintage-valo" tai "vintage tumma". Nämä sisäiset teeman esimääritykset ovat kehittäjien luomia, ja niitä voidaan käyttää uusien sivustomallien aloituspisteinä.

Sivustonmuodostimessa tekijät voivat valita teeman valmiiden esimääritysten joukosta, tai he voivat luoda omia tyylin esimäärityksiä ja mukautuksia käyttämällä käytössä olevien tyylien muuttujia. Tyylin esimääritys voidaan esikatsella sivustonmuodostimessa, ennen kuin se aktivoidaan Live-sivustossa. Kun tekijän tyylin muutokset on tarkistettu, tyylin esimäärityksen tilaksi voidaan määrittää "aktiivinen" Live-sivustossa.

## <a name="preview-a-style-preset"></a>Tyylin esimäärityksen esikatselu

Voit esikatsella sivuston tyylin esimääritystä sivustonmuodostimessa seuraavasti.

1. Siirry sivuston vasemmassa siirtymisruudussa kohtaan **Sivuston asetukset \> Suunnittelu**.
1. Valitse muotoilueditorin yläosan **tyylin esimääritykset** -välilehdestä **käytettävissä olevat esimääritykset** -luettelosta haluamasi esimääritys ja esimääritys siirry sitten editoriin valitsemalla **Näytä**.

    Jos **käytettävissä olevat esimääritykset** -luettelossa ei ole esiasetuksia, lisätietoja [mukautettujen tyylien esimääritysten luomisesta](#create-a-custom-style-preset) on kohdassa mukautetun tyylin esimäärityksen luominen.

    > [!NOTE]
    > Teemaan sisältyvät esimääritykset osoitetaan **sisäisellä** merkillä. Nämä valmiit esimääritykset ovat vain luku -muotoisia. Jos haluat kopioida valmiin esimäärityksen uudeksi mukautetuksi esimääritykseksi, valitse esimääritykselle kolme pistettä sisältävä painike (**...**) ja valitse sitten **Tallenna nimellä**.

1. Valitse komentopalkissa **Esikatsele**.
1. Valitse sivuston URL-osoite, jota käytetään tyylin esimääritysten esikatseluun, ja valitse sitten **OK**.
1. Valitse esikatseltava kanava- ja kielikohtainen URL-variantti valitsemalla muuttujan nimi. Näyttöön avautuu uusi esikatseluselainikkuna, jossa valitun tyylin esimääritystä käytetään määritetylle sivulle.

> [!NOTE]
> Esikatselun URL-osoite on pysyvä ja todennettu. Tämän vuoksi voit kopioida, liittää ja lähettää sen tarkistettavaksi muille todennetuille työtovereille ennen kuin määrität sen aktiiviseksi Live-sivustoosi. Esikatselun URL-osoite on hyödyllinen myös eri laitteiden, eri selainten ja eri näyttöjen tyylien tarkistamiseen.

> [!TIP]
> Kun muokkaat tyylin esimääritystä, voi olla hyödyllistä jättää esikatseluselainikkuna auki erillisessä selainikkunassa, jotta voit tarkistaa tekemäsi muutokset nopeasti. Kun olet tallentanut muutokset esimäärityksiin, päivitä avoin esikatseluselainikkuna, jossa käyttäjäkokemus tarkistetaan.

## <a name="create-a-custom-style-preset"></a>Mukautetun tyylin esimäärityksen luominen

Luo mukautettu tyylin esimääritys sivustonmuodostimessa seuraavasti.

1. Siirry sivuston vasemmassa siirtymisruudussa kohtaan **Sivuston asetukset \> Suunnittelu**.
1. Valitse suunnittelueditorin yläosan **tyylin esimääritykset** -välilehdestä **Uusi esimääritys**.
1. Kirjoita uuden esimäärityksen nimi ja kuvaus ja valitse sitten **Tallenna**. Luodaan uusi mukautettava esimääritys, joka käyttää teeman oletusarvoja lähtökohtana.

> [!NOTE]
> Voit myös luoda uuden mukautetun tyylin esimäärityksen mistä tahansa valmiista esimäärityksistä valitsemalla kolmen pisteen painikkeen (**...**) ja valitsemalla sitten **Tallenna nimellä**. Vaihtoehtoisesti, valitse **Tallenna nimellä** esimääritetyn editorin komentopalkissa.

## <a name="modify-global-and-module-type-style-values"></a>Yleisten ja moduulityyppien tyylienarvojen muokkaaminen

Jotkin teeman tyylimuuttujat jaetaan useiden moduulityyppien kesken. Näitä tyylimuuttujia kutsutaan *yleisiksi* tyylimuuttujiksi. Esimerkkejä ovat ensisijaiset sivuston värit, oletusfonttityylit ja painiketyylit. Määrittämällä yleisiä muuttujia voit muuttaa ulkoasua useissa eri moduulityypeissä.

Jotkin tyyliarvot voivat olla moduulityypin yksilöiviä, tai niiden on ehkä halutessasi ohitettava yleinen oletusarvo. Jos sivuston teema on ottanut moduulityypin tyylimuuttujat käyttöön, sivustonmuodostimen käyttäjät voivat mukauttaa moduulityypin tyylin yleisasetuksista riippumatta. Moduulin tyyppimuuttujat voivat joko lisätä tai ohittaa teeman yleisiä tyylimuuttujia.

> [!NOTE]
> Sivuston tyyliarvojen hierarkia käyttäytyy seuraavalla tavalla. Kauemmaksi oikealle tulevat tyyliarvot ohittavat tyyliarvot niiden vasemmalla puolella.
>
> Teeman oletusarvot \< Yleiset tyyliarvot \< Moduulityyppityyliarvot \< CSS-ohitus

Jos haluat muuttaa tyylin esimäärityksen yleisiä tai moduulityypin arvoja sivustonmuodostimessa, toimi seuraavasti.

1. Siirry sivuston vasemmassa siirtymisruudussa kohtaan **Sivuston asetukset \> Suunnittelu**.
1. Valitse suunnittelueditorin yläosan **tyylin esimääritykset** -välilehdestä **Näytä**, jos haluat siirtyä esimäärityseditoriin.
1. Valitse **Esikatselu** ja avaa sitten esimäärityksen koko selainikkunan esikatselu noudattamalla URL-osoitteen valintaohjeita. Jätä tämä esikatseluselainikkuna avoimeksi.
1. Valitse esimäärityseditorissa **Muokkaa** oikeassa yläkulmassa.
1. Editorin tyylimuuttuja-ohjausobjektien avulla voit muuttaa joitakin yleisiä tyyliarvoja.
1. Valitse editorin yläosassa **Yleinen**-välilehden **moduulit**-välilehdestä moduulityyppi, jonka on oltava tyylitelty.
1. Voit muuttaa joitakin moduulityypin arvoja tyyliohjausobjektien avulla.
1. Kun olet valmis esikatselemaan muutoksia, valitse komentopalkissa **Tallenna**.
1. Palaa avaa esikatseluselainikkunaan ja päivitä se. Koko selainikkunan esikatselu on kätevä tapa tarkistaa tyylin muutokset eri näkymän keskeytyskohdissa, eri selaimissa ja eri laiteympäristöissä.
1. Kun kaikki muutokset on tehty ja vahvistettu, valitse editorin oikeasta yläkulmasta **valmis muokkaus**.

> [!NOTE]
> Jos muokkaat sivustossa tällä hetkellä aktiivisena olevaa esimääritystä, editorissa näkyy sininen **Aktiivinen**-merkki. Tämä merkki ilmaisee, että esimääritys on tällä hetkellä toiminnassa sivustossasi. Jos muutat aktiivista esimääritystä, paina **Julkaise**-painiketta, jos haluat siirtää muutokset Live-sivustoosi.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Uuden tyylin esimäärityksen luominen Live-sivustossa

Jos haluat määrittää tyylin esimäärityksen sivuston uudeksi aktiiviseksi esimääritykseksi, toimi seuraavasti.

- Valitse **Aseta aktiiviseksi painikkeeksi** jossakin seuraavista paikoista:

    - Komentopalkki tyylin esimäärityseditorissa
    - Kaikkien käytettävissä olevien esimääritysten valikko (**...**), jonka päänäkymässä on **tyylin esimääritykset** -välilehti kohdassa **sivuston asetukset \> suunnittelu**

Esimääritysten tyyliarvot ovat aktiivisia julkisessa sivustossa.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
